---
title: Tas partagés
description: Le partage est utile pour les architectures multiprocessus et multi-adaptateurs.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4271055f88e38484041c225b6b17c6d75f0d98
ms.sourcegitcommit: d6102d9e2b26368142fe5b006c65acb50c98be65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2019
ms.locfileid: "74104452"
---
# <a name="shared-heaps"></a>Tas partagés

Le partage est utile pour les architectures multiprocessus et multi-adaptateurs.

-   [Vue d’ensemble du partage](#sharing-overview)
-   [Partage des tas entre les processus](#sharing-heaps-across-processes)
-   [Partage des segments de mémoire entre les adaptateurs](#sharing-heaps-across-adapters)
-   [Rubriques connexes](#related-topics)

## <a name="sharing-overview"></a>Vue d’ensemble du partage

Les tas partagés permettent deux choses : le partage de données dans un segment de mémoire dans un ou plusieurs processus et l’empêchement d’un choix non déterministe de disposition de texture non définie pour les ressources placées dans le tas. Le partage de tas entre les adaptateurs élimine également le besoin de marshaling de l’UC des données.

Les tas et les ressources validées peuvent être partagés. Le partage d’une ressource validée partage en fait le tas implicite ainsi que la description de la ressource validée, de sorte qu’une description de ressource compatible peut être mappée au segment de mémoire à partir d’un autre appareil.

Toutes les méthodes sont libres de threads et héritent de la sémantique D3D11 existante de la conception de partage de handle NT.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Partage des tas entre les processus

Les tas partagés sont spécifiés avec l' \_ \_ indicateur de segment de mémoire D3D12 \_ membre Shared de l’énumération des [**\_ \_ indicateurs de tas D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

Les tas partagés ne sont pas pris en charge sur les segments de mémoire accessibles par le processeur : D3D12 le type de segment de mémoire, D3D12 de type de segment \_ \_ \_ \_ \_ \_ READBACK et \_ type de segment D3D12 \_ \_ personnalisé sans \_ propriété de page d’UC D3D12 \_ \_ \_ non \_ disponible.

En excluant un choix non déterministe de la mise en page de texture non définie, vous risquez de nuire considérablement aux scénarios de rendu différés sur certains GPU, ce qui n’est donc pas le comportement par défaut pour les ressources placées et validées. Le rendu différé est altéré sur certaines architectures GPU, car les dispositions de texture déterministes diminuent la bande passante de mémoire effective atteinte lors du rendu simultané à plusieurs textures cibles de rendu de même format et de même taille. Les architectures GPU évoluent en tirant parti des dispositions de texture non déterministes afin de prendre en charge des modèles Swizzle standardisés et des mises en page standardisées efficaces pour le rendu différé.

Les tas partagés sont également associés à d’autres coûts mineurs :

-   Les données du tas partagé ne peuvent pas être recyclées de manière flexible en tant que segments in-process en raison de problèmes de divulgation d’informations. la mémoire physique est donc zero’ed plus souvent.
-   La surcharge du processeur supplémentaire et l’utilisation de la mémoire système augmentent lors de la création et de la destruction des tas partagés.

## <a name="sharing-heaps-across-adapters"></a>Partage des segments de mémoire entre les adaptateurs

Les segments de mémoire partagés entre les adaptateurs sont spécifiés avec l' \_ \_ indicateur de tas D3D12 \_ \_ membre Cross- \_ adapter partagé de l’énumération d' [**\_ \_ indicateurs de tas D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

Les tas partagés entre les adaptateurs permettent à plusieurs adaptateurs de partager des données sans que l’UC ne remarshale les données entre eux. Bien que les capacités des adaptateurs déterminent la manière dont les adaptateurs efficaces peuvent passer des données entre eux, l’activation des copies GPU augmente la bande passante effective. Certaines dispositions de texture sont autorisées sur les tas d’adaptateurs croisés pour prendre en charge un échange de données de texture, même si ces dispositions de texture ne sont pas prises en charge par ailleurs. Certaines restrictions peuvent s’appliquer à ces textures, telles que la prise en charge de la copie uniquement.

Le partage entre les adaptateurs fonctionne avec les tas créés en appelant [**ID3D12Device :: CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Les applications peuvent ensuite créer des ressources via [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource). Elle est également autorisée par les ressources/segments de mémoire créés par [**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) , mais uniquement pour les ressources TEXTURE2D de la dimension D3D12 des ressources principales \_ \_ \_ (reportez-vous à la [**\_ \_ dimension de ressource D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). Le partage entre les adaptateurs ne fonctionne pas avec [**CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

Pour le partage entre les adaptateurs, toutes les règles habituelles de partage des ressources entre les files d’attente s’appliquent toujours. Les applications doivent émettre les barrières appropriées pour garantir une synchronisation et une cohérence appropriées entre les deux cartes. Les applications doivent utiliser des limites entre les adaptateurs pour coordonner la planification des listes de commandes soumises à plusieurs adaptateurs. Il n’existe aucun mécanisme permettant de partager des ressources entre les adaptateurs entre les versions de l’API D3D. Les ressources partagées entre les adaptateurs sont uniquement prises en charge dans la mémoire système. Les segments de mémoire partagés/ressources entre les adaptateurs sont pris en charge dans \_ \_ les segments par défaut du type de tas D3D12 \_ et \_ \_ les tas personnalisés de type de tas D3D12 \_ (avec le pool de mémoire N0 et les propriétés de la page d’UC de combinaison d’écriture). Les pilotes doivent s’assurer que les opérations de lecture/écriture GPU pour les tas partagés entre les adaptateurs sont cohérentes avec d’autres GPU sur le système. Par exemple, il se peut que le pilote doive exclure les données du tas résidant dans les caches GPU qui ne sont généralement pas nécessaires lorsque l’UC ne peut pas accéder directement aux données du tas.

Les applications doivent limiter l’utilisation des tas entre les adaptateurs uniquement aux scénarios qui requièrent les fonctionnalités qu’ils fournissent. Les tas entre les adaptateurs se trouvent dans \_ le pool de mémoire D3D12 \_ \_ L0, ce qui n’est pas toujours ce que [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) suggère. Ce pool de mémoire n’est pas efficace pour les architectures d’adaptateurs discrètes/NUMA. Et, les dispositions de texture les plus efficaces ne sont pas toujours disponibles.

Les limitations suivantes s'appliquent également :

-   Les indicateurs de tas associés aux niveaux de segment de mémoire doivent être un \_ indicateur de tas D3D12 \_ \_ autoriser \_ toutes les \_ mémoires tampons \_ et les \_ textures.
-   L' \_ indicateur de segment de mémoire D3D12 \_ \_ partagé doit également être défini.
-   Le \_ type de segment D3D12 \_ \_ par défaut doit être défini ou le \_ \_ type de segment D3D12 \_ personnalisé avec le \_ pool de mémoires D3D12 \_ \_ N0 et la propriété de page d' \_ UC D3D12 \_ \_ \_ non \_ disponible doivent être définis.
-   Seules les ressources avec l' \_ indicateur de ressource D3D12 \_ \_ allow \_ travers \_ adapter peuvent être placées sur des segments de mémoire entre les adaptateurs.

Pour plus d’informations sur l’utilisation de plusieurs cartes, reportez-vous à la section [systèmes à plusieurs adaptateurs](multi-engine.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sous-allocation au sein des tas](suballocation-within-heaps.md)
</dt> </dl>

 

 




