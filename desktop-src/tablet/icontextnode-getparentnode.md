---
description: Récupère le nœud parent de ce IContextNode dans l’arborescence du nœud de contexte.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'IContextNode :: GetParentNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526529"
---
# <a name="icontextnodegetparentnode-method"></a><span data-ttu-id="3e42a-103">IContextNode :: GetParentNode, méthode</span><span class="sxs-lookup"><span data-stu-id="3e42a-103">IContextNode::GetParentNode method</span></span>

<span data-ttu-id="3e42a-104">Récupère le nœud parent de ce [**IContextNode**](icontextnode.md) dans l’arborescence du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="3e42a-104">Retrieves the parent node of this [**IContextNode**](icontextnode.md) in the context node tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e42a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e42a-105">Syntax</span></span>


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="3e42a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e42a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e42a-107">*ppParentContextNode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3e42a-107">*ppParentContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e42a-108">Pointeur vers le nœud parent de cet objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3e42a-108">A pointer to the parent node of this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e42a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e42a-109">Return value</span></span>

<span data-ttu-id="3e42a-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3e42a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e42a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3e42a-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3e42a-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppParentContextNode* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte parent.</span><span class="sxs-lookup"><span data-stu-id="3e42a-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppParentContextNode* when you no longer need to use the parent context node.</span></span>

 

<span data-ttu-id="3e42a-113">S’il s’agit du nœud racine, le paramètre *ppParentContextNode* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="3e42a-113">If this is the root node, the *ppParentContextNode* parameter is set to **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="3e42a-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="3e42a-114">Examples</span></span>

<span data-ttu-id="3e42a-115">L’exemple suivant montre une méthode d’assistance qui récupère des informations sur un nœud spécifié, son paramètre *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="3e42a-115">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="3e42a-116">Cette méthode d’assistance retourne des informations à partir des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3e42a-116">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="3e42a-117">**IContextNode :: GetId**</span><span class="sxs-lookup"><span data-stu-id="3e42a-117">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="3e42a-118">**IContextNode :: GetType**</span><span class="sxs-lookup"><span data-stu-id="3e42a-118">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="3e42a-119">**IContextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="3e42a-119">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   <span data-ttu-id="3e42a-120">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="3e42a-120">**IContextNode::GetParentNode**</span></span>


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="3e42a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e42a-121">Requirements</span></span>



| <span data-ttu-id="3e42a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e42a-122">Requirement</span></span> | <span data-ttu-id="3e42a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e42a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e42a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e42a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3e42a-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e42a-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e42a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e42a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3e42a-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e42a-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3e42a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e42a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e42a-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3e42a-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e42a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3e42a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e42a-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e42a-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3e42a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e42a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e42a-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3e42a-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3e42a-134">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="3e42a-134">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="3e42a-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3e42a-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

