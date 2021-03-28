---
description: L’objectif du test d’atteinte est de déterminer si le curseur se trouve sur un objet donné, tel qu’une icône ou un bouton.
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: Test de positionnement avec une région
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24913d8d890e3e1ded87eb48e2d52f1726663a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991332"
---
# <a name="hit-testing-with-a-region"></a><span data-ttu-id="ec045-103">Test de positionnement avec une région</span><span class="sxs-lookup"><span data-stu-id="ec045-103">Hit Testing with a Region</span></span>

<span data-ttu-id="ec045-104">L’objectif du test d’atteinte est de déterminer si le curseur se trouve sur un objet donné, tel qu’une icône ou un bouton.</span><span class="sxs-lookup"><span data-stu-id="ec045-104">The purpose of hit testing is to determine whether the cursor is over a given object, such as an icon or a button.</span></span> <span data-ttu-id="ec045-105">L’exemple suivant crée une région en forme de plus en formant l’Union de deux régions rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="ec045-105">The following example creates a plus-shaped region by forming the union of two rectangular regions.</span></span> <span data-ttu-id="ec045-106">Supposons que le **point** variable conserve l’emplacement du clic le plus récent.</span><span class="sxs-lookup"><span data-stu-id="ec045-106">Assume that the variable **point** holds the location of the most recent click.</span></span> <span data-ttu-id="ec045-107">Le code vérifie si le **point** se trouve dans la zone en forme de plus.</span><span class="sxs-lookup"><span data-stu-id="ec045-107">The code checks to see whether **point** is in the plus-shaped region.</span></span> <span data-ttu-id="ec045-108">Si le **point** se trouve dans la région (un accès), la zone est remplie avec un pinceau rouge opaque.</span><span class="sxs-lookup"><span data-stu-id="ec045-108">If **point** is in the region (a hit), the region is filled with an opaque red brush.</span></span> <span data-ttu-id="ec045-109">Dans le cas contraire, la zone est remplie avec un pinceau rouge semi-transparent.</span><span class="sxs-lookup"><span data-stu-id="ec045-109">Otherwise, the region is filled with a semitransparent red brush.</span></span>


```
Point point(60, 10);
// Assume that the variable "point" contains the location
// of the most recent click.
// To simulate a hit, assign (60, 10) to point.
// To simulate a miss, assign (0, 0) to point.
SolidBrush solidBrush(Color());
Region region1(Rect(50, 0, 50, 150));
Region region2(Rect(0, 50, 150, 50));
// Create a plus-shaped region by forming the union of region1 and region2.
// The union replaces region1.
region1.Union(&region2);
if(region1.IsVisible(point, &graphics))
{
   // The point is in the region. Use an opaque brush.
   solidBrush.SetColor(Color(255, 255, 0, 0));
}
else
{
   // The point is not in the region. Use a semitransparent brush.
   solidBrush.SetColor(Color(64, 255, 0, 0));
}
graphics.FillRegion(&solidBrush, &region1);
```



 

 



