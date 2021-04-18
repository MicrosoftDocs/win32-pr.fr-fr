---
description: Développe la zone de ce IAnalysisRegion vers la zone créée par son Union avec le IAnalysisRegion spécifié.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'IAnalysisRegion :: UnionRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516020"
---
# <a name="ianalysisregionunionregion-method"></a><span data-ttu-id="be94b-103">IAnalysisRegion :: UnionRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="be94b-103">IAnalysisRegion::UnionRegion method</span></span>

<span data-ttu-id="be94b-104">Développe la zone de ce [**IAnalysisRegion**](ianalysisregion.md) vers la zone créée par son Union avec le **IAnalysisRegion** spécifié.</span><span class="sxs-lookup"><span data-stu-id="be94b-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="be94b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be94b-105">Syntax</span></span>


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a><span data-ttu-id="be94b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be94b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be94b-107">*pRegionToUnion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be94b-107">*pRegionToUnion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be94b-108">[**IAnalysisRegion**](ianalysisregion.md) avec lequel effectuer la combinaison.</span><span class="sxs-lookup"><span data-stu-id="be94b-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to combine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be94b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be94b-109">Return value</span></span>

<span data-ttu-id="be94b-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="be94b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be94b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="be94b-111">Remarks</span></span>

<span data-ttu-id="be94b-112">Si l’une des zones est infinie, la nouvelle zone est également infinie.</span><span class="sxs-lookup"><span data-stu-id="be94b-112">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="be94b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be94b-113">Requirements</span></span>



| <span data-ttu-id="be94b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be94b-114">Requirement</span></span> | <span data-ttu-id="be94b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="be94b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be94b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be94b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be94b-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be94b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be94b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be94b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be94b-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be94b-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be94b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="be94b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be94b-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be94b-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be94b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="be94b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be94b-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be94b-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be94b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be94b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be94b-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="be94b-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="be94b-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="be94b-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="be94b-127">**IAnalysisRegion :: ExcludeRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="be94b-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="be94b-128">**IAnalysisRegion :: IntersectRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="be94b-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="be94b-129">**IAnalysisRegion :: IntersectRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="be94b-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="be94b-130">**IAnalysisRegion :: UnionRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="be94b-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="be94b-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="be94b-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




