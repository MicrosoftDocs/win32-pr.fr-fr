---
description: La méthode deliver fournit un exemple de support à la broche d’entrée connectée.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: CBaseOutputPin. Deliver, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521707"
---
# <a name="cbaseoutputpindeliver-method"></a><span data-ttu-id="9da81-103">CBaseOutputPin. Deliver, méthode</span><span class="sxs-lookup"><span data-stu-id="9da81-103">CBaseOutputPin.Deliver method</span></span>

<span data-ttu-id="9da81-104">La `Deliver` méthode remet un échantillon de média à la broche d’entrée connectée.</span><span class="sxs-lookup"><span data-stu-id="9da81-104">The `Deliver` method delivers a media sample to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da81-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9da81-105">Syntax</span></span>


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="9da81-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9da81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da81-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="9da81-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="9da81-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9da81-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9da81-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9da81-109">Return value</span></span>

<span data-ttu-id="9da81-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9da81-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9da81-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9da81-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9da81-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9da81-112">Return code</span></span>                                                                                           | <span data-ttu-id="9da81-113">Description</span><span class="sxs-lookup"><span data-stu-id="9da81-113">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9da81-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9da81-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="9da81-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9da81-115">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="9da81-116"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="9da81-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9da81-117">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="9da81-117">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9da81-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9da81-118">Remarks</span></span>

<span data-ttu-id="9da81-119">Cette méthode appelle la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9da81-119">This method calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input pin.</span></span> <span data-ttu-id="9da81-120">**Receive** peut être bloqué si la méthode [**IMemInputPin :: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9da81-120">**Receive** can block if the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method returns S\_OK.</span></span>

<span data-ttu-id="9da81-121">Libérez l’exemple après avoir appelé cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9da81-121">Release the sample after calling this method.</span></span> <span data-ttu-id="9da81-122">La broche d’entrée peut contenir un décompte de références sur l’échantillon, donc ne pas réutiliser l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9da81-122">The input pin might hold a reference count on the sample, so do not reuse the sample.</span></span> <span data-ttu-id="9da81-123">Appelez toujours la méthode [**CBaseOutputPin :: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) pour obtenir un nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="9da81-123">Always call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain a new sample.</span></span>

<span data-ttu-id="9da81-124">Maintenez la section critique du filtre avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9da81-124">Hold the filter's critical section before calling this method.</span></span> <span data-ttu-id="9da81-125">Dans le cas contraire, le code pin peut être déconnecté pendant l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="9da81-125">Otherwise, the pin might get disconnected during the method call.</span></span> <span data-ttu-id="9da81-126">Si le filtre utilise un thread de travail pour fournir des exemples, conservez la section critique lorsque le filtre est prêt à remettre un échantillon.</span><span class="sxs-lookup"><span data-stu-id="9da81-126">If the filter uses a worker thread to deliver samples, hold the critical section when the filter is ready to deliver a sample.</span></span> <span data-ttu-id="9da81-127">Dans le cas contraire, vous pouvez conserver la section critique dans la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) du filtre, où le filtre traite les exemples.</span><span class="sxs-lookup"><span data-stu-id="9da81-127">Otherwise, you can hold the critical section in the filter's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, where the filter processes samples.</span></span>

<span data-ttu-id="9da81-128">Les threads de travail peuvent créer un interblocage potentiel.</span><span class="sxs-lookup"><span data-stu-id="9da81-128">Worker threads can create a potential deadlock.</span></span> <span data-ttu-id="9da81-129">Lorsque le thread contient la section critique, il peut attendre une modification d’État dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="9da81-129">When the thread holds the critical section, it might wait on a state change in the filter.</span></span> <span data-ttu-id="9da81-130">En même temps, il est possible que le changement d’État attende que le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="9da81-130">At the same time, the state change might be waiting for the thread to complete.</span></span> <span data-ttu-id="9da81-131">Pour éviter cela, le code de modification d’État doit signaler un événement qui termine le thread, puis attendre que le thread signale la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9da81-131">To prevent this, the state-change code should signal an event that terminates the thread, and then wait for the thread to signal completion.</span></span>

## <a name="requirements"></a><span data-ttu-id="9da81-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9da81-132">Requirements</span></span>



| <span data-ttu-id="9da81-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9da81-133">Requirement</span></span> | <span data-ttu-id="9da81-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9da81-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da81-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="9da81-135">Header</span></span><br/>  | <dl> <span data-ttu-id="9da81-136"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9da81-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9da81-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9da81-137">Library</span></span><br/> | <dl> <span data-ttu-id="9da81-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9da81-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da81-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9da81-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da81-140">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="9da81-140">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




