---
description: Certaines applications traduisent (ou décalent) des objets dessinés dans la zone cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traduction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987777"
---
# <a name="translation"></a><span data-ttu-id="3b045-103">Traduction</span><span class="sxs-lookup"><span data-stu-id="3b045-103">Translation</span></span>

<span data-ttu-id="3b045-104">Certaines applications traduisent (ou décalent) des objets dessinés dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="3b045-104">Some applications translate (or shift) objects drawn in the client area.</span></span> <span data-ttu-id="3b045-105">en appelant la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir l’espace universel approprié sur la transformation d’espace de page.</span><span class="sxs-lookup"><span data-stu-id="3b045-105">by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="3b045-106">La fonction SetWorldTransform reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="3b045-106">The SetWorldTransform function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="3b045-107">Les membres eDx et eDy de XFORM spécifient respectivement les composants de traduction horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="3b045-107">The eDx and eDy members of XFORM specify the horizontal and vertical translation components, respectively.</span></span>

<span data-ttu-id="3b045-108">En cas de *traduction* , chaque point d’un objet est décalé verticalement, horizontalement, ou les deux, selon une valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3b045-108">When *translation* occurs, each point in an object is shifted vertically, horizontally, or both, by a specified amount.</span></span> <span data-ttu-id="3b045-109">L’illustration suivante montre un rectangle de 20 par 20 qui a été traduit à droite de 10 unités lorsqu’il est copié à partir d’un espace de coordonnées universelles vers l’espace de coordonnées de page.</span><span class="sxs-lookup"><span data-stu-id="3b045-109">The following illustration shows a 20- by 20-unit rectangle that was translated to the right by 10 units when copied from world-coordinate space to page-coordinate space.</span></span>

![Illustration montrant un rectangle à une position dans l’espace universel et à une autre position dans l’espace de la page](images/cstrn-09.png)

<span data-ttu-id="3b045-111">Dans l’illustration précédente, la coordonnée x de chaque point du rectangle est égale à 10 unités supérieures à la coordonnée x d’origine.</span><span class="sxs-lookup"><span data-stu-id="3b045-111">In the preceding illustration, the x-coordinate of each point in the rectangle is 10 units greater than the original x-coordinate.</span></span>

<span data-ttu-id="3b045-112">La traduction horizontale peut être représentée par l’algorithme suivant.</span><span class="sxs-lookup"><span data-stu-id="3b045-112">Horizontal translation can be represented by the following algorithm.</span></span>

``` syntax
x' = x + Dx 
```

<span data-ttu-id="3b045-113">Où x correspond à la nouvelle coordonnée x, x correspond à la coordonnée x d’origine et DX à la distance horizontale déplacée.</span><span class="sxs-lookup"><span data-stu-id="3b045-113">Where x' is the new x-coordinate, x is the original x-coordinate, and Dx is the horizontal distance moved.</span></span>

<span data-ttu-id="3b045-114">La traduction verticale peut être représentée par l’algorithme suivant.</span><span class="sxs-lookup"><span data-stu-id="3b045-114">Vertical translation can be represented by the following algorithm.</span></span>

``` syntax
y' = y + Dy 
```

<span data-ttu-id="3b045-115">Où y est la nouvelle coordonnée y, y est la coordonnée y d’origine et dy la distance verticale déplacée.</span><span class="sxs-lookup"><span data-stu-id="3b045-115">Where y' is the new y-coordinate, y is the original y-coordinate, and Dy is the vertical distance moved.</span></span>

<span data-ttu-id="3b045-116">Les transformations de translation horizontale et verticale peuvent être combinées en une seule opération à l’aide d’une matrice 3 par 3.</span><span class="sxs-lookup"><span data-stu-id="3b045-116">The horizontal and vertical translation transformations can be combined into a single operation by using a 3-by-3 matrix.</span></span>

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

<span data-ttu-id="3b045-117">(Règles d’état de la multiplication de matrice selon lesquelles le nombre de lignes dans une matrice doit être égal au nombre de colonnes dans l’autre.</span><span class="sxs-lookup"><span data-stu-id="3b045-117">(The rules of matrix multiplication state that the number of rows in one matrix must equal the number of columns in the other.</span></span> <span data-ttu-id="3b045-118">L’entier 1 dans la matrice \| x y 1 \| est un espace réservé qui a été ajouté pour répondre à cette exigence.)</span><span class="sxs-lookup"><span data-stu-id="3b045-118">The integer 1 in the matrix \|x y 1\| is a placeholder that was added to meet this requirement.)</span></span>

<span data-ttu-id="3b045-119">La matrice 3-par-3 qui a produit la transformation de traduction illustrée contient les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b045-119">The 3-by-3 matrix that produced the illustrated translation transformation contains the following values.</span></span>

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



