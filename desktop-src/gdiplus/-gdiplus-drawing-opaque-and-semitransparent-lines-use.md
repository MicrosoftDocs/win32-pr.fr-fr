---
description: Quand vous dessinez une ligne, vous devez passer l’adresse d’un objet Pen à la méthode DrawLine de la classe Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Dessin de lignes opaques et semi-transparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556407"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a><span data-ttu-id="ed7ee-103">Dessin de lignes opaques et semi-transparentes</span><span class="sxs-lookup"><span data-stu-id="ed7ee-103">Drawing Opaque and Semitransparent Lines</span></span>

<span data-ttu-id="ed7ee-104">Quand vous dessinez une ligne, vous devez passer l’adresse d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) à la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ed7ee-104">When you draw a line, you must pass the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="ed7ee-105">L’un des paramètres du constructeur **Pen** est un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="ed7ee-105">One of the parameters of the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="ed7ee-106">Pour dessiner une ligne opaque, affectez au composant alpha de la couleur la valeur 255.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-106">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="ed7ee-107">Pour dessiner une ligne translucide, affectez au composant alpha n'importe quelle valeur comprise entre 1 et 254.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-107">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="ed7ee-108">Quand vous dessinez une ligne translucide sur un arrière-plan, la couleur de la ligne est fusionnée avec les couleurs de l'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-108">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="ed7ee-109">Le composant alpha spécifie la manière dont les couleurs de ligne et d’arrière-plan sont mélangées ; les valeurs alpha proches de 0 placent plus de poids sur les couleurs d’arrière-plan, tandis que les valeurs alpha proches de 255 placent plus peser sur la couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-109">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the line color.</span></span>

<span data-ttu-id="ed7ee-110">L’exemple suivant dessine une image, puis dessine trois lignes qui utilisent l’image comme arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-110">The following example draws an image and then draws three lines that use the image as a background.</span></span> <span data-ttu-id="ed7ee-111">La première ligne utilise un composant alpha de 255. Elle est donc opaque.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="ed7ee-112">Les deuxième et troisième lignes utilisent un composant alpha de 128 et sont donc translucides. Vous pouvez voir l'image d'arrière-plan sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="ed7ee-113">L’appel à [**Graphics :: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) fait en sorte que la fusion pour la troisième ligne soit effectuée conjointement avec la correction gamma.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-113">The call to [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third line to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



<span data-ttu-id="ed7ee-114">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="ed7ee-114">The following illustration shows the output of the preceding code.</span></span>

![Illustration montrant une image superposée par trois traits larges : un opaque, un léger et un peu transparent](images/compqualline.png)

 

 



