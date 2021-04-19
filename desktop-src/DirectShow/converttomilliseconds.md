---
description: La fonction ConvertToMilliseconds convertit une durée de référence en millisecondes.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: ConvertToMilliseconds, fonction (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520898"
---
# <a name="converttomilliseconds-function"></a><span data-ttu-id="c4f60-103">ConvertToMilliseconds fonction)</span><span class="sxs-lookup"><span data-stu-id="c4f60-103">ConvertToMilliseconds function</span></span>

<span data-ttu-id="c4f60-104">La `ConvertToMilliseconds` fonction convertit une durée de référence en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="c4f60-104">The `ConvertToMilliseconds` function converts a reference time to milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4f60-105">Syntax</span></span>


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a><span data-ttu-id="c4f60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4f60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f60-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="c4f60-107">*RT* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f60-108">Temps de référence, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="c4f60-108">Reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f60-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4f60-109">Return value</span></span>

<span data-ttu-id="c4f60-110">Retourne la durée de référence convertie en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="c4f60-110">Returns the reference time converted to milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4f60-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4f60-111">Requirements</span></span>



| <span data-ttu-id="c4f60-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4f60-112">Requirement</span></span> | <span data-ttu-id="c4f60-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4f60-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f60-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4f60-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c4f60-115"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4f60-115"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c4f60-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4f60-116">Library</span></span><br/> | <dl> <span data-ttu-id="c4f60-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c4f60-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4f60-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4f60-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f60-119">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="c4f60-119">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




