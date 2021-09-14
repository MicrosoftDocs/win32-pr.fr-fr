---
title: Effet d’éclairage diffus par spot
description: Utilisez l’effet Eclairage en lumière diffuse pour créer une image qui semble être une surface non réfléchissante dans laquelle la source de lumière est limitée à un cône dirigé de lumière et la lumière est dispersée dans toutes les directions.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- effet d’éclairage diffus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d085e43f161275cbe46d5b8eeb03f0ad13ff5f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113358"
---
# <a name="spot-diffuse-lighting-effect"></a>Effet d’éclairage diffus par spot

Utilisez l’effet Eclairage en lumière diffuse pour créer une image qui semble être une surface non réfléchissante dans laquelle la source de lumière est limitée à un cône dirigé de lumière et la lumière est dispersée dans toutes les directions. Cet effet utilise le canal alpha comme carte de hauteur et met en lumière l’image avec une source de lumière.

La couleur de l’image bitmap de sortie est un résultat de la couleur claire, de la position de la lumière et de la géométrie de la surface. La sortie de canal alpha pour chaque pixel avec éclairage diffus est toujours 1,0.

Le CLSID de cet effet est CLSID \_ D2D1SpotDiffuse.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de mise à l’échelle](#scale-modes)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet d’éclairage diffus.

![exemple de capture d’écran montrant ](images/spot-diffuse-example.png)

L’effet calcule les valeurs de pixels de sortie finales calculées à l’aide des équations suivantes :

![calcul de bitmap de sortie](images/spot-diffuse-formula.png)

Où :<dl> k<sub>d</sub> = constante d’éclairage diffus. Spécifié par l’utilisateur.  
![symbole de vecteur normal.](images/point-spec-mathchar-n.png) = vecteur d’unité normale de surface, fonction de x et y.  
![symbole de vecteur clair.](images/distant-spec-mathchar-l.png) = vecteur unitaire pointant d’une surface à une lumière.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = couleur claire des composants RVB.  
</dl>

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                     | Type et valeur par défaut                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> POSITION de la \_ lumière d2d1 SPOTDIFFUSE \_ prop \_ \_<br/>           | \_Vecteur d2d1 \_ 3F<br/> {0.0 f, 0.0 f, 0.0 f}<br/>                                   | Position claire de la source de lumière de point. La propriété est un \_ vecteur d2d1 \_ 3F défini en tant que (x, y, z). Les unités sont en pixels indépendants du périphérique (DIP) et ne sont pas liées.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ points \_ à<br/>                     | \_Vecteur d2d1 \_ 3F<br/> {0.0 f, 0.0 f, 0.0 f}<br/>                                   | Où le feu est concentré. La propriété est exposée sous la forme d’un \_ vecteur d2d1 \_ 3F avec (x, y, z). Les unités sont dans des DIP et les valeurs ne sont pas liées.<br/>                                                                                                                                                                                                                                          |
| Priorité<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ focus<br/>                             | FLOAT<br/> supérieures<br/>                                                            | Focus de la lumière. Cette propriété est sans unité et est définie entre 0 et 200.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitingConeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ - \_ angle limite du cône \_<br/> | FLOAT<br/> 90.0 f<br/>                                                           | Angle conique qui limite la zone dans laquelle la lumière est projetée. Aucune lumière n’est projetée à l’extérieur du cône. L’angle de cône limiteur est l’angle entre l’axe des tons directs (l’axe entre les propriétés *LightPosition* et *PointsAt* ) et le cône de lumière. Cette propriété est définie en degrés et doit être comprise entre 0 et 90 degrés.<br/>                                            |
| DiffuseConstant<br/> \_ \_ \_ Constante diffuse d2d1 SPOTDIFFUSE prop \_<br/>       | FLOAT<br/> supérieures<br/>                                                            | Rapport entre la réflexion diffuse et la quantité de lumière entrante. Cette propriété doit être comprise entre 0 et 10 000 et est sans unité. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> \_Échelle de surface d2d1 SPOTDIFFUSE \_ prop \_ \_<br/>             | FLOAT<br/> supérieures<br/>                                                            | Facteur d’échelle dans la direction Z. L’échelle de surface est sans unité et doit être comprise entre 0 et 10 000.<br/>                                                                                                                                                                                                                                                                                          |
| Couleur<br/> \_Couleur d2d1 SPOTDIFFUSE \_ prop \_<br/>                             | \_Vecteur d2d1 \_ 3F<br/> {1.0 f, 1.0 f, 1.0 f}<br/>                                   | Couleur de la lumière entrante. Cette propriété est exposée comme vecteur 3 (R, G, B) et utilisée pour calculer L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> Longueur de l' \_ unité de noyau d2d1 SPOTDIFFUSE \_ prop \_ \_ \_<br/>   | \_Vecteur d2d1 \_ 2F<br/> {1.0 f, 1.0 f}<br/>                                         | Taille d’un élément dans le noyau Sobel utilisé pour générer la surface normale dans les directions X et Y. Cette propriété est mappée aux valeurs DX et dy dans le dégradé Sobel. Cette propriété est un \_ vecteur d2d1 \_ 2F (longueur d’unité de noyau X, longueur d’unité de noyau Y) et est défini dans (DIP/unité noyau). L’effet utilise l’interpolation bilinéaire pour mettre à l’échelle l’image bitmap afin qu’elle corresponde à la taille des éléments de noyau.<br/> |
| Devient<br/> MODE de mise à l' \_ échelle d2d1 SPOTDIFFUSE \_ prop \_ \_<br/>                   | MODE de mise à l' \_ échelle d2d1 SPOTDIFFUSE \_ \_<br/> D2D1 mode de mise à l' \_ \_ échelle SPOTDIFFUSE \_ \_ linéaire<br/> | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle de la longueur de l’unité de noyau correspondante. Il existe six modes de mise à l’échelle qui vont de la qualité et de la vitesse. Pour plus d’informations, consultez modes de mise à l' [échelle](#scale-modes) .<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Modes de mise à l’échelle



| Énumération                                           | Description                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE de mise à l' \_ échelle d2d1 SPOTDIFFUSE \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 mode de mise à l' \_ \_ échelle SPOTDIFFUSE \_ \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode génère une image de qualité supérieure à celle du voisin le plus proche.                                                                                   |
| D2D1 mode de mise à l' \_ \_ échelle SPOTDIFFUSE \_ \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| MODE de mise à l' \_ échelle d2d1 SPOTDIFFUSE \_ multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode Scale \_ SPOTDIFFUSE \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ SPOTDIFFUSE \_ \_ en mode Scale de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ SPOTDIFFUSE \_ Scale \_ mode \_ linéaire.

 

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

 

