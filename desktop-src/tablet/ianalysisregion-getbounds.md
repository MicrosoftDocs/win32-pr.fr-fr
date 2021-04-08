---
description: Obtient le rectangle englobant du IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'IAnalysisRegion :: GetBounds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751876"
---
# <a name="ianalysisregiongetbounds-method"></a><span data-ttu-id="3bdd8-103">IAnalysisRegion :: GetBounds, méthode</span><span class="sxs-lookup"><span data-stu-id="3bdd8-103">IAnalysisRegion::GetBounds method</span></span>

<span data-ttu-id="3bdd8-104">Obtient le rectangle englobant du [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="3bdd8-104">Gets the bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bdd8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bdd8-105">Syntax</span></span>


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="3bdd8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bdd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bdd8-107">*pBoundingRectangle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3bdd8-107">*pBoundingRectangle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bdd8-108">Rectangle englobant du [**IAnalysisRegion**](ianalysisregion.md) dans les coordonnées de l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="3bdd8-108">The bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md) in ink space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bdd8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bdd8-109">Return value</span></span>

<span data-ttu-id="3bdd8-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3bdd8-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3bdd8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3bdd8-111">Remarks</span></span>

<span data-ttu-id="3bdd8-112">Les limites sont exprimées en coordonnées d’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="3bdd8-112">The bounds are in ink-space coordinates.</span></span>

<span data-ttu-id="3bdd8-113">Si le [**IAnalysisRegion**](ianalysisregion.md) représente une zone infinie, les limites gauche et supérieure sont **int \_ min**; et les limites droite et inférieure sont **int \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="3bdd8-113">If the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite area, the left and top bounds are **INT\_MIN**; and the right and bottom bounds are **INT\_MAX**.</span></span>

<span data-ttu-id="3bdd8-114">Si le [**IAnalysisRegion**](ianalysisregion.md) représente une zone vide, toutes les limites du rectangle sont 0.</span><span class="sxs-lookup"><span data-stu-id="3bdd8-114">If the [**IAnalysisRegion**](ianalysisregion.md) represents an empty area, all the bounds of the rectangle are 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bdd8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bdd8-115">Requirements</span></span>



| <span data-ttu-id="3bdd8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bdd8-116">Requirement</span></span> | <span data-ttu-id="3bdd8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bdd8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bdd8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bdd8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3bdd8-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bdd8-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3bdd8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bdd8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3bdd8-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bdd8-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3bdd8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bdd8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bdd8-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3bdd8-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3bdd8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3bdd8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bdd8-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bdd8-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3bdd8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bdd8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bdd8-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="3bdd8-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="3bdd8-128">**IAnalysisRegion :: GetRegionScans, méthode**</span><span class="sxs-lookup"><span data-stu-id="3bdd8-128">**IAnalysisRegion::GetRegionScans Method**</span></span>](ianalysisregion-getregionscans.md)
</dt> <dt>

[<span data-ttu-id="3bdd8-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3bdd8-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




