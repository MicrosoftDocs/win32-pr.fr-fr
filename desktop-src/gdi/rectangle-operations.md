---
description: La fonction SetRect crée un rectangle, la fonction CopyRect effectue une copie d’un rectangle donné et la fonction SetRectEmpty crée un rectangle vide.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Opérations de rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318833"
---
# <a name="rectangle-operations"></a><span data-ttu-id="094d1-103">Opérations de rectangle</span><span class="sxs-lookup"><span data-stu-id="094d1-103">Rectangle Operations</span></span>

<span data-ttu-id="094d1-104">La fonction [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crée un rectangle, la fonction [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) effectue une copie d’un rectangle donné et la fonction [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crée un rectangle vide.</span><span class="sxs-lookup"><span data-stu-id="094d1-104">The [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) function creates a rectangle, the [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) function makes a copy of a given rectangle, and the [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) function creates an empty rectangle.</span></span> <span data-ttu-id="094d1-105">Un rectangle vide est un rectangle qui a une largeur égale à zéro, une hauteur de zéro, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="094d1-105">An empty rectangle is any rectangle that has zero width, zero height, or both.</span></span> <span data-ttu-id="094d1-106">La fonction [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) détermine si un rectangle donné est vide.</span><span class="sxs-lookup"><span data-stu-id="094d1-106">The [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) function determines whether a given rectangle is empty.</span></span> <span data-ttu-id="094d1-107">La fonction [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) détermine si deux rectangles sont identiques, c’est-à-dire s’ils ont les mêmes coordonnées.</span><span class="sxs-lookup"><span data-stu-id="094d1-107">The [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) function determines whether two rectangles are identical that is, whether they have the same coordinates.</span></span>

<span data-ttu-id="094d1-108">La fonction [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) augmente ou diminue la largeur ou la hauteur d’un rectangle, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="094d1-108">The [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) function increases or decreases the width or height of a rectangle, or both.</span></span> <span data-ttu-id="094d1-109">Elle peut ajouter ou supprimer la largeur des deux extrémités du rectangle ; elle peut ajouter ou supprimer la hauteur à la fois du haut et du bas du rectangle.</span><span class="sxs-lookup"><span data-stu-id="094d1-109">It can add or remove width from both ends of the rectangle; it can add or remove height from both the top and bottom of the rectangle.</span></span>

<span data-ttu-id="094d1-110">La fonction [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) déplace un rectangle d’une quantité donnée.</span><span class="sxs-lookup"><span data-stu-id="094d1-110">The [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) function moves a rectangle by a given amount.</span></span> <span data-ttu-id="094d1-111">Il déplace le rectangle en ajoutant les valeurs x-amount, y-volume ou x et y indiquées aux coordonnées d’angle.</span><span class="sxs-lookup"><span data-stu-id="094d1-111">It moves the rectangle by adding the given x-amount, y-amount, or x- and y-amounts to the corner coordinates.</span></span>

<span data-ttu-id="094d1-112">La fonction [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) détermine si un point donné se trouve dans un rectangle donné.</span><span class="sxs-lookup"><span data-stu-id="094d1-112">The [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) function determines whether a given point lies within a given rectangle.</span></span> <span data-ttu-id="094d1-113">Le point se trouve dans le rectangle s’il se trouve sur le côté gauche ou supérieur ou s’il est entièrement dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="094d1-113">The point is in the rectangle if it lies on the left or top side or is completely within the rectangle.</span></span> <span data-ttu-id="094d1-114">Le point n’est pas dans le rectangle s’il se trouve sur le côté droit ou inférieur.</span><span class="sxs-lookup"><span data-stu-id="094d1-114">The point is not in the rectangle if it lies on the right or bottom side.</span></span>

<span data-ttu-id="094d1-115">La fonction [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crée un nouveau rectangle qui est l’intersection de deux rectangles existants, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="094d1-115">The [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) function creates a new rectangle that is the intersection of two existing rectangles, as shown in the following figure.</span></span>

![<span data-ttu-id="094d1-116">Illustration montrant deux rectangles qui se chevauchent, avec un ombrage plus sombre pour indiquer l’intersection</span><span class="sxs-lookup"><span data-stu-id="094d1-116">illustration showing two overlapping rectangles, with darker shading to indicate the intersection</span></span> ](images/csrec-01.png)

<span data-ttu-id="094d1-117">La fonction [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crée un nouveau rectangle qui est l’Union de deux rectangles existants, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="094d1-117">The [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) function creates a new rectangle that is the union of two existing rectangles, as shown in the following figure.</span></span>

![illustration de deux rectangles qui se chevauchent, avec un ombrage plus sombre indiquant les zones de l’Union, mais pas dans les deux rectangles](images/csrec-02.png)

<span data-ttu-id="094d1-119">Pour plus d’informations sur les fonctions qui dessinent des ellipses et des polygones, consultez [remplissage de formes](filled-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="094d1-119">For information about functions that draw ellipses and polygons, see [Filled Shapes](filled-shapes.md).</span></span>

 

 



