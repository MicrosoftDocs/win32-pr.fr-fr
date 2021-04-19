---
description: Effectue une analyse de l’encre synchrone.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'IInkAnalyzer :: Analyze, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517510"
---
# <a name="iinkanalyzeranalyze-method"></a><span data-ttu-id="54513-103">IInkAnalyzer :: Analyze, méthode</span><span class="sxs-lookup"><span data-stu-id="54513-103">IInkAnalyzer::Analyze method</span></span>

<span data-ttu-id="54513-104">Effectue une analyse de l’encre synchrone.</span><span class="sxs-lookup"><span data-stu-id="54513-104">Performs synchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="54513-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54513-105">Syntax</span></span>


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a><span data-ttu-id="54513-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54513-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54513-107">*ppStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54513-107">*ppStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54513-108">Pointeur vers un [**IAnalysisStatus**](ianalysisstatus.md) qui décrit l’état de l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="54513-108">A pointer to an [**IAnalysisStatus**](ianalysisstatus.md) that describes the status of the analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54513-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54513-109">Return value</span></span>

<span data-ttu-id="54513-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="54513-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54513-111">Notes</span><span class="sxs-lookup"><span data-stu-id="54513-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="54513-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppStatus* lorsque vous n’avez plus besoin d’utiliser l’état d’analyse.</span><span class="sxs-lookup"><span data-stu-id="54513-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppStatus* when you no longer need to use the analysis status.</span></span>

 

<span data-ttu-id="54513-113">Cette méthode démarre une opération d’analyse d’encre synchrone.</span><span class="sxs-lookup"><span data-stu-id="54513-113">This method starts a synchronous ink analysis operation.</span></span> <span data-ttu-id="54513-114">L’analyse de l’encre comprend l’analyse de la disposition, l’écriture et la classification des dessins et la reconnaissance de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="54513-114">Ink analysis includes layout analysis, writing and drawing classification, and handwriting recognition.</span></span> <span data-ttu-id="54513-115">Cette méthode est retournée une fois l’opération d’analyse terminée.</span><span class="sxs-lookup"><span data-stu-id="54513-115">This method returns after the analysis operation is complete.</span></span>

<span data-ttu-id="54513-116">Cette méthode retourne **le \_ pointeur E** si *PpStatus* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="54513-116">This method returns **E\_POINTER** if *ppStatus* is **NULL**.</span></span>

<span data-ttu-id="54513-117">Pendant un appel à la méthode **IInkAnalyzer :: Analyze** ou à la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), le [**IInkAnalyzer**](iinkanalyzer.md) analyse l’encre au sein de sa région modifiée (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="54513-117">During a call to **IInkAnalyzer::Analyze Method** or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), the [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span> <span data-ttu-id="54513-118">Toutefois, le **IInkAnalyzer** peut développer l’opération d’analyse pour inclure les régions voisines.</span><span class="sxs-lookup"><span data-stu-id="54513-118">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="54513-119">Cette méthode définit la région de modification de l’objet [**IInkAnalyzer**](iinkanalyzer.md) sur une zone vide.</span><span class="sxs-lookup"><span data-stu-id="54513-119">This method sets the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region to an empty region.</span></span> <span data-ttu-id="54513-120">Si un autre thread a ajouté des données de trait qui n’ont pas été analysées, le **IInkAnalyzer** ajoute le cadre englobant des traits non analysés à sa région modifiée pendant la phase de rapprochement de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="54513-120">If another thread has added stroke data that has not been analyzed, the **IInkAnalyzer** adds the bounding box of the unanalyzed strokes to its dirty region during the reconcile phase of the analysis.</span></span>

<span data-ttu-id="54513-121">Cette méthode retourne une erreur si votre application ne gère pas l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="54513-121">This method returns an error if your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

<span data-ttu-id="54513-122">[**IInkAnalyzer**](iinkanalyzer.md) ne déclenche pas les événements [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) et [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) en réponse à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="54513-122">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) events in response to this method.</span></span>

<span data-ttu-id="54513-123">Pour modifier la façon dont l’analyse de l’encre est effectuée, utilisez la [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).</span><span class="sxs-lookup"><span data-stu-id="54513-123">To modify the way ink analysis is performed, use [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md).</span></span>

<span data-ttu-id="54513-124">Pour plus d’informations sur l’analyse des encres, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="54513-124">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54513-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="54513-125">Examples</span></span>

<span data-ttu-id="54513-126">L’exemple suivant effectue une analyse de l’encre de premier plan.</span><span class="sxs-lookup"><span data-stu-id="54513-126">The following example performs foreground ink analysis.</span></span>


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="54513-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54513-127">Requirements</span></span>



| <span data-ttu-id="54513-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54513-128">Requirement</span></span> | <span data-ttu-id="54513-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="54513-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54513-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54513-130">Minimum supported client</span></span><br/> | <span data-ttu-id="54513-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54513-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="54513-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54513-132">Minimum supported server</span></span><br/> | <span data-ttu-id="54513-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="54513-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="54513-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="54513-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="54513-135"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="54513-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="54513-136">DLL</span><span class="sxs-lookup"><span data-stu-id="54513-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54513-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54513-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="54513-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54513-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54513-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="54513-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="54513-140">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="54513-140">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="54513-141">**IInkAnalyzer :: GetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="54513-141">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="54513-142">**IInkAnalyzer :: SetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="54513-142">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="54513-143">**IInkAnalyzer :: GetRootNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="54513-143">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="54513-144">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="54513-144">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

