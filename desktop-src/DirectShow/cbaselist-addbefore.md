---
description: La méthode AddBefore insère une liste avant la position spécifiée.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Méthode CBaseList. AddBefore (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539689"
---
# <a name="cbaselistaddbefore-method"></a><span data-ttu-id="60eb1-103">Méthode CBaseList. AddBefore</span><span class="sxs-lookup"><span data-stu-id="60eb1-103">CBaseList.AddBefore method</span></span>

<span data-ttu-id="60eb1-104">La `AddBefore` méthode insère une liste avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="60eb1-104">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="60eb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60eb1-105">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="60eb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60eb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60eb1-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="60eb1-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="60eb1-108">Position avant laquelle insérer la liste.</span><span class="sxs-lookup"><span data-stu-id="60eb1-108">Position before which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="60eb1-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="60eb1-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="60eb1-110">Pointeur vers la liste à insérer.</span><span class="sxs-lookup"><span data-stu-id="60eb1-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60eb1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60eb1-111">Return value</span></span>

<span data-ttu-id="60eb1-112">Retourne la **valeur true** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="60eb1-112">Returns **TRUE** if successful.</span></span> <span data-ttu-id="60eb1-113">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="60eb1-113">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="60eb1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="60eb1-114">Remarks</span></span>

<span data-ttu-id="60eb1-115">Les indicateurs de position existants, y compris celui spécifié dans le paramètre *pos* , restent valides.</span><span class="sxs-lookup"><span data-stu-id="60eb1-115">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="60eb1-116">Si la méthode échoue, certains éléments ont peut-être été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="60eb1-116">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="60eb1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60eb1-117">Requirements</span></span>



| <span data-ttu-id="60eb1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60eb1-118">Requirement</span></span> | <span data-ttu-id="60eb1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="60eb1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60eb1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="60eb1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="60eb1-121"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60eb1-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="60eb1-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60eb1-122">Library</span></span><br/> | <dl> <span data-ttu-id="60eb1-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60eb1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60eb1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60eb1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60eb1-125">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="60eb1-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




