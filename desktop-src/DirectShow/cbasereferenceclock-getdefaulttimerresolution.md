---
description: La méthode GetDefaultTimerResolution retourne la résolution actuelle de la minuterie de l’horloge de référence.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Méthode CBaseReferenceClock. GetDefaultTimerResolution (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520922"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a><span data-ttu-id="6581b-103">Méthode CBaseReferenceClock. GetDefaultTimerResolution</span><span class="sxs-lookup"><span data-stu-id="6581b-103">CBaseReferenceClock.GetDefaultTimerResolution method</span></span>

<span data-ttu-id="6581b-104">La `GetDefaultTimerResolution` méthode retourne la résolution actuelle de la minuterie de l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="6581b-104">The `GetDefaultTimerResolution` method returns the current resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6581b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6581b-105">Syntax</span></span>


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="6581b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6581b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6581b-107">*pTimerResolution*</span><span class="sxs-lookup"><span data-stu-id="6581b-107">*pTimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="6581b-108">Reçoit la résolution de la minuterie demandée, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="6581b-108">Receives the requested timer resolution, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6581b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6581b-109">Return value</span></span>

<span data-ttu-id="6581b-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6581b-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6581b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6581b-111">Remarks</span></span>

<span data-ttu-id="6581b-112">Cette méthode implémente la méthode [**IReferenceClockTimerControl :: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="6581b-112">This method implements the [**IReferenceClockTimerControl::GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6581b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6581b-113">Requirements</span></span>



| <span data-ttu-id="6581b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6581b-114">Requirement</span></span> | <span data-ttu-id="6581b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6581b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6581b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6581b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6581b-117"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6581b-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6581b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6581b-118">Library</span></span><br/> | <dl> <span data-ttu-id="6581b-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6581b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6581b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6581b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6581b-121">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="6581b-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




