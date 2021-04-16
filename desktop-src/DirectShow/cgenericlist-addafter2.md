---
description: La méthode AddAfter insère une liste après la position spécifiée et utilise les paramètres « POS » et « plist ».
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Méthode CGenericList. AddAfter (Wxlist. h)-POS, paramètres plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531107"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="acbca-103">Méthode CGenericList. AddAfter (Wxlist. h)-POS, paramètres plist</span><span class="sxs-lookup"><span data-stu-id="acbca-103">CGenericList.AddAfter method (Wxlist.h) - pos, plist parameters</span></span>

<span data-ttu-id="acbca-104">La `AddAfter` méthode insère une liste après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="acbca-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="acbca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acbca-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="acbca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acbca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acbca-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="acbca-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="acbca-108">Position d’insertion de la liste.</span><span class="sxs-lookup"><span data-stu-id="acbca-108">Position to insert the list.</span></span> <span data-ttu-id="acbca-109">La liste est insérée après cette position.</span><span class="sxs-lookup"><span data-stu-id="acbca-109">The list is inserted after this position.</span></span>

</dd> <dt>

<span data-ttu-id="acbca-110">*pList*</span><span class="sxs-lookup"><span data-stu-id="acbca-110">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="acbca-111">Pointeur vers la liste à insérer.</span><span class="sxs-lookup"><span data-stu-id="acbca-111">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acbca-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acbca-112">Return value</span></span>

<span data-ttu-id="acbca-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="acbca-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="acbca-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acbca-114">Requirements</span></span>

| <span data-ttu-id="acbca-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acbca-115">Requirement</span></span> | <span data-ttu-id="acbca-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="acbca-116">Value</span></span> |
|-|-|
| <span data-ttu-id="acbca-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="acbca-117">Header</span></span> | <span data-ttu-id="acbca-118">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="acbca-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="acbca-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="acbca-119">Library</span></span>| <span data-ttu-id="acbca-120">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="acbca-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="acbca-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acbca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbca-122">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="acbca-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




