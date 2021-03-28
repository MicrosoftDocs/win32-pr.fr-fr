---
description: Le découpage implique la restriction du dessin à une certaine région. L’illustration suivante montre la chaîne &\# 0034 ; Bonjour&\# 0034 ; ajusté à une région en forme de cœur.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Découpage (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034363"
---
# <a name="clipping-gdi"></a><span data-ttu-id="da4c9-104">Découpage (GDI+)</span><span class="sxs-lookup"><span data-stu-id="da4c9-104">Clipping (GDI+)</span></span>

<span data-ttu-id="da4c9-105">Le découpage implique la restriction du dessin à une certaine région.</span><span class="sxs-lookup"><span data-stu-id="da4c9-105">Clipping involves restricting drawing to a certain region.</span></span> <span data-ttu-id="da4c9-106">L’illustration suivante montre la chaîne « Hello » découpée en une région en forme de cœur.</span><span class="sxs-lookup"><span data-stu-id="da4c9-106">The following illustration shows the string "Hello" clipped to a heart-shaped region.</span></span>

![Illustration montrant des parties de la chaîne « Hello » dans un cœur rouge](images/aboutgdip02-art30.png)

<span data-ttu-id="da4c9-108">Les régions peuvent être construites à partir de chemins d’accès, et les chemins d’accès peuvent contenir des contours de chaînes, ce qui vous permet d’utiliser du texte avec contour pour le découpage.</span><span class="sxs-lookup"><span data-stu-id="da4c9-108">Regions can be constructed from paths, and paths can contain the outlines of strings, so you can use outlined text for clipping.</span></span> <span data-ttu-id="da4c9-109">L’illustration suivante montre un ensemble de points de suspension concentriques tronqués à l’intérieur d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="da4c9-109">The following illustration shows a set of concentric ellipses clipped to the interior of a string of text.</span></span>

![Illustration montrant la chaîne « Hello » remplie par un modèle de cercles concentriques](images/aboutgdip02-art31.png)

<span data-ttu-id="da4c9-111">Pour dessiner avec un découpage, créez un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , appelez sa méthode [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) , puis appelez les méthodes de dessin de ce même objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="da4c9-111">To draw with clipping, create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, call its [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method, and then call the drawing methods of that same **Graphics** object.</span></span> <span data-ttu-id="da4c9-112">L’exemple suivant dessine une ligne découpée dans une zone rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="da4c9-112">The following example draws a line that is clipped to a rectangular region.</span></span>


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



<span data-ttu-id="da4c9-113">L’illustration suivante montre la zone rectangulaire avec la ligne découpée.</span><span class="sxs-lookup"><span data-stu-id="da4c9-113">The following illustration shows the rectangular region along with the clipped line.</span></span>

![Illustration montrant un rectangle avec une ligne diagonale de haut en bas](images/aboutgdip02-art31a.png)

 

 



