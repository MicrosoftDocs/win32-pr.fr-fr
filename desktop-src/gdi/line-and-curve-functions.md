---
description: Les fonctions suivantes sont utilisées avec les lignes et les courbes.
ms.assetid: 90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b
title: Fonctions de ligne et de courbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bf04160e8b9cc0a5c2fb28378bce82a1c7650a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991196"
---
# <a name="line-and-curve-functions"></a><span data-ttu-id="0be58-103">Fonctions de ligne et de courbe</span><span class="sxs-lookup"><span data-stu-id="0be58-103">Line and Curve Functions</span></span>

<span data-ttu-id="0be58-104">Les fonctions suivantes sont utilisées avec les lignes et les courbes.</span><span class="sxs-lookup"><span data-stu-id="0be58-104">The following functions are used with lines and curves.</span></span>



| <span data-ttu-id="0be58-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="0be58-105">Function</span></span>                                   | <span data-ttu-id="0be58-106">Description</span><span class="sxs-lookup"><span data-stu-id="0be58-106">Description</span></span>                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0be58-107">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="0be58-107">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)               | <span data-ttu-id="0be58-108">Dessine un segment de ligne et un arc.</span><span class="sxs-lookup"><span data-stu-id="0be58-108">Draws a line segment and an arc.</span></span>                                                                              |
| [<span data-ttu-id="0be58-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="0be58-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)                         | <span data-ttu-id="0be58-110">Dessine un arc elliptique.</span><span class="sxs-lookup"><span data-stu-id="0be58-110">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="0be58-111">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="0be58-111">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)                     | <span data-ttu-id="0be58-112">Dessine un arc elliptique.</span><span class="sxs-lookup"><span data-stu-id="0be58-112">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="0be58-113">**GetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="0be58-113">**GetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) | <span data-ttu-id="0be58-114">Récupère la direction d’arc actuelle pour le contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="0be58-114">Retrieves the current arc direction for the specified device context.</span></span>                                         |
| [<span data-ttu-id="0be58-115">**LineDDA**</span><span class="sxs-lookup"><span data-stu-id="0be58-115">**LineDDA**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-linedda)                 | <span data-ttu-id="0be58-116">Détermine les pixels à mettre en surbrillance pour une ligne définie par les points de départ et de fin spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0be58-116">Determines which pixels should be highlighted for a line defined by the specified starting and ending points.</span></span> |
| [<span data-ttu-id="0be58-117">**LineDDAProc**</span><span class="sxs-lookup"><span data-stu-id="0be58-117">**LineDDAProc**</span></span>](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)         | <span data-ttu-id="0be58-118">Fonction de rappel définie par l’application utilisée avec la fonction LineDDA.</span><span class="sxs-lookup"><span data-stu-id="0be58-118">An application-defined callback function used with the LineDDA function.</span></span>                                      |
| [<span data-ttu-id="0be58-119">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="0be58-119">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)                   | <span data-ttu-id="0be58-120">Dessine une ligne à partir de la position actuelle jusqu’au point spécifié, mais sans l’inclure.</span><span class="sxs-lookup"><span data-stu-id="0be58-120">Draws a line from the current position up to, but not including, the specified point.</span></span>                         |
| [<span data-ttu-id="0be58-121">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="0be58-121">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)               | <span data-ttu-id="0be58-122">Met à jour la position actuelle au point spécifié et retourne éventuellement la position précédente.</span><span class="sxs-lookup"><span data-stu-id="0be58-122">Updates the current position to the specified point and optionally returns the previous position.</span></span>             |
| [<span data-ttu-id="0be58-123">**Polybézier**</span><span class="sxs-lookup"><span data-stu-id="0be58-123">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)           | <span data-ttu-id="0be58-124">Dessine une ou plusieurs courbes de Bézier.</span><span class="sxs-lookup"><span data-stu-id="0be58-124">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="0be58-125">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="0be58-125">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)       | <span data-ttu-id="0be58-126">Dessine une ou plusieurs courbes de Bézier.</span><span class="sxs-lookup"><span data-stu-id="0be58-126">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="0be58-127">**Polydraw**</span><span class="sxs-lookup"><span data-stu-id="0be58-127">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)               | <span data-ttu-id="0be58-128">Dessine un ensemble de segments de ligne et de courbes de Bézier.</span><span class="sxs-lookup"><span data-stu-id="0be58-128">Draws a set of line segments and Bézier curves.</span></span>                                                               |
| [<span data-ttu-id="0be58-129">**Polyligne**</span><span class="sxs-lookup"><span data-stu-id="0be58-129">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)               | <span data-ttu-id="0be58-130">Dessine une série de segments de ligne en connectant les points du tableau spécifié.</span><span class="sxs-lookup"><span data-stu-id="0be58-130">Draws a series of line segments by connecting the points in the specified array.</span></span>                              |
| [<span data-ttu-id="0be58-131">**PolylineTo**</span><span class="sxs-lookup"><span data-stu-id="0be58-131">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)           | <span data-ttu-id="0be58-132">Dessine une ou plusieurs lignes droites.</span><span class="sxs-lookup"><span data-stu-id="0be58-132">Draws one or more straight lines.</span></span>                                                                             |
| [<span data-ttu-id="0be58-133">**Polyligne**</span><span class="sxs-lookup"><span data-stu-id="0be58-133">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)       | <span data-ttu-id="0be58-134">Dessine plusieurs séries de segments de ligne connectés.</span><span class="sxs-lookup"><span data-stu-id="0be58-134">Draws multiple series of connected line segments.</span></span>                                                             |
| [<span data-ttu-id="0be58-135">**SetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="0be58-135">**SetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) | <span data-ttu-id="0be58-136">Définit la direction de dessin à utiliser pour les fonctions d’arc et de rectangle.</span><span class="sxs-lookup"><span data-stu-id="0be58-136">Sets the drawing direction to be used for arc and rectangle functions.</span></span>                                        |



 

 

 



