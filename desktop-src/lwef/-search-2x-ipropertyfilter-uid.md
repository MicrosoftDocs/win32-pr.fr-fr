---
title: Propriété UID IPropertyFilter (WdsSharedIDL. h)
description: UID pour la propriété sur laquelle filtrer.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- Propriété UID fonctionnalités d’environnement Windows héritées
- Propriété UID fonctionnalités d’environnement Windows héritées, interface IPropertyFilter
- Interface IPropertyFilter fonctionnalités d’environnement Windows héritées, propriété UID
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317337"
---
# <a name="ipropertyfilteruid-property"></a><span data-ttu-id="1e752-106">IPropertyFilter :: UID, propriété</span><span class="sxs-lookup"><span data-stu-id="1e752-106">IPropertyFilter::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="1e752-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1e752-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="1e752-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="1e752-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="1e752-109">UID pour la propriété sur laquelle filtrer.</span><span class="sxs-lookup"><span data-stu-id="1e752-109">UID for the property to filter by.</span></span>

<span data-ttu-id="1e752-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1e752-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e752-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e752-111">Syntax</span></span>


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="1e752-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1e752-112">Property value</span></span>

<span data-ttu-id="1e752-113">Définit la propriété UID.</span><span class="sxs-lookup"><span data-stu-id="1e752-113">Sets the UID property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e752-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e752-114">Requirements</span></span>



| <span data-ttu-id="1e752-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e752-115">Requirement</span></span> | <span data-ttu-id="1e752-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e752-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e752-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e752-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1e752-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e752-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1e752-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e752-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1e752-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e752-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1e752-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1e752-121">Redistributable</span></span><br/>          | <span data-ttu-id="1e752-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="1e752-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="1e752-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e752-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e752-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e752-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





