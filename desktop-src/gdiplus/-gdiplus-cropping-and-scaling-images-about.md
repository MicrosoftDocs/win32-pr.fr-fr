---
title: À propos du rognage et de la mise à l’échelle d’images GDI+
description: Vous pouvez utiliser la méthode DrawImage de la classe Graphics pour dessiner et positionner des images.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115238"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>À propos du rognage et de la mise à l’échelle d’images GDI+

Vous pouvez utiliser la méthode [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour dessiner et positionner des images. DrawImage étant une méthode surchargée, il existe plusieurs façons de la fournir avec des arguments. Une variante de la méthode [**Graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) reçoit l’adresse d’un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) et une référence à un objet [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) . Le rectangle spécifie la destination de l’opération de dessin ; autrement dit, il spécifie le rectangle dans lequel l’image sera dessinée. Si la taille du rectangle de destination est différente de la taille de l’image d’origine, l’image est mise à l’échelle pour s’ajuster au rectangle de destination. L’exemple suivant dessine la même image trois fois : une fois sans mise à l’échelle, une fois avec une expansion et une fois avec une compression.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



Le code précédent, ainsi qu’un fichier particulier, Spiral.png, ont produit la sortie suivante.

![Illustration montrant trois versions d’une image : normale, étendue étendue et réduite à la moitié de la taille d’origine](images/aboutgdip03-art06.png)

Certaines variations de la méthode [**Graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) ont un paramètre de rectangle source, ainsi qu’un paramètre de rectangle de destination. Le rectangle source spécifie la partie de l’image d’origine qui sera dessinée. Le rectangle de destination spécifie l’emplacement où cette partie de l’image sera dessinée. Si la taille du rectangle de destination est différente de la taille du rectangle source, l’image est mise à l’échelle pour s’ajuster au rectangle de destination.

L’exemple suivant construit un objet [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) à partir du fichier Runner.jpg. La totalité de l’image est dessinée sans mise à l’échelle à (0,0). Une petite partie de l’image est ensuite dessinée deux fois : une fois avec une compression et une fois avec une expansion.


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



L’illustration suivante montre l’image non mise à l’échelle, ainsi que les parties de l’image compressée et développée.

![capture d’écran montrant une image, puis une partie de l’image compressée, puis la même partie développée](images/aboutgdip03-art07.png)

 

 



