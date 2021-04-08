---
description: Expose des méthodes et des propriétés pour une zone qui représente une zone d’un document.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interface IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751860"
---
# <a name="ianalysisregion-interface"></a><span data-ttu-id="e8632-103">Interface IAnalysisRegion</span><span class="sxs-lookup"><span data-stu-id="e8632-103">IAnalysisRegion interface</span></span>

<span data-ttu-id="e8632-104">Expose des méthodes et des propriétés pour une zone qui représente une zone d’un document.</span><span class="sxs-lookup"><span data-stu-id="e8632-104">Exposes methods and properties for a region that represents an area of a document.</span></span>

## <a name="members"></a><span data-ttu-id="e8632-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e8632-105">Members</span></span>

<span data-ttu-id="e8632-106">L’interface **IAnalysisRegion** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e8632-106">The **IAnalysisRegion** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e8632-107">**IAnalysisRegion** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e8632-107">**IAnalysisRegion** also has these types of members:</span></span>

-   [<span data-ttu-id="e8632-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e8632-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e8632-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e8632-109">Methods</span></span>

<span data-ttu-id="e8632-110">L’interface **IAnalysisRegion** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e8632-110">The **IAnalysisRegion** interface has these methods.</span></span>



| <span data-ttu-id="e8632-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="e8632-111">Method</span></span>                                                           | <span data-ttu-id="e8632-112">Description</span><span class="sxs-lookup"><span data-stu-id="e8632-112">Description</span></span>                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8632-113">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="e8632-113">**Clone**</span></span>](ianalysisregion-clone.md)                           | <span data-ttu-id="e8632-114">Crée une copie du **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="e8632-114">Creates a copy of the **IAnalysisRegion**.</span></span><br/>                                                                                          |
| [<span data-ttu-id="e8632-115">**ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="e8632-115">**ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)     | <span data-ttu-id="e8632-116">Limite la zone du **IAnalysisRegion** à la partie de sa zone qui ne croise pas le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8632-116">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified rectangle.</span></span><br/>           |
| [<span data-ttu-id="e8632-117">**ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="e8632-117">**ExcludeRegion**</span></span>](ianalysisregion-excluderegion.md)           | <span data-ttu-id="e8632-118">Limite la zone du **IAnalysisRegion** à la partie de sa zone qui ne croise pas le **IAnalysisRegion** spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8632-118">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span><br/> |
| [<span data-ttu-id="e8632-119">**GetBounds**</span><span class="sxs-lookup"><span data-stu-id="e8632-119">**GetBounds**</span></span>](ianalysisregion-getbounds.md)                   | <span data-ttu-id="e8632-120">Récupère le rectangle englobant du **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="e8632-120">Retrieves the bounding rectangle of the **IAnalysisRegion**.</span></span><br/>                                                                        |
| [<span data-ttu-id="e8632-121">**GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="e8632-121">**GetRegionScans**</span></span>](ianalysisregion-getregionscans.md)         | <span data-ttu-id="e8632-122">Récupère un tableau de rectangles qui définit la zone du **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="e8632-122">Retrieves an array of rectangles that defines the area of the **IAnalysisRegion**.</span></span><br/>                                                  |
| [<span data-ttu-id="e8632-123">**IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="e8632-123">**IntersectRectangle**</span></span>](ianalysisregion-intersectrectangle.md) | <span data-ttu-id="e8632-124">Limite la zone de ce **IAnalysisRegion** à la zone créée par son intersection avec le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8632-124">Restricts the area of this **IAnalysisRegion** to the area created by its intersection with the specified rectangle.</span></span><br/>                |
| [<span data-ttu-id="e8632-125">**IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="e8632-125">**IntersectRegion**</span></span>](ianalysisregion-intersectregion.md)       | <span data-ttu-id="e8632-126">Limite la zone du **IAnalysisRegion** à la zone créée par son intersection avec le **IAnalysisRegion** spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8632-126">Restricts the area of the **IAnalysisRegion** to the area created by its intersection with the specified **IAnalysisRegion**.</span></span><br/>       |
| [<span data-ttu-id="e8632-127">**IntersectsWith**</span><span class="sxs-lookup"><span data-stu-id="e8632-127">**IntersectsWith**</span></span>](ianalysisregion-intersectswith.md)         | <span data-ttu-id="e8632-128">Détermine si la zone du **IAnalysisRegion** entre en intersection avec le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8632-128">Determines whether the area of the **IAnalysisRegion** intersects with the specified rectangle.</span></span><br/>                                     |
| [<span data-ttu-id="e8632-129">**IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="e8632-129">**IsEmpty**</span></span>](ianalysisregion-isempty.md)                       | <span data-ttu-id="e8632-130">Récupère une valeur indiquant si le **IAnalysisRegion** représente une zone vide.</span><span class="sxs-lookup"><span data-stu-id="e8632-130">Retrieves a value indicating whether the **IAnalysisRegion** represents an empty region.</span></span><br/>                                            |
| [<span data-ttu-id="e8632-131">**IsInfinite**</span><span class="sxs-lookup"><span data-stu-id="e8632-131">**IsInfinite**</span></span>](ianalysisregion-isinfinite.md)                 | <span data-ttu-id="e8632-132">Récupère une valeur indiquant si le **IAnalysisRegion** représente une région infinie.</span><span class="sxs-lookup"><span data-stu-id="e8632-132">Retrieves a value indicating whether the **IAnalysisRegion** represents an infinite region.</span></span><br/>                                         |
| [<span data-ttu-id="e8632-133">**MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="e8632-133">**MakeEmpty**</span></span>](ianalysisregion-makeempty.md)                   | <span data-ttu-id="e8632-134">Réduit le **IAnalysisRegion** pour représenter une zone vide.</span><span class="sxs-lookup"><span data-stu-id="e8632-134">Reduces the **IAnalysisRegion** to represent an empty area.</span></span><br/>                                                                         |
| [<span data-ttu-id="e8632-135">**MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="e8632-135">**MakeInfinite**</span></span>](ianalysisregion-makeinfinite.md)             | <span data-ttu-id="e8632-136">Développe le **IAnalysisRegion** pour représenter une zone infinie.</span><span class="sxs-lookup"><span data-stu-id="e8632-136">Expands the **IAnalysisRegion** to represent an infinite area.</span></span><br/>                                                                      |
| [<span data-ttu-id="e8632-137">**UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="e8632-137">**UnionRectangle**</span></span>](ianalysisregion-unionrectangle.md)         | <span data-ttu-id="e8632-138">Développe la zone de ce **IAnalysisRegion** vers la zone créée par son Union avec le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8632-138">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified rectangle.</span></span><br/>                         |
| [<span data-ttu-id="e8632-139">**UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="e8632-139">**UnionRegion**</span></span>](ianalysisregion-unionregion.md)               | <span data-ttu-id="e8632-140">Développe la zone de ce **IAnalysisRegion** vers la zone créée par son Union avec le **IAnalysisRegion** spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8632-140">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified **IAnalysisRegion**.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="e8632-141">Notes</span><span class="sxs-lookup"><span data-stu-id="e8632-141">Remarks</span></span>

<span data-ttu-id="e8632-142">Cette interface représente une zone qui est construite à partir de régions rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="e8632-142">This interface represents an area that is constructed from rectangular regions.</span></span> <span data-ttu-id="e8632-143">[**IInkAnalyzer**](iinkanalyzer.md) retourne ou interprète les coordonnées d’une zone dans l’espace de coordonnées dans lequel elle reçoit les données de trait.</span><span class="sxs-lookup"><span data-stu-id="e8632-143">The [**IInkAnalyzer**](iinkanalyzer.md) returns or interprets an area's coordinates within the coordinate space in which it receives stroke data.</span></span>

<span data-ttu-id="e8632-144">Pour récupérer les limites actuelles du **IAnalysisRegion**, utilisez la méthode [**IAnalysisRegion :: GetBounds**](ianalysisregion-getbounds.md) ou la [**méthode IAnalysisRegion :: GetRegionScans**](ianalysisregion-getregionscans.md).</span><span class="sxs-lookup"><span data-stu-id="e8632-144">To get the current bounds of the **IAnalysisRegion**, use [**IAnalysisRegion::GetBounds Method**](ianalysisregion-getbounds.md) or [**IAnalysisRegion::GetRegionScans Method**](ianalysisregion-getregionscans.md).</span></span>

<span data-ttu-id="e8632-145">Pour modifier la zone d’un **IAnalysisRegion** existant, utilisez les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8632-145">To modify the area of an existing **IAnalysisRegion**, use the following methods.</span></span>

-   [<span data-ttu-id="e8632-146">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="e8632-146">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
-   [<span data-ttu-id="e8632-147">**IAnalysisRegion :: ExcludeRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="e8632-147">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
-   [<span data-ttu-id="e8632-148">**IAnalysisRegion :: IntersectRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="e8632-148">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
-   [<span data-ttu-id="e8632-149">**IAnalysisRegion :: IntersectRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="e8632-149">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
-   [<span data-ttu-id="e8632-150">**IAnalysisRegion :: MakeEmpty, méthode**</span><span class="sxs-lookup"><span data-stu-id="e8632-150">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
-   [<span data-ttu-id="e8632-151">**IAnalysisRegion :: MakeInfinite, méthode**</span><span class="sxs-lookup"><span data-stu-id="e8632-151">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
-   [<span data-ttu-id="e8632-152">**IAnalysisRegion :: UnionRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="e8632-152">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
-   [<span data-ttu-id="e8632-153">**IAnalysisRegion :: UnionRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="e8632-153">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)

<span data-ttu-id="e8632-154">Cette interface est équivalente à la classe System. Windows. Ink. AnalysisCore. AnalysisRegionBase dans la .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e8632-154">This interface is equivalent to the System.Windows.Ink.AnalysisCore.AnalysisRegionBase class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8632-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8632-155">Requirements</span></span>



| <span data-ttu-id="e8632-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8632-156">Requirement</span></span> | <span data-ttu-id="e8632-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8632-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8632-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8632-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e8632-159">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8632-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e8632-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8632-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e8632-161">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8632-161">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e8632-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8632-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8632-163"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e8632-163"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e8632-164">DLL</span><span class="sxs-lookup"><span data-stu-id="e8632-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8632-165"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8632-165"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e8632-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8632-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8632-167">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e8632-167">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e8632-168">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e8632-168">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

