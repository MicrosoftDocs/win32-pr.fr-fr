---
description: Récupère l’objet IContextNode à l’index spécifié dans cette collection.
ms.assetid: 4b266512-9e58-43d2-8430-68310230fc27
title: 'IContextNodes :: GetContextNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ec907fdcac5a1ed18cca54c79a876959868f2ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485097"
---
# <a name="icontextnodesgetcontextnode-method"></a><span data-ttu-id="eecdc-103">IContextNodes :: GetContextNode, méthode</span><span class="sxs-lookup"><span data-stu-id="eecdc-103">IContextNodes::GetContextNode method</span></span>

<span data-ttu-id="eecdc-104">Récupère l’objet [**IContextNode**](icontextnode.md) à l’index spécifié dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="eecdc-104">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eecdc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eecdc-105">Syntax</span></span>


```C++
HRESULT GetContextNode(
  [in]  ULONG        ulIndex,
  [out] IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="eecdc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eecdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eecdc-107">*ulIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eecdc-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eecdc-108">Index de base zéro de l’objet [**IContextNode**](icontextnode.md) à récupérer.</span><span class="sxs-lookup"><span data-stu-id="eecdc-108">The zero-based index of the [**IContextNode**](icontextnode.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="eecdc-109">*ppContextNode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eecdc-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eecdc-110">Pointeur vers le [**IContextNode**](icontextnode.md) référencé à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="eecdc-110">Pointer to the [**IContextNode**](icontextnode.md) referenced at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eecdc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eecdc-111">Return value</span></span>

<span data-ttu-id="eecdc-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eecdc-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eecdc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eecdc-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="eecdc-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextNode* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="eecdc-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNode* when you no longer need to use the context node.</span></span>

 

## <a name="examples"></a><span data-ttu-id="eecdc-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="eecdc-115">Examples</span></span>

<span data-ttu-id="eecdc-116">Cet exemple montre une méthode, `ExploreContextNode` , qui examine un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="eecdc-116">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="eecdc-117">La méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="eecdc-117">The method does the following:</span></span>

-   <span data-ttu-id="eecdc-118">Obtient le type du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="eecdc-118">Gets the context node's type.</span></span>
-   <span data-ttu-id="eecdc-119">Examine les propriétés spécifiques du type de nœud en appelant une méthode d’assistance, si le nœud de contexte est une entrée non classifiée, un indicateur d’analyse ou un nœud de reconnaissance personnalisé.</span><span class="sxs-lookup"><span data-stu-id="eecdc-119">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="eecdc-120">Examine chaque sous-nœud en s’appelant lui-même, si le nœud possède des sous-nœuds.</span><span class="sxs-lookup"><span data-stu-id="eecdc-120">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="eecdc-121">Examine les données de trait du nœud en appelant une méthode d’assistance, si le nœud est un nœud terminal d’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="eecdc-121">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="eecdc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eecdc-122">Requirements</span></span>



| <span data-ttu-id="eecdc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eecdc-123">Requirement</span></span> | <span data-ttu-id="eecdc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="eecdc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eecdc-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eecdc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eecdc-126">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eecdc-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eecdc-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eecdc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eecdc-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eecdc-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="eecdc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="eecdc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="eecdc-130"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eecdc-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eecdc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="eecdc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eecdc-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eecdc-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="eecdc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eecdc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eecdc-134">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="eecdc-134">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="eecdc-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="eecdc-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

