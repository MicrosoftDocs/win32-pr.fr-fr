---
description: Un rectangle est un polygone à quatre côtés dont les côtés opposés sont parallèles et de longueur égale.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Dessiner des rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863650"
---
# <a name="drawing-rectangles"></a><span data-ttu-id="dddc4-103">Dessiner des rectangles</span><span class="sxs-lookup"><span data-stu-id="dddc4-103">Drawing Rectangles</span></span>

<span data-ttu-id="dddc4-104">Un rectangle est un polygone à quatre côtés dont les côtés opposés sont parallèles et de longueur égale.</span><span class="sxs-lookup"><span data-stu-id="dddc4-104">A rectangle is a four-sided polygon whose opposing sides are parallel and equal in length.</span></span> <span data-ttu-id="dddc4-105">Bien qu’une application puisse dessiner un rectangle en appelant la fonction [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , en fournissant les coordonnées de chaque angle, la fonction [**rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) fournit une méthode plus simple.</span><span class="sxs-lookup"><span data-stu-id="dddc4-105">Although an application can draw a rectangle by calling the [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) function, supplying the coordinates of each corner, the [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) function provides a simpler method.</span></span> <span data-ttu-id="dddc4-106">Cette fonction ne requiert que les coordonnées des angles supérieur gauche et inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="dddc4-106">This function requires only the coordinates for the upper-left and the lower-right corners.</span></span> <span data-ttu-id="dddc4-107">Quand une application appelle la fonction [**rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , le système dessine le rectangle, à l’exclusion des côtés droits et inférieurs si aucune transformation universelle n’est définie pour le contexte de périphérique donné.</span><span class="sxs-lookup"><span data-stu-id="dddc4-107">When an application calls the [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) function, the system draws the rectangle, excluding the right and lower sides if no world transformation is set for the given device context.</span></span>

<span data-ttu-id="dddc4-108">Si une transformation universelle a été définie à l’aide de la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ou [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , le système inclut les bords droits et inférieurs.</span><span class="sxs-lookup"><span data-stu-id="dddc4-108">If a world transformation has been set by using the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower edges.</span></span>

<span data-ttu-id="dddc4-109">En plus de dessiner un rectangle traditionnel, vous pouvez dessiner des rectangles avec des angles arrondis.</span><span class="sxs-lookup"><span data-stu-id="dddc4-109">In addition to drawing a traditional rectangle, you can draw rectangles with rounded corners.</span></span> <span data-ttu-id="dddc4-110">La fonction [**roundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) nécessite que l’application fournisse les coordonnées des angles inférieur gauche et supérieur droit, ainsi que la largeur et la hauteur de l’ellipse utilisée pour arrondir chaque angle.</span><span class="sxs-lookup"><span data-stu-id="dddc4-110">The [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) function requires that the application supply the coordinates of the lower-left and upper-right corners, as well as the width and height of the ellipse used to round each corner.</span></span>

<span data-ttu-id="dddc4-111">Les applications peuvent utiliser les fonctions suivantes pour manipuler des rectangles.</span><span class="sxs-lookup"><span data-stu-id="dddc4-111">Applications can use the following functions to manipulate rectangles.</span></span>



| <span data-ttu-id="dddc4-112">Fonction</span><span class="sxs-lookup"><span data-stu-id="dddc4-112">Function</span></span>                         | <span data-ttu-id="dddc4-113">Description</span><span class="sxs-lookup"><span data-stu-id="dddc4-113">Description</span></span>                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="dddc4-114">**FillRect**</span><span class="sxs-lookup"><span data-stu-id="dddc4-114">**FillRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | <span data-ttu-id="dddc4-115">Repeint l’intérieur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="dddc4-115">Repaints the interior of a rectangle.</span></span>                              |
| [<span data-ttu-id="dddc4-116">**FrameRect**</span><span class="sxs-lookup"><span data-stu-id="dddc4-116">**FrameRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-framerect)   | <span data-ttu-id="dddc4-117">Redessine les côtés d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="dddc4-117">Redraws the sides of a rectangle.</span></span>                                  |
| [<span data-ttu-id="dddc4-118">**InvertRect**</span><span class="sxs-lookup"><span data-stu-id="dddc4-118">**InvertRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-invertrect) | <span data-ttu-id="dddc4-119">Inverse les couleurs qui apparaissent à l’intérieur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="dddc4-119">Inverts the colors that appear within the interior of a rectangle.</span></span> |



 

 

 
