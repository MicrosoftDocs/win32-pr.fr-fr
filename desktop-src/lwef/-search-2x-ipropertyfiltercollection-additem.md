---
title: IPropertyFilterCollection, propriété AddItem (WdsSharedIDL. h)
description: Ajoute un nouveau filtre à la collection.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- AddItem, propriété fonctionnalités d’environnement Windows héritées
- AddItem, propriété fonctionnalités de l’environnement Windows héritées, interface IPropertyFilterCollection
- Interface IPropertyFilterCollection fonctionnalités de l’environnement Windows héritées, propriété AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032716"
---
# <a name="ipropertyfiltercollectionadditem-property"></a><span data-ttu-id="9329e-106">IPropertyFilterCollection :: AddItem, propriété</span><span class="sxs-lookup"><span data-stu-id="9329e-106">IPropertyFilterCollection::AddItem property</span></span>

> [!NOTE]
> <span data-ttu-id="9329e-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9329e-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9329e-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="9329e-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9329e-109">Ajoute un nouveau filtre à la collection.</span><span class="sxs-lookup"><span data-stu-id="9329e-109">Adds a new filter to the collection.</span></span>

<span data-ttu-id="9329e-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9329e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9329e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9329e-111">Syntax</span></span>


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="9329e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9329e-112">Property value</span></span>

<span data-ttu-id="9329e-113">retourne un pointeur vers l’adresse du nouveau filtre.</span><span class="sxs-lookup"><span data-stu-id="9329e-113">returns a pointer to the address for the new filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9329e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9329e-114">Requirements</span></span>



| <span data-ttu-id="9329e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9329e-115">Requirement</span></span> | <span data-ttu-id="9329e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9329e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9329e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9329e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9329e-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9329e-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9329e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9329e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9329e-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9329e-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9329e-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9329e-121">Redistributable</span></span><br/>          | <span data-ttu-id="9329e-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="9329e-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9329e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9329e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9329e-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9329e-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





