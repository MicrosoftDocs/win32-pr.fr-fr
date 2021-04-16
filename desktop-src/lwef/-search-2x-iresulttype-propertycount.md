---
title: IResultType PropertyCount, propriété (WdsSharedIDL. h)
description: Cette propriété contient le nombre de propriétés exposées par le type.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Propriétés PropertyCount héritées fonctionnalités de l’environnement Windows
- Propriété PropertyCount fonctionnalités de l’environnement Windows héritées, interface IResultType
- Interface IResultType fonctionnalités d’environnement Windows héritées, propriété PropertyCount
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508317"
---
# <a name="iresulttypepropertycount-property"></a><span data-ttu-id="ca2a8-106">IResultType ::P propriété ropertyCount</span><span class="sxs-lookup"><span data-stu-id="ca2a8-106">IResultType::PropertyCount property</span></span>

> [!NOTE]
> <span data-ttu-id="ca2a8-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ca2a8-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ca2a8-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="ca2a8-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="ca2a8-109">Cette propriété contient le nombre de propriétés exposées par le type.</span><span class="sxs-lookup"><span data-stu-id="ca2a8-109">This property contains the number of properties exposed by the type.</span></span>

<span data-ttu-id="ca2a8-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ca2a8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2a8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca2a8-111">Syntax</span></span>


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="ca2a8-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ca2a8-112">Property value</span></span>

<span data-ttu-id="ca2a8-113">retourne l’adresse du nombre de propriétés exposées.</span><span class="sxs-lookup"><span data-stu-id="ca2a8-113">returns the address of the number of properties exposed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2a8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca2a8-114">Requirements</span></span>



| <span data-ttu-id="ca2a8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca2a8-115">Requirement</span></span> | <span data-ttu-id="ca2a8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca2a8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2a8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca2a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2a8-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca2a8-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ca2a8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca2a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2a8-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca2a8-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ca2a8-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ca2a8-121">Redistributable</span></span><br/>          | <span data-ttu-id="ca2a8-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="ca2a8-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="ca2a8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca2a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca2a8-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca2a8-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





