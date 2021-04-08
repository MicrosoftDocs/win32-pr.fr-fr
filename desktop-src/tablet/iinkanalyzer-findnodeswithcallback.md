---
description: Récupère tous les objets IContextNode qui correspondent aux critères spécifiés.
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'IInkAnalyzer :: FindNodesWithCallBack, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751829"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a><span data-ttu-id="4e20e-103">IInkAnalyzer :: FindNodesWithCallBack, méthode</span><span class="sxs-lookup"><span data-stu-id="4e20e-103">IInkAnalyzer::FindNodesWithCallBack method</span></span>

<span data-ttu-id="4e20e-104">Récupère tous les objets [**IContextNode**](icontextnode.md) qui correspondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4e20e-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e20e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e20e-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="4e20e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e20e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e20e-107">*pCriteria* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e20e-108">Objet [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) utilisé pour déterminer si un objet [**IContextNode**](icontextnode.md) satisfait ou échoue à ses critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4e20e-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="4e20e-109">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e20e-110">Pointeur vers la collection [**IContextNodes**](icontextnodes.md) contenant tous les nœuds qui répondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4e20e-110">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e20e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e20e-111">Return value</span></span>

<span data-ttu-id="4e20e-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="4e20e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e20e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4e20e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4e20e-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e20e-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="4e20e-115">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="4e20e-115">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e20e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e20e-116">Requirements</span></span>



| <span data-ttu-id="4e20e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e20e-117">Requirement</span></span> | <span data-ttu-id="4e20e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e20e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e20e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e20e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e20e-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4e20e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e20e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e20e-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e20e-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4e20e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e20e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e20e-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4e20e-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4e20e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4e20e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e20e-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e20e-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4e20e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e20e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e20e-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4e20e-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4e20e-129">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="4e20e-130">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="4e20e-131">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="4e20e-132">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="4e20e-133">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="4e20e-134">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="4e20e-135">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="4e20e-136">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e20e-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="4e20e-137">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="4e20e-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

