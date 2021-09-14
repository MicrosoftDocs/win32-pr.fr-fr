---
description: Négociation des allocateurs
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Négociation des allocateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2faa393ba9fcd8585d68947cec172d4cfca6decf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223236"
---
# <a name="negotiating-allocators"></a>Négociation des allocateurs

Lorsque deux codes confidentiels se connectent, ils ont besoin d’un mécanisme d’échange de données multimédias. Ce mécanisme est appelé le *transport*. en général, l’architecture DirectShow est neutre sur les transports. Deux filtres peuvent accepter de se connecter à l’aide des transports pris en charge par les deux.

Le transport le plus courant est le transport de *mémoire local* , dans lequel les données multimédias résident dans la mémoire principale. Il existe deux versions de transport de mémoire locale, le *modèle push* et le *modèle pull*. Dans le modèle push, le filtre source transmet les données au filtre en aval, à l’aide de l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sur la broche d’entrée du filtre en aval. Dans le modèle d’extraction, le filtre en aval demande des données à partir du filtre source, à l’aide de l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sur la broche de sortie du filtre source. pour plus d’informations sur ces deux modèles de transmission de données, consultez [Flow de données dans le Graph de filtre](data-flow-in-the-filter-graph.md).

Dans le transport de mémoire locale, l’objet chargé d’allouer des mémoires tampons est appelé *Allocator*. Un allocateur prend en charge l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Les deux broches partagent un seul allocateur. L’un ou l’autre des codes confidentiels peut fournir un allocateur, mais la broche de sortie sélectionne l’allocation à utiliser.

La broche de sortie définit également les propriétés Allocator, qui déterminent le nombre de mémoires tampons créées par l’allocateur, la taille de chaque mémoire tampon et l’alignement de la mémoire. La broche de sortie peut déférer à la broche d’entrée pour les exigences de mémoire tampon.

Dans une connexion **IMemInputPin** , la négociation d’allocateur fonctionne comme suit :

1.  Le cas échéant, la broche de sortie appelle [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements). Cette méthode récupère les exigences de mémoire tampon du code confidentiel d’entrée, telles que l’alignement de la mémoire. En général, la broche de sortie doit honorer la demande du code confidentiel d’entrée, à moins qu’il y ait une bonne raison de ne pas le faire.
2.  Le cas échéant, la broche de sortie appelle [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator). Cette méthode demande un allocateur à partir de la broche d’entrée. La broche d’entrée en fournit une ou retourne un code d’erreur.
3.  La broche de sortie sélectionne un allocateur. Il peut en utiliser un fourni par la broche d’entrée ou créer son propre code.
4.  La broche de sortie appelle [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) pour définir les propriétés Allocator. Toutefois, l’allocateur peut ne pas honorer les propriétés demandées. (Par exemple, cela peut se produire si la broche d’entrée fournit l’allocateur.) L’allocateur retourne les propriétés réelles sous la forme d’un paramètre de sortie dans la méthode **SetProperties** .
5.  Outpin appelle [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) pour informer la broche d’entrée de la sélection.
6.  La broche d’entrée doit appeler [**IMemAllocator :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) pour vérifier si les propriétés Allocator sont acceptables.
7.  La broche de sortie est chargée de la validation et de la désactivation de l’allocateur. Cela se produit lorsque la diffusion en continu démarre et s’arrête.

Dans une connexion **IAsyncReader** , la négociation d’allocateur fonctionne comme suit :

1.  La broche d’entrée appelle [**IAsyncReader :: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) sur la broche de sortie. La broche d’entrée spécifie ses exigences en matière de mémoire tampon et, éventuellement, fournit un allocateur.
2.  La broche de sortie sélectionne un allocateur. Il peut utiliser celui fourni par la broche d’entrée, le cas échéant, ou créer son propre code.
3.  La broche de sortie retourne l’allocateur en tant que paramètre sortant dans la méthode **RequestAllocator** . La broche d’entrée doit vérifier les propriétés de l’allocateur.
4.  La broche d’entrée est chargée de la validation et de la désactivation de l’allocateur.
5.  À tout moment pendant le processus de négociation de l’allocateur, le code pin peut faire échouer la connexion.
6.  Si la broche de sortie utilise l’allocateur de la broche d’entrée, elle peut utiliser cet allocateur uniquement pour fournir des échantillons à cette broche d’entrée. Le filtre propriétaire ne doit pas utiliser l’allocateur pour remettre des échantillons à d’autres broches.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fourniture d’un allocateur personnalisé](providing-a-custom-allocator.md)
</dt> </dl>

 

 



