---
description: 'La méthode SetClockDelta ajuste l’heure de l’horloge. Cette méthode implémente la méthode IAMClockAdjust :: SetClockDelta.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Méthode CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530373"
---
# <a name="csystemclocksetclockdelta-method"></a><span data-ttu-id="adae1-104">Méthode CSystemClock. SetClockDelta</span><span class="sxs-lookup"><span data-stu-id="adae1-104">CSystemClock.SetClockDelta method</span></span>

<span data-ttu-id="adae1-105">La `SetClockDelta` méthode ajuste l’heure de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="adae1-105">The `SetClockDelta` method adjusts the clock time.</span></span> <span data-ttu-id="adae1-106">Cette méthode implémente la méthode [**IAMClockAdjust :: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .</span><span class="sxs-lookup"><span data-stu-id="adae1-106">This method implements the [**IAMClockAdjust::SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="adae1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adae1-107">Syntax</span></span>


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a><span data-ttu-id="adae1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adae1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adae1-109">*rtDelta*</span><span class="sxs-lookup"><span data-stu-id="adae1-109">*rtDelta*</span></span> 
</dt> <dd>

<span data-ttu-id="adae1-110">Spécifie la quantité d’ajustement de l’horloge, en tant que valeur de [**\_ temps de référence**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="adae1-110">Specifies the amount by which to adjust the clock, as a [**REFERENCE\_TIME**](reference-time.md) value.</span></span> <span data-ttu-id="adae1-111">Une valeur positive déplace l’avance de l’horloge et une valeur négative déplace l’horloge vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="adae1-111">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adae1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adae1-112">Return value</span></span>

<span data-ttu-id="adae1-113">Retourne \_ un ou un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="adae1-113">Returns S\_OK or an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="adae1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="adae1-114">Remarks</span></span>

<span data-ttu-id="adae1-115">Cette méthode appelle simplement [**CBaseReferenceClock :: SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span><span class="sxs-lookup"><span data-stu-id="adae1-115">This method simply calls [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span></span>

<span data-ttu-id="adae1-116">Les valeurs d’heure retournées par [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) augmentent de manière monotone.</span><span class="sxs-lookup"><span data-stu-id="adae1-116">The time values returned by [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) are monotonically increasing.</span></span> <span data-ttu-id="adae1-117">Si vous redéfinissez l’horloge, **getTime** continue à signaler l’ancienne fois jusqu’à ce que l’horloge interne rattrape.</span><span class="sxs-lookup"><span data-stu-id="adae1-117">If you set the clock back, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="adae1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adae1-118">Requirements</span></span>



| <span data-ttu-id="adae1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adae1-119">Requirement</span></span> | <span data-ttu-id="adae1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="adae1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adae1-121">Version</span><span class="sxs-lookup"><span data-stu-id="adae1-121">Version</span></span><br/> | <span data-ttu-id="adae1-122">CSystemClock, classe</span><span class="sxs-lookup"><span data-stu-id="adae1-122">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="adae1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="adae1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="adae1-124"><dt>Sysclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adae1-124"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="adae1-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adae1-125">Library</span></span><br/> | <dl> <span data-ttu-id="adae1-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="adae1-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




