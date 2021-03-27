---
description: Pour dessiner des lignes et des rectangles, vous avez besoin d’un objet Graphics et d’un objet Pen. L’objet Graphics fournit la méthode DrawLine, et l’objet Pen stocke les fonctionnalités de la ligne, telles que la couleur et la largeur.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Utilisation d’un stylo pour tracer des lignes et des rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951692"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a><span data-ttu-id="1179b-104">Utilisation d’un stylo pour tracer des lignes et des rectangles</span><span class="sxs-lookup"><span data-stu-id="1179b-104">Using a Pen to Draw Lines and Rectangles</span></span>

<span data-ttu-id="1179b-105">Pour dessiner des lignes et des rectangles, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="1179b-105">To draw lines and rectangles, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="1179b-106">L’objet **Graphics** fournit la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , et l’objet **Pen** stocke les fonctionnalités de la ligne, telles que la couleur et la largeur.</span><span class="sxs-lookup"><span data-stu-id="1179b-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores features of the line, such as color and width.</span></span>

<span data-ttu-id="1179b-107">L’exemple suivant dessine une ligne de (20, 10) à (300, 100).</span><span class="sxs-lookup"><span data-stu-id="1179b-107">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="1179b-108">Supposons que **Graphics** est un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existant.</span><span class="sxs-lookup"><span data-stu-id="1179b-108">Assume **graphics** is an existing [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



<span data-ttu-id="1179b-109">La première instruction du code utilise le constructeur de classe [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) pour créer un stylet noir.</span><span class="sxs-lookup"><span data-stu-id="1179b-109">The first statement of code uses the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) class constructor to create a black pen.</span></span> <span data-ttu-id="1179b-110">L’argument passé au constructeur **Pen** est un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="1179b-110">The one argument passed to the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="1179b-111">Les valeurs utilisées pour construire l’objet **Color** ((255, 0, 0,0)) correspondent aux composants alpha, rouge, vert et bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="1179b-111">The values used to construct the **Color** object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="1179b-112">Ces valeurs définissent un stylet noir opaque.</span><span class="sxs-lookup"><span data-stu-id="1179b-112">These values define an opaque black pen.</span></span>

<span data-ttu-id="1179b-113">L’exemple suivant dessine un rectangle avec son angle supérieur gauche à (10, 10).</span><span class="sxs-lookup"><span data-stu-id="1179b-113">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="1179b-114">Le rectangle a une largeur de 100 et une hauteur de 50.</span><span class="sxs-lookup"><span data-stu-id="1179b-114">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="1179b-115">Le deuxième argument passé au constructeur [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indique que la largeur du stylet est de 5 pixels.</span><span class="sxs-lookup"><span data-stu-id="1179b-115">The second argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor indicates that the pen width is 5 pixels.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



<span data-ttu-id="1179b-116">Lorsque le rectangle est dessiné, le stylet est centré sur la limite du rectangle.</span><span class="sxs-lookup"><span data-stu-id="1179b-116">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="1179b-117">Étant donné que la largeur du stylet est de 5, les côtés du rectangle sont dessinés à 5 pixels de large, ce qui fait que 1 pixel est dessiné sur la limite elle-même, 2 pixels sont dessinés à l’intérieur et 2 pixels à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="1179b-117">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="1179b-118">Pour plus d’informations sur l’alignement du stylet, consultez Définition de la [largeur et de l’alignement du stylet](-gdiplus-setting-pen-width-and-alignment-use.md).</span><span class="sxs-lookup"><span data-stu-id="1179b-118">For more details on pen alignment, see [Setting Pen Width and Alignment](-gdiplus-setting-pen-width-and-alignment-use.md).</span></span>

<span data-ttu-id="1179b-119">L’illustration suivante montre le rectangle résultant.</span><span class="sxs-lookup"><span data-stu-id="1179b-119">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="1179b-120">Les lignes en pointillés indiquent où le rectangle aurait été dessiné si la largeur du stylet avait été d’un pixel.</span><span class="sxs-lookup"><span data-stu-id="1179b-120">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="1179b-121">La vue agrandie de l’angle supérieur gauche du rectangle montre que les lignes noires épaisses sont centrées sur ces lignes en pointillés.</span><span class="sxs-lookup"><span data-stu-id="1179b-121">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>

![illustration d’un Rectangle dessiné avec une ligne noire épaisse qui entoure une ligne fine, grise, en pointillés](images/pens1.png)

 

 



