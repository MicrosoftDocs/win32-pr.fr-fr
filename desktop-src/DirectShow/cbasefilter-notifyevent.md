---
description: La méthode NotifyEvent envoie une notification d’événement au gestionnaire de graphique de filtre.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Méthode CBaseFilter. NotifyEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523443"
---
# <a name="cbasefilternotifyevent-method"></a><span data-ttu-id="236f7-103">Méthode CBaseFilter. NotifyEvent</span><span class="sxs-lookup"><span data-stu-id="236f7-103">CBaseFilter.NotifyEvent method</span></span>

<span data-ttu-id="236f7-104">La `NotifyEvent` méthode envoie une notification d’événement au gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="236f7-104">The `NotifyEvent` method sends an event notification to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="236f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="236f7-105">Syntax</span></span>


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a><span data-ttu-id="236f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="236f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="236f7-107">*EventCode*</span><span class="sxs-lookup"><span data-stu-id="236f7-107">*EventCode*</span></span> 
</dt> <dd>

<span data-ttu-id="236f7-108">Code de notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="236f7-108">Event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="236f7-109">*EventParam1*</span><span class="sxs-lookup"><span data-stu-id="236f7-109">*EventParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="236f7-110">Premier paramètre de l’événement.</span><span class="sxs-lookup"><span data-stu-id="236f7-110">First parameter of the event.</span></span>

</dd> <dt>

<span data-ttu-id="236f7-111">*EventParam2*</span><span class="sxs-lookup"><span data-stu-id="236f7-111">*EventParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="236f7-112">Deuxième paramètre de l’événement.</span><span class="sxs-lookup"><span data-stu-id="236f7-112">Second parameter of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="236f7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="236f7-113">Return value</span></span>

<span data-ttu-id="236f7-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="236f7-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="236f7-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="236f7-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="236f7-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="236f7-116">Return code</span></span>                                                                               | <span data-ttu-id="236f7-117">Description</span><span class="sxs-lookup"><span data-stu-id="236f7-117">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="236f7-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="236f7-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="236f7-119">Le gestionnaire de graphique de filtre n’accepte pas les notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="236f7-119">The filter graph manager is not accepting event notifications.</span></span><br/>                              |
| <dl> <span data-ttu-id="236f7-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="236f7-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="236f7-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="236f7-121">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="236f7-122"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="236f7-122"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="236f7-123">Le filtre n’a pas de pointeur vers l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="236f7-123">Filter does not have a pointer to the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="236f7-124">Notes</span><span class="sxs-lookup"><span data-stu-id="236f7-124">Remarks</span></span>

<span data-ttu-id="236f7-125">Pour obtenir la liste des codes de notification et des valeurs de paramètres, consultez [codes de notification d’événement](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="236f7-125">For a list of notification codes and parameter values, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="236f7-126">Dans la classe de base, si le code d’événement est EC \_ Complete, la méthode définit le paramètre *EventParam2* sur un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre.</span><span class="sxs-lookup"><span data-stu-id="236f7-126">In the base class, if the event code is EC\_COMPLETE, the method sets the *EventParam2* parameter to a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="236f7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="236f7-127">Requirements</span></span>



| <span data-ttu-id="236f7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="236f7-128">Requirement</span></span> | <span data-ttu-id="236f7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="236f7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="236f7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="236f7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="236f7-131"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="236f7-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="236f7-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="236f7-132">Library</span></span><br/> | <dl> <span data-ttu-id="236f7-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="236f7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="236f7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="236f7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="236f7-135">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="236f7-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




