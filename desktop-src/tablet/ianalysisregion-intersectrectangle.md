---
description: Limite la zone de ce IAnalysisRegion à la zone créée par son intersection avec le rectangle spécifié.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'IAnalysisRegion :: IntersectRectangle, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526554"
---
# <a name="ianalysisregionintersectrectangle-method"></a><span data-ttu-id="a8251-103">IAnalysisRegion :: IntersectRectangle, méthode</span><span class="sxs-lookup"><span data-stu-id="a8251-103">IAnalysisRegion::IntersectRectangle method</span></span>

<span data-ttu-id="a8251-104">Limite la zone de ce [**IAnalysisRegion**](ianalysisregion.md) à la zone créée par son intersection avec le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8251-104">Restricts the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8251-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8251-105">Syntax</span></span>


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="a8251-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8251-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8251-107">*pIntersectingRectangle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8251-107">*pIntersectingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8251-108">Pointeur vers le rectangle avec lequel effectuer l’intersection, en coordonnées d’espace manuscrit.</span><span class="sxs-lookup"><span data-stu-id="a8251-108">A pointer to the rectangle with which to intersect, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8251-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8251-109">Return value</span></span>

<span data-ttu-id="a8251-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a8251-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8251-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a8251-111">Remarks</span></span>

<span data-ttu-id="a8251-112">Les coordonnées du rectangle sont exprimées en unités HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="a8251-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="a8251-113">Si les deux zones ne se croisent pas, la nouvelle zone est vide.</span><span class="sxs-lookup"><span data-stu-id="a8251-113">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8251-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8251-114">Requirements</span></span>



| <span data-ttu-id="a8251-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8251-115">Requirement</span></span> | <span data-ttu-id="a8251-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8251-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8251-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8251-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8251-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8251-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a8251-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8251-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8251-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8251-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a8251-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8251-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8251-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a8251-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a8251-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a8251-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8251-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8251-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a8251-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8251-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8251-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="a8251-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="a8251-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="a8251-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="a8251-128">**IAnalysisRegion :: ExcludeRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="a8251-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="a8251-129">**IAnalysisRegion :: IntersectRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="a8251-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="a8251-130">**IAnalysisRegion :: UnionRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="a8251-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="a8251-131">**IAnalysisRegion :: UnionRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="a8251-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="a8251-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a8251-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




