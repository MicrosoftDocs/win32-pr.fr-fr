---
title: IPropertyFilterCollection, propriété GetITem (WdsSharedIDL. h)
description: Retourne un filtre spécifique dans la collection.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Propriété GetITem fonctionnalités de l’environnement Windows héritées
- Propriété GetITem fonctionnalités de l’environnement Windows héritées, interface IPropertyFilterCollection
- Interface IPropertyFilterCollection fonctionnalités de l’environnement Windows héritées, propriété GetITem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941977"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a><span data-ttu-id="8dfbc-106">IPropertyFilterCollection :: GetITem, propriété</span><span class="sxs-lookup"><span data-stu-id="8dfbc-106">IPropertyFilterCollection::GetITem property</span></span>

> [!NOTE]
> <span data-ttu-id="8dfbc-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8dfbc-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8dfbc-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfbc-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8dfbc-109">Retourne un filtre spécifique dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8dfbc-109">Returns a specific filter within the collection.</span></span>

<span data-ttu-id="8dfbc-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8dfbc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfbc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dfbc-111">Syntax</span></span>


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="8dfbc-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8dfbc-112">Property value</span></span>

<span data-ttu-id="8dfbc-113">Définit l’adresse du filtre.</span><span class="sxs-lookup"><span data-stu-id="8dfbc-113">Sets the address of the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dfbc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dfbc-114">Requirements</span></span>



| <span data-ttu-id="8dfbc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dfbc-115">Requirement</span></span> | <span data-ttu-id="8dfbc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dfbc-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfbc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dfbc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfbc-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dfbc-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8dfbc-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dfbc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfbc-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dfbc-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8dfbc-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8dfbc-121">Redistributable</span></span><br/>          | <span data-ttu-id="8dfbc-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8dfbc-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="8dfbc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8dfbc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dfbc-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dfbc-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





