---
description: Récupère l’identificateur pour l’objet IContextNode.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'IContextNode :: GetId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862718"
---
# <a name="icontextnodegetid-method"></a><span data-ttu-id="1f78c-103">IContextNode :: GetId, méthode</span><span class="sxs-lookup"><span data-stu-id="1f78c-103">IContextNode::GetId method</span></span>

<span data-ttu-id="1f78c-104">Récupère l’identificateur pour l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1f78c-104">Retrieves the identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f78c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f78c-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="1f78c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f78c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f78c-107">*PID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f78c-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f78c-108">Identificateur de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1f78c-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f78c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f78c-109">Return value</span></span>

<span data-ttu-id="1f78c-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1f78c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f78c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1f78c-111">Remarks</span></span>

<span data-ttu-id="1f78c-112">L’analyseur d’encre affecte un identificateur unique à tous les nœuds de contexte qu’il crée.</span><span class="sxs-lookup"><span data-stu-id="1f78c-112">The ink analyzer assigns a unique identifier to all context nodes it creates.</span></span> <span data-ttu-id="1f78c-113">Pendant l’analyse de l’encre, l’analyseur d’encre peut modifier l’identificateur d’un nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="1f78c-113">During ink analysis, the ink analyzer may change the identifier for a context node.</span></span> <span data-ttu-id="1f78c-114">Par exemple, l’analyseur d’encre peut reclassifier un nœud Word en deux nœuds Word, puis assigner l’identificateur d’origine à un et un nouvel identificateur à l’autre.</span><span class="sxs-lookup"><span data-stu-id="1f78c-114">For example, the ink analyzer may reclassify one word node as two word nodes and then assign the original identifier to one and a new identifier to the other.</span></span> <span data-ttu-id="1f78c-115">Ou bien, l’analyseur d’encre peut reclasser deux nœuds Word en un seul nœud Word et assigner l’un des identificateurs originaux au nouveau nœud Word.</span><span class="sxs-lookup"><span data-stu-id="1f78c-115">Or, the ink analyzer may reclassify two word nodes as one word node and assign one of the original identifiers to the new word node.</span></span>

## <a name="examples"></a><span data-ttu-id="1f78c-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="1f78c-116">Examples</span></span>

<span data-ttu-id="1f78c-117">L’exemple suivant montre une méthode d’assistance qui récupère des informations sur un nœud spécifié, son paramètre *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="1f78c-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="1f78c-118">Cette méthode d’assistance retourne des informations à partir des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f78c-118">This helper method returns information from the following methods.</span></span>

-   <span data-ttu-id="1f78c-119">**IContextNode :: GetId**</span><span class="sxs-lookup"><span data-stu-id="1f78c-119">**IContextNode::GetId**</span></span>
-   [<span data-ttu-id="1f78c-120">**IContextNode :: GetType**</span><span class="sxs-lookup"><span data-stu-id="1f78c-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="1f78c-121">**IContextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="1f78c-121">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="1f78c-122">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="1f78c-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="1f78c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f78c-123">Requirements</span></span>



| <span data-ttu-id="1f78c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f78c-124">Requirement</span></span> | <span data-ttu-id="1f78c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f78c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f78c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f78c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1f78c-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f78c-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1f78c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f78c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1f78c-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f78c-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1f78c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f78c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f78c-131"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1f78c-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1f78c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1f78c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f78c-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f78c-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1f78c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f78c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f78c-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="1f78c-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1f78c-136">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="1f78c-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




