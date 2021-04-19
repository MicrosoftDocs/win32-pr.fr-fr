---
description: La méthode AddTailI ajoute un élément à la fin de la liste.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Méthode CBaseList. AddTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521646"
---
# <a name="cbaselistaddtaili-method"></a><span data-ttu-id="7efc4-103">Méthode CBaseList. AddTailI</span><span class="sxs-lookup"><span data-stu-id="7efc4-103">CBaseList.AddTailI method</span></span>

<span data-ttu-id="7efc4-104">La `AddTailI` méthode ajoute un élément à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="7efc4-104">The `AddTailI` method adds an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7efc4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7efc4-105">Syntax</span></span>


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="7efc4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7efc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7efc4-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="7efc4-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="7efc4-108">Pointeur désignant l’élément.</span><span class="sxs-lookup"><span data-stu-id="7efc4-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7efc4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7efc4-109">Return value</span></span>

<span data-ttu-id="7efc4-110">Retourne une valeur de POSITION pour la nouvelle position de fin.</span><span class="sxs-lookup"><span data-stu-id="7efc4-110">Returns a POSITION value for the new tail position.</span></span>

## <a name="remarks"></a><span data-ttu-id="7efc4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7efc4-111">Remarks</span></span>

<span data-ttu-id="7efc4-112">Si la méthode échoue, elle retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7efc4-112">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7efc4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7efc4-113">Requirements</span></span>



| <span data-ttu-id="7efc4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7efc4-114">Requirement</span></span> | <span data-ttu-id="7efc4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7efc4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7efc4-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="7efc4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7efc4-117"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7efc4-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7efc4-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7efc4-118">Library</span></span><br/> | <dl> <span data-ttu-id="7efc4-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7efc4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7efc4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7efc4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efc4-121">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="7efc4-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




