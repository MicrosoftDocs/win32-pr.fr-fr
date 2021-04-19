---
description: Ajoute un nouveau IContextLink à la collection de liens de contexte de l’objet IContextNode.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'IContextNode :: AddContextLink, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516678"
---
# <a name="icontextnodeaddcontextlink-method"></a><span data-ttu-id="b5239-103">IContextNode :: AddContextLink, méthode</span><span class="sxs-lookup"><span data-stu-id="b5239-103">IContextNode::AddContextLink method</span></span>

<span data-ttu-id="b5239-104">Ajoute un nouveau [**IContextLink**](icontextlink.md) à la collection de liens de contexte de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b5239-104">Adds a new [**IContextLink**](icontextlink.md) to the [**IContextNode**](icontextnode.md) object's collection of context links.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5239-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5239-105">Syntax</span></span>


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a><span data-ttu-id="b5239-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5239-107">*pDestinationNode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5239-107">*pDestinationNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5239-108">[**IContextNode**](icontextnode.md) de destination pour le nouveau [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="b5239-108">The destination [**IContextNode**](icontextnode.md) for the new [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5239-109">*linkDirection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5239-109">*linkDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5239-110">Direction de l’objet [**IContextLink**](icontextlink.md) à créer.</span><span class="sxs-lookup"><span data-stu-id="b5239-110">The direction of [**IContextLink**](icontextlink.md) object to create.</span></span>

</dd> <dt>

<span data-ttu-id="b5239-111">*ppContextLinkToAdd* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b5239-111">*ppContextLinkToAdd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5239-112">Pointeur vers le nouvel objet [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="b5239-112">A pointer to the new [**IContextLink**](icontextlink.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5239-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5239-113">Return value</span></span>

<span data-ttu-id="b5239-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b5239-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5239-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b5239-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b5239-116">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextLinkToAdd* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="b5239-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinkToAdd* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="b5239-117">Cet objet [**IContextNode**](icontextnode.md) est le nœud source (consultez [**IContextLink :: GetSourceNode**](icontextlink-getsourcenode.md)) pour le nouvel objet [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="b5239-117">This [**IContextNode**](icontextnode.md) object is the source node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) for the new [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5239-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5239-118">Requirements</span></span>



| <span data-ttu-id="b5239-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5239-119">Requirement</span></span> | <span data-ttu-id="b5239-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5239-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5239-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5239-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5239-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5239-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5239-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5239-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5239-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5239-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b5239-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5239-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5239-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b5239-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b5239-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b5239-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5239-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5239-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b5239-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5239-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5239-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b5239-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b5239-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="b5239-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="b5239-132">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="b5239-132">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="b5239-133">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="b5239-133">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="b5239-134">**IContextNode ::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="b5239-134">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="b5239-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="b5239-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="b5239-136">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b5239-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

