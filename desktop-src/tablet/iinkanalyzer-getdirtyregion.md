---
description: Récupère la zone qui a été modifiée depuis la dernière opération d’analyse.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'IInkAnalyzer :: GetDirtyRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201499"
---
# <a name="iinkanalyzergetdirtyregion-method"></a><span data-ttu-id="475d4-103">IInkAnalyzer :: GetDirtyRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="475d4-103">IInkAnalyzer::GetDirtyRegion method</span></span>

<span data-ttu-id="475d4-104">Récupère la zone qui a été modifiée depuis la dernière opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="475d4-104">Retrieves the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="475d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="475d4-105">Syntax</span></span>


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="475d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="475d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="475d4-107">*ppDirtyRegion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="475d4-107">*ppDirtyRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="475d4-108">[**IAnalysisRegion**](ianalysisregion.md) qui décrit la zone qui a été modifiée depuis la dernière opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="475d4-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="475d4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="475d4-109">Return value</span></span>

<span data-ttu-id="475d4-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="475d4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="475d4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="475d4-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="475d4-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppDirtyRegion* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="475d4-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppDirtyRegion* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="475d4-113">Cette méthode identifie les zones qui doivent être analysées ou réanalysées.</span><span class="sxs-lookup"><span data-stu-id="475d4-113">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="475d4-114">Toutes les méthodes [**IInkAnalyzer**](iinkanalyzer.md) qui ajoutent, mettent à jour ou suppriment des données de trait mettent à jour la région modifiée.</span><span class="sxs-lookup"><span data-stu-id="475d4-114">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="475d4-115">Pour marquer manuellement une zone pour la réanalyse :</span><span class="sxs-lookup"><span data-stu-id="475d4-115">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="475d4-116">Récupérez la région modifiée à l’aide de la **méthode IInkAnalyzer :: GetDirtyRegion**.</span><span class="sxs-lookup"><span data-stu-id="475d4-116">Get the dirty region using **IInkAnalyzer::GetDirtyRegion Method**.</span></span>
2.  <span data-ttu-id="475d4-117">Utilisez la méthode [**IAnalysisRegion :: UnionRegion**](ianalysisregion-unionregion.md) ou [**IAnalysisRegion :: UnionRectangle**](ianalysisregion-unionrectangle.md) pour ajouter la zone à la région à partir de l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="475d4-117">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="475d4-118">Utilisez la [**méthode IInkAnalyzer :: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) pour mettre à jour la région modifiée.</span><span class="sxs-lookup"><span data-stu-id="475d4-118">Use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to update the dirty region.</span></span>

<span data-ttu-id="475d4-119">Le [**IInkAnalyzer**](iinkanalyzer.md) analyse l’encre au sein de sa région modifiée pendant un appel à la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou à la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="475d4-119">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="475d4-120">Toutefois, le **IInkAnalyzer** peut développer l’opération d’analyse pour inclure les régions voisines.</span><span class="sxs-lookup"><span data-stu-id="475d4-120">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="475d4-121">Cette propriété peut contenir des zones non adjacentes.</span><span class="sxs-lookup"><span data-stu-id="475d4-121">This property may contain nonadjacent areas.</span></span>

<span data-ttu-id="475d4-122">Utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire du tableau *ppDirtyRegion* lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="475d4-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory from the *ppDirtyRegion* array when you are finished with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="475d4-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="475d4-123">Requirements</span></span>



| <span data-ttu-id="475d4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="475d4-124">Requirement</span></span> | <span data-ttu-id="475d4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="475d4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="475d4-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="475d4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="475d4-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="475d4-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="475d4-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="475d4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="475d4-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="475d4-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="475d4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="475d4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="475d4-131"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="475d4-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="475d4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="475d4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="475d4-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="475d4-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="475d4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="475d4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475d4-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="475d4-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="475d4-136">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="475d4-137">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="475d4-138">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-138">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="475d4-139">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-139">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="475d4-140">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-140">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="475d4-141">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-141">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="475d4-142">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-142">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="475d4-143">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-143">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="475d4-144">**IInkAnalyzer :: UpdateStrokesData, méthode**</span><span class="sxs-lookup"><span data-stu-id="475d4-144">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="475d4-145">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="475d4-145">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

