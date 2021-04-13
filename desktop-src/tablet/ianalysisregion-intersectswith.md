---
description: Détermine si la zone du IAnalysisRegion entre en intersection avec le rectangle spécifié.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'IAnalysisRegion :: IntersectsWith, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526553"
---
# <a name="ianalysisregionintersectswith-method"></a><span data-ttu-id="3512e-103">IAnalysisRegion :: IntersectsWith, méthode</span><span class="sxs-lookup"><span data-stu-id="3512e-103">IAnalysisRegion::IntersectsWith method</span></span>

<span data-ttu-id="3512e-104">Détermine si la zone du [**IAnalysisRegion**](ianalysisregion.md) entre en intersection avec le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="3512e-104">Determines whether the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="3512e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3512e-105">Syntax</span></span>


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a><span data-ttu-id="3512e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3512e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3512e-107">*pRectangle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3512e-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3512e-108">Pointeur vers le rectangle avec lequel comparer, en coordonnées d’espace manuscrit.</span><span class="sxs-lookup"><span data-stu-id="3512e-108">A pointer to the rectangle with which to compare, in ink-space coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="3512e-109">*pfIsIntersecting* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3512e-109">*pfIsIntersecting* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3512e-110">**Variante \_ TRUE** si la zone du [**IAnalysisRegion**](ianalysisregion.md) entre en intersection avec le rectangle spécifié ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="3512e-110">**VARIANT\_TRUE** if the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3512e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3512e-111">Return value</span></span>

<span data-ttu-id="3512e-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3512e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3512e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3512e-113">Remarks</span></span>

<span data-ttu-id="3512e-114">La comparaison est en coordonnées d’espace manuscrit.</span><span class="sxs-lookup"><span data-stu-id="3512e-114">The comparison is in ink-space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="3512e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3512e-115">Requirements</span></span>



| <span data-ttu-id="3512e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3512e-116">Requirement</span></span> | <span data-ttu-id="3512e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3512e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3512e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3512e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3512e-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3512e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3512e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3512e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3512e-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3512e-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3512e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3512e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3512e-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3512e-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3512e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3512e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3512e-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3512e-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3512e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3512e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3512e-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="3512e-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="3512e-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3512e-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




