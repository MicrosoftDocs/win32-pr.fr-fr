---
description: Vous pouvez utiliser la classe image pour charger et afficher des images raster (bitmaps) et des images vectorielles (sous-fichiers).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Dessin, positionnement et clonage d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa265a8f75cbfcaf0ff614ded4466482e5b986b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202425"
---
# <a name="drawing-positioning-and-cloning-images"></a>Dessin, positionnement et clonage d’images

Vous pouvez utiliser la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) pour charger et afficher des images raster (bitmaps) et des images vectorielles (sous-fichiers). Pour afficher une image, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet **image** . L’objet **Graphics** fournit la méthode [**graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , qui reçoit l’adresse de l’objet **image** sous la forme d’un argument.

L’exemple suivant construit un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier Climber.jpg puis affiche l’image. Le point de destination pour l’angle supérieur gauche de l’image, (10, 10), est spécifié dans les deuxième et troisième paramètres de la méthode [**Graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



Le code précédent, ainsi qu’un fichier particulier, Climber.jpg, ont produit la sortie suivante.

![capture d’écran d’une fenêtre contenant une photo](images/aboutgdip03-art04.png)

Vous pouvez construire des objets [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir de différents formats de fichiers graphiques : BMP, GIF, JPEG, EXIF, png, TIFF, WMF, EMF et Icon.

L’exemple suivant construit des objets [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir de divers types de fichiers, puis affiche les images.


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



La classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) fournit une [**méthode image :: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) que vous pouvez utiliser pour effectuer une copie d’une **image**, d’un [**métafichier**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)ou d’un objet [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) existant. La méthode [clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) est surchargée dans la classe **bitmap** , et l’une des variantes a un paramètre rectangle source que vous pouvez utiliser pour spécifier la partie de l’image d’origine que vous souhaitez copier. L’exemple suivant crée un objet **bitmap** en clonant la moitié supérieure d’un objet **bitmap** existant. Les deux images sont alors affichées.


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



Le code précédent, ainsi qu’un fichier particulier, Spiral.png, ont produit la sortie suivante.

![illustration d’une image, suivie de la moitié supérieure de l’image replacer](images/aboutgdip03-art05.png)

 

 
