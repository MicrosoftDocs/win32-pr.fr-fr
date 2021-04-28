---
description: 'Méthode CDynamicOutputPin. DeliverEndFlush : la méthode DeliverEndFlush demande à la broche d’entrée connectée de terminer une opération de vidage.'
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
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095707"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="581d0-103">Méthode CDynamicOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="581d0-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="581d0-104">La `DeliverEndFlush` méthode demande à la broche d’entrée connectée de terminer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="581d0-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="581d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="581d0-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="581d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="581d0-106">Parameters</span></span>

<span data-ttu-id="581d0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="581d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="581d0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="581d0-108">Return value</span></span>

<span data-ttu-id="581d0-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="581d0-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="581d0-110">Notes </span><span class="sxs-lookup"><span data-stu-id="581d0-110">Remarks</span></span>

<span data-ttu-id="581d0-111">Cette méthode remplace la méthode [**CBaseOutputPin ::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="581d0-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="581d0-112">Il réinitialise l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="581d0-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="581d0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="581d0-113">Requirements</span></span>



| <span data-ttu-id="581d0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="581d0-114">Requirement</span></span> | <span data-ttu-id="581d0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="581d0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="581d0-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="581d0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="581d0-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="581d0-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="581d0-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="581d0-118">Library</span></span><br/> | <dl> <span data-ttu-id="581d0-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="581d0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581d0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="581d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581d0-121">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="581d0-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




