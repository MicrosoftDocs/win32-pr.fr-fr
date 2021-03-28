---
description: La transformation universelle est une propriété de la classe Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilisation de la transformation universelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201404"
---
# <a name="using-the-world-transformation"></a>Utilisation de la transformation universelle

La transformation universelle est une propriété de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Les nombres qui spécifient la transformation universelle sont stockés dans un objet [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , qui représente une matrice 3 × 3. Les classes **Matrix** et **Graphics** disposent de plusieurs méthodes pour définir les nombres dans la matrice de transformation universelle. Les exemples de cette section manipulent des rectangles, car les rectangles sont faciles à dessiner et il est facile de voir les effets des transformations sur les rectangles.

Nous commençons par créer un rectangle de 50 par 50 et en le localisant à l’origine (0,0). L’origine se trouve dans le coin supérieur gauche de la zone cliente.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



Le code suivant applique une transformation de mise à l’échelle qui développe le rectangle d’un facteur de 1,75 dans la direction x et réduit le rectangle d’un facteur de 0,5 dans l’axe y :


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



Le résultat est un rectangle qui est plus long dans la direction x et plus petit dans le sens y que l’original.

Pour faire pivoter le rectangle au lieu de le mettre à l’échelle, utilisez le code suivant au lieu du code précédent :


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



Pour traduire le rectangle, utilisez le code suivant :


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



