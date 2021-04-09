---
description: Déclenché par la source de Sequencer lorsqu’un segment est terminé et qu’il est suivi d’un autre segment. Lorsque le segment final est terminé, la source de Sequencer déclenche un événement MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Événement MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863621"
---
# <a name="meendofpresentationsegment-event"></a><span data-ttu-id="5fbfb-104">Événement MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="5fbfb-104">MEEndOfPresentationSegment event</span></span>

<span data-ttu-id="5fbfb-105">Déclenché par la source de Sequencer lorsqu’un segment est terminé et qu’il est suivi d’un autre segment.</span><span class="sxs-lookup"><span data-stu-id="5fbfb-105">Raised by the sequencer source when a segment is completed and is followed by another segment.</span></span> <span data-ttu-id="5fbfb-106">Lorsque le segment final est terminé, la source de Sequencer déclenche un événement [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="5fbfb-106">When the final segment is completed, the sequencer source raises an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

<span data-ttu-id="5fbfb-107">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="5fbfb-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="5fbfb-108">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="5fbfb-108">Event values</span></span>

<span data-ttu-id="5fbfb-109">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="5fbfb-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5fbfb-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5fbfb-110">VARTYPE</span></span>              | <span data-ttu-id="5fbfb-111">Description</span><span class="sxs-lookup"><span data-stu-id="5fbfb-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5fbfb-112">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="5fbfb-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5fbfb-113">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="5fbfb-113">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="5fbfb-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="5fbfb-114">Attributes</span></span>

<span data-ttu-id="5fbfb-115">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="5fbfb-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="5fbfb-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="5fbfb-116">Attribute</span></span>                                                                                               | <span data-ttu-id="5fbfb-117">Description</span><span class="sxs-lookup"><span data-stu-id="5fbfb-117">Description</span></span>                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fbfb-118">**TOPOLOGIE de la \_ source d’événements MF \_ \_ \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="5fbfb-118">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="5fbfb-119">Spécifie si la source de Sequencer a annulé ce segment.</span><span class="sxs-lookup"><span data-stu-id="5fbfb-119">Specifies whether the sequencer source canceled this segment.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5fbfb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fbfb-120">Requirements</span></span>



| <span data-ttu-id="5fbfb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fbfb-121">Requirement</span></span> | <span data-ttu-id="5fbfb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fbfb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbfb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fbfb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5fbfb-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fbfb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5fbfb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fbfb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5fbfb-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fbfb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5fbfb-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fbfb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fbfb-128"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fbfb-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fbfb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fbfb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbfb-130">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fbfb-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="5fbfb-131">À propos de la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="5fbfb-131">About the Sequencer Source</span></span>](about-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="5fbfb-132">Événements de source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="5fbfb-132">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




