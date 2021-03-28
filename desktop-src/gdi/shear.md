---
description: Certaines applications fournissent des fonctionnalités qui déforment les objets dessinés dans la zone cliente.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Incliné
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203885"
---
# <a name="shear"></a><span data-ttu-id="4ce91-103">Incliné</span><span class="sxs-lookup"><span data-stu-id="4ce91-103">Shear</span></span>

<span data-ttu-id="4ce91-104">Certaines applications fournissent des fonctionnalités qui déforment les objets dessinés dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="4ce91-104">Some applications provide features that shear objects drawn in the client area.</span></span> <span data-ttu-id="4ce91-105">Les applications qui utilisent les fonctionnalités de cisaillement utilisent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir les valeurs appropriées dans l’espace universel pour la transformation d’espace de page.</span><span class="sxs-lookup"><span data-stu-id="4ce91-105">Applications that use shear capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="4ce91-106">Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="4ce91-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="4ce91-107">Les membres eM12 et eM21 de XFORM spécifient respectivement les constantes de proportionnalité horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="4ce91-107">The eM12 and eM21 members of XFORM specify the horizontal and vertical proportionality constants, respectively.</span></span>

<span data-ttu-id="4ce91-108">Il existe deux composants de la *transformation d’inclinaison*.</span><span class="sxs-lookup"><span data-stu-id="4ce91-108">There are two components of the *shear transformation*.</span></span> <span data-ttu-id="4ce91-109">La première modifie les lignes verticales dans un objet. la seconde modifie les lignes horizontales.</span><span class="sxs-lookup"><span data-stu-id="4ce91-109">The first alters the vertical lines in an object; the second alters the horizontal lines.</span></span> <span data-ttu-id="4ce91-110">L’illustration suivante montre un rectangle 20 par 20 déformé horizontalement lorsqu’il est copié de l’espace universel vers l’espace de page.</span><span class="sxs-lookup"><span data-stu-id="4ce91-110">The following illustration shows a 20-by-20-unit rectangle sheared horizontally when copied from world space to page space.</span></span>

![Illustration montrant un rectangle dans l’espace universel et un trapeziod dans l’espace de la page](images/cstrn-13.png)

<span data-ttu-id="4ce91-112">Un cisaillement horizontal peut être représenté par l’algorithme suivant :</span><span class="sxs-lookup"><span data-stu-id="4ce91-112">A horizontal shear can be represented by the following algorithm:</span></span>

``` syntax
x' = x + (Sx * y) 
```

<span data-ttu-id="4ce91-113">où x est la coordonnée d’origine x, SX est la constante de proportionnalité et x’est le résultat de la transformation d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="4ce91-113">where x is the original x-coordinate, Sx is the proportionality constant, and x' is the result of the shear transformation.</span></span>

<span data-ttu-id="4ce91-114">Une inclinaison verticale peut être représentée par l’algorithme suivant :</span><span class="sxs-lookup"><span data-stu-id="4ce91-114">A vertical shear can be represented by the following algorithm:</span></span>

``` syntax
y' = y + (Sy * x) 
```

<span data-ttu-id="4ce91-115">où y est la coordonnée y d’origine, SY est la constante de proportionnalité et y est le résultat de la transformation d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="4ce91-115">where y is the original y-coordinate, Sy is the proportionality constant, and y' is the result of the shear transformation.</span></span>

<span data-ttu-id="4ce91-116">Les transformations d’inclinaison horizontale et verticale peuvent être combinées en une seule opération à l’aide d’une matrice 2 par 2.</span><span class="sxs-lookup"><span data-stu-id="4ce91-116">The horizontal-shear and vertical-shear transformations can be combined into a single operation using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

<span data-ttu-id="4ce91-117">La matrice 2-par-2 qui a produit l’inclinaison contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ce91-117">The 2-by-2 matrix that produced the shear contains the following values:</span></span>

``` syntax
|1    1| 
|0    1| 
```

 

 



