---
description: Obtient les nœuds enfants directs de l’objet IContextNode.
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: 'IContextNode :: GetSubNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetSubNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5c0526ca4a5b4db355c1f895a44ebbf634cb8bc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514447"
---
# <a name="icontextnodegetsubnodes-method"></a><span data-ttu-id="fce43-103">IContextNode :: GetSubNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="fce43-103">IContextNode::GetSubNodes method</span></span>

<span data-ttu-id="fce43-104">Obtient les nœuds enfants directs de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="fce43-104">Gets the direct child nodes of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce43-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fce43-105">Syntax</span></span>


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="fce43-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fce43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce43-107">*ppSubContextNodes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fce43-107">*ppSubContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fce43-108">Collection d’objets [**IContextNode**](icontextnode.md) qui sont des nœuds enfants directs de ce **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="fce43-108">A collection of the [**IContextNode**](icontextnode.md) objects that are direct child nodes of this **IContextNode**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce43-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fce43-109">Return value</span></span>

<span data-ttu-id="fce43-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="fce43-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fce43-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fce43-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fce43-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppSubContextNodes* lorsque vous n’avez plus besoin d’utiliser la collection de sous-nœuds.</span><span class="sxs-lookup"><span data-stu-id="fce43-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSubContextNodes* when you no longer need to use the collection of subnodes.</span></span>

 

<span data-ttu-id="fce43-113">Cela retourne uniquement les nœuds enfants directs, pas tous les nœuds descendants.</span><span class="sxs-lookup"><span data-stu-id="fce43-113">This returns only the direct child nodes, not all of the descendant nodes.</span></span>

## <a name="examples"></a><span data-ttu-id="fce43-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="fce43-114">Examples</span></span>

<span data-ttu-id="fce43-115">Cet exemple montre une méthode, `ExploreContextNode` , qui examine un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="fce43-115">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="fce43-116">La méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fce43-116">The method does the following:</span></span>

-   <span data-ttu-id="fce43-117">Obtient le type du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="fce43-117">Gets the context node's type.</span></span>
-   <span data-ttu-id="fce43-118">Examine les propriétés spécifiques du type de nœud en appelant une méthode d’assistance, si le nœud de contexte est une entrée non classifiée, un indicateur d’analyse ou un nœud de reconnaissance personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fce43-118">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="fce43-119">Examine chaque sous-nœud en s’appelant lui-même, si le nœud possède des sous-nœuds.</span><span class="sxs-lookup"><span data-stu-id="fce43-119">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="fce43-120">Examine les données de trait du nœud en appelant une méthode d’assistance, si le nœud est un nœud terminal d’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="fce43-120">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="fce43-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fce43-121">Requirements</span></span>



| <span data-ttu-id="fce43-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fce43-122">Requirement</span></span> | <span data-ttu-id="fce43-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fce43-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce43-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce43-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fce43-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fce43-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fce43-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce43-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fce43-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce43-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fce43-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fce43-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce43-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fce43-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fce43-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fce43-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fce43-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fce43-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fce43-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce43-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce43-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fce43-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fce43-134">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="fce43-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="fce43-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="fce43-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

