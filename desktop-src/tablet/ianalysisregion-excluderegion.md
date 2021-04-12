---
description: Limite la zone du IAnalysisRegion à la partie de sa zone qui ne croise pas le IAnalysisRegion spécifié.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'IAnalysisRegion :: ExcludeRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526559"
---
# <a name="ianalysisregionexcluderegion-method"></a><span data-ttu-id="a4f60-103">IAnalysisRegion :: ExcludeRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="a4f60-103">IAnalysisRegion::ExcludeRegion method</span></span>

<span data-ttu-id="a4f60-104">Limite la zone du [**IAnalysisRegion**](ianalysisregion.md) à la partie de sa zone qui ne croise pas le **IAnalysisRegion** spécifié.</span><span class="sxs-lookup"><span data-stu-id="a4f60-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4f60-105">Syntax</span></span>


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a><span data-ttu-id="a4f60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4f60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f60-107">*pRegionToExclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4f60-107">*pRegionToExclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f60-108">[**IAnalysisRegion**](ianalysisregion.md) à exclure de ce **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="a4f60-108">The [**IAnalysisRegion**](ianalysisregion.md) to exclude from this **IAnalysisRegion**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f60-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4f60-109">Return value</span></span>

<span data-ttu-id="a4f60-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a4f60-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f60-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a4f60-111">Remarks</span></span>

<span data-ttu-id="a4f60-112">Si les deux zones ne se croisent pas, ce [**IAnalysisRegion**](ianalysisregion.md) est inchangé.</span><span class="sxs-lookup"><span data-stu-id="a4f60-112">If the two areas do not intersect, this [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f60-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4f60-113">Requirements</span></span>



| <span data-ttu-id="a4f60-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4f60-114">Requirement</span></span> | <span data-ttu-id="a4f60-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f60-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f60-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f60-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f60-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4f60-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a4f60-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f60-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f60-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f60-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a4f60-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4f60-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f60-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f60-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a4f60-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f60-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4f60-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4f60-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a4f60-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4f60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f60-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="a4f60-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="a4f60-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="a4f60-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="a4f60-127">**IAnalysisRegion :: IntersectRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="a4f60-127">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="a4f60-128">**IAnalysisRegion :: IntersectRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="a4f60-128">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="a4f60-129">**IAnalysisRegion :: UnionRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="a4f60-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="a4f60-130">**IAnalysisRegion :: UnionRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="a4f60-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="a4f60-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a4f60-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




