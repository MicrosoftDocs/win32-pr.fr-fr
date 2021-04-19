---
description: La méthode AsynchronousBlockOutputPin bloque le code confidentiel. La méthode peut retourner avant que le code confidentiel soit bloqué.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Méthode CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542784"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a><span data-ttu-id="d1078-104">Méthode CDynamicOutputPin. AsynchronousBlockOutputPin</span><span class="sxs-lookup"><span data-stu-id="d1078-104">CDynamicOutputPin.AsynchronousBlockOutputPin method</span></span>

<span data-ttu-id="d1078-105">La `AsynchronousBlockOutputPin` méthode bloque le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d1078-105">The `AsynchronousBlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="d1078-106">La méthode peut retourner avant que le code confidentiel soit bloqué.</span><span class="sxs-lookup"><span data-stu-id="d1078-106">The method might return before the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1078-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1078-107">Syntax</span></span>


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a><span data-ttu-id="d1078-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1078-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1078-109">*hNotifyCallerPinBlockedEvent*</span><span class="sxs-lookup"><span data-stu-id="d1078-109">*hNotifyCallerPinBlockedEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="d1078-110">Handle vers un événement.</span><span class="sxs-lookup"><span data-stu-id="d1078-110">Handle to an event.</span></span> <span data-ttu-id="d1078-111">L’événement est signalé lorsque la broche de sortie est bloquée, ou si l’appelant annule l’opération de blocage.</span><span class="sxs-lookup"><span data-stu-id="d1078-111">The event is signaled when the output pin is blocked, or if the caller cancels the block operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1078-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1078-112">Return value</span></span>

<span data-ttu-id="d1078-113">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1078-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d1078-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1078-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d1078-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d1078-115">Return code</span></span>                                                                                                                    | <span data-ttu-id="d1078-116">Description</span><span class="sxs-lookup"><span data-stu-id="d1078-116">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="d1078-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1078-117"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="d1078-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d1078-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d1078-119"><dt>**\_code PIN de VFW E \_ \_ déjà \_ bloqué**</dt></span><span class="sxs-lookup"><span data-stu-id="d1078-119"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="d1078-120">Le code PIN est déjà bloqué sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="d1078-120">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="d1078-121"><dt>**\_ \_ code PIN de VFW E \_ déjà \_ bloqué \_ sur \_ ce \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="d1078-121"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="d1078-122">Le code PIN est déjà bloqué sur le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="d1078-122">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1078-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d1078-123">Remarks</span></span>

<span data-ttu-id="d1078-124">N’appelez pas cette méthode à partir du thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="d1078-124">Do not call this method from the streaming thread.</span></span>

<span data-ttu-id="d1078-125">Si aucun thread de streaming n’utilise le code confidentiel, cette méthode bloque immédiatement le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d1078-125">If no streaming thread is using the pin, this method immediately blocks the pin.</span></span> <span data-ttu-id="d1078-126">Dans le cas contraire, elle définit l’état du pin sur « Pending » et retourne.</span><span class="sxs-lookup"><span data-stu-id="d1078-126">Otherwise, it sets the pin status to "pending" and returns.</span></span> <span data-ttu-id="d1078-127">Lorsque l’opération de diffusion en continu est terminée, le thread de streaming appelle la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , qui bloque le code confidentiel et signale l’événement **hNotifyCallerPinBlockedEvent** .</span><span class="sxs-lookup"><span data-stu-id="d1078-127">When the streaming operation completes, the streaming thread calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, which blocks the pin and signals the **hNotifyCallerPinBlockedEvent** event.</span></span> <span data-ttu-id="d1078-128">Pour annuler un bloc en attente, appelez la méthode [**CDynamicOutputPin :: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="d1078-128">To cancel a pending block, call the [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1078-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1078-129">Requirements</span></span>



| <span data-ttu-id="d1078-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1078-130">Requirement</span></span> | <span data-ttu-id="d1078-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1078-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1078-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1078-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d1078-133"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1078-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d1078-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1078-134">Library</span></span><br/> | <dl> <span data-ttu-id="d1078-135"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1078-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1078-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1078-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1078-137">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="d1078-137">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




