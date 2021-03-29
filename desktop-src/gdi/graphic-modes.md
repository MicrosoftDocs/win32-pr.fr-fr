---
description: Windows prend en charge cinq modes graphiques qui permettent à une application de spécifier le mode de mélange des couleurs, le mode de mise à l’échelle de la sortie, et ainsi de suite. Ces modes, qui sont stockés dans un DC, sont décrits dans le tableau suivant.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modes graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528342"
---
# <a name="graphic-modes"></a><span data-ttu-id="602fc-104">Modes graphiques</span><span class="sxs-lookup"><span data-stu-id="602fc-104">Graphic Modes</span></span>

<span data-ttu-id="602fc-105">Windows prend en charge cinq modes graphiques qui permettent à une application de spécifier le mode de mélange des couleurs, le mode de mise à l’échelle de la sortie, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="602fc-105">Windows supports five graphic modes that allow an application to specify how colors are mixed, where output appears, how the output is scaled, and so on.</span></span> <span data-ttu-id="602fc-106">Ces modes, qui sont stockés dans un DC, sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="602fc-106">These modes, which are stored in a DC, are described in the following table.</span></span>



| <span data-ttu-id="602fc-107">Mode graphique</span><span class="sxs-lookup"><span data-stu-id="602fc-107">Graphics mode</span></span> | <span data-ttu-id="602fc-108">Description</span><span class="sxs-lookup"><span data-stu-id="602fc-108">Description</span></span>                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="602fc-109">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="602fc-109">Background</span></span>    | <span data-ttu-id="602fc-110">Définit comment les couleurs d’arrière-plan sont mélangées avec des couleurs de fenêtre ou d’écran existantes pour les opérations de bitmap et de texte.</span><span class="sxs-lookup"><span data-stu-id="602fc-110">Defines how background colors are mixed with existing window or screen colors for bitmap and text operations.</span></span>              |
| <span data-ttu-id="602fc-111">Dessin</span><span class="sxs-lookup"><span data-stu-id="602fc-111">Drawing</span></span>       | <span data-ttu-id="602fc-112">Définit comment les couleurs de premier plan sont mélangées avec des couleurs de fenêtre ou d’écran existantes pour les opérations de stylet, de pinceau, de bitmap et de texte.</span><span class="sxs-lookup"><span data-stu-id="602fc-112">Defines how foreground colors are mixed with existing window or screen colors for pen, brush, bitmap, and text operations.</span></span> |
| <span data-ttu-id="602fc-113">Mappage</span><span class="sxs-lookup"><span data-stu-id="602fc-113">Mapping</span></span>       | <span data-ttu-id="602fc-114">Définit la façon dont la sortie graphique est mappée de l’espace logique (ou universel) sur le papier de la fenêtre, de l’écran ou de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="602fc-114">Defines how graphics output is mapped from logical (or world) space onto the window, screen, or printer paper.</span></span>             |
| <span data-ttu-id="602fc-115">Polygone-remplissage</span><span class="sxs-lookup"><span data-stu-id="602fc-115">Polygon-fill</span></span>  | <span data-ttu-id="602fc-116">Définit la façon dont le modèle de pinceau est utilisé pour remplir l’intérieur des régions complexes.</span><span class="sxs-lookup"><span data-stu-id="602fc-116">Defines how the brush pattern is used to fill the interior of complex regions.</span></span>                                             |
| <span data-ttu-id="602fc-117">Étirement</span><span class="sxs-lookup"><span data-stu-id="602fc-117">Stretching</span></span>    | <span data-ttu-id="602fc-118">Définit comment les couleurs de la bitmap sont mélangées avec des couleurs de fenêtre ou d’écran existantes lorsque la bitmap est compressée (ou réduite).</span><span class="sxs-lookup"><span data-stu-id="602fc-118">Defines how bitmap colors are mixed with existing window or screen colors when the bitmap is compressed (or scaled down).</span></span>  |



 

<span data-ttu-id="602fc-119">Comme c’est le cas avec les objets graphiques, le système Initialise un contrôleur de réseau avec les modes graphiques par défaut.</span><span class="sxs-lookup"><span data-stu-id="602fc-119">As it does with graphic objects, the system initializes a DC with default graphic modes.</span></span> <span data-ttu-id="602fc-120">Une application peut récupérer et examiner ces modes par défaut en appelant les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="602fc-120">An application can retrieve and examine these default modes by calling the following functions.</span></span>



| <span data-ttu-id="602fc-121">Mode graphique</span><span class="sxs-lookup"><span data-stu-id="602fc-121">Graphics mode</span></span> | <span data-ttu-id="602fc-122">Fonction</span><span class="sxs-lookup"><span data-stu-id="602fc-122">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="602fc-123">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="602fc-123">Background</span></span>    | [<span data-ttu-id="602fc-124">**GetBkMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-124">**GetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| <span data-ttu-id="602fc-125">Dessin</span><span class="sxs-lookup"><span data-stu-id="602fc-125">Drawing</span></span>       | [<span data-ttu-id="602fc-126">**GetROP2**</span><span class="sxs-lookup"><span data-stu-id="602fc-126">**GetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| <span data-ttu-id="602fc-127">Mappage</span><span class="sxs-lookup"><span data-stu-id="602fc-127">Mapping</span></span>       | [<span data-ttu-id="602fc-128">**GetMapMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-128">**GetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| <span data-ttu-id="602fc-129">Polygone-remplissage</span><span class="sxs-lookup"><span data-stu-id="602fc-129">Polygon-fill</span></span>  | [<span data-ttu-id="602fc-130">**GetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-130">**GetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| <span data-ttu-id="602fc-131">Étirement</span><span class="sxs-lookup"><span data-stu-id="602fc-131">Stretching</span></span>    | [<span data-ttu-id="602fc-132">**GetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-132">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

<span data-ttu-id="602fc-133">Une application peut modifier les modes par défaut en appelant l’une des fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="602fc-133">An application can change the default modes by calling one of the following functions.</span></span>



| <span data-ttu-id="602fc-134">Mode graphique</span><span class="sxs-lookup"><span data-stu-id="602fc-134">Graphics mode</span></span> | <span data-ttu-id="602fc-135">Fonction</span><span class="sxs-lookup"><span data-stu-id="602fc-135">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="602fc-136">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="602fc-136">Background</span></span>    | [<span data-ttu-id="602fc-137">**SetBkMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-137">**SetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| <span data-ttu-id="602fc-138">Dessin</span><span class="sxs-lookup"><span data-stu-id="602fc-138">Drawing</span></span>       | [<span data-ttu-id="602fc-139">**SetROP2**</span><span class="sxs-lookup"><span data-stu-id="602fc-139">**SetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| <span data-ttu-id="602fc-140">Mappage</span><span class="sxs-lookup"><span data-stu-id="602fc-140">Mapping</span></span>       | [<span data-ttu-id="602fc-141">**SetMapMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-141">**SetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| <span data-ttu-id="602fc-142">Polygone-remplissage</span><span class="sxs-lookup"><span data-stu-id="602fc-142">Polygon-fill</span></span>  | [<span data-ttu-id="602fc-143">**SetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-143">**SetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| <span data-ttu-id="602fc-144">Étirement</span><span class="sxs-lookup"><span data-stu-id="602fc-144">Stretching</span></span>    | [<span data-ttu-id="602fc-145">**SetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="602fc-145">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



