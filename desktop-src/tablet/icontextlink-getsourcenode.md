---
description: Récupère l’objet IContextNode qui est la source de ce IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'IContextLink :: GetSourceNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201510"
---
# <a name="icontextlinkgetsourcenode-method"></a><span data-ttu-id="d3dc4-103">IContextLink :: GetSourceNode, méthode</span><span class="sxs-lookup"><span data-stu-id="d3dc4-103">IContextLink::GetSourceNode method</span></span>

<span data-ttu-id="d3dc4-104">Récupère l’objet [**IContextNode**](icontextnode.md) qui est la source de ce [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="d3dc4-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3dc4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3dc4-105">Syntax</span></span>


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="d3dc4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3dc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3dc4-107">*ppSrcContextNodeId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d3dc4-107">*ppSrcContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3dc4-108">Pointeur vers l’objet [**IContextNode**](icontextnode.md) qui est la source de ce [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="d3dc4-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3dc4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3dc4-109">Return value</span></span>

<span data-ttu-id="d3dc4-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="d3dc4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3dc4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d3dc4-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d3dc4-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppSrcContextNodeId* lorsque vous n’avez plus besoin d’utiliser le nœud source.</span><span class="sxs-lookup"><span data-stu-id="d3dc4-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSrcContextNodeId* when you no longer need to use the source node.</span></span>

 

<span data-ttu-id="d3dc4-113">Si l’objet [**IContextLink**](icontextlink.md) est lié entre un nœud qui contient l’écriture et un nœud qui contient Drawing, le nœud source est généralement le nœud qui contient Drawing.</span><span class="sxs-lookup"><span data-stu-id="d3dc4-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the source node is generally the node that contains drawing.</span></span>

<span data-ttu-id="d3dc4-114">Si l’objet [**IContextLink**](icontextlink.md) a un type de lien (voir [**IContextLink :: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), le nœud source est le nœud qui englobe le nœud de destination.</span><span class="sxs-lookup"><span data-stu-id="d3dc4-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the source node is the node that encloses the destination node.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3dc4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3dc4-115">Requirements</span></span>



| <span data-ttu-id="d3dc4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3dc4-116">Requirement</span></span> | <span data-ttu-id="d3dc4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3dc4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3dc4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3dc4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d3dc4-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3dc4-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3dc4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3dc4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d3dc4-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3dc4-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d3dc4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3dc4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3dc4-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d3dc4-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d3dc4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d3dc4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3dc4-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3dc4-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d3dc4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3dc4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3dc4-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="d3dc4-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="d3dc4-128">**IContextLink::GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="d3dc4-128">**IContextLink::GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)
</dt> <dt>

[<span data-ttu-id="d3dc4-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="d3dc4-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="d3dc4-130">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="d3dc4-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

