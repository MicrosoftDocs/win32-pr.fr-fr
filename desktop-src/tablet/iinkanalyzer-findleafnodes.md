---
description: Récupère tous les nœuds terminaux.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'IInkAnalyzer :: FindLeafNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526499"
---
# <a name="iinkanalyzerfindleafnodes-method"></a><span data-ttu-id="75634-103">IInkAnalyzer :: FindLeafNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="75634-103">IInkAnalyzer::FindLeafNodes method</span></span>

<span data-ttu-id="75634-104">Récupère tous les nœuds terminaux.</span><span class="sxs-lookup"><span data-stu-id="75634-104">Retrieves all of the leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="75634-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75634-105">Syntax</span></span>


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="75634-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75634-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75634-107">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75634-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75634-108">Pointeur vers la collection [**IContextNodes**](icontextnodes.md) contenant tous les nœuds feuille.</span><span class="sxs-lookup"><span data-stu-id="75634-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75634-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75634-109">Return value</span></span>

<span data-ttu-id="75634-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="75634-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75634-111">Notes</span><span class="sxs-lookup"><span data-stu-id="75634-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="75634-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="75634-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="75634-113">Les nœuds terminaux ne contiennent pas de nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="75634-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="75634-114">Exemples de nœuds de feuille manuscrite : InkWord, TextWord, image, InkDrawing et InkBullet [**IContextNode**](icontextnode.md) objets.</span><span class="sxs-lookup"><span data-stu-id="75634-114">Examples of ink leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="75634-115">Pour plus d’informations, consultez [types de nœuds de contexte](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="75634-115">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75634-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75634-116">Requirements</span></span>



| <span data-ttu-id="75634-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75634-117">Requirement</span></span> | <span data-ttu-id="75634-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="75634-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75634-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75634-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75634-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75634-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75634-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75634-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75634-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="75634-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75634-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="75634-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75634-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75634-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75634-125">DLL</span><span class="sxs-lookup"><span data-stu-id="75634-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75634-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75634-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75634-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75634-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75634-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="75634-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="75634-129">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="75634-130">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="75634-131">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-131">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="75634-132">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="75634-133">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="75634-134">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="75634-135">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="75634-136">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="75634-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="75634-137">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="75634-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

