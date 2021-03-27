---
title: Accès du pipeline aux ressources en mosaïque
description: Les ressources en mosaïque peuvent être utilisées dans les vues de ressource de nuanceur (SRV), les affichages de cible de rendu (RTV), les vues de stencil de profondeur (DSV) et les vues d’accès non ordonnées (UAV), ainsi que certains points de liaison où les vues ne sont pas utilisées, telles que les liaisons de mémoire tampon de vertex.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729253"
---
# <a name="pipeline-access-to-tiled-resources"></a>Accès du pipeline aux ressources en mosaïque

Les ressources en mosaïque peuvent être utilisées dans les vues de ressource de nuanceur (SRV), les affichages de cible de rendu (RTV), les vues de stencil de profondeur (DSV) et les vues d’accès non ordonnées (UAV), ainsi que certains points de liaison où les vues ne sont pas utilisées, telles que les liaisons de mémoire tampon de vertex. Pour obtenir la liste des liaisons prises en charge, consultez [paramètres de création de ressources en mosaïque](tiled-resource-creation-parameters.md). Les \* opérations de copie fonctionnent également sur les ressources en mosaïque.

Si plusieurs coordonnées de mosaïque dans une ou plusieurs vues sont liées au même emplacement de mémoire, les lectures et écritures à partir de différents chemins d’accès à la même mémoire se produisent dans un ordre non déterministe et non reproductible d’accès à la mémoire.

Si toutes les vignettes derrière un encombrement d’accès à la mémoire à partir d’un nuanceur sont mappées à des vignettes uniques, le comportement est identique sur toutes les implémentations à la surface ayant le même contenu de mémoire en mode non en mosaïque.

Cette section fournit plus d’informations sur l’accès du pipeline aux ressources en mosaïque.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                              | Description                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comportement du SRV avec les vignettes non mappées](srv-behavior-with-non-mapped-tiles.md)<br/>                            | Le comportement des lectures de la vue de ressource de nuanceur (SRV) qui impliquent des vignettes non mappées dépend du niveau de support matériel. <br/>                                          |
| [Comportement de l’UAV avec les vignettes non mappées](uav-behavior-with-non-mapped-tiles.md)<br/>                            | Le comportement des lectures et écritures de la vue d’accès non triée (UAV) dépend du niveau de support matériel. <br/>                                                            |
| [Comportement du rastériseur avec les vignettes non mappées](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | Cette section décrit le comportement du rastériseur avec les vignettes non mappées.<br/>                                                                                              |
| [Restrictions d’accès aux vignettes avec des mappages en double](tile-access-limitations-with-duplicate-mappings-.md)<br/> | Cette section décrit les limitations d’accès aux vignettes avec des mappages en double.<br/>                                                                                        |
| [Fonctionnalités d’échantillonnage de texture des ressources en mosaïque](tiled-resources-texture-sampling-features.md)<br/>              | Cette section décrit les fonctionnalités d’échantillonnage de texture des ressources en mosaïque.<br/>                                                                                              |
| [Exposition des ressources en mosaïque HLSL](hlsl-tiled-resources-exposure.md)<br/>                                      | La nouvelle syntaxe HLSL (High Level Shader Language) de Microsoft est requise pour prendre en charge les ressources en mosaïque dans le [nuancier Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5). <br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources en mosaïque](tiled-resources.md)
</dt> </dl>

 

