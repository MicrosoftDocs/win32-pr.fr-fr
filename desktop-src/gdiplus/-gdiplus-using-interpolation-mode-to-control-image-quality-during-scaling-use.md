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
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="2f394-103">Utilisation du mode d’interpolation pour contrôler la qualité d’image pendant la mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="2f394-103">Using Interpolation Mode to Control Image Quality During Scaling</span></span>

<span data-ttu-id="2f394-104">Le mode d’interpolation d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influence la manière dont GDI+ met à l’échelle (étire et réduit) les images.</span><span class="sxs-lookup"><span data-stu-id="2f394-104">The interpolation mode of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object influences the way Windows GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="2f394-105">L’énumération [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) dans Gdiplusenums. h définit plusieurs modes d’interpolation, dont certains sont répertoriés dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="2f394-105">The [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration in Gdiplusenums.h defines several interpolation modes, some of which are shown in the following list:</span></span>

-   <span data-ttu-id="2f394-106">InterpolationModeNearestNeighbor</span><span class="sxs-lookup"><span data-stu-id="2f394-106">InterpolationModeNearestNeighbor</span></span>
-   <span data-ttu-id="2f394-107">InterpolationModeBilinear</span><span class="sxs-lookup"><span data-stu-id="2f394-107">InterpolationModeBilinear</span></span>
-   <span data-ttu-id="2f394-108">InterpolationModeHighQualityBilinear</span><span class="sxs-lookup"><span data-stu-id="2f394-108">InterpolationModeHighQualityBilinear</span></span>
-   <span data-ttu-id="2f394-109">InterpolationModeBicubic</span><span class="sxs-lookup"><span data-stu-id="2f394-109">InterpolationModeBicubic</span></span>
-   <span data-ttu-id="2f394-110">InterpolationModeHighQualityBicubic</span><span class="sxs-lookup"><span data-stu-id="2f394-110">InterpolationModeHighQualityBicubic</span></span>

<span data-ttu-id="2f394-111">Pour étirer une image, chaque pixel de l’image d’origine doit être mappé à un groupe de pixels dans l’image de plus grande taille.</span><span class="sxs-lookup"><span data-stu-id="2f394-111">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="2f394-112">Pour réduire une image, les groupes de pixels de l’image d’origine doivent être mappés à des pixels uniques dans l’image de petite taille.</span><span class="sxs-lookup"><span data-stu-id="2f394-112">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="2f394-113">L’efficacité des algorithmes qui effectuent ces mappages détermine la qualité d’une image mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="2f394-113">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="2f394-114">Les algorithmes qui produisent des images mises à l’échelle de qualité supérieure ont tendance à nécessiter plus de temps de traitement.</span><span class="sxs-lookup"><span data-stu-id="2f394-114">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="2f394-115">Dans la liste précédente, InterpolationModeNearestNeighbor est le mode de qualité la plus faible et InterpolationModeHighQualityBicubic est le mode de qualité le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="2f394-115">In the preceding list, InterpolationModeNearestNeighbor is the lowest-quality mode and InterpolationModeHighQualityBicubic is the highest-quality mode.</span></span>

<span data-ttu-id="2f394-116">Pour définir le mode d’interpolation, transmettez l’un des membres de l’énumération [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) à la méthode **SetInterpolationMode** d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="2f394-116">To set the interpolation mode, pass one of the members of the [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration to the **SetInterpolationMode** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="2f394-117">L’exemple suivant dessine une image, puis réduit la taille de l’image à l’aide de trois modes d’interpolation différents :</span><span class="sxs-lookup"><span data-stu-id="2f394-117">The following example draws an image and then shrinks the image with three different interpolation modes:</span></span>


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



<span data-ttu-id="2f394-118">L’illustration suivante montre l’image d’origine et les trois images plus petites.</span><span class="sxs-lookup"><span data-stu-id="2f394-118">The following illustration shows the original image and the three smaller images.</span></span>

![Illustration montrant une image originale de grande taille et trois images plus petites de qualité variable](images/grapes1.png)

 

 



