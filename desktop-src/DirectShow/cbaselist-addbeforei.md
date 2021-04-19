---
description: La méthode AddBeforeI insère un élément avant la position spécifiée.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Méthode CBaseList. AddBeforeI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536016"
---
# <a name="cbaselistaddbeforei-method"></a><span data-ttu-id="f342f-103">Méthode CBaseList. AddBeforeI</span><span class="sxs-lookup"><span data-stu-id="f342f-103">CBaseList.AddBeforeI method</span></span>

<span data-ttu-id="f342f-104">La `AddBeforeI` méthode insère un élément avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f342f-104">The `AddBeforeI` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="f342f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f342f-105">Syntax</span></span>


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="f342f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f342f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f342f-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="f342f-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="f342f-108">Position avant laquelle l’élément doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="f342f-108">Position before which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="f342f-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="f342f-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="f342f-110">Pointeur désignant l’élément.</span><span class="sxs-lookup"><span data-stu-id="f342f-110">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f342f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f342f-111">Return value</span></span>

<span data-ttu-id="f342f-112">Retourne l’indicateur de position pour l’élément inséré.</span><span class="sxs-lookup"><span data-stu-id="f342f-112">Returns the position indicator for the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="f342f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f342f-113">Remarks</span></span>

<span data-ttu-id="f342f-114">Si *pos* a la **valeur null**, cette méthode ajoute l’élément à la fin de la liste (équivalent à l’appel de la méthode [**CBaseList :: AddTailI**](cbaselist-addtaili.md) ).</span><span class="sxs-lookup"><span data-stu-id="f342f-114">If *pos* is **NULL**, this method adds the item to the tail of the list (equivalent to calling the [**CBaseList::AddTailI**](cbaselist-addtaili.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="f342f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f342f-115">Requirements</span></span>



| <span data-ttu-id="f342f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f342f-116">Requirement</span></span> | <span data-ttu-id="f342f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f342f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f342f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f342f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f342f-119"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f342f-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f342f-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f342f-120">Library</span></span><br/> | <dl> <span data-ttu-id="f342f-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f342f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f342f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f342f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f342f-123">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="f342f-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




