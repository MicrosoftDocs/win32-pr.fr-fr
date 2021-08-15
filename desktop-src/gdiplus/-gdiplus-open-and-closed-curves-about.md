---
description: 'L’illustration suivante montre deux courbes : une ouverte et une fermée.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Courbes ouvertes et fermées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383f7c68909a73291c00c6e760d1cc6554b061d5749b33e6e90ba3a986c71906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885124"
---
# <a name="open-and-closed-curves"></a>Courbes ouvertes et fermées

L’illustration suivante montre deux courbes : une ouverte et une fermée.

![illustration d’une courbe ouverte (une ligne courbée) et d’une courbe fermée (le contour d’une forme)](images/aboutgdip02-art24.png)

Les courbes fermées ont un intérieur et peuvent par conséquent être remplies à l’aide d’un pinceau. la classe [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) de Windows GDI+ fournit les méthodes suivantes pour remplir les figures fermées et les courbes : [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**graphics :: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)et [**graphics :: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). Chaque fois que vous appelez l’une de ces méthodes, vous devez passer l’adresse de l’un des types de pinceau spécifiques ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)ou [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) comme argument.

La méthode [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) est associée à la méthode [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) . Tout comme la méthode DrawArc dessine une partie du contour d’une ellipse, la méthode FillPie remplit une partie de l’intérieur d’une ellipse. L’exemple suivant dessine un arc et remplit la partie correspondante de l’intérieur de l’ellipse.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



L’illustration suivante montre l’arc et le secteur rempli.

![Illustration montrant un segment d’une Ellipse remplie](images/aboutgdip02-art25.png)

La méthode [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) est un complément de la méthode [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) . Les deux méthodes ferment automatiquement la courbe en connectant le point de fin au point de départ. L’exemple suivant dessine une courbe qui passe par (0, 0), (60, 20) et (40, 50). Ensuite, la courbe est fermée automatiquement en connectant (40, 50) au point de départ (0, 0), et l’intérieur est rempli avec une couleur unie.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Un chemin d’accès peut comprendre plusieurs figures (sous-tracés). La méthode [**Graphics :: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplit l’intérieur de chaque figure. Si une figure n’est pas fermée, la méthode **Graphics :: FillPath** remplit la zone qui serait placée si la figure était fermée. L’exemple suivant dessine et remplit un tracé constitué d’un arc, d’une spline cardinale, d’une chaîne et d’un graphique à secteurs.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



L’illustration suivante montre le chemin d’accès avant et après qu’il a été rempli d’un pinceau plein. Notez que le texte de la chaîne est entouré, mais pas rempli, par la méthode [**Graphics ::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . Il s’agit de la méthode [**Graphics :: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) qui peint l’intérieur des caractères de la chaîne.

![Illustration montrant deux fois le texte et une courbe ouverte et fermée ; ils sont vides la première fois et remplis la deuxième fois](images/aboutgdip02-art26.png)

 

 



