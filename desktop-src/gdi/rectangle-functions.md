---
description: Les fonctions suivantes sont utilisées avec des rectangles.
ms.assetid: b03da8c9-ee6d-4045-8d90-8beceb09ead5
title: Fonctions rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5c72812363185217e5cf30ae88447f82edc42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202014"
---
# <a name="rectangle-functions"></a><span data-ttu-id="720a4-103">Fonctions rectangle</span><span class="sxs-lookup"><span data-stu-id="720a4-103">Rectangle Functions</span></span>

<span data-ttu-id="720a4-104">Les fonctions suivantes sont utilisées avec des rectangles.</span><span class="sxs-lookup"><span data-stu-id="720a4-104">The following functions are used with rectangles.</span></span>



| <span data-ttu-id="720a4-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="720a4-105">Function</span></span>                               | <span data-ttu-id="720a4-106">Description</span><span class="sxs-lookup"><span data-stu-id="720a4-106">Description</span></span>                                                                                                                                   |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="720a4-107">**CopyRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-107">**CopyRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyrect)           | <span data-ttu-id="720a4-108">Copie les coordonnées d’un rectangle dans un autre.</span><span class="sxs-lookup"><span data-stu-id="720a4-108">Copies the coordinates of one rectangle to another.</span></span>                                                                                           |
| [<span data-ttu-id="720a4-109">**EqualRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-109">**EqualRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-equalrect)         | <span data-ttu-id="720a4-110">Détermine si les deux rectangles spécifiés sont égaux en comparant les coordonnées des angles supérieur gauche et inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="720a4-110">Determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.</span></span>           |
| [<span data-ttu-id="720a4-111">**InflateRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-111">**InflateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-inflaterect)     | <span data-ttu-id="720a4-112">Augmente ou diminue la largeur et la hauteur du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="720a4-112">Increases or decreases the width and height of the specified rectangle.</span></span>                                                                       |
| [<span data-ttu-id="720a4-113">**IntersectRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-113">**IntersectRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-intersectrect) | <span data-ttu-id="720a4-114">Calcule l’intersection de deux rectangles sources et place les coordonnées du rectangle d’intersection dans le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="720a4-114">Calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.</span></span> |
| [<span data-ttu-id="720a4-115">**IsRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="720a4-115">**IsRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isrectempty)     | <span data-ttu-id="720a4-116">Détermine si le rectangle spécifié est vide.</span><span class="sxs-lookup"><span data-stu-id="720a4-116">Determines whether the specified rectangle is empty.</span></span>                                                                                          |
| [<span data-ttu-id="720a4-117">**OffsetRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-117">**OffsetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-offsetrect)       | <span data-ttu-id="720a4-118">Déplace le rectangle spécifié selon les décalages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="720a4-118">Moves the specified rectangle by the specified offsets.</span></span>                                                                                       |
| [<span data-ttu-id="720a4-119">**PtInRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-119">**PtInRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ptinrect)           | <span data-ttu-id="720a4-120">Détermine si le point spécifié se trouve dans le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="720a4-120">Determines whether the specified point lies within the specified rectangle.</span></span>                                                                   |
| [<span data-ttu-id="720a4-121">**SetRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-121">**SetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrect)             | <span data-ttu-id="720a4-122">Définit les coordonnées du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="720a4-122">Sets the coordinates of the specified rectangle.</span></span>                                                                                              |
| [<span data-ttu-id="720a4-123">**SetRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="720a4-123">**SetRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrectempty)   | <span data-ttu-id="720a4-124">Crée un rectangle vide dans lequel toutes les coordonnées sont définies à zéro.</span><span class="sxs-lookup"><span data-stu-id="720a4-124">Creates an empty rectangle in which all coordinates are set to zero.</span></span>                                                                          |
| [<span data-ttu-id="720a4-125">**SubtractRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-125">**SubtractRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-subtractrect)   | <span data-ttu-id="720a4-126">Détermine les coordonnées d’un rectangle formé en soustrayant un rectangle d’un autre.</span><span class="sxs-lookup"><span data-stu-id="720a4-126">Determines the coordinates of a rectangle formed by subtracting one rectangle from another.</span></span>                                                   |
| [<span data-ttu-id="720a4-127">**UnionRect**</span><span class="sxs-lookup"><span data-stu-id="720a4-127">**UnionRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unionrect)         | <span data-ttu-id="720a4-128">Crée l’Union de deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="720a4-128">Creates the union of two rectangles.</span></span>                                                                                                          |



 

 

 



