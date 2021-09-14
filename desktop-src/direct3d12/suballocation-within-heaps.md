---
title: Sous-allocation au sein des tas
description: Les tas de ressources transfèrent les données de l’UC vers le GPU (chargement) et du GPU vers le processeur (lecture en retour).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012868"
---
# <a name="suballocation-within-heaps"></a>Sous-allocation au sein des tas

Les tas de ressources transfèrent les données de l’UC vers le GPU (chargement) et du GPU vers le processeur (lecture en retour).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alias de mémoire et héritage de données](memory-aliasing-and-data-inheritance.md)<br/> | Les ressources placées et réservées peuvent avoir un alias de la mémoire physique dans un segment. Les ressources passées activent davantage de scénarios d’héritage de données que les ressources réservées lorsque l’indicateur partagé est défini pour le tas ou lorsque les ressources avec alias ont des dispositions de mémoire entièrement définies. <br/> |
| [Tas partagés](shared-heaps.md)<br/>                                                 | Le partage est utile pour les architectures multiprocessus et multi-adaptateurs.<br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID3D12Device :: CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gestion de la mémoire](memory-management.md)
</dt> </dl>

 

 





