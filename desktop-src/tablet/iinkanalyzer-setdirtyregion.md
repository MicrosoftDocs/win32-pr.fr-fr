---
description: Modifie la zone qui a été modifiée depuis la dernière opération d’analyse.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'IInkAnalyzer :: SetDirtyRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113323"
---
# <a name="iinkanalyzersetdirtyregion-method"></a><span data-ttu-id="ddff9-103">IInkAnalyzer :: SetDirtyRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="ddff9-103">IInkAnalyzer::SetDirtyRegion method</span></span>

<span data-ttu-id="ddff9-104">Modifie la zone qui a été modifiée depuis la dernière opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="ddff9-104">Modifies the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddff9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddff9-105">Syntax</span></span>


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="ddff9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddff9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddff9-107">*pDirtyRegion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ddff9-107">*pDirtyRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddff9-108">[**IAnalysisRegion**](ianalysisregion.md) qui décrit la zone qui a été modifiée depuis la dernière opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="ddff9-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddff9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddff9-109">Return value</span></span>

<span data-ttu-id="ddff9-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ddff9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ddff9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ddff9-111">Remarks</span></span>

<span data-ttu-id="ddff9-112">Cette méthode identifie les zones qui doivent être analysées ou réanalysées.</span><span class="sxs-lookup"><span data-stu-id="ddff9-112">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="ddff9-113">Toutes les méthodes [**IInkAnalyzer**](iinkanalyzer.md) qui ajoutent, mettent à jour ou suppriment des données de trait mettent à jour la région modifiée.</span><span class="sxs-lookup"><span data-stu-id="ddff9-113">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="ddff9-114">Pour marquer manuellement une zone pour la réanalyse :</span><span class="sxs-lookup"><span data-stu-id="ddff9-114">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="ddff9-115">Récupérez la région modifiée à l’aide de la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).</span><span class="sxs-lookup"><span data-stu-id="ddff9-115">Get the dirty region using [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md).</span></span>
2.  <span data-ttu-id="ddff9-116">Utilisez la méthode [**IAnalysisRegion :: UnionRegion**](ianalysisregion-unionregion.md) ou [**IAnalysisRegion :: UnionRectangle**](ianalysisregion-unionrectangle.md) pour ajouter la zone à la région à partir de l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ddff9-116">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="ddff9-117">Utilisez la **méthode IInkAnalyzer :: SetDirtyRegion** pour mettre à jour la région modifiée.</span><span class="sxs-lookup"><span data-stu-id="ddff9-117">Use **IInkAnalyzer::SetDirtyRegion Method** to update the dirty region.</span></span>

<span data-ttu-id="ddff9-118">Le [**IInkAnalyzer**](iinkanalyzer.md) analyse l’encre au sein de sa région modifiée pendant un appel à la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou à la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="ddff9-118">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="ddff9-119">Toutefois, le **IInkAnalyzer** peut développer l’opération d’analyse pour inclure les régions voisines.</span><span class="sxs-lookup"><span data-stu-id="ddff9-119">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddff9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddff9-120">Requirements</span></span>



| <span data-ttu-id="ddff9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddff9-121">Requirement</span></span> | <span data-ttu-id="ddff9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddff9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddff9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddff9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ddff9-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddff9-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ddff9-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddff9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ddff9-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddff9-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ddff9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddff9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddff9-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ddff9-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ddff9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ddff9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddff9-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddff9-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ddff9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddff9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddff9-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ddff9-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ddff9-133">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ddff9-134">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ddff9-135">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-135">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="ddff9-136">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-136">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="ddff9-137">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-137">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="ddff9-138">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-138">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="ddff9-139">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-139">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="ddff9-140">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-140">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="ddff9-141">**IInkAnalyzer :: UpdateStrokesData, méthode**</span><span class="sxs-lookup"><span data-stu-id="ddff9-141">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="ddff9-142">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="ddff9-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




