---
description: Se produit lorsque le IInkAnalyzer est prêt à rapprocher les résultats de l’analyse en arrière-plan avec son état actuel.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: '_IAnalysisEvents :: ReadyToReconcile, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211297"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a><span data-ttu-id="5f5cd-103">\_Événement IAnalysisEvents :: ReadyToReconcile</span><span class="sxs-lookup"><span data-stu-id="5f5cd-103">\_IAnalysisEvents::ReadyToReconcile event</span></span>

<span data-ttu-id="5f5cd-104">Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) est prêt à rapprocher les résultats de l’analyse en arrière-plan avec son état actuel.</span><span class="sxs-lookup"><span data-stu-id="5f5cd-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f5cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f5cd-105">Syntax</span></span>


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a><span data-ttu-id="5f5cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f5cd-106">Parameters</span></span>

<span data-ttu-id="5f5cd-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5f5cd-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f5cd-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f5cd-108">Return value</span></span>

<span data-ttu-id="5f5cd-109">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="5f5cd-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f5cd-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5f5cd-110">Remarks</span></span>

<span data-ttu-id="5f5cd-111">Le [**IInkAnalyzer**](iinkanalyzer.md) effectue un rapprochement automatique lorsque l’indicateur **\_ AutomaticReconciliation AnalysisModes** de l’analyseur d’encre est défini (consultez [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="5f5cd-111">The [**IInkAnalyzer**](iinkanalyzer.md) performs automatic reconciliation when the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag is set (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)).</span></span> <span data-ttu-id="5f5cd-112">Lorsque l’indicateur **AnalysisModes \_ AutomaticReconciliation** n’est pas défini, votre application doit rapprocher manuellement les résultats de l’analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5f5cd-112">When the **AnalysisModes\_AutomaticReconciliation** flag is not set, your application needs to reconcile background analysis results manually.</span></span>

<span data-ttu-id="5f5cd-113">Pour effectuer un rapprochement manuel, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="5f5cd-113">To perform manual reconciliation, follow these steps.</span></span>

1.  <span data-ttu-id="5f5cd-114">Effacez l’indicateur **AnalysisModes \_ AutomaticReconciliation** de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="5f5cd-114">Clear the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag.</span></span>
2.  <span data-ttu-id="5f5cd-115">Gérez l’événement **\_ IAnalysisEvents :: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="5f5cd-115">Handle the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>
3.  <span data-ttu-id="5f5cd-116">Pour rapprocher les résultats de l’analyse, appelez la méthode [**IInkAnalyzer :: rapprochee**](iinkanalyzer-reconcile.md) de la méthode à partir du gestionnaire d’événements pour l’événement **\_ IAnalysisEvents :: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="5f5cd-116">To reconcile the analysis results, call the [**IInkAnalyzer::Reconcile Method**](iinkanalyzer-reconcile.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span> <span data-ttu-id="5f5cd-117">Pour annuler l’opération d’analyse en arrière-plan actuelle, appelez la méthode de [**méthode IInkAnalyzer :: Abort**](iinkanalyzer-abort.md) à partir du gestionnaire d’événements pour l’événement **\_ IAnalysisEvents :: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="5f5cd-117">To cancel the current background analysis operation, call the [**IInkAnalyzer::Abort Method**](iinkanalyzer-abort.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>

<span data-ttu-id="5f5cd-118">Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement avant de déclencher l’événement [**\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="5f5cd-118">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event before it raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span>

<span data-ttu-id="5f5cd-119">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5f5cd-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="5f5cd-120">Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement lors de l’analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5f5cd-120">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during background analysis.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5cd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f5cd-121">Requirements</span></span>



| <span data-ttu-id="5f5cd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f5cd-122">Requirement</span></span> | <span data-ttu-id="5f5cd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f5cd-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5cd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f5cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5cd-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f5cd-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f5cd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f5cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5cd-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f5cd-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5f5cd-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f5cd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5cd-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5f5cd-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5f5cd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5f5cd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f5cd-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f5cd-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5f5cd-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f5cd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5cd-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="5f5cd-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="5f5cd-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="5f5cd-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="5f5cd-135">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="5f5cd-135">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="5f5cd-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5f5cd-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5f5cd-137">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="5f5cd-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="5f5cd-138">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="5f5cd-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5f5cd-139">**IInkAnalyzer :: Reconcile, méthode**</span><span class="sxs-lookup"><span data-stu-id="5f5cd-139">**IInkAnalyzer::Reconcile Method**</span></span>](iinkanalyzer-reconcile.md)
</dt> <dt>

[<span data-ttu-id="5f5cd-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="5f5cd-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




