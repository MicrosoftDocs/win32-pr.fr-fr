---
description: Déclenché par la session multimédia au démarrage d’une nouvelle présentation. Cet événement indique la date de début de la présentation et le décalage entre l’heure de la présentation et l’heure de la source.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Événement MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527379"
---
# <a name="mesessionnotifypresentationtime-event"></a><span data-ttu-id="7935a-104">Événement MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="7935a-104">MESessionNotifyPresentationTime event</span></span>

<span data-ttu-id="7935a-105">Déclenché par la session multimédia au démarrage d’une nouvelle présentation.</span><span class="sxs-lookup"><span data-stu-id="7935a-105">Raised by the Media Session when a new presentation starts.</span></span> <span data-ttu-id="7935a-106">Cet événement indique la date de début de la présentation et le décalage entre l’heure de la présentation et l’heure de la source.</span><span class="sxs-lookup"><span data-stu-id="7935a-106">This event indicates when the presentation will start and the offset between the presentation time and the source time.</span></span>

## <a name="event-values"></a><span data-ttu-id="7935a-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="7935a-107">Event values</span></span>

<span data-ttu-id="7935a-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7935a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7935a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7935a-109">VARTYPE</span></span>              | <span data-ttu-id="7935a-110">Description</span><span class="sxs-lookup"><span data-stu-id="7935a-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7935a-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="7935a-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7935a-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="7935a-112">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="7935a-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="7935a-113">Attributes</span></span>

<span data-ttu-id="7935a-114">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="7935a-114">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="7935a-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="7935a-115">Attribute</span></span>                                                                                                                   | <span data-ttu-id="7935a-116">Description</span><span class="sxs-lookup"><span data-stu-id="7935a-116">Description</span></span>                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7935a-117">**heure de la présentation du démarrage de l' \_ événement MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7935a-117">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)<br/>                       | <span data-ttu-id="7935a-118">Heure de début de la présentation.</span><span class="sxs-lookup"><span data-stu-id="7935a-118">Starting time for the presentation.</span></span><br/> <br/>                                                      |
| [<span data-ttu-id="7935a-119">**décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7935a-119">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/>                     | <span data-ttu-id="7935a-120">Décalage entre l’heure de présentation et les horodatages de la source du média.</span><span class="sxs-lookup"><span data-stu-id="7935a-120">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/>                 |
| [<span data-ttu-id="7935a-121">**\_ \_ \_ heure de début de la présentation de l’événement MF \_ \_ à la \_ sortie**</span><span class="sxs-lookup"><span data-stu-id="7935a-121">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md)<br/> | <span data-ttu-id="7935a-122">Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.</span><span class="sxs-lookup"><span data-stu-id="7935a-122">Presentation time when the media sinks will render the first sample of the new topology.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="7935a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7935a-123">Requirements</span></span>



| <span data-ttu-id="7935a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7935a-124">Requirement</span></span> | <span data-ttu-id="7935a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7935a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7935a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7935a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7935a-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7935a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7935a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7935a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7935a-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7935a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7935a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="7935a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7935a-131"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7935a-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7935a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7935a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7935a-133">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="7935a-133">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="7935a-134">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7935a-134">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




