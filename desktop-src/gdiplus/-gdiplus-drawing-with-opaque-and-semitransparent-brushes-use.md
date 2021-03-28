---
description: Lorsque vous remplissez une forme, vous devez passer l’adresse d’un objet Brush à l’une des méthodes de remplissage de la classe Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Dessiner avec des pinceaux opaques et translucides
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115234"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a><span data-ttu-id="cb9c8-103">Dessiner avec des pinceaux opaques et translucides</span><span class="sxs-lookup"><span data-stu-id="cb9c8-103">Drawing with Opaque and Semitransparent Brushes</span></span>

<span data-ttu-id="cb9c8-104">Lorsque vous remplissez une forme, vous devez passer l’adresse d’un objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) à l’une des méthodes de remplissage de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="cb9c8-104">When you fill a shape, you must pass the address of a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="cb9c8-105">Le paramètre un du constructeur [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) est un objet [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="cb9c8-105">The one parameter of the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor is a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="cb9c8-106">Pour remplir une forme opaque, affectez au composant alpha de la couleur la valeur 255.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-106">To fill an opaque shape, set the alpha component of the color to 255.</span></span> <span data-ttu-id="cb9c8-107">Pour remplir une forme translucide, affectez au composant alpha n'importe quelle valeur comprise entre 1 et 254.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-107">To fill a semitransparent shape, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="cb9c8-108">Quand vous remplissez une forme translucide, la couleur de la forme est fusionnée avec les couleurs d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-108">When you fill a semitransparent shape, the color of the shape is blended with the colors of the background.</span></span> <span data-ttu-id="cb9c8-109">Le composant alpha spécifie comment les couleurs de forme et d’arrière-plan sont mélangées. les valeurs alpha proches de 0 placent plus de poids sur les couleurs d’arrière-plan, tandis que les valeurs alpha proches de 255 placent plus peser sur la couleur de la forme.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-109">The alpha component specifies how the shape and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the shape color.</span></span>

<span data-ttu-id="cb9c8-110">L’exemple suivant dessine une image, puis remplit trois points de suspension qui chevauchent l’image.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-110">The following example draws an image and then fills three ellipses that overlap the image.</span></span> <span data-ttu-id="cb9c8-111">La première ellipse utilise un composant alpha de 255. Elle est donc opaque.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-111">The first ellipse uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="cb9c8-112">Les deuxième et troisième ellipses utilisent un composant alpha de 128 et sont donc translucides. Vous pouvez voir l'image d'arrière-plan à travers les ellipses.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-112">The second and third ellipses use an alpha component of 128, so they are semitransparent; you can see the background image through the ellipses.</span></span> <span data-ttu-id="cb9c8-113">L’appel à [**Graphics :: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) fait en sorte que la fusion de la troisième ellipse soit effectuée conjointement avec la correction gamma.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-113">The call to [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third ellipse to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



<span data-ttu-id="cb9c8-114">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="cb9c8-114">The following illustration shows the output of the preceding code.</span></span>

![Illustration montrant une image superposée par trois ellipses : une opaque, une légèrement transparente, une très transparente](images/compqualellipse.png)

 

 



