---
description: Récupère une collection d’objets IContextLink qui représentent des relations avec d’autres objets IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'IContextNode :: GetContextLinks, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514633"
---
# <a name="icontextnodegetcontextlinks-method"></a><span data-ttu-id="a0dcc-103">IContextNode :: GetContextLinks, méthode</span><span class="sxs-lookup"><span data-stu-id="a0dcc-103">IContextNode::GetContextLinks method</span></span>

<span data-ttu-id="a0dcc-104">Récupère une collection d’objets [**IContextLink**](icontextlink.md) qui représentent des relations avec d’autres objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="a0dcc-104">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0dcc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0dcc-105">Syntax</span></span>


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a><span data-ttu-id="a0dcc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0dcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0dcc-107">*ppContextLinks* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a0dcc-107">*ppContextLinks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0dcc-108">Pointeur vers une collection d’objets [**IContextLink**](icontextlink.md) qui représente des relations avec d’autres objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="a0dcc-108">A pointer to a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0dcc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0dcc-109">Return value</span></span>

<span data-ttu-id="a0dcc-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a0dcc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0dcc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a0dcc-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a0dcc-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextLinks* lorsque vous n’avez plus besoin d’utiliser la collection de liens de contexte.</span><span class="sxs-lookup"><span data-stu-id="a0dcc-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinks* when you no longer need to use the context links collection.</span></span>

 

<span data-ttu-id="a0dcc-113">Pour obtenir des informations sur les relations de nœud parent ou enfant, utilisez [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md) ou [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md).</span><span class="sxs-lookup"><span data-stu-id="a0dcc-113">To get information about parent or child node relationships, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) or [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).</span></span>

<span data-ttu-id="a0dcc-114">Pour plus d’informations sur les genres de relations qui sont décrits par les liens, consultez [**IContextLink**](icontextlink.md) et [**ContextLinkDirection**](contextlinkdirection.md).</span><span class="sxs-lookup"><span data-stu-id="a0dcc-114">For more information about the kinds of relationships that are described by links, see [**IContextLink**](icontextlink.md) and [**ContextLinkDirection**](contextlinkdirection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0dcc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0dcc-115">Requirements</span></span>



| <span data-ttu-id="a0dcc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0dcc-116">Requirement</span></span> | <span data-ttu-id="a0dcc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0dcc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dcc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0dcc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a0dcc-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0dcc-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0dcc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0dcc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a0dcc-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0dcc-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a0dcc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0dcc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0dcc-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a0dcc-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a0dcc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a0dcc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0dcc-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0dcc-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a0dcc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0dcc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0dcc-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a0dcc-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="a0dcc-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="a0dcc-130">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="a0dcc-130">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="a0dcc-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a0dcc-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

