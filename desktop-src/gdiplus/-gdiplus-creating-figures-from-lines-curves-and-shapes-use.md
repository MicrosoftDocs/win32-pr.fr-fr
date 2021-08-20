---
description: Pour créer un chemin d’accès, construisez un objet GraphicsPath, puis appelez des méthodes, telles que AddLine et AddCurve, pour ajouter des primitives au chemin d’accès.
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: Création de figures à partir de lignes, de courbes et de formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2c0d2914eb1edb740d7a9bca6a8b521aed6a0443b6dcd1ee92c68326f748af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067606"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a>Création de figures à partir de lignes, de courbes et de formes

Pour créer un chemin d’accès, construisez un objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) , puis appelez des méthodes, telles que [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) et [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), pour ajouter des primitives au chemin d’accès.

L’exemple suivant crée un tracé qui a un seul arc. L’ARC a un angle de balayage de-180 degrés, qui est dans le sens inverse des aiguilles d’une passe dans le système de coordonnées par défaut.


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



L’exemple suivant crée un tracé qui a deux figures. La première figure est un arc suivi d’une ligne. La deuxième figure est une ligne suivie d’une courbe, suivie d’une ligne. La première figure est laissée ouverte et la deuxième figure est fermée.


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



Outre l’ajout de lignes et de courbes aux tracés, vous pouvez ajouter des formes fermées : des rectangles, des ellipses, des secteurs et des polygones. L’exemple suivant crée un tracé qui comporte deux lignes, un rectangle et une ellipse. Le code utilise un stylet pour dessiner le tracé et un pinceau pour remplir le tracé.


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



Le chemin d’accès dans l’exemple précédent a trois figures. La première figure comprend les deux lignes, la deuxième figure le rectangle et la troisième figure l’ellipse. Même s’il n’y a aucun appel à [**GraphicsPath :: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) ou [**GraphicsPath :: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), les formes fermées intrinsèquement, telles que les rectangles et les ellipses, sont considérées comme des figures distinctes.

 

 



