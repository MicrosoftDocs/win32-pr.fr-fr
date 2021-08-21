---
title: Fonctionnalités Direct3D 11,3
description: Les sections suivantes décrivent la fonctionnalité qui a été ajoutée dans Direct3D 11,3. Ces fonctionnalités sont également disponibles dans Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bfdead81de43cbe0391b661f450db0acfa402417148ed1d1731e4a22f05f1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099241"
---
# <a name="direct3d-113-features"></a>Fonctionnalités Direct3D 11,3

Les sections suivantes décrivent la fonctionnalité qui a été ajoutée dans Direct3D 11,3. Ces fonctionnalités sont également disponibles dans Direct3D 12.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pixellisation conservatrice](conservative-rasterization.md)<br/>                             | La pixellisation conservatrice apporte une certaine certitude au rendu des pixels, ce qui est utile en particulier pour les algorithmes de détection des collisions.<br/>                                                                                                                                                                                                                                              |
| [Mappage de texture par défaut](default-texture-mapping.md)<br/>                                   | L’utilisation du mappage de texture par défaut réduit la copie et l’utilisation de la mémoire tout en partageant des données d’image entre le GPU et le processeur. Toutefois, il ne doit être utilisé que dans des situations spécifiques. La disposition standard Swizzle évite la copie ou la swizzling des données dans plusieurs dispositions.<br/>                                                                                                               |
| [Vues de l’ordre du rastériseur](rasterizer-order-views.md)<br/>                                     | Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs. Cela permet l’utilisation d’algorithmes OIT (commande Independent transparent), ce qui donne de meilleurs résultats de rendu lorsque plusieurs objets transparents sont alignés les uns avec les autres dans une vue. <br/> |
| [Valeur de référence du stencil spécifié par le nuanceur](shader-specified-stencil-reference-value.md)<br/> | L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.<br/>                                                                                                                                                                                                              |
| [Chargements de vues d’accès non ordonnées typées](typed-unordered-access-view-loads.md)<br/>               | Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un format DXGI spécifique \_ .<br/>                                                                                                                                                                                                                                                               |
| [Architecture de la mémoire unifiée](unified-memory-architecture.md)<br/>                           | L’interrogation de la prise en charge de l’architecture mémoire unifiée (UMA) peut vous aider à déterminer comment gérer certaines ressources.<br/>                                                                                                                                                                                                                                                              |
| [Ressources en mosaïque de volume](volume-tiled-resources.md)<br/>                                     | Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nouveautés de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





