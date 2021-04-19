---
description: La méthode StartUsingOutputPin obtient l’accès au code confidentiel pour une opération de diffusion en continu.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Méthode CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541720"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a><span data-ttu-id="71d49-103">Méthode CDynamicOutputPin. StartUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="71d49-103">CDynamicOutputPin.StartUsingOutputPin method</span></span>

<span data-ttu-id="71d49-104">La `StartUsingOutputPin` méthode obtient l’accès au code confidentiel pour une opération de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="71d49-104">The `StartUsingOutputPin` method obtains access to the pin for a streaming operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d49-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71d49-105">Syntax</span></span>


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="71d49-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71d49-106">Parameters</span></span>

<span data-ttu-id="71d49-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="71d49-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71d49-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71d49-108">Return value</span></span>

<span data-ttu-id="71d49-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71d49-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71d49-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="71d49-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="71d49-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="71d49-111">Return code</span></span>                                                                                           | <span data-ttu-id="71d49-112">Description</span><span class="sxs-lookup"><span data-stu-id="71d49-112">Description</span></span>                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="71d49-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71d49-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="71d49-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="71d49-114">Success.</span></span><br/>                                               |
| <dl> <span data-ttu-id="71d49-115"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="71d49-115"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>          | <span data-ttu-id="71d49-116">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="71d49-116">Unexpected error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="71d49-117"><dt>**\_État VFW \_ E \_ modifié**</dt></span><span class="sxs-lookup"><span data-stu-id="71d49-117"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="71d49-118">Le filtre a été arrêté ou le code pin a commencé à être vidé.</span><span class="sxs-lookup"><span data-stu-id="71d49-118">The filter was stopped, or the pin has begun flushing.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71d49-119">Notes</span><span class="sxs-lookup"><span data-stu-id="71d49-119">Remarks</span></span>

<span data-ttu-id="71d49-120">Appelez cette méthode avant d’appeler des méthodes qui fournissent des données à la broche d’entrée connectée ou qui modifient le type de média de la connexion.</span><span class="sxs-lookup"><span data-stu-id="71d49-120">Call this method before calling any methods that deliver data to the connected input pin or that change the connection's media type.</span></span> <span data-ttu-id="71d49-121">Par exemple, cette règle s’applique aux méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="71d49-121">For example, this rule applies to the following methods:</span></span>

-   [<span data-ttu-id="71d49-122">**CDynamicOutputPin::ChangeOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="71d49-122">**CDynamicOutputPin::ChangeOutputFormat**</span></span>](cdynamicoutputpin-changeoutputformat.md)
-   [<span data-ttu-id="71d49-123">**CDynamicOutputPin::ChangeMediaType**</span><span class="sxs-lookup"><span data-stu-id="71d49-123">**CDynamicOutputPin::ChangeMediaType**</span></span>](cdynamicoutputpin-changemediatype.md)
-   [<span data-ttu-id="71d49-124">**CDynamicOutputPin ::D ynamicReconnect**</span><span class="sxs-lookup"><span data-stu-id="71d49-124">**CDynamicOutputPin::DynamicReconnect**</span></span>](cdynamicoutputpin-dynamicreconnect.md)
-   [<span data-ttu-id="71d49-125">**CBaseOutputPin ::D eliver**</span><span class="sxs-lookup"><span data-stu-id="71d49-125">**CBaseOutputPin::Deliver**</span></span>](cbaseoutputpin-deliver.md)
-   [<span data-ttu-id="71d49-126">**CBaseOutputPin ::D eliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="71d49-126">**CBaseOutputPin::DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md)
-   [<span data-ttu-id="71d49-127">**CBaseOutputPin ::D eliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="71d49-127">**CBaseOutputPin::DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)
-   [<span data-ttu-id="71d49-128">**IMemInputPin :: Receive**</span><span class="sxs-lookup"><span data-stu-id="71d49-128">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="71d49-129">**IMemInputPin::ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="71d49-129">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="71d49-130">**IPin :: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="71d49-130">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="71d49-131">**IPin::NewSegment**</span><span class="sxs-lookup"><span data-stu-id="71d49-131">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

<span data-ttu-id="71d49-132">Ensuite, appelez la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) pour libérer l’accès au code PIN.</span><span class="sxs-lookup"><span data-stu-id="71d49-132">Afterward, call the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method to release the access to the pin.</span></span>

<span data-ttu-id="71d49-133">Si le code PIN est bloqué, `StartUsingOutputPin` attend le déblocage du code PIN.</span><span class="sxs-lookup"><span data-stu-id="71d49-133">If the pin is blocked, `StartUsingOutputPin` waits for the pin to become unblocked.</span></span> <span data-ttu-id="71d49-134">Si le filtre s’arrête pendant que la méthode attend, la méthode retourne immédiatement \_ l' \_ État VFW E \_ modifié.</span><span class="sxs-lookup"><span data-stu-id="71d49-134">If the filter stops while the method is waiting, the method immediately returns VFW\_E\_STATE\_CHANGED.</span></span> <span data-ttu-id="71d49-135">Le code PIN gère le nombre de fois que `StartUsingOutputPin` a été appelé sans appel correspondant à **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="71d49-135">The pin maintains a count of how many times `StartUsingOutputPin` has been called without a corresponding call to **StopUsingOutputPin**.</span></span> <span data-ttu-id="71d49-136">Si un autre thread tente de bloquer le pin alors que ce nombre est différent de zéro, le code PIN définit son état de blocage sur « en attente ».</span><span class="sxs-lookup"><span data-stu-id="71d49-136">If another thread tries to block the pin while this count is non-zero, the pin sets its blocking status to "pending."</span></span> <span data-ttu-id="71d49-137">Le code PIN est bloqué une fois que toutes les opérations de streaming sont terminées, dans le dernier appel à **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="71d49-137">The pin becomes blocked once all of the streaming operations have completed, in the final call to **StopUsingOutputPin**.</span></span>

<span data-ttu-id="71d49-138">Ne conservez pas la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) lorsque vous appelez cette méthode.</span><span class="sxs-lookup"><span data-stu-id="71d49-138">Do not hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section when you call this method.</span></span> <span data-ttu-id="71d49-139">Dans le cas contraire, si le code PIN est bloqué, il ne peut jamais être débloqué, provoquant ainsi un blocage.</span><span class="sxs-lookup"><span data-stu-id="71d49-139">Otherwise, if the pin is blocked, it can never become unblocked, causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d49-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71d49-140">Requirements</span></span>



| <span data-ttu-id="71d49-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71d49-141">Requirement</span></span> | <span data-ttu-id="71d49-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="71d49-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d49-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="71d49-143">Header</span></span><br/>  | <dl> <span data-ttu-id="71d49-144"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71d49-144"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71d49-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71d49-145">Library</span></span><br/> | <dl> <span data-ttu-id="71d49-146"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="71d49-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d49-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71d49-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d49-148">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="71d49-148">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




