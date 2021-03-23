---
title: Gestion de la mémoire dans Direct3D 12
description: Le passage à D3D12 implique une synchronisation et une gestion appropriées de la résidence en mémoire.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104618"
---
# <a name="memory-management-in-direct3d-12"></a>Gestion de la mémoire dans Direct3D 12

Le passage à D3D12 implique une synchronisation et une gestion appropriées de la résidence en mémoire. La gestion de la résidence en mémoire signifie qu’une plus grande synchronisation doit être effectuée. Cette section traite des stratégies de gestion de la mémoire et de la sous-allocation au sein des tas et des mémoires tampons.

-   [Dans cette section](#in-this-section)
-   [Rubriques connexes](#related-topics)

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stratégies de gestion de la mémoire](memory-management-strategies.md)<br/> | Un gestionnaire de mémoire pour Direct3D 12 peut être très compliqué rapidement avec les différents niveaux de prise en charge, pour les adaptateurs UMA ou discrets (non-UMA) et avec un large éventail de différences d’architecture entre les adaptateurs GPU.<br/> La stratégie recommandée pour la gestion de la mémoire Direct3D 12, décrite dans cette section, est « classification, budget et flux ».<br/> |
| [Sous-allocation dans des mémoires tampons](large-buffers.md)<br/>                | Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU. Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.<br/>                                                                                                                                     |
| [Sous-allocation au sein des tas](suballocation-within-heaps.md)<br/>     | Les tas de ressources transfèrent les données de l’UC vers le GPU (chargement) et du GPU vers le processeur (lecture en retour). <br/>                                                                                                                                                                                                                                                                  |
| [Résidence](residency.md)<br/>                                       | Un objet est considéré comme *résident* lorsqu’il est accessible par le GPU.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> </dl>

 

 





