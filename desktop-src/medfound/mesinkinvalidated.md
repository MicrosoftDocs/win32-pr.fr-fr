---
description: Déclenché lorsqu’un récepteur multimédia devient non valide.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Événement MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201616"
---
# <a name="mesinkinvalidated-event"></a><span data-ttu-id="0e35b-103">Événement MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="0e35b-103">MESinkInvalidated event</span></span>

<span data-ttu-id="0e35b-104">Déclenché lorsqu’un récepteur multimédia devient non valide.</span><span class="sxs-lookup"><span data-stu-id="0e35b-104">Raised when a media sink becomes invalid.</span></span>

## <a name="event-values"></a><span data-ttu-id="0e35b-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="0e35b-105">Event values</span></span>

<span data-ttu-id="0e35b-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e35b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0e35b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0e35b-107">VARTYPE</span></span>              | <span data-ttu-id="0e35b-108">Description</span><span class="sxs-lookup"><span data-stu-id="0e35b-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0e35b-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="0e35b-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0e35b-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="0e35b-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="0e35b-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="0e35b-111">Attributes</span></span>

<span data-ttu-id="0e35b-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="0e35b-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="0e35b-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="0e35b-113">Attribute</span></span>                                                                    | <span data-ttu-id="0e35b-114">Description</span><span class="sxs-lookup"><span data-stu-id="0e35b-114">Description</span></span>                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="0e35b-115">**\_ \_ nœud sortie de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="0e35b-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="0e35b-116">Identifie le nœud de topologie de ce récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="0e35b-116">Identifies the topology node for this media sink.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0e35b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0e35b-117">Remarks</span></span>

<span data-ttu-id="0e35b-118">La session multimédia déclenche cet événement si elle reçoit l’un des événements suivants du récepteur multimédia :</span><span class="sxs-lookup"><span data-stu-id="0e35b-118">The Media Session raises this event if it receives any of the following events from the media sink:</span></span>

-   [<span data-ttu-id="0e35b-119">MEAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="0e35b-119">MEAudioSessionDeviceRemoved</span></span>](meaudiosessiondeviceremoved.md)

-   [<span data-ttu-id="0e35b-120">MEAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="0e35b-120">MEAudioSessionDisconnected</span></span>](meaudiosessiondisconnected.md)

-   [<span data-ttu-id="0e35b-121">MEAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="0e35b-121">MEAudioSessionExclusiveModeOverride</span></span>](meaudiosessionexclusivemodeoverride.md)

-   [<span data-ttu-id="0e35b-122">MEAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="0e35b-122">MEAudioSessionFormatChanged</span></span>](meaudiosessionformatchanged.md)

-   [<span data-ttu-id="0e35b-123">MEAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="0e35b-123">MEAudioSessionServerShutdown</span></span>](meaudiosessionservershutdown.md)

<span data-ttu-id="0e35b-124">Un récepteur multimédia peut également déclencher cet événement, auquel cas la session multimédia définit l’attribut [**de \_ \_ \_ nœud sortie d’événement MF**](mf-event-output-node-attribute.md) sur l’événement et transfère l’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="0e35b-124">A media sink can also raise this event, in which case the Media Session sets the [**MF\_EVENT\_OUTPUT\_NODE**](mf-event-output-node-attribute.md) attribute on the event and forwards the event to the application.</span></span>

<span data-ttu-id="0e35b-125">Si l’application reçoit cet événement, elle a besoin de recréer le récepteur multimédia et de recréer la file d’attente de la topologie.</span><span class="sxs-lookup"><span data-stu-id="0e35b-125">If the application receives this event, it needs to recreate the media sink and queue the topology again.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e35b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e35b-126">Requirements</span></span>



| <span data-ttu-id="0e35b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e35b-127">Requirement</span></span> | <span data-ttu-id="0e35b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e35b-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e35b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e35b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0e35b-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e35b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0e35b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e35b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0e35b-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e35b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e35b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e35b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e35b-134"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e35b-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e35b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e35b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e35b-136">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e35b-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




