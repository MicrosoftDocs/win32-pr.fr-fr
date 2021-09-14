---
description: Pour dessiner des lignes et des rectangles, vous avez besoin d’un objet Graphics et d’un objet Pen. L’objet Graphics fournit la méthode DrawLine, et l’objet Pen stocke les fonctionnalités de la ligne, telles que la couleur et la largeur.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Utilisation d’un stylo pour tracer des lignes et des rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414297"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Utilisation d’un stylo pour tracer des lignes et des rectangles

Pour dessiner des lignes et des rectangles, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L’objet **Graphics** fournit la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , et l’objet **Pen** stocke les fonctionnalités de la ligne, telles que la couleur et la largeur.

L’exemple suivant dessine une ligne de (20, 10) à (300, 100). Supposons que **Graphics** est un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existant.


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



La première instruction du code utilise le constructeur de classe [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) pour créer un stylet noir. L’argument passé au constructeur **Pen** est un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Les valeurs utilisées pour construire l’objet **Color** ((255, 0, 0,0)) correspondent aux composants alpha, rouge, vert et bleu de la couleur. Ces valeurs définissent un stylet noir opaque.

L’exemple suivant dessine un rectangle avec son angle supérieur gauche à (10, 10). Le rectangle a une largeur de 100 et une hauteur de 50. Le deuxième argument passé au constructeur [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indique que la largeur du stylet est de 5 pixels.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Lorsque le rectangle est dessiné, le stylet est centré sur la limite du rectangle. Étant donné que la largeur du stylet est de 5, les côtés du rectangle sont dessinés à 5 pixels de large, ce qui fait que 1 pixel est dessiné sur la limite elle-même, 2 pixels sont dessinés à l’intérieur et 2 pixels à l’extérieur. Pour plus d’informations sur l’alignement du stylet, consultez Définition de la [largeur et de l’alignement du stylet](-gdiplus-setting-pen-width-and-alignment-use.md).

L’illustration suivante montre le rectangle résultant. Les lignes en pointillés indiquent où le rectangle aurait été dessiné si la largeur du stylet avait été d’un pixel. La vue agrandie de l’angle supérieur gauche du rectangle montre que les lignes noires épaisses sont centrées sur ces lignes en pointillés.

![illustration d’un Rectangle dessiné avec une ligne noire épaisse qui entoure une ligne fine, grise, en pointillés](images/pens1.png)

 

 



