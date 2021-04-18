---
description: 'La méthode NewSegment avertit le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment. Implémente la méthode IPin :: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Méthode CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532879"
---
# <a name="cbasepinnewsegment-method"></a><span data-ttu-id="a0ef2-104">Méthode CBasePin. NewSegment</span><span class="sxs-lookup"><span data-stu-id="a0ef2-104">CBasePin.NewSegment method</span></span>

<span data-ttu-id="a0ef2-105">La `NewSegment` méthode notifie le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment.</span><span class="sxs-lookup"><span data-stu-id="a0ef2-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="a0ef2-106">Implémente la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="a0ef2-106">Implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ef2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0ef2-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="a0ef2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0ef2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ef2-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="a0ef2-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ef2-110">Position du média de départ du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a0ef2-110">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef2-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="a0ef2-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ef2-112">Position du média de fin du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a0ef2-112">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef2-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="a0ef2-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ef2-114">Taux auquel ce segment doit être traité, sous la forme d’un pourcentage du taux d’origine.</span><span class="sxs-lookup"><span data-stu-id="a0ef2-114">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ef2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0ef2-115">Return value</span></span>

<span data-ttu-id="a0ef2-116">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0ef2-116">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0ef2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a0ef2-117">Remarks</span></span>

<span data-ttu-id="a0ef2-118">Cette méthode définit les variables membres [**CBasePin :: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin :: m \_ tStop**](cbasepin-m-tstop.md)et [**CBasePin :: m \_ dRate**](cbasepin-m-drate.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ef2-118">This method sets the [**CBasePin::m\_tStart**](cbasepin-m-tstart.md), [**CBasePin::m\_tStop**](cbasepin-m-tstop.md), and [**CBasePin::m\_dRate**](cbasepin-m-drate.md) member variables.</span></span> <span data-ttu-id="a0ef2-119">Dans votre classe dérivée, substituez cette méthode pour passer la notification en aval.</span><span class="sxs-lookup"><span data-stu-id="a0ef2-119">In your derived class, override this method to pass the notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ef2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0ef2-120">Requirements</span></span>



| <span data-ttu-id="a0ef2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0ef2-121">Requirement</span></span> | <span data-ttu-id="a0ef2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0ef2-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ef2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0ef2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a0ef2-124"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ef2-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a0ef2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a0ef2-125">Library</span></span><br/> | <dl> <span data-ttu-id="a0ef2-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ef2-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0ef2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0ef2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ef2-128">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="a0ef2-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




