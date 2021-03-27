---
description: Une application récupère les dimensions du rectangle englobant d’une région en appelant la fonction GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Récupération d’un rectangle englobant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754308"
---
# <a name="retrieving-a-bounding-rectangle"></a><span data-ttu-id="45161-103">Récupération d’un rectangle englobant</span><span class="sxs-lookup"><span data-stu-id="45161-103">Retrieving a Bounding Rectangle</span></span>

<span data-ttu-id="45161-104">Une application récupère les dimensions du rectangle englobant d’une région en appelant la fonction [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) .</span><span class="sxs-lookup"><span data-stu-id="45161-104">An application retrieves the dimensions of a region's bounding rectangle by calling the [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) function.</span></span> <span data-ttu-id="45161-105">Si la région est rectangulaire, **GetRgnBox** retourne les dimensions de la région.</span><span class="sxs-lookup"><span data-stu-id="45161-105">If the region is rectangular, **GetRgnBox** returns the dimensions of the region.</span></span> <span data-ttu-id="45161-106">Si la région est elliptique, la fonction retourne les dimensions du plus petit rectangle qui peut être dessiné autour de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="45161-106">If the region is elliptical, the function returns the dimensions of the smallest rectangle that can be drawn around the ellipse.</span></span> <span data-ttu-id="45161-107">Les longs côtés du rectangle sont de la même longueur que l’axe principal de l’ellipse, et les côtés courts du rectangle sont de la même longueur que l’axe secondaire de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="45161-107">The long sides of the rectangle are the same length as the ellipse's major axis, and the short sides of the rectangle are the same length as the ellipse's minor axis.</span></span> <span data-ttu-id="45161-108">Si la région est polygonale, **GetRgnBox** retourne les dimensions du plus petit rectangle qui peut être dessiné autour du polygone entier.</span><span class="sxs-lookup"><span data-stu-id="45161-108">If the region is polygonal, **GetRgnBox** returns the dimensions of the smallest rectangle that can be drawn around the entire polygon.</span></span>

 

 



