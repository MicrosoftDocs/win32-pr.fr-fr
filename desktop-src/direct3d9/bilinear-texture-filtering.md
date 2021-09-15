---
description: Les textures sont toujours traitées de manière linéaire (0,0, 0,0) dans le coin supérieur gauche pour (1,0, 1,0) dans le coin inférieur droit, comme indiqué dans l’illustration suivante.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtrage de texture bilinéaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516996"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a>Filtrage de texture bilinéaire (Direct3D 9)

Les textures sont toujours traitées de manière linéaire (0,0, 0,0) dans le coin supérieur gauche pour (1,0, 1,0) dans le coin inférieur droit, comme indiqué dans l’illustration suivante.

![illustration de la texture 4x4 avec des blocs de couleur solides](images/bilinear-fig7a.png)

Les textures sont généralement représentées comme si elles étaient composées de blocs de couleur solides, mais il est en fait plus approprié de considérer les textures de la même façon que l’affichage raster : chaque Texel est défini au centre exact d’une cellule de grille, comme indiqué dans l’illustration suivante.

![illustration de la texture 4x4 avec des texels définis au centre des cellules de la grille](images/bilinear-fig7b.png)

Si vous demandez l’échantillonneur de texture pour la couleur de cette texture aux coordonnées UV (0,375, 0,375), vous obtenez un rouge Uni (255, 0,0). Cela est parfait, car le centre exact de la cellule Texel rouge est UV (0,375, 0,375). Que se passe-t-il si vous demandez à l’échantillonneur la couleur de la texture sur UV (0,25, 0,25) ? Ce n’est pas tout aussi simple, car le point à UV (0,25, 0,25) se trouve à l’angle exact de 4 texels.

Le schéma le plus simple consiste simplement à faire en sorte que l’échantillonneur retourne la couleur de la Texel la plus proche. C’est ce que l’on appelle le filtrage des points (voir [échantillonnage à point le plus proche (Direct3D 9)](nearest-point-sampling.md)) et qui est généralement indésirable en raison des résultats de granularité ou de blocage. L’échantillonnage par pointage de notre texture à l’UV (0,25, 0,25) illustre un autre problème subtil avec le filtrage de point le plus proche : il y a quatre texels équidistants à partir du point d’échantillonnage. il n’y a donc pas de Texel unique le plus proche. L’un de ces quatre texels est choisi comme couleur renvoyée, mais la sélection dépend de la manière dont la coordonnée est arrondie, ce qui peut introduire des artefacts de déchirement (consultez l’article Nearest-Point d’échantillonnage dans le kit de développement logiciel (SDK)).

Un schéma de filtrage légèrement plus précis et plus courant consiste à calculer la moyenne pondérée des 4 texels les plus proches du point d’échantillonnage ; C’est ce que l’on appelle le filtrage bilinéaire et le coût de calcul supplémentaire est généralement négligeable, car cette routine est implémentée dans le matériel graphique moderne. Voici les couleurs que nous obtenons à quelques points d’échantillonnage différents en utilisant le filtrage bilinéaire :


```
UV: (0.5, 0.5)
```



Ce point se trouve à la bordure exacte entre les texels rouge, vert, bleu et blanc. La couleur renvoyée par l’échantillonneur est grise :


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



Ce point se trouve au milieu de la bordure entre les texels rouges et verts. La couleur renvoyée par l’échantillonneur est jaune-gris (Notez que les contributions des texels bleu et blanc sont mises à l’échelle sur 0) :


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



Il s’agit de l’adresse du Texel rouge, qui est la couleur retournée (toutes les autres textures dans le calcul de filtrage sont pondérées à 0) :


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



Comparez ces calculs à l’illustration suivante, qui montre ce qui se passe si le calcul de filtrage bilinéaire est effectué à chaque adresse de texture à travers la texture 4x4.

![illustration de la texture 4x4 avec Filtrage bilinéaire effectué à chaque adresse de texture](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage de texture](texture-filtering.md)
</dt> </dl>

 

 



