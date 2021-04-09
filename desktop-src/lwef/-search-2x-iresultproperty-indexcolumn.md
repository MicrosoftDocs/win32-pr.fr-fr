---
title: IResultProperty IndexColumn, propriété (WdsSharedIDL. h)
description: Nom de la colonne des propriétés dans l’index.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Propriétés IndexColumn héritées fonctionnalités de l’environnement Windows
- Propriété IndexColumn fonctionnalités de l’environnement Windows héritées, interface IResultProperty
- Interface IResultProperty fonctionnalités d’environnement Windows héritées, propriété IndexColumn
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843377"
---
# <a name="iresultpropertyindexcolumn-property"></a><span data-ttu-id="d7535-106">IResultProperty :: IndexColumn, propriété</span><span class="sxs-lookup"><span data-stu-id="d7535-106">IResultProperty::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="d7535-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d7535-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d7535-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d7535-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d7535-109">Nom de la colonne des propriétés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d7535-109">Properties column name in the index.</span></span>

<span data-ttu-id="d7535-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d7535-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7535-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7535-111">Syntax</span></span>


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="d7535-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d7535-112">Property value</span></span>

<span data-ttu-id="d7535-113">retourne un pointeur vers le nom de colonne dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d7535-113">returns a pointer to the column name in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7535-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7535-114">Requirements</span></span>



| <span data-ttu-id="d7535-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7535-115">Requirement</span></span> | <span data-ttu-id="d7535-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7535-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7535-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7535-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7535-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7535-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d7535-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7535-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7535-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7535-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7535-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d7535-121">Redistributable</span></span><br/>          | <span data-ttu-id="d7535-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="d7535-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="d7535-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7535-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7535-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7535-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





