---
description: Le remappage est le processus de conversion des couleurs d’une image en fonction d’une table de remappage des couleurs. La table de remappage des couleurs est un tableau de structures ColorMap. Chaque structure ColorMap du tableau a un membre oldColor et un membre newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Utilisation d’une table de remappage des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112939"
---
# <a name="using-a-color-remap-table"></a><span data-ttu-id="99eea-105">Utilisation d’une table de remappage des couleurs</span><span class="sxs-lookup"><span data-stu-id="99eea-105">Using a Color Remap Table</span></span>

<span data-ttu-id="99eea-106">Le remappage est le processus de conversion des couleurs d’une image en fonction d’une table de remappage des couleurs.</span><span class="sxs-lookup"><span data-stu-id="99eea-106">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="99eea-107">La table de remappage des couleurs est un tableau de structures [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="99eea-107">The color remap table is an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="99eea-108">Chaque structure **ColorMap** du tableau a un membre **oldColor** et un membre **NewColor** .</span><span class="sxs-lookup"><span data-stu-id="99eea-108">Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.</span></span>

<span data-ttu-id="99eea-109">Lorsque GDI+ dessine une image, chaque pixel de l’image est comparé au tableau des anciennes couleurs.</span><span class="sxs-lookup"><span data-stu-id="99eea-109">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="99eea-110">Si la couleur d’un pixel correspond à une ancienne couleur, sa couleur est remplacée par la nouvelle couleur correspondante.</span><span class="sxs-lookup"><span data-stu-id="99eea-110">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="99eea-111">Les couleurs sont modifiées uniquement pour le rendu : les valeurs de couleur de l’image elle-même (stockées dans une [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ou un objet [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) ne sont pas modifiées.</span><span class="sxs-lookup"><span data-stu-id="99eea-111">The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object) are not changed.</span></span>

<span data-ttu-id="99eea-112">Pour dessiner une image remappée, initialisez un tableau de structures [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="99eea-112">To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="99eea-113">Transmettez l’adresse de ce tableau à la méthode [**ImageAttributes :: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) d’un objet [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , puis transmettez l’adresse de l’objet **ImageAttributes** à la méthode [DrawImage des méthodes](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="99eea-113">Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) method of an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="99eea-114">L’exemple suivant crée un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier RemapInput.bmp.</span><span class="sxs-lookup"><span data-stu-id="99eea-114">The following example creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file RemapInput.bmp.</span></span> <span data-ttu-id="99eea-115">Le code crée une table de remappage des couleurs qui se compose d’une structure [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) unique.</span><span class="sxs-lookup"><span data-stu-id="99eea-115">The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structure.</span></span> <span data-ttu-id="99eea-116">Le membre **oldColor** de la structure **ColorMap** est rouge et le membre **NewColor** est bleu.</span><span class="sxs-lookup"><span data-stu-id="99eea-116">The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue.</span></span> <span data-ttu-id="99eea-117">L’image est dessinée une seule fois sans remappage et une fois avec le remappage.</span><span class="sxs-lookup"><span data-stu-id="99eea-117">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="99eea-118">Le processus de remappage remplace tous les pixels rouges par le bleu.</span><span class="sxs-lookup"><span data-stu-id="99eea-118">The remapping process changes all the red pixels to blue.</span></span>


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="99eea-119">L’illustration suivante montre l’image d’origine à gauche et l’image remappée à droite.</span><span class="sxs-lookup"><span data-stu-id="99eea-119">The following illustration shows the original image on the left and the remapped image on the right.</span></span>

![Illustration montrant deux versions d’une image multicolore ; la région rouge de la première version est bleue dans la deuxième version](images/colortrans7.png)

 

 



