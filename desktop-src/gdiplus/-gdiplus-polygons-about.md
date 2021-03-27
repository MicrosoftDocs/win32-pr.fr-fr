---
description: Un polygone est une figure fermée avec au moins trois côtés droits.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Polygones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751317"
---
# <a name="polygons"></a><span data-ttu-id="02c0e-103">Polygones</span><span class="sxs-lookup"><span data-stu-id="02c0e-103">Polygons</span></span>

<span data-ttu-id="02c0e-104">Un polygone est une figure fermée avec au moins trois côtés droits.</span><span class="sxs-lookup"><span data-stu-id="02c0e-104">A polygon is a closed figure with three or more straight sides.</span></span> <span data-ttu-id="02c0e-105">Par exemple, un triangle est un polygone avec trois côtés, un rectangle est un polygone avec quatre côtés et un pentagone est un polygone avec cinq côtés.</span><span class="sxs-lookup"><span data-stu-id="02c0e-105">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="02c0e-106">L’illustration suivante montre plusieurs polygones.</span><span class="sxs-lookup"><span data-stu-id="02c0e-106">The following illustration shows several polygons.</span></span>

![Illustration montrant cinq polygones de différentes formes, tailles et couleurs](images/aboutgdip02-art07.png)

<span data-ttu-id="02c0e-108">Pour dessiner un polygone, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et d’un tableau d’objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (ou [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).</span><span class="sxs-lookup"><span data-stu-id="02c0e-108">To draw a polygon, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span> <span data-ttu-id="02c0e-109">L’objet **Graphics** fournit la méthode [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="02c0e-109">The **Graphics** object provides the [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="02c0e-110">L’objet **Pen** stocke les attributs du polygone, tels que la largeur et la couleur de ligne, et le tableau d’objets **point** stocke les points à connecter par des lignes droites.</span><span class="sxs-lookup"><span data-stu-id="02c0e-110">The **Pen** object stores attributes of the polygon, such as line width and color, and the array of **Point** objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="02c0e-111">Les adresses de l’objet **Pen** et le tableau d’objets **point** sont passés comme arguments à la méthode DrawPolygon.</span><span class="sxs-lookup"><span data-stu-id="02c0e-111">The addresses of the **Pen** object and the array of **Point** objects are passed as arguments to the DrawPolygon method.</span></span> <span data-ttu-id="02c0e-112">L’exemple suivant dessine un polygone à trois côtés.</span><span class="sxs-lookup"><span data-stu-id="02c0e-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="02c0e-113">Notez qu’il n’y a que trois points dans **myPointArray**: (0, 0), (50, 30) et (30, 60).</span><span class="sxs-lookup"><span data-stu-id="02c0e-113">Note that there are only three points in **myPointArray**: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="02c0e-114">La méthode DrawPolygon ferme automatiquement le polygone en dessinant une ligne de (30, 60) au point de départ (0,0);</span><span class="sxs-lookup"><span data-stu-id="02c0e-114">The DrawPolygon method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0);</span></span>


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



<span data-ttu-id="02c0e-115">L’illustration suivante montre le polygone.</span><span class="sxs-lookup"><span data-stu-id="02c0e-115">The following illustration shows the polygon.</span></span>

![Illustration montrant un triangle par rapport aux axes de coordonnées](images/aboutgdip02-art08.png)

 

 



