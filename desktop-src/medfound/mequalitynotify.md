---
description: Fournit des commentaires à Quality Manager sur la qualité de la lecture.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Événement MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528270"
---
# <a name="mequalitynotify-event"></a><span data-ttu-id="50b13-103">Événement MEQualityNotify</span><span class="sxs-lookup"><span data-stu-id="50b13-103">MEQualityNotify event</span></span>

<span data-ttu-id="50b13-104">Fournit des commentaires à Quality Manager sur la qualité de la lecture.</span><span class="sxs-lookup"><span data-stu-id="50b13-104">Provides feedback to the quality manager about playback quality.</span></span>

## <a name="event-values"></a><span data-ttu-id="50b13-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="50b13-105">Event values</span></span>

<span data-ttu-id="50b13-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="50b13-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="50b13-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="50b13-107">VARTYPE</span></span>           | <span data-ttu-id="50b13-108">Description</span><span class="sxs-lookup"><span data-stu-id="50b13-108">Description</span></span>                         |
|-------------------|-------------------------------------|
| <span data-ttu-id="50b13-109">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="50b13-109">VT\_I8</span></span><br/> | <span data-ttu-id="50b13-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="50b13-110">See Remarks.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="50b13-111">Notes</span><span class="sxs-lookup"><span data-stu-id="50b13-111">Remarks</span></span>

<span data-ttu-id="50b13-112">Cet événement est déclenché par certains composants de pipeline.</span><span class="sxs-lookup"><span data-stu-id="50b13-112">This event is raised by some pipeline components.</span></span> <span data-ttu-id="50b13-113">La session multimédia transfère l’événement au gestionnaire de qualité en appelant la méthode [**IMFQualityManager :: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .</span><span class="sxs-lookup"><span data-stu-id="50b13-113">The Media Session forwards the event to the quality manager by calling the [**IMFQualityManager::NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) method.</span></span>

<span data-ttu-id="50b13-114">Le type étendu de l’événement indique la signification des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="50b13-114">The event's extended type indicates the meaning of the event data.</span></span>



| <span data-ttu-id="50b13-115">Type étendu</span><span class="sxs-lookup"><span data-stu-id="50b13-115">Extended type</span></span>                            | <span data-ttu-id="50b13-116">Données d’événement</span><span class="sxs-lookup"><span data-stu-id="50b13-116">Event data</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b13-117">\_latence du \_ traitement des notifications de qualité MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="50b13-117">MF\_QUALITY\_NOTIFY\_PROCESSING\_LATENCY</span></span> | <span data-ttu-id="50b13-118">Latence de traitement approximative introduite par le composant, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="50b13-118">Approximate processing latency introduced by the component, in 100-nanosecond units.</span></span><br/> <span data-ttu-id="50b13-119">La latence de traitement est la quantité de latence introduite par un composant dans le pipeline en traitant un exemple.</span><span class="sxs-lookup"><span data-stu-id="50b13-119">Processing latency is the amount of latency that a component introduces into the pipeline by processing a sample.</span></span> <span data-ttu-id="50b13-120">Dans certains cas, la latence ne peut pas être dérivée simplement en examinant les appels à [**IMFQualityManager :: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) et [**IMFQualityManager :: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span><span class="sxs-lookup"><span data-stu-id="50b13-120">In some cases, the latency cannot be derived simply by looking at the calls to [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) and [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span></span> <span data-ttu-id="50b13-121">Par exemple, il se peut qu’il n’y ait pas de correspondance un-à-un entre les exemples d’entrée et les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="50b13-121">For example, there may not be a one-to-one correspondence between input samples and output samples.</span></span> <span data-ttu-id="50b13-122">Dans ce cas, le composant peut envoyer un événement MEQualityNotify avec la latence de traitement.</span><span class="sxs-lookup"><span data-stu-id="50b13-122">In this case, the component might send an MEQualityNotify event with the processing latency.</span></span> <span data-ttu-id="50b13-123">Si la latence de traitement change, le composant peut envoyer un nouvel événement à tout moment pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="50b13-123">If the processing latency changes, the component can send a new event at any time during streaming.</span></span><br/> |
| <span data-ttu-id="50b13-124">retard de l’exemple de notification de \_ qualité MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="50b13-124">MF\_QUALITY\_NOTIFY\_SAMPLE\_LAG</span></span>         | <span data-ttu-id="50b13-125">Délai d’attente de l’échantillon, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="50b13-125">Lag time for the sample, in 100-nanosecond units.</span></span> <span data-ttu-id="50b13-126">Si la valeur est positive, l’échantillon était en retard.</span><span class="sxs-lookup"><span data-stu-id="50b13-126">If the value is positive, the sample was late.</span></span> <span data-ttu-id="50b13-127">Si la valeur est négative, l’échantillon était tôt.</span><span class="sxs-lookup"><span data-stu-id="50b13-127">If the value is negative, the sample was early.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="50b13-128">Pour récupérer le type étendu, appelez [**IMFMediaEvent :: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="50b13-128">To get the extended type, call [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

<span data-ttu-id="50b13-129">Les composants de pipeline ne sont pas requis pour envoyer cet événement.</span><span class="sxs-lookup"><span data-stu-id="50b13-129">Pipeline components are not required to send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b13-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50b13-130">Requirements</span></span>



| <span data-ttu-id="50b13-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50b13-131">Requirement</span></span> | <span data-ttu-id="50b13-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="50b13-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b13-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50b13-133">Minimum supported client</span></span><br/> | <span data-ttu-id="50b13-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50b13-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50b13-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50b13-135">Minimum supported server</span></span><br/> | <span data-ttu-id="50b13-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50b13-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50b13-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="50b13-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="50b13-138"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50b13-138"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b13-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b13-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b13-140">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="50b13-140">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[<span data-ttu-id="50b13-141">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50b13-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




