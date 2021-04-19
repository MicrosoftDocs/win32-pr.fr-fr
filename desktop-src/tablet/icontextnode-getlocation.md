---
description: Récupère la position et la taille de l’objet IContextNode.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'IContextNode :: GetLocation, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515258"
---
# <a name="icontextnodegetlocation-method"></a><span data-ttu-id="93bd7-103">IContextNode :: GetLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="93bd7-103">IContextNode::GetLocation method</span></span>

<span data-ttu-id="93bd7-104">Récupère la position et la taille de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="93bd7-104">Retrieves the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bd7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93bd7-105">Syntax</span></span>


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="93bd7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93bd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bd7-107">*ppIAnalysisRegion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="93bd7-107">*ppIAnalysisRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93bd7-108">Pointeur vers la position et la taille de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="93bd7-108">A pointer to the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bd7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93bd7-109">Return value</span></span>

<span data-ttu-id="93bd7-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="93bd7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="93bd7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="93bd7-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="93bd7-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppIAnalysisRegion* lorsque vous n’avez plus besoin d’utiliser la région d’analyse.</span><span class="sxs-lookup"><span data-stu-id="93bd7-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppIAnalysisRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="93bd7-113">L’emplacement d’un nœud de conteneur est déterminé par la recherche de l’Union de tous les emplacements de la feuille.</span><span class="sxs-lookup"><span data-stu-id="93bd7-113">The location for a container node is determined by finding the union of all the leaf's locations.</span></span> <span data-ttu-id="93bd7-114">L’emplacement d’un nœud terminal d’encre est déterminé par la recherche de l’Union du cadre englobant des traits associés.</span><span class="sxs-lookup"><span data-stu-id="93bd7-114">The location for an ink leaf node is determined by finding the union of the bounding box of the associated strokes.</span></span> <span data-ttu-id="93bd7-115">L’emplacement d’un nœud terminal non manuscrit est défini lors de la création du nœud et peut être mis à jour à l’aide de [**IContextNode :: SetLocation**](icontextnode-setlocation.md).</span><span class="sxs-lookup"><span data-stu-id="93bd7-115">The location for a non-ink leaf node is set when the node is created and can be updated using [**IContextNode::SetLocation**](icontextnode-setlocation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="93bd7-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="93bd7-116">Examples</span></span>

<span data-ttu-id="93bd7-117">L’exemple suivant montre une méthode d’assistance qui récupère des informations sur un nœud spécifié, son paramètre *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="93bd7-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="93bd7-118">Cette méthode d’assistance retourne des informations à partir des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="93bd7-118">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="93bd7-119">**IContextNode :: GetId**</span><span class="sxs-lookup"><span data-stu-id="93bd7-119">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="93bd7-120">**IContextNode :: GetType**</span><span class="sxs-lookup"><span data-stu-id="93bd7-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   <span data-ttu-id="93bd7-121">**IContextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="93bd7-121">**IContextNode::GetLocation**</span></span>
-   [<span data-ttu-id="93bd7-122">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="93bd7-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="93bd7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93bd7-123">Requirements</span></span>



| <span data-ttu-id="93bd7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93bd7-124">Requirement</span></span> | <span data-ttu-id="93bd7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="93bd7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bd7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93bd7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93bd7-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93bd7-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="93bd7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93bd7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93bd7-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="93bd7-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="93bd7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="93bd7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="93bd7-131"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="93bd7-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="93bd7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="93bd7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93bd7-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93bd7-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="93bd7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93bd7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bd7-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="93bd7-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="93bd7-136">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="93bd7-136">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="93bd7-137">**IContextNode :: SetLocation**</span><span class="sxs-lookup"><span data-stu-id="93bd7-137">**IContextNode::SetLocation**</span></span>](icontextnode-setlocation.md)
</dt> <dt>

[<span data-ttu-id="93bd7-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="93bd7-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

