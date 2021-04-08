---
title: Propriété HelpText IResultVerb (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers la chaîne d’aide localisée pour le verbe.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- Propriété HelpText fonctionnalités d’environnement Windows héritées
- Propriété HelpText fonctionnalités d’environnement Windows héritées, interface IResultVerb
- Interface IResultVerb fonctionnalités de l’environnement Windows héritées, propriété HelpText
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741036"
---
# <a name="iresultverbhelptext-property"></a><span data-ttu-id="d2c58-106">IResultVerb :: HelpText, propriété</span><span class="sxs-lookup"><span data-stu-id="d2c58-106">IResultVerb::HelpText property</span></span>

> [!NOTE]
> <span data-ttu-id="d2c58-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d2c58-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d2c58-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d2c58-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d2c58-109">Cette propriété retourne un pointeur vers la chaîne d’aide localisée pour le verbe.</span><span class="sxs-lookup"><span data-stu-id="d2c58-109">This property returns a pointer to the localized help string for the verb.</span></span>

<span data-ttu-id="d2c58-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d2c58-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c58-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2c58-111">Syntax</span></span>


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="d2c58-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d2c58-112">Property value</span></span>

<span data-ttu-id="d2c58-113">La valeur de cette propriété est un pointeur vers la chaîne d’aide localisée pour ce verbe.</span><span class="sxs-lookup"><span data-stu-id="d2c58-113">The value of this property is a pointer to the localized help string for this verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c58-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2c58-114">Requirements</span></span>



| <span data-ttu-id="d2c58-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2c58-115">Requirement</span></span> | <span data-ttu-id="d2c58-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2c58-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c58-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2c58-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c58-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2c58-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d2c58-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2c58-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c58-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2c58-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d2c58-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d2c58-121">Redistributable</span></span><br/>          | <span data-ttu-id="d2c58-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="d2c58-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="d2c58-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2c58-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c58-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c58-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





