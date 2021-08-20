---
description: Une ellipse est spécifiée par son rectangle englobant. L’illustration suivante montre une ellipse avec son rectangle englobant.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Ellipses et arcs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadd0a34107681d2d155ead5d4f80b7208b8926603f21fa4541d502886edaf73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036747"
---
# <a name="ellipses-and-arcs"></a>Ellipses et arcs

Une ellipse est spécifiée par son rectangle englobant. L’illustration suivante montre une ellipse avec son rectangle englobant.

![illustration d’une ellipse placée dans un rectangle englobant](images/aboutgdip02-art05.png)

Pour dessiner une ellipse, vous avez besoin d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . L’objet **Graphics** fournit la méthode [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , et l’objet **Pen** stocke les attributs de l’ellipse, tels que la largeur et la couleur de ligne. L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawEllipse. Les arguments restants passés à la méthode DrawEllipse spécifient le rectangle englobant pour l’ellipse. L’exemple suivant dessine une ellipse. le rectangle englobant a une largeur de 160, une hauteur de 80 et un angle supérieur gauche de (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) étant une méthode surchargée de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , il existe plusieurs façons de la fournir avec des arguments. Par exemple, vous pouvez construire un objet [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) et passer une référence à l’objet **Rect** en tant qu’argument à la méthode DrawEllipse.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Un arc est une partie d’une ellipse. Pour dessiner un arc, vous appelez la méthode [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Les paramètres de la méthode DrawArc sont les mêmes que les paramètres de la méthode [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , sauf que DrawArc requiert un angle de départ et un angle de balayage. L’exemple suivant dessine un arc avec un angle de départ de 30 degrés et un angle de balayage de 180 degrés.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



L’illustration suivante montre l’arc, l’ellipse et le rectangle englobant.

![illustration d’une ellipse dans un rectangle englobant ; la moitié inférieure gauche de l’ellipse est dessinée en rouge](images/aboutgdip02-art06.png)

 

 



