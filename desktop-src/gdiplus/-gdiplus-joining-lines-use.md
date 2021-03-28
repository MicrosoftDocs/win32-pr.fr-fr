---
description: Une jointure de ligne est la zone commune qui est formée par deux lignes dont les extrémités se rencontrent ou se chevauchent.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Joindre des lignes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558819"
---
# <a name="joining-lines"></a><span data-ttu-id="b4145-103">Joindre des lignes</span><span class="sxs-lookup"><span data-stu-id="b4145-103">Joining Lines</span></span>

<span data-ttu-id="b4145-104">Une jointure de ligne est la zone commune qui est formée par deux lignes dont les extrémités se rencontrent ou se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="b4145-104">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="b4145-105">Windows GDI+ fournit quatre styles de jointure de ligne : Mitre, biseau, arrondi et mitre.</span><span class="sxs-lookup"><span data-stu-id="b4145-105">Windows GDI+ provides four line join styles: miter, bevel, round, and miter clipped.</span></span> <span data-ttu-id="b4145-106">Le style de jonction de ligne est une propriété de la classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="b4145-106">Line join style is a property of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="b4145-107">Lorsque vous spécifiez un style de jonction de ligne pour un stylet, puis utilisez ce stylet pour dessiner un tracé, le style de jointure spécifié est appliqué à toutes les lignes connectées dans le tracé.</span><span class="sxs-lookup"><span data-stu-id="b4145-107">When you specify a line join style for a pen and then use that pen to draw a path, the specified join style is applied to all the connected lines in the path.</span></span>

<span data-ttu-id="b4145-108">Vous pouvez spécifier le style de jonction de ligne à l’aide de la méthode [**Pen :: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) de la classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="b4145-108">You can specify the line join style by using the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="b4145-109">L’exemple suivant illustre une jointure de ligne biseautée entre une ligne horizontale et une ligne verticale :</span><span class="sxs-lookup"><span data-stu-id="b4145-109">The following example demonstrates a beveled line join between a horizontal line and a vertical line:</span></span>


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



<span data-ttu-id="b4145-110">L’illustration suivante montre la jointure de ligne biseautée résultante.</span><span class="sxs-lookup"><span data-stu-id="b4145-110">The following illustration shows the resulting beveled line join.</span></span>

![Illustration montrant deux lignes réunis à un angle droit, avec une jointure biseautés](images/pens5.png)

<span data-ttu-id="b4145-112">Dans l’exemple précédent, la valeur (**LineJoinBevel**) transmise à la méthode [**Pen :: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) est un élément de l’énumération [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .</span><span class="sxs-lookup"><span data-stu-id="b4145-112">In the preceding example, the value (**LineJoinBevel**) passed to the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method is an element of the [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) enumeration.</span></span>

 

 



