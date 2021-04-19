---
description: La méthode GetI récupère l’élément à la position spécifiée.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Méthode CBaseList. GetI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525271"
---
# <a name="cbaselistgeti-method"></a><span data-ttu-id="28055-103">Méthode CBaseList. GetI</span><span class="sxs-lookup"><span data-stu-id="28055-103">CBaseList.GetI method</span></span>

<span data-ttu-id="28055-104">La `GetI` méthode récupère l’élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="28055-104">The `GetI` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="28055-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28055-105">Syntax</span></span>


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="28055-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28055-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="28055-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="28055-108">Indicateur de position de l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="28055-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28055-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28055-109">Return value</span></span>

<span data-ttu-id="28055-110">Retourne un pointeur vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="28055-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="28055-111">Notes</span><span class="sxs-lookup"><span data-stu-id="28055-111">Remarks</span></span>

<span data-ttu-id="28055-112">Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="28055-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="28055-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28055-113">Requirements</span></span>



| <span data-ttu-id="28055-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28055-114">Requirement</span></span> | <span data-ttu-id="28055-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="28055-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28055-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="28055-116">Header</span></span><br/>  | <dl> <span data-ttu-id="28055-117"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28055-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="28055-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="28055-118">Library</span></span><br/> | <dl> <span data-ttu-id="28055-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="28055-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28055-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28055-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28055-121">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="28055-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




