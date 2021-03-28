---
description: Une ellipse est spécifiée par son rectangle englobant. L’illustration suivante montre une ellipse avec son rectangle englobant.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Ellipses et arcs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115230"
---
# <a name="ellipses-and-arcs"></a><span data-ttu-id="9a33a-104">Ellipses et arcs</span><span class="sxs-lookup"><span data-stu-id="9a33a-104">Ellipses and Arcs</span></span>

<span data-ttu-id="9a33a-105">Une ellipse est spécifiée par son rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="9a33a-105">An ellipse is specified by its bounding rectangle.</span></span> <span data-ttu-id="9a33a-106">L’illustration suivante montre une ellipse avec son rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="9a33a-106">The following illustration shows an ellipse along with its bounding rectangle.</span></span>

![illustration d’une ellipse placée dans un rectangle englobant](images/aboutgdip02-art05.png)

<span data-ttu-id="9a33a-108">Pour dessiner une ellipse, vous avez besoin d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="9a33a-108">To draw an ellipse, you need a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="9a33a-109">L’objet **Graphics** fournit la méthode [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , et l’objet **Pen** stocke les attributs de l’ellipse, tels que la largeur et la couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="9a33a-109">The **Graphics** object provides the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, and the **Pen** object stores attributes of the ellipse, such as line width and color.</span></span> <span data-ttu-id="9a33a-110">L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="9a33a-110">The address of the **Pen** object is passed as one of the arguments to the DrawEllipse method.</span></span> <span data-ttu-id="9a33a-111">Les arguments restants passés à la méthode DrawEllipse spécifient le rectangle englobant pour l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="9a33a-111">The remaining arguments passed to the DrawEllipse method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="9a33a-112">L’exemple suivant dessine une ellipse. le rectangle englobant a une largeur de 160, une hauteur de 80 et un angle supérieur gauche de (100, 50).</span><span class="sxs-lookup"><span data-stu-id="9a33a-112">The following example draws an ellipse; the bounding rectangle has a width of 160, a height of 80, and an upper-left corner of (100, 50).</span></span>


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



<span data-ttu-id="9a33a-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) étant une méthode surchargée de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , il existe plusieurs façons de la fournir avec des arguments.</span><span class="sxs-lookup"><span data-stu-id="9a33a-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) is an overloaded method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="9a33a-114">Par exemple, vous pouvez construire un objet [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) et passer une référence à l’objet **Rect** en tant qu’argument à la méthode DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="9a33a-114">For example, you can construct a [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawEllipse method.</span></span>


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



<span data-ttu-id="9a33a-115">Un arc est une partie d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="9a33a-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="9a33a-116">Pour dessiner un arc, vous appelez la méthode [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="9a33a-116">To draw an arc, you call the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="9a33a-117">Les paramètres de la méthode DrawArc sont les mêmes que les paramètres de la méthode [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , sauf que DrawArc requiert un angle de départ et un angle de balayage.</span><span class="sxs-lookup"><span data-stu-id="9a33a-117">The parameters of the DrawArc method are the same as the parameters of the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, except that DrawArc requires a starting angle and sweep angle.</span></span> <span data-ttu-id="9a33a-118">L’exemple suivant dessine un arc avec un angle de départ de 30 degrés et un angle de balayage de 180 degrés.</span><span class="sxs-lookup"><span data-stu-id="9a33a-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees.</span></span>


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



<span data-ttu-id="9a33a-119">L’illustration suivante montre l’arc, l’ellipse et le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="9a33a-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>

![illustration d’une ellipse dans un rectangle englobant ; la moitié inférieure gauche de l’ellipse est dessinée en rouge](images/aboutgdip02-art06.png)

 

 



