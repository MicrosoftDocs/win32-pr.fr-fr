---
description: Une application doit utiliser une structure RECT pour définir un rectangle.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordonnées des rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991173"
---
# <a name="rectangle-coordinates"></a><span data-ttu-id="e2ce1-103">Coordonnées des rectangles</span><span class="sxs-lookup"><span data-stu-id="e2ce1-103">Rectangle Coordinates</span></span>

<span data-ttu-id="e2ce1-104">Une application doit utiliser une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour définir un rectangle.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-104">An application must use a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to define a rectangle.</span></span> <span data-ttu-id="e2ce1-105">La structure spécifie les coordonnées de deux points : les angles supérieur gauche et inférieur droit du rectangle.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-105">The structure specifies the coordinates of two points: the upper left and lower right corners of the rectangle.</span></span> <span data-ttu-id="e2ce1-106">Les côtés du rectangle s’étendent à partir de ces deux points et sont parallèles aux axes x et y.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-106">The sides of the rectangle extend from these two points and are parallel to the x-axis and y-axis.</span></span>

<span data-ttu-id="e2ce1-107">Les valeurs de coordonnée d’un rectangle sont exprimées en tant qu’entiers signés.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-107">The coordinate values for a rectangle are expressed as signed integers.</span></span> <span data-ttu-id="e2ce1-108">La valeur de coordonnée du côté droit d’un rectangle doit être supérieure à celle du côté gauche.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-108">The coordinate value of a rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="e2ce1-109">De même, la valeur de coordonnée du bas doit être supérieure à celle du haut.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-109">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

<span data-ttu-id="e2ce1-110">Étant donné que les applications peuvent utiliser des rectangles à de nombreuses fins différentes, les fonctions rectangle n’utilisent pas d’unité de mesure explicite.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-110">Because applications can use rectangles for many different purposes, the rectangle functions do not use an explicit unit of measure.</span></span> <span data-ttu-id="e2ce1-111">Au lieu de cela, toutes les coordonnées et les dimensions des rectangles sont indiquées dans des valeurs logiques signées.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-111">Instead, all rectangle coordinates and dimensions are given in signed, logical values.</span></span> <span data-ttu-id="e2ce1-112">Le mode de mappage et la fonction dans laquelle le rectangle est utilisé déterminent les unités de mesure.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-112">The mapping mode and the function in which the rectangle is used determine the units of measure.</span></span> <span data-ttu-id="e2ce1-113">Pour plus d’informations sur les coordonnées et les modes de mappage, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="e2ce1-113">For more information about coordinates and mapping modes, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

 
