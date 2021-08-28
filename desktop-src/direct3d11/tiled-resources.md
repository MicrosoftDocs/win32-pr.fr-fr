---
title: Ressources en mosaïque
description: Les ressources en mosaïque peuvent être considérées comme des ressources logiques volumineuses qui utilisent de petites quantités de mémoire physique.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73835d6603d1d8d7e708cd422e3991bb88ac1f91cebf016ccce36f2466270c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124087"
---
# <a name="tiled-resources"></a>Ressources en mosaïque

Les ressources en mosaïque peuvent être considérées comme des ressources logiques volumineuses qui utilisent de petites quantités de mémoire physique.

Cette section décrit les raisons pour lesquelles des ressources en mosaïque sont nécessaires et comment créer et utiliser des ressources en mosaïque.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                   | Description                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pourquoi les ressources en mosaïque sont-elles nécessaires ?](why-are-tiled-resources-needed-.md)<br/>       | Les ressources en mosaïque sont nécessaires afin que la mémoire de l’unité de traitement graphique (GPU) soit gaspillée pour stocker des régions de surfaces inaccessibles par l’application, et le matériel peut comprendre comment filtrer sur des vignettes adjacentes.<br/>     |
| [Création de ressources en mosaïque](creating-tiled-resources.md)<br/>                     | Les ressources en mosaïque sont créées en spécifiant l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) quand vous créez une ressource.<br/>                                                                                          |
| [API de ressources en mosaïque](tiled-resource-apis.md)<br/>                               | Les API décrites dans cette section fonctionnent avec les ressources en mosaïque et le pool de mosaïques.<br/>                                                                                                                                                              |
| [Accès du pipeline aux ressources en mosaïque](pipeline-access-to-tiled-resources.md)<br/> | Les ressources en mosaïque peuvent être utilisées dans les vues de ressource de nuanceur (SRV), les affichages de cible de rendu (RTV), les vues de stencil de profondeur (DSV) et les vues d’accès non ordonnées (UAV), ainsi que certains points de liaison où les vues ne sont pas utilisées, telles que les liaisons de mémoire tampon de vertex. <br/> |
| [Niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md)<br/>         | Direct3D 11,2 expose la prise en charge des ressources en mosaïque dans deux niveaux avec les valeurs de [**\_ niveau de \_ ressources \_ en mosaïque d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) . <br/>                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





