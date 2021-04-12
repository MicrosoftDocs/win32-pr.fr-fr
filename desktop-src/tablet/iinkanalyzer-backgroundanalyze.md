---
description: Effectue une analyse d’encre asynchrone.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'IInkAnalyzer :: BackgroundAnalyze, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526505"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a><span data-ttu-id="b7feb-103">IInkAnalyzer :: BackgroundAnalyze, méthode</span><span class="sxs-lookup"><span data-stu-id="b7feb-103">IInkAnalyzer::BackgroundAnalyze method</span></span>

<span data-ttu-id="b7feb-104">Effectue une analyse d’encre asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b7feb-104">Performs asynchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7feb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7feb-105">Syntax</span></span>


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a><span data-ttu-id="b7feb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7feb-106">Parameters</span></span>

<span data-ttu-id="b7feb-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b7feb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7feb-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7feb-108">Return value</span></span>

<span data-ttu-id="b7feb-109">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b7feb-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7feb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b7feb-110">Remarks</span></span>

<span data-ttu-id="b7feb-111">Lorsque cette méthode est appelée, le [**IInkAnalyzer**](iinkanalyzer.md) effectue l’analyse de l’encre sur un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b7feb-111">When this method is called, the [**IInkAnalyzer**](iinkanalyzer.md) performs the ink analysis on a background thread.</span></span>

<span data-ttu-id="b7feb-112">Cette méthode retourne **S \_ false** et ne démarre pas une nouvelle opération d’analyse en arrière-plan dans les circonstances suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7feb-112">This method returns **S\_FALSE** and does not start a new background analysis operation under the following circumstances.</span></span>

-   <span data-ttu-id="b7feb-113">[**IInkAnalyzer**](iinkanalyzer.md) effectue actuellement une analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b7feb-113">The [**IInkAnalyzer**](iinkanalyzer.md) is currently performing background analysis.</span></span>
-   <span data-ttu-id="b7feb-114">la région modifiée (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) représente une zone vide.</span><span class="sxs-lookup"><span data-stu-id="b7feb-114">the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) represents an empty area.</span></span>

<span data-ttu-id="b7feb-115">Le [**IInkAnalyzer**](iinkanalyzer.md) analyse l’encre au sein de sa région modifiée pendant un appel à la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou à la **méthode IInkAnalyzer :: BackgroundAnalyze**.</span><span class="sxs-lookup"><span data-stu-id="b7feb-115">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or **IInkAnalyzer::BackgroundAnalyze Method**.</span></span> <span data-ttu-id="b7feb-116">Toutefois, le **IInkAnalyzer** peut développer l’opération d’analyse pour inclure les régions voisines.</span><span class="sxs-lookup"><span data-stu-id="b7feb-116">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="b7feb-117">Cette méthode définit la région de modification sur une zone vide.</span><span class="sxs-lookup"><span data-stu-id="b7feb-117">This method sets the dirty region to an empty region.</span></span>

<span data-ttu-id="b7feb-118">Si les données de trait ont été ajoutées au [**IInkAnalyzer**](iinkanalyzer.md) après l’appel de la **méthode IInkAnalyzer :: BackgroundAnalyze**, le **IInkAnalyzer** peut mettre à jour la région modifiée pendant la phase de rapprochement de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b7feb-118">If stroke data was added to the [**IInkAnalyzer**](iinkanalyzer.md) after the call to **IInkAnalyzer::BackgroundAnalyze Method**, the **IInkAnalyzer** may update the dirty region during the reconcile phase of ink analysis.</span></span>

<span data-ttu-id="b7feb-119">Le paramètre des modes d’analyse (consultez la [**méthode IInkAnalyzer :: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)) spécifie la manière dont le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b7feb-119">The analysis modes setting (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs background analysis.</span></span> <span data-ttu-id="b7feb-120">Pour plus d’informations sur l’analyse des encres, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b7feb-120">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

<span data-ttu-id="b7feb-121">Cette méthode retourne un code d’erreur dans les circonstances suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7feb-121">This method returns an error code under the following circumstances.</span></span>

-   <span data-ttu-id="b7feb-122">Votre application a défini la valeur [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults** dans le [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) et ne gère pas l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) .</span><span class="sxs-lookup"><span data-stu-id="b7feb-122">Your application has set [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_IntermediateResults** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) event.</span></span>
-   <span data-ttu-id="b7feb-123">Votre application a effacé la valeur [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** dans le [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) et ne gère pas l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="b7feb-123">Your application has cleared [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_AutomaticReconciliation** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>
-   <span data-ttu-id="b7feb-124">Votre application ne gère pas l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="b7feb-124">Your application does not handle the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>
-   <span data-ttu-id="b7feb-125">Votre application ne gère pas l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="b7feb-125">Your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

## <a name="examples"></a><span data-ttu-id="b7feb-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7feb-126">Examples</span></span>

<span data-ttu-id="b7feb-127">L’exemple suivant vérifie la région de modification de l’analyseur d’encre, puis lance l’analyse de l’encre en arrière-plan si la région modifiée n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="b7feb-127">The following example checks the ink analyzer's dirty region, and then initiates background ink analysis if the dirty region is not empty.</span></span>


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



## <a name="requirements"></a><span data-ttu-id="b7feb-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7feb-128">Requirements</span></span>



| <span data-ttu-id="b7feb-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7feb-129">Requirement</span></span> | <span data-ttu-id="b7feb-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7feb-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7feb-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7feb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b7feb-132">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7feb-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7feb-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7feb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b7feb-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7feb-134">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b7feb-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7feb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7feb-136"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b7feb-136"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b7feb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b7feb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7feb-138"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7feb-138"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b7feb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7feb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7feb-140">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b7feb-140">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b7feb-141">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="b7feb-141">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="b7feb-142">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="b7feb-142">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b7feb-143">**IInkAnalyzer :: GetAnalysisModes, méthode**</span><span class="sxs-lookup"><span data-stu-id="b7feb-143">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="b7feb-144">**IInkAnalyzer :: SetAnalysisModes, méthode**</span><span class="sxs-lookup"><span data-stu-id="b7feb-144">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="b7feb-145">**IInkAnalyzer :: GetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="b7feb-145">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="b7feb-146">**IInkAnalyzer :: SetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="b7feb-146">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="b7feb-147">**IInkAnalyzer :: GetRootNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="b7feb-147">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="b7feb-148">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b7feb-148">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




