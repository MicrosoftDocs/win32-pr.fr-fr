---
description: La méthode SetDefaultTimerResolution définit la résolution de la minuterie de l’horloge de référence.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Méthode CBaseReferenceClock. SetDefaultTimerResolution (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533439"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a><span data-ttu-id="7f045-103">Méthode CBaseReferenceClock. SetDefaultTimerResolution</span><span class="sxs-lookup"><span data-stu-id="7f045-103">CBaseReferenceClock.SetDefaultTimerResolution method</span></span>

<span data-ttu-id="7f045-104">La `SetDefaultTimerResolution` méthode définit la résolution de la minuterie de l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="7f045-104">The `SetDefaultTimerResolution` method sets the resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f045-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f045-105">Syntax</span></span>


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="7f045-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f045-107">*timerResolution*</span><span class="sxs-lookup"><span data-stu-id="7f045-107">*timerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="7f045-108">Résolution minimale de la minuterie, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="7f045-108">Minimum timer resolution, in 100-nanosecond units.</span></span> <span data-ttu-id="7f045-109">Si la valeur est égale à zéro, l’horloge de référence annule la requête précédente.</span><span class="sxs-lookup"><span data-stu-id="7f045-109">If the value is zero, the reference clock cancels its previous request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f045-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f045-110">Return value</span></span>

<span data-ttu-id="7f045-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f045-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f045-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7f045-112">Remarks</span></span>

<span data-ttu-id="7f045-113">Cette méthode implémente la méthode [**IReferenceClockTimerControl :: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="7f045-113">This method implements the [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f045-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f045-114">Requirements</span></span>



| <span data-ttu-id="7f045-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f045-115">Requirement</span></span> | <span data-ttu-id="7f045-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f045-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f045-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f045-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7f045-118"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f045-118"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7f045-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f045-119">Library</span></span><br/> | <dl> <span data-ttu-id="7f045-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f045-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f045-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f045-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f045-122">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="7f045-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




