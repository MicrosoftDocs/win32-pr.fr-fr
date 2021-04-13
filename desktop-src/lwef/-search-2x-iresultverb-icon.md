---
title: IResultVerb Icon, propriété (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers un handle de l’icône facultative associée au verbe.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Propriété Icon fonctionnalités de l’environnement Windows hérité
- Propriété Icon fonctionnalités de l’environnement Windows héritées, interface IResultVerb
- Interface IResultVerb fonctionnalités de l’environnement Windows héritées, propriété Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465942"
---
# <a name="iresultverbicon-property"></a><span data-ttu-id="73322-106">IResultVerb :: Icon, propriété</span><span class="sxs-lookup"><span data-stu-id="73322-106">IResultVerb::Icon property</span></span>

> [!NOTE]
> <span data-ttu-id="73322-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73322-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="73322-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="73322-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="73322-109">Cette propriété retourne un pointeur vers un handle de l’icône facultative associée au verbe.</span><span class="sxs-lookup"><span data-stu-id="73322-109">This property returns a pointer to handle of the optional icon associated with the verb.</span></span>

<span data-ttu-id="73322-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="73322-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73322-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73322-111">Syntax</span></span>


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a><span data-ttu-id="73322-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="73322-112">Property value</span></span>

<span data-ttu-id="73322-113">HICON est un pointeur vers le handle de l’icône facultative assocuated avec le verbe.</span><span class="sxs-lookup"><span data-stu-id="73322-113">hicon is a pointer to the handle of the optional icon assocuated with the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="73322-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73322-114">Requirements</span></span>



| <span data-ttu-id="73322-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73322-115">Requirement</span></span> | <span data-ttu-id="73322-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="73322-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="73322-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73322-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73322-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73322-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="73322-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73322-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73322-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73322-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="73322-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="73322-121">Redistributable</span></span><br/>          | <span data-ttu-id="73322-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="73322-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="73322-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="73322-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="73322-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="73322-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





