---
description: L’une des propriétés de la classe Graphics est la zone de découpage. Tout le dessin effectué par un objet Graphics donné est limité à la zone de découpage de cet objet Graphics. Vous pouvez définir la région de découpage en appelant la méthode SetClip.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Découpage avec une région
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa19426d62d5d3af99150bf9ac8e8099628fe2f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564062"
---
# <a name="clipping-with-a-region"></a><span data-ttu-id="28251-105">Découpage avec une région</span><span class="sxs-lookup"><span data-stu-id="28251-105">Clipping with a Region</span></span>

<span data-ttu-id="28251-106">L’une des propriétés de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est la zone de découpage.</span><span class="sxs-lookup"><span data-stu-id="28251-106">One of the properties of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the clipping region.</span></span> <span data-ttu-id="28251-107">Tout le dessin effectué par un objet **Graphics** donné est limité à la zone de découpage de cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="28251-107">All drawing done by a given **Graphics** object is restricted to the clipping region of that **Graphics** object.</span></span> <span data-ttu-id="28251-108">Vous pouvez définir la région de découpage en appelant la méthode **SetClip** .</span><span class="sxs-lookup"><span data-stu-id="28251-108">You can set the clipping region by calling the **SetClip** method.</span></span>

<span data-ttu-id="28251-109">L’exemple suivant construit un tracé qui se compose d’un seul polygone.</span><span class="sxs-lookup"><span data-stu-id="28251-109">The following example constructs a path that consists of a single polygon.</span></span> <span data-ttu-id="28251-110">Ensuite, le code construit une région basée sur ce chemin.</span><span class="sxs-lookup"><span data-stu-id="28251-110">Then the code constructs a region based on that path.</span></span> <span data-ttu-id="28251-111">L’adresse de la région est passée à la méthode **SetClip** d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , puis deux chaînes sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="28251-111">The address of the region is passed to the **SetClip** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, and then two strings are drawn.</span></span>


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



<span data-ttu-id="28251-112">L’illustration suivante montre les chaînes découpées.</span><span class="sxs-lookup"><span data-stu-id="28251-112">The following illustration shows the clipped strings.</span></span>

![Illustration montrant des parties de deux phrases apparaissant à l’intérieur d’une forme à quatre côtés](images/clip1.png)

 

 



