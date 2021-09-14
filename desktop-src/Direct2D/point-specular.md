---
title: Effet d’éclairage spéculaire par point
description: Utilisez l’effet d’éclairage point-spéculaire pour créer une image qui semble être une surface réfléchissante.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- effet d’éclairage spéculaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355c573888604af8dfac443f4f53554a8a780071
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112601"
---
# <a name="point-specular-lighting-effect"></a>Effet d’éclairage spéculaire par point

Utilisez l’effet d’éclairage point-spéculaire pour créer une image qui semble être une surface réfléchissante. L’effet utilise le canal alpha de l’image comme carte de hauteur et une source de lumière de point que vous placez, puis calcule la réflexion et la lumière en fonction de la partie spéculaire du modèle d’éclairage Phong.

La couleur de l’image bitmap de sortie est un résultat de la couleur claire, de la position de la lumière et de la géométrie de la surface. La sortie de canal alpha pour chaque pixel avec éclairage spéculaire est le nombre maximal de sorties de canal rouge, vert et bleu pour ce pixel.

Le CLSID de cet effet est CLSID \_ D2D1PointSpecular.

-   [Exemple d’image](#example-image)
-   [Source de lumière de point](#point-light-source)
-   [Carte de hauteur et vecteur normal](#height-map-and-normal-vector)
-   [Constante d’éclairage spéculaire et exposant](#specular-lighting-constant-and-exponent)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de mise à l’échelle](#scales-modes)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet d’éclairage de point-spéculaire.

![exemple de capture d’écran montrant les images d’entrée et de sortie de l’effet d’éclairage spéculaire du point.](images/point-spec-example.png)

La lumière spéculaire fait référence à la lumière qui est reflétée dans une direction spécifique en fonction du modèle d’éclairage Phong.

![diagramme des vecteurs utilisés pour cacluate une sortie d’éclairage spéculaire pour une image bitmap.](images/point-spec-reflected1.png)

L’effet calcule les valeurs de pixel de sortie finales à l’aide des équations ici :

![équations pour le calcul des valeurs de pixels finales. ](images/point-spec-formula-output.png)

where<dl> DK? = constante d’éclairage spéculaire.  
![symbole de vecteur d’unité normale de surface. ](images/point-spec-mathchar-n.png) = vecteur d’unité normale de surface qui est une fonction de x et y. Consultez [carte de hauteur et vecteur normal](#height-map-and-normal-vector) pour les calculs.  
![symbole de vecteur d’unité à mi-chemin. ](images/point-spec-mathchar-h.png) = vecteur d’unité « mi » entre le vecteur d’unité oculaire et le vecteur d’unité clair. Consultez [source de lumière de point](#point-light-source) pour les calculs.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = couleur claire des composants RVB.  
</dl>

Vous définissez la constante d’éclairage spéculaire sur la propriété *SpecularConstant* et la couleur claire comme propriété de *couleur* .

## <a name="point-light-source"></a>Source de lumière de point

Une source de lumière de point émet de la lumière dans toutes les directions comme dans l’image ici.

![lumière de point émettant de la lumière dans toutes les directions.](images/point-spec-light.png)

Vous définissez la position de la source de lumière à l’aide de la propriété *LightPosition* . L’effet calcule le vecteur clair, L, pour une source de lumière de point à l’aide des équations ici :

![équation de vecteur clair.](images/point-spec-formula3.png)

où Light ?, Light<sub>y</sub>et Light<sub>z</sub> sont la position de la lumière d’entrée. L’effet calcule le vecteur à mi- ![ chemin.](images/point-spec-mathchar-h.png) comme défini dans le modèle d’éclairage Phong, à l’aide de l’équation ici. Le modèle d’éclairage suppose que le vecteur oculaire, ![ le symbole de vecteur oculaire ](images/point-spec-mathchar-e.png) , se trouve à (0, 0, 1).

![équation à moitié vecteur.](images/point-spec-formula4.png)

L et H sont normalisés en vecteurs de longueur unitaire.

## <a name="height-map-and-normal-vector"></a>Carte de hauteur et vecteur normal

L’effet génère une carte de hauteur pour l’image d’entrée en fonction de son canal alpha.

Le composant Height (Z) est calculé à l’aide de l’équation suivante :

![équation pour le calcul de la hauteur (z) de la surface.](images/point-spec-formula6.png)

L’effet calcule la normale de la surface, ![symbole de vecteur normal.](images/point-spec-mathchar-n.png), pour la bitmap d’entrée à l’aide d’un dégradé Sobel.

## <a name="specular-lighting-constant-and-exponent"></a>Constante d’éclairage spéculaire et exposant

La lumière spéculaire représente la lumière réfléchie à partir de la surface du de la carte de la hauteur de l’image. Vous spécifiez la propriété *SpecularExponent* qui détermine la quantité de réflexion spéculaire à partir de l’image bitmap.

Les exposants plus grands représentent des objets shinier et reflètent la lumière dans une forme plus ciblée.

La propriété *SpecularConstant* K ? définit la quantité de lumière réfléchie comme rapport de la lumière entrante.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> POSITION de la \_ lumière d2d1 POINTSPECULAR \_ prop \_ \_<br/>         | Position claire de la source de lumière de point. La propriété est un \_ vecteur d2d1 \_ 3F défini en tant que (x, y, z). Les unités sont en pixels indépendants du périphérique (DIP) et les valeurs sont sans unité et illimitée. Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> \_ \_ \_ Exposant spéculaire d2d1 POINTSPECULAR prop \_<br/>   | Exposant du terme spéculaire dans l’équation d’éclairage Phong. Une plus grande valeur correspond à une surface plus réfléchissante. Cette valeur est sans unité et doit être comprise entre 1,0 et 128. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> \_ \_ \_ Constante spéculaire d2d1 POINTSPECULAR prop \_<br/>   | Rapport entre la réflexion spéculaire et la lumière entrante. La valeur est sans unité et doit être comprise entre 0 et 10 000. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> \_Échelle de surface d2d1 POINTSPECULAR \_ prop \_ \_<br/>           | Facteur d’échelle dans la direction Z pour la génération d’une carte de hauteur. La valeur est sans unité et doit être comprise entre 0 et 10 000. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Couleur<br/> \_Couleur d2d1 POINTSPECULAR \_ prop \_<br/>                           | Couleur de la lumière entrante. Cette propriété est exposée en tant que \_ vecteur d2d1 \_ 3F (R, G, B) et utilisée pour calculer l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> Longueur de l' \_ unité de noyau d2d1 POINTSPECULAR \_ prop \_ \_ \_<br/> | Taille d’un élément dans le noyau Sobel utilisé pour générer la surface normale dans les directions X et Y. Cette propriété est mappée aux valeurs DX et dy dans le dégradé Sobel. Cette propriété est un \_ vecteur d2d1 \_ 2F (longueur d’unité de noyau X, longueur d’unité de noyau Y) et est défini dans (DIP/unité noyau). L’effet utilise l’interpolation bilinéaire pour mettre à l’échelle l’image bitmap afin qu’elle corresponde à la taille des éléments de noyau. Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {1.0 f, 1.0 f}.<br/> |
| Devient<br/> MODE de mise à l' \_ échelle d2d1 POINTSPECULAR \_ prop \_ \_<br/>                 | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle de la longueur de l’unité de noyau correspondante. Il existe six modes de mise à l’échelle qui vont de la qualité et de la vitesse. Pour plus d’informations, consultez modes de mise à l' [échelle](#scales-modes) . <br/> Le type est D2D1 \_ POINTSPECULAR \_ Scale \_ mode.<br/> La valeur par défaut est D2D1 \_ POINTSPECULAR \_ Scale \_ mode \_ linéaire.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Modes de mise à l’échelle



| Énumération                                             | Description                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE de mise à l' \_ échelle d2d1 POINTSPECULAR \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 mode de mise à l' \_ \_ échelle POINTSPECULAR \_ \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode génère une image de qualité supérieure à celle du voisin le plus proche.                                                                                   |
| D2D1 mode de mise à l' \_ \_ échelle POINTSPECULAR \_ \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| MODE de mise à l' \_ échelle d2d1 POINTSPECULAR \_ multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode Scale \_ POINTSPECULAR \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ POINTSPECULAR \_ \_ en mode Scale de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ POINTSPECULAR \_ Scale \_ mode \_ linéaire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

