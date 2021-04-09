---
description: Crée un objet IContextNode enfant qui contient uniquement des informations sur le type, l’identificateur et l’emplacement.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'IContextNode :: CreatePartiallyPopulatedSubNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862722"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a><span data-ttu-id="33baa-103">IContextNode :: CreatePartiallyPopulatedSubNode, méthode</span><span class="sxs-lookup"><span data-stu-id="33baa-103">IContextNode::CreatePartiallyPopulatedSubNode method</span></span>

<span data-ttu-id="33baa-104">Crée un objet [**IContextNode**](icontextnode.md) enfant qui contient uniquement des informations sur le type, l’identificateur et l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="33baa-104">Creates a child [**IContextNode**](icontextnode.md) object that contains only information about type, identifier, and location.</span></span>

## <a name="syntax"></a><span data-ttu-id="33baa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33baa-105">Syntax</span></span>


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="33baa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33baa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33baa-107">*pNodeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33baa-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33baa-108">Type de nœud de contexte à créer.</span><span class="sxs-lookup"><span data-stu-id="33baa-108">The type of context node to create.</span></span>

</dd> <dt>

<span data-ttu-id="33baa-109">*pNodeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33baa-109">*pNodeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33baa-110">Identificateur du nouveau nœud.</span><span class="sxs-lookup"><span data-stu-id="33baa-110">The identifier for the new node.</span></span>

</dd> <dt>

<span data-ttu-id="33baa-111">*pNodeLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33baa-111">*pNodeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33baa-112">Emplacement du nouveau nœud.</span><span class="sxs-lookup"><span data-stu-id="33baa-112">The location of the new node.</span></span>

</dd> <dt>

<span data-ttu-id="33baa-113">*pPartiallyPopulatedContextNodeCreated* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="33baa-113">*pPartiallyPopulatedContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33baa-114">Pointeur vers le nouveau [**IContextNode**](icontextnode.md)partiellement rempli.</span><span class="sxs-lookup"><span data-stu-id="33baa-114">A pointer to the new, partially populated [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33baa-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33baa-115">Return value</span></span>

<span data-ttu-id="33baa-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="33baa-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33baa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="33baa-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="33baa-118">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *pPartiallyPopulatedContextNodeCreated* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="33baa-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pPartiallyPopulatedContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="33baa-119">Le nouveau [**IContextNode**](icontextnode.md) est ajouté à la collection de nœuds enfants de ce nœud de contexte (consultez [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="33baa-119">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="33baa-120">Lorsqu’il existe des nœuds enfants existants, le nouveau **IContextNode** créé est ajouté en tant que dernier nœud enfant.</span><span class="sxs-lookup"><span data-stu-id="33baa-120">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="33baa-121">Pour plus d’informations sur le type, l’identificateur et l’emplacement, consultez [**IContextNode :: GetType**](icontextnode-gettype.md), [**IContextNode :: GetId**](icontextnode-getid.md)et [**IContextNode :: GetLocation**](icontextnode-getlocation.md).</span><span class="sxs-lookup"><span data-stu-id="33baa-121">For more information about type, identifier, and location, see [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md), and [**IContextNode::GetLocation**](icontextnode-getlocation.md).</span></span>

<span data-ttu-id="33baa-122">Cette méthode est utilisée pour le proxy de données comme moyen de créer un objet [**IContextNode**](icontextnode.md) dans l’arborescence de nœuds de contexte avant que toutes les informations le concernant soient disponibles.</span><span class="sxs-lookup"><span data-stu-id="33baa-122">This method is used for data proxy as a way to create an [**IContextNode**](icontextnode.md) object in the context node tree before all the information about it is available.</span></span> <span data-ttu-id="33baa-123">Pour plus d’informations, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="33baa-123">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33baa-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33baa-124">Requirements</span></span>



| <span data-ttu-id="33baa-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33baa-125">Requirement</span></span> | <span data-ttu-id="33baa-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="33baa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33baa-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33baa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="33baa-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33baa-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33baa-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33baa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="33baa-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="33baa-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="33baa-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="33baa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="33baa-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="33baa-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33baa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="33baa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33baa-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33baa-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="33baa-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33baa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33baa-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="33baa-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="33baa-137">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="33baa-137">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="33baa-138">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="33baa-138">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="33baa-139">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="33baa-139">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="33baa-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="33baa-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

