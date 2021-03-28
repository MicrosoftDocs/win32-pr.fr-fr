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
# <a name="global-and-local-transformations"></a>Transformations globales et locales

Une transformation globale est une transformation qui s’applique à chaque élément dessiné par un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) donné. Pour créer une transformation globale, construisez un objet **Graphics** , puis appelez sa méthode [**Graphics :: setTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) . La méthode **Graphics :: setTransform** manipule un objet [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) associé à l’objet **Graphics** . La transformation stockée dans cet objet de **matrice** est appelée *transformation universelle*. La transformation universelle peut être une transformation affine simple ou une séquence complexe de transformations affines, mais quelle que soit sa complexité, la transformation universelle est stockée dans un objet **matrice** unique.

La [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit plusieurs méthodes pour créer une transformation universelle composite : [**Graphics :: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics :: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics :: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)et [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform). L’exemple suivant dessine une ellipse deux fois : une fois avant de créer une transformation universelle et une fois après. La transformation se met d’abord à l’échelle d’un facteur de 0,5 sur l’axe y, puis convertit 50 unités dans la direction x, puis pivote de 30 degrés.


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



L’illustration suivante montre l’ellipse d’origine et l’ellipse transformée.

![capture d’écran d’une fenêtre contenant deux ellipses qui se chevauchent ; l’un est plus étroit et pivoté](images/aboutgdip05-art14.png)

> [!Note]  
> Dans l’exemple précédent, l’ellipse est pivotée sur l’origine du système de coordonnées, qui se trouve dans l’angle supérieur gauche de la zone cliente. Cela produit un résultat différent de la rotation de l’ellipse autour de son propre centre.

 

Une transformation locale est une transformation qui s’applique à un élément spécifique à dessiner. Par exemple, un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) a une méthode [**GraphicsPath :: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) qui vous permet de transformer les points de données de ce chemin d’accès. L’exemple suivant dessine un rectangle sans transformation et un tracé avec une transformation de rotation. (Supposez qu’il n’y a pas de transformation universelle.)


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Vous pouvez combiner la transformation universelle avec les transformations locales pour obtenir un grand nombre de résultats. Par exemple, vous pouvez utiliser la transformation universelle pour réviser le système de coordonnées et utiliser des transformations locales pour faire pivoter et mettre à l’échelle des objets dessinés sur le nouveau système de coordonnées.

Supposons que vous souhaitiez un système de coordonnées qui a son origine 200 pixels du bord gauche de la zone client et 150 pixels en haut de la zone cliente. En outre, supposons que vous souhaitiez que l’unité de mesure soit le pixel, l’axe des x pointant vers la droite et l’axe des y pointant vers le haut. Le système de coordonnées par défaut a l’axe des y pointant vers le dessous. vous devez donc effectuer une réflexion sur l’axe horizontal. L’illustration suivante montre la matrice d’une telle réflexion.

![Illustration montrant une matrice trois par trois](images/aboutgdip05-art15.png)

Supposons ensuite que vous deviez effectuer une translation de 200 unités à droite et de 150 unités.

L’exemple suivant établit le système de coordonnées qui vient d’être décrit en définissant la transformation universelle d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



Le code suivant (placé après le code de l’exemple précédent) crée un tracé qui se compose d’un seul rectangle avec son angle inférieur gauche à l’origine du nouveau système de coordonnées. Le rectangle est rempli une seule fois sans transformation locale et une fois avec une transformation locale. La transformation locale se compose d’une mise à l’échelle horizontale d’un facteur de 2, suivi d’une rotation de 30 degrés.


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



L’illustration suivante montre le nouveau système de coordonnées et les deux rectangles.

![capture d’écran d’un axe x et y, et un carré bleu superposé par un rectagle semi-transparent pivoté dans son angle inférieur gauche](images/aboutgdip05-art16.png)

 

 



