---
title: Propriété DisplayName IResultVerb (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Propriété DisplayName fonctionnalités d’environnement Windows héritées
- Propriété DisplayName fonctionnalités d’environnement Windows héritées, interface IResultVerb
- Interface IResultVerb fonctionnalités d’environnement Windows héritées, propriété DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032713"
---
# <a name="iresultverbdisplayname-property"></a><span data-ttu-id="7f1a5-106">IResultVerb ::D propriété isplayName</span><span class="sxs-lookup"><span data-stu-id="7f1a5-106">IResultVerb::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="7f1a5-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7f1a5-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7f1a5-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="7f1a5-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7f1a5-109">Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.</span><span class="sxs-lookup"><span data-stu-id="7f1a5-109">This property returns a pointer to the localized display name for the verb.</span></span>

<span data-ttu-id="7f1a5-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7f1a5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f1a5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f1a5-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a><span data-ttu-id="7f1a5-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7f1a5-112">Property value</span></span>

<span data-ttu-id="7f1a5-113">Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.</span><span class="sxs-lookup"><span data-stu-id="7f1a5-113">This property returns a pointer to the localized display name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f1a5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f1a5-114">Requirements</span></span>



| <span data-ttu-id="7f1a5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f1a5-115">Requirement</span></span> | <span data-ttu-id="7f1a5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f1a5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1a5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f1a5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7f1a5-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f1a5-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7f1a5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f1a5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7f1a5-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f1a5-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7f1a5-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7f1a5-121">Redistributable</span></span><br/>          | <span data-ttu-id="7f1a5-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="7f1a5-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7f1a5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f1a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f1a5-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f1a5-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





