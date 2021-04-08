---
title: Propriété Count IPropertyFilterCollection (WdsSharedIDL. h)
description: Nombre de filtres dans la collection.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- Propriété Count fonctionnalités héritées de l’environnement Windows
- Propriété Count fonctionnalités de l’environnement Windows héritées, interface IPropertyFilterCollection
- Interface IPropertyFilterCollection fonctionnalités de l’environnement Windows héritées, propriété Count
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258a2ca8089cecb8e2e15fbe7e9e92ce1ed3468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741045"
---
# <a name="ipropertyfiltercollectioncount-property"></a><span data-ttu-id="687a0-106">IPropertyFilterCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="687a0-106">IPropertyFilterCollection::Count property</span></span>

> [!NOTE]
> <span data-ttu-id="687a0-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="687a0-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="687a0-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="687a0-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="687a0-109">Nombre de filtres dans la collection.</span><span class="sxs-lookup"><span data-stu-id="687a0-109">Number of filters in the collection.</span></span>

<span data-ttu-id="687a0-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="687a0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="687a0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="687a0-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="687a0-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="687a0-112">Property value</span></span>

<span data-ttu-id="687a0-113">retourne un pointeur vers le nombre de filtres dans la collection.</span><span class="sxs-lookup"><span data-stu-id="687a0-113">returns a pointer to the number of filters in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="687a0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="687a0-114">Requirements</span></span>



| <span data-ttu-id="687a0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="687a0-115">Requirement</span></span> | <span data-ttu-id="687a0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="687a0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="687a0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="687a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="687a0-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="687a0-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="687a0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="687a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="687a0-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="687a0-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="687a0-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="687a0-121">Redistributable</span></span><br/>          | <span data-ttu-id="687a0-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="687a0-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="687a0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="687a0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="687a0-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="687a0-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





