---
description: Une spline cardinale est une courbe qui passe en douceur à un ensemble donné de points.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Dessiner des splines cardinales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c780cb4486f579acb57170a8eda4fd187a421ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549884"
---
# <a name="drawing-cardinal-splines"></a>Dessiner des splines cardinales

Une spline cardinale est une courbe qui passe en douceur à un ensemble donné de points. Pour dessiner une spline cardinale, créez un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et transmettez l’adresse d’un tableau de points à la méthode [**graphics ::D rawcurve**](/previous-versions//ms536070(v=vs.85)) . L’exemple suivant dessine une spline cardinale en forme de cloche qui passe par cinq points désignés :


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



L’illustration suivante montre la courbe et cinq points.

![illustration d’une spline cardinale qui passe par un ensemble de cinq points](images/cardinalspline1.png)

Vous pouvez utiliser la méthode [**Graphics ::D rawclosedcurve**](/previous-versions//ms536143(v=vs.85)) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour dessiner une spline cardinale fermée. Dans une spline cardinale fermée, la courbe continue jusqu’au dernier point du tableau et se connecte au premier point du tableau.

L’exemple suivant dessine une spline cardinale fermée qui passe par six points désignés.


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



L’illustration suivante montre la spline fermée avec les six points suivants :

![illustration d’une spline cardinale fermée qui passe par un ensemble de six points](images/cardinalspline1a.png)

Vous pouvez modifier le mode de courbure d’une spline cardinale en passant un argument de tension à la méthode [**Graphics ::D rawcurve**](/previous-versions//ms536070(v=vs.85)) . L’exemple suivant dessine trois splines cardinales qui passent par le même ensemble de points :


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



L’illustration suivante montre les trois splines, ainsi que leurs valeurs de tension. Notez que lorsque la tension est égale à 0, les points sont connectés par des lignes droites.

![illustration de trois splines cardinales passant par le même ensemble de points, mais à des tensions différentes](images/cardinalspline2.png)

 

 
