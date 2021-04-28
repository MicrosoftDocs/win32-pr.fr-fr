---
description: 'Méthode CDynamicOutputPin. DeliverBeginFlush : la méthode DeliverBeginFlush demande à la broche d’entrée connectée de commencer une opération de vidage.'
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Méthode CDynamicOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099317"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="753f3-103">Méthode CDynamicOutputPin. DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="753f3-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="753f3-104">La `DeliverBeginFlush` méthode demande à la broche d’entrée connectée de commencer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="753f3-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="753f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="753f3-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="753f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="753f3-106">Parameters</span></span>

<span data-ttu-id="753f3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="753f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="753f3-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="753f3-108">Return value</span></span>

<span data-ttu-id="753f3-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="753f3-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="753f3-110">Notes </span><span class="sxs-lookup"><span data-stu-id="753f3-110">Remarks</span></span>

<span data-ttu-id="753f3-111">Cette méthode remplace la méthode [**CBaseOutputPin ::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="753f3-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="753f3-112">Il définit l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="753f3-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="753f3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="753f3-113">Requirements</span></span>



| <span data-ttu-id="753f3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="753f3-114">Requirement</span></span> | <span data-ttu-id="753f3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="753f3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="753f3-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="753f3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="753f3-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="753f3-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="753f3-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="753f3-118">Library</span></span><br/> | <dl> <span data-ttu-id="753f3-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="753f3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="753f3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="753f3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="753f3-121">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="753f3-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




