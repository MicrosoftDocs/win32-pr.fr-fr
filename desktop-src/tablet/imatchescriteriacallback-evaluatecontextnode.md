---
description: En cas de substitution dans une classe dérivée, évalue si un objet IContextNode spécifié répond aux critères.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'IMatchesCriteriaCallBack :: EvaluateContextNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544221"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a><span data-ttu-id="cc82a-103">IMatchesCriteriaCallBack :: EvaluateContextNode, méthode</span><span class="sxs-lookup"><span data-stu-id="cc82a-103">IMatchesCriteriaCallBack::EvaluateContextNode method</span></span>

<span data-ttu-id="cc82a-104">En cas de substitution dans une classe dérivée, évalue si un objet [**IContextNode**](icontextnode.md) spécifié répond aux critères.</span><span class="sxs-lookup"><span data-stu-id="cc82a-104">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc82a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc82a-105">Syntax</span></span>


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a><span data-ttu-id="cc82a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc82a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc82a-107">*pContextNodeToEvaluate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc82a-107">*pContextNodeToEvaluate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc82a-108">Objet [**IContextNode**](icontextnode.md) à évaluer.</span><span class="sxs-lookup"><span data-stu-id="cc82a-108">The [**IContextNode**](icontextnode.md) object to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="cc82a-109">*pbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc82a-109">*pbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc82a-110">**Variante \_ TRUE** si *pContextNodeToEvaluate* correspond aux critères ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cc82a-110">**VARIANT\_TRUE** if *pContextNodeToEvaluate* matches the criteria; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc82a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc82a-111">Return value</span></span>

<span data-ttu-id="cc82a-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="cc82a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc82a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cc82a-113">Remarks</span></span>

<span data-ttu-id="cc82a-114">Pour utiliser la méthode [**IInkAnalyzer :: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou [**IInkAnalyzer :: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), créez une classe qui implémente [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span><span class="sxs-lookup"><span data-stu-id="cc82a-114">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span></span> <span data-ttu-id="cc82a-115">Implémentez **IMatchesCriteriaCallBack :: EvaluateContextNode** pour retourner la **\_ valeur variant true** si l’objet [**IContextNode**](icontextnode.md) correspond à vos critères, et **Variant \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cc82a-115">Implement **IMatchesCriteriaCallBack::EvaluateContextNode** to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="cc82a-116">Pour certains critères, vous devrez peut-être fournir un moyen d’initialiser ou de maintenir l’état de votre objet **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="cc82a-116">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc82a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc82a-117">Requirements</span></span>



| <span data-ttu-id="cc82a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc82a-118">Requirement</span></span> | <span data-ttu-id="cc82a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc82a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc82a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc82a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cc82a-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc82a-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cc82a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc82a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cc82a-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc82a-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cc82a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc82a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc82a-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cc82a-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cc82a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cc82a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc82a-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc82a-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cc82a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc82a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc82a-129">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="cc82a-129">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md)
</dt> <dt>

[<span data-ttu-id="cc82a-130">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="cc82a-130">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="cc82a-131">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="cc82a-131">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="cc82a-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="cc82a-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




