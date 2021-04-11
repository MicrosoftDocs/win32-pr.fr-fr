---
title: Propriété UID IResultProperty (WdsSharedIDL. h)
description: Identificateur unique de la propriété.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- Propriété UID fonctionnalités d’environnement Windows héritées
- Propriété UID fonctionnalités d’environnement Windows héritées, interface IResultProperty
- Interface IResultProperty fonctionnalités d’environnement Windows héritées, propriété UID
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032715"
---
# <a name="iresultpropertyuid-property"></a><span data-ttu-id="da2db-106">IResultProperty :: UID, propriété</span><span class="sxs-lookup"><span data-stu-id="da2db-106">IResultProperty::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="da2db-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="da2db-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="da2db-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="da2db-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="da2db-109">Identificateur unique de la propriété.</span><span class="sxs-lookup"><span data-stu-id="da2db-109">Unique identifier for the property.</span></span>

<span data-ttu-id="da2db-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="da2db-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da2db-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da2db-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="da2db-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="da2db-112">Property value</span></span>

<span data-ttu-id="da2db-113">retourne un pointeur vers l’identificateur de propriété unique.</span><span class="sxs-lookup"><span data-stu-id="da2db-113">returns a pointer to the unique property identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="da2db-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da2db-114">Requirements</span></span>



| <span data-ttu-id="da2db-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da2db-115">Requirement</span></span> | <span data-ttu-id="da2db-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="da2db-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2db-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da2db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da2db-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da2db-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="da2db-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da2db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da2db-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da2db-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="da2db-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="da2db-121">Redistributable</span></span><br/>          | <span data-ttu-id="da2db-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="da2db-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="da2db-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="da2db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="da2db-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2db-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





