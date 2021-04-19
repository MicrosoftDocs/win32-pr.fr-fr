---
description: 'La méthode ReceiveCanBlock détermine si les appels à la méthode IMemInputPin :: Receive peuvent se bloquer. Cette méthode implémente la méthode IMemInputPin :: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Méthode CBaseInputPin. ReceiveCanBlock (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541759"
---
# <a name="cbaseinputpinreceivecanblock-method"></a><span data-ttu-id="dd41d-104">Méthode CBaseInputPin. ReceiveCanBlock</span><span class="sxs-lookup"><span data-stu-id="dd41d-104">CBaseInputPin.ReceiveCanBlock method</span></span>

<span data-ttu-id="dd41d-105">La `ReceiveCanBlock` méthode détermine si les appels à la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) peuvent se bloquer.</span><span class="sxs-lookup"><span data-stu-id="dd41d-105">The `ReceiveCanBlock` method determines whether calls to the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method might block.</span></span> <span data-ttu-id="dd41d-106">Cette méthode implémente la méthode [**IMemInputPin :: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .</span><span class="sxs-lookup"><span data-stu-id="dd41d-106">This method implements the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd41d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd41d-107">Syntax</span></span>


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a><span data-ttu-id="dd41d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd41d-108">Parameters</span></span>

<span data-ttu-id="dd41d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd41d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd41d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd41d-110">Return value</span></span>

<span data-ttu-id="dd41d-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd41d-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dd41d-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dd41d-112">Possible value include those listed in the following table.</span></span>



| <span data-ttu-id="dd41d-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dd41d-113">Return code</span></span>                                                                             | <span data-ttu-id="dd41d-114">Description</span><span class="sxs-lookup"><span data-stu-id="dd41d-114">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="dd41d-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="dd41d-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="dd41d-116">Le pin ne se bloquera pas sur un appel à **Receive**.</span><span class="sxs-lookup"><span data-stu-id="dd41d-116">The pin will not block on a call to **Receive**.</span></span><br/> |
| <dl> <span data-ttu-id="dd41d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd41d-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="dd41d-118">Le code pin peut se bloquer sur un appel à **Receive**.</span><span class="sxs-lookup"><span data-stu-id="dd41d-118">The pin might block on a call to **Receive**.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="dd41d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="dd41d-119">Remarks</span></span>

<span data-ttu-id="dd41d-120">Retourne la \_ valeur false si les appels à la méthode **Receive** ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="dd41d-120">Return S\_FALSE if calls to the **Receive** method are guaranteed not to block.</span></span> <span data-ttu-id="dd41d-121">Sinon, retourne S \_ OK ou un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dd41d-121">Otherwise, return S\_OK or an error code.</span></span> <span data-ttu-id="dd41d-122">Si la méthode de **réception** appelle **Receive** sur un code confidentiel en aval, le code pin en aval peut se bloquer. `ReceiveCanBlock` ce facteur doit être pris en compte.</span><span class="sxs-lookup"><span data-stu-id="dd41d-122">If the **Receive** method calls **Receive** on a downstream pin, the downstream pin might block; `ReceiveCanBlock` must take that factor into account.</span></span>

<span data-ttu-id="dd41d-123">Un filtre amont peut utiliser cette méthode pour déterminer sa stratégie de thread.</span><span class="sxs-lookup"><span data-stu-id="dd41d-123">An upstream filter can use this method to determine its threading strategy.</span></span> <span data-ttu-id="dd41d-124">Si la méthode de **réception** est bloquée, le filtre en amont peut décider d’utiliser un thread de travail qui met en mémoire tampon les données.</span><span class="sxs-lookup"><span data-stu-id="dd41d-124">If the **Receive** method might block, the upstream filter might decide to use a worker thread that buffers data.</span></span> <span data-ttu-id="dd41d-125">Pour une implémentation de cette stratégie, consultez la classe [**COutputQueue**](coutputqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="dd41d-125">See the [**COutputQueue**](coutputqueue.md) class for an implementation of this strategy.</span></span>

<span data-ttu-id="dd41d-126">Dans la classe de base, cette méthode retourne S \_ OK lorsque l’une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="dd41d-126">In the base class, this method returns S\_OK when any of the following are true:</span></span>

-   <span data-ttu-id="dd41d-127">Le filtre n’a aucune broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="dd41d-127">The filter has no output pins.</span></span>
-   <span data-ttu-id="dd41d-128">Une broche d’entrée connectée à ce filtre signale qu’elle peut se bloquer.</span><span class="sxs-lookup"><span data-stu-id="dd41d-128">An input pin connected to this filter signals that it might block.</span></span>
-   <span data-ttu-id="dd41d-129">Une broche d’entrée connectée à ce filtre ne prend pas en charge l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="dd41d-129">An input pin connected to this filter does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd41d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd41d-130">Requirements</span></span>



| <span data-ttu-id="dd41d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd41d-131">Requirement</span></span> | <span data-ttu-id="dd41d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd41d-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd41d-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd41d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dd41d-134"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd41d-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dd41d-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd41d-135">Library</span></span><br/> | <dl> <span data-ttu-id="dd41d-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dd41d-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd41d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd41d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd41d-138">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="dd41d-138">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




