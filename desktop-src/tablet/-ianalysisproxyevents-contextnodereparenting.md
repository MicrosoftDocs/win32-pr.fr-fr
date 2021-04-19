---
description: Se produit avant que le IInkAnalyzer déplace un objet IContextNode en modifiant son nœud parent.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: '_IAnalysisProxyEvents :: ContextNodeReparenting, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523764"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a><span data-ttu-id="3fd31-103">\_Événement IAnalysisProxyEvents :: ContextNodeReparenting</span><span class="sxs-lookup"><span data-stu-id="3fd31-103">\_IAnalysisProxyEvents::ContextNodeReparenting event</span></span>

<span data-ttu-id="3fd31-104">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) déplace un objet [**IContextNode**](icontextnode.md) en modifiant son nœud parent.</span><span class="sxs-lookup"><span data-stu-id="3fd31-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fd31-105">Syntax</span></span>


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a><span data-ttu-id="3fd31-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fd31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd31-107">*pInkAnalyzer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fd31-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd31-108">Objet [**IInkAnalyzer**](iinkanalyzer.md) qui déplace l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd31-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3fd31-109">*pNewParentContextNode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fd31-109">*pNewParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd31-110">Nouvel objet [**IContextNode**](icontextnode.md) parent.</span><span class="sxs-lookup"><span data-stu-id="3fd31-110">The new parent [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3fd31-111">*pContextNodeToBeReparented* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fd31-111">*pContextNodeToBeReparented* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd31-112">Objet [**IContextNode**](icontextnode.md) à déplacer.</span><span class="sxs-lookup"><span data-stu-id="3fd31-112">The [**IContextNode**](icontextnode.md) object to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd31-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fd31-113">Return value</span></span>

<span data-ttu-id="3fd31-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3fd31-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd31-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3fd31-115">Remarks</span></span>

<span data-ttu-id="3fd31-116">Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3fd31-116">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="3fd31-117">Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode qui déplace un [**IContextNode**](icontextnode.md) d’une collection de sous-nœuds à une autre (consultez [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="3fd31-117">This event occurs during the reconcile phase of ink analysis, or in response to a method that moves an [**IContextNode**](icontextnode.md) from one collection of subnodes to another (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="3fd31-118">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3fd31-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd31-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fd31-119">Requirements</span></span>



| <span data-ttu-id="3fd31-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fd31-120">Requirement</span></span> | <span data-ttu-id="3fd31-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fd31-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd31-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fd31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd31-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3fd31-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3fd31-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fd31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd31-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fd31-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3fd31-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3fd31-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd31-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3fd31-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3fd31-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd31-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fd31-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fd31-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3fd31-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fd31-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd31-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="3fd31-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="3fd31-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3fd31-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3fd31-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3fd31-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3fd31-134">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="3fd31-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="3fd31-135">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="3fd31-135">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="3fd31-136">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="3fd31-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="3fd31-137">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="3fd31-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="3fd31-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3fd31-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




