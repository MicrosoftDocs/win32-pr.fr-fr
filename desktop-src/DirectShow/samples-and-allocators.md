---
description: Exemples et allocators
ms.assetid: 1fbea741-f29a-4815-9885-94ca9cf4bb95
title: Exemples et allocators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9132ff2c70b5ade63f8853b5c03bacb7a25371
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104561978"
---
# <a name="samples-and-allocators"></a>Exemples et allocators

Lorsqu’un code PIN transmet des données multimédia à un autre code confidentiel, il ne passe pas de pointeur direct vers la mémoire tampon. Au lieu de cela, il fournit un pointeur vers un objet COM qui gère la mémoire. Cet objet, appelé *exemple de support*, expose l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Le code PIN de réception accède à la mémoire tampon en appelant des méthodes **IMediaSample** , telles que [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer), [**IMediaSample ::**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)deIMediaSample et [**GetActualDataLength ::**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength).

Les exemples voyagent toujours en aval, de la broche de sortie à la broche d’entrée. Dans le modèle push, la broche de sortie fournit un exemple en appelant [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée. La broche d’entrée traite les données de manière synchrone (c’est-à-dire complètement à l’intérieur de la méthode de **réception** ), ou les traite de façon asynchrone sur un thread de travail. La broche d’entrée est autorisée à bloquer dans la méthode **Receive** , si elle doit attendre des ressources.

Un autre objet COM, appelé *Allocator*, est responsable de la création et de la gestion des exemples de médias. Les allocateurs exposent l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Chaque fois qu’un filtre a besoin d’un échantillon de média avec une mémoire tampon vide, il appelle la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , qui retourne un pointeur vers l’exemple. Chaque connexion de code confidentiel partage un allocateur. Lorsque deux codes confidentiels se connectent, ils décident du filtre qui fournira l’allocateur. Les broches définissent également des propriétés sur l’allocateur, telles que le nombre de mémoires tampons et la taille de chaque mémoire tampon. (Pour plus d’informations, consultez [Comment les filtres se connectent](how-filters-connect.md) et [négocient des allocateurs](negotiating-allocators.md).)

L’illustration suivante montre les relations entre l’allocateur, les exemples de média et le filtre.

![exemples de supports et allocators](images/mediasamples.png)

**Exemples de références de média**

Un allocateur crée un pool fini d’exemples. À tout moment, certains exemples peuvent être utilisés, tandis que d’autres sont disponibles pour les appels **GetBuffer** . L’allocateur utilise le comptage de références pour effectuer le suivi des exemples. La méthode **GetBuffer** retourne un exemple avec un nombre de références de 1. Si le décompte de références atteint zéro, l’exemple repasse dans le pool de l’allocateur, où il peut être utilisé lors de l’appel **GetBuffer** suivant. Tant que le décompte de références reste au-dessus de zéro, l’exemple n’est pas disponible pour **GetBuffer**. Si chaque exemple appartenant à l’allocateur est en cours d’utilisation, la méthode **GetBuffer** se bloque jusqu’à ce qu’un exemple devienne disponible.

Supposons, par exemple, qu’une broche d’entrée reçoit un exemple. S’il traite l’exemple de façon synchrone, à l’intérieur de la méthode **Receive** , il n’incrémente pas le nombre de références. Une fois la **réception** retournée, la broche de sortie libère l’exemple, le décompte de références atteint zéro et l’exemple retourne au pool de l’allocateur. En revanche, si la broche d’entrée traite l’exemple sur un thread de travail, elle incrémente le nombre de références avant de quitter la méthode de **réception** . Le décompte de références est maintenant 2. Lorsque la broche de sortie libère l’exemple, le nombre atteint 1 ; l’exemple ne retourne pas encore dans le pool. Une fois que le thread de travail est terminé avec l’exemple, il appelle **Release** pour libérer l’exemple. À présent, l’exemple retourne au pool.

Lorsqu’un code confidentiel reçoit un échantillon, il peut copier les données vers un autre exemple, ou il peut modifier l’exemple d’origine et remettre celui-ci au filtre suivant. Peut-être qu’un exemple parcourt la longueur totale du graphique, chaque filtre appelant **AddRef** et **Release** à son tour. Par conséquent, la broche de sortie ne doit jamais réutiliser un exemple après avoir appelé **Receive**, car un filtre en aval peut utiliser l’exemple. La broche de sortie doit toujours appeler **GetBuffer** pour obtenir un nouvel exemple.

Ce mécanisme réduit la quantité d’allocation de mémoire, car les filtres réutilisent les mêmes tampons. Il empêche également les filtres d’écrire accidentellement des données qui n’ont pas été traitées, car l’allocateur gère une liste d’exemples disponibles.

Un filtre peut utiliser des allocateurs distincts pour l’entrée et la sortie. Cela peut se faire si elle développe les données d’entrée (par exemple, en les décompressant). Si la sortie n’est pas supérieure à l’entrée, un filtre peut traiter les données en place, sans les copier dans un nouvel exemple. Dans ce cas, deux ou plusieurs connexions de code confidentiel peuvent partager un allocateur.

**Validation et dévalidation des allocateurs**

Lorsqu’un filtre crée d’abord un allocateur, il n’a pas réservé de mémoire tampon. À ce stade, tous les appels à la méthode **GetBuffer** échouent. Lors du démarrage de la diffusion en continu, la broche de sortie appelle [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit), qui valide l’allocateur, provoquant l’allocation de mémoire. Les broches peuvent désormais appeler **GetBuffer**.

Lorsque la diffusion en continu s’arrête, le code PIN appelle [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit), qui annule l’allocation. Tous les appels suivants à **GetBuffer** échouent jusqu’à ce que l’allocateur soit de nouveau validé. En outre, si des appels à **GetBuffer** sont bloqués actuellement en attente d’un exemple, ils retournent immédiatement un code d’échec. La méthode de **dévalidation** peut ou non libérer la mémoire, en fonction de l’implémentation. Par exemple, la classe [**CMemAllocator**](cmemallocator.md) attend que sa méthode de destructeur libère de la mémoire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 
