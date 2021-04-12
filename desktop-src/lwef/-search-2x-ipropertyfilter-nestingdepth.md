---
title: IPropertyFilter NestingDepth, propriété (WdsSharedIDL. h)
description: Filtre la profondeur dans un ensemble imbriqué de parenthèses.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Propriétés NestingDepth héritées fonctionnalités de l’environnement Windows
- Propriété NestingDepth fonctionnalités de l’environnement Windows héritées, interface IPropertyFilter
- Interface IPropertyFilter fonctionnalités d’environnement Windows héritées, propriété NestingDepth
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384604"
---
# <a name="ipropertyfilternestingdepth-property"></a><span data-ttu-id="6a821-106">IPropertyFilter :: NestingDepth, propriété</span><span class="sxs-lookup"><span data-stu-id="6a821-106">IPropertyFilter::NestingDepth property</span></span>

> [!NOTE]
> <span data-ttu-id="6a821-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6a821-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6a821-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="6a821-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6a821-109">Filtre la profondeur dans un ensemble imbriqué de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="6a821-109">Filters depth within a nested set of parentheses.</span></span>

<span data-ttu-id="6a821-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6a821-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a821-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a821-111">Syntax</span></span>


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a><span data-ttu-id="6a821-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6a821-112">Property value</span></span>

<span data-ttu-id="6a821-113">Définit le nombre indiquant la profondeur des parenthèses imbriquées.</span><span class="sxs-lookup"><span data-stu-id="6a821-113">Sets the number indicating the depth of nested parentheses.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a821-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a821-114">Requirements</span></span>



| <span data-ttu-id="6a821-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a821-115">Requirement</span></span> | <span data-ttu-id="6a821-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a821-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a821-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a821-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a821-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a821-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6a821-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a821-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a821-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a821-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a821-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6a821-121">Redistributable</span></span><br/>          | <span data-ttu-id="6a821-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="6a821-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="6a821-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a821-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a821-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a821-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





