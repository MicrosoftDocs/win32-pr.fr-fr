---
description: 'La méthode AdvisePeriodic crée une demande de notification périodique. Cette méthode implémente la méthode IReferenceClock :: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Méthode CBaseReferenceClock. AdvisePeriodic (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529916"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a><span data-ttu-id="38670-104">Méthode CBaseReferenceClock. AdvisePeriodic</span><span class="sxs-lookup"><span data-stu-id="38670-104">CBaseReferenceClock.AdvisePeriodic method</span></span>

<span data-ttu-id="38670-105">La `AdvisePeriodic` méthode crée une demande de notification périodique.</span><span class="sxs-lookup"><span data-stu-id="38670-105">The `AdvisePeriodic` method creates a periodic advise request.</span></span> <span data-ttu-id="38670-106">Cette méthode implémente la méthode [**IReferenceClock :: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .</span><span class="sxs-lookup"><span data-stu-id="38670-106">This method implements the [**IReferenceClock::AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="38670-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38670-107">Syntax</span></span>


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="38670-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38670-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38670-109">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="38670-109">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="38670-110">Heure de la première notification, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="38670-110">Time of the first notification, in 100-nanosecond units.</span></span> <span data-ttu-id="38670-111">Doit être supérieur à zéro et inférieur à la \_ durée maximale.</span><span class="sxs-lookup"><span data-stu-id="38670-111">Must be greater than zero and less than MAX\_TIME.</span></span>

</dd> <dt>

<span data-ttu-id="38670-112">*PeriodTime*</span><span class="sxs-lookup"><span data-stu-id="38670-112">*PeriodTime*</span></span> 
</dt> <dd>

<span data-ttu-id="38670-113">Temps entre les notifications, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="38670-113">Time between notifications, in 100-nanosecond units.</span></span> <span data-ttu-id="38670-114">Doit être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="38670-114">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="38670-115">*hSemaphore*</span><span class="sxs-lookup"><span data-stu-id="38670-115">*hSemaphore*</span></span> 
</dt> <dd>

<span data-ttu-id="38670-116">Handle vers un sémaphore, créé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="38670-116">Handle to a semaphore, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="38670-117">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="38670-117">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="38670-118">Pointeur vers une variable qui reçoit un identificateur pour la demande de notification.</span><span class="sxs-lookup"><span data-stu-id="38670-118">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38670-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38670-119">Return value</span></span>

<span data-ttu-id="38670-120">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="38670-120">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="38670-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="38670-121">Return code</span></span>                                                                                   | <span data-ttu-id="38670-122">Description</span><span class="sxs-lookup"><span data-stu-id="38670-122">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="38670-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38670-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="38670-124">Succès</span><span class="sxs-lookup"><span data-stu-id="38670-124">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="38670-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="38670-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="38670-126">Valeurs de temps non valides</span><span class="sxs-lookup"><span data-stu-id="38670-126">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="38670-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="38670-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="38670-128">Échec</span><span class="sxs-lookup"><span data-stu-id="38670-128">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="38670-129"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="38670-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="38670-130">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="38670-130">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38670-131">Notes</span><span class="sxs-lookup"><span data-stu-id="38670-131">Remarks</span></span>

<span data-ttu-id="38670-132">À chaque heure de notification, l’horloge libère le sémaphore spécifié dans le paramètre *hSemaphore* .</span><span class="sxs-lookup"><span data-stu-id="38670-132">At each notification time, the clock releases the semaphore specified in the *hSemaphore* parameter.</span></span> <span data-ttu-id="38670-133">Quand aucune autre notification n’est requise, appelez la méthode [**CBaseReferenceClock :: Unadvise**](cbasereferenceclock-unadvise.md) et transmettez la valeur *pdwAdviseToken* retournée à partir de cet appel.</span><span class="sxs-lookup"><span data-stu-id="38670-133">When no further notifications are required, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span>

## <a name="requirements"></a><span data-ttu-id="38670-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38670-134">Requirements</span></span>



| <span data-ttu-id="38670-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38670-135">Requirement</span></span> | <span data-ttu-id="38670-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="38670-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38670-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="38670-137">Header</span></span><br/>  | <dl> <span data-ttu-id="38670-138"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38670-138"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="38670-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38670-139">Library</span></span><br/> | <dl> <span data-ttu-id="38670-140"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="38670-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38670-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38670-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38670-142">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="38670-142">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




