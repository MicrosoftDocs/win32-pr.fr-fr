---
description: pour dessiner des lignes avec Windows GDI+ vous devez créer un objet graphics et un objet Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Stylos, lignes et rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ac54d1e98a617492aa6f5f1194767fc56a34ffcaaee71ba71753dda08f8bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359589"
---
# <a name="pens-lines-and-rectangles"></a>Stylos, lignes et rectangles

pour dessiner des lignes avec Windows GDI+ vous devez créer un objet [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L’objet **Graphics** fournit les méthodes qui effectuent le dessin, et l’objet **Pen** stocke les attributs de la ligne, tels que la couleur, la largeur et le style. Pour dessiner une ligne, il suffit d’appeler la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) de l’objet **Graphics** . L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawLine. L’exemple suivant dessine une ligne à partir du point (4, 2) jusqu’au point (12, 6).


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) est une méthode surchargée de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . il existe donc plusieurs façons de le fournir avec des arguments. Par exemple, vous pouvez construire deux objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) et passer des références aux objets **point** en tant qu’arguments à la méthode DrawLine.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



Vous pouvez spécifier certains attributs lorsque vous construisez un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Par exemple, un constructeur de [stylet](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) vous permet de spécifier la couleur et la largeur. L’exemple suivant dessine une ligne bleue de largeur 2 comprise entre (0,0) et (60, 30).


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



L’objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) possède également des attributs, tels que le style Dash, que vous pouvez utiliser pour spécifier les fonctionnalités de la ligne. Par exemple, l’exemple suivant dessine une ligne en pointillés de (100, 50) à (300, 80).


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



Vous pouvez utiliser différentes méthodes de l’objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) pour définir de nombreux autres attributs de la ligne. Les méthodes [**Pen :: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) et [**Pen :: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) spécifient l’apparence des extrémités de la ligne ; les extrémités peuvent être de forme plate, carrée, arrondie, triangulaire ou personnalisée. La méthode [**Pen :: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) vous permet de spécifier si les lignes connectées sont mitres (jointes avec des angles aigus), biseautées, arrondies ou découpées. L’illustration suivante montre des lignes avec différents styles d’extrémité et de jointure.

![illustration de deux lignes montrant des extrémités arrondies et circulaires, des angles arrondis et mitres, et deux styles de flèche](images/aboutgdip02-art04.png)

le dessin de rectangles avec GDI+ est semblable au dessin de lignes. Pour dessiner un rectangle, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L’objet **Graphics** fournit une méthode [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) , et l’objet **Pen** stocke des attributs, tels que la largeur et la couleur de ligne. L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawRectangle. L’exemple suivant dessine un rectangle avec son angle supérieur gauche à (100, 50), une largeur de 80 et une hauteur de 40.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) étant une méthode surchargée de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , il existe plusieurs façons de la fournir avec des arguments. Par exemple, vous pouvez construire un objet [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) et passer une référence à l’objet **Rect** en tant qu’argument à la méthode DrawRectangle.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Un objet [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) possède des méthodes pour manipuler et collecter des informations sur le rectangle. Par exemple, les méthodes d' [augmentation](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) et de [décalage](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) modifient la taille et la position du rectangle. La méthode [**Rect :: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) vous indique si le rectangle croise un autre rectangle donné, et la méthode [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) vous indique si un point donné se trouve à l’intérieur du rectangle.

 

 
