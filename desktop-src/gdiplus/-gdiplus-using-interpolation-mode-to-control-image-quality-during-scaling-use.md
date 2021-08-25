---
description: le mode d’interpolation d’un objet graphics influe sur la façon dont Windows GDI+ met à l’échelle les images.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Utilisation du mode d’interpolation pour contrôler la qualité d’image pendant la mise à l’échelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fefe314ef680a54f9d885bb185c77b3349e84cbe5f7bcf347cf9ff3fa0a4ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943699"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Utilisation du mode d’interpolation pour contrôler la qualité d’image pendant la mise à l’échelle

le mode d’interpolation d’un objet [**graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influe sur la façon dont Windows GDI+ met à l’échelle les images. L’énumération [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) dans Gdiplusenums. h définit plusieurs modes d’interpolation, dont certains sont répertoriés dans la liste suivante :

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

 

 



