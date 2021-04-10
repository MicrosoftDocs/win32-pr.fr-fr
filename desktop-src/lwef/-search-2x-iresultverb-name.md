---
title: Propriété IResultVerb Name (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers le nom de cononical pour le verbe, tel que imprimer, ouvrir, etc.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Propriété de nom fonctionnalités héritées de l’environnement Windows
- Propriété de nom fonctionnalités de l’environnement Windows héritées, interface IResultVerb
- Interface IResultVerb fonctionnalités de l’environnement Windows héritées, propriété Name
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941723"
---
# <a name="iresultverbname-property"></a><span data-ttu-id="62179-106">IResultVerb :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="62179-106">IResultVerb::Name property</span></span>

> [!NOTE]
> <span data-ttu-id="62179-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="62179-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="62179-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="62179-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="62179-109">Cette propriété retourne un pointeur vers le nom de cononical pour le verbe, tel que imprimer, ouvrir, etc.</span><span class="sxs-lookup"><span data-stu-id="62179-109">This property returns a pointer to the cononical name for the verb such as print, open, etc.</span></span>

<span data-ttu-id="62179-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="62179-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="62179-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62179-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="62179-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="62179-112">Property value</span></span>

<span data-ttu-id="62179-113">Name est un pointeur vers le nom de cononical pour le verbe.</span><span class="sxs-lookup"><span data-stu-id="62179-113">name is a pointer to the cononical name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="62179-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62179-114">Requirements</span></span>



| <span data-ttu-id="62179-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62179-115">Requirement</span></span> | <span data-ttu-id="62179-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="62179-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="62179-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62179-117">Minimum supported client</span></span><br/> | <span data-ttu-id="62179-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62179-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="62179-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62179-119">Minimum supported server</span></span><br/> | <span data-ttu-id="62179-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62179-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="62179-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="62179-121">Redistributable</span></span><br/>          | <span data-ttu-id="62179-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="62179-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="62179-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="62179-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62179-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="62179-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





