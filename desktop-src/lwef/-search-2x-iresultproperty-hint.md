---
title: Propriété de l’indicateur IResultProperty (WdsSharedIDL. h)
description: Valeur spéciale utilisée pour faciliter la récupération de données.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Propriété d’indicateur fonctionnalités héritées de l’environnement Windows
- Propriété d’indicateur fonctionnalités héritées de l’environnement Windows, interface IResultProperty
- Interface IResultProperty fonctionnalités de l’environnement Windows héritées, propriété Hint
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512381"
---
# <a name="iresultpropertyhint-property"></a><span data-ttu-id="19417-106">IResultProperty :: Hint, propriété</span><span class="sxs-lookup"><span data-stu-id="19417-106">IResultProperty::Hint property</span></span>

> [!NOTE]
> <span data-ttu-id="19417-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="19417-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="19417-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="19417-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="19417-109">Valeur spéciale utilisée pour faciliter la récupération de données.</span><span class="sxs-lookup"><span data-stu-id="19417-109">Special value used to aid data retrieval.</span></span>

<span data-ttu-id="19417-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="19417-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="19417-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19417-111">Syntax</span></span>


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a><span data-ttu-id="19417-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="19417-112">Property value</span></span>

<span data-ttu-id="19417-113">retourne un pointeur désignant l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="19417-113">returns a pointer to the hint.</span></span>

## <a name="requirements"></a><span data-ttu-id="19417-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19417-114">Requirements</span></span>



| <span data-ttu-id="19417-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19417-115">Requirement</span></span> | <span data-ttu-id="19417-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="19417-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="19417-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19417-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19417-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19417-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="19417-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19417-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19417-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19417-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="19417-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="19417-121">Redistributable</span></span><br/>          | <span data-ttu-id="19417-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="19417-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="19417-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="19417-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19417-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="19417-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





