---
description: Récupère tous les objets IContextNode du type spécifié qui contiennent les traits spécifiés.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513428"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a><span data-ttu-id="8a74e-103">IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode</span><span class="sxs-lookup"><span data-stu-id="8a74e-103">IInkAnalyzer::FindNodesOfTypeForStrokes method</span></span>

<span data-ttu-id="8a74e-104">Récupère tous les objets [**IContextNode**](icontextnode.md) du type spécifié qui contiennent les traits spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8a74e-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a74e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a74e-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="8a74e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a74e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a74e-107">*pNodeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a74e-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a74e-108">Identificateur global unique (GUID) qui spécifie le type de nœud.</span><span class="sxs-lookup"><span data-stu-id="8a74e-108">The globally unique identifier (GUID) that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="8a74e-109">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a74e-109">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a74e-110">Nombre d’identificateurs de trait transmis.</span><span class="sxs-lookup"><span data-stu-id="8a74e-110">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="8a74e-111">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a74e-111">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a74e-112">Tableau des identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="8a74e-112">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8a74e-113">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a74e-113">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a74e-114">Collection d’objets [**IContextNode**](icontextnode.md) qui contiennent tous les nœuds de type *pNodeType* qui contiennent les traits avec des identificateurs dans le tableau *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="8a74e-114">The collection of [**IContextNode**](icontextnode.md) objects that contain all the nodes of type *pNodeType* that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a74e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a74e-115">Return value</span></span>

<span data-ttu-id="8a74e-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="8a74e-116">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a74e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8a74e-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8a74e-118">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="8a74e-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="8a74e-119">La propriété *pNodeType* doit contenir un GUID à partir des constantes de [type de nœud de contexte](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="8a74e-119">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="8a74e-120">Si le type de nœud spécifié n’est pas un nœud terminal, mais qu’un des descendants du nœud référence un trait dans la collection Strokes, ce nœud est ajouté à la collection retournée.</span><span class="sxs-lookup"><span data-stu-id="8a74e-120">If the specified node type is not a leaf node, but one of the node's descendants references a stroke in the strokes collection, that node is added to the collection that is returned.</span></span>

<span data-ttu-id="8a74e-121">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="8a74e-121">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a74e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a74e-122">Requirements</span></span>



| <span data-ttu-id="8a74e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a74e-123">Requirement</span></span> | <span data-ttu-id="8a74e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a74e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a74e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a74e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8a74e-126">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a74e-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a74e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a74e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8a74e-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a74e-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a74e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a74e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a74e-130"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8a74e-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a74e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8a74e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a74e-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a74e-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a74e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a74e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a74e-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8a74e-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8a74e-135">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-135">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="8a74e-136">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-136">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="8a74e-137">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="8a74e-138">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="8a74e-139">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="8a74e-140">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-140">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="8a74e-141">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-141">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="8a74e-142">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a74e-142">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="8a74e-143">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="8a74e-143">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

