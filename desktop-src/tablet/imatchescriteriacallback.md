---
description: Expose une méthode pour évaluer si un objet IContextNode satisfait ou échoue à un critère spécifié.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interface IMatchesCriteriaCallBack (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525318"
---
# <a name="imatchescriteriacallback-interface"></a><span data-ttu-id="d7557-103">Interface IMatchesCriteriaCallBack</span><span class="sxs-lookup"><span data-stu-id="d7557-103">IMatchesCriteriaCallBack interface</span></span>

<span data-ttu-id="d7557-104">Expose une méthode pour évaluer si un objet [**IContextNode**](icontextnode.md) satisfait ou échoue à un critère spécifié.</span><span class="sxs-lookup"><span data-stu-id="d7557-104">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span>

## <a name="members"></a><span data-ttu-id="d7557-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d7557-105">Members</span></span>

<span data-ttu-id="d7557-106">L’interface **IMatchesCriteriaCallBack** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d7557-106">The **IMatchesCriteriaCallBack** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d7557-107">**IMatchesCriteriaCallBack** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d7557-107">**IMatchesCriteriaCallBack** also has these types of members:</span></span>

-   [<span data-ttu-id="d7557-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d7557-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7557-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d7557-109">Methods</span></span>

<span data-ttu-id="d7557-110">L’interface **IMatchesCriteriaCallBack** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d7557-110">The **IMatchesCriteriaCallBack** interface has these methods.</span></span>



| <span data-ttu-id="d7557-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="d7557-111">Method</span></span>                                                                      | <span data-ttu-id="d7557-112">Description</span><span class="sxs-lookup"><span data-stu-id="d7557-112">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7557-113">**EvaluateContextNode**</span><span class="sxs-lookup"><span data-stu-id="d7557-113">**EvaluateContextNode**</span></span>](imatchescriteriacallback-evaluatecontextnode.md) | <span data-ttu-id="d7557-114">En cas de substitution dans une classe dérivée, évalue si un objet [**IContextNode**](icontextnode.md) spécifié répond aux critères.</span><span class="sxs-lookup"><span data-stu-id="d7557-114">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7557-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d7557-115">Remarks</span></span>

<span data-ttu-id="d7557-116">Pour utiliser la méthode [**IInkAnalyzer :: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou [**IInkAnalyzer :: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), créez une classe qui implémente **IMatchesCriteriaCallBack**.</span><span class="sxs-lookup"><span data-stu-id="d7557-116">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements **IMatchesCriteriaCallBack**.</span></span> <span data-ttu-id="d7557-117">Implémentez [**IMatchesCriteriaCallBack :: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) pour retourner la **\_ valeur variant true** si l’objet [**IContextNode**](icontextnode.md) correspond à vos critères, et **Variant \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d7557-117">Implement [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="d7557-118">Pour certains critères, vous devrez peut-être fournir un moyen d’initialiser ou de maintenir l’état de votre objet **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="d7557-118">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7557-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7557-119">Requirements</span></span>



| <span data-ttu-id="d7557-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7557-120">Requirement</span></span> | <span data-ttu-id="d7557-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7557-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7557-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7557-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7557-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7557-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7557-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7557-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7557-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7557-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d7557-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7557-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7557-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d7557-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d7557-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d7557-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7557-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7557-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d7557-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7557-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7557-131">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="d7557-131">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="d7557-132">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="d7557-132">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="d7557-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="d7557-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

