---
description: 'La méthode GetTime récupère le temps de référence actuel. Cette méthode implémente la méthode IReferenceClock :: GetTime.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: CBaseReferenceClock. GetTime, méthode (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531091"
---
# <a name="cbasereferenceclockgettime-method"></a><span data-ttu-id="6fd04-104">CBaseReferenceClock. GetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="6fd04-104">CBaseReferenceClock.GetTime method</span></span>

<span data-ttu-id="6fd04-105">La `GetTime` méthode récupère le temps de référence actuel.</span><span class="sxs-lookup"><span data-stu-id="6fd04-105">The `GetTime` method retrieves the current reference time.</span></span> <span data-ttu-id="6fd04-106">Cette méthode implémente la méthode [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="6fd04-106">This method implements the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd04-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fd04-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="6fd04-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fd04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd04-109">*pTime*</span><span class="sxs-lookup"><span data-stu-id="6fd04-109">*pTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd04-110">Pointeur vers une variable qui reçoit l’heure actuelle, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="6fd04-110">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd04-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fd04-111">Return value</span></span>

<span data-ttu-id="6fd04-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6fd04-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="6fd04-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6fd04-113">Return code</span></span>                                                                               | <span data-ttu-id="6fd04-114">Description</span><span class="sxs-lookup"><span data-stu-id="6fd04-114">Description</span></span>                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="6fd04-115"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="6fd04-115"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="6fd04-116">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="6fd04-116">**NULL** pointer argument.</span></span><br/>                       |
| <dl> <span data-ttu-id="6fd04-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6fd04-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="6fd04-118">L’heure retournée est identique à la valeur précédente.</span><span class="sxs-lookup"><span data-stu-id="6fd04-118">Returned time is the same as the previous value.</span></span><br/> |
| <dl> <span data-ttu-id="6fd04-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6fd04-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="6fd04-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6fd04-120">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="6fd04-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6fd04-121">Remarks</span></span>

<span data-ttu-id="6fd04-122">Cette méthode appelle la méthode [**CBaseReferenceClock :: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) pour déterminer l’heure réelle de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="6fd04-122">This method calls the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method to determine the real clock time.</span></span> <span data-ttu-id="6fd04-123">Si l’heure de l’horloge est strictement supérieure à la valeur précédente, `GetTime` utilise l’heure de l’horloge et retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6fd04-123">If the clock time is strictly greater than the previous value, `GetTime` uses the clock time and returns S\_OK.</span></span> <span data-ttu-id="6fd04-124">Dans le cas contraire, `GetTime` utilise la valeur précédente et retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="6fd04-124">Otherwise, `GetTime` uses the previous value and returns S\_FALSE.</span></span> <span data-ttu-id="6fd04-125">Par conséquent, l’horloge interne peut s’exécuter en arrière pendant une brève période, sans entraîner la réexécution du temps de référence.</span><span class="sxs-lookup"><span data-stu-id="6fd04-125">Therefore, the internal clock can run backward for a short period, without causing the reference time to run backward.</span></span> <span data-ttu-id="6fd04-126">Au lieu de cela, le temps de référence est « bloqué » à la même valeur jusqu’à ce que l’horloge interne soit interceptée.</span><span class="sxs-lookup"><span data-stu-id="6fd04-126">Instead, the reference time will "stall" at the same value until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd04-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fd04-127">Requirements</span></span>



| <span data-ttu-id="6fd04-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fd04-128">Requirement</span></span> | <span data-ttu-id="6fd04-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fd04-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd04-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fd04-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6fd04-131"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fd04-131"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6fd04-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6fd04-132">Library</span></span><br/> | <dl> <span data-ttu-id="6fd04-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6fd04-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd04-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fd04-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd04-135">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="6fd04-135">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




