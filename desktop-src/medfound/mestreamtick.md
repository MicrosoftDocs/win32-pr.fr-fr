---
description: Signale qu’un flux multimédia n’a pas de données disponibles à une heure spécifiée.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Événement MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533751"
---
# <a name="mestreamtick-event"></a><span data-ttu-id="8ad09-103">Événement MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="8ad09-103">MEStreamTick event</span></span>

<span data-ttu-id="8ad09-104">Signale qu’un flux multimédia n’a pas de données disponibles à une heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ad09-104">Signals that a media stream does not have data available at a specified time.</span></span>

## <a name="event-values"></a><span data-ttu-id="8ad09-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="8ad09-105">Event values</span></span>

<span data-ttu-id="8ad09-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="8ad09-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8ad09-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8ad09-107">VARTYPE</span></span>           | <span data-ttu-id="8ad09-108">Description</span><span class="sxs-lookup"><span data-stu-id="8ad09-108">Description</span></span>                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8ad09-109">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="8ad09-109">VT\_I8</span></span><br/> | <span data-ttu-id="8ad09-110">Heure à laquelle l’intervalle se produit, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="8ad09-110">Time at which the gap occurs, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8ad09-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8ad09-111">Remarks</span></span>

<span data-ttu-id="8ad09-112">Cet événement signale un écart dans les données.</span><span class="sxs-lookup"><span data-stu-id="8ad09-112">This event signals a gap in the data.</span></span> <span data-ttu-id="8ad09-113">L’événement avertit les composants en aval qu’ils n’attendent aucune donnée à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ad09-113">The event notifies downstream components not to expect any data at the specified time.</span></span>

<span data-ttu-id="8ad09-114">L’événement doit être envoyé par l’objet qui génère les horodatages pour les échantillons de média dans le flux.</span><span class="sxs-lookup"><span data-stu-id="8ad09-114">The event should be sent by whichever object generates the time stamps for the media samples in the stream.</span></span> <span data-ttu-id="8ad09-115">Selon le format des données, il peut s’agir de l’une des deux opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ad09-115">Depending on the format of the data, this is either:</span></span>

-   <span data-ttu-id="8ad09-116">Le flux multimédia sur la source du média (interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ), ou</span><span class="sxs-lookup"><span data-stu-id="8ad09-116">The media stream on the media source ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface), or</span></span>
-   <span data-ttu-id="8ad09-117">Transformation de décodeur (interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).</span><span class="sxs-lookup"><span data-stu-id="8ad09-117">The decoder transform ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface).</span></span>

<span data-ttu-id="8ad09-118">Pendant ce laps de temps, l’objet doit envoyer l’événement sur aussi souvent qu’il produirait normalement des exemples.</span><span class="sxs-lookup"><span data-stu-id="8ad09-118">During the gap, the object should send the event about as often as it would normally produce samples.</span></span> <span data-ttu-id="8ad09-119">Pour la vidéo, envoyer un événement pour chaque frame manquant.</span><span class="sxs-lookup"><span data-stu-id="8ad09-119">For video, send one event for each missing frame.</span></span> <span data-ttu-id="8ad09-120">Pour l’audio, envoyez l’événement au moins une fois par seconde pendant l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="8ad09-120">For audio, send the event at least once per second during the gap.</span></span> <span data-ttu-id="8ad09-121">La valeur de l’événement est l’horodatage de l’échantillon manquant.</span><span class="sxs-lookup"><span data-stu-id="8ad09-121">The value of the event is the time stamp of the missing sample.</span></span> <span data-ttu-id="8ad09-122">Envoyez autant d’événements MEStreamTick que nécessaire pour combler l’écart dans les données.</span><span class="sxs-lookup"><span data-stu-id="8ad09-122">Send as many MEStreamTick events as needed to fill the gap in the data.</span></span>

<span data-ttu-id="8ad09-123">Si une source de média a plusieurs flux et qu’il y a un écart dans plusieurs flux, chaque flux doit envoyer des événements MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="8ad09-123">If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events.</span></span> <span data-ttu-id="8ad09-124">Par exemple, s’il existe un écart dans les données audio et vidéo, les deux flux envoient l’événement.</span><span class="sxs-lookup"><span data-stu-id="8ad09-124">For example, if there is a gap in both audio and video data, then both streams send the event.</span></span>

<span data-ttu-id="8ad09-125">L’événement MEStreamTick ne termine pas une demande [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="8ad09-125">The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) request.</span></span> <span data-ttu-id="8ad09-126">La source du média doit toujours envoyer un événement [MEMediaSample](memediasample.md) pour chaque appel à **RequestSample**.</span><span class="sxs-lookup"><span data-stu-id="8ad09-126">The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.</span></span>

<span data-ttu-id="8ad09-127">Les récepteurs multimédias ne peuvent pas utiliser cet événement directement.</span><span class="sxs-lookup"><span data-stu-id="8ad09-127">Media sinks cannot consume this event directly.</span></span> <span data-ttu-id="8ad09-128">Pour signaler un intervalle dans le flux à un récepteur multimédia, appelez [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) avec un marqueur de **\_ \_ graduation de marqueur MFSTREAMSINK** .</span><span class="sxs-lookup"><span data-stu-id="8ad09-128">To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) with an **MFSTREAMSINK\_MARKER\_TICK** marker.</span></span> <span data-ttu-id="8ad09-129">Le pipeline Media Foundation convertit les événements MEStreamTick en marqueurs de **\_ \_ graduation MFSTREAMSINK** , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8ad09-129">The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.</span></span>

<span data-ttu-id="8ad09-130">Ne définissez pas l’attribut de [**\_ discontinuité MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sur l’exemple de support suivant après un événement MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="8ad09-130">Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event.</span></span> <span data-ttu-id="8ad09-131">L’attribut de **\_ discontinuité MFSampleExtension** implique que l’horodatage est discontinu avec les horodatages précédents, tandis que MEStreamTick implique que les horodatages sont continus, mais que certaines données sont manquantes.</span><span class="sxs-lookup"><span data-stu-id="8ad09-131">The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.</span></span>

> [!Note]  
> <span data-ttu-id="8ad09-132">Une version antérieure de la documentation indiquait de façon erronée que l’exemple après un événement MEStreamTick doit avoir l’attribut [**\_ discontinu MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad09-132">An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ad09-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ad09-133">Requirements</span></span>



| <span data-ttu-id="8ad09-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ad09-134">Requirement</span></span> | <span data-ttu-id="8ad09-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ad09-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad09-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ad09-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8ad09-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ad09-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ad09-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ad09-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8ad09-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ad09-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ad09-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ad09-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ad09-141"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ad09-141"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ad09-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ad09-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad09-143">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ad09-143">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




