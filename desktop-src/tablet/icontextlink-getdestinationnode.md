---
description: Récupère l’objet IContextNode qui est la destination de ce IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'IContextLink :: GetDestinationNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318466"
---
# <a name="icontextlinkgetdestinationnode-method"></a><span data-ttu-id="f97a1-103">IContextLink :: GetDestinationNode, méthode</span><span class="sxs-lookup"><span data-stu-id="f97a1-103">IContextLink::GetDestinationNode method</span></span>

<span data-ttu-id="f97a1-104">Récupère l’objet [**IContextNode**](icontextnode.md) qui est la destination de ce [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="f97a1-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f97a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f97a1-105">Syntax</span></span>


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="f97a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f97a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f97a1-107">*ppDstContextNodeId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f97a1-107">*ppDstContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f97a1-108">Pointeur vers l’objet [**IContextNode**](icontextnode.md) qui est la destination de ce [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="f97a1-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f97a1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f97a1-109">Return value</span></span>

<span data-ttu-id="f97a1-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="f97a1-110">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f97a1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f97a1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f97a1-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppDstContextNodeId* lorsque vous n’avez plus besoin d’utiliser le nœud de destination.</span><span class="sxs-lookup"><span data-stu-id="f97a1-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppDstContextNodeId* when you no longer need to use the destination node.</span></span>

 

<span data-ttu-id="f97a1-113">Si l’objet [**IContextLink**](icontextlink.md) est lié entre un nœud qui contient l’écriture et un nœud qui contient Drawing, le nœud de destination est généralement le nœud qui contient l’écriture.</span><span class="sxs-lookup"><span data-stu-id="f97a1-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the destination node is generally the node that contains writing.</span></span>

<span data-ttu-id="f97a1-114">Si l’objet [**IContextLink**](icontextlink.md) a un type de lien (voir [**IContextLink :: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), le nœud de destination est l’objet [**IContextNode**](icontextnode.md) qui est entouré.</span><span class="sxs-lookup"><span data-stu-id="f97a1-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the destination node is the [**IContextNode**](icontextnode.md) object that is enclosed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f97a1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f97a1-115">Requirements</span></span>



| <span data-ttu-id="f97a1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f97a1-116">Requirement</span></span> | <span data-ttu-id="f97a1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f97a1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f97a1-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f97a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f97a1-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f97a1-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f97a1-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f97a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f97a1-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f97a1-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f97a1-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f97a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f97a1-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f97a1-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f97a1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f97a1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f97a1-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f97a1-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f97a1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f97a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f97a1-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="f97a1-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="f97a1-128">**IContextLink::GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="f97a1-128">**IContextLink::GetSourceNode**</span></span>](icontextlink-getsourcenode.md)
</dt> <dt>

[<span data-ttu-id="f97a1-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="f97a1-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="f97a1-130">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="f97a1-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

