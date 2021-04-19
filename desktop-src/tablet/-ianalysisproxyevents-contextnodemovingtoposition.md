---
description: Se produit avant que le IInkAnalyzer déplace un objet IContextNode vers une nouvelle position dans la collection de sous-nœuds du nœud parent.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: '_IAnalysisProxyEvents :: ContextNodeMovingToPosition, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531462"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a><span data-ttu-id="b4f8e-103">\_Événement IAnalysisProxyEvents :: ContextNodeMovingToPosition</span><span class="sxs-lookup"><span data-stu-id="b4f8e-103">\_IAnalysisProxyEvents::ContextNodeMovingToPosition event</span></span>

<span data-ttu-id="b4f8e-104">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) déplace un objet [**IContextNode**](icontextnode.md) vers une nouvelle position dans la collection de sous-nœuds du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b4f8e-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4f8e-105">Syntax</span></span>


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b4f8e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4f8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f8e-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4f8e-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f8e-108">Objet [**IInkAnalyzer**](iinkanalyzer.md) qui déplace l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b4f8e-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b4f8e-109">*pISubNodeToMove* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4f8e-109">*pISubNodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f8e-110">Objet [**IContextNode**](icontextnode.md) à déplacer.</span><span class="sxs-lookup"><span data-stu-id="b4f8e-110">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="b4f8e-111">*pParentContextNode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4f8e-111">*pParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f8e-112">Objet [**IContextNode**](icontextnode.md) parent de *pISubNodeToMove*.</span><span class="sxs-lookup"><span data-stu-id="b4f8e-112">The parent [**IContextNode**](icontextnode.md) object of *pISubNodeToMove*.</span></span>

</dd> <dt>

<span data-ttu-id="b4f8e-113">*ulNewIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4f8e-113">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f8e-114">Nouvel emplacement de *pISubNodeToMove* dans la collection de sous-nœuds du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b4f8e-114">The new location of *pISubNodeToMove* in its parent node's collection of subnodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f8e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4f8e-115">Return value</span></span>

<span data-ttu-id="b4f8e-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b4f8e-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4f8e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b4f8e-117">Remarks</span></span>

<span data-ttu-id="b4f8e-118">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b4f8e-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="b4f8e-119">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui déplace un [**IContextNode**](icontextnode.md) dans la collection de sous-nœuds du nœud parent (voir [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="b4f8e-119">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that moves an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="b4f8e-120">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b4f8e-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f8e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4f8e-121">Requirements</span></span>



| <span data-ttu-id="b4f8e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4f8e-122">Requirement</span></span> | <span data-ttu-id="b4f8e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f8e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f8e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4f8e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f8e-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4f8e-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4f8e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4f8e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f8e-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4f8e-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4f8e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4f8e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4f8e-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4f8e-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4f8e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b4f8e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4f8e-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4f8e-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4f8e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4f8e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f8e-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="b4f8e-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="b4f8e-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b4f8e-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b4f8e-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b4f8e-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b4f8e-136">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4f8e-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b4f8e-137">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4f8e-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b4f8e-138">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="b4f8e-138">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="b4f8e-139">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="b4f8e-139">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="b4f8e-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b4f8e-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




