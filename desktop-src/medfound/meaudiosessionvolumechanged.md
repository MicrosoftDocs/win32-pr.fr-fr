---
description: Envoyé par le convertisseur audio de streaming (SAR) lorsque l’état du volume ou du silence de la session audio change.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Événement MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520384"
---
# <a name="meaudiosessionvolumechanged-event"></a><span data-ttu-id="a8453-103">Événement MEAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="a8453-103">MEAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="a8453-104">Envoyé par le convertisseur audio de streaming (SAR) lorsque l’état du volume ou du silence de la session audio change.</span><span class="sxs-lookup"><span data-stu-id="a8453-104">Sent by the streaming audio renderer (SAR) when the volume or mute state of the audio session changes.</span></span>

<span data-ttu-id="a8453-105">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="a8453-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="a8453-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="a8453-106">Event values</span></span>

<span data-ttu-id="a8453-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8453-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a8453-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a8453-108">VARTYPE</span></span>                | <span data-ttu-id="a8453-109">Description</span><span class="sxs-lookup"><span data-stu-id="a8453-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8453-110">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="a8453-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="a8453-111">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="a8453-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="a8453-112">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="a8453-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="a8453-113">Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="a8453-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a8453-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a8453-114">Remarks</span></span>

<span data-ttu-id="a8453-115">Cet événement est déclenché par le récepteur de flux de la RAS.</span><span class="sxs-lookup"><span data-stu-id="a8453-115">This event is raised by the stream sink of the SAR.</span></span> <span data-ttu-id="a8453-116">L’événement est déclenché lorsque le SAR reçoit un événement [**IAudioSessionEvents :: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) à partir de la session audio.</span><span class="sxs-lookup"><span data-stu-id="a8453-116">The event is triggered when the SAR receives an [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) event from the audio session.</span></span> <span data-ttu-id="a8453-117">Pour accéder au nouveau niveau de volume et à l’État muet, appelez [**IMFSimpleAudioVolume :: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) et [**IMFSimpleAudioVolume :: GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span><span class="sxs-lookup"><span data-stu-id="a8453-117">To get the new volume level and mute state, call [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) and [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span></span>

<span data-ttu-id="a8453-118">Le SAR envoie cet événement si une action externe modifie le volume, par exemple, si l’utilisateur modifie le volume par le biais du programme de contrôle de volume système (SndVol).</span><span class="sxs-lookup"><span data-stu-id="a8453-118">The SAR sends this event if an external action changes the volume—for example, if the user changes the volume through the system volume-control program (SndVol).</span></span> <span data-ttu-id="a8453-119">Le SAR n’envoie pas l’événement si l’application modifie le volume directement sur le SAR.</span><span class="sxs-lookup"><span data-stu-id="a8453-119">The SAR does not send the event if the application changes the volume directly on the SAR.</span></span>

<span data-ttu-id="a8453-120">En outre, le SAR n’envoie pas cet événement lorsque le volume du canal change ([**IAudioSessionEvents :: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span><span class="sxs-lookup"><span data-stu-id="a8453-120">Also, the SAR does not send this event when the channel volume changes ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8453-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8453-121">Requirements</span></span>



| <span data-ttu-id="a8453-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8453-122">Requirement</span></span> | <span data-ttu-id="a8453-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8453-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8453-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8453-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8453-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8453-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8453-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8453-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8453-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8453-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8453-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8453-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8453-129"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8453-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8453-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8453-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8453-131">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8453-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="a8453-132">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="a8453-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
