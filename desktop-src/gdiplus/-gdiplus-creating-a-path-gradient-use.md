---
description: La classe PathGradientBrush vous permet de personnaliser la façon dont vous remplissez une forme avec des couleurs à variation progressive.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Création d’un dégradé de tracé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562487"
---
# <a name="creating-a-path-gradient"></a><span data-ttu-id="a66bc-103">Création d’un dégradé de tracé</span><span class="sxs-lookup"><span data-stu-id="a66bc-103">Creating a Path Gradient</span></span>

<span data-ttu-id="a66bc-104">La classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) vous permet de personnaliser la façon dont vous remplissez une forme avec des couleurs à variation progressive.</span><span class="sxs-lookup"><span data-stu-id="a66bc-104">The [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class allows you to customize the way you fill a shape with gradually changing colors.</span></span> <span data-ttu-id="a66bc-105">Un objet **PathGradientBrush** possède un chemin d’accès de limite et un point central.</span><span class="sxs-lookup"><span data-stu-id="a66bc-105">A **PathGradientBrush** object has a boundary path and a center point.</span></span> <span data-ttu-id="a66bc-106">Vous pouvez spécifier une couleur pour le point central et une autre couleur pour la limite.</span><span class="sxs-lookup"><span data-stu-id="a66bc-106">You can specify one color for the center point and another color for the boundary.</span></span> <span data-ttu-id="a66bc-107">Vous pouvez également spécifier des couleurs distinctes pour chacun des points situés le long de la limite.</span><span class="sxs-lookup"><span data-stu-id="a66bc-107">You can also specify separate colors for each of several points along the boundary.</span></span>

> [!Note]  
> <span data-ttu-id="a66bc-108">Dans GDI+, un chemin d’accès est une séquence de lignes et de courbes gérée par un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="a66bc-108">In GDI+, a path is a sequence of lines and curves maintained by a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="a66bc-109">Pour plus d’informations sur les chemins d’accès GDI+, consultez [chemins](-gdiplus-paths-about.md) d’accès et [construction et traçage de chemins d'](-gdiplus-constructing-and-drawing-paths-use.md)accès.</span><span class="sxs-lookup"><span data-stu-id="a66bc-109">For more information about GDI+ paths, see [Paths](-gdiplus-paths-about.md) and [Constructing and Drawing Paths](-gdiplus-constructing-and-drawing-paths-use.md).</span></span>

 

<span data-ttu-id="a66bc-110">L’exemple suivant remplit une ellipse avec un pinceau de dégradé de tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-110">The following example fills an ellipse with a path gradient brush.</span></span> <span data-ttu-id="a66bc-111">La couleur centrale est définie sur bleu et la couleur limite est cyan.</span><span class="sxs-lookup"><span data-stu-id="a66bc-111">The center color is set to blue and the boundary color is set to aqua.</span></span>


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



<span data-ttu-id="a66bc-112">L’illustration suivante montre l’Ellipse remplie.</span><span class="sxs-lookup"><span data-stu-id="a66bc-112">The following illustration shows the filled ellipse.</span></span>

![Illustration montrant une ellipse avec un remplissage dégradé](images/pathgradient1.png)

<span data-ttu-id="a66bc-114">Par défaut, un pinceau de dégradé de tracé ne s’étend pas en dehors de la limite du tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-114">By default, a path gradient brush does not extend outside the boundary of the path.</span></span> <span data-ttu-id="a66bc-115">Si vous utilisez le pinceau de dégradé de tracé pour remplir une forme qui s’étend au-delà de la limite du tracé, la zone de l’écran à l’extérieur du tracé n’est pas remplie.</span><span class="sxs-lookup"><span data-stu-id="a66bc-115">If you use the path gradient brush to fill a shape that extends beyond the boundary of the path, the area of the screen outside the path will not be filled.</span></span> <span data-ttu-id="a66bc-116">L’illustration suivante montre ce qui se passe si vous remplacez l’appel [**Graphics :: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) dans le code précédent par `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .</span><span class="sxs-lookup"><span data-stu-id="a66bc-116">The following illustration shows what happens if you change the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) call in the preceding code to `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)`.</span></span>

![Illustration montrant une tranche horizontale de l’ellipse précédente](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a><span data-ttu-id="a66bc-118">Spécification de points sur la limite</span><span class="sxs-lookup"><span data-stu-id="a66bc-118">Specifying Points on the Boundary</span></span>

<span data-ttu-id="a66bc-119">L’exemple suivant construit un pinceau de dégradé de tracé à partir d’un tracé en forme d’étoile.</span><span class="sxs-lookup"><span data-stu-id="a66bc-119">The following example constructs a path gradient brush from a star-shaped path.</span></span> <span data-ttu-id="a66bc-120">Le code appelle la méthode [**PathGradientBrush :: SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) pour définir la couleur du centre de l’étoile sur rouge.</span><span class="sxs-lookup"><span data-stu-id="a66bc-120">The code calls the [**PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) method to set the color at the centroid of the star to red.</span></span> <span data-ttu-id="a66bc-121">Le code appelle ensuite la méthode [**PathGradientBrush :: SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) pour spécifier différentes couleurs (stockées dans le tableau de [**couleurs**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) aux points individuels dans le tableau de [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="a66bc-121">Then the code calls the [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) method to specify various colors (stored in the [**colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) array) at the individual points in the [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) array.</span></span> <span data-ttu-id="a66bc-122">L’instruction de code finale remplit le tracé en forme d’étoile avec le pinceau de dégradé du tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-122">The final code statement fills the star-shaped path with the path gradient brush.</span></span>


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



<span data-ttu-id="a66bc-123">L’illustration suivante montre l’étoile remplie.</span><span class="sxs-lookup"><span data-stu-id="a66bc-123">The following illustration shows the filled star.</span></span>

![Illustration montrant une étoile à cinq branches qui remplit le rouge au centre de différentes couleurs dans chaque point de l’étoile](images/pathgradient3.png)

<span data-ttu-id="a66bc-125">L’exemple suivant construit un pinceau de dégradé de tracé basé sur un tableau de points.</span><span class="sxs-lookup"><span data-stu-id="a66bc-125">The following example constructs a path gradient brush based on an array of points.</span></span> <span data-ttu-id="a66bc-126">Une couleur est assignée à chacun des cinq points du tableau.</span><span class="sxs-lookup"><span data-stu-id="a66bc-126">A color is assigned to each of the five points in the array.</span></span> <span data-ttu-id="a66bc-127">Si vous deviez relier les cinq points par des lignes droites, vous obtiendriez un polygone à cinq côtés.</span><span class="sxs-lookup"><span data-stu-id="a66bc-127">If you were to connect the five points by straight lines, you would get a five-sided polygon.</span></span> <span data-ttu-id="a66bc-128">Une couleur est également assignée au Centre (Centre de gravité) de ce polygone. dans cet exemple, le Centre (80, 75) est défini sur blanc.</span><span class="sxs-lookup"><span data-stu-id="a66bc-128">A color is also assigned to the center (centroid) of that polygon — in this example, the center (80, 75) is set to white.</span></span> <span data-ttu-id="a66bc-129">L’instruction de code finale dans l’exemple remplit un rectangle avec le pinceau de dégradé du tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-129">The final code statement in the example fills a rectangle with the path gradient brush.</span></span>

<span data-ttu-id="a66bc-130">La couleur utilisée pour remplir le rectangle est blanche à (80, 75) et change progressivement à mesure que vous vous éloignez de (80, 75) vers les points du tableau.</span><span class="sxs-lookup"><span data-stu-id="a66bc-130">The color used to fill the rectangle is white at (80, 75) and changes gradually as you move away from (80, 75) toward the points in the array.</span></span> <span data-ttu-id="a66bc-131">Par exemple, lorsque vous passez de (80, 75) à (0, 0), la couleur passe progressivement du blanc au rouge, et à mesure que vous passez de (80, 75) à (160), la couleur passe progressivement du blanc au vert.</span><span class="sxs-lookup"><span data-stu-id="a66bc-131">For example, as you move from (80, 75) to (0, 0), the color changes gradually from white to red, and as you move from (80, 75) to (160, 0), the color changes gradually from white to green.</span></span>


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



<span data-ttu-id="a66bc-132">Notez qu’il n’y a pas d’objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) dans le code précédent.</span><span class="sxs-lookup"><span data-stu-id="a66bc-132">Note that there is no [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object in the preceding code.</span></span> <span data-ttu-id="a66bc-133">Le constructeur [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) particulier de l’exemple reçoit un pointeur vers un tableau de points, mais ne requiert pas d’objet **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="a66bc-133">The particular [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) constructor in the example receives a pointer to an array of points but does not require a **GraphicsPath** object.</span></span> <span data-ttu-id="a66bc-134">Notez également que le pinceau de dégradé de tracé est utilisé pour remplir un rectangle, et non un tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-134">Also, note that the path gradient brush is used to fill a rectangle, not a path.</span></span> <span data-ttu-id="a66bc-135">Le rectangle est plus grand que le tracé utilisé pour définir le pinceau, donc un rectangle n’est pas peint par le pinceau.</span><span class="sxs-lookup"><span data-stu-id="a66bc-135">The rectangle is larger than the path used to define the brush, so some of the rectangle is not painted by the brush.</span></span> <span data-ttu-id="a66bc-136">L’illustration suivante montre le rectangle (ligne en pointillés) et la partie du rectangle peinte par le pinceau de dégradé du tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-136">The following illustration shows the rectangle (dotted line) and the portion of the rectangle painted by the path gradient brush.</span></span>

![Illustration montrant un rectangle délimité par une ligne en pointillés, partiellement peinte par un dégradé multicolore](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a><span data-ttu-id="a66bc-138">Personnalisation d’un dégradé de tracé</span><span class="sxs-lookup"><span data-stu-id="a66bc-138">Customizing a Path Gradient</span></span>

<span data-ttu-id="a66bc-139">L’une des façons de personnaliser un pinceau de dégradé de tracé consiste à définir ses échelles de focus.</span><span class="sxs-lookup"><span data-stu-id="a66bc-139">One way to customize a path gradient brush is to set its focus scales.</span></span> <span data-ttu-id="a66bc-140">Les échelles de focus spécifient un chemin d’accès interne qui se trouve à l’intérieur du chemin d’accès principal.</span><span class="sxs-lookup"><span data-stu-id="a66bc-140">The focus scales specify an inner path that lies inside the main path.</span></span> <span data-ttu-id="a66bc-141">La couleur centrale est affichée partout à l’intérieur de ce tracé interne et non uniquement au point central.</span><span class="sxs-lookup"><span data-stu-id="a66bc-141">The center color is displayed everywhere inside that inner path rather than only at the center point.</span></span> <span data-ttu-id="a66bc-142">Pour définir les échelles de focus d’un pinceau de dégradé de tracé, appelez la méthode [**PathGradientBrush :: SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .</span><span class="sxs-lookup"><span data-stu-id="a66bc-142">To set the focus scales of a path gradient brush, call the [**PathGradientBrush::SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) method.</span></span>

<span data-ttu-id="a66bc-143">L’exemple suivant crée un pinceau de dégradé de tracé basé sur un tracé elliptique.</span><span class="sxs-lookup"><span data-stu-id="a66bc-143">The following example creates a path gradient brush based on an elliptical path.</span></span> <span data-ttu-id="a66bc-144">Le code définit la couleur de la limite sur bleu, définit la couleur centrale en cyan, puis utilise le pinceau de dégradé du tracé pour remplir le tracé elliptique.</span><span class="sxs-lookup"><span data-stu-id="a66bc-144">The code sets the boundary color to blue, sets the center color to aqua, and then uses the path gradient brush to fill the elliptical path.</span></span>

<span data-ttu-id="a66bc-145">Ensuite, le code définit les échelles de focus du pinceau de dégradé du tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-145">Next the code sets the focus scales of the path gradient brush.</span></span> <span data-ttu-id="a66bc-146">L’échelle de focus x est définie sur 0,3, et l’échelle de focus y est définie sur 0,8.</span><span class="sxs-lookup"><span data-stu-id="a66bc-146">The x focus scale is set to 0.3, and the y focus scale is set to 0.8.</span></span> <span data-ttu-id="a66bc-147">Le code appelle la méthode [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) afin que l’appel suivant à [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplisse une ellipse qui se trouve à droite de la première ellipse.</span><span class="sxs-lookup"><span data-stu-id="a66bc-147">The code calls the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills an ellipse that sits to the right of the first ellipse.</span></span>

<span data-ttu-id="a66bc-148">Pour voir l’effet des échelles de focus, Imaginez une petite Ellipse qui partage son centre avec l’ellipse principale.</span><span class="sxs-lookup"><span data-stu-id="a66bc-148">To see the effect of the focus scales, imagine a small ellipse that shares its center with the main ellipse.</span></span> <span data-ttu-id="a66bc-149">La petite ellipse (interne) est l’ellipse principale mise à l’échelle (à propos de son centre) horizontalement par un facteur de 0,3 et verticalement par un facteur de 0,8.</span><span class="sxs-lookup"><span data-stu-id="a66bc-149">The small (inner) ellipse is the main ellipse scaled (about its center) horizontally by a factor of 0.3 and vertically by a factor of 0.8.</span></span> <span data-ttu-id="a66bc-150">Lorsque vous passez de la limite de l’ellipse externe à la limite de l’ellipse interne, la couleur passe progressivement du bleu au cyan.</span><span class="sxs-lookup"><span data-stu-id="a66bc-150">As you move from the boundary of the outer ellipse to the boundary of the inner ellipse, the color changes gradually from blue to aqua.</span></span> <span data-ttu-id="a66bc-151">Lorsque vous passez de la limite de l’ellipse interne au centre partagé, la couleur reste cyan.</span><span class="sxs-lookup"><span data-stu-id="a66bc-151">As you move from the boundary of the inner ellipse to the shared center, the color remains aqua.</span></span>


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



<span data-ttu-id="a66bc-152">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="a66bc-152">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="a66bc-153">L’ellipse sur la gauche est Aqua uniquement au point central.</span><span class="sxs-lookup"><span data-stu-id="a66bc-153">The ellipse on the left is aqua only at the center point.</span></span> <span data-ttu-id="a66bc-154">L’ellipse située à droite est Aqua partout dans le chemin interne.</span><span class="sxs-lookup"><span data-stu-id="a66bc-154">The ellipse on the right is aqua everywhere inside the inner path.</span></span>

![Illustration montrant deux ellipses qui dépassent de l’Aqua au bleu : la première a très peu de bleu clair ; la seconde a bien plus](images/focusscales1.png)

<span data-ttu-id="a66bc-156">Une autre façon de personnaliser un pinceau de dégradé de tracé consiste à spécifier un tableau de couleurs prédéfinies et un tableau de positions d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="a66bc-156">Another way to customize a path gradient brush is to specify an array of preset colors and an array of interpolation positions.</span></span>

<span data-ttu-id="a66bc-157">L’exemple suivant crée un pinceau de dégradé de tracé basé sur un triangle.</span><span class="sxs-lookup"><span data-stu-id="a66bc-157">The following example creates a path gradient brush based on a triangle.</span></span> <span data-ttu-id="a66bc-158">Le code appelle la méthode [**PathGradientBrush :: SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) du pinceau de dégradé de tracé pour spécifier un tableau de couleurs d’interpolation (vert foncé, cyan, bleu) et un tableau de positions d’interpolation (0, 0,25, 1).</span><span class="sxs-lookup"><span data-stu-id="a66bc-158">The code calls the [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) method of the path gradient brush to specify an array of interpolation colors (dark green, aqua, blue) and an array of interpolation positions (0, 0.25, 1).</span></span> <span data-ttu-id="a66bc-159">Lorsque vous passez de la limite du triangle au point central, la couleur passe progressivement du vert foncé au cyan, puis de l’Aqua au bleu.</span><span class="sxs-lookup"><span data-stu-id="a66bc-159">As you move from the boundary of the triangle to the center point, the color changes gradually from dark green to aqua and then from aqua to blue.</span></span> <span data-ttu-id="a66bc-160">Le changement du vert foncé au cyan se produit à 25% de la distance du vert foncé au bleu.</span><span class="sxs-lookup"><span data-stu-id="a66bc-160">The change from dark green to aqua happens in 25 percent of the distance from dark green to blue.</span></span>


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



<span data-ttu-id="a66bc-161">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="a66bc-161">The following illustration shows the output of the preceding code.</span></span>

![Illustration montrant un triangle qui s’ombre du bleu au centre, vers l’Aqua, en vert à l’arête](images/pathgradient4.png)

## <a name="setting-the-center-point"></a><span data-ttu-id="a66bc-163">Définition du point central</span><span class="sxs-lookup"><span data-stu-id="a66bc-163">Setting the Center Point</span></span>

<span data-ttu-id="a66bc-164">Par défaut, le point central d’un pinceau de dégradé de tracé est au centre de gravité du tracé utilisé pour construire le pinceau.</span><span class="sxs-lookup"><span data-stu-id="a66bc-164">By default, the center point of a path gradient brush is at the centroid of the path used to construct the brush.</span></span> <span data-ttu-id="a66bc-165">Vous pouvez modifier l’emplacement du point central en appelant la méthode [**PathGradientBrush :: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) de la classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="a66bc-165">You can change the location of the center point by calling the [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) method of the [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class.</span></span>

<span data-ttu-id="a66bc-166">L’exemple suivant crée un pinceau de dégradé de tracé basé sur une ellipse.</span><span class="sxs-lookup"><span data-stu-id="a66bc-166">The following example creates a path gradient brush based on an ellipse.</span></span> <span data-ttu-id="a66bc-167">Le centre de l’ellipse est à (70, 35), mais le point central du pinceau de dégradé du tracé est défini sur (120, 40).</span><span class="sxs-lookup"><span data-stu-id="a66bc-167">The center of the ellipse is at (70, 35), but the center point of the path gradient brush is set to (120, 40).</span></span>


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



<span data-ttu-id="a66bc-168">L’illustration suivante montre l’Ellipse remplie et le point central du pinceau de dégradé du tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-168">The following illustration shows the filled ellipse and the center point of the path gradient brush.</span></span>

![Illustration montrant une ellipse qui se remplit de bleu à cyan à partir d’un point central près d’une extrémité](images/pathgradient5.png)

<span data-ttu-id="a66bc-170">Vous pouvez définir le point central d’un pinceau de dégradé de tracé sur un emplacement en dehors du tracé utilisé pour construire le pinceau.</span><span class="sxs-lookup"><span data-stu-id="a66bc-170">You can set the center point of a path gradient brush to a location outside the path that was used to construct the brush.</span></span> <span data-ttu-id="a66bc-171">Dans le code précédent, si vous remplacez l’appel à [**PathGradientBrush :: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) par `pthGrBrush.SetCenterPoint(Point(145, 35))` , vous obtiendrez le résultat suivant.</span><span class="sxs-lookup"><span data-stu-id="a66bc-171">In the preceding code, if you replace the call to [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) with `pthGrBrush.SetCenterPoint(Point(145, 35))`, you will get the following result.</span></span>

![Illustration montrant une ellipse qui se remplit du rouge au jaune à partir d’un point central situé en dehors du bord de l’ellipse](images/pathgradient6.png)

<span data-ttu-id="a66bc-173">Dans l’illustration précédente, les points situés à l’extrême droite de l’ellipse ne sont pas des bleus purs (bien qu’ils soient très proches).</span><span class="sxs-lookup"><span data-stu-id="a66bc-173">In the preceding illustration, the points at the far right of the ellipse are not pure blue (although they are very close).</span></span> <span data-ttu-id="a66bc-174">Les couleurs du dégradé sont positionnées comme si le remplissage avait été autorisé à atteindre le point (145, 35), la couleur aurait atteint le bleu pur (0, 0, 255).</span><span class="sxs-lookup"><span data-stu-id="a66bc-174">The colors in the gradient are positioned as if the fill had been allowed to reach the point (145, 35), the color would have reached pure blue (0, 0, 255).</span></span> <span data-ttu-id="a66bc-175">Mais le remplissage n’atteint jamais (145, 35), car un pinceau de dégradé de tracé peint uniquement à l’intérieur de son tracé.</span><span class="sxs-lookup"><span data-stu-id="a66bc-175">But the fill never reaches (145, 35) because a path gradient brush paints only inside its path.</span></span>

 

 
