---
description: Les systèmes de coordonnées pour Direct3D 10 sont définis pour les pixels et les texels.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Systèmes de coordonnées (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748972"
---
# <a name="coordinate-systems-direct3d-10"></a>Systèmes de coordonnées (Direct3D 10)

Les systèmes de coordonnées pour Direct3D 10 sont définis pour les pixels et les texels.



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 10 :<br/> Direct3D 10 définit le coin supérieur gauche du pixel supérieur gauche comme l’origine d’une cible de rendu.<br/> Direct3D 9 définit le centre du pixel supérieur gauche comme l’origine d’une cible de rendu.<br/> |



 

-   [Système de coordonnées de pixels](#pixel-coordinate-system)
    -   [Système de coordonnées en pixels pour Direct3D 9](#pixel-coordinate-system-for-direct3d-9)
-   [Système de coordonnées Texel](#texel-coordinate-system)
    -   [Système de coordonnées Texel](#texel-coordinate-system)
-   [Rubriques connexes](#related-topics)

## <a name="pixel-coordinate-system"></a>Système de coordonnées de pixels

Le système de coordonnées en pixels dans Direct3D 10 définit l’origine d’une cible de rendu dans l’angle supérieur gauche. comme indiqué dans le diagramme suivant. Les centres de pixels sont décalés de (0,5 f, 0,5 f) à partir des emplacements d’entiers.

![diagramme du système de coordonnées en pixels dans Direct3D 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Système de coordonnées en pixels pour Direct3D 9

Pour référence, voici le système de coordonnées en pixels pour Direct3D 9, qui a défini l’origine ou une cible de rendu en tant que centre du pixel supérieur gauche, (0.5, 0.5) en dehors de l’angle supérieur gauche, comme indiqué dans le diagramme suivant. Dans Direct3D 9, les centres de pixels sont à des emplacements entiers.

![diagramme du système de coordonnées en pixels dans Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Système de coordonnées Texel

Le système de coordonnées Texel a son origine dans l’angle supérieur gauche de la texture, comme indiqué dans le diagramme suivant. Cela rend le rendu des textures alignées à l’écran trivial (dans Direct3D 10), car le système de coordonnées de pixels est aligné avec le système de coordonnées Texel.

![diagramme du système de coordonnées texels](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Système de coordonnées Texel

Les coordonnées de texture sont représentées par un nombre normalisé ou à l’échelle ; chaque coordonnée de texture est mappée à un Texel spécifique comme suit :

Pour une coordonnée normalisée :

-   Échantillonnage de point : Texel \# = Floor ( \* largeur U)
-   Échantillonnage linéaire : Texel gauche \# = plancher ( \* largeur U), Texel à droite \# = Texel gauche \# + 1

Pour une coordonnée mise à l’échelle :

-   Échantillonnage de point : Texel \# = Floor (U)
-   Échantillonnage linéaire : Texel gauche \# = Floor (U-0,5), Texel Right \# = Texel gauche \# + 1

Où la largeur correspond à la largeur de la texture (dans les texels).

L’encapsulation d’adresse de texture se produit après le calcul de l’emplacement de Texel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




