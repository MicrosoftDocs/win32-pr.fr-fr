---
description: Retourne les identificateurs de trait associés à ce IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'IAnalysisAlternate :: GetStrokeIds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862730"
---
# <a name="ianalysisalternategetstrokeids-method"></a><span data-ttu-id="22d63-103">IAnalysisAlternate :: GetStrokeIds, méthode</span><span class="sxs-lookup"><span data-stu-id="22d63-103">IAnalysisAlternate::GetStrokeIds method</span></span>

<span data-ttu-id="22d63-104">Retourne les identificateurs de trait associés à ce [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="22d63-104">Returns the stroke identifiers that are associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="22d63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22d63-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="22d63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22d63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d63-107">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="22d63-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22d63-108">Pointeur vers un **ULong** qui a pour valeur le nombre d’identificateurs de trait associés à ce [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="22d63-108">A pointer to a **ULONG** that is set to the number of stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> <dt>

<span data-ttu-id="22d63-109">*pplStrokeIds* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="22d63-109">*pplStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22d63-110">\[out, size \_ is ( \* *PULSTROKEIDSCOUNT* \* sizeof (long))\]</span><span class="sxs-lookup"><span data-stu-id="22d63-110">\[out, size\_is(\**pulStrokeIdsCount* \* sizeof(LONG))\]</span></span>

<span data-ttu-id="22d63-111">Tableau de *pulStrokeIdsCount* de longueur **long** qui a pour valeur les identificateurs de trait associés à ce [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="22d63-111">An array of **LONG** of length *pulStrokeIdsCount* that is set to the stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d63-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22d63-112">Return value</span></span>

<span data-ttu-id="22d63-113">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="22d63-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22d63-114">Notes</span><span class="sxs-lookup"><span data-stu-id="22d63-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="22d63-115">Pour éviter une fuite de mémoire, utilisez [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *pplStrokeIds* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="22d63-115">To avoid a memory leak, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokeIds* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22d63-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22d63-116">Requirements</span></span>



| <span data-ttu-id="22d63-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22d63-117">Requirement</span></span> | <span data-ttu-id="22d63-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="22d63-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d63-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22d63-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22d63-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22d63-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="22d63-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22d63-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22d63-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="22d63-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="22d63-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="22d63-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="22d63-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="22d63-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="22d63-125">DLL</span><span class="sxs-lookup"><span data-stu-id="22d63-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22d63-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22d63-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="22d63-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22d63-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d63-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="22d63-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="22d63-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="22d63-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

