---
description: Si la fin du flux a été atteinte, la méthode SendEndOfStream planifie un \_ événement d’achèvement ce pour le gestionnaire de graphes de filtre.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Méthode CBaseRenderer. SendEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541275"
---
# <a name="cbaserenderersendendofstream-method"></a><span data-ttu-id="7336f-103">Méthode CBaseRenderer. SendEndOfStream</span><span class="sxs-lookup"><span data-stu-id="7336f-103">CBaseRenderer.SendEndOfStream method</span></span>

<span data-ttu-id="7336f-104">Si la fin du flux a été atteinte, la `SendEndOfStream` méthode planifie un \_ événement d’achèvement ce pour le gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="7336f-104">If end-of-stream was reached, the `SendEndOfStream` method schedules an EC\_COMPLETE event for the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="7336f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7336f-105">Syntax</span></span>


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="7336f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7336f-106">Parameters</span></span>

<span data-ttu-id="7336f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7336f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7336f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7336f-108">Return value</span></span>

<span data-ttu-id="7336f-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7336f-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7336f-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7336f-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7336f-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7336f-111">Return code</span></span>                                                                             | <span data-ttu-id="7336f-112">Description</span><span class="sxs-lookup"><span data-stu-id="7336f-112">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7336f-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7336f-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7336f-114">Le gestionnaire de graphique de filtre n’accepte pas les notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="7336f-114">The filter graph manager is not accepting event notifications.</span></span><br/> |
| <dl> <span data-ttu-id="7336f-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7336f-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7336f-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7336f-116">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7336f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7336f-117">Remarks</span></span>

<span data-ttu-id="7336f-118">Le filtre peut recevoir une notification de fin de flux avant l’heure d’arrêt de l’exemple actuel.</span><span class="sxs-lookup"><span data-stu-id="7336f-118">The filter might receive an end-of-stream notification before the current sample's stop time.</span></span> <span data-ttu-id="7336f-119">Si c’est le cas, le filtre doit attendre avant de publier une notification d' [**\_ achèvement ce**](ec-complete.md) dans le gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="7336f-119">If so, the filter should wait before posting an [**EC\_COMPLETE**](ec-complete.md) notification to the filter graph manager.</span></span>

<span data-ttu-id="7336f-120">Par conséquent :</span><span class="sxs-lookup"><span data-stu-id="7336f-120">Therefore:</span></span>

-   <span data-ttu-id="7336f-121">Si le filtre a reçu une notification EOS (End-of-Stream) précoce, cette méthode planifie un événement de minuterie.</span><span class="sxs-lookup"><span data-stu-id="7336f-121">If the filter has received an early end-of-stream (EOS) notification, this method schedules a timer event.</span></span> <span data-ttu-id="7336f-122">Lorsque l’événement du minuteur est activé, le filtre publie l' \_ événement EC Complete.</span><span class="sxs-lookup"><span data-stu-id="7336f-122">When the timer event is activated, the filter posts the EC\_COMPLETE event.</span></span>
-   <span data-ttu-id="7336f-123">Si le filtre a reçu une notification EOS qui n’était pas précoce, cette méthode publie \_ immédiatement l’événement EC Complete.</span><span class="sxs-lookup"><span data-stu-id="7336f-123">If the filter has received an EOS notification that was not early, this method posts the EC\_COMPLETE event immediately.</span></span>
-   <span data-ttu-id="7336f-124">Si le filtre n’a pas de notification EOS en attente, la méthode retourne sans rien faire.</span><span class="sxs-lookup"><span data-stu-id="7336f-124">If the filter does not have any pending EOS notification, the method returns without doing anything.</span></span>

<span data-ttu-id="7336f-125">La méthode de rappel de la minuterie est [**CBaseRenderer :: TimerCallback**](cbaserenderer-timercallback.md).</span><span class="sxs-lookup"><span data-stu-id="7336f-125">The timer callback method is [**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md).</span></span> <span data-ttu-id="7336f-126">Pour remettre l' \_ événement EC Complete, le filtre appelle la méthode [**CBaseRenderer :: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="7336f-126">To deliver the EC\_COMPLETE event, the filter calls the [**CBaseRenderer::NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7336f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7336f-127">Requirements</span></span>



| <span data-ttu-id="7336f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7336f-128">Requirement</span></span> | <span data-ttu-id="7336f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7336f-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7336f-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="7336f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7336f-131"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7336f-131"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7336f-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7336f-132">Library</span></span><br/> | <dl> <span data-ttu-id="7336f-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7336f-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7336f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7336f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7336f-135">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="7336f-135">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




