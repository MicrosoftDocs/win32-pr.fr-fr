---
description: Limite la zone du IAnalysisRegion à la partie de sa zone qui ne croise pas le rectangle spécifié.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'IAnalysisRegion :: ExcludeRectangle, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514197"
---
# <a name="ianalysisregionexcluderectangle-method"></a><span data-ttu-id="e1de4-103">IAnalysisRegion :: ExcludeRectangle, méthode</span><span class="sxs-lookup"><span data-stu-id="e1de4-103">IAnalysisRegion::ExcludeRectangle method</span></span>

<span data-ttu-id="e1de4-104">Limite la zone du [**IAnalysisRegion**](ianalysisregion.md) à la partie de sa zone qui ne croise pas le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="e1de4-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1de4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1de4-105">Syntax</span></span>


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="e1de4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1de4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1de4-107">*pExcludingRectangle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1de4-107">*pExcludingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1de4-108">Rectangle à exclure de ce [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="e1de4-108">The rectangle to exclude from this [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1de4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1de4-109">Return value</span></span>

<span data-ttu-id="e1de4-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e1de4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1de4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e1de4-111">Remarks</span></span>

<span data-ttu-id="e1de4-112">Les coordonnées du rectangle sont exprimées en unités HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="e1de4-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="e1de4-113">Si les deux zones ne se croisent pas, le [**IAnalysisRegion**](ianalysisregion.md) est inchangé.</span><span class="sxs-lookup"><span data-stu-id="e1de4-113">If the two areas do not intersect, the [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1de4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1de4-114">Requirements</span></span>



| <span data-ttu-id="e1de4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1de4-115">Requirement</span></span> | <span data-ttu-id="e1de4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1de4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1de4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1de4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1de4-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1de4-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1de4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1de4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1de4-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1de4-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e1de4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1de4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1de4-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e1de4-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e1de4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e1de4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1de4-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1de4-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e1de4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1de4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1de4-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="e1de4-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="e1de4-127">**IAnalysisRegion :: ExcludeRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="e1de4-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="e1de4-128">**IAnalysisRegion :: IntersectRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="e1de4-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="e1de4-129">**IAnalysisRegion :: IntersectRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="e1de4-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="e1de4-130">**IAnalysisRegion :: UnionRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="e1de4-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="e1de4-131">**IAnalysisRegion :: UnionRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="e1de4-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="e1de4-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e1de4-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




