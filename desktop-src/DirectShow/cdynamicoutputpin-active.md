---
description: La méthode active indique au code confidentiel que le filtre est maintenant actif.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: CDynamicOutputPin. active, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533252"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="0bada-103">CDynamicOutputPin. active, méthode</span><span class="sxs-lookup"><span data-stu-id="0bada-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="0bada-104">La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="0bada-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bada-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bada-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="0bada-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bada-106">Parameters</span></span>

<span data-ttu-id="0bada-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0bada-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bada-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bada-108">Return value</span></span>

<span data-ttu-id="0bada-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0bada-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0bada-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0bada-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0bada-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0bada-111">Return code</span></span>                                                                            | <span data-ttu-id="0bada-112">Description</span><span class="sxs-lookup"><span data-stu-id="0bada-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0bada-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0bada-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0bada-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0bada-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0bada-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0bada-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0bada-116">Échec.</span><span class="sxs-lookup"><span data-stu-id="0bada-116">Failure.</span></span> <span data-ttu-id="0bada-117">[**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) n’a pas été appelé.</span><span class="sxs-lookup"><span data-stu-id="0bada-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0bada-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0bada-118">Remarks</span></span>

<span data-ttu-id="0bada-119">Cette méthode remplace la méthode [**CBaseOutputPin :: active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="0bada-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="0bada-120">Il réinitialise l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="0bada-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="0bada-121">Si le filtre propriétaire n’a pas appelé **SetConfigInfo**, cette méthode retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="0bada-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bada-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bada-122">Requirements</span></span>



| <span data-ttu-id="0bada-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bada-123">Requirement</span></span> | <span data-ttu-id="0bada-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bada-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bada-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bada-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0bada-126"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bada-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0bada-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bada-127">Library</span></span><br/> | <dl> <span data-ttu-id="0bada-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0bada-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bada-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bada-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bada-130">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="0bada-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




