---
title: Effet d’éclairage spéculaire par spot
description: Utilisez l’effet d’éclairage spéculaire pour créer une image qui semble être une surface réfléchissante dans laquelle la source de lumière est limitée à un cône dirigé de lumière.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- détecter l’éclairage spéculaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9edc4c75eaa17369ba0d0d9f1838d8857053def9aaab3dacceb8bf761b9c04c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000374"
---
# <a name="spot-specular-lighting-effect"></a>Effet d’éclairage spéculaire par spot

Utilisez l’effet d’éclairage spéculaire pour créer une image qui semble être une surface réfléchissante dans laquelle la source de lumière est limitée à un cône dirigé de lumière. Cet effet utilise le canal alpha comme carte de hauteur et met en lumière l’image avec une source de lumière de point.

La couleur de la bitmap de sortie est un résultat de la couleur claire, de la position claire, de la direction du cône et de la géométrie de la surface en fonction de la partie spéculaire du modèle d’éclairage Phong. La sortie de canal alpha pour chaque pixel avec éclairage spéculaire est le nombre maximal de sorties de canal rouge, vert et bleu pour ce pixel.

Le CLSID de cet effet est CLSID \_ D2D1SpotSpecular.

-   [Exemple d’image](#example-image)
-   [Source de lumière ponctuelle](#spot-light-source)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de mise à l’échelle](#scale-modes)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet d’éclairage spéculaire.

![capture d’écran de l’exemple d’effet.](images/spot-spec-example.png)

La lumière spéculaire fait référence à la lumière qui est reflétée dans une direction particulière.

![diagramme des vecteurs utilisés pour cacluate une sortie d’éclairage spéculaire pour une image bitmap.](images/point-spec-reflected1.png)

L’effet calcule les valeurs de pixel de sortie finales est calculé à l’aide des équations ici :

![équations de pixels de sortie.](images/spot-formula1.png)

where

![définitions de variables.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Source de lumière ponctuelle

Une source de lumière des points émet une lumière dans un cône dans une direction spécifique et n’émet pas de lumière en dehors du cône.

La source de lumière des points calcule le vecteur clair L et le vecteur H à mi-chemin de la même façon que l’effet [de point-spéculaire](point-specular.md) .

L’effet calcule la couleur claire, L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub>, en tant que fonction de position de la source de lumière, comme illustré par les équations ici :

![équation pour la source de lumière de spot](images/spot-formula3.png)

Le vecteur ![symbole de vecteur clair.](images/spot-mathchar-l.png) est défini par les équations suivantes :

![équation : Vector](images/spot-formula4.png)

Le vecteur ![symbole de vecteur t](images/spot-mathchar-t.png) est défini par les équations suivantes :

![équation : Vector 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> POSITION de la \_ lumière d2d1 SPOTSPECULAR \_ prop \_ \_<br/>             | Position claire de la source de lumière de point. La propriété est un \_ vecteur d2d1 \_ 3F défini en tant que (x, y, z). Les unités sont en pixels indépendants du périphérique (DIP) et ne sont pas liées. Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                                              |
| PointsAt<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ points \_ à<br/>                       | Où le feu est concentré. La propriété est exposée sous la forme d’un \_ vecteur d2d1 \_ 3F avec (x, y, z). Les unités sont dans des DIP et les valeurs ne sont pas liées. Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                                                                     |
| Priorité<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ focus<br/>                               | Focus de la lumière. Cette propriété est sans unité et est définie entre 0 et 200. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                          |
| LimitingConeAngle<br/> D2D1 \_ angle de cône de la \_ cale spéculaire \_ \_ limite \_ \_<br/> | Angle conique qui limite la zone dans laquelle la lumière est projetée. Aucune lumière n’est projetée à l’extérieur du cône. L’angle de cône limiteur est l’angle entre l’axe des tons directs (l’axe entre les propriétés *LightPosition* et *PointsAt* ) et le cône de lumière. Cette propriété est définie en degrés et doit être comprise entre 0 et 90 degrés. Le type est FLOAT.<br/> La valeur par défaut est 90.0 f.<br/>                                                               |
| SpecularExponent<br/> \_ \_ \_ Exposant spéculaire d2d1 SPOTSPECULAR prop \_<br/>       | Exposant du terme spéculaire dans l’équation d’éclairage Phong. Une plus grande valeur correspond à une surface plus réfléchissante. Cette valeur est sans unité et doit être comprise entre 1,0 et 128. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> \_ \_ \_ Constante spéculaire d2d1 SPOTSPECULAR prop \_<br/>       | Rapport entre la réflexion spéculaire et la lumière entrante. La valeur est sans unité et doit être comprise entre 0 et 10 000. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> \_Échelle de surface d2d1 SPOTSPECULAR \_ prop \_ \_<br/>               | Facteur d’échelle dans la direction Z pour la génération d’une carte de hauteur. La valeur est sans unité et doit être comprise entre 0 et 10 000. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Couleur<br/> \_Couleur d2d1 SPOTSPECULAR \_ prop \_<br/>                               | Couleur de la lumière entrante. Cette propriété est exposée comme vecteur 3 (R, G, B) et utilisée pour calculer L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> Longueur de l' \_ unité de noyau d2d1 SPOTSPECULAR \_ prop \_ \_ \_<br/>     | Taille d’un élément dans le noyau Sobel utilisé pour générer la surface normale dans les directions X et Y. Cette propriété est mappée aux valeurs DX et dy dans le dégradé Sobel. Cette propriété est un \_ vecteur d2d1 \_ 2F (longueur d’unité de noyau X, longueur d’unité de noyau Y) et est défini dans (DIP/unité noyau). L’effet utilise l’interpolation bilinéaire pour mettre à l’échelle l’image bitmap afin qu’elle corresponde à la taille des éléments de noyau. Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {1.0 f, 1.0 f}.<br/> |
| Devient<br/> MODE de mise à l' \_ échelle d2d1 SPOTSPECULAR \_ prop \_ \_<br/>                     | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle de la longueur de l’unité de noyau correspondante. Il existe six modes de mise à l’échelle qui vont de la qualité et de la vitesse. Pour plus d’informations, consultez modes de mise à l' [échelle](#scale-modes) . <br/> Le type est D2D1 \_ SPOTSPECULAR \_ Scale \_ mode.<br/> La valeur par défaut est D2D1 \_ SPOTSPECULAR \_ Scale \_ mode \_ linéaire.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Modes de mise à l’échelle



| Énumération                                            | Description                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE de mise à l' \_ échelle d2d1 SPOTSPECULAR \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 mode de mise à l' \_ \_ échelle SPOTSPECULAR \_ \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode génère une image de qualité supérieure à celle du voisin le plus proche.                                                                                   |
| D2D1 mode de mise à l' \_ \_ échelle SPOTSPECULAR \_ \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| MODE de mise à l' \_ échelle d2d1 SPOTSPECULAR \_ multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode Scale \_ SPOTSPECULAR \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ SPOTSPECULAR \_ \_ en mode Scale de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ SPOTSPECULAR \_ Scale \_ mode \_ linéaire.

## <a name="requirements"></a>Configuration requise



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

 

