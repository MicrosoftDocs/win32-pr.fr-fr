---
description: La classe CBaseOutputPin est une classe de base abstraite qui implémente une broche de sortie.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: CBaseOutputPin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541643"
---
# <a name="cbaseoutputpin-class"></a><span data-ttu-id="99e7c-103">CBaseOutputPin, classe</span><span class="sxs-lookup"><span data-stu-id="99e7c-103">CBaseOutputPin class</span></span>

![hiérarchie de la classe cbaseoutputpin](images/filter06.png)

<span data-ttu-id="99e7c-105">La `CBaseOutputPin` classe est une classe de base abstraite qui implémente une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="99e7c-105">The `CBaseOutputPin` class is an abstract base class that implements an output pin.</span></span>

<span data-ttu-id="99e7c-106">Cette classe dérive de [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="99e7c-106">This class derives from [**CBasePin**](cbasepin.md).</span></span> <span data-ttu-id="99e7c-107">Il diffère de **CBasePin** en respectant les points suivants :</span><span class="sxs-lookup"><span data-stu-id="99e7c-107">It differs from **CBasePin** in the following respects:</span></span>

-   <span data-ttu-id="99e7c-108">Il se connecte uniquement aux broches d’entrée qui prennent en charge l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="99e7c-108">It connects only to input pins that support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="99e7c-109">Il prend en charge le transport de mémoire locale par le biais de l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="99e7c-109">It supports local memory transport through the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>
-   <span data-ttu-id="99e7c-110">Elle rejette les notifications de fin de flux, de vidage et de segmentation.</span><span class="sxs-lookup"><span data-stu-id="99e7c-110">It rejects end-of-stream, flush, and new-segment notifications.</span></span> <span data-ttu-id="99e7c-111">(Ils ne doivent pas être envoyés à une broche de sortie.)</span><span class="sxs-lookup"><span data-stu-id="99e7c-111">(These should not be sent to an output pin.)</span></span>
-   <span data-ttu-id="99e7c-112">Il fournit des méthodes pour fournir des exemples en aval.</span><span class="sxs-lookup"><span data-stu-id="99e7c-112">It provides methods for delivering samples downstream.</span></span>

<span data-ttu-id="99e7c-113">Lorsque le code confidentiel se connecte, il demande un allocateur de mémoire à partir de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="99e7c-113">When the pin connects, it requests a memory allocator from the input pin.</span></span> <span data-ttu-id="99e7c-114">En échec, elle crée un nouvel objet allocateur.</span><span class="sxs-lookup"><span data-stu-id="99e7c-114">Failing that, it creates a new allocator object.</span></span> <span data-ttu-id="99e7c-115">La broche de sortie est chargée de définir les propriétés de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="99e7c-115">The output pin is responsible for setting the allocator properties.</span></span> <span data-ttu-id="99e7c-116">Pour ce faire, il utilise la méthode virtuelle pure [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="99e7c-116">It does this through the pure virtual method [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span> <span data-ttu-id="99e7c-117">Substituez cette méthode dans votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="99e7c-117">Override this method in your derived class.</span></span> <span data-ttu-id="99e7c-118">Si la broche d’entrée a des exigences de mémoire tampon, elles sont passées à la méthode **DecideBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="99e7c-118">If the input pin has any buffer requirements, they are passed to the **DecideBufferSize** method.</span></span>

<span data-ttu-id="99e7c-119">Appelez la méthode [**CBaseOutputPin :: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) pour obtenir un exemple de support vide.</span><span class="sxs-lookup"><span data-stu-id="99e7c-119">Call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain an empty media sample.</span></span> <span data-ttu-id="99e7c-120">Appelez la méthode [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md) pour remettre des exemples en aval.</span><span class="sxs-lookup"><span data-stu-id="99e7c-120">Call the [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) method to deliver samples downstream.</span></span>

<span data-ttu-id="99e7c-121">Votre classe dérivée doit substituer la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure pour valider le type de média lors des connexions de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="99e7c-121">Your derived class must override the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to validate the media type during pin connections.</span></span>



| <span data-ttu-id="99e7c-122">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="99e7c-122">Protected Member Variables</span></span>                                      | <span data-ttu-id="99e7c-123">Description</span><span class="sxs-lookup"><span data-stu-id="99e7c-123">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="99e7c-124">**m \_ pAllocator**</span><span class="sxs-lookup"><span data-stu-id="99e7c-124">**m\_pAllocator**</span></span>](cbaseoutputpin-m-pallocator.md)            | <span data-ttu-id="99e7c-125">Pointeur vers l’allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="99e7c-125">Pointer to the memory allocator.</span></span>                                           |
| [<span data-ttu-id="99e7c-126">**m \_ pInputPin**</span><span class="sxs-lookup"><span data-stu-id="99e7c-126">**m\_pInputPin**</span></span>](cbaseoutputpin-m-pinputpin.md)              | <span data-ttu-id="99e7c-127">Pointeur vers la broche d’entrée connectée à ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="99e7c-127">Pointer to the input pin connected to this pin.</span></span>                            |
| <span data-ttu-id="99e7c-128">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="99e7c-128">Public Methods</span></span>                                                  | <span data-ttu-id="99e7c-129">Description</span><span class="sxs-lookup"><span data-stu-id="99e7c-129">Description</span></span>                                                                |
| [<span data-ttu-id="99e7c-130">**CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="99e7c-130">**CBaseOutputPin**</span></span>](cbaseoutputpin-cbaseoutputpin.md)         | <span data-ttu-id="99e7c-131">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="99e7c-131">Constructor method.</span></span>                                                        |
| [<span data-ttu-id="99e7c-132">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="99e7c-132">**CompleteConnect**</span></span>](cbaseoutputpin-completeconnect.md)       | <span data-ttu-id="99e7c-133">Termine une connexion à une broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="99e7c-133">Completes a connection to an input pin.</span></span> <span data-ttu-id="99e7c-134">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-134">Virtual.</span></span>                           |
| [<span data-ttu-id="99e7c-135">**DecideAllocator**</span><span class="sxs-lookup"><span data-stu-id="99e7c-135">**DecideAllocator**</span></span>](cbaseoutputpin-decideallocator.md)       | <span data-ttu-id="99e7c-136">Sélectionne un allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="99e7c-136">Selects a memory allocator.</span></span> <span data-ttu-id="99e7c-137">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-137">Virtual.</span></span>                                       |
| [<span data-ttu-id="99e7c-138">**GetDeliveryBuffer**</span><span class="sxs-lookup"><span data-stu-id="99e7c-138">**GetDeliveryBuffer**</span></span>](cbaseoutputpin-getdeliverybuffer.md)   | <span data-ttu-id="99e7c-139">Récupère un exemple de média qui contient une mémoire tampon vide.</span><span class="sxs-lookup"><span data-stu-id="99e7c-139">Retrieves a media sample that contains an empty buffer.</span></span> <span data-ttu-id="99e7c-140">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-140">Virtual.</span></span>           |
| [<span data-ttu-id="99e7c-141">**Remettre**</span><span class="sxs-lookup"><span data-stu-id="99e7c-141">**Deliver**</span></span>](cbaseoutputpin-deliver.md)                       | <span data-ttu-id="99e7c-142">Remet un échantillon de média à la broche d’entrée connectée.</span><span class="sxs-lookup"><span data-stu-id="99e7c-142">Delivers a media sample to the connected input pin.</span></span> <span data-ttu-id="99e7c-143">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-143">Virtual.</span></span>               |
| [<span data-ttu-id="99e7c-144">**InitAllocator**</span><span class="sxs-lookup"><span data-stu-id="99e7c-144">**InitAllocator**</span></span>](cbaseoutputpin-initallocator.md)           | <span data-ttu-id="99e7c-145">Crée un allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="99e7c-145">Creates a memory allocator.</span></span> <span data-ttu-id="99e7c-146">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-146">Virtual.</span></span>                                       |
| [<span data-ttu-id="99e7c-147">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="99e7c-147">**CheckConnect**</span></span>](cbaseoutputpin-checkconnect.md)             | <span data-ttu-id="99e7c-148">Détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="99e7c-148">Determines whether a pin connection is suitable.</span></span>                           |
| [<span data-ttu-id="99e7c-149">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="99e7c-149">**BreakConnect**</span></span>](cbaseoutputpin-breakconnect.md)             | <span data-ttu-id="99e7c-150">Libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="99e7c-150">Releases the pin from a connection.</span></span>                                        |
| [<span data-ttu-id="99e7c-151">**Proactive**</span><span class="sxs-lookup"><span data-stu-id="99e7c-151">**Active**</span></span>](cbaseoutputpin-active.md)                         | <span data-ttu-id="99e7c-152">Notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="99e7c-152">Notifies the pin that the filter is now active.</span></span>                            |
| [<span data-ttu-id="99e7c-153">**Inactif**</span><span class="sxs-lookup"><span data-stu-id="99e7c-153">**Inactive**</span></span>](cbaseoutputpin-inactive.md)                     | <span data-ttu-id="99e7c-154">Notifie le code confidentiel que le filtre n’est plus actif.</span><span class="sxs-lookup"><span data-stu-id="99e7c-154">Notifies the pin that the filter is no longer active.</span></span>                      |
| [<span data-ttu-id="99e7c-155">**DeliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="99e7c-155">**DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md) | <span data-ttu-id="99e7c-156">Fournit une notification de fin de flux à la broche d’entrée connectée. Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-156">Delivers an end-of-stream notification to the connected input pin.Virtual.</span></span> |
| [<span data-ttu-id="99e7c-157">**DeliverBeginFlush**</span><span class="sxs-lookup"><span data-stu-id="99e7c-157">**DeliverBeginFlush**</span></span>](cbaseoutputpin-deliverbeginflush.md)   | <span data-ttu-id="99e7c-158">Demande la broche d’entrée connectée pour commencer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="99e7c-158">Requests the connected input pin to begin a flush operation.</span></span> <span data-ttu-id="99e7c-159">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-159">Virtual.</span></span>      |
| [<span data-ttu-id="99e7c-160">**DeliverEndFlush**</span><span class="sxs-lookup"><span data-stu-id="99e7c-160">**DeliverEndFlush**</span></span>](cbaseoutputpin-deliverendflush.md)       | <span data-ttu-id="99e7c-161">Demande la broche d’entrée connectée pour terminer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="99e7c-161">Requests the connected input pin to end a flush operation.</span></span> <span data-ttu-id="99e7c-162">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-162">Virtual.</span></span>        |
| [<span data-ttu-id="99e7c-163">**DeliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="99e7c-163">**DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)   | <span data-ttu-id="99e7c-164">Remet une notification de nouveau segment à la broche d’entrée connectée.</span><span class="sxs-lookup"><span data-stu-id="99e7c-164">Delivers a new-segment notification to the connected input pin.</span></span> <span data-ttu-id="99e7c-165">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="99e7c-165">Virtual.</span></span>   |
| <span data-ttu-id="99e7c-166">Méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="99e7c-166">Pure Virtual Methods</span></span>                                            | <span data-ttu-id="99e7c-167">Description</span><span class="sxs-lookup"><span data-stu-id="99e7c-167">Description</span></span>                                                                |
| [<span data-ttu-id="99e7c-168">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="99e7c-168">**DecideBufferSize**</span></span>](cbaseoutputpin-decidebuffersize.md)     | <span data-ttu-id="99e7c-169">Définit les exigences de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="99e7c-169">Sets the buffer requirements.</span></span>                                              |
| <span data-ttu-id="99e7c-170">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="99e7c-170">IPin Methods</span></span>                                                    | <span data-ttu-id="99e7c-171">Description</span><span class="sxs-lookup"><span data-stu-id="99e7c-171">Description</span></span>                                                                |
| [<span data-ttu-id="99e7c-172">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="99e7c-172">**BeginFlush**</span></span>](cbaseoutputpin-beginflush.md)                 | <span data-ttu-id="99e7c-173">Commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="99e7c-173">Begins a flush operation.</span></span>                                                  |
| [<span data-ttu-id="99e7c-174">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="99e7c-174">**EndFlush**</span></span>](cbaseoutputpin-endflush.md)                     | <span data-ttu-id="99e7c-175">Termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="99e7c-175">Ends a flush operation.</span></span>                                                    |
| [<span data-ttu-id="99e7c-176">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="99e7c-176">**EndOfStream**</span></span>](cbaseoutputpin-endofstream.md)               | <span data-ttu-id="99e7c-177">Notifie le code confidentiel qu’aucune donnée supplémentaire n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="99e7c-177">Notifies the pin that no additional data is expected.</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="99e7c-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99e7c-178">Requirements</span></span>



| <span data-ttu-id="99e7c-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99e7c-179">Requirement</span></span> | <span data-ttu-id="99e7c-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="99e7c-180">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e7c-181">En-tête</span><span class="sxs-lookup"><span data-stu-id="99e7c-181">Header</span></span><br/>  | <dl> <span data-ttu-id="99e7c-182"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99e7c-182"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99e7c-183">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99e7c-183">Library</span></span><br/> | <dl> <span data-ttu-id="99e7c-184"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99e7c-184"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




