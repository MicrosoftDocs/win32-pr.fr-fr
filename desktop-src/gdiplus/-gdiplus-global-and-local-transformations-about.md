---
description: Une transformation globale est une transformation qui s’applique à chaque élément dessiné par un objet Graphics donné.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Transformations globales et locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558811"
---
# <a name="global-and-local-transformations"></a><span data-ttu-id="93f8c-103">Transformations globales et locales</span><span class="sxs-lookup"><span data-stu-id="93f8c-103">Global and Local Transformations</span></span>

<span data-ttu-id="93f8c-104">Une transformation globale est une transformation qui s’applique à chaque élément dessiné par un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) donné.</span><span class="sxs-lookup"><span data-stu-id="93f8c-104">A global transformation is a transformation that applies to every item drawn by a given [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="93f8c-105">Pour créer une transformation globale, construisez un objet **Graphics** , puis appelez sa méthode [**Graphics :: setTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) .</span><span class="sxs-lookup"><span data-stu-id="93f8c-105">To create a global transformation, construct a **Graphics** object, and then call its [**Graphics::SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) method.</span></span> <span data-ttu-id="93f8c-106">La méthode **Graphics :: setTransform** manipule un objet [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) associé à l’objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="93f8c-106">The **Graphics::SetTransform** method manipulates a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object that is associated with the **Graphics** object.</span></span> <span data-ttu-id="93f8c-107">La transformation stockée dans cet objet de **matrice** est appelée *transformation universelle*.</span><span class="sxs-lookup"><span data-stu-id="93f8c-107">The transformation stored in that **Matrix** object is called the *world transformation*.</span></span> <span data-ttu-id="93f8c-108">La transformation universelle peut être une transformation affine simple ou une séquence complexe de transformations affines, mais quelle que soit sa complexité, la transformation universelle est stockée dans un objet **matrice** unique.</span><span class="sxs-lookup"><span data-stu-id="93f8c-108">The world transformation can be a simple affine transformation or a complex sequence of affine transformations, but regardless of its complexity, the world transformation is stored in a single **Matrix** object.</span></span>

<span data-ttu-id="93f8c-109">La [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit plusieurs méthodes pour créer une transformation universelle composite : [**Graphics :: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics :: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics :: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)et [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span><span class="sxs-lookup"><span data-stu-id="93f8c-109">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several methods for building up a composite world transformation: [**Graphics::MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics::ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform), and [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span></span> <span data-ttu-id="93f8c-110">L’exemple suivant dessine une ellipse deux fois : une fois avant de créer une transformation universelle et une fois après.</span><span class="sxs-lookup"><span data-stu-id="93f8c-110">The following example draws an ellipse twice: once before creating a world transformation and once after.</span></span> <span data-ttu-id="93f8c-111">La transformation se met d’abord à l’échelle d’un facteur de 0,5 sur l’axe y, puis convertit 50 unités dans la direction x, puis pivote de 30 degrés.</span><span class="sxs-lookup"><span data-stu-id="93f8c-111">The transformation first scales by a factor of 0.5 in the y direction, then translates 50 units in the x direction, and then rotates 30 degrees.</span></span>


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



<span data-ttu-id="93f8c-112">L’illustration suivante montre l’ellipse d’origine et l’ellipse transformée.</span><span class="sxs-lookup"><span data-stu-id="93f8c-112">The following illustration shows the original ellipse and the transformed ellipse.</span></span>

![capture d’écran d’une fenêtre contenant deux ellipses qui se chevauchent ; l’un est plus étroit et pivoté](images/aboutgdip05-art14.png)

> [!Note]  
> <span data-ttu-id="93f8c-114">Dans l’exemple précédent, l’ellipse est pivotée sur l’origine du système de coordonnées, qui se trouve dans l’angle supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="93f8c-114">In the previous example, the ellipse is rotated about the origin of the coordinate system, which is at the upper–left corner of the client area.</span></span> <span data-ttu-id="93f8c-115">Cela produit un résultat différent de la rotation de l’ellipse autour de son propre centre.</span><span class="sxs-lookup"><span data-stu-id="93f8c-115">This produces a different result than rotating the ellipse about its own center.</span></span>

 

<span data-ttu-id="93f8c-116">Une transformation locale est une transformation qui s’applique à un élément spécifique à dessiner.</span><span class="sxs-lookup"><span data-stu-id="93f8c-116">A local transformation is a transformation that applies to a specific item to be drawn.</span></span> <span data-ttu-id="93f8c-117">Par exemple, un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) a une méthode [**GraphicsPath :: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) qui vous permet de transformer les points de données de ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="93f8c-117">For example, a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object has a [**GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) method that allows you to transform the data points of that path.</span></span> <span data-ttu-id="93f8c-118">L’exemple suivant dessine un rectangle sans transformation et un tracé avec une transformation de rotation.</span><span class="sxs-lookup"><span data-stu-id="93f8c-118">The following example draws a rectangle with no transformation and a path with a rotation transformation.</span></span> <span data-ttu-id="93f8c-119">(Supposez qu’il n’y a pas de transformation universelle.)</span><span class="sxs-lookup"><span data-stu-id="93f8c-119">(Assume that there is no world transformation.)</span></span>


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="93f8c-120">Vous pouvez combiner la transformation universelle avec les transformations locales pour obtenir un grand nombre de résultats.</span><span class="sxs-lookup"><span data-stu-id="93f8c-120">You can combine the world transformation with local transformations to achieve a variety of results.</span></span> <span data-ttu-id="93f8c-121">Par exemple, vous pouvez utiliser la transformation universelle pour réviser le système de coordonnées et utiliser des transformations locales pour faire pivoter et mettre à l’échelle des objets dessinés sur le nouveau système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="93f8c-121">For example, you can use the world transformation to revise the coordinate system and use local transformations to rotate and scale objects drawn on the new coordinate system.</span></span>

<span data-ttu-id="93f8c-122">Supposons que vous souhaitiez un système de coordonnées qui a son origine 200 pixels du bord gauche de la zone client et 150 pixels en haut de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="93f8c-122">Suppose you want a coordinate system that has its origin 200 pixels from the left edge of the client area and 150 pixels from the top of the client area.</span></span> <span data-ttu-id="93f8c-123">En outre, supposons que vous souhaitiez que l’unité de mesure soit le pixel, l’axe des x pointant vers la droite et l’axe des y pointant vers le haut.</span><span class="sxs-lookup"><span data-stu-id="93f8c-123">Furthermore, assume that you want the unit of measure to be the pixel, with the x-axis pointing to the right and the y-axis pointing up.</span></span> <span data-ttu-id="93f8c-124">Le système de coordonnées par défaut a l’axe des y pointant vers le dessous. vous devez donc effectuer une réflexion sur l’axe horizontal.</span><span class="sxs-lookup"><span data-stu-id="93f8c-124">The default coordinate system has the y-axis pointing down, so you need to perform a reflection across the horizontal axis.</span></span> <span data-ttu-id="93f8c-125">L’illustration suivante montre la matrice d’une telle réflexion.</span><span class="sxs-lookup"><span data-stu-id="93f8c-125">The following illustration shows the matrix of such a reflection.</span></span>

![Illustration montrant une matrice trois par trois](images/aboutgdip05-art15.png)

<span data-ttu-id="93f8c-127">Supposons ensuite que vous deviez effectuer une translation de 200 unités à droite et de 150 unités.</span><span class="sxs-lookup"><span data-stu-id="93f8c-127">Next, assume you need to perform a translation 200 units to the right and 150 units down.</span></span>

<span data-ttu-id="93f8c-128">L’exemple suivant établit le système de coordonnées qui vient d’être décrit en définissant la transformation universelle d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="93f8c-128">The following example establishes the coordinate system just described by setting the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



<span data-ttu-id="93f8c-129">Le code suivant (placé après le code de l’exemple précédent) crée un tracé qui se compose d’un seul rectangle avec son angle inférieur gauche à l’origine du nouveau système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="93f8c-129">The following code (placed after the code in the preceding example) creates a path that consists of a single rectangle with its lower-left corner at the origin of the new coordinate system.</span></span> <span data-ttu-id="93f8c-130">Le rectangle est rempli une seule fois sans transformation locale et une fois avec une transformation locale.</span><span class="sxs-lookup"><span data-stu-id="93f8c-130">The rectangle is filled once with no local transformation and once with a local transformation.</span></span> <span data-ttu-id="93f8c-131">La transformation locale se compose d’une mise à l’échelle horizontale d’un facteur de 2, suivi d’une rotation de 30 degrés.</span><span class="sxs-lookup"><span data-stu-id="93f8c-131">The local transformation consists of a horizontal scaling by a factor of 2 followed by a 30-degree rotation.</span></span>


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



<span data-ttu-id="93f8c-132">L’illustration suivante montre le nouveau système de coordonnées et les deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="93f8c-132">The following illustration shows the new coordinate system and the two rectangles.</span></span>

![capture d’écran d’un axe x et y, et un carré bleu superposé par un rectagle semi-transparent pivoté dans son angle inférieur gauche](images/aboutgdip05-art16.png)

 

 



