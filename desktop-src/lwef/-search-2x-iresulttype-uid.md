---
title: Propriété UID IResultType (WdsSharedIDL. h)
description: Cette propriété contient l’identificateur unique pour le type.
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- Propriété UID fonctionnalités d’environnement Windows héritées
- Propriété UID fonctionnalités d’environnement Windows héritées, interface IResultType
- Interface IResultType fonctionnalités d’environnement Windows héritées, propriété UID
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbdd5a9b17da9cde04ac0b371a885b07415d0e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106303"
---
# <a name="iresulttypeuid-property"></a><span data-ttu-id="c6e6c-106">IResultType :: UID, propriété</span><span class="sxs-lookup"><span data-stu-id="c6e6c-106">IResultType::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="c6e6c-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c6e6c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c6e6c-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c6e6c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c6e6c-109">Cette propriété contient l’identificateur unique pour le type.</span><span class="sxs-lookup"><span data-stu-id="c6e6c-109">This property contains the unique identifier for the type.</span></span>

<span data-ttu-id="c6e6c-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c6e6c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e6c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6e6c-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="c6e6c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c6e6c-112">Property value</span></span>

<span data-ttu-id="c6e6c-113">adresse de l’emplacement contenant l’UID.</span><span class="sxs-lookup"><span data-stu-id="c6e6c-113">the address of the location containing the uid.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e6c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6e6c-114">Requirements</span></span>



| <span data-ttu-id="c6e6c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6e6c-115">Requirement</span></span> | <span data-ttu-id="c6e6c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6e6c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e6c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e6c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e6c-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e6c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c6e6c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e6c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e6c-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e6c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c6e6c-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c6e6c-121">Redistributable</span></span><br/>          | <span data-ttu-id="c6e6c-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c6e6c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="c6e6c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6e6c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e6c-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6e6c-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





