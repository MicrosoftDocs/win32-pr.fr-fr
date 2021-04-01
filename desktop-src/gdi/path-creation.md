---
description: Pour créer un chemin d’accès et le sélectionner dans un DC, vous devez d’abord définir les points qui le décrivent.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Création du chemin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202022"
---
# <a name="path-creation"></a><span data-ttu-id="9035c-103">Création du chemin</span><span class="sxs-lookup"><span data-stu-id="9035c-103">Path Creation</span></span>

<span data-ttu-id="9035c-104">Pour créer un chemin d’accès et le sélectionner dans un DC, vous devez d’abord définir les points qui le décrivent.</span><span class="sxs-lookup"><span data-stu-id="9035c-104">To create a path and select it into a DC, it is first necessary to define the points that describe it.</span></span> <span data-ttu-id="9035c-105">Pour ce faire, appelez la fonction [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , en spécifiant les fonctions de dessin appropriées, puis en appelant la fonction [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="9035c-105">This is done by calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function, specifying the appropriate drawing functions, and then by calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="9035c-106">Cette combinaison de fonctions (**BeginPath**, Drawing Functions et **EndPath**) constitue un *crochet de chemin*.</span><span class="sxs-lookup"><span data-stu-id="9035c-106">This combination of functions (**BeginPath**, drawing functions, and **EndPath**) constitute a *path bracket*.</span></span> <span data-ttu-id="9035c-107">La liste suivante répertorie les fonctions de dessin qui peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="9035c-107">The following is the list of drawing functions that can be used.</span></span>

-   [<span data-ttu-id="9035c-108">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="9035c-108">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [<span data-ttu-id="9035c-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="9035c-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [<span data-ttu-id="9035c-110">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="9035c-110">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [<span data-ttu-id="9035c-111">**Chord**</span><span class="sxs-lookup"><span data-stu-id="9035c-111">**Chord**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [<span data-ttu-id="9035c-112">**CloseFigure**</span><span class="sxs-lookup"><span data-stu-id="9035c-112">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [<span data-ttu-id="9035c-113">**Ellipse**</span><span class="sxs-lookup"><span data-stu-id="9035c-113">**Ellipse**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [<span data-ttu-id="9035c-114">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="9035c-114">**ExtTextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="9035c-115">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="9035c-115">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [<span data-ttu-id="9035c-116">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="9035c-116">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [<span data-ttu-id="9035c-117">**Secteurs**</span><span class="sxs-lookup"><span data-stu-id="9035c-117">**Pie**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [<span data-ttu-id="9035c-118">**Polybézier**</span><span class="sxs-lookup"><span data-stu-id="9035c-118">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [<span data-ttu-id="9035c-119">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="9035c-119">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [<span data-ttu-id="9035c-120">**Polydraw**</span><span class="sxs-lookup"><span data-stu-id="9035c-120">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [<span data-ttu-id="9035c-121">**Polygone**</span><span class="sxs-lookup"><span data-stu-id="9035c-121">**Polygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [<span data-ttu-id="9035c-122">**Polyligne**</span><span class="sxs-lookup"><span data-stu-id="9035c-122">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [<span data-ttu-id="9035c-123">**PolylineTo**</span><span class="sxs-lookup"><span data-stu-id="9035c-123">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [<span data-ttu-id="9035c-124">**Polypolygone**</span><span class="sxs-lookup"><span data-stu-id="9035c-124">**PolyPolygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [<span data-ttu-id="9035c-125">**Polyligne**</span><span class="sxs-lookup"><span data-stu-id="9035c-125">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [<span data-ttu-id="9035c-126">**Rectangle**</span><span class="sxs-lookup"><span data-stu-id="9035c-126">**Rectangle**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [<span data-ttu-id="9035c-127">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="9035c-127">**RoundRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [<span data-ttu-id="9035c-128">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="9035c-128">**TextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="9035c-129">Quand une application appelle [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), le système sélectionne le chemin d’accès associé dans le contrôleur de réseau spécifié.</span><span class="sxs-lookup"><span data-stu-id="9035c-129">When an application calls [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), the system selects the associated path into the specified DC.</span></span> <span data-ttu-id="9035c-130">(Si un autre chemin avait déjà été sélectionné dans le contrôleur de réseau, le système supprime ce chemin sans l’enregistrer.) Une fois que le système a sélectionné le chemin d’accès dans le contrôleur de réseau, une application peut fonctionner sur le chemin d’accès de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="9035c-130">(If another path had previously been selected into the DC, the system deletes that path without saving it.) After the system selects the path into the DC, an application can operate on the path in one of the following ways:</span></span>

-   <span data-ttu-id="9035c-131">Dessine le contour du tracé (à l’aide du stylet actuel).</span><span class="sxs-lookup"><span data-stu-id="9035c-131">Draw the outline of the path (using the current pen).</span></span>
-   <span data-ttu-id="9035c-132">Peindre l’intérieur du tracé (à l’aide du pinceau actuel).</span><span class="sxs-lookup"><span data-stu-id="9035c-132">Paint the interior of the path (using the current brush).</span></span>
-   <span data-ttu-id="9035c-133">Dessinez le contour et remplissez l’intérieur du tracé.</span><span class="sxs-lookup"><span data-stu-id="9035c-133">Draw the outline and fill the interior of the path.</span></span>
-   <span data-ttu-id="9035c-134">Modifiez le chemin d’accès (en convertissant les courbes en segments de ligne).</span><span class="sxs-lookup"><span data-stu-id="9035c-134">Modify the path (converting curves to line segments).</span></span>
-   <span data-ttu-id="9035c-135">Convertit le tracé en tracé de clip.</span><span class="sxs-lookup"><span data-stu-id="9035c-135">Convert the path into a clip path.</span></span>
-   <span data-ttu-id="9035c-136">Convertit le tracé en une région.</span><span class="sxs-lookup"><span data-stu-id="9035c-136">Convert the path into a region.</span></span>
-   <span data-ttu-id="9035c-137">Aplatir le tracé en convertissant chaque courbe du tracé en une série de segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="9035c-137">Flatten the path by converting each curve in the path into a series of line segments.</span></span>
-   <span data-ttu-id="9035c-138">Récupérez les coordonnées des lignes et des courbes qui composent un tracé.</span><span class="sxs-lookup"><span data-stu-id="9035c-138">Retrieve the coordinates of the lines and curves that compose a path.</span></span>

 

 



