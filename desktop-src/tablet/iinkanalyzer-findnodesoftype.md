---
description: Récupère tous les objets IContextNode du type spécifié.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'IInkAnalyzer :: FindNodesOfType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862690"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a><span data-ttu-id="04364-103">IInkAnalyzer :: FindNodesOfType, méthode</span><span class="sxs-lookup"><span data-stu-id="04364-103">IInkAnalyzer::FindNodesOfType method</span></span>

<span data-ttu-id="04364-104">Récupère tous les objets [**IContextNode**](icontextnode.md) du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="04364-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="04364-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04364-105">Syntax</span></span>


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="04364-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04364-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04364-107">*pNodeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04364-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04364-108">**GUID** qui spécifie le type de nœud.</span><span class="sxs-lookup"><span data-stu-id="04364-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="04364-109">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04364-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04364-110">Pointeur vers le [**IContextNodes**](icontextnodes.md) contenant tous les nœuds de type *pNodeType*.</span><span class="sxs-lookup"><span data-stu-id="04364-110">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes of type *pNodeType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04364-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04364-111">Return value</span></span>

<span data-ttu-id="04364-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="04364-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04364-113">Notes</span><span class="sxs-lookup"><span data-stu-id="04364-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="04364-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="04364-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="04364-115">La propriété *pNodeType* doit contenir un GUID à partir des constantes de [type de nœud de contexte](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="04364-115">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="04364-116">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="04364-116">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="04364-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04364-117">Requirements</span></span>



| <span data-ttu-id="04364-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04364-118">Requirement</span></span> | <span data-ttu-id="04364-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="04364-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04364-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04364-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04364-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04364-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04364-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04364-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04364-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04364-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="04364-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="04364-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="04364-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="04364-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04364-126">DLL</span><span class="sxs-lookup"><span data-stu-id="04364-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04364-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04364-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="04364-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04364-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04364-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="04364-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="04364-130">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-130">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="04364-131">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-131">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="04364-132">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-132">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="04364-133">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-133">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="04364-134">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="04364-135">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="04364-136">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="04364-137">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="04364-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="04364-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="04364-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

