---
title: Effet d’éclairage spéculaire distant
description: Utilisez l’effet d’éclairage spéculaire à distance pour créer une image qui semble être une surface réfléchissante dans laquelle la source de lumière semble provenir d’une longue distance (telle que le soleil ou les lumières de la caténaire).
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- éclairage spéculaire distant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fa21553e36839f854b4567b2aa2a3805406380
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113265"
---
# <a name="distant-specular-lighting-effect"></a>Effet d’éclairage spéculaire distant

Utilisez l’effet d’éclairage spéculaire à distance pour créer une image qui semble être une surface réfléchissante dans laquelle la source de lumière semble provenir d’une longue distance (telle que le soleil ou les lumières de la caténaire). Cet effet utilise le canal alpha comme carte de hauteur et met en lumière l’image avec une source de lumière distante.

La couleur de l’image bitmap de sortie est un résultat de la couleur claire, de la position de la lumière et de la géométrie de la surface. La sortie de canal alpha pour chaque pixel avec éclairage spéculaire est le nombre maximal de sorties de canal rouge, vert et bleu pour ce pixel.

Le CLSID de cet effet est CLSID \_ D2D1DistantSpecular.

-   [Exemple d’image](#example-image)
-   [Source de lumière distante](#distant-light-source)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de mise à l’échelle](#scale-modes)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet d’éclairage spéculaire distant.

![exemple de capture d’écran montrant les images d’entrée et de sortie de l’effet d’éclairage spéculaire distant. ](images/distant-spec-example.png)

La bitmap de sortie finale peut être calculée à l’aide des équations suivantes.

![calcul de bitmap de sortie](images/distant-spec-formula1.png)

where <dl> DK? = constante d’éclairage spéculaire.  
![symbole de surface normal. ](images/point-spec-mathchar-n.png) = vecteur d’unité normale de surface.  
![symbole de vecteur à mi-chemin. ](images/point-spec-mathchar-h.png) = vecteur d’unité « mi » entre le vecteur d’unité oculaire et le vecteur d’unité clair.  
C<sub>r</sub>, c<sub>g</sub>, c<sub>b</sub> = couleur claire dans les composants RVB.  
</dl>

## <a name="distant-light-source"></a>Source de lumière distante

L’image ici montre un exemple de la direction de la lumière à partir d’une source de lumière distante.

![source de lumière distante](images/distant-spec-lightsource.png)

L’effet utilise les paramètres d’azimut et d’élévation pour calculer le vecteur clair ![vecteur l.](images/distant-spec-mathchar-l.png) à l’aide des équations suivantes :

![calcul de vecteur léger](images/distant-spec-formula2.png)

où Light ?, Light<sub>y</sub>et Light<sub>z</sub> sont les valeurs de position de la lumière d’entrée.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimut<br/> D2D1 \_ DISTANTSPECULAR \_ prop \_ azimut<br/>                       | Angle de direction de la source de lumière dans le plan XY par rapport à l’axe X dans la direction de l’horloge du compteur. Les unités sont en degrés et doivent être comprises entre 0 et 360 degrés.<br/> Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                              |
| Elevation<br/> \_Élévation d2d1 DISTANTSPECULAR \_ prop \_<br/>                   | Angle de direction de la source de lumière dans le plan YZ par rapport à l’axe Y dans la direction de l’horloge du compteur. Les unités sont en degrés et doivent être comprises entre 0 et 360 degrés. <br/> Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                             |
| SpecularExponent<br/> \_ \_ \_ Exposant spéculaire d2d1 DISTANTSPECULAR prop \_<br/>   | Exposant du terme spéculaire dans l’équation d’éclairage Phong. Une plus grande valeur correspond à une surface plus réfléchissante. La valeur est sans unité et doit être comprise entre 1,0 et 128. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                          |
| SpecularConstant<br/> \_ \_ \_ Constante spéculaire d2d1 DISTANTSPECULAR prop \_<br/>   | Rapport entre la réflexion spéculaire et la lumière entrante. La valeur est sans unité et doit être comprise entre 0 et 10 000. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                             |
| SurfaceScale<br/> \_Échelle de surface d2d1 DISTANTSPECULAR \_ prop \_ \_<br/>           | Facteur d’échelle dans la direction Z. La valeur est sans unité et doit être comprise entre 0 et 10 000. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                |
| Couleur<br/> \_Couleur d2d1 DISTANTSPECULAR \_ prop \_<br/>                           | Couleur de la lumière entrante. Cette propriété est exposée en tant que \_ vecteur d2d1 \_ 3F (R, G, B) et utilisée pour calculer l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                       |
| KernelUnitLength<br/> Longueur de l' \_ unité de noyau d2d1 DISTANTSPECULAR \_ prop \_ \_ \_<br/> | Taille d’un élément dans le noyau Sobel utilisé pour générer la surface normale dans les directions X et Y. Cette propriété est un \_ vecteur d2d1 \_ 2F (longueur d’unité de noyau X, longueur d’unité de noyau Y) et est défini dans (DIP (Device-Independent Pixel). L’effet utilise l’interpolation bilinéaire pour mettre à l’échelle l’image bitmap afin qu’elle corresponde à la taille des éléments de noyau. Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {1.0 f, 1.0 f}.<br/> |
| Devient<br/> MODE de mise à l' \_ échelle d2d1 DISTANTSPECULAR \_ prop \_ \_<br/>                 | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle de la longueur de l’unité de noyau correspondante. Il existe six modes de mise à l’échelle qui vont de la qualité et de la vitesse.<br/> Le type est D2D1 \_ DISTANTSPECULAR \_ Scale \_ mode.<br/> La valeur par défaut est D2D1 \_ DISTANTSPECULAR \_ Scale \_ mode \_ linéaire.<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>Modes de mise à l’échelle



| Énumération                                               | Description                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE de mise à l' \_ échelle d2d1 DISTANTSPECULAR \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 mode de mise à l' \_ \_ échelle DISTANTSPECULAR \_ \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode génère une image de qualité supérieure à celle du voisin le plus proche.                                                                                   |
| D2D1 mode de mise à l' \_ \_ échelle DISTANTSPECULAR \_ \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| MODE de mise à l' \_ échelle d2d1 DISTANTSPECULAR \_ multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode Scale \_ DISTANTSPECULAR \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ DISTANTSPECULAR \_ \_ en mode Scale de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ DISTANTSPECULAR \_ Scale \_ mode \_ linéaire.

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

 

