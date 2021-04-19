---
description: La classe CBaseInputPin est une classe de base abstraite pour l’implémentation des codes confidentiels d’entrée. Cette classe ajoute la prise en charge de l’interface IMemInputPin, en plus de la prise en charge de l’interface IPin fournie par CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: CBaseInputPin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544095"
---
# <a name="cbaseinputpin-class"></a><span data-ttu-id="930c7-104">CBaseInputPin, classe</span><span class="sxs-lookup"><span data-stu-id="930c7-104">CBaseInputPin class</span></span>

![hiérarchie de la classe cbaseinputpin](images/filter07.png)

<span data-ttu-id="930c7-106">La `CBaseInputPin` classe est une classe de base abstraite pour l’implémentation des codes confidentiels d’entrée.</span><span class="sxs-lookup"><span data-stu-id="930c7-106">The `CBaseInputPin` class is an abstract base class for implementing input pins.</span></span> <span data-ttu-id="930c7-107">Cette classe ajoute la prise en charge de l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , en plus de la prise en charge de l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) fournie par [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="930c7-107">This class adds support for the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, in addition to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface support provided by [**CBasePin**](cbasepin.md).</span></span>

<span data-ttu-id="930c7-108">Pour utiliser cette classe, dérivez une nouvelle classe et substituez au moins les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="930c7-108">To use this class, derive a new class and override at least the following methods:</span></span>

-   [<span data-ttu-id="930c7-109">**CBaseInputPin::BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="930c7-109">**CBaseInputPin::BeginFlush**</span></span>](cbaseinputpin-beginflush.md)
-   [<span data-ttu-id="930c7-110">**CBaseInputPin::EndFlush**</span><span class="sxs-lookup"><span data-stu-id="930c7-110">**CBaseInputPin::EndFlush**</span></span>](cbaseinputpin-endflush.md)
-   [<span data-ttu-id="930c7-111">**CBaseInputPin :: Receive**</span><span class="sxs-lookup"><span data-stu-id="930c7-111">**CBaseInputPin::Receive**</span></span>](cbaseinputpin-receive.md)
-   [<span data-ttu-id="930c7-112">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="930c7-112">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="930c7-113">**CBasePin::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="930c7-113">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="930c7-114">Selon la fonction du code PIN, vous devrez peut-être remplacer des méthodes supplémentaires dans `CBaseInputPin` ou **CBasePin**.</span><span class="sxs-lookup"><span data-stu-id="930c7-114">Depending on the function of the pin, you might need to override additional methods in `CBaseInputPin` or **CBasePin**.</span></span>



| <span data-ttu-id="930c7-115">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="930c7-115">Protected Member Variables</span></span>                                                 | <span data-ttu-id="930c7-116">Description</span><span class="sxs-lookup"><span data-stu-id="930c7-116">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="930c7-117">**m \_ pAllocator**</span><span class="sxs-lookup"><span data-stu-id="930c7-117">**m\_pAllocator**</span></span>](cbaseinputpin-m-pallocator.md)                        | <span data-ttu-id="930c7-118">Pointeur vers l’allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="930c7-118">Pointer to the memory allocator.</span></span>                                                                            |
| [<span data-ttu-id="930c7-119">**m \_ bReadOnly**</span><span class="sxs-lookup"><span data-stu-id="930c7-119">**m\_bReadOnly**</span></span>](cbaseinputpin-m-breadonly.md)                          | <span data-ttu-id="930c7-120">Indicateur qui spécifie si l’allocateur produit des exemples de supports en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="930c7-120">Flag that indicates whether the allocator produces read-only media samples.</span></span>                                 |
| [<span data-ttu-id="930c7-121">**m \_ bFlushing**</span><span class="sxs-lookup"><span data-stu-id="930c7-121">**m\_bFlushing**</span></span>](cbaseinputpin-m-bflushing.md)                          | <span data-ttu-id="930c7-122">Indicateur qui spécifie si le pin est actuellement en cours de vidage.</span><span class="sxs-lookup"><span data-stu-id="930c7-122">Flag that indicates whether the pin is currently flushing.</span></span>                                                  |
| [<span data-ttu-id="930c7-123">**m \_ SampleProps**</span><span class="sxs-lookup"><span data-stu-id="930c7-123">**m\_SampleProps**</span></span>](cbaseinputpin-m-sampleprops.md)                      | <span data-ttu-id="930c7-124">Propriétés de l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="930c7-124">Properties of the most recent sample.</span></span>                                                                       |
| <span data-ttu-id="930c7-125">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="930c7-125">Public Methods</span></span>                                                             | <span data-ttu-id="930c7-126">Description</span><span class="sxs-lookup"><span data-stu-id="930c7-126">Description</span></span>                                                                                                 |
| [<span data-ttu-id="930c7-127">**CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="930c7-127">**CBaseInputPin**</span></span>](cbaseinputpin-cbaseinputpin.md)                       | <span data-ttu-id="930c7-128">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="930c7-128">Constructor method.</span></span>                                                                                         |
| [<span data-ttu-id="930c7-129">**~ CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="930c7-129">**~CBaseInputPin**</span></span>](cbaseinputpin--cbaseinputpin.md)                     | <span data-ttu-id="930c7-130">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="930c7-130">Destructor method.</span></span>                                                                                          |
| [<span data-ttu-id="930c7-131">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="930c7-131">**BreakConnect**</span></span>](cbaseinputpin-breakconnect.md)                         | <span data-ttu-id="930c7-132">Libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="930c7-132">Releases the pin from a connection.</span></span>                                                                         |
| [<span data-ttu-id="930c7-133">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="930c7-133">**IsReadOnly**</span></span>](cbaseinputpin-isreadonly.md)                             | <span data-ttu-id="930c7-134">Interroge si l’allocateur utilise des exemples de supports en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="930c7-134">Queries whether the allocator uses read-only media samples.</span></span>                                                 |
| [<span data-ttu-id="930c7-135">**IsFlushing**</span><span class="sxs-lookup"><span data-stu-id="930c7-135">**IsFlushing**</span></span>](cbaseinputpin-isflushing.md)                             | <span data-ttu-id="930c7-136">Interroge si le filtre est en cours de vidage.</span><span class="sxs-lookup"><span data-stu-id="930c7-136">Queries whether the filter is currently flushing.</span></span>                                                           |
| [<span data-ttu-id="930c7-137">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="930c7-137">**CheckStreaming**</span></span>](cbaseinputpin-checkstreaming.md)                     | <span data-ttu-id="930c7-138">Détermine si le code confidentiel peut accepter des exemples.</span><span class="sxs-lookup"><span data-stu-id="930c7-138">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="930c7-139">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="930c7-139">Virtual.</span></span>                                                     |
| [<span data-ttu-id="930c7-140">**PassNotify**</span><span class="sxs-lookup"><span data-stu-id="930c7-140">**PassNotify**</span></span>](cbaseinputpin-passnotify.md)                             | <span data-ttu-id="930c7-141">Transmet un message de contrôle qualité à l’objet approprié.</span><span class="sxs-lookup"><span data-stu-id="930c7-141">Passes a quality-control message to the appropriate object.</span></span>                                                 |
| [<span data-ttu-id="930c7-142">**Inactif**</span><span class="sxs-lookup"><span data-stu-id="930c7-142">**Inactive**</span></span>](cbaseinputpin-inactive.md)                                 | <span data-ttu-id="930c7-143">Notifie le code confidentiel que le filtre n’est plus actif.</span><span class="sxs-lookup"><span data-stu-id="930c7-143">Notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="930c7-144">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="930c7-144">Virtual.</span></span>                                              |
| [<span data-ttu-id="930c7-145">**SampleProps**</span><span class="sxs-lookup"><span data-stu-id="930c7-145">**SampleProps**</span></span>](cbaseinputpin-sampleprops.md)                           | <span data-ttu-id="930c7-146">Récupère les propriétés de l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="930c7-146">Retrieves the properties of the most recent sample.</span></span>                                                         |
| <span data-ttu-id="930c7-147">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="930c7-147">IPin Methods</span></span>                                                               | <span data-ttu-id="930c7-148">Description</span><span class="sxs-lookup"><span data-stu-id="930c7-148">Description</span></span>                                                                                                 |
| [<span data-ttu-id="930c7-149">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="930c7-149">**BeginFlush**</span></span>](cbaseinputpin-beginflush.md)                             | <span data-ttu-id="930c7-150">Commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="930c7-150">Begins a flush operation.</span></span>                                                                                   |
| [<span data-ttu-id="930c7-151">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="930c7-151">**EndFlush**</span></span>](cbaseinputpin-endflush.md)                                 | <span data-ttu-id="930c7-152">Termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="930c7-152">Ends a flush operation.</span></span>                                                                                     |
| <span data-ttu-id="930c7-153">Méthodes IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="930c7-153">IMemInputPin Methods</span></span>                                                       | <span data-ttu-id="930c7-154">Description</span><span class="sxs-lookup"><span data-stu-id="930c7-154">Description</span></span>                                                                                                 |
| [<span data-ttu-id="930c7-155">**GetAllocator**</span><span class="sxs-lookup"><span data-stu-id="930c7-155">**GetAllocator**</span></span>](cbaseinputpin-getallocator.md)                         | <span data-ttu-id="930c7-156">Récupère l’allocateur de mémoire proposé par ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="930c7-156">Retrieves the memory allocator proposed by this pin.</span></span>                                                        |
| [<span data-ttu-id="930c7-157">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="930c7-157">**NotifyAllocator**</span></span>](cbaseinputpin-notifyallocator.md)                   | <span data-ttu-id="930c7-158">Spécifie un allocateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="930c7-158">Specifies an allocator for the connection.</span></span>                                                                  |
| [<span data-ttu-id="930c7-159">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="930c7-159">**GetAllocatorRequirements**</span></span>](cbaseinputpin-getallocatorrequirements.md) | <span data-ttu-id="930c7-160">Récupère les propriétés d’allocateur demandées par la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="930c7-160">Retrieves the allocator properties requested by the input pin.</span></span>                                              |
| [<span data-ttu-id="930c7-161">**Çoive**</span><span class="sxs-lookup"><span data-stu-id="930c7-161">**Receive**</span></span>](cbaseinputpin-receive.md)                                   | <span data-ttu-id="930c7-162">Reçoit l’échantillon de média suivant dans le flux.</span><span class="sxs-lookup"><span data-stu-id="930c7-162">Receives the next media sample in the stream.</span></span>                                                               |
| [<span data-ttu-id="930c7-163">**ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="930c7-163">**ReceiveMultiple**</span></span>](cbaseinputpin-receivemultiple.md)                   | <span data-ttu-id="930c7-164">Reçoit plusieurs exemples dans le flux.</span><span class="sxs-lookup"><span data-stu-id="930c7-164">Receives multiple samples in the stream.</span></span>                                                                    |
| [<span data-ttu-id="930c7-165">**ReceiveCanBlock**</span><span class="sxs-lookup"><span data-stu-id="930c7-165">**ReceiveCanBlock**</span></span>](cbaseinputpin-receivecanblock.md)                   | <span data-ttu-id="930c7-166">Détermine si les appels à la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) peuvent se bloquer.</span><span class="sxs-lookup"><span data-stu-id="930c7-166">Determines whether calls to the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method might block.</span></span> |
| <span data-ttu-id="930c7-167">Méthodes IQualityControl</span><span class="sxs-lookup"><span data-stu-id="930c7-167">IQualityControl Methods</span></span>                                                    | <span data-ttu-id="930c7-168">Description</span><span class="sxs-lookup"><span data-stu-id="930c7-168">Description</span></span>                                                                                                 |
| [<span data-ttu-id="930c7-169">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="930c7-169">**Notify**</span></span>](cbaseinputpin-notify.md)                                     | <span data-ttu-id="930c7-170">Reçoit un message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="930c7-170">Receives a quality-control message.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="930c7-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="930c7-171">Requirements</span></span>



| <span data-ttu-id="930c7-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="930c7-172">Requirement</span></span> | <span data-ttu-id="930c7-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="930c7-173">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930c7-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="930c7-174">Header</span></span><br/>  | <dl> <span data-ttu-id="930c7-175"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="930c7-175"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="930c7-176">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="930c7-176">Library</span></span><br/> | <dl> <span data-ttu-id="930c7-177"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="930c7-177"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




