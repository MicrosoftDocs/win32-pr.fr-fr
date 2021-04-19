---
description: Se produit lorsque l’étape d’analyse intermédiaire actuelle est terminée.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: '_IAnalysisEvents :: IntermediateResults, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106542105"
---
# <a name="_ianalysiseventsintermediateresults-event"></a><span data-ttu-id="d41ba-103">\_Événement IAnalysisEvents :: IntermediateResults</span><span class="sxs-lookup"><span data-stu-id="d41ba-103">\_IAnalysisEvents::IntermediateResults event</span></span>

<span data-ttu-id="d41ba-104">Se produit lorsque l’étape d’analyse intermédiaire actuelle est terminée.</span><span class="sxs-lookup"><span data-stu-id="d41ba-104">Occurs when the current intermediate analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41ba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d41ba-105">Syntax</span></span>


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d41ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d41ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41ba-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d41ba-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d41ba-108">[**IInkAnalyzer**](iinkanalyzer.md) qui effectue l’analyse.</span><span class="sxs-lookup"><span data-stu-id="d41ba-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is performing the analysis.</span></span>

</dd> <dt>

<span data-ttu-id="d41ba-109">*pAnalysisStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d41ba-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d41ba-110">Objet [**IAnalysisStatus**](ianalysisstatus.md) représentant l’état des résultats intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="d41ba-110">The [**IAnalysisStatus**](ianalysisstatus.md) object representing the status of the intermediate results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d41ba-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d41ba-111">Return value</span></span>

<span data-ttu-id="d41ba-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="d41ba-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d41ba-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d41ba-113">Remarks</span></span>

<span data-ttu-id="d41ba-114">Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement après qu’il a concilié les résultats intermédiaires pour l’étape d’analyse actuelle.</span><span class="sxs-lookup"><span data-stu-id="d41ba-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the intermediate results for the current analysis stage.</span></span>

<span data-ttu-id="d41ba-115">Si votre application gère sa propre structure de données, qui est synchronisée avec celle de [**IInkAnalyzer**](iinkanalyzer.md), cet événement indique que le **IInkAnalyzer** a terminé d’apporter des modifications à ses données internes pour cette étape d’analyse.</span><span class="sxs-lookup"><span data-stu-id="d41ba-115">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="d41ba-116">Verrouillez votre structure de données lorsque [**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement [**\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="d41ba-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="d41ba-117">Les modifications apportées à la structure de vos données au cours de cette phase d’analyse peuvent entraîner des erreurs dans l’analyse et la synchronisation de l’encre.</span><span class="sxs-lookup"><span data-stu-id="d41ba-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="d41ba-118">Vous pouvez déverrouiller votre structure de données lorsque **IInkAnalyzer** déclenche l’événement **\_ IAnalysisEvents :: IntermediateResults** ou [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="d41ba-118">You can unlock your data structure when the **IInkAnalyzer** raises the **\_IAnalysisEvents::IntermediateResults** or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="d41ba-119">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d41ba-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="d41ba-120">[**IInkAnalyzer**](iinkanalyzer.md) génère des résultats intermédiaires uniquement lorsque l’indicateur **AnalysisModes \_ IntermediateResults** est défini pour ses modes d’analyse (consultez [**méthode IInkAnalyzer :: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="d41ba-120">The [**IInkAnalyzer**](iinkanalyzer.md) generates intermediate results only when its analysis modes has the **AnalysisModes\_IntermediateResults** flag set (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d41ba-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d41ba-121">Requirements</span></span>



| <span data-ttu-id="d41ba-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d41ba-122">Requirement</span></span> | <span data-ttu-id="d41ba-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d41ba-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d41ba-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d41ba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d41ba-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d41ba-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d41ba-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d41ba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d41ba-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d41ba-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d41ba-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d41ba-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d41ba-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d41ba-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d41ba-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d41ba-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d41ba-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d41ba-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d41ba-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d41ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41ba-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="d41ba-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="d41ba-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="d41ba-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="d41ba-135">**\_IAnalysisEvents :: Results**</span><span class="sxs-lookup"><span data-stu-id="d41ba-135">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="d41ba-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="d41ba-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d41ba-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d41ba-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d41ba-138">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="d41ba-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d41ba-139">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="d41ba-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d41ba-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="d41ba-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>
