---
description: L’objectif du test d’atteinte est de déterminer si le curseur se trouve sur un objet donné, tel qu’une icône ou un bouton.
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: Test de positionnement avec une région
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0673466bc368c9288765b1c7e6f460716d8d40674802a0977690a7ef79b58b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885397"
---
# <a name="hit-testing-with-a-region"></a>Test de positionnement avec une région

L’objectif du test d’atteinte est de déterminer si le curseur se trouve sur un objet donné, tel qu’une icône ou un bouton. L’exemple suivant crée une région en forme de plus en formant l’Union de deux régions rectangulaires. Supposons que le **point** variable conserve l’emplacement du clic le plus récent. Le code vérifie si le **point** se trouve dans la zone en forme de plus. Si le **point** se trouve dans la région (un accès), la zone est remplie avec un pinceau rouge opaque. Dans le cas contraire, la zone est remplie avec un pinceau rouge semi-transparent.


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



 

 



