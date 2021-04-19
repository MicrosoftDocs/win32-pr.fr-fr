---
description: La méthode AddHeadI ajoute un élément au début de la liste.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Méthode CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542388"
---
# <a name="cbaselistaddheadi-method"></a><span data-ttu-id="845ca-103">Méthode CBaseList. AddHeadI</span><span class="sxs-lookup"><span data-stu-id="845ca-103">CBaseList.AddHeadI method</span></span>

<span data-ttu-id="845ca-104">La `AddHeadI` méthode ajoute un élément au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="845ca-104">The `AddHeadI` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="845ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="845ca-105">Syntax</span></span>


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="845ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="845ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="845ca-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="845ca-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="845ca-108">Pointeur désignant l’élément.</span><span class="sxs-lookup"><span data-stu-id="845ca-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="845ca-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="845ca-109">Return value</span></span>

<span data-ttu-id="845ca-110">Retourne une valeur de POSITION indiquant la nouvelle position de la tête.</span><span class="sxs-lookup"><span data-stu-id="845ca-110">Returns a POSITION value indicating the new head position.</span></span>

## <a name="remarks"></a><span data-ttu-id="845ca-111">Notes</span><span class="sxs-lookup"><span data-stu-id="845ca-111">Remarks</span></span>

<span data-ttu-id="845ca-112">Si la méthode échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="845ca-112">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="845ca-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="845ca-113">Requirements</span></span>



| <span data-ttu-id="845ca-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="845ca-114">Requirement</span></span> | <span data-ttu-id="845ca-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="845ca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845ca-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="845ca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="845ca-117"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="845ca-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="845ca-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="845ca-118">Library</span></span><br/> | <dl> <span data-ttu-id="845ca-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="845ca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="845ca-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="845ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="845ca-121">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="845ca-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




