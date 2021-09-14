---
description: La classe PathGradientBrush vous permet de personnaliser la façon dont vous remplissez une forme avec des couleurs à variation progressive.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Création d’un dégradé de tracé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192144"
---
# <a name="creating-a-path-gradient"></a>Création d’un dégradé de tracé

La classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) vous permet de personnaliser la façon dont vous remplissez une forme avec des couleurs à variation progressive. Un objet **PathGradientBrush** possède un chemin d’accès de limite et un point central. Vous pouvez spécifier une couleur pour le point central et une autre couleur pour la limite. Vous pouvez également spécifier des couleurs distinctes pour chacun des points situés le long de la limite.

> [!Note]  
> dans GDI+, un chemin d’accès est une séquence de lignes et de courbes gérée par un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . pour plus d’informations sur les chemins d’accès GDI+, consultez [chemins](-gdiplus-paths-about.md) d’accès et [construction et traçage de chemins d'](-gdiplus-constructing-and-drawing-paths-use.md)accès.

 

L’exemple suivant remplit une ellipse avec un pinceau de dégradé de tracé. La couleur centrale est définie sur bleu et la couleur limite est cyan.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



L’illustration suivante montre l’Ellipse remplie.

![Illustration montrant une ellipse avec un remplissage dégradé](images/pathgradient1.png)

Par défaut, un pinceau de dégradé de tracé ne s’étend pas en dehors de la limite du tracé. Si vous utilisez le pinceau de dégradé de tracé pour remplir une forme qui s’étend au-delà de la limite du tracé, la zone de l’écran à l’extérieur du tracé n’est pas remplie. L’illustration suivante montre ce qui se passe si vous remplacez l’appel [**Graphics :: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) dans le code précédent par `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .

![Illustration montrant une tranche horizontale de l’ellipse précédente](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a>Spécification de points sur la limite

L’exemple suivant construit un pinceau de dégradé de tracé à partir d’un tracé en forme d’étoile. Le code appelle la méthode [**PathGradientBrush :: SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) pour définir la couleur du centre de l’étoile sur rouge. Le code appelle ensuite la méthode [**PathGradientBrush :: SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) pour spécifier différentes couleurs (stockées dans le tableau de [**couleurs**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) aux points individuels dans le tableau de [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . L’instruction de code finale remplit le tracé en forme d’étoile avec le pinceau de dégradé du tracé.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

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
```



L’illustration suivante montre l’étoile remplie.

![Illustration montrant une étoile à cinq branches qui remplit le rouge au centre de différentes couleurs dans chaque point de l’étoile](images/pathgradient3.png)

L’exemple suivant construit un pinceau de dégradé de tracé basé sur un tableau de points. Une couleur est assignée à chacun des cinq points du tableau. Si vous deviez relier les cinq points par des lignes droites, vous obtiendriez un polygone à cinq côtés. Une couleur est également assignée au Centre (Centre de gravité) de ce polygone. dans cet exemple, le Centre (80, 75) est défini sur blanc. L’instruction de code finale dans l’exemple remplit un rectangle avec le pinceau de dégradé du tracé.

La couleur utilisée pour remplir le rectangle est blanche à (80, 75) et change progressivement à mesure que vous vous éloignez de (80, 75) vers les points du tableau. Par exemple, lorsque vous passez de (80, 75) à (0, 0), la couleur passe progressivement du blanc au rouge, et à mesure que vous passez de (80, 75) à (160), la couleur passe progressivement du blanc au vert.


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



Notez qu’il n’y a pas d’objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) dans le code précédent. Le constructeur [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) particulier de l’exemple reçoit un pointeur vers un tableau de points, mais ne requiert pas d’objet **GraphicsPath** . Notez également que le pinceau de dégradé de tracé est utilisé pour remplir un rectangle, et non un tracé. Le rectangle est plus grand que le tracé utilisé pour définir le pinceau, donc un rectangle n’est pas peint par le pinceau. L’illustration suivante montre le rectangle (ligne en pointillés) et la partie du rectangle peinte par le pinceau de dégradé du tracé.

![Illustration montrant un rectangle délimité par une ligne en pointillés, partiellement peinte par un dégradé multicolore](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a>Personnalisation d’un dégradé de tracé

L’une des façons de personnaliser un pinceau de dégradé de tracé consiste à définir ses échelles de focus. Les échelles de focus spécifient un chemin d’accès interne qui se trouve à l’intérieur du chemin d’accès principal. La couleur centrale est affichée partout à l’intérieur de ce tracé interne et non uniquement au point central. Pour définir les échelles de focus d’un pinceau de dégradé de tracé, appelez la méthode [**PathGradientBrush :: SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .

L’exemple suivant crée un pinceau de dégradé de tracé basé sur un tracé elliptique. Le code définit la couleur de la limite sur bleu, définit la couleur centrale en cyan, puis utilise le pinceau de dégradé du tracé pour remplir le tracé elliptique.

Ensuite, le code définit les échelles de focus du pinceau de dégradé du tracé. L’échelle de focus x est définie sur 0,3, et l’échelle de focus y est définie sur 0,8. Le code appelle la méthode [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) afin que l’appel suivant à [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplisse une ellipse qui se trouve à droite de la première ellipse.

Pour voir l’effet des échelles de focus, Imaginez une petite Ellipse qui partage son centre avec l’ellipse principale. La petite ellipse (interne) est l’ellipse principale mise à l’échelle (à propos de son centre) horizontalement par un facteur de 0,3 et verticalement par un facteur de 0,8. Lorsque vous passez de la limite de l’ellipse externe à la limite de l’ellipse interne, la couleur passe progressivement du bleu au cyan. Lorsque vous passez de la limite de l’ellipse interne au centre partagé, la couleur reste cyan.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



L’illustration suivante montre la sortie du code précédent. L’ellipse sur la gauche est Aqua uniquement au point central. L’ellipse située à droite est Aqua partout dans le chemin interne.

![Illustration montrant deux ellipses qui dépassent de l’Aqua au bleu : la première a très peu de bleu clair ; la seconde a bien plus](images/focusscales1.png)

Une autre façon de personnaliser un pinceau de dégradé de tracé consiste à spécifier un tableau de couleurs prédéfinies et un tableau de positions d’interpolation.

L’exemple suivant crée un pinceau de dégradé de tracé basé sur un triangle. Le code appelle la méthode [**PathGradientBrush :: SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) du pinceau de dégradé de tracé pour spécifier un tableau de couleurs d’interpolation (vert foncé, cyan, bleu) et un tableau de positions d’interpolation (0, 0,25, 1). Lorsque vous passez de la limite du triangle au point central, la couleur passe progressivement du vert foncé au cyan, puis de l’Aqua au bleu. Le changement du vert foncé au cyan se produit à 25% de la distance du vert foncé au bleu.


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



L’illustration suivante montre la sortie du code précédent.

![Illustration montrant un triangle qui s’ombre du bleu au centre, vers l’Aqua, en vert à l’arête](images/pathgradient4.png)

## <a name="setting-the-center-point"></a>Définition du point central

Par défaut, le point central d’un pinceau de dégradé de tracé est au centre de gravité du tracé utilisé pour construire le pinceau. Vous pouvez modifier l’emplacement du point central en appelant la méthode [**PathGradientBrush :: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) de la classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .

L’exemple suivant crée un pinceau de dégradé de tracé basé sur une ellipse. Le centre de l’ellipse est à (70, 35), mais le point central du pinceau de dégradé du tracé est défini sur (120, 40).


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



L’illustration suivante montre l’Ellipse remplie et le point central du pinceau de dégradé du tracé.

![Illustration montrant une ellipse qui se remplit de bleu à cyan à partir d’un point central près d’une extrémité](images/pathgradient5.png)

Vous pouvez définir le point central d’un pinceau de dégradé de tracé sur un emplacement en dehors du tracé utilisé pour construire le pinceau. Dans le code précédent, si vous remplacez l’appel à [**PathGradientBrush :: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) par `pthGrBrush.SetCenterPoint(Point(145, 35))` , vous obtiendrez le résultat suivant.

![Illustration montrant une ellipse qui se remplit du rouge au jaune à partir d’un point central situé en dehors du bord de l’ellipse](images/pathgradient6.png)

Dans l’illustration précédente, les points situés à l’extrême droite de l’ellipse ne sont pas des bleus purs (bien qu’ils soient très proches). Les couleurs du dégradé sont positionnées comme si le remplissage avait été autorisé à atteindre le point (145, 35), la couleur aurait atteint le bleu pur (0, 0, 255). Mais le remplissage n’atteint jamais (145, 35), car un pinceau de dégradé de tracé peint uniquement à l’intérieur de son tracé.

 

 
