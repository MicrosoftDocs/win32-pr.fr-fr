---
description: Se produit après que le IInkAnalyzer a créé un objet IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: '_IAnalysisProxyEvents :: ContextNodeCreated, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103953489"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a><span data-ttu-id="f7a20-103">\_Événement IAnalysisProxyEvents :: ContextNodeCreated</span><span class="sxs-lookup"><span data-stu-id="f7a20-103">\_IAnalysisProxyEvents::ContextNodeCreated event</span></span>

<span data-ttu-id="f7a20-104">Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a créé un objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f7a20-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7a20-105">Syntax</span></span>


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="f7a20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7a20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a20-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7a20-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a20-108">[**IInkAnalyzer**](iinkanalyzer.md) créant l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f7a20-108">The [**IInkAnalyzer**](iinkanalyzer.md) creating the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f7a20-109">*pContextNodeCreated* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7a20-109">*pContextNodeCreated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a20-110">Nouvel objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f7a20-110">The new [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a20-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7a20-111">Return value</span></span>

<span data-ttu-id="f7a20-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="f7a20-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a20-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f7a20-113">Remarks</span></span>

<span data-ttu-id="f7a20-114">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="f7a20-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="f7a20-115">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui crée un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="f7a20-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that creates an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="f7a20-116">Lorsque le [**IInkAnalyzer**](iinkanalyzer.md) crée un [**IContextNode**](icontextnode.md), le nouveau **IContextNode** ne contient aucun trait, ne contient pas de liens vers d’autres objets **IContextNode** et peut ne pas avoir toutes ses propriétés définies.</span><span class="sxs-lookup"><span data-stu-id="f7a20-116">When the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md), the new **IContextNode** does not contain any strokes, does not contain links to other **IContextNode** objects, and may not have all of its properties set.</span></span> <span data-ttu-id="f7a20-117">En outre, le nouveau **IContextNode** est ajouté à la fin de la collection de sous-nœuds du nœud parent (consultez [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="f7a20-117">Also, the new **IContextNode** is added to the end of its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="f7a20-118">Après cet événement, **IInkAnalyzer** peut déclencher les événements suivants.</span><span class="sxs-lookup"><span data-stu-id="f7a20-118">After this event, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="f7a20-119">L’événement [**\_ IAnalysisProxyEvents :: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) lorsqu’il déplace un trait d’un nœud de contexte à un autre.</span><span class="sxs-lookup"><span data-stu-id="f7a20-119">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from one context node to another.</span></span>
-   <span data-ttu-id="f7a20-120">L’événement [**\_ IAnalysisProxyEvents :: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) lorsqu’il ajoute un [**IContextLink**](icontextlink.md) à un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="f7a20-120">The [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) event when it adds an [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="f7a20-121">L’événement [**\_ IAnalysisProxyEvents :: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) lors de la modification de l’ordre d’un [**IContextNode**](icontextnode.md) dans la collection de sous-nœuds du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="f7a20-121">The [**\_IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) event when it changes the order of an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes.</span></span>
-   <span data-ttu-id="f7a20-122">[**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement [**\_ IAnalysisProxyEvents :: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) une fois qu’il a résolu l’état du [**IContextNode**](icontextnode.md) pour cette phase d’analyse.</span><span class="sxs-lookup"><span data-stu-id="f7a20-122">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) event after it resolves the state of the [**IContextNode**](icontextnode.md) for this analysis phase.</span></span>

<span data-ttu-id="f7a20-123">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f7a20-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a20-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7a20-124">Requirements</span></span>



| <span data-ttu-id="f7a20-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7a20-125">Requirement</span></span> | <span data-ttu-id="f7a20-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7a20-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a20-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7a20-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a20-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7a20-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f7a20-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7a20-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a20-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7a20-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f7a20-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7a20-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7a20-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f7a20-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f7a20-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f7a20-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7a20-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7a20-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f7a20-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7a20-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a20-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="f7a20-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="f7a20-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f7a20-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f7a20-138">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f7a20-138">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f7a20-139">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="f7a20-139">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="f7a20-140">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="f7a20-140">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="f7a20-141">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="f7a20-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




