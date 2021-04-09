---
title: Effet d’éclairage diffus par point
description: Utilisez l’effet d’éclairage point-diffus pour créer une image qui semble être une surface non réfléchissante avec la lumière dispersée dans toutes les directions. Cet effet utilise le canal alpha comme carte de hauteur et met en lumière l’image avec une source de lumière de point.
ms.assetid: C98A4962-B9EB-4095-9AC4-F1C32C574892
keywords:
- effet d’éclairage de diffusion de point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de97edfa6c2166d5c29649aabfe97761440f8f18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033135"
---
# <a name="point-diffuse-lighting-effect"></a>Effet d’éclairage diffus par point

Utilisez l’effet d’éclairage point-diffus pour créer une image qui semble être une surface non réfléchissante avec la lumière dispersée dans toutes les directions. Cet effet utilise le canal alpha comme carte de hauteur et met en lumière l’image avec une source de lumière de point.

La couleur de l’image bitmap de sortie est un résultat de la couleur claire, de la position de la lumière et de la géométrie de la surface. La sortie de canal alpha pour chaque pixel avec éclairage diffus est toujours 1,0.

Le CLSID de cet effet est CLSID \_ D2D1PointDiffuse. Pour utiliser cet effet, ajoutez dxguid. lib aux dépendances de l’éditeur de liens.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de mise à l’échelle](#scale-modes)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet d’éclairage point-diffus.

![exemple de capture d’écran montrant les images d’entrée et de sortie de l’effet d’éclairage diffus de point.](images/point-diffuse-example.png)

L’éclairage diffus fait référence à la lumière qui est reflétée dans plusieurs directions comme indiqué ici.

![le voyant d’éclairage diffus est dispersé dans toutes les directions.](images/point-diffuse-lighting.png)

L’effet calcule les valeurs de pixels de sortie finales calculées à l’aide des équations suivantes :

![calculs de bitmap de sortie.](images/point-diffuse-formula1.png)

Où :<dl> k<sub>d</sub> = constante d’éclairage diffus. Spécifié par l’utilisateur.  
![symbole de vecteur normal de surface.](images/point-spec-mathchar-n.png) = vecteur d’unité normale de surface, fonction de x et y.  
![symbole de vecteur d’unité.](images/distant-spec-mathchar-l.png) = vecteur unitaire pointant d’une surface à une lumière.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = couleur claire des composants RVB.  
</dl>

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> POSITION de la \_ lumière d2d1 POINTDIFFUSE \_ prop \_ \_<br/>         | Position claire de la source de lumière de point. La propriété est un \_ vecteur d2d1 \_ 3F défini en tant que (x, y, z). Les unités sont en pixels indépendants du périphérique (DIP) et ne sont pas liées. <br/> Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                                              |
| DiffuseConstant<br/> \_ \_ \_ Constante diffuse d2d1 POINTDIFFUSE prop \_<br/>     | Rapport entre la réflexion diffuse et la quantité de lumière entrante. Cette propriété doit être comprise entre 0 et 10 000 et est sans unité. <br/> Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                          |
| SurfaceScale<br/> \_Échelle de surface d2d1 POINTDIFFUSE \_ prop \_ \_<br/>           | Facteur d’échelle dans la direction Z. L’échelle de surface est sans unité et doit être comprise entre 0 et 10 000.<br/> Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                               |
| Couleur<br/> \_Couleur d2d1 POINTDIFFUSE \_ prop \_<br/>                           | Couleur de la lumière entrante. Cette propriété est exposée comme vecteur 3 (R, G, B) et utilisée pour calculer L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/> Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> Longueur de l' \_ unité de noyau d2d1 POINTDIFFUSE \_ prop \_ \_ \_<br/> | Taille d’un élément dans le noyau Sobel utilisé pour générer la surface normale dans les directions X et Y. Cette propriété est mappée aux valeurs DX et dy dans le dégradé Sobel. Cette propriété est un \_ vecteur d2d1 \_ 2F (longueur d’unité de noyau X, longueur d’unité de noyau Y) et est défini dans (DIP/unité noyau). L’effet utilise l’interpolation bilinéaire pour mettre à l’échelle l’image bitmap afin qu’elle corresponde à la taille des éléments de noyau. <br/> Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {1.0 f, 1.0 f}.<br/> |
| Devient<br/> MODE de mise à l' \_ échelle d2d1 POINTDIFFUSE \_ prop \_ \_<br/>                 | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle de la longueur de l’unité de noyau correspondante. Il existe six modes de mise à l’échelle qui vont de la qualité et de la vitesse. Pour plus d’informations, consultez modes de mise à l' [échelle](#scale-modes) . <br/> Le type est D2D1 \_ POINTDIFFUSE \_ Scale \_ mode.<br/> La valeur par défaut est D2D1 \_ POINTDIFFUSE \_ Scale \_ mode \_ linéaire.<br/>                                                                                                                                         |



 

## <a name="scale-modes"></a>Modes de mise à l’échelle



| Énumération                                            | Description                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE de mise à l' \_ échelle d2d1 POINTDIFFUSE \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 mode de mise à l' \_ \_ échelle POINTDIFFUSE \_ \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode génère une image de qualité supérieure à celle du voisin le plus proche.                                                                                   |
| D2D1 mode de mise à l' \_ \_ échelle POINTDIFFUSE \_ \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| MODE de mise à l' \_ échelle d2d1 POINTDIFFUSE \_ multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode Scale \_ POINTDIFFUSE \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ POINTDIFFUSE \_ \_ en mode Scale de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ POINTDIFFUSE \_ Scale \_ mode \_ linéaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| Serveur minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

