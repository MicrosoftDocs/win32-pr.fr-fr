---
description: La plupart des applications de CAO et de dessin fournissent des fonctionnalités qui permettent de mettre à l’échelle la sortie créée par l’utilisateur.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Mise à l'échelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973523"
---
# <a name="scaling"></a><span data-ttu-id="1c864-103">Mise à l'échelle</span><span class="sxs-lookup"><span data-stu-id="1c864-103">Scaling</span></span>

<span data-ttu-id="1c864-104">La plupart des applications de CAO et de dessin fournissent des fonctionnalités qui permettent de mettre à l’échelle la sortie créée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c864-104">Most CAD and drawing applications provide features that scale output created by the user.</span></span> <span data-ttu-id="1c864-105">Les applications qui incluent des fonctionnalités de mise à l’échelle (ou zoom) appellent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir l’espace universel approprié sur la transformation d’espace de page.</span><span class="sxs-lookup"><span data-stu-id="1c864-105">Applications that include scaling (or zoom) capabilities call the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="1c864-106">Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="1c864-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="1c864-107">Les membres eM11 et eM22 de XFORM spécifient respectivement les composants de mise à l’échelle horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="1c864-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical scaling components, respectively.</span></span>

<span data-ttu-id="1c864-108">Lorsque la *mise à l’échelle* se produit, les lignes verticales et horizontales (ou les vecteurs) qui constituent un objet sont étirées ou compressées par rapport à l’axe x ou y.</span><span class="sxs-lookup"><span data-stu-id="1c864-108">When *scaling* occurs, the vertical and horizontal lines (or vectors), that constitute an object, are stretched or compressed with respect to the x- or y-axis.</span></span> <span data-ttu-id="1c864-109">L’illustration suivante montre un rectangle de 20 par 20 mis à l’échelle verticalement jusqu’à deux fois sa hauteur d’origine lorsqu’il est copié à partir d’un espace de coordonnées universelles vers l’espace de coordonnées de page.</span><span class="sxs-lookup"><span data-stu-id="1c864-109">The following illustration shows a 20-by-20-unit rectangle scaled vertically to twice its original height when copied from world-coordinate space to page-coordinate space.</span></span>

![Illustration montrant un petit rectangle dans l’espace universel et un plus haut dans l’espace de la page](images/cstrn-10.png)

<span data-ttu-id="1c864-111">Dans l’illustration précédente, les lignes verticales qui définissent la mesure latérale du rectangle d’origine sont 20 unités, tandis que les lignes verticales qui définissent les côtés du rectangle mis à l’échelle mesurent 40 unités.</span><span class="sxs-lookup"><span data-stu-id="1c864-111">In the preceding illustration, the vertical lines that define the original rectangle's side measure 20 units, while the vertical lines that define the scaled rectangle's sides measure 40 units.</span></span>

<span data-ttu-id="1c864-112">La mise à l’échelle verticale peut être représentée par l’algorithme suivant.</span><span class="sxs-lookup"><span data-stu-id="1c864-112">Vertical scaling can be represented by the following algorithm.</span></span>

``` syntax
y' = y * Dy 
```

<span data-ttu-id="1c864-113">Où y est la nouvelle longueur, y est la longueur d’origine et dy est le facteur d’échelle verticale.</span><span class="sxs-lookup"><span data-stu-id="1c864-113">Where y' is the new length, y is the original length, and Dy is the vertical scaling factor.</span></span>

<span data-ttu-id="1c864-114">La mise à l’échelle horizontale peut être représentée par l’algorithme suivant.</span><span class="sxs-lookup"><span data-stu-id="1c864-114">Horizontal scaling can be represented by the following algorithm.</span></span>

``` syntax
x' = x * Dx 
```

<span data-ttu-id="1c864-115">Où x est la nouvelle longueur, x est la longueur d’origine et DX le facteur de mise à l’échelle horizontale.</span><span class="sxs-lookup"><span data-stu-id="1c864-115">Where x' is the new length, x is the original length, and Dx is the horizontal scaling factor.</span></span>

<span data-ttu-id="1c864-116">Les transformations de mise à l’échelle verticale et horizontale peuvent être combinées en une seule opération à l’aide d’une matrice 2 par 2.</span><span class="sxs-lookup"><span data-stu-id="1c864-116">The vertical and horizontal scaling transformations can be combined into a single operation by using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

<span data-ttu-id="1c864-117">La matrice 2-par-2 qui a produit la transformation de mise à l’échelle contient les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1c864-117">The 2-by-2 matrix that produced the scaling transformation contains the following values.</span></span>

``` syntax
|1    0| 
|0    2| 
```

 

 



