---
description: Développe la zone de ce IAnalysisRegion vers la zone créée par son Union avec le rectangle spécifié.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'IAnalysisRegion :: UnionRectangle, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514635"
---
# <a name="ianalysisregionunionrectangle-method"></a><span data-ttu-id="12670-103">IAnalysisRegion :: UnionRectangle, méthode</span><span class="sxs-lookup"><span data-stu-id="12670-103">IAnalysisRegion::UnionRectangle method</span></span>

<span data-ttu-id="12670-104">Développe la zone de ce [**IAnalysisRegion**](ianalysisregion.md) vers la zone créée par son Union avec le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="12670-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="12670-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12670-105">Syntax</span></span>


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="12670-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12670-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12670-107">*pRectangle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12670-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12670-108">Pointeur vers le rectangle avec lequel combiner, en coordonnées d’espace manuscrit.</span><span class="sxs-lookup"><span data-stu-id="12670-108">A pointer to the rectangle with which to combine, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12670-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12670-109">Return value</span></span>

<span data-ttu-id="12670-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="12670-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12670-111">Notes</span><span class="sxs-lookup"><span data-stu-id="12670-111">Remarks</span></span>

<span data-ttu-id="12670-112">Les coordonnées du rectangle sont exprimées en unités HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="12670-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="12670-113">Si l’une des zones est infinie, la nouvelle zone est également infinie.</span><span class="sxs-lookup"><span data-stu-id="12670-113">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="12670-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12670-114">Requirements</span></span>



| <span data-ttu-id="12670-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12670-115">Requirement</span></span> | <span data-ttu-id="12670-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="12670-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12670-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12670-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12670-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12670-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12670-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12670-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12670-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="12670-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="12670-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="12670-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="12670-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="12670-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="12670-123">DLL</span><span class="sxs-lookup"><span data-stu-id="12670-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12670-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12670-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="12670-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12670-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12670-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="12670-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="12670-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="12670-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="12670-128">**IAnalysisRegion :: ExcludeRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="12670-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="12670-129">**IAnalysisRegion :: IntersectRectangle, méthode**</span><span class="sxs-lookup"><span data-stu-id="12670-129">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="12670-130">**IAnalysisRegion :: IntersectRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="12670-130">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="12670-131">**IAnalysisRegion :: UnionRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="12670-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="12670-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="12670-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




