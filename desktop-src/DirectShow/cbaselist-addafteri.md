---
description: La méthode AddAfterI insère un élément après la position spécifiée.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Méthode CBaseList. AddAfterI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525273"
---
# <a name="cbaselistaddafteri-method"></a><span data-ttu-id="af799-103">Méthode CBaseList. AddAfterI</span><span class="sxs-lookup"><span data-stu-id="af799-103">CBaseList.AddAfterI method</span></span>

<span data-ttu-id="af799-104">La `AddAfterI` méthode insère un élément après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="af799-104">The `AddAfterI` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="af799-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af799-105">Syntax</span></span>


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="af799-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af799-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="af799-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="af799-108">Position après laquelle l’élément doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="af799-108">Position after which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="af799-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="af799-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="af799-110">Pointeur vers l’élément à ajouter.</span><span class="sxs-lookup"><span data-stu-id="af799-110">Pointer to the item to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af799-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af799-111">Return value</span></span>

<span data-ttu-id="af799-112">Retourne l’indicateur de position de l’élément inséré.</span><span class="sxs-lookup"><span data-stu-id="af799-112">Returns the position indicator of the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="af799-113">Notes</span><span class="sxs-lookup"><span data-stu-id="af799-113">Remarks</span></span>

<span data-ttu-id="af799-114">Si *pos* a la **valeur null**, cette méthode ajoute l’élément au début de la liste (équivalent à l’appel de la méthode [**CBaseList :: AddHeadI**](cbaselist-addheadi.md) ).</span><span class="sxs-lookup"><span data-stu-id="af799-114">If *pos* is **NULL**, this method adds the item to the head of the list (equivalent to calling the [**CBaseList::AddHeadI**](cbaselist-addheadi.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="af799-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af799-115">Requirements</span></span>



| <span data-ttu-id="af799-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af799-116">Requirement</span></span> | <span data-ttu-id="af799-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="af799-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af799-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="af799-118">Header</span></span><br/>  | <dl> <span data-ttu-id="af799-119"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af799-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="af799-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af799-120">Library</span></span><br/> | <dl> <span data-ttu-id="af799-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="af799-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af799-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af799-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af799-123">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="af799-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




