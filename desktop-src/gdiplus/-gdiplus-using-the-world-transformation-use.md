---
description: La transformation universelle est une propriété de la classe Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilisation de la transformation universelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201404"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="7c9e9-103">Utilisation de la transformation universelle</span><span class="sxs-lookup"><span data-stu-id="7c9e9-103">Using the World Transformation</span></span>

<span data-ttu-id="7c9e9-104">La transformation universelle est une propriété de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="7c9e9-104">The world transformation is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="7c9e9-105">Les nombres qui spécifient la transformation universelle sont stockés dans un objet [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , qui représente une matrice 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="7c9e9-105">The numbers that specify the world transformation are stored in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object, which represents a 3 ×3 matrix.</span></span> <span data-ttu-id="7c9e9-106">Les classes **Matrix** et **Graphics** disposent de plusieurs méthodes pour définir les nombres dans la matrice de transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="7c9e9-106">The **Matrix** and **Graphics** classes have several methods for setting the numbers in the world transformation matrix.</span></span> <span data-ttu-id="7c9e9-107">Les exemples de cette section manipulent des rectangles, car les rectangles sont faciles à dessiner et il est facile de voir les effets des transformations sur les rectangles.</span><span class="sxs-lookup"><span data-stu-id="7c9e9-107">The examples in this section manipulate rectangles because rectangles are easy to draw and it is easy to see the effects of transformations on rectangles.</span></span>

<span data-ttu-id="7c9e9-108">Nous commençons par créer un rectangle de 50 par 50 et en le localisant à l’origine (0,0).</span><span class="sxs-lookup"><span data-stu-id="7c9e9-108">We start by creating a 50 by 50 rectangle and locating it at the origin (0, 0).</span></span> <span data-ttu-id="7c9e9-109">L’origine se trouve dans le coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="7c9e9-109">The origin is at the upper-left corner of the client area.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="7c9e9-110">Le code suivant applique une transformation de mise à l’échelle qui développe le rectangle d’un facteur de 1,75 dans la direction x et réduit le rectangle d’un facteur de 0,5 dans l’axe y :</span><span class="sxs-lookup"><span data-stu-id="7c9e9-110">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="7c9e9-111">Le résultat est un rectangle qui est plus long dans la direction x et plus petit dans le sens y que l’original.</span><span class="sxs-lookup"><span data-stu-id="7c9e9-111">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>

<span data-ttu-id="7c9e9-112">Pour faire pivoter le rectangle au lieu de le mettre à l’échelle, utilisez le code suivant au lieu du code précédent :</span><span class="sxs-lookup"><span data-stu-id="7c9e9-112">To rotate the rectangle instead of scaling it, use the following code instead of the preceding code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="7c9e9-113">Pour traduire le rectangle, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="7c9e9-113">To translate the rectangle, use the following code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



