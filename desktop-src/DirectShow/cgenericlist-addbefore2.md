---
description: La méthode AddBefore insère une liste avant la position spécifiée. Cette méthode utilise les paramètres « POS » et « plist ».
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Méthode CGenericList. AddBefore (Wxlist. h)-POS, paramètres plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762422"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="588e3-104">Méthode CGenericList. AddBefore (Wxlist. h)-POS, paramètres plist</span><span class="sxs-lookup"><span data-stu-id="588e3-104">CGenericList.AddBefore method (Wxlist.h) - pos, pList parameters</span></span>

<span data-ttu-id="588e3-105">La `AddBefore` méthode insère une liste avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="588e3-105">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="588e3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="588e3-106">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="588e3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="588e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="588e3-108">*pos*</span><span class="sxs-lookup"><span data-stu-id="588e3-108">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="588e3-109">Position d’insertion de la liste.</span><span class="sxs-lookup"><span data-stu-id="588e3-109">Position to insert the list.</span></span> <span data-ttu-id="588e3-110">La liste est insérée avant cette position.</span><span class="sxs-lookup"><span data-stu-id="588e3-110">The list is inserted before this position.</span></span>

</dd> <dt>

<span data-ttu-id="588e3-111">*pList*</span><span class="sxs-lookup"><span data-stu-id="588e3-111">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="588e3-112">Pointeur vers la liste à insérer.</span><span class="sxs-lookup"><span data-stu-id="588e3-112">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="588e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="588e3-113">Return value</span></span>

<span data-ttu-id="588e3-114">Retourne la **valeur true** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="588e3-114">Returns **TRUE** if successful.</span></span> <span data-ttu-id="588e3-115">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="588e3-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="588e3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="588e3-116">Requirements</span></span>

| <span data-ttu-id="588e3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="588e3-117">Requirement</span></span> | <span data-ttu-id="588e3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="588e3-118">Value</span></span> |
|-|-|
| <span data-ttu-id="588e3-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="588e3-119">Header</span></span> | <span data-ttu-id="588e3-120">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="588e3-120">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="588e3-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="588e3-121">Library</span></span>| <span data-ttu-id="588e3-122">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="588e3-122">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="588e3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="588e3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588e3-124">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="588e3-124">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




