---
description: Une figure fermée, telle qu’un rectangle ou une ellipse, se compose d’un plan et d’un intérieur.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pinceaux et formes remplies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566200"
---
# <a name="brushes-and-filled-shapes"></a><span data-ttu-id="3bcd7-103">Pinceaux et formes remplies</span><span class="sxs-lookup"><span data-stu-id="3bcd7-103">Brushes and Filled Shapes</span></span>

<span data-ttu-id="3bcd7-104">Une figure fermée, telle qu’un rectangle ou une ellipse, se compose d’un plan et d’un intérieur.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-104">A closed figure such as a rectangle or an ellipse consists of an outline and an interior.</span></span> <span data-ttu-id="3bcd7-105">Le contour est dessiné à l’aide d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et l’intérieur est rempli d’un objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="3bcd7-105">The outline is drawn with a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and the interior is filled with a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="3bcd7-106">Windows GDI+ fournit plusieurs classes Brush pour remplir l’intérieur des figures fermées : [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)et [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="3bcd7-106">Windows GDI+ provides several brush classes for filling the interiors of closed figures: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), and [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span></span> <span data-ttu-id="3bcd7-107">Toutes ces classes héritent de la classe **Brush** .</span><span class="sxs-lookup"><span data-stu-id="3bcd7-107">All these classes inherit from the **Brush** class.</span></span> <span data-ttu-id="3bcd7-108">L’illustration suivante montre un rectangle rempli d’un pinceau plein et une Ellipse remplie avec un pinceau hachuré.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-108">The following illustration shows a rectangle filled with a solid brush and an ellipse filled with a hatch brush.</span></span>

![Illustration montrant un rectangle bleu et une ellipse magenta remplie d’un motif hachuré bleu](images/aboutgdip02-art17.png)

 

-   [<span data-ttu-id="3bcd7-110">Pinceaux solides</span><span class="sxs-lookup"><span data-stu-id="3bcd7-110">Solid Brushes</span></span>](#solid-brushes)
-   [<span data-ttu-id="3bcd7-111">Pinceaux hachuré</span><span class="sxs-lookup"><span data-stu-id="3bcd7-111">Hatch Brushes</span></span>](#hatch-brushes)
-   [<span data-ttu-id="3bcd7-112">Pinceaux de texture</span><span class="sxs-lookup"><span data-stu-id="3bcd7-112">Texture Brushes</span></span>](#texture-brushes)
-   [<span data-ttu-id="3bcd7-113">Pinceaux de dégradé</span><span class="sxs-lookup"><span data-stu-id="3bcd7-113">Gradient Brushes</span></span>](#gradient-brushes)

## <a name="solid-brushes"></a><span data-ttu-id="3bcd7-114">Pinceaux solides</span><span class="sxs-lookup"><span data-stu-id="3bcd7-114">Solid Brushes</span></span>

<span data-ttu-id="3bcd7-115">Pour remplir une forme fermée, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="3bcd7-115">To fill a closed shape, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="3bcd7-116">L’objet **Graphics** fournit des méthodes, telles que [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) et [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), et l’objet **Brush** stocke les attributs du remplissage, tels que la couleur et le motif.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-116">The **Graphics** object provides methods, such as [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) and [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), and the **Brush** object stores attributes of the fill, such as color and pattern.</span></span> <span data-ttu-id="3bcd7-117">L’adresse de l’objet **Brush** est passée comme l’un des arguments à la méthode Fill.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-117">The address of the **Brush** object is passed as one of the arguments to the fill method.</span></span> <span data-ttu-id="3bcd7-118">L’exemple suivant remplit une ellipse avec une couleur rouge unie.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-118">The following example fills an ellipse with a solid red color.</span></span>


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



<span data-ttu-id="3bcd7-119">Notez que dans l’exemple précédent, le pinceau est de type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), qui hérite de [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span><span class="sxs-lookup"><span data-stu-id="3bcd7-119">Note that in the preceding example, the brush is of type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), which inherits from [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span></span>

## <a name="hatch-brushes"></a><span data-ttu-id="3bcd7-120">Pinceaux hachuré</span><span class="sxs-lookup"><span data-stu-id="3bcd7-120">Hatch Brushes</span></span>

<span data-ttu-id="3bcd7-121">Lorsque vous remplissez une forme avec un pinceau hachuré, vous spécifiez une couleur de premier plan, une couleur d’arrière-plan et un style de hachurage.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-121">When you fill a shape with a hatch brush, you specify a foreground color, a background color, and a hatch style.</span></span> <span data-ttu-id="3bcd7-122">La couleur de premier plan est la couleur de la hachure.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-122">The foreground color is the color of the hatching.</span></span>


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



<span data-ttu-id="3bcd7-123">GDI+ fournit plus de 50 styles de hachures, spécifiés dans [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span><span class="sxs-lookup"><span data-stu-id="3bcd7-123">GDI+ provides more than 50 hatch styles, specified in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span></span> <span data-ttu-id="3bcd7-124">Les trois styles indiqués dans l’illustration suivante sont horizontal, ForwardDiagonal et Cross.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-124">The three styles shown in the following illustration are Horizontal, ForwardDiagonal, and Cross.</span></span>

![Illustration montrant trois ellipses colorées en bleu, chacune avec un style de hachurage différent](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a><span data-ttu-id="3bcd7-126">Pinceaux de texture</span><span class="sxs-lookup"><span data-stu-id="3bcd7-126">Texture Brushes</span></span>

<span data-ttu-id="3bcd7-127">Avec un pinceau de texture, vous pouvez remplir une forme à l’aide d’un modèle stocké dans une bitmap.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-127">With a texture brush, you can fill a shape with a pattern stored in a bitmap.</span></span> <span data-ttu-id="3bcd7-128">Par exemple, supposons que l’image suivante soit stockée dans un fichier sur disque nommé MyTexture.bmp.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-128">For example, suppose the following picture is stored in a disk file named MyTexture.bmp.</span></span>

![capture d’écran d’un petit carré rempli avec différentes couleurs](images/aboutgdip02-art19.png)

<span data-ttu-id="3bcd7-130&quot;>L’exemple suivant remplit une ellipse en répétant l’image stockée dans MyTexture.bmp.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3bcd7-130&quot;>The following example fills an ellipse by repeating the picture stored in MyTexture.bmp.</span></span>


```
Image myImage(L&quot;MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



<span data-ttu-id="3bcd7-131">L’illustration suivante montre l’Ellipse remplie.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-131">The following illustration shows the filled ellipse.</span></span>

![Illustration montrant une Ellipse remplie avec le modèle défini précédemment](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a><span data-ttu-id="3bcd7-133">Pinceaux de dégradé</span><span class="sxs-lookup"><span data-stu-id="3bcd7-133">Gradient Brushes</span></span>

<span data-ttu-id="3bcd7-134">Vous pouvez utiliser un pinceau de dégradé pour remplir une forme avec une couleur qui change progressivement d’une partie de la forme à une autre.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-134">You can use a gradient brush to fill a shape with a color that changes gradually from one part of the shape to another.</span></span> <span data-ttu-id="3bcd7-135">Par exemple, un pinceau de dégradé horizontal change de couleur lorsque vous passez du côté gauche d’une figure à droite.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-135">For example, a horizontal gradient brush will change color as you move from the left side of a figure to the right side.</span></span> <span data-ttu-id="3bcd7-136">L’exemple suivant remplit une ellipse avec un pinceau de dégradé horizontal qui passe du bleu au vert lorsque vous vous déplacez du côté gauche de l’ellipse vers le côté droit.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-136">The following example fills an ellipse with a horizontal gradient brush that changes from blue to green as you move from the left side of the ellipse to the right side.</span></span>


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



<span data-ttu-id="3bcd7-137">L’illustration suivante montre l’Ellipse remplie.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-137">The following illustration shows the filled ellipse.</span></span>

![Illustration montrant une ellipse avec un dégradé : bleu à droite au vert à gauche](images/aboutgdip02-art21.png)

<span data-ttu-id="3bcd7-139">Vous pouvez configurer un pinceau de dégradé de tracé pour modifier la couleur au fur et à mesure que vous déplacez du centre d’une figure vers la limite.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-139">A path gradient brush can be configured to change color as you move from the center of a figure toward the boundary.</span></span>

![Ilustration d’une ellipse en bleu foncé au centre, en l’ombrage du bleu clair à la périphérie](images/aboutgdip02-art22.png)

<span data-ttu-id="3bcd7-141">Les pinceaux de dégradé de tracés sont relativement flexibles.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-141">Path gradient brushes are quite flexible.</span></span> <span data-ttu-id="3bcd7-142">Le pinceau de dégradé utilisé pour remplir le triangle dans l’illustration suivante change progressivement du rouge au centre de trois couleurs différentes aux sommets.</span><span class="sxs-lookup"><span data-stu-id="3bcd7-142">The gradient brush used to fill the triangle in the following illustration changes gradually from red at the center to each of three different colors at the vertices.</span></span>

![illustration d’un triangle rouge au centre, en l’ombrage d’une couleur différente à chaque vertex](images/aboutgdip02-art23.png)

 

 



