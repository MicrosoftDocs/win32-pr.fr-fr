---
title: Rognage et mise à l’échelle d’images GDI+
description: La classe Graphics fournit plusieurs méthodes DrawImage, dont certaines ont des paramètres de rectangle source et de destination que vous pouvez utiliser pour rogner et mettre à l’échelle des images.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988328"
---
# <a name="cropping-and-scaling-gdi-images"></a>Rognage et mise à l’échelle d’images GDI+

La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit plusieurs méthodes **DrawImage** , dont certaines ont des paramètres de rectangle source et de destination que vous pouvez utiliser pour rogner et mettre à l’échelle des images.

L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier Apple.gif. Le code dessine la totalité de l’image Apple dans sa taille d’origine. Le code appelle ensuite la méthode **DrawImage** d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour dessiner une partie de l’image Apple dans un rectangle de destination qui est plus grand que l’image Apple d’origine.

La méthode **DrawImage** détermine la partie de l’Apple à dessiner en examinant le rectangle source, qui est spécifié par les troisième, quatrième, cinquième et sixième arguments. Dans ce cas, l’Apple est rognée à 75% de sa largeur et à 75% de sa hauteur.

La méthode **DrawImage** détermine où dessiner l’Apple rognée et la taille de la pomme rognée en regardant le rectangle de destination, qui est spécifié par le deuxième argument. Dans ce cas, le rectangle de destination est 30 pour cent de largeur et 30 pour cent plus haut que l’image d’origine.


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



L’illustration suivante montre l’Apple d’origine et le pommier mis à l’échelle et rogné.

![Illustration montrant une pomme, puis une partie agrandie de la pomme d’origine](images/cropscale1.png)

 

 



