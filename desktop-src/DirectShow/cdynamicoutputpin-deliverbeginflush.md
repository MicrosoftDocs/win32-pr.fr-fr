---
description: La méthode DeliverBeginFlush demande à la broche d’entrée connectée de commencer une opération de vidage.
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
ms.openlocfilehash: 242394a327b63fcc901b08f572096bf2f42238b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542366"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="b0b7a-103">Méthode CDynamicOutputPin. DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="b0b7a-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="b0b7a-104">La `DeliverBeginFlush` méthode demande à la broche d’entrée connectée de commencer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b7a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0b7a-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="b0b7a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0b7a-106">Parameters</span></span>

<span data-ttu-id="b0b7a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0b7a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0b7a-108">Return value</span></span>

<span data-ttu-id="b0b7a-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b7a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b0b7a-110">Remarks</span></span>

<span data-ttu-id="b0b7a-111">Cette méthode remplace la méthode [**CBaseOutputPin ::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b7a-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="b0b7a-112">Il définit l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b7a-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b7a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0b7a-113">Requirements</span></span>



| <span data-ttu-id="b0b7a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0b7a-114">Requirement</span></span> | <span data-ttu-id="b0b7a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b7a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b7a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0b7a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b0b7a-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0b7a-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b0b7a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0b7a-118">Library</span></span><br/> | <dl> <span data-ttu-id="b0b7a-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0b7a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b7a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0b7a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b7a-121">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="b0b7a-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




