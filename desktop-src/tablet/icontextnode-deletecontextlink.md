---
description: Supprime un objet IContextLink de la collection de liens de l’objet IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: IContextNode ::D méthode eleteContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538855"
---
# <a name="icontextnodedeletecontextlink-method"></a><span data-ttu-id="7613c-103">IContextNode ::D méthode eleteContextLink</span><span class="sxs-lookup"><span data-stu-id="7613c-103">IContextNode::DeleteContextLink method</span></span>

<span data-ttu-id="7613c-104">Supprime un objet [**IContextLink**](icontextlink.md) de la collection de liens de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="7613c-104">Deletes an [**IContextLink**](icontextlink.md) object from the [**IContextNode**](icontextnode.md) object's link collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7613c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7613c-105">Syntax</span></span>


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="7613c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7613c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7613c-107">*pContextLinkToDelete* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7613c-107">*pContextLinkToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7613c-108">Objet [**IContextLink**](icontextlink.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="7613c-108">The [**IContextLink**](icontextlink.md) object to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7613c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7613c-109">Return value</span></span>

<span data-ttu-id="7613c-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="7613c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7613c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7613c-111">Remarks</span></span>

<span data-ttu-id="7613c-112">Un lien de contexte a un nœud source et un nœud de destination (voir [**IContextLink :: GetSourceNode**](icontextlink-getsourcenode.md) et [**IContextLink :: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="7613c-112">A context link has a source node and a destination node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span> <span data-ttu-id="7613c-113">Cette méthode supprime le [**IContextLink**](icontextlink.md) de la collection de liens de contexte des nœuds source et de destination (voir [**IContextNode :: GetContextLinks**](icontextnode-getcontextlinks.md)).</span><span class="sxs-lookup"><span data-stu-id="7613c-113">This method removes the [**IContextLink**](icontextlink.md) from both the source and destination nodes' collection of context links (see [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="7613c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7613c-114">Requirements</span></span>



| <span data-ttu-id="7613c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7613c-115">Requirement</span></span> | <span data-ttu-id="7613c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7613c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7613c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7613c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7613c-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7613c-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7613c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7613c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7613c-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7613c-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7613c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7613c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7613c-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7613c-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7613c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7613c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7613c-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7613c-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7613c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7613c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7613c-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7613c-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7613c-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="7613c-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="7613c-128">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="7613c-128">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="7613c-129">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="7613c-129">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="7613c-130">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="7613c-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




