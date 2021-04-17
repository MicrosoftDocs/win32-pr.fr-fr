---
description: Obtient le nombre de traits associés à l’objet IContextNode.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'IContextNode :: GetStrokeCount, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485105"
---
# <a name="icontextnodegetstrokecount-method"></a><span data-ttu-id="33682-103">IContextNode :: GetStrokeCount, méthode</span><span class="sxs-lookup"><span data-stu-id="33682-103">IContextNode::GetStrokeCount method</span></span>

<span data-ttu-id="33682-104">Obtient le nombre de traits associés à l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="33682-104">Gets the number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="33682-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33682-105">Syntax</span></span>


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a><span data-ttu-id="33682-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33682-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33682-107">*pulStrokeCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="33682-107">*pulStrokeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33682-108">Nombre de traits associés à l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="33682-108">The number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33682-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33682-109">Return value</span></span>

<span data-ttu-id="33682-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="33682-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33682-111">Notes</span><span class="sxs-lookup"><span data-stu-id="33682-111">Remarks</span></span>

<span data-ttu-id="33682-112">Seuls les nœuds de contexte de feuille manuscrite ont des données de trait associées (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="33682-112">Only ink leaf context nodes have associated stroke data (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="33682-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="33682-113">Examples</span></span>

<span data-ttu-id="33682-114">Cet exemple montre une méthode, `ExploreContextNode` , qui examine un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="33682-114">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="33682-115">La méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="33682-115">The method does the following:</span></span>

-   <span data-ttu-id="33682-116">Obtient le type du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="33682-116">Gets the context node's type.</span></span>
-   <span data-ttu-id="33682-117">Examine les propriétés spécifiques du type de nœud en appelant une méthode d’assistance, si le nœud de contexte est une entrée non classifiée, un indicateur d’analyse ou un nœud de reconnaissance personnalisé.</span><span class="sxs-lookup"><span data-stu-id="33682-117">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="33682-118">Examine chaque sous-nœud en s’appelant lui-même, si le nœud possède des sous-nœuds.</span><span class="sxs-lookup"><span data-stu-id="33682-118">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="33682-119">Examine les données de trait du nœud en appelant une méthode d’assistance, si le nœud est un nœud terminal d’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="33682-119">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="33682-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33682-120">Requirements</span></span>



| <span data-ttu-id="33682-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33682-121">Requirement</span></span> | <span data-ttu-id="33682-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="33682-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33682-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33682-123">Minimum supported client</span></span><br/> | <span data-ttu-id="33682-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33682-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33682-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33682-125">Minimum supported server</span></span><br/> | <span data-ttu-id="33682-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="33682-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="33682-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="33682-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="33682-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="33682-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33682-129">DLL</span><span class="sxs-lookup"><span data-stu-id="33682-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33682-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33682-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="33682-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33682-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33682-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="33682-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="33682-133">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="33682-133">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="33682-134">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="33682-134">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="33682-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="33682-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




