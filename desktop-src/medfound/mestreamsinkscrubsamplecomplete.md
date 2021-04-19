---
description: Déclenché par un récepteur de flux lorsqu’il termine une demande de nettoyage.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Événement MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520754"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a><span data-ttu-id="4be02-103">Événement MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="4be02-103">MEStreamSinkScrubSampleComplete event</span></span>

<span data-ttu-id="4be02-104">Déclenché par un récepteur de flux lorsqu’il termine une demande de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="4be02-104">Raised by a stream sink when it completes a scrubbing request.</span></span>

<span data-ttu-id="4be02-105">Le nettoyage se produit lorsque la vitesse de lecture est égale à zéro et que l’horloge de la présentation est démarrée avec une heure de srubbing spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4be02-105">Scrubbing occurs when the playback rate is zero and the presentation clock is started with a specified srubbing time.</span></span> <span data-ttu-id="4be02-106">Si un récepteur multimédia prend en charge le nettoyage, chaque flux du récepteur déclenche cet événement chaque fois que la méthode [**IMFClockStateSink :: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) est appelée alors que la vitesse de lecture est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4be02-106">If a media sink supports scrubbing, every stream on the sink raises this event whenever the [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) method is called while the playback rate is zero.</span></span>

<span data-ttu-id="4be02-107">Si le flux restitue des données lors du nettoyage, il envoie l’événement dès que les données sont restituées.</span><span class="sxs-lookup"><span data-stu-id="4be02-107">If the stream renders data while scrubbing, it sends the event as soon as the data is rendered.</span></span> <span data-ttu-id="4be02-108">Si le flux ne rend pas les données, il envoie l’événement immédiatement après l’appel de [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .</span><span class="sxs-lookup"><span data-stu-id="4be02-108">If the stream does not render data, it sends the event immediately after [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="4be02-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="4be02-109">Event values</span></span>

<span data-ttu-id="4be02-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="4be02-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4be02-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4be02-111">VARTYPE</span></span>              | <span data-ttu-id="4be02-112">Description</span><span class="sxs-lookup"><span data-stu-id="4be02-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4be02-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="4be02-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4be02-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="4be02-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="4be02-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="4be02-115">Attributes</span></span>

<span data-ttu-id="4be02-116">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="4be02-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="4be02-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="4be02-117">Attribute</span></span>                                                                              | <span data-ttu-id="4be02-118">Description</span><span class="sxs-lookup"><span data-stu-id="4be02-118">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4be02-119">**\_ \_ heure SCRUBSAMPLE de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="4be02-119">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)<br/> | <span data-ttu-id="4be02-120">Heure de présentation pour laquelle les données ont été rendues.</span><span class="sxs-lookup"><span data-stu-id="4be02-120">Presentation time for which data was rendered.</span></span> <span data-ttu-id="4be02-121">Si le récepteur multimédia ne rend pas les données lors du nettoyage, il ne définit pas cet attribut.</span><span class="sxs-lookup"><span data-stu-id="4be02-121">If the media sink does not render data while scrubbing, it does not set this attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="4be02-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4be02-122">Requirements</span></span>



| <span data-ttu-id="4be02-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4be02-123">Requirement</span></span> | <span data-ttu-id="4be02-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4be02-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be02-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4be02-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4be02-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4be02-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4be02-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4be02-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4be02-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4be02-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4be02-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4be02-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be02-130"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4be02-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be02-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4be02-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be02-132">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4be02-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4be02-133">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="4be02-133">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="4be02-134">MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="4be02-134">MESessionScrubSampleComplete</span></span>](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




