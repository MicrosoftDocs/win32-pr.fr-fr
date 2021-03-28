---
title: Textures
description: Cette section décrit les textures utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197090"
---
# <a name="textures"></a>Textures

Une texture stocke les informations de Texel. Cette section décrit les textures utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Présentation des textures dans Direct3D 11](overviews-direct3d-11-resources-textures-intro.md)<br/> | Une ressource de texture est une collection structurée de données conçue pour stocker des texels. Un Texel représente la plus petite unité d’une texture qui peut être lue ou écrite par le pipeline. Contrairement aux mémoires tampons, les textures peuvent être filtrées par des échantillonneurs de texture, car elles sont lues par des unités de nuanceur. Le type de texture affecte la manière dont la texture est filtrée. Chaque Texel contient des composants de 1 à 4, organisés dans l’un des formats DXGI définis par l' \_ énumération de format DXGI.<br/> |
| [Compression de bloc de texture dans Direct3D 11](texture-block-compression-in-direct3d-11.md)<br/>      | La prise en charge de la compression par bloc (BC) des textures a été étendue dans Direct3D 11 pour inclure les algorithmes BC6H et BC7. BC6H prend en charge les données sources de plage haute dynamique, et BC7 fournit une compression de qualité supérieure à la moyenne avec moins d’artefacts pour les données sources RGB standard.<br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment : créer une texture](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[Comment : initialiser une texture par programmation](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[Comment : initialiser une texture à partir d’un fichier](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[Ressources](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





