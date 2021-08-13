---
title: Effet d’éclairage diffus distant
description: Utilisez l’effet d’éclairage diffus à distance pour créer une image qui semble être une surface non réfléchissante dans laquelle la source de lumière semble provenir d’une longue distance (comme les lumières de soleil ou de la caténaire) et la lumière est dispersée dans toutes les directions.
ms.assetid: 981FD58B-0565-4D0E-957C-3ED81BA8A6EB
keywords:
- effet d’éclairage diffus distant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f1860f196685c3d7dc0dcc30ae575cee70bc1eb0fcc29e8da7709c1174ee411
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260402"
---
# <a name="distant-diffuse-lighting-effect"></a>Effet d’éclairage diffus distant

Utilisez l’effet d’éclairage diffus à distance pour créer une image qui semble être une surface non réfléchissante dans laquelle la source de lumière semble provenir d’une longue distance (comme les lumières de soleil ou de la caténaire) et la lumière est dispersée dans toutes les directions. Cet effet utilise le canal alpha comme carte de hauteur et met en lumière l’image avec une source de lumière distante.

La couleur de la bitmap de sortie est un résultat de la couleur claire, de la position de la lumière et de la géométrie de surface de l’image. La sortie de canal alpha pour chaque pixel avec éclairage diffus est toujours 1,0.

Le CLSID de cet effet est CLSID \_ D2D1DistantDiffuse.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de mise à l’échelle](#scale-modes)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet d’éclairage diffus distant.

![exemple de capture d’écran des images d’entrée et de sortie de l’effet d’éclairage diffus distant.](images/distant-diffuse-example.png)

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimut<br/> D2D1 \_ DISTANTDIFFUSE \_ prop \_ azimut<br/>                       | Angle de direction de la source de lumière dans le plan XY par rapport à l’axe X dans la direction de l’horloge du compteur. Les unités sont en degrés et doivent être comprises entre 0 et 360 degrés.<br/> Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                                                                                                            |
| Elevation<br/> \_Élévation d2d1 DISTANTDIFFUSE \_ prop \_<br/>                   | Angle de direction de la source de lumière dans le plan YZ par rapport à l’axe Y dans la direction de l’horloge du compteur. Les unités sont en degrés et doivent être comprises entre 0 et 360 degrés. <br/> Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                                                                                                           |
| DiffuseConstant<br/> \_ \_ \_ Constante diffuse d2d1 DISTANTDIFFUSE prop \_<br/>     | Rapport entre la réflexion diffuse et la quantité de lumière entrante. Cette propriété doit être comprise entre 0 et 10 000 et est sans unité. <br/> Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                      |
| SurfaceScale<br/> \_Échelle de surface d2d1 DISTANTDIFFUSE \_ prop \_ \_<br/>           | Facteur d’échelle dans la direction Z. L’échelle de surface est sans unité et doit être comprise entre 0 et 10 000.<br/> Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Couleur<br/> \_Couleur d2d1 DISTANTDIFFUSE \_ prop \_<br/>                           | Couleur de la lumière entrante. Cette propriété est exposée en tant que \_ vecteur d2d1 \_ 3F (R, G, B) et utilisée pour calculer l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/> Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> Longueur de l' \_ unité de noyau d2d1 DISTANTDIFFUSE \_ prop \_ \_ \_<br/> | Taille d’un élément dans le noyau Sobel utilisé pour générer la surface normale dans les directions X et Y. Cette propriété est mappée aux valeurs DX et dy dans le dégradé Sobel. Cette propriété est un \_ vecteur d2d1 \_ 2F (longueur d’unité de noyau X, longueur d’unité de noyau Y) et est défini dans (DIP (Device-Independent Pixel). L’effet utilise l’interpolation bilinéaire pour mettre à l’échelle l’image bitmap afin qu’elle corresponde à la taille des éléments de noyau. <br/> Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {1.0 f, 1.0 f}.<br/> |
| Devient<br/> MODE de mise à l' \_ échelle d2d1 DISTANTDIFFUSE \_ prop \_ \_<br/>                 | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle de la longueur de l’unité de noyau correspondante. Il existe six modes de mise à l’échelle qui vont de la qualité et de la vitesse.<br/> Le type est D2D1 \_ DISTANTDIFFUSE \_ Scale \_ mode.<br/> La valeur par défaut est D2D1 \_ DISTANTDIFFUSE \_ Scale \_ mode \_ linéaire.<br/>                                                                                                                                                                                                                 |



 

## <a name="scale-modes"></a>Modes de mise à l’échelle



| Énumération                                              | Description                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE de mise à l' \_ échelle d2d1 DISTANTDIFFUSE \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 mode de mise à l' \_ \_ échelle DISTANTDIFFUSE \_ \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode génère une image de qualité supérieure à celle du voisin le plus proche.                                                                                   |
| D2D1 mode de mise à l' \_ \_ échelle DISTANTDIFFUSE \_ \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| MODE de mise à l' \_ échelle d2d1 DISTANTDIFFUSE \_ multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode Scale \_ DISTANTDIFFUSE \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ DISTANTDIFFUSE \_ \_ en mode Scale de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ DISTANTDIFFUSE \_ Scale \_ mode \_ linéaire.

 
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

 

