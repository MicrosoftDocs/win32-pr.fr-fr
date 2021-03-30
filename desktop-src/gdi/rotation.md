---
description: De nombreuses applications CAO offrent des fonctionnalités qui font pivoter des objets dessinés dans la zone cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973711"
---
# <a name="rotation"></a><span data-ttu-id="bbae5-103">Rotation</span><span class="sxs-lookup"><span data-stu-id="bbae5-103">Rotation</span></span>

<span data-ttu-id="bbae5-104">De nombreuses applications CAO offrent des fonctionnalités qui font pivoter des objets dessinés dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="bbae5-104">Many CAD applications provide features that rotate objects drawn in the client area.</span></span> <span data-ttu-id="bbae5-105">Les applications qui incluent des fonctionnalités de rotation utilisent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir l’espace universel approprié sur la transformation d’espace de page.</span><span class="sxs-lookup"><span data-stu-id="bbae5-105">Applications that include rotation capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="bbae5-106">Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="bbae5-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="bbae5-107">Les membres eM11, eM12, eM21 et eM22 de XFORM spécifient respectivement le cosinus, le sinus, le sinus négatif et le cosinus de l’angle de rotation.</span><span class="sxs-lookup"><span data-stu-id="bbae5-107">The eM11, eM12, eM21, and eM22 members of XFORM specify respectively, the cosine, sine, negative sine, and cosine of the angle of rotation.</span></span>

<span data-ttu-id="bbae5-108">Lorsque la *rotation* se produit, les points qui constituent un objet sont pivotés par rapport à l’origine de l’espace de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="bbae5-108">When *rotation* occurs, the points that constitute an object are rotated with respect to the coordinate-space origin.</span></span> <span data-ttu-id="bbae5-109">L’illustration suivante montre un rectangle 20 par 20, pivoté de 30 degrés lorsqu’il est copié à partir de l’espace de coordonnées universelles vers l’espace de coordonnées de page.</span><span class="sxs-lookup"><span data-stu-id="bbae5-109">The following illustration shows a 20-by-20-unit rectangle rotated 30 degrees when copied from world-coordinate space to page-coordinate space.</span></span>

![Illustration montrant deux espaces de coordonnées ; chaque a un rectange dans un emplacement différent et avec une rotation différente](images/cstrn-11.png)

<span data-ttu-id="bbae5-111">Dans l’illustration précédente, chaque point du rectangle a pivoté de 30 degrés par rapport à l’origine de l’espace de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="bbae5-111">In the preceding illustration, each point in the rectangle was rotated 30 degrees with respect to the coordinate-space origin.</span></span>

<span data-ttu-id="bbae5-112">L’algorithme suivant calcule la nouvelle coordonnée x (x) pour un point (x, y) qui pivote par angle A par rapport à l’origine de l’espace de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="bbae5-112">The following algorithm computes the new x-coordinate (x ') for a point (x,y ) that is rotated by angle A with respect to the coordinate-space origin.</span></span>

``` syntax
x' = (x * cos A) - (y * sin A) 
```

<span data-ttu-id="bbae5-113">L’algorithme suivant calcule la coordonnée y (y) pour un point (x, y) qui est pivoté par l’angle A par rapport à l’origine.</span><span class="sxs-lookup"><span data-stu-id="bbae5-113">The following algorithm computes the y-coordinate (y ') for a point (x,y ) that is rotated by the angle A with respect to the origin.</span></span>

``` syntax
y' = (x * sin A) + (y * cos A) 
```

<span data-ttu-id="bbae5-114">Les deux transformations de rotation peuvent être combinées dans une matrice 2 par 2 comme suit.</span><span class="sxs-lookup"><span data-stu-id="bbae5-114">The two rotation transformations can be combined in a 2-by-2 matrix as follows.</span></span>

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

<span data-ttu-id="bbae5-115">La matrice 2-par-2 qui a produit la rotation contient les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bbae5-115">The 2-by-2 matrix that produced the rotation contains the following values.</span></span>

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a><span data-ttu-id="bbae5-116">Dérivation de l’algorithme de rotation</span><span class="sxs-lookup"><span data-stu-id="bbae5-116">Rotation Algorithm Derivation</span></span>

<span data-ttu-id="bbae5-117">Les algorithmes de rotation sont basés sur le niveau de l’addition de trigonométrie, indiquant que la fonction trigonométrique d’une somme de deux angles (a1 et a2) peut être exprimée en termes de fonctions trigonométriques des deux angles.</span><span class="sxs-lookup"><span data-stu-id="bbae5-117">Rotation algorithms are based on trigonometry's addition theorem stating that the trigonometric function of a sum of two angles (A1 and A2 ) can be expressed in terms of the trigonometric functions of the two angles.</span></span>

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

<span data-ttu-id="bbae5-118">L’illustration suivante montre un point p pivoté dans le sens inverse des aiguilles d’une montre vers une nouvelle position p.</span><span class="sxs-lookup"><span data-stu-id="bbae5-118">The following illustration shows a point p rotated counterclockwise to a new position p'.</span></span> <span data-ttu-id="bbae5-119">En outre, il affiche deux triangles formés par une ligne dessinée de l’origine de l’espace de coordonnées à chaque point et une ligne dessinée à partir de chaque point sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="bbae5-119">In addition, it shows two triangles formed by a line drawn from the coordinate-space origin to each point and a line drawn from each point through the x-axis.</span></span>

![Diagramme montrant l’origine, p et p et deux triangles](images/cstrn-12.png)

<span data-ttu-id="bbae5-121">À l’aide de trigonométriques, la coordonnée x du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le cosinus de a1.</span><span class="sxs-lookup"><span data-stu-id="bbae5-121">Using trigonometry, the x-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the cosine of A1.</span></span>

``` syntax
x = h * cos A1 
```

<span data-ttu-id="bbae5-122">La coordonnée y du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le sinus de a1.</span><span class="sxs-lookup"><span data-stu-id="bbae5-122">The y-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the sine of A1.</span></span>

``` syntax
y = h * sin A1 
```

<span data-ttu-id="bbae5-123">De même, la coordonnée x du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le cosinus de (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="bbae5-123">Likewise, the x-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the cosine of (A1 +A2 ).</span></span>

``` syntax
x' = h * cos (A1 + A2) 
```

<span data-ttu-id="bbae5-124">Enfin, la coordonnée y du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le sinus de (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="bbae5-124">Finally, the y-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the sine of (A1 +A2 ).</span></span>

``` syntax
y' = h * sin (A1 + A2) 
```

<span data-ttu-id="bbae5-125">À l’aide de l’ajout de l’ajout, les algorithmes précédents deviennent les suivants :</span><span class="sxs-lookup"><span data-stu-id="bbae5-125">Using the addition theorem, the preceding algorithms become the following:</span></span>

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

<span data-ttu-id="bbae5-126">Les algorithmes de rotation d’un point donné pivotés par angle a2 peuvent être obtenus en remplaçant x pour chaque occurrence de (h \* cos a1) et en remplaçant y par chaque occurrence de (h \* Sin a1).</span><span class="sxs-lookup"><span data-stu-id="bbae5-126">The rotation algorithms for a given point rotated by angle A2 can be obtained by substituting x for each occurrence of (h \* cos A1 ) and by substituting y for each occurrence of (h \* sin A1 ).</span></span>

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



