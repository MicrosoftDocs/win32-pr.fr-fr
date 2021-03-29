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
# <a name="drawing-positioning-and-cloning-images"></a><span data-ttu-id="1d36e-103">Dessin, positionnement et clonage d’images</span><span class="sxs-lookup"><span data-stu-id="1d36e-103">Drawing, Positioning, and Cloning Images</span></span>

<span data-ttu-id="1d36e-104">Vous pouvez utiliser la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) pour charger et afficher des images raster (bitmaps) et des images vectorielles (sous-fichiers).</span><span class="sxs-lookup"><span data-stu-id="1d36e-104">You can use the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class to load and display raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="1d36e-105">Pour afficher une image, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet **image** .</span><span class="sxs-lookup"><span data-stu-id="1d36e-105">To display an image, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and an **Image** object.</span></span> <span data-ttu-id="1d36e-106">L’objet **Graphics** fournit la méthode [**graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , qui reçoit l’adresse de l’objet **image** sous la forme d’un argument.</span><span class="sxs-lookup"><span data-stu-id="1d36e-106">The **Graphics** object provides the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method, which receives the address of the **Image** object as an argument.</span></span>

<span data-ttu-id="1d36e-107">L’exemple suivant construit un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier Climber.jpg puis affiche l’image.</span><span class="sxs-lookup"><span data-stu-id="1d36e-107">The following example constructs an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Climber.jpg and then displays the image.</span></span> <span data-ttu-id="1d36e-108">Le point de destination pour l’angle supérieur gauche de l’image, (10, 10), est spécifié dans les deuxième et troisième paramètres de la méthode [**Graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="1d36e-108">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method.</span></span>


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



<span data-ttu-id="1d36e-109">Le code précédent, ainsi qu’un fichier particulier, Climber.jpg, ont produit la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="1d36e-109">The preceding code, along with a particular file, Climber.jpg, produced the following output.</span></span>

![capture d’écran d’une fenêtre contenant une photo](images/aboutgdip03-art04.png)

<span data-ttu-id="1d36e-111">Vous pouvez construire des objets [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir de différents formats de fichiers graphiques : BMP, GIF, JPEG, EXIF, png, TIFF, WMF, EMF et Icon.</span><span class="sxs-lookup"><span data-stu-id="1d36e-111">You can construct [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of graphics file formats: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF, and ICON.</span></span>

<span data-ttu-id="1d36e-112">L’exemple suivant construit des objets [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir de divers types de fichiers, puis affiche les images.</span><span class="sxs-lookup"><span data-stu-id="1d36e-112">The following example constructs [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of file types and then displays the images.</span></span>


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



<span data-ttu-id="1d36e-113">La classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) fournit une [**méthode image :: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) que vous pouvez utiliser pour effectuer une copie d’une **image**, d’un [**métafichier**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)ou d’un objet [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) existant.</span><span class="sxs-lookup"><span data-stu-id="1d36e-113">The [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class provides a [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) method that you can use to make a copy of an existing **Image**, [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile), or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="1d36e-114">La méthode [clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) est surchargée dans la classe **bitmap** , et l’une des variantes a un paramètre rectangle source que vous pouvez utiliser pour spécifier la partie de l’image d’origine que vous souhaitez copier.</span><span class="sxs-lookup"><span data-stu-id="1d36e-114">The [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) method is overloaded in the **Bitmap** class, and one of the variations has a source-rectangle parameter that you can use to specify the portion of the original image that you want to copy.</span></span> <span data-ttu-id="1d36e-115">L’exemple suivant crée un objet **bitmap** en clonant la moitié supérieure d’un objet **bitmap** existant.</span><span class="sxs-lookup"><span data-stu-id="1d36e-115">The following example creates a **Bitmap** object by cloning the top half of an existing **Bitmap** object.</span></span> <span data-ttu-id="1d36e-116">Les deux images sont alors affichées.</span><span class="sxs-lookup"><span data-stu-id="1d36e-116">Then both images are displayed.</span></span>


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



<span data-ttu-id="1d36e-117">Le code précédent, ainsi qu’un fichier particulier, Spiral.png, ont produit la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="1d36e-117">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![illustration d’une image, suivie de la moitié supérieure de l’image replacer](images/aboutgdip03-art05.png)

 

 
