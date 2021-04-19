---
description: La méthode AddAfter insère une liste après la position spécifiée.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Méthode CBaseList. AddAfter (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525274"
---
# <a name="cbaselistaddafter-method"></a><span data-ttu-id="9d545-103">Méthode CBaseList. AddAfter</span><span class="sxs-lookup"><span data-stu-id="9d545-103">CBaseList.AddAfter method</span></span>

<span data-ttu-id="9d545-104">La `AddAfter` méthode insère une liste après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9d545-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d545-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d545-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="9d545-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d545-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d545-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="9d545-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="9d545-108">Position après laquelle insérer la liste.</span><span class="sxs-lookup"><span data-stu-id="9d545-108">Position after which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="9d545-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="9d545-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="9d545-110">Pointeur vers la liste à insérer.</span><span class="sxs-lookup"><span data-stu-id="9d545-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d545-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d545-111">Return value</span></span>

<span data-ttu-id="9d545-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9d545-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d545-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9d545-113">Remarks</span></span>

<span data-ttu-id="9d545-114">Les indicateurs de position existants, y compris celui spécifié dans le paramètre *pos* , restent valides.</span><span class="sxs-lookup"><span data-stu-id="9d545-114">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="9d545-115">Si la méthode échoue, certains éléments ont peut-être été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="9d545-115">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d545-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d545-116">Requirements</span></span>



| <span data-ttu-id="9d545-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d545-117">Requirement</span></span> | <span data-ttu-id="9d545-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d545-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d545-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d545-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9d545-120"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d545-120"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9d545-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d545-121">Library</span></span><br/> | <dl> <span data-ttu-id="9d545-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d545-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d545-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d545-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d545-124">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="9d545-124">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




