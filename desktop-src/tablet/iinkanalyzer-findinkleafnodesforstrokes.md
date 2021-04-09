---
description: Récupère les nœuds de feuille d’encre qui contiennent les traits spécifiés.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862693"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a><span data-ttu-id="8a5dd-103">IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode</span><span class="sxs-lookup"><span data-stu-id="8a5dd-103">IInkAnalyzer::FindInkLeafNodesForStrokes method</span></span>

<span data-ttu-id="8a5dd-104">Récupère les nœuds de feuille d’encre qui contiennent les traits spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-104">Retrieves the ink leaf nodes that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a5dd-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="8a5dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a5dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a5dd-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a5dd-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5dd-108">Nombre d’identificateurs de trait transmis.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-108">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="8a5dd-109">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a5dd-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5dd-110">Tableau des identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-110">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8a5dd-111">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a5dd-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5dd-112">Collection d’objets [**IContextNode**](icontextnode.md) qui contiennent tous les nœuds de feuille d’encre qui contiennent les traits avec des identificateurs dans le tableau *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="8a5dd-112">The collection of [**IContextNode**](icontextnode.md) objects that contain all the ink leaf nodes that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a5dd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a5dd-113">Return value</span></span>

<span data-ttu-id="8a5dd-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a5dd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8a5dd-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8a5dd-116">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="8a5dd-117">Les nœuds terminaux ne contiennent pas de nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-117">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="8a5dd-118">Les nœuds d’entrée contiennent des données de trait.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-118">Ink nodes contain stroke data.</span></span> <span data-ttu-id="8a5dd-119">Exemples de nœuds de feuille manuscrite : InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objets.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-119">Examples of ink leaf nodes are InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="8a5dd-120">Pour plus d’informations, consultez [types de nœuds de contexte](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="8a5dd-120">For more information, see [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="8a5dd-121">Si aucun nœud ne contient les traits spécifiés, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-121">If no nodes contain the specified strokes, an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span> <span data-ttu-id="8a5dd-122">De même, si *ulStrokeIdsCount* est égal à zéro, une collection **IContextNodes** vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="8a5dd-122">Similarly, if *ulStrokeIdsCount* is zero, an empty **IContextNodes** collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a5dd-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a5dd-123">Requirements</span></span>



| <span data-ttu-id="8a5dd-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a5dd-124">Requirement</span></span> | <span data-ttu-id="8a5dd-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a5dd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5dd-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a5dd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5dd-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a5dd-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a5dd-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a5dd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5dd-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a5dd-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a5dd-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a5dd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a5dd-131"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8a5dd-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a5dd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8a5dd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a5dd-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a5dd-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a5dd-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a5dd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5dd-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-136">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-136">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-137">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-138">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-139">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-140">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-140">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-141">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-141">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-142">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-142">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-143">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="8a5dd-143">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="8a5dd-144">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="8a5dd-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

