---
description: La méthode SetTimeDelta ajuste l’heure de l’horloge interne.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Méthode CBaseReferenceClock. SetTimeDelta (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544044"
---
# <a name="cbasereferenceclocksettimedelta-method"></a><span data-ttu-id="7957d-103">Méthode CBaseReferenceClock. SetTimeDelta</span><span class="sxs-lookup"><span data-stu-id="7957d-103">CBaseReferenceClock.SetTimeDelta method</span></span>

<span data-ttu-id="7957d-104">La `SetTimeDelta` méthode ajuste l’heure de l’horloge interne.</span><span class="sxs-lookup"><span data-stu-id="7957d-104">The `SetTimeDelta` method adjusts the internal clock time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7957d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7957d-105">Syntax</span></span>


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a><span data-ttu-id="7957d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7957d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7957d-107">*TimeDelta* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="7957d-107">*TimeDelta* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7957d-108">Montant pour ajuster l’heure de l’horloge, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="7957d-108">Amount to adjust the clock time, in 100-nanosecond units.</span></span> <span data-ttu-id="7957d-109">Une valeur positive déplace l’avance de l’horloge et une valeur négative déplace l’horloge vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="7957d-109">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7957d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7957d-110">Return value</span></span>

<span data-ttu-id="7957d-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7957d-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7957d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7957d-112">Remarks</span></span>

<span data-ttu-id="7957d-113">La classe dérivée peut utiliser cette méthode pour ajuster l’horloge interne, si elle dérive du périphérique qui fournit des informations de minutage.</span><span class="sxs-lookup"><span data-stu-id="7957d-113">The derived class can use this method to adjust the internal clock, if it drifts from the device that is providing timing information.</span></span>

<span data-ttu-id="7957d-114">La méthode [**CBaseReferenceClock :: getTime**](cbasereferenceclock-gettime.md) ne retourne jamais de valeurs décroissantes.</span><span class="sxs-lookup"><span data-stu-id="7957d-114">The [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method never returns decreasing values.</span></span> <span data-ttu-id="7957d-115">Si vous ajustez l’horloge vers l’arrière, **getTime** retourne la valeur précédente jusqu’à ce que l’horloge atteigne à nouveau cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7957d-115">If you adjust the clock backward, **GetTime** returns the previous value until the clock reaches that value again.</span></span>

## <a name="requirements"></a><span data-ttu-id="7957d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7957d-116">Requirements</span></span>



| <span data-ttu-id="7957d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7957d-117">Requirement</span></span> | <span data-ttu-id="7957d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7957d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7957d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7957d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7957d-120"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7957d-120"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7957d-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7957d-121">Library</span></span><br/> | <dl> <span data-ttu-id="7957d-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7957d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7957d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7957d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7957d-124">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="7957d-124">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




