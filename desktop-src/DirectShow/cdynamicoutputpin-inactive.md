---
description: La méthode inactive indique au code confidentiel que le filtre a été arrêté.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: CDynamicOutputPin. inactive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528366"
---
# <a name="cdynamicoutputpininactive-method"></a><span data-ttu-id="c48b2-103">CDynamicOutputPin. inactive, méthode</span><span class="sxs-lookup"><span data-stu-id="c48b2-103">CDynamicOutputPin.Inactive method</span></span>

<span data-ttu-id="c48b2-104">La `Inactive` méthode notifie le code confidentiel que le filtre a arrêté.</span><span class="sxs-lookup"><span data-stu-id="c48b2-104">The `Inactive` method notifies the pin that the filter has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c48b2-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="c48b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c48b2-106">Parameters</span></span>

<span data-ttu-id="c48b2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c48b2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c48b2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c48b2-108">Return value</span></span>

<span data-ttu-id="c48b2-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="c48b2-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c48b2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c48b2-110">Remarks</span></span>

<span data-ttu-id="c48b2-111">Cette méthode remplace la méthode [**CBaseOutputPin :: inactive**](cbaseoutputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="c48b2-111">This method overrides the [**CBaseOutputPin::Inactive**](cbaseoutputpin-inactive.md) method.</span></span> <span data-ttu-id="c48b2-112">Il définit l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="c48b2-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c48b2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c48b2-113">Requirements</span></span>



| <span data-ttu-id="c48b2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c48b2-114">Requirement</span></span> | <span data-ttu-id="c48b2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c48b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c48b2-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c48b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c48b2-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c48b2-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c48b2-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c48b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="c48b2-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c48b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c48b2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c48b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48b2-121">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="c48b2-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




