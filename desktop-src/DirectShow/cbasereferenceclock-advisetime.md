---
description: 'La méthode AdviseTime crée une demande de notification à une seule capture. Cette méthode implémente la méthode IReferenceClock :: AdviseTime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Méthode CBaseReferenceClock. AdviseTime (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521632"
---
# <a name="cbasereferenceclockadvisetime-method"></a><span data-ttu-id="bdfa3-104">Méthode CBaseReferenceClock. AdviseTime</span><span class="sxs-lookup"><span data-stu-id="bdfa3-104">CBaseReferenceClock.AdviseTime method</span></span>

<span data-ttu-id="bdfa3-105">La `AdviseTime` méthode crée une demande de notification à une seule capture.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-105">The `AdviseTime` method creates a one-shot advise request.</span></span> <span data-ttu-id="bdfa3-106">Cette méthode implémente la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .</span><span class="sxs-lookup"><span data-stu-id="bdfa3-106">This method implements the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdfa3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdfa3-107">Syntax</span></span>


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="bdfa3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdfa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdfa3-109">*baseTime*</span><span class="sxs-lookup"><span data-stu-id="bdfa3-109">*baseTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bdfa3-110">Temps de référence de base, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-110">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="bdfa3-111">*streamTime*</span><span class="sxs-lookup"><span data-stu-id="bdfa3-111">*streamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bdfa3-112">Temps de décalage du flux, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-112">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="bdfa3-113">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="bdfa3-113">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="bdfa3-114">Handle vers un événement, créé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-114">Handle to an event, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="bdfa3-115">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="bdfa3-115">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="bdfa3-116">Pointeur vers une variable qui reçoit un identificateur pour la demande de notification.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-116">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdfa3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdfa3-117">Return value</span></span>

<span data-ttu-id="bdfa3-118">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-118">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="bdfa3-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bdfa3-119">Return code</span></span>                                                                                   | <span data-ttu-id="bdfa3-120">Description</span><span class="sxs-lookup"><span data-stu-id="bdfa3-120">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="bdfa3-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdfa3-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bdfa3-122">Succès</span><span class="sxs-lookup"><span data-stu-id="bdfa3-122">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="bdfa3-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bdfa3-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bdfa3-124">Valeurs de temps non valides</span><span class="sxs-lookup"><span data-stu-id="bdfa3-124">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="bdfa3-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdfa3-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bdfa3-126">Échec</span><span class="sxs-lookup"><span data-stu-id="bdfa3-126">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="bdfa3-127"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdfa3-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bdfa3-128">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="bdfa3-128">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdfa3-129">Notes</span><span class="sxs-lookup"><span data-stu-id="bdfa3-129">Remarks</span></span>

<span data-ttu-id="bdfa3-130">Cette méthode crée une demande de notification d’une seule capture pour le streamTime de temps de référence *baseTime*  +  .</span><span class="sxs-lookup"><span data-stu-id="bdfa3-130">This method creates a one-shot advise request for the reference time *baseTime* + *streamTime*.</span></span> <span data-ttu-id="bdfa3-131">La somme doit être supérieure à zéro et inférieure à la \_ durée maximale, ou la méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-131">The sum must be greater than zero and less than MAX\_TIME, or the method returns E\_INVALIDARG.</span></span> <span data-ttu-id="bdfa3-132">À l’heure demandée, l’horloge signale l’événement spécifié dans le paramètre *hEvent* .</span><span class="sxs-lookup"><span data-stu-id="bdfa3-132">At the requested time, the clock signals the event specified in the *hEvent* parameter.</span></span>

<span data-ttu-id="bdfa3-133">Pour annuler la notification avant l’heure d’expiration, appelez la méthode [**CBaseReferenceClock :: Unadvise**](cbasereferenceclock-unadvise.md) et transmettez la valeur *pdwAdviseToken* retournée à partir de cet appel.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-133">To cancel the notification before the time is reached, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span> <span data-ttu-id="bdfa3-134">Une fois la notification effectuée, l’horloge l’efface automatiquement. il n’est donc pas nécessaire d’appeler **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-134">After the notification has occurred, the clock automatically clears it, so it is not necessary to call **Unadvise**.</span></span> <span data-ttu-id="bdfa3-135">Toutefois, ce n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="bdfa3-135">However, it is not an error to do so.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdfa3-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdfa3-136">Requirements</span></span>



| <span data-ttu-id="bdfa3-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdfa3-137">Requirement</span></span> | <span data-ttu-id="bdfa3-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdfa3-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfa3-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdfa3-139">Header</span></span><br/>  | <dl> <span data-ttu-id="bdfa3-140"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdfa3-140"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bdfa3-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bdfa3-141">Library</span></span><br/> | <dl> <span data-ttu-id="bdfa3-142"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bdfa3-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdfa3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdfa3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdfa3-144">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="bdfa3-144">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




