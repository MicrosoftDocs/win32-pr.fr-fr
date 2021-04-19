---
title: IResultProperty DisplayState, propriété (WdsSharedIDL. h)
description: Visability de la propriété.
ms.assetid: 4fdf6cdb-30bd-4582-a573-a1cc9f4052e6
keywords:
- Propriété DisplayState fonctionnalités héritées de l’environnement Windows
- DisplayState, propriété fonctionnalités de l’environnement Windows héritées, interface IResultProperty
- Interface IResultProperty fonctionnalités de l’environnement Windows héritées, propriété DisplayState
topic_type:
- apiref
api_name:
- IResultProperty.DisplayState
- IResultProperty.get_DisplayState
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85634441a38c2cb2130010c79f8ee3ebcb78a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509533"
---
# <a name="iresultpropertydisplaystate-property"></a><span data-ttu-id="21501-106">IResultProperty ::D propriété isplayState</span><span class="sxs-lookup"><span data-stu-id="21501-106">IResultProperty::DisplayState property</span></span>

> [!NOTE]
> <span data-ttu-id="21501-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="21501-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="21501-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="21501-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="21501-109">Visability de la propriété.</span><span class="sxs-lookup"><span data-stu-id="21501-109">Visability of the property.</span></span>

<span data-ttu-id="21501-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="21501-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21501-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21501-111">Syntax</span></span>


```C++
HRESULT get_DisplayState(
  [out, retval] PropertyDisplayState *state
);
```



## <a name="property-value"></a><span data-ttu-id="21501-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="21501-112">Property value</span></span>

<span data-ttu-id="21501-113">retourne un pointeur vers la valeur d’état d’affichage.</span><span class="sxs-lookup"><span data-stu-id="21501-113">returns a pointer to the display state value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21501-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21501-114">Requirements</span></span>



| <span data-ttu-id="21501-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21501-115">Requirement</span></span> | <span data-ttu-id="21501-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="21501-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="21501-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21501-117">Minimum supported client</span></span><br/> | <span data-ttu-id="21501-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21501-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="21501-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21501-119">Minimum supported server</span></span><br/> | <span data-ttu-id="21501-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21501-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="21501-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="21501-121">Redistributable</span></span><br/>          | <span data-ttu-id="21501-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="21501-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="21501-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="21501-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="21501-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="21501-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





