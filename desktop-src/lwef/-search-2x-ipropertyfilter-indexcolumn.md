---
title: IPropertyFilter IndexColumn, propriété (WdsSharedIDL. h)
description: Nom de la colonne indexée de la propriété sur laquelle filtrer.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Propriétés IndexColumn héritées fonctionnalités de l’environnement Windows
- Propriété IndexColumn fonctionnalités de l’environnement Windows héritées, interface IPropertyFilter
- Interface IPropertyFilter fonctionnalités d’environnement Windows héritées, propriété IndexColumn
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032810"
---
# <a name="ipropertyfilterindexcolumn-property"></a><span data-ttu-id="59d09-106">IPropertyFilter :: IndexColumn, propriété</span><span class="sxs-lookup"><span data-stu-id="59d09-106">IPropertyFilter::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="59d09-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="59d09-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="59d09-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="59d09-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="59d09-109">Nom de la colonne indexée de la propriété sur laquelle filtrer.</span><span class="sxs-lookup"><span data-stu-id="59d09-109">Indexed column name of the property to filter by.</span></span>

<span data-ttu-id="59d09-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="59d09-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d09-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59d09-111">Syntax</span></span>


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="59d09-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="59d09-112">Property value</span></span>

<span data-ttu-id="59d09-113">Définit la propriété de colonne.</span><span class="sxs-lookup"><span data-stu-id="59d09-113">Sets the Column property.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d09-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59d09-114">Requirements</span></span>



| <span data-ttu-id="59d09-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59d09-115">Requirement</span></span> | <span data-ttu-id="59d09-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="59d09-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d09-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59d09-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59d09-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59d09-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="59d09-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59d09-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59d09-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59d09-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="59d09-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="59d09-121">Redistributable</span></span><br/>          | <span data-ttu-id="59d09-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="59d09-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="59d09-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="59d09-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d09-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="59d09-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





