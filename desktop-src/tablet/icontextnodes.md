---
description: Contient une collection d’objets qui implémentent l’interface IContextNode et qui sont le résultat d’une opération d’analyse d’encre.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interface IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516270"
---
# <a name="icontextnodes-interface"></a><span data-ttu-id="ecec6-103">Interface IContextNodes</span><span class="sxs-lookup"><span data-stu-id="ecec6-103">IContextNodes interface</span></span>

<span data-ttu-id="ecec6-104">Contient une collection d’objets qui implémentent l’interface [**IContextNode**](icontextnode.md) et qui sont le résultat d’une opération d’analyse d’encre.</span><span class="sxs-lookup"><span data-stu-id="ecec6-104">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="ecec6-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ecec6-105">Members</span></span>

<span data-ttu-id="ecec6-106">L’interface **IContextNodes** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ecec6-106">The **IContextNodes** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ecec6-107">**IContextNodes** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ecec6-107">**IContextNodes** also has these types of members:</span></span>

-   [<span data-ttu-id="ecec6-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ecec6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ecec6-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ecec6-109">Methods</span></span>

<span data-ttu-id="ecec6-110">L’interface **IContextNodes** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ecec6-110">The **IContextNodes** interface has these methods.</span></span>



| <span data-ttu-id="ecec6-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="ecec6-111">Method</span></span>                                                       | <span data-ttu-id="ecec6-112">Description</span><span class="sxs-lookup"><span data-stu-id="ecec6-112">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecec6-113">**AddContextNode**</span><span class="sxs-lookup"><span data-stu-id="ecec6-113">**AddContextNode**</span></span>](icontextnodes-addcontextnode.md)       | <span data-ttu-id="ecec6-114">Ajoute un objet [**IContextNode**](icontextnode.md) à cette collection.</span><span class="sxs-lookup"><span data-stu-id="ecec6-114">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span> <br/>                                  |
| [<span data-ttu-id="ecec6-115">**GetContextNode**</span><span class="sxs-lookup"><span data-stu-id="ecec6-115">**GetContextNode**</span></span>](icontextnodes-getcontextnode.md)       | <span data-ttu-id="ecec6-116">Récupère l’objet [**IContextNode**](icontextnode.md) à l’index spécifié dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="ecec6-116">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span> <br/> |
| [<span data-ttu-id="ecec6-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="ecec6-117">**GetCount**</span></span>](icontextnodes-getcount.md)                   | <span data-ttu-id="ecec6-118">Récupère le nombre d’objets [**IContextNode**](icontextnode.md) contenus dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="ecec6-118">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span> <br/>       |
| [<span data-ttu-id="ecec6-119">**RemoveContextNode**</span><span class="sxs-lookup"><span data-stu-id="ecec6-119">**RemoveContextNode**</span></span>](icontextnodes-removecontextnode.md) | <span data-ttu-id="ecec6-120">Supprime un objet [**IContextNode**](icontextnode.md) de cette collection.</span><span class="sxs-lookup"><span data-stu-id="ecec6-120">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span> <br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="ecec6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecec6-121">Requirements</span></span>



| <span data-ttu-id="ecec6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecec6-122">Requirement</span></span> | <span data-ttu-id="ecec6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecec6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecec6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecec6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ecec6-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecec6-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ecec6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecec6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ecec6-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecec6-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ecec6-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecec6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecec6-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ecec6-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ecec6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ecec6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecec6-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecec6-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ecec6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecec6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecec6-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ecec6-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ecec6-134">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="ecec6-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

