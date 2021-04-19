---
description: La méthode GetNext récupère l’élément à la position spécifiée et avance la position.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: CGenericList. GetNext, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539284"
---
# <a name="cgenericlistgetnext-method"></a><span data-ttu-id="1d637-103">CGenericList. GetNext, méthode</span><span class="sxs-lookup"><span data-stu-id="1d637-103">CGenericList.GetNext method</span></span>

<span data-ttu-id="1d637-104">La `GetNext` méthode récupère l’élément à la position spécifiée et avance la position.</span><span class="sxs-lookup"><span data-stu-id="1d637-104">The `GetNext` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d637-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d637-105">Syntax</span></span>


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="1d637-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d637-107">*RP* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="1d637-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1d637-108">Référence à une valeur de POSITION.</span><span class="sxs-lookup"><span data-stu-id="1d637-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d637-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d637-109">Return value</span></span>

<span data-ttu-id="1d637-110">Retourne un pointeur vers un objet de type **Object** (le type de modèle).</span><span class="sxs-lookup"><span data-stu-id="1d637-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d637-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1d637-111">Remarks</span></span>

<span data-ttu-id="1d637-112">Cette méthode avance l’indicateur de position à la position suivante.</span><span class="sxs-lookup"><span data-stu-id="1d637-112">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="1d637-113">Si l’indicateur de position se déplace au-delà de la fin de la liste, la méthode lui affecte la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1d637-113">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

<span data-ttu-id="1d637-114">Si *RP* a la **valeur null**, la méthode retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1d637-114">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d637-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d637-115">Requirements</span></span>



| <span data-ttu-id="1d637-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d637-116">Requirement</span></span> | <span data-ttu-id="1d637-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d637-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d637-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d637-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1d637-119"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d637-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1d637-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1d637-120">Library</span></span><br/> | <dl> <span data-ttu-id="1d637-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1d637-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d637-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d637-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d637-123">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="1d637-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




