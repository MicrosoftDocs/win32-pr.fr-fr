---
description: Se produit avant que le IInkAnalyzer ne rapproche les résultats de l’analyse afin qu’une application puisse synchroniser les données avec le IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: '_IAnalysisProxyEvents :: InkAnalyzerStateChanging, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106524784"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a><span data-ttu-id="a2500-103">\_Événement IAnalysisProxyEvents :: InkAnalyzerStateChanging</span><span class="sxs-lookup"><span data-stu-id="a2500-103">\_IAnalysisProxyEvents::InkAnalyzerStateChanging event</span></span>

<span data-ttu-id="a2500-104">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) ne rapproche les résultats de l’analyse afin qu’une application puisse synchroniser les données avec le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="a2500-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2500-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2500-105">Syntax</span></span>


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a><span data-ttu-id="a2500-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2500-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2500-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2500-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2500-108">[**IInkAnalyzer**](iinkanalyzer.md) qui va rapprocher ses résultats d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a2500-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is about to reconcile its analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2500-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2500-109">Return value</span></span>

<span data-ttu-id="a2500-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a2500-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2500-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a2500-111">Remarks</span></span>

<span data-ttu-id="a2500-112">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a2500-112">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="a2500-113">Lorsque le **IInkAnalyzer** déclenche cet événement, votre application doit remplir les sous-nœuds du nœud racine de l’analyseur d’encre (consultez la méthode [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) et [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="a2500-113">When the **IInkAnalyzer** raises this event, your application should populate the subnodes of the ink analyzer's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="a2500-114">Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement après qu’il a déclenché l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="a2500-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="a2500-115">Il déclenche cet événement uniquement lors de l’analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a2500-115">It raises this event only while performing background analysis.</span></span>

<span data-ttu-id="a2500-116">Verrouillez votre structure de données lorsque [**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement **\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging** .</span><span class="sxs-lookup"><span data-stu-id="a2500-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the **\_IAnalysisProxyEvents::InkAnalyzerStateChanging** event.</span></span> <span data-ttu-id="a2500-117">Les modifications apportées à la structure de vos données au cours de cette phase d’analyse peuvent entraîner des erreurs dans l’analyse et la synchronisation de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a2500-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="a2500-118">Déverrouillez votre structure de données lorsque **IInkAnalyzer** déclenche l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="a2500-118">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="a2500-119">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a2500-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2500-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2500-120">Requirements</span></span>



| <span data-ttu-id="a2500-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2500-121">Requirement</span></span> | <span data-ttu-id="a2500-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2500-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2500-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2500-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2500-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2500-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2500-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2500-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2500-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2500-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a2500-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2500-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2500-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a2500-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a2500-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a2500-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2500-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2500-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a2500-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2500-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2500-132">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="a2500-132">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="a2500-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a2500-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a2500-134">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a2500-134">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a2500-135">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="a2500-135">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a2500-136">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="a2500-136">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a2500-137">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a2500-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




