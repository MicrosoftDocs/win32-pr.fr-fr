---
description: Pour dessiner des lignes avec Windows GDI+, vous devez créer un objet Graphics et un objet Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Stylos, lignes et rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972851"
---
# <a name="pens-lines-and-rectangles"></a><span data-ttu-id="c13c0-103">Stylos, lignes et rectangles</span><span class="sxs-lookup"><span data-stu-id="c13c0-103">Pens, Lines, and Rectangles</span></span>

<span data-ttu-id="c13c0-104">Pour dessiner des lignes avec Windows GDI+, vous devez créer un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="c13c0-104">To draw lines with Windows GDI+ you need to create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="c13c0-105">L’objet **Graphics** fournit les méthodes qui effectuent le dessin, et l’objet **Pen** stocke les attributs de la ligne, tels que la couleur, la largeur et le style.</span><span class="sxs-lookup"><span data-stu-id="c13c0-105">The **Graphics** object provides the methods that actually do the drawing, and the **Pen** object stores attributes of the line, such as color, width, and style.</span></span> <span data-ttu-id="c13c0-106">Pour dessiner une ligne, il suffit d’appeler la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) de l’objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c13c0-106">Drawing a line is simply a matter of calling the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object.</span></span> <span data-ttu-id="c13c0-107">L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawLine.</span><span class="sxs-lookup"><span data-stu-id="c13c0-107">The address of the **Pen** object is passed as one of the arguments to the DrawLine method.</span></span> <span data-ttu-id="c13c0-108">L’exemple suivant dessine une ligne à partir du point (4, 2) jusqu’au point (12, 6).</span><span class="sxs-lookup"><span data-stu-id="c13c0-108">The following example draws a line from the point (4, 2) to the point (12, 6).</span></span>


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



<span data-ttu-id="c13c0-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) est une méthode surchargée de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . il existe donc plusieurs façons de le fournir avec des arguments.</span><span class="sxs-lookup"><span data-stu-id="c13c0-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="c13c0-110">Par exemple, vous pouvez construire deux objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) et passer des références aux objets **point** en tant qu’arguments à la méthode DrawLine.</span><span class="sxs-lookup"><span data-stu-id="c13c0-110">For example, you can construct two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects and pass references to the **Point** objects as arguments to the DrawLine method.</span></span>


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



<span data-ttu-id="c13c0-111">Vous pouvez spécifier certains attributs lorsque vous construisez un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="c13c0-111">You can specify certain attributes when you construct a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="c13c0-112">Par exemple, un constructeur de [stylet](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) vous permet de spécifier la couleur et la largeur.</span><span class="sxs-lookup"><span data-stu-id="c13c0-112">For example, one [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) constructor allows you to specify color and width.</span></span> <span data-ttu-id="c13c0-113">L’exemple suivant dessine une ligne bleue de largeur 2 comprise entre (0,0) et (60, 30).</span><span class="sxs-lookup"><span data-stu-id="c13c0-113">The following example draws a blue line of width 2 from (0, 0) to (60, 30).</span></span>


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



<span data-ttu-id="c13c0-114">L’objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) possède également des attributs, tels que le style Dash, que vous pouvez utiliser pour spécifier les fonctionnalités de la ligne.</span><span class="sxs-lookup"><span data-stu-id="c13c0-114">The [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object also has attributes, such as dash style, that you can use to specify features of the line.</span></span> <span data-ttu-id="c13c0-115">Par exemple, l’exemple suivant dessine une ligne en pointillés de (100, 50) à (300, 80).</span><span class="sxs-lookup"><span data-stu-id="c13c0-115">For example, the following example draws a dashed line from (100, 50) to (300, 80).</span></span>


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



<span data-ttu-id="c13c0-116">Vous pouvez utiliser différentes méthodes de l’objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) pour définir de nombreux autres attributs de la ligne.</span><span class="sxs-lookup"><span data-stu-id="c13c0-116">You can use various methods of the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to set many more attributes of the line.</span></span> <span data-ttu-id="c13c0-117">Les méthodes [**Pen :: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) et [**Pen :: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) spécifient l’apparence des extrémités de la ligne ; les extrémités peuvent être de forme plate, carrée, arrondie, triangulaire ou personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c13c0-117">The [**Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) and [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) methods specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="c13c0-118">La méthode [**Pen :: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) vous permet de spécifier si les lignes connectées sont mitres (jointes avec des angles aigus), biseautées, arrondies ou découpées.</span><span class="sxs-lookup"><span data-stu-id="c13c0-118">The [**Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="c13c0-119">L’illustration suivante montre des lignes avec différents styles d’extrémité et de jointure.</span><span class="sxs-lookup"><span data-stu-id="c13c0-119">The following illustration shows lines with various cap and join styles.</span></span>

![illustration de deux lignes montrant des extrémités arrondies et circulaires, des angles arrondis et mitres, et deux styles de flèche](images/aboutgdip02-art04.png)

<span data-ttu-id="c13c0-121">Le dessin de rectangles avec GDI+ est semblable au dessin de lignes.</span><span class="sxs-lookup"><span data-stu-id="c13c0-121">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="c13c0-122">Pour dessiner un rectangle, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="c13c0-122">To draw a rectangle, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="c13c0-123">L’objet **Graphics** fournit une méthode [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) , et l’objet **Pen** stocke des attributs, tels que la largeur et la couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="c13c0-123">The **Graphics** object provides a [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores attributes, such as line width and color.</span></span> <span data-ttu-id="c13c0-124">L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="c13c0-124">The address of the **Pen** object is passed as one of the arguments to the DrawRectangle method.</span></span> <span data-ttu-id="c13c0-125">L’exemple suivant dessine un rectangle avec son angle supérieur gauche à (100, 50), une largeur de 80 et une hauteur de 40.</span><span class="sxs-lookup"><span data-stu-id="c13c0-125">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40.</span></span>


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



<span data-ttu-id="c13c0-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) étant une méthode surchargée de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , il existe plusieurs façons de la fournir avec des arguments.</span><span class="sxs-lookup"><span data-stu-id="c13c0-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="c13c0-127">Par exemple, vous pouvez construire un objet [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) et passer une référence à l’objet **Rect** en tant qu’argument à la méthode DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="c13c0-127">For example, you can construct a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawRectangle method.</span></span>


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



<span data-ttu-id="c13c0-128">Un objet [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) possède des méthodes pour manipuler et collecter des informations sur le rectangle.</span><span class="sxs-lookup"><span data-stu-id="c13c0-128">A [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object has methods for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="c13c0-129">Par exemple, les méthodes d' [augmentation](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) et de [décalage](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) modifient la taille et la position du rectangle.</span><span class="sxs-lookup"><span data-stu-id="c13c0-129">For example, the [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) and [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) methods change the size and position of the rectangle.</span></span> <span data-ttu-id="c13c0-130">La méthode [**Rect :: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) vous indique si le rectangle croise un autre rectangle donné, et la méthode [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) vous indique si un point donné se trouve à l’intérieur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="c13c0-130">The [**Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) method tells you whether the rectangle intersects another given rectangle, and the [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) method tells you whether a given point is inside the rectangle.</span></span>

 

 
