---
description: Se produit avant que le IInkAnalyzer effectue une analyse dans la région d’un objet IContextNode partiellement rempli.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents ::P événement opulateContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211304"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a><span data-ttu-id="fc304-103">\_IAnalysisProxyEvents ::P événement opulateContextNode</span><span class="sxs-lookup"><span data-stu-id="fc304-103">\_IAnalysisProxyEvents::PopulateContextNode event</span></span>

<span data-ttu-id="fc304-104">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse dans la région d’un objet [**IContextNode**](icontextnode.md) partiellement rempli.</span><span class="sxs-lookup"><span data-stu-id="fc304-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc304-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc304-105">Syntax</span></span>


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a><span data-ttu-id="fc304-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc304-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc304-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc304-108">Objet [**IInkAnalyzer**](iinkanalyzer.md) sur lequel exécuter l’analyse.</span><span class="sxs-lookup"><span data-stu-id="fc304-108">The [**IInkAnalyzer**](iinkanalyzer.md) object about to perform analysis.</span></span>

</dd> <dt>

<span data-ttu-id="fc304-109">*pContextNodeToPopulate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc304-109">*pContextNodeToPopulate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc304-110">Objet [**IContextNode**](icontextnode.md) partiellement rempli.</span><span class="sxs-lookup"><span data-stu-id="fc304-110">The partially populated [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc304-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc304-111">Return value</span></span>

<span data-ttu-id="fc304-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="fc304-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc304-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fc304-113">Remarks</span></span>

<span data-ttu-id="fc304-114">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="fc304-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="fc304-115">Lorsque le **IInkAnalyzer** déclenche cet événement, votre application doit remplir le *pContextNodeToPopulate*.</span><span class="sxs-lookup"><span data-stu-id="fc304-115">When the **IInkAnalyzer** raises this event, your application should populate the *pContextNodeToPopulate*.</span></span> <span data-ttu-id="fc304-116">Pendant la phase d’analyse, le **IInkAnalyzer** déclenche cet événement pour obtenir des informations sur les zones dans lesquelles il analyse l’encre.</span><span class="sxs-lookup"><span data-stu-id="fc304-116">During the analysis phase, the **IInkAnalyzer** raises this event to get information for areas in which it is analyzing ink.</span></span>

<span data-ttu-id="fc304-117">Si le document contient des liens pour le *pContextNodeToPopulate*, votre application doit créer et ajouter ces liens.</span><span class="sxs-lookup"><span data-stu-id="fc304-117">If the document contains links for the *pContextNodeToPopulate*, your application should create and add these links.</span></span> <span data-ttu-id="fc304-118">Ce processus requiert que les nœuds source et de destination, y compris leurs ancêtres, soient entièrement remplis avant que le gestionnaire d’événements de cet événement ne se termine (consultez [**IContextLink :: GetSourceNode**](icontextlink-getsourcenode.md) et [**IContextLink :: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="fc304-118">This process requires that both the source and destination nodes, including their ancestors, are fully populated before the event handler for this event exits (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span>

<span data-ttu-id="fc304-119">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fc304-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="fc304-120">Pendant l’analyse en arrière-plan, le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement après avoir déclenché l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="fc304-120">During background analysis, the [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc304-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc304-121">Requirements</span></span>



| <span data-ttu-id="fc304-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc304-122">Requirement</span></span> | <span data-ttu-id="fc304-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc304-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc304-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc304-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc304-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc304-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fc304-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc304-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc304-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc304-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fc304-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc304-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc304-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fc304-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fc304-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fc304-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc304-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc304-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fc304-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc304-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc304-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="fc304-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="fc304-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fc304-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fc304-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fc304-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fc304-136">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="fc304-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="fc304-137">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="fc304-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="fc304-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="fc304-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




