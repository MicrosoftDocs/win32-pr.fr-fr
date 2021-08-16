---
description: Les tracés sont formés en combinant des lignes, des rectangles et des courbes simples. Rappelez-vous à partir de la vue d’ensemble des graphiques vectoriels que les blocs de construction de base suivants se sont avérés les plus utiles pour dessiner des images.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Chemins (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54dae290138314cac3dae8d259591939490764d371e9a2caf9423801e985ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695475"
---
# <a name="paths-gdi"></a>Chemins (GDI+)

Les tracés sont formés en combinant des lignes, des rectangles et des courbes simples. Rappelez-vous à partir de la [vue d’ensemble des graphiques vectoriels](-gdiplus-overview-of-vector-graphics-about.md) que les blocs de construction de base suivants se sont avérés les plus utiles pour dessiner des images.

-   Lignes
-   Rectangles
-   Suspension
-   Arcs
-   Polygones
-   Splines cardinales
-   Splines de Bézier

dans Windows GDI+, l’objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) vous permet de collecter une séquence de ces blocs de construction en une seule unité. L’intégralité de la séquence de lignes, de rectangles, de polygones et de courbes peut ensuite être dessinée à l’aide d’un appel à la méthode [**Graphics ::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L’illustration suivante montre un tracé créé en combinant une ligne, un arc, une spline de Bézier et une spline cardinale.

![illustration d’un tracé qui combine une ligne, un arc, une spline de Bézier et une spline cardinale](images/aboutgdip02-art14.png)

La classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) fournit les méthodes suivantes pour créer une séquence d’éléments à dessiner : [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (pour les splines cardinales) et [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Chacune de ces méthodes est surchargée ; autrement dit, chaque méthode est proposée en plusieurs variations avec différentes listes de paramètres. Par exemple, une variante de la méthode AddLine reçoit quatre entiers et une autre variante de la méthode AddLine reçoit deux objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

Les méthodes permettant d’ajouter des lignes, des rectangles et des splines de Bézier à un chemin d’accès ont des méthodes auxiliaires qui ajoutent plusieurs éléments au chemin d’accès en un seul appel : [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))et [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)). En outre, la méthode [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) a une méthode auxiliaire, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), qui ajoute une courbe fermée au tracé.

Pour dessiner un tracé, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et d’un objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . L’objet **Graphics** fournit la méthode [**graphics ::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) , et l’objet **Pen** stocke les attributs du chemin d’accès, tels que la largeur et la couleur de ligne. L’objet **GraphicsPath** stocke la séquence de lignes, de rectangles et de courbes qui composent le chemin d’accès. Les adresses de l’objet **Pen** et de l’objet **GraphicsPath** sont passées comme arguments à la méthode **Graphics ::D rawpath** . L’exemple suivant dessine un tracé qui se compose d’une ligne, d’une ellipse et d’une spline de Bézier.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



L’illustration suivante montre le chemin d’accès.

![illustration d’un tracé composé d’une ligne, d’une ellipse et d’une spline de Bézier](images/aboutgdip02-art15.png)

En plus d’ajouter des lignes, des rectangles et des courbes à un tracé, vous pouvez ajouter des tracés à un chemin d’accès. Cela vous permet de combiner des chemins existants pour former des chemins d’accès volumineux et complexes. Le code suivant ajoute **graphicsPath1** et **graphicsPath2** à **myGraphicsPath**. Le deuxième paramètre de la méthode [**GraphicsPath :: AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) spécifie si le chemin d’accès ajouté est connecté au chemin d’accès existant.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



Il existe deux autres éléments que vous pouvez ajouter à un chemin d’accès : des chaînes et des secteurs. Un secteur est une partie de l’intérieur d’une ellipse. L’exemple suivant crée un tracé à partir d’un arc, d’une spline cardinale, d’une chaîne et d’un graphique à secteurs.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



L’illustration suivante montre le chemin d’accès. Notez qu’il n’est pas nécessaire de connecter un chemin d’accès ; l’arc, la spline cardinale, la chaîne et le secteur sont séparés.

![illustration d’un tracé constitué de lignes déconnectées : un arc, une spline cardinale, une chaîne et un graphique à secteurs](images/aboutgdip02-art16.png)

 

 



