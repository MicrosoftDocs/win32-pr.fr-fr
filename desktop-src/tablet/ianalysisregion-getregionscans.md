---
description: Récupère un tableau de rectangles qui définit la zone du IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'IAnalysisRegion :: GetRegionScans, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516485"
---
# <a name="ianalysisregiongetregionscans-method"></a><span data-ttu-id="828e3-103">IAnalysisRegion :: GetRegionScans, méthode</span><span class="sxs-lookup"><span data-stu-id="828e3-103">IAnalysisRegion::GetRegionScans method</span></span>

<span data-ttu-id="828e3-104">Récupère un tableau de rectangles qui définit la zone du [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="828e3-104">Retrieves an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="828e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="828e3-105">Syntax</span></span>


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a><span data-ttu-id="828e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="828e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="828e3-107">*pulCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="828e3-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="828e3-108">Nombre de rectangles retournés dans *pRegionScans*.</span><span class="sxs-lookup"><span data-stu-id="828e3-108">The number of rectangles returned in *pRegionScans*.</span></span>

</dd> <dt>

<span data-ttu-id="828e3-109">*pRegionScans* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="828e3-109">*pRegionScans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="828e3-110">Pointeur vers un tableau de rectangles qui définit la zone du [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="828e3-110">A pointer to an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="828e3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="828e3-111">Return value</span></span>

<span data-ttu-id="828e3-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="828e3-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="828e3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="828e3-113">Remarks</span></span>

<span data-ttu-id="828e3-114">Si *pRegionScans* est passé comme **null**, la méthode **GetRegionScans** retourne **S \_ OK** et le nombre de rectangles est retourné dans *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="828e3-114">If *pRegionScans* is passed as **NULL**, the **GetRegionScans** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="828e3-115">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *pRegionScans* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="828e3-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pRegionScans* when you no longer need the information.</span></span>

 

<span data-ttu-id="828e3-116">Les limites des rectangles sont exprimées en coordonnées d’espace manuscrit.</span><span class="sxs-lookup"><span data-stu-id="828e3-116">The bounds of the rectangles are in ink-space coordinates.</span></span>

<span data-ttu-id="828e3-117">L’Union des rectangles retournés représente la zone du [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="828e3-117">The union of the returned rectangles represents the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="examples"></a><span data-ttu-id="828e3-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="828e3-118">Examples</span></span>

<span data-ttu-id="828e3-119">L’exemple suivant montre comment récupérer les rectangles qui définissent la zone du [**IAnalysisRegion**](ianalysisregion.md) `region` et comment récupérer uniquement le nombre de rectangles.</span><span class="sxs-lookup"><span data-stu-id="828e3-119">The following example shows how to get the rectangles that define the area of the [**IAnalysisRegion**](ianalysisregion.md), `region` and how to get only the number of rectangles.</span></span>


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="828e3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="828e3-120">Requirements</span></span>



| <span data-ttu-id="828e3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="828e3-121">Requirement</span></span> | <span data-ttu-id="828e3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="828e3-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="828e3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="828e3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="828e3-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="828e3-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="828e3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="828e3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="828e3-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="828e3-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="828e3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="828e3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="828e3-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="828e3-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="828e3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="828e3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="828e3-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="828e3-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="828e3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="828e3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828e3-132">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="828e3-132">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="828e3-133">**IAnalysisRegion :: GetBounds, méthode**</span><span class="sxs-lookup"><span data-stu-id="828e3-133">**IAnalysisRegion::GetBounds Method**</span></span>](ianalysisregion-getbounds.md)
</dt> <dt>

[<span data-ttu-id="828e3-134">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="828e3-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

