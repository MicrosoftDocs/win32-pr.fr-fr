---
description: ICE95 vérifie la table de contrôle et la table BBControl pour vérifier que les contrôles de tableau blanc s’intègrent à tous les panneaux.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209897"
---
# <a name="ice95"></a><span data-ttu-id="7dda5-103">ICE95</span><span class="sxs-lookup"><span data-stu-id="7dda5-103">ICE95</span></span>

<span data-ttu-id="7dda5-104">ICE95 vérifie la table de contrôle et la [table BBControl](bbcontrol-table.md) pour vérifier que les contrôles de [tableau](control-table.md) blanc s’intègrent à tous les panneaux.</span><span class="sxs-lookup"><span data-stu-id="7dda5-104">ICE95 checks the [Control table](control-table.md) and [BBControl table](bbcontrol-table.md) to verify that the billboard controls fit onto all the billboards.</span></span>

## <a name="result"></a><span data-ttu-id="7dda5-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="7dda5-105">Result</span></span>

<span data-ttu-id="7dda5-106">Si l’une des conditions suivantes est vraie, un contrôle d’affichage des panneaux ne peut pas être contenu dans un panneau.</span><span class="sxs-lookup"><span data-stu-id="7dda5-106">If any of the following are true, a billboard control fails to fit on a billboard.</span></span> <span data-ttu-id="7dda5-107">ICE95 publie les avertissements suivants.</span><span class="sxs-lookup"><span data-stu-id="7dda5-107">ICE95 posts the following warnings.</span></span>



| <span data-ttu-id="7dda5-108">AVERTISSEMENT ICE95</span><span class="sxs-lookup"><span data-stu-id="7dda5-108">ICE95 warning</span></span>                                                                                                                                                                                                              | <span data-ttu-id="7dda5-109">Description</span><span class="sxs-lookup"><span data-stu-id="7dda5-109">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dda5-110">Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7dda5-110">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="7dda5-111">La coordonnée X dépasse la limite de la largeur minimale du contrôle de tableau blanc% s</span><span class="sxs-lookup"><span data-stu-id="7dda5-111">The X coordinate exceeds the boundary of the minimum billboard control width %s</span></span>                   | <span data-ttu-id="7dda5-112">La coordonnée X du contrôle est en dehors de la largeur du panneau.</span><span class="sxs-lookup"><span data-stu-id="7dda5-112">The control's X coordinate is outside the width of the billboard.</span></span>                          |
| <span data-ttu-id="7dda5-113">Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7dda5-113">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="7dda5-114">La coordonnée Y dépasse la limite de la hauteur minimale du contrôle de tableau blanc% s</span><span class="sxs-lookup"><span data-stu-id="7dda5-114">The Y coordinate exceeds the boundary of the minimum billboard control height %s</span></span>                  | <span data-ttu-id="7dda5-115">La coordonnée Y du contrôle est en dessous du bas du panneau.</span><span class="sxs-lookup"><span data-stu-id="7dda5-115">The control's Y coordinate is below the bottom of the billboard.</span></span>                           |
| <span data-ttu-id="7dda5-116">Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7dda5-116">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="7dda5-117">La coordonnée X et la largeur combinés dépassent la largeur minimale du contrôle de tableau blanc% s</span><span class="sxs-lookup"><span data-stu-id="7dda5-117">The X coordinate and the width combined together exceeds the minimum billboard control width %s</span></span>   | <span data-ttu-id="7dda5-118">La coordonnée X du contrôle plus la largeur du contrôle est en dehors de la largeur du panneau.</span><span class="sxs-lookup"><span data-stu-id="7dda5-118">The control's X coordinate plus the control's width is outside the width of the billboard.</span></span> |
| <span data-ttu-id="7dda5-119">Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7dda5-119">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="7dda5-120">La coordonnée Y et la hauteur combinés dépassent la hauteur minimale du contrôle de tableau blanc% s</span><span class="sxs-lookup"><span data-stu-id="7dda5-120">The Y coordinate and the height combined together exceeds the minimum billboard control height %s</span></span> | <span data-ttu-id="7dda5-121">La coordonnée Y du contrôle plus la hauteur du contrôle se trouve en dessous du bas du panneau.</span><span class="sxs-lookup"><span data-stu-id="7dda5-121">The control's Y coordinate plus the control's height is below the bottom of the billboard.</span></span> |



 

## <a name="example"></a><span data-ttu-id="7dda5-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="7dda5-122">Example</span></span>

<span data-ttu-id="7dda5-123">ICE95 signale les avertissements suivants pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="7dda5-123">ICE95 reports the following warnings for the example:</span></span>

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

<span data-ttu-id="7dda5-124">Table de contrôle (partielle) (partielle)</span><span class="sxs-lookup"><span data-stu-id="7dda5-124">Control Table (partial) (partial)</span></span>



| <span data-ttu-id="7dda5-125">Contrôler</span><span class="sxs-lookup"><span data-stu-id="7dda5-125">Control</span></span>  | <span data-ttu-id="7dda5-126">Type</span><span class="sxs-lookup"><span data-stu-id="7dda5-126">Type</span></span>      | <span data-ttu-id="7dda5-127">Largeur</span><span class="sxs-lookup"><span data-stu-id="7dda5-127">Width</span></span> | <span data-ttu-id="7dda5-128">Hauteur</span><span class="sxs-lookup"><span data-stu-id="7dda5-128">Height</span></span> |
|----------|-----------|-------|--------|
| <span data-ttu-id="7dda5-129">Control1</span><span class="sxs-lookup"><span data-stu-id="7dda5-129">control1</span></span> | <span data-ttu-id="7dda5-130">Blanc</span><span class="sxs-lookup"><span data-stu-id="7dda5-130">Billboard</span></span> | <span data-ttu-id="7dda5-131">300</span><span class="sxs-lookup"><span data-stu-id="7dda5-131">300</span></span>   | <span data-ttu-id="7dda5-132">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-132">100</span></span>    |
| <span data-ttu-id="7dda5-133">Control2</span><span class="sxs-lookup"><span data-stu-id="7dda5-133">Control2</span></span> | <span data-ttu-id="7dda5-134">Blanc</span><span class="sxs-lookup"><span data-stu-id="7dda5-134">Billboard</span></span> | <span data-ttu-id="7dda5-135">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-135">100</span></span>   | <span data-ttu-id="7dda5-136">300</span><span class="sxs-lookup"><span data-stu-id="7dda5-136">300</span></span>    |



 

[<span data-ttu-id="7dda5-137">Table BBControl</span><span class="sxs-lookup"><span data-stu-id="7dda5-137">BBControl table</span></span>](bbcontrol-table.md)



| <span data-ttu-id="7dda5-138">Blanc\_</span><span class="sxs-lookup"><span data-stu-id="7dda5-138">Billboard\_</span></span> | <span data-ttu-id="7dda5-139">BBControl</span><span class="sxs-lookup"><span data-stu-id="7dda5-139">BBControl</span></span>  | <span data-ttu-id="7dda5-140">X</span><span class="sxs-lookup"><span data-stu-id="7dda5-140">X</span></span>   | <span data-ttu-id="7dda5-141">O</span><span class="sxs-lookup"><span data-stu-id="7dda5-141">Y</span></span>   | <span data-ttu-id="7dda5-142">Largeur</span><span class="sxs-lookup"><span data-stu-id="7dda5-142">Width</span></span> | <span data-ttu-id="7dda5-143">Hauteur</span><span class="sxs-lookup"><span data-stu-id="7dda5-143">Height</span></span> |
|-------------|------------|-----|-----|-------|--------|
| <span data-ttu-id="7dda5-144">billboard1</span><span class="sxs-lookup"><span data-stu-id="7dda5-144">billboard1</span></span>  | <span data-ttu-id="7dda5-145">bbcontrol1</span><span class="sxs-lookup"><span data-stu-id="7dda5-145">bbcontrol1</span></span> | <span data-ttu-id="7dda5-146">200</span><span class="sxs-lookup"><span data-stu-id="7dda5-146">200</span></span> | <span data-ttu-id="7dda5-147">0</span><span class="sxs-lookup"><span data-stu-id="7dda5-147">0</span></span>   | <span data-ttu-id="7dda5-148">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-148">100</span></span>   | <span data-ttu-id="7dda5-149">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-149">100</span></span>    |
| <span data-ttu-id="7dda5-150">billboard1</span><span class="sxs-lookup"><span data-stu-id="7dda5-150">billboard1</span></span>  | <span data-ttu-id="7dda5-151">bbcontrol2</span><span class="sxs-lookup"><span data-stu-id="7dda5-151">bbcontrol2</span></span> | <span data-ttu-id="7dda5-152">0</span><span class="sxs-lookup"><span data-stu-id="7dda5-152">0</span></span>   | <span data-ttu-id="7dda5-153">200</span><span class="sxs-lookup"><span data-stu-id="7dda5-153">200</span></span> | <span data-ttu-id="7dda5-154">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-154">100</span></span>   | <span data-ttu-id="7dda5-155">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-155">100</span></span>    |
| <span data-ttu-id="7dda5-156">billboard1</span><span class="sxs-lookup"><span data-stu-id="7dda5-156">billboard1</span></span>  | <span data-ttu-id="7dda5-157">bbcontrol3</span><span class="sxs-lookup"><span data-stu-id="7dda5-157">bbcontrol3</span></span> | <span data-ttu-id="7dda5-158">50</span><span class="sxs-lookup"><span data-stu-id="7dda5-158">50</span></span>  | <span data-ttu-id="7dda5-159">0</span><span class="sxs-lookup"><span data-stu-id="7dda5-159">0</span></span>   | <span data-ttu-id="7dda5-160">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-160">100</span></span>   | <span data-ttu-id="7dda5-161">50</span><span class="sxs-lookup"><span data-stu-id="7dda5-161">50</span></span>     |
| <span data-ttu-id="7dda5-162">billboard1</span><span class="sxs-lookup"><span data-stu-id="7dda5-162">billboard1</span></span>  | <span data-ttu-id="7dda5-163">bbcontrol4</span><span class="sxs-lookup"><span data-stu-id="7dda5-163">bbcontrol4</span></span> | <span data-ttu-id="7dda5-164">0</span><span class="sxs-lookup"><span data-stu-id="7dda5-164">0</span></span>   | <span data-ttu-id="7dda5-165">50</span><span class="sxs-lookup"><span data-stu-id="7dda5-165">50</span></span>  | <span data-ttu-id="7dda5-166">50</span><span class="sxs-lookup"><span data-stu-id="7dda5-166">50</span></span>    | <span data-ttu-id="7dda5-167">100</span><span class="sxs-lookup"><span data-stu-id="7dda5-167">100</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="7dda5-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7dda5-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dda5-169">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="7dda5-169">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



