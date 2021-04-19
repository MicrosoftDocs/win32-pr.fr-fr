---
description: Récupère tous les objets IContextNode du type spécifié qui sont des descendants de l’objet IContextNode spécifié.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516016"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a><span data-ttu-id="b4cd9-103">IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode</span><span class="sxs-lookup"><span data-stu-id="b4cd9-103">IInkAnalyzer::FindNodesOfTypeInSubTree method</span></span>

<span data-ttu-id="b4cd9-104">Récupère tous les objets [**IContextNode**](icontextnode.md) du type spécifié qui sont des descendants de l’objet **IContextNode** spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4cd9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4cd9-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="b4cd9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4cd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4cd9-107">*pNodeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4cd9-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4cd9-108">**GUID** qui spécifie le type de nœud.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="b4cd9-109">*pContextNodeToSearchFrom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4cd9-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4cd9-110">Objet [**IContextNode**](icontextnode.md) dont les descendants sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="b4cd9-111">*ppContextNodesFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4cd9-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4cd9-112">Collection [**IContextNodes**](icontextnodes.md) contenant tous les nœuds de type *pNodeType* qui sont des descendants de *pContextNodeToSearchFrom*.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-112">The [**IContextNodes**](icontextnodes.md) collection containing all nodes of type *pNodeType* that are descendants of *pContextNodeToSearchFrom*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4cd9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4cd9-113">Return value</span></span>

<span data-ttu-id="b4cd9-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4cd9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b4cd9-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b4cd9-116">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="b4cd9-117">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas le nœud *pContextNodeToSearchFrom* , cette méthode retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="b4cd9-118">La propriété *pNodeType* doit contenir un identificateur global unique (Guid) à partir des constantes de [type de nœud de contexte](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="b4cd9-118">The *pNodeType* property must contain a globally unique identifier (GUID) from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="b4cd9-119">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="b4cd9-119">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4cd9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4cd9-120">Requirements</span></span>



| <span data-ttu-id="b4cd9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4cd9-121">Requirement</span></span> | <span data-ttu-id="b4cd9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4cd9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cd9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4cd9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b4cd9-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4cd9-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4cd9-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4cd9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b4cd9-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4cd9-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4cd9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4cd9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4cd9-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4cd9-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4cd9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b4cd9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4cd9-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4cd9-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4cd9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4cd9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cd9-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-133">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-133">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-134">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-134">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-135">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-135">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-136">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-136">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-137">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-137">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-138">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-138">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-139">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-140">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="b4cd9-140">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b4cd9-141">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b4cd9-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

