---
description: Récupère tous les nœuds de feuille d’encre.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'IInkAnalyzer :: FindInkLeafNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862697"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a><span data-ttu-id="4e2ef-103">IInkAnalyzer :: FindInkLeafNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="4e2ef-103">IInkAnalyzer::FindInkLeafNodes method</span></span>

<span data-ttu-id="4e2ef-104">Récupère tous les nœuds de feuille d’encre.</span><span class="sxs-lookup"><span data-stu-id="4e2ef-104">Retrieves all of the ink leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e2ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e2ef-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="4e2ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e2ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2ef-107">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4e2ef-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e2ef-108">Pointeur vers la collection [**IContextNodes**](icontextnodes.md) contenant tous les nœuds de feuille d’encre.</span><span class="sxs-lookup"><span data-stu-id="4e2ef-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all ink leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2ef-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e2ef-109">Return value</span></span>

<span data-ttu-id="4e2ef-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="4e2ef-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e2ef-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4e2ef-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4e2ef-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e2ef-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="4e2ef-113">Les nœuds terminaux ne contiennent pas de nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="4e2ef-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="4e2ef-114">Les nœuds d’entrée contiennent des données de trait.</span><span class="sxs-lookup"><span data-stu-id="4e2ef-114">Ink nodes contain stroke data.</span></span> <span data-ttu-id="4e2ef-115">Les objets InkWord, InkDrawing et InkBullet [**IContextNode**](icontextnode.md) sont des exemples de nœuds feuille d’encre.</span><span class="sxs-lookup"><span data-stu-id="4e2ef-115">Examples of ink leaf nodes are InkWord, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="4e2ef-116">Pour plus d’informations, consultez [types de nœuds de contexte](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="4e2ef-116">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2ef-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e2ef-117">Requirements</span></span>



| <span data-ttu-id="4e2ef-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e2ef-118">Requirement</span></span> | <span data-ttu-id="4e2ef-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e2ef-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2ef-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e2ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2ef-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e2ef-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4e2ef-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e2ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2ef-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e2ef-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4e2ef-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e2ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2ef-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4e2ef-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4e2ef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4e2ef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e2ef-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e2ef-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4e2ef-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e2ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e2ef-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-130">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-131">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-132">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-133">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-134">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-135">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-136">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-137">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="4e2ef-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="4e2ef-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="4e2ef-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

