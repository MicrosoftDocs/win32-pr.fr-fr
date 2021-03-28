---
description: 'Vous pouvez activer la correction gamma pour un pinceau de dégradé en passant TRUE à la méthode PathGradientBrush :: SetGammaCorrection de ce pinceau.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Application d’une correction gamma à un dégradé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115271"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Application d’une correction gamma à un dégradé

Vous pouvez activer la correction gamma pour un pinceau de dégradé en passant **true** à la méthode [**PathGradientBrush :: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) de ce pinceau. Vous pouvez désactiver la correction gamma en passant la **valeur false** à la méthode **PathGradientBrush :: SetGammaCorrection** . La correction gamma est désactivée par défaut.

L’exemple suivant crée un pinceau de dégradé linéaire et utilise ce pinceau pour remplir deux rectangles. Le premier rectangle est rempli sans correction gamma et le deuxième rectangle est rempli avec la correction gamma.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



L’illustration suivante montre les deux rectangles remplis. Le rectangle supérieur, qui n’a pas de correction gamma, apparaît sombre au milieu. Le rectangle inférieur, qui a une correction gamma, semble avoir une intensité plus uniforme.

![Illustration montrant deux rectangles : le remplissage de couleur de la première varie en fonction de l’intensité, le remplissage de la seconde varie moins](images/gammagradient1.png)

L’exemple suivant crée un pinceau de dégradé de tracé basé sur un tracé en forme d’étoile. Le code utilise le pinceau de dégradé de tracé avec la correction gamma désactivée (valeur par défaut) pour remplir le tracé. Ensuite, le code passe **true** à la méthode [**PathGradientBrush :: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) pour activer la correction gamma pour le pinceau de dégradé du tracé. L’appel à [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) définit la transformation universelle d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) afin que l’appel suivant à [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplisse une étoile qui se trouve à droite de la première étoile.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



L’illustration suivante montre la sortie du code précédent. L’étoile à droite a une correction gamma. Notez que l’étoile sur la gauche, qui n’a pas de correction gamma, a des zones qui apparaissent sombres.

![illustration de 2 5-pointé commence par un dégradé de couleur ; la première a des zones sombres, la seconde ne le fait pas](images/gammagradient2.png)

 

 



