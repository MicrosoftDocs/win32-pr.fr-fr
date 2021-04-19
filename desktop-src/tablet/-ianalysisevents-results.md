---
description: Se produit lorsque l’étape d’analyse finale est terminée.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: '_IAnalysisEvents :: Results, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531463"
---
# <a name="_ianalysiseventsresults-event"></a><span data-ttu-id="3e04a-103">\_IAnalysisEvents :: Results, événement</span><span class="sxs-lookup"><span data-stu-id="3e04a-103">\_IAnalysisEvents::Results event</span></span>

<span data-ttu-id="3e04a-104">Se produit lorsque l’étape d’analyse finale est terminée.</span><span class="sxs-lookup"><span data-stu-id="3e04a-104">Occurs when the final analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e04a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e04a-105">Syntax</span></span>


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="3e04a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e04a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e04a-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e04a-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e04a-108">[**IInkAnalyzer**](iinkanalyzer.md) qui produit les résultats de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="3e04a-108">The [**IInkAnalyzer**](iinkanalyzer.md) that produces the analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="3e04a-109">*pAnalysisStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e04a-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e04a-110">Objet [**IAnalysisStatus**](ianalysisstatus.md) qui représente l’état de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="3e04a-110">The [**IAnalysisStatus**](ianalysisstatus.md) object that represents the status of the analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e04a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e04a-111">Return value</span></span>

<span data-ttu-id="3e04a-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3e04a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e04a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3e04a-113">Remarks</span></span>

<span data-ttu-id="3e04a-114">Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement après qu’il a concilié les résultats de l’étape d’analyse finale.</span><span class="sxs-lookup"><span data-stu-id="3e04a-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the results for the final analysis stage.</span></span>

<span data-ttu-id="3e04a-115">Si votre application appelle la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), cet événement signale que les résultats de l’analyse sont prêts.</span><span class="sxs-lookup"><span data-stu-id="3e04a-115">If your application calls [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), this event signals when analysis results are ready.</span></span>

<span data-ttu-id="3e04a-116">Si votre application gère sa propre structure de données, qui est synchronisée avec celle de [**IInkAnalyzer**](iinkanalyzer.md), cet événement indique que le **IInkAnalyzer** a terminé d’apporter des modifications à ses données internes pour cette étape d’analyse.</span><span class="sxs-lookup"><span data-stu-id="3e04a-116">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="3e04a-117">Verrouillez votre structure de données lorsque [**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement [**\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="3e04a-117">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="3e04a-118">Les modifications apportées à la structure de vos données au cours de cette phase d’analyse peuvent entraîner des erreurs dans l’analyse et la synchronisation de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3e04a-118">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="3e04a-119">Déverrouillez votre structure de données lorsque **IInkAnalyzer** déclenche l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou **\_ IAnalysisEvents :: Results** .</span><span class="sxs-lookup"><span data-stu-id="3e04a-119">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or **\_IAnalysisEvents::Results** event.</span></span>

<span data-ttu-id="3e04a-120">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3e04a-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e04a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e04a-121">Requirements</span></span>



| <span data-ttu-id="3e04a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e04a-122">Requirement</span></span> | <span data-ttu-id="3e04a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e04a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e04a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e04a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3e04a-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e04a-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e04a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e04a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3e04a-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e04a-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3e04a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e04a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e04a-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3e04a-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e04a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3e04a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e04a-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e04a-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3e04a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e04a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e04a-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="3e04a-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="3e04a-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="3e04a-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="3e04a-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3e04a-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3e04a-136">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="3e04a-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="3e04a-137">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="3e04a-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="3e04a-138">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="3e04a-138">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="3e04a-139">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3e04a-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




