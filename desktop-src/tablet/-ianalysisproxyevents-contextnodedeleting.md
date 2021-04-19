---
description: Se produit avant que le IInkAnalyzer supprime un objet IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: '_IAnalysisProxyEvents :: ContextNodeDeleting, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106543009"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a><span data-ttu-id="3081d-103">\_Événement IAnalysisProxyEvents :: ContextNodeDeleting</span><span class="sxs-lookup"><span data-stu-id="3081d-103">\_IAnalysisProxyEvents::ContextNodeDeleting event</span></span>

<span data-ttu-id="3081d-104">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) supprime un objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3081d-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3081d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3081d-105">Syntax</span></span>


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="3081d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3081d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3081d-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3081d-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3081d-108">Objet [**IInkAnalyzer**](iinkanalyzer.md) qui supprime l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3081d-108">The [**IInkAnalyzer**](iinkanalyzer.md) object deleting the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3081d-109">*pContextNodeToBeDeleted* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3081d-109">*pContextNodeToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3081d-110">Objet [**IContextNode**](icontextnode.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3081d-110">The [**IContextNode**](icontextnode.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3081d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3081d-111">Return value</span></span>

<span data-ttu-id="3081d-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3081d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3081d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3081d-113">Remarks</span></span>

<span data-ttu-id="3081d-114">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3081d-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="3081d-115">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui supprime un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="3081d-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that deletes an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="3081d-116">Avant que [**IInkAnalyzer**](iinkanalyzer.md) ne supprime un [**IContextNode**](icontextnode.md), le **IInkAnalyzer** supprime tous les traits du nœud de contexte et supprime tous les liens vers d’autres nœuds de contexte.</span><span class="sxs-lookup"><span data-stu-id="3081d-116">Before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md), the **IInkAnalyzer** removes all of the strokes from the context node and removes all of the links to other context nodes.</span></span> <span data-ttu-id="3081d-117">Avant de supprimer le nœud de contexte, **IInkAnalyzer** peut déclencher les événements suivants.</span><span class="sxs-lookup"><span data-stu-id="3081d-117">Before the context node is removed, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="3081d-118">L’événement [**\_ IAnalysisProxyEvents :: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) lorsqu’il déplace un trait du [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="3081d-118">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="3081d-119">L’événement [**\_ IAnalysisProxyEvents :: ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) avant de supprimer un [**IContextLink**](icontextlink.md) du [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="3081d-119">The [**\_IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) event before it removes a [**IContextLink**](icontextlink.md) from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="3081d-120">L’événement **\_ IAnalysisProxyEvents :: ContextNodeDeleting** avant de supprimer un nœud de contexte parent qui n’a plus de nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="3081d-120">The **\_IAnalysisProxyEvents::ContextNodeDeleting** event before it removes a parent context node that no longer has child nodes.</span></span>

<span data-ttu-id="3081d-121">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3081d-121">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3081d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3081d-122">Requirements</span></span>



| <span data-ttu-id="3081d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3081d-123">Requirement</span></span> | <span data-ttu-id="3081d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3081d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3081d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3081d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3081d-126">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3081d-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3081d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3081d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3081d-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3081d-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3081d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3081d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3081d-130"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3081d-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3081d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3081d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3081d-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3081d-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3081d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3081d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3081d-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="3081d-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="3081d-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3081d-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3081d-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3081d-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3081d-137">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="3081d-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="3081d-138">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="3081d-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="3081d-139">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3081d-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




