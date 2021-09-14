---
description: Windows GDI+ dessine des lignes, des rectangles et d’autres figures sur un système de coordonnées.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Vue d’ensemble du graphisme vectoriel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9bfe98585ef8e073cf1c563c237436b7c982bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012415"
---
# <a name="overview-of-vector-graphics"></a>Vue d’ensemble du graphisme vectoriel

Windows GDI+ dessine des lignes, des rectangles et d’autres figures sur un système de coordonnées. Vous pouvez choisir parmi un large éventail de systèmes de coordonnées, mais le système de coordonnées par défaut a l’origine dans le coin supérieur gauche avec l’axe des x pointant vers la droite et l’axe des y pointant vers le haut. L’unité de mesure dans le système de coordonnées par défaut est le pixel.

![illustration d’un système de coordonnées avec l’axe des x qui s’étend vers la droite et l’étendue de l’axe y](images/aboutgdip02-art01.png)

Un moniteur d’ordinateur crée son affichage sur un tableau rectangulaire de points appelés éléments d’image ou pixels. Le nombre de pixels apparaissant sur l’écran varie d’un moniteur à l’autre, et le nombre de pixels apparaissant sur une analyse individuelle peut généralement être configuré dans une certaine mesure par l’utilisateur.

![illustration d’une grille rectangulaire, avec trois cellules de cette grille libellées par leurs coordonnées](images/aboutgdip02-art02.png)

lorsque vous utilisez GDI+ pour dessiner une ligne, un rectangle ou une courbe, vous fournissez certaines informations clés sur l’élément à dessiner. Par exemple, vous pouvez spécifier une ligne en fournissant deux points, et vous pouvez spécifier un rectangle en fournissant un point, une hauteur et une largeur. GDI+ fonctionne conjointement avec le logiciel de pilote d’affichage pour déterminer les pixels qui doivent être activés pour afficher la ligne, le rectangle ou la courbe. L’illustration suivante montre les pixels activés pour afficher une ligne du point (4, 2) jusqu’au point (12, 8).

![Illustration montrant une grille rectangulaire avec des cellules remplies pour indiquer une ligne entre deux points de terminaison](images/aboutgdip02-art03.png)

Au fil du temps, certains blocs de construction de base se sont avérés les plus utiles pour créer des images à deux dimensions. ces blocs de construction, tous pris en charge par GDI+, sont répertoriés dans la liste suivante :

-   Lignes
-   Rectangles
-   Suspension
-   Arcs
-   Polygones
-   Splines cardinales
-   Splines de Bézier

la [**classe graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dans GDI+ fournit les méthodes suivantes pour dessiner les éléments de la liste précédente : [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (pour les splines cardinales) et [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Chacune de ces méthodes est surchargée ; autrement dit, chaque méthode est proposée en plusieurs variations avec différentes listes de paramètres. Par exemple, une variante de la méthode DrawLine reçoit l’adresse d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et quatre entiers, tandis qu’une autre variante de la méthode DrawLine reçoit l’adresse d’un objet **Pen** et deux références d’objet [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

Les méthodes permettant de dessiner des lignes, des rectangles et des splines de Bézier ont des méthodes auxiliaires qui dessinent plusieurs éléments dans un seul appel : [DrawLines](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)), [DrawRectangles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))et [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)). En outre, la méthode [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) a une méthode auxiliaire, [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)), qui ferme une courbe en reliant le point de fin de la courbe au point de départ.

Toutes les méthodes de dessin de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fonctionnent conjointement avec un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Par conséquent, pour pouvoir dessiner tout, vous devez créer au moins deux objets : un objet **Graphics** et un objet **Pen** . L’objet **Pen** stocke les attributs de l’élément à dessiner, tels que la largeur et la couleur de ligne. L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode de dessin. Par exemple, une variante de la méthode [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) reçoit l’adresse d’un objet **Pen** et quatre entiers comme indiqué dans le code suivant, qui dessine un rectangle avec une largeur de 100, une hauteur de 50 et un angle supérieur gauche de (20, 10).


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



