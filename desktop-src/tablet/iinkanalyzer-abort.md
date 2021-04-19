---
description: Annule l’opération d’analyse en cours.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'IInkAnalyzer :: Abort, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515044"
---
# <a name="iinkanalyzerabort-method"></a><span data-ttu-id="a5145-103">IInkAnalyzer :: Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="a5145-103">IInkAnalyzer::Abort method</span></span>

<span data-ttu-id="a5145-104">Annule l’opération d’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="a5145-104">Cancels the current analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5145-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5145-105">Syntax</span></span>


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="a5145-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5145-107">*ppAbortedRegion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a5145-107">*ppAbortedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5145-108">Pointeur vers un [**IAnalysisRegion**](ianalysisregion.md) qui représente la région modifiée (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) de l’opération d’analyse actuelle.</span><span class="sxs-lookup"><span data-stu-id="a5145-108">A pointer to an [**IAnalysisRegion**](ianalysisregion.md) that represents the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) of the current analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5145-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5145-109">Return value</span></span>

<span data-ttu-id="a5145-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a5145-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5145-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a5145-111">Remarks</span></span>

<span data-ttu-id="a5145-112">Appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAbortedRegion* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="a5145-112">Call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAbortedRegion* when you no longer need to use the object.</span></span>

<span data-ttu-id="a5145-113">Cette méthode annule l’opération d’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="a5145-113">This method cancels the current analysis operation.</span></span>

<span data-ttu-id="a5145-114">Quand *ppAbortedRegion* a la valeur **null**, cette méthode effectue l’abandon comme normal, car cela indique que l’appelant n’a aucun intérêt dans la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a5145-114">When *ppAbortedRegion* is **NULL**, this method performs the abort as normal, because this indicates that the caller has no interest in the return value.</span></span>

<span data-ttu-id="a5145-115">La **méthode IInkAnalyzer :: Abort** interrompt les événements [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) et [**\_ IAnalysisEvents :: Activity**](-ianalysisevents-activity.md) pour l’opération d’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="a5145-115">**IInkAnalyzer::Abort Method** silences the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::Activity**](-ianalysisevents-activity.md) events for the current analysis operation.</span></span>

<span data-ttu-id="a5145-116">La **méthode IInkAnalyzer :: Abort** s’exécute de façon asynchrone jusqu’à ce que l’opération d’analyse en arrière-plan actuelle soit annulée.</span><span class="sxs-lookup"><span data-stu-id="a5145-116">**IInkAnalyzer::Abort Method** runs asynchronously until the current background analysis operation is canceled.</span></span> <span data-ttu-id="a5145-117">Étant donné que le processus d’annulation est asynchrone, l’application peut effectuer d’autres tâches pendant que l’analyse vers actuelle est annulée.</span><span class="sxs-lookup"><span data-stu-id="a5145-117">Because the cancellation process is asynchronous, the application can perform other tasks while the current analysis opertions is canceled.</span></span>

<span data-ttu-id="a5145-118">Si aucune opération d’analyse n’est en cours, cette méthode retourne une région d’analyse vide.</span><span class="sxs-lookup"><span data-stu-id="a5145-118">If no analysis operations are in progress, this method returns an empty analysis region.</span></span>

<span data-ttu-id="a5145-119">Si une opération d’analyse est en cours, cette méthode annule l’opération.</span><span class="sxs-lookup"><span data-stu-id="a5145-119">If one analysis operation is in progress, this method cancels the operation.</span></span>

<span data-ttu-id="a5145-120">Si les opérations d’analyse synchrones et asynchrones sont en cours, cette méthode annule l’opération synchrone.</span><span class="sxs-lookup"><span data-stu-id="a5145-120">If both synchronous and asynchronous analysis operations are in progress, this method cancels the synchronous operation.</span></span>

<span data-ttu-id="a5145-121">Si cette méthode est appelée plusieurs fois pour la même opération d’analyse, le premier appel retourne la région modifiée pour l’opération, et les appels suivants retournent une région vide.</span><span class="sxs-lookup"><span data-stu-id="a5145-121">If this method is called more than once for the same analysis operation, the first call returns the dirty region for the operation, and the subsequent calls return an empty region.</span></span>

<span data-ttu-id="a5145-122">Si votre application gère sa propre structure de données qui est synchronisée avec celle de [**IInkAnalyzer**](iinkanalyzer.md), l’appel de la **méthode IInkAnalyzer :: Abort** peut conserver votre document avec des résultats partiels.</span><span class="sxs-lookup"><span data-stu-id="a5145-122">If your application maintains its own data structure that is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), calling **IInkAnalyzer::Abort Method** can leave your document with partial results.</span></span> <span data-ttu-id="a5145-123">Pour éviter cela, n’appelez pas la **méthode IInkAnalyzer :: Abort** entre le moment où le **IInkAnalyzer** reçoit l’événement [**\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) et l’heure à laquelle le **IInkAnalyzer** reçoit l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="a5145-123">To avoid this, do not call **IInkAnalyzer::Abort Method** between the time the **IInkAnalyzer** receives the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event and the time the **IInkAnalyzer** receives the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="a5145-124">Pour plus d’informations sur la synchronisation de vos données d’application avec l’analyseur d’encre, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a5145-124">For more information about synchronizing your application data with the ink analyzer, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5145-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5145-125">Requirements</span></span>



| <span data-ttu-id="a5145-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5145-126">Requirement</span></span> | <span data-ttu-id="a5145-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5145-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5145-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5145-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a5145-129">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5145-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a5145-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5145-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a5145-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5145-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a5145-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5145-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5145-133"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a5145-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a5145-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a5145-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5145-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5145-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a5145-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5145-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5145-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a5145-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a5145-138">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="a5145-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a5145-139">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="a5145-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a5145-140">**IInkAnalyzer :: GetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="a5145-140">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="a5145-141">**IInkAnalyzer :: SetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="a5145-141">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="a5145-142">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a5145-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

