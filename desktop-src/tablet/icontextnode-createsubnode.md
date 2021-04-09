---
description: Crée un nouvel objet IContextNode enfant.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'IContextNode :: CreateSubNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862721"
---
# <a name="icontextnodecreatesubnode-method"></a><span data-ttu-id="fc1e6-103">IContextNode :: CreateSubNode, méthode</span><span class="sxs-lookup"><span data-stu-id="fc1e6-103">IContextNode::CreateSubNode method</span></span>

<span data-ttu-id="fc1e6-104">Crée un nouvel objet [**IContextNode**](icontextnode.md) enfant.</span><span class="sxs-lookup"><span data-stu-id="fc1e6-104">Creates a new child [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc1e6-105">Syntax</span></span>


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="fc1e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc1e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc1e6-107">*pNodeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc1e6-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1e6-108">**GUID** qui représente le type de [**IContextNode**](icontextnode.md) à créer.</span><span class="sxs-lookup"><span data-stu-id="fc1e6-108">A **GUID** that represents the type of [**IContextNode**](icontextnode.md) to create.</span></span>

</dd> <dt>

<span data-ttu-id="fc1e6-109">*ppContextNodeCreated* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fc1e6-109">*ppContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1e6-110">Pointeur vers le nouvel [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="fc1e6-110">A pointer to the new [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc1e6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc1e6-111">Return value</span></span>

<span data-ttu-id="fc1e6-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="fc1e6-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1e6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fc1e6-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fc1e6-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextNodeCreated* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="fc1e6-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="fc1e6-115">Le nouveau [**IContextNode**](icontextnode.md) est ajouté à la collection de nœuds enfants de ce nœud de contexte (consultez [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="fc1e6-115">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="fc1e6-116">Lorsqu’il existe des nœuds enfants existants, le nouveau **IContextNode** créé est ajouté en tant que dernier nœud enfant.</span><span class="sxs-lookup"><span data-stu-id="fc1e6-116">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="fc1e6-117">Pour obtenir la liste des types de nœuds de contexte, consultez [types de nœuds de contexte](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="fc1e6-117">For a list of context node types, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1e6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc1e6-118">Requirements</span></span>



| <span data-ttu-id="fc1e6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc1e6-119">Requirement</span></span> | <span data-ttu-id="fc1e6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc1e6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1e6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc1e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1e6-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc1e6-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fc1e6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc1e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1e6-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc1e6-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fc1e6-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc1e6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc1e6-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e6-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fc1e6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fc1e6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc1e6-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e6-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fc1e6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc1e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1e6-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fc1e6-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fc1e6-131">**IContextNode ::D eleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="fc1e6-131">**IContextNode::DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)
</dt> <dt>

[<span data-ttu-id="fc1e6-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="fc1e6-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

