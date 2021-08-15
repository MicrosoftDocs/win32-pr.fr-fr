---
description: 'Lorsque vous créez un objet Pen, vous pouvez indiquer la largeur du stylet comme l’un des arguments du constructeur. Vous pouvez également modifier la largeur du stylet à l’aide de la méthode Pen :: SetWidth.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Définition de la largeur et de l’alignement du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2a6bd5be00fde0f27657cef558365d857775a5b55f9f108074884906916b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885012"
---
# <a name="setting-pen-width-and-alignment"></a>Définition de la largeur et de l’alignement du stylet

Lorsque vous créez un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) , vous pouvez indiquer la largeur du stylet comme l’un des arguments du constructeur. Vous pouvez également modifier la largeur du stylet à l’aide de la méthode [**Pen :: SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .

Une ligne théorique a une largeur de zéro. Quand vous dessinez une ligne, les pixels sont centrés sur la ligne théorique. L’exemple suivant dessine une ligne spécifiée deux fois : une fois avec un stylet noir de largeur 1 et une fois avec un stylet vert de la largeur 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



L’illustration suivante montre la sortie du code précédent. Les pixels verts et les pixels noirs sont centrés sur la ligne théorique.

![Illustration montrant une ligne noire fine, en diagonale, entourée d’un trait vert épais ](images/pens1a.png)

L’exemple suivant dessine un rectangle spécifié deux fois : une fois avec un stylet noir de largeur 1 et une fois avec un stylet vert de la largeur 10. Le code passe la valeur **PenAlignmentCenter** (un élément de l’énumération [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) à la méthode [**Pen :: SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) pour spécifier que les pixels dessinés avec le stylet vert sont centrés sur la limite du rectangle.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



L’illustration suivante montre la sortie du code précédent. Les pixels verts sont centrés sur le rectangle théorique, représenté par les pixels noirs.

![Illustration montrant une fine ligne noire dans la forme d’un rectangle, entourée d’une ligne verte plus grande](images/pens2.png)

Vous pouvez modifier l’alignement du stylet vert en modifiant la troisième instruction de l’exemple précédent comme suit :


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



À présent, les pixels de la ligne verte de l’épaisseur apparaissent à l’intérieur du rectangle, comme indiqué dans l’illustration suivante.

![Illustration montrant une fine ligne noire dans la forme d’un rectange, englobant une ligne verte de la même forme](images/pens3.png)

 

 



