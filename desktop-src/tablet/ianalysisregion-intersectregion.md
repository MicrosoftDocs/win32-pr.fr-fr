---
description: Limite la zone du IAnalysisRegion à la zone créée par son intersection avec le IAnalysisRegion spécifié.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'IAnalysisRegion :: IntersectRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516484"
---
# <a name="ianalysisregionintersectregion-method"></a><span data-ttu-id="4218e-103">IAnalysisRegion :: IntersectRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="4218e-103">IAnalysisRegion::IntersectRegion method</span></span>

<span data-ttu-id="4218e-104">Limite la zone du [**IAnalysisRegion**](ianalysisregion.md) à la zone créée par son intersection avec le **IAnalysisRegion** spécifié.</span><span class="sxs-lookup"><span data-stu-id="4218e-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4218e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4218e-105">Syntax</span></span>


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a><span data-ttu-id="4218e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4218e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4218e-107">*pRegionToIntersect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4218e-107">*pRegionToIntersect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4218e-108">[**IAnalysisRegion**](ianalysisregion.md) avec lequel effectuer l’intersection.</span><span class="sxs-lookup"><span data-stu-id="4218e-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to intersect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4218e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4218e-109">Return value</span></span>

<span data-ttu-id="4218e-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="4218e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4218e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4218e-111">Remarks</span></span>

<span data-ttu-id="4218e-112">Si les deux zones ne se croisent pas, la nouvelle zone est vide.</span><span class="sxs-lookup"><span data-stu-id="4218e-112">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="4218e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4218e-113">Requirements</span></span>



| <span data-ttu-id="4218e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4218e-114">Requirement</span></span> | <span data-ttu-id="4218e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4218e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4218e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4218e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4218e-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4218e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4218e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4218e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4218e-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4218e-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4218e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4218e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4218e-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4218e-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4218e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4218e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4218e-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4218e-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4218e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4218e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4218e-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="4218e-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="4218e-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="4218e-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="4218e-127">**IAnalysisRegion :: ExcludeRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="4218e-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="4218e-128">**IAnalysisRegion :: IntersectRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="4218e-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="4218e-129">**IAnalysisRegion :: UnionRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="4218e-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="4218e-130">**IAnalysisRegion :: UnionRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="4218e-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="4218e-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="4218e-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




