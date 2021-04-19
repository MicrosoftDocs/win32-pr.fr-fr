---
description: La méthode GetNextI récupère l’élément à la position spécifiée et avance la position.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Méthode CBaseList. GetNextI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530535"
---
# <a name="cbaselistgetnexti-method"></a><span data-ttu-id="7be73-103">Méthode CBaseList. GetNextI</span><span class="sxs-lookup"><span data-stu-id="7be73-103">CBaseList.GetNextI method</span></span>

<span data-ttu-id="7be73-104">La `GetNextI` méthode récupère l’élément à la position spécifiée et avance la position.</span><span class="sxs-lookup"><span data-stu-id="7be73-104">The `GetNextI` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7be73-105">Syntax</span></span>


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="7be73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7be73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be73-107">*RP* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="7be73-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7be73-108">Référence à une valeur de POSITION.</span><span class="sxs-lookup"><span data-stu-id="7be73-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be73-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7be73-109">Return value</span></span>

<span data-ttu-id="7be73-110">Retourne un pointeur vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="7be73-110">Returns a pointer to the item.</span></span> <span data-ttu-id="7be73-111">Si *RP* a la **valeur null**, la méthode retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7be73-111">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7be73-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7be73-112">Remarks</span></span>

<span data-ttu-id="7be73-113">Cette méthode avance l’indicateur de position à la position suivante.</span><span class="sxs-lookup"><span data-stu-id="7be73-113">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="7be73-114">Si l’indicateur de position se déplace au-delà de la fin de la liste, la méthode lui affecte la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7be73-114">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be73-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7be73-115">Requirements</span></span>



| <span data-ttu-id="7be73-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7be73-116">Requirement</span></span> | <span data-ttu-id="7be73-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7be73-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be73-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="7be73-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7be73-119"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7be73-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7be73-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7be73-120">Library</span></span><br/> | <dl> <span data-ttu-id="7be73-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7be73-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be73-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7be73-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be73-123">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="7be73-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




