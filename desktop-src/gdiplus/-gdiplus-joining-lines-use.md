---
description: Une jointure de ligne est la zone commune qui est formée par deux lignes dont les extrémités se rencontrent ou se chevauchent.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Joindre des lignes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aa93eac405bd77f6d87b2a8b86edc8a4043a57de3e4c4d5f31fb45acecc955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066973"
---
# <a name="joining-lines"></a>Joindre des lignes

Une jointure de ligne est la zone commune qui est formée par deux lignes dont les extrémités se rencontrent ou se chevauchent. Windows GDI+ fournit quatre styles de jointure de ligne : mitre, biseau, arrondi et mitre. Le style de jonction de ligne est une propriété de la classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Lorsque vous spécifiez un style de jonction de ligne pour un stylet, puis utilisez ce stylet pour dessiner un tracé, le style de jointure spécifié est appliqué à toutes les lignes connectées dans le tracé.

Vous pouvez spécifier le style de jonction de ligne à l’aide de la méthode [**Pen :: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) de la classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . L’exemple suivant illustre une jointure de ligne biseautée entre une ligne horizontale et une ligne verticale :


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



L’illustration suivante montre la jointure de ligne biseautée résultante.

![Illustration montrant deux lignes réunis à un angle droit, avec une jointure biseautés](images/pens5.png)

Dans l’exemple précédent, la valeur (**LineJoinBevel**) transmise à la méthode [**Pen :: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) est un élément de l’énumération [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .

 

 



