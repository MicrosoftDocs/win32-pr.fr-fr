---
description: Récupère le type de l’objet IContextNode.
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'IContextNode :: GetType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113378"
---
# <a name="icontextnodegettype-method"></a><span data-ttu-id="80735-103">IContextNode :: GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="80735-103">IContextNode::GetType method</span></span>

<span data-ttu-id="80735-104">Récupère le type de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="80735-104">Retrieves the type of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="80735-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80735-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="80735-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80735-107">*pContextNodeType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80735-107">*pContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80735-108">Type de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="80735-108">The type of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80735-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80735-109">Return value</span></span>

<span data-ttu-id="80735-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="80735-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="80735-111">Notes</span><span class="sxs-lookup"><span data-stu-id="80735-111">Remarks</span></span>

<span data-ttu-id="80735-112">Les types de nœuds sont décrits dans les constantes de [type de nœud de contexte](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="80735-112">Types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="80735-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="80735-113">Examples</span></span>

<span data-ttu-id="80735-114">L’exemple suivant montre une méthode d’assistance qui récupère des informations sur un nœud spécifié, son paramètre *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="80735-114">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="80735-115">Cette méthode d’assistance retourne des informations à partir des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="80735-115">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="80735-116">**IContextNode :: GetId**</span><span class="sxs-lookup"><span data-stu-id="80735-116">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   <span data-ttu-id="80735-117">**IContextNode :: GetType**</span><span class="sxs-lookup"><span data-stu-id="80735-117">**IContextNode::GetType**</span></span>
-   [<span data-ttu-id="80735-118">**IContextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="80735-118">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="80735-119">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="80735-119">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="80735-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80735-120">Requirements</span></span>



| <span data-ttu-id="80735-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80735-121">Requirement</span></span> | <span data-ttu-id="80735-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="80735-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80735-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80735-123">Minimum supported client</span></span><br/> | <span data-ttu-id="80735-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80735-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="80735-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80735-125">Minimum supported server</span></span><br/> | <span data-ttu-id="80735-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="80735-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="80735-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="80735-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="80735-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="80735-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="80735-129">DLL</span><span class="sxs-lookup"><span data-stu-id="80735-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80735-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80735-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="80735-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80735-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80735-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="80735-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="80735-133">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="80735-133">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="80735-134">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="80735-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




