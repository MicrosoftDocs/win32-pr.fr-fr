---
description: La rotation dans un espace de couleurs à quatre dimensions est difficile à visualiser.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Rotation des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09a84c4c51181c672c549369783ac476fa1d3c79f1598c1c29ca14604429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036427"
---
# <a name="rotating-colors"></a>Rotation des couleurs

La rotation dans un espace de couleurs à quatre dimensions est difficile à visualiser. Nous pouvons faciliter la visualisation de la rotation en acceptant de conserver l’un des composants de couleur fixe. Supposons que nous acceptions de conserver le composant alpha fixe à 1 (entièrement opaque). Ensuite, nous pouvons visualiser un espace de couleurs à trois dimensions avec des axes rouge, vert et bleu, comme indiqué dans l’illustration suivante.

![illustration d’une vue en perspective d’un espace de couleurs à trois dimensions avec des axes intitulés rouge, vert et bleu](images/recoloring03.png)

Une couleur peut être considérée comme un point dans l’espace 3D. Par exemple, le point (1,0, 0) dans l’espace représente la couleur rouge et le point (0, 1, 0) de l’espace représente la couleur verte.

L’illustration suivante montre ce que cela signifie pour faire pivoter la couleur (1, 0, 0) à l’aide d’un angle de 60 degrés dans le plan Red-Green. La rotation d’un plan parallèle au plan de Red-Green peut être considérée comme une rotation autour de l’axe bleu.

![Illustration montrant le point (1, 0, 0) pivoté de 60 degrés à (0,5, 0,866, 0)](images/recoloring04.png)

L’illustration suivante montre comment initialiser une matrice de couleurs pour effectuer des rotations sur chacun des trois axes de coordonnées (rouge, vert, bleu).

![Illustration montrant des matrices de couleurs qui effectuent des rotations sur chacun des trois axes de coordonnées](images/recoloring05.png)

L’exemple suivant prend une image qui est une seule couleur (1, 0, 0,6) et applique une rotation de 60 degrés autour de l’axe bleu. L’angle de rotation est balayé dans un plan parallèle au plan de Red-Green.


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



L’illustration suivante montre l’image d’origine sur la gauche et l’image de rotation de couleur à droite.

![Illustration montrant des rectangles remplis avec l’image d’origine (rouge violet) et une image de rotation des couleurs (vert marin)](images/colortrans5.png)

La rotation des couleurs effectuée dans l’exemple de code précédent peut être visualisée comme suit.

![Illustration montrant un espace de couleurs 3D et le point (1, 0, 0,6) pivoté de 60 degrés vers (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



