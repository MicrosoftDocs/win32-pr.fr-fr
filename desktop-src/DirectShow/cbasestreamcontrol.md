---
description: Cette classe implémente l’interface IAMStreamControl pour les broches d’entrée et de sortie.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: CBaseStreamControl, classe (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532218"
---
# <a name="cbasestreamcontrol-class"></a><span data-ttu-id="897fe-103">CBaseStreamControl, classe</span><span class="sxs-lookup"><span data-stu-id="897fe-103">CBaseStreamControl class</span></span>

![hiérarchie de la classe cbasestreamcontrol](images/strmctl1.png)

<span data-ttu-id="897fe-105">Cette classe implémente l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) pour les broches d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="897fe-105">This class implements the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface for input and output pins.</span></span> <span data-ttu-id="897fe-106">Il permet de contrôler le démarrage et l’arrêt d’un code confidentiel individuel sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="897fe-106">It provides control over starting and stopping an individual pin on the filter.</span></span> <span data-ttu-id="897fe-107">Un code confidentiel qui prend en charge **IAMStreamControl** doit hériter de cette classe de base.</span><span class="sxs-lookup"><span data-stu-id="897fe-107">A pin that supports **IAMStreamControl** should inherit from this base class.</span></span> <span data-ttu-id="897fe-108">Voici une déclaration classique pour une broche d’entrée :</span><span class="sxs-lookup"><span data-stu-id="897fe-108">The following is a typical declaration for an input pin:</span></span>

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

<span data-ttu-id="897fe-109">Veillez à remplacer **NonDelegatingQueryInteface** pour exposer **IAMStreamControl**.</span><span class="sxs-lookup"><span data-stu-id="897fe-109">Be sure to override **NonDelegatingQueryInteface** to expose **IAMStreamControl**.</span></span> <span data-ttu-id="897fe-110">Pour plus d’informations, consultez [comment implémenter IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="897fe-110">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>



| <span data-ttu-id="897fe-111">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="897fe-111">Public Methods</span></span>                                                        | <span data-ttu-id="897fe-112">Description</span><span class="sxs-lookup"><span data-stu-id="897fe-112">Description</span></span>                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="897fe-113">**CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="897fe-113">**CBaseStreamControl**</span></span>](cbasestreamcontrol-cbasestreamcontrol.md)   | <span data-ttu-id="897fe-114">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="897fe-114">Constructor method.</span></span>                                                                                  |
| [<span data-ttu-id="897fe-115">**~ CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="897fe-115">**~CBaseStreamControl**</span></span>](cbasestreamcontrol--cbasestreamcontrol.md) | <span data-ttu-id="897fe-116">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="897fe-116">Destructor method.</span></span>                                                                                   |
| [<span data-ttu-id="897fe-117">**CheckStreamState**</span><span class="sxs-lookup"><span data-stu-id="897fe-117">**CheckStreamState**</span></span>](cbasestreamcontrol-checkstreamstate.md)       | <span data-ttu-id="897fe-118">Détermine si un échantillon de média doit être remis ou ignoré.</span><span class="sxs-lookup"><span data-stu-id="897fe-118">Determines whether a media sample should be delivered or discarded.</span></span>                                  |
| [<span data-ttu-id="897fe-119">**Vidage**</span><span class="sxs-lookup"><span data-stu-id="897fe-119">**Flushing**</span></span>](cbasestreamcontrol-flushing.md)                       | <span data-ttu-id="897fe-120">Notifie la classe de base que le code confidentiel a démarré ou a arrêté le vidage.</span><span class="sxs-lookup"><span data-stu-id="897fe-120">Notifies the base class that the pin has started or stopped flushing.</span></span>                                |
| [<span data-ttu-id="897fe-121">**NotifyFilterState**</span><span class="sxs-lookup"><span data-stu-id="897fe-121">**NotifyFilterState**</span></span>](cbasestreamcontrol-notifyfilterstate.md)     | <span data-ttu-id="897fe-122">Notifie le code confidentiel lorsque l’état du filtre change.</span><span class="sxs-lookup"><span data-stu-id="897fe-122">Notifies the pin when the filter's state changes.</span></span>                                                    |
| [<span data-ttu-id="897fe-123">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="897fe-123">**SetFilterGraph**</span></span>](cbasestreamcontrol-setfiltergraph.md)           | <span data-ttu-id="897fe-124">Spécifie le récepteur d’événements pour les événements de contrôle de flux.</span><span class="sxs-lookup"><span data-stu-id="897fe-124">Specifies the event sink for stream control events.</span></span>                                                  |
| [<span data-ttu-id="897fe-125">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="897fe-125">**SetSyncSource**</span></span>](cbasestreamcontrol-setsyncsource.md)             | <span data-ttu-id="897fe-126">Notifie la classe de base de l’horloge de référence actuelle.</span><span class="sxs-lookup"><span data-stu-id="897fe-126">Notifies the base class of the current reference clock.</span></span>                                              |
| <span data-ttu-id="897fe-127">Méthodes IAMStreamControl</span><span class="sxs-lookup"><span data-stu-id="897fe-127">IAMStreamControl Methods</span></span>                                              | <span data-ttu-id="897fe-128">Description</span><span class="sxs-lookup"><span data-stu-id="897fe-128">Description</span></span>                                                                                          |
| [<span data-ttu-id="897fe-129">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="897fe-129">**GetInfo**</span></span>](cbasestreamcontrol-getinfo.md)                         | <span data-ttu-id="897fe-130">Récupère des informations sur les paramètres de contrôle de flux actuels, y compris les heures de démarrage et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="897fe-130">Retrieves information about the current stream-control settings, including the start and stop times.</span></span> |
| [<span data-ttu-id="897fe-131">**Commencer**</span><span class="sxs-lookup"><span data-stu-id="897fe-131">**StartAt**</span></span>](cbasestreamcontrol-startat.md)                         | <span data-ttu-id="897fe-132">Informe le code confidentiel quand il faut commencer à transmettre des données.</span><span class="sxs-lookup"><span data-stu-id="897fe-132">Informs the pin when to start delivering data.</span></span>                                                       |
| [<span data-ttu-id="897fe-133">**StopAt**</span><span class="sxs-lookup"><span data-stu-id="897fe-133">**StopAt**</span></span>](cbasestreamcontrol-stopat.md)                           | <span data-ttu-id="897fe-134">Informe le code confidentiel quand il faut arrêter la transmission de données.</span><span class="sxs-lookup"><span data-stu-id="897fe-134">Informs the pin when to stop delivering data.</span></span>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="897fe-135">Notes</span><span class="sxs-lookup"><span data-stu-id="897fe-135">Remarks</span></span>

<span data-ttu-id="897fe-136">Cette classe requiert le code confidentiel et le filtre propriétaire pour notifier la classe lorsque divers événements se produisent, tels que le filtre qui rejoint le graphique ou la réception d’une nouvelle horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="897fe-136">This class requires the pin and the owning filter to notify the class when various events occur, such as the filter joining the graph or receiving a new reference clock.</span></span> <span data-ttu-id="897fe-137">Vous devez appeler les méthodes de classe suivantes :</span><span class="sxs-lookup"><span data-stu-id="897fe-137">You should call the following class methods:</span></span>

-   <span data-ttu-id="897fe-138">Dans la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) du filtre, appelez la méthode [**CBaseStreamControl :: SetSyncSource**](cbasestreamcontrol-setsyncsource.md) .</span><span class="sxs-lookup"><span data-stu-id="897fe-138">In the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method, call the [**CBaseStreamControl::SetSyncSource**](cbasestreamcontrol-setsyncsource.md) method.</span></span> <span data-ttu-id="897fe-139">Cette méthode notifie la classe de l’horloge de référence actuelle.</span><span class="sxs-lookup"><span data-stu-id="897fe-139">This method notifies the class of the current reference clock.</span></span>
-   <span data-ttu-id="897fe-140">Dans la méthode [**CBaseFilter :: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) du filtre, appelez la méthode [**CBaseStreamControl :: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="897fe-140">In the filter's [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, call the [**CBaseStreamControl::SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) method.</span></span> <span data-ttu-id="897fe-141">Cette méthode donne à la classe un pointeur vers le gestionnaire de graphes de filtres, afin que la classe puisse envoyer les événements de contrôle de flux appropriés.</span><span class="sxs-lookup"><span data-stu-id="897fe-141">This method gives the class a pointer to the Filter Graph Manager, so that the class can send the right stream-control events.</span></span>
-   <span data-ttu-id="897fe-142">Chaque fois que le filtre change d’État (en en cours d’exécution, suspendu ou arrêté), appelez la méthode [**CBaseStreamControl :: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="897fe-142">Whenever the filter changes state (to running, paused, or stopped), call the [**CBaseStreamControl::NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) method.</span></span>
-   <span data-ttu-id="897fe-143">Dans les méthodes [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) et [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) du pin, appelez la méthode [**CBaseStreamControl :: Flush**](cbasestreamcontrol-flushing.md) .</span><span class="sxs-lookup"><span data-stu-id="897fe-143">In the pin's [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods, call the [**CBaseStreamControl::Flushing**](cbasestreamcontrol-flushing.md) method.</span></span>

<span data-ttu-id="897fe-144">La `CBaseStreamControl` classe utilise l’horloge de référence du graphique de filtre pour déterminer les échantillons que le filtre doit remettre et celui qu’il doit ignorer.</span><span class="sxs-lookup"><span data-stu-id="897fe-144">The `CBaseStreamControl` class uses the filter graph's reference clock to determine which samples the filter should be deliver, and which it should discard.</span></span> <span data-ttu-id="897fe-145">Dans la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de votre pin, appelez la méthode [**CBaseStreamControl :: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) avec un pointeur vers l’exemple de média entrant.</span><span class="sxs-lookup"><span data-stu-id="897fe-145">In your pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, call the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method with a pointer to the incoming media sample.</span></span> <span data-ttu-id="897fe-146">Si la méthode retourne le flux de flux de valeur \_ , fournissez l’exemple en aval.</span><span class="sxs-lookup"><span data-stu-id="897fe-146">If the method returns the value STREAM\_FLOWING, deliver the sample downstream.</span></span> <span data-ttu-id="897fe-147">Sinon, ignorez-le.</span><span class="sxs-lookup"><span data-stu-id="897fe-147">Otherwise, discard it.</span></span>

## <a name="requirements"></a><span data-ttu-id="897fe-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="897fe-148">Requirements</span></span>



| <span data-ttu-id="897fe-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="897fe-149">Requirement</span></span> | <span data-ttu-id="897fe-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="897fe-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="897fe-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="897fe-151">Header</span></span><br/>  | <dl> <span data-ttu-id="897fe-152"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="897fe-152"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="897fe-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="897fe-153">Library</span></span><br/> | <dl> <span data-ttu-id="897fe-154"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="897fe-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




