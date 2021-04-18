---
description: La méthode DeliverEndFlush demande à la broche d’entrée connectée de terminer une opération de vidage.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Méthode CDynamicOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540171"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="4e4cc-103">Méthode CDynamicOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="4e4cc-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="4e4cc-104">La `DeliverEndFlush` méthode demande à la broche d’entrée connectée de terminer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="4e4cc-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e4cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e4cc-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="4e4cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e4cc-106">Parameters</span></span>

<span data-ttu-id="4e4cc-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e4cc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e4cc-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e4cc-108">Return value</span></span>

<span data-ttu-id="4e4cc-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="4e4cc-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e4cc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4e4cc-110">Remarks</span></span>

<span data-ttu-id="4e4cc-111">Cette méthode remplace la méthode [**CBaseOutputPin ::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4cc-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="4e4cc-112">Il réinitialise l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4cc-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e4cc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e4cc-113">Requirements</span></span>



| <span data-ttu-id="4e4cc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e4cc-114">Requirement</span></span> | <span data-ttu-id="4e4cc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e4cc-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4cc-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e4cc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4e4cc-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e4cc-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e4cc-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e4cc-118">Library</span></span><br/> | <dl> <span data-ttu-id="4e4cc-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4e4cc-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e4cc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e4cc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e4cc-121">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="4e4cc-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




