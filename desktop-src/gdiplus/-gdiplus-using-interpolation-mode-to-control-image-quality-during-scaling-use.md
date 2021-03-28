---
description: Le mode d’interpolation d’un objet Graphics influence la manière dont GDI+ met à l’échelle (étire et réduit) les images.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Utilisation du mode d’interpolation pour contrôler la qualité d’image pendant la mise à l’échelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972138"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Utilisation du mode d’interpolation pour contrôler la qualité d’image pendant la mise à l’échelle

Le mode d’interpolation d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influence la manière dont GDI+ met à l’échelle (étire et réduit) les images. L’énumération [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) dans Gdiplusenums. h définit plusieurs modes d’interpolation, dont certains sont répertoriés dans la liste suivante :

-   InterpolationModeNearestNeighbor
-   InterpolationModeBilinear
-   InterpolationModeHighQualityBilinear
-   InterpolationModeBicubic
-   InterpolationModeHighQualityBicubic

Pour étirer une image, chaque pixel de l’image d’origine doit être mappé à un groupe de pixels dans l’image de plus grande taille. Pour réduire une image, les groupes de pixels de l’image d’origine doivent être mappés à des pixels uniques dans l’image de petite taille. L’efficacité des algorithmes qui effectuent ces mappages détermine la qualité d’une image mise à l’échelle. Les algorithmes qui produisent des images mises à l’échelle de qualité supérieure ont tendance à nécessiter plus de temps de traitement. Dans la liste précédente, InterpolationModeNearestNeighbor est le mode de qualité la plus faible et InterpolationModeHighQualityBicubic est le mode de qualité le plus élevé.

Pour définir le mode d’interpolation, transmettez l’un des membres de l’énumération [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) à la méthode **SetInterpolationMode** d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

L’exemple suivant dessine une image, puis réduit la taille de l’image à l’aide de trois modes d’interpolation différents :


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



L’illustration suivante montre l’image d’origine et les trois images plus petites.

![Illustration montrant une image originale de grande taille et trois images plus petites de qualité variable](images/grapes1.png)

 

 



