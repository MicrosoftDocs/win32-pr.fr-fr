---
description: vue d’ensemble des Flow de données dans DirectShow
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: vue d’ensemble des Flow de données dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b755b9472690913cf8a53d2c7a8575111e336e54a81835438aa8cc9e959ed5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107641"
---
# <a name="overview-of-data-flow-in-directshow"></a>vue d’ensemble des Flow de données dans DirectShow

Cette section fournit une vue d’ensemble générale du fonctionnement du workflow de données dans DirectShow. Vous trouverez plus d’informations dans d’autres sections de la documentation.

Les données sont conservées dans des mémoires tampons, qui sont simplement des tableaux d’octets. Chaque mémoire tampon est encapsulée par un objet COM appelé *exemple de média*, qui implémente l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Les exemples sont créés par un autre type d’objet, appelé Allocator, qui implémente l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Un allocateur est attribué pour chaque connexion de code confidentiel, bien que deux connexions de code confidentiel ou plus peuvent partager le même allocateur. L’illustration suivante montre ce processus.

![mémoires tampons, exemples et allocators](images/dataflow.png)

Chaque allocateur crée un pool d’exemples de supports et alloue les tampons pour chaque exemple. Chaque fois qu’un filtre doit remplir une mémoire tampon avec des données, il demande un exemple à partir de l’allocateur en appelant [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Si l’allocateur a des échantillons qui ne sont pas actuellement utilisés par un autre filtre, la méthode **GetBuffer** retourne immédiatement avec un pointeur vers l’exemple. Si tous les exemples de l’allocateur sont en cours d’utilisation, la méthode se bloque jusqu’à ce qu’un exemple devienne disponible. Lorsque la méthode retourne un exemple, le filtre place les données dans la mémoire tampon, définit les indicateurs appropriés sur l’échantillon (en général, en incluant un horodatage) et remet l’exemple en aval.

Lorsqu’un filtre de convertisseur reçoit un exemple, il vérifie l’horodatage et le maintient sur l’exemple jusqu’à ce que l’horloge de référence du graphique de filtre indique que les données doivent être rendues. Une fois que le filtre a rendu les données, il libère l’exemple. L’exemple ne repasse pas dans le pool d’exemples de l’allocateur tant que le nombre de références de l’exemple n’est pas égal à zéro, ce qui signifie que chaque filtre a libéré l’exemple. L’illustration suivante montre ce processus.

![décodeur en attente d’un exemple de support gratuit](images/dataflow2.png)

Le filtre en amont peut s’exécuter avant le convertisseur, autrement dit, il peut remplir les mémoires tampons plus rapidement que le convertisseur ne les consomme. Même dans ce cas, les exemples ne sont pas rendus tôt, car le convertisseur conserve chaque fois son heure de présentation. En outre, le filtre amont ne remplace pas les tampons par inadvertance, car **méthode getsample** retourne uniquement des exemples qui ne sont pas en cours d’utilisation. La quantité d’exécution du filtre en amont est déterminée par le nombre d’échantillons dans le pool de l’allocateur.

Le diagramme précédent n’affiche qu’un seul allocateur, mais il existe généralement plusieurs allocateurs par flux. Ainsi, lorsque le convertisseur libère un exemple, il peut avoir un effet en cascade. Le diagramme suivant illustre une situation où un décodeur contient une image vidéo compressée pendant qu’il attend que le convertisseur libère un exemple. Un filtre d’analyseur attend également que le décodeur libère un exemple.

![deux filtres en attente d’exemples](images/dataflow3.png)

Quand le convertisseur libère son exemple, l’appel en attente du décodeur à **GetBuffer** retourne. Le décodeur peut ensuite décoder la trame vidéo compressée et libérer l’exemple qu’il a bloqué, ce qui a pour effet de débloquer l’appel **GetBuffer** en attente de l’analyseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[données Flow dans le filtre Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



