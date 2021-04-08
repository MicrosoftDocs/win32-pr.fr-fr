---
description: Récupère tous les objets IContextNode qui correspondent aux critères spécifiés et sont des descendants de l’objet IContextNode spécifié.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751828"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a><span data-ttu-id="05032-103">IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode</span><span class="sxs-lookup"><span data-stu-id="05032-103">IInkAnalyzer::FindNodesWithCallBackInSubTree method</span></span>

<span data-ttu-id="05032-104">Récupère tous les objets [**IContextNode**](icontextnode.md) qui correspondent aux critères spécifiés et sont des descendants de l’objet **IContextNode** spécifié.</span><span class="sxs-lookup"><span data-stu-id="05032-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria and are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="05032-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05032-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="05032-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05032-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05032-107">*pCriteria* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05032-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05032-108">Objet [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) utilisé pour déterminer si un objet [**IContextNode**](icontextnode.md) satisfait ou échoue à ses critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="05032-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="05032-109">*pContextNodeToSearchFrom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05032-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05032-110">Objet [**IContextNode**](icontextnode.md) dont les descendants sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="05032-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="05032-111">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05032-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05032-112">Pointeur vers le [**IContextNodes**](icontextnodes.md) contenant tous les nœuds qui répondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="05032-112">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05032-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05032-113">Return value</span></span>

<span data-ttu-id="05032-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="05032-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05032-115">Notes</span><span class="sxs-lookup"><span data-stu-id="05032-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="05032-116">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="05032-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="05032-117">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas le nœud *pContextNodeToSearchFrom* , cette méthode retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="05032-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="05032-118">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="05032-118">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="05032-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05032-119">Requirements</span></span>



| <span data-ttu-id="05032-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05032-120">Requirement</span></span> | <span data-ttu-id="05032-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="05032-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05032-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05032-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05032-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05032-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05032-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05032-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05032-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05032-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05032-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="05032-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="05032-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="05032-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05032-128">DLL</span><span class="sxs-lookup"><span data-stu-id="05032-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05032-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05032-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05032-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05032-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05032-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="05032-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="05032-132">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-132">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="05032-133">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-133">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="05032-134">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-134">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="05032-135">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-135">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="05032-136">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-136">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="05032-137">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-137">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="05032-138">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-138">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="05032-139">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="05032-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="05032-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="05032-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

