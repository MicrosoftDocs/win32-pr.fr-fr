---
description: Contient une collection d’objets qui implémentent l’interface IContextLink.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Interface IContextLinks (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951224"
---
# <a name="icontextlinks-interface"></a><span data-ttu-id="8b761-103">Interface IContextLinks</span><span class="sxs-lookup"><span data-stu-id="8b761-103">IContextLinks interface</span></span>

<span data-ttu-id="8b761-104">Contient une collection d’objets qui implémentent l’interface [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="8b761-104">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="8b761-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8b761-105">Members</span></span>

<span data-ttu-id="8b761-106">L’interface **IContextLinks** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b761-106">The **IContextLinks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b761-107">**IContextLinks** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b761-107">**IContextLinks** also has these types of members:</span></span>

-   [<span data-ttu-id="8b761-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b761-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b761-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b761-109">Methods</span></span>

<span data-ttu-id="8b761-110">L’interface **IContextLinks** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8b761-110">The **IContextLinks** interface has these methods.</span></span>



| <span data-ttu-id="8b761-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="8b761-111">Method</span></span>                                                 | <span data-ttu-id="8b761-112">Description</span><span class="sxs-lookup"><span data-stu-id="8b761-112">Description</span></span>                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b761-113">**GetContextLink**</span><span class="sxs-lookup"><span data-stu-id="8b761-113">**GetContextLink**</span></span>](icontextlinks-getcontextlink.md) | <span data-ttu-id="8b761-114">Récupère le [**IContextLink**](icontextlink.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8b761-114">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span><br/>               |
| [<span data-ttu-id="8b761-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="8b761-115">**GetCount**</span></span>](icontextlinks-getcount.md)             | <span data-ttu-id="8b761-116">Récupère le nombre d’objets [**IContextLink**](icontextlink.md) dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="8b761-116">Retrieves the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b761-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8b761-117">Remarks</span></span>

<span data-ttu-id="8b761-118">Cette méthode est généralement accessible par le biais de la méthode [**IContextNode :: GetContextLinks**](icontextnode-getcontextlinks.md) .</span><span class="sxs-lookup"><span data-stu-id="8b761-118">This is usually accessed through the [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b761-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b761-119">Requirements</span></span>



| <span data-ttu-id="8b761-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b761-120">Requirement</span></span> | <span data-ttu-id="8b761-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b761-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b761-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b761-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b761-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b761-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8b761-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b761-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b761-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b761-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8b761-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b761-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b761-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8b761-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8b761-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8b761-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b761-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b761-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8b761-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b761-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b761-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="8b761-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="8b761-132">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="8b761-132">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="8b761-133">**IContextNode ::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="8b761-133">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="8b761-134">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="8b761-134">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="8b761-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="8b761-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

