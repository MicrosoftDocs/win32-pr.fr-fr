---
description: Déclenché par le convertisseur audio lorsque la session audio est déconnectée d’une session Windows Terminal Services (WTS). Le convertisseur audio n’est plus valide.
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: Événement MEAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2d31349585d26c61cb2940cea70ddaf0617901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533763"
---
# <a name="meaudiosessiondisconnected-event"></a><span data-ttu-id="0b434-104">Événement MEAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="0b434-104">MEAudioSessionDisconnected event</span></span>

<span data-ttu-id="0b434-105">Déclenché par le convertisseur audio lorsque la session audio est déconnectée d’une session Windows Terminal Services (WTS).</span><span class="sxs-lookup"><span data-stu-id="0b434-105">Raised by the audio renderer when the audio session is disconnected from a Windows Terminal Services (WTS) session.</span></span> <span data-ttu-id="0b434-106">Le convertisseur audio n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="0b434-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="0b434-107">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="0b434-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0b434-108">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="0b434-108">Event values</span></span>

<span data-ttu-id="0b434-109">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0b434-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0b434-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0b434-110">VARTYPE</span></span>                | <span data-ttu-id="0b434-111">Description</span><span class="sxs-lookup"><span data-stu-id="0b434-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b434-112">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="0b434-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="0b434-113">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="0b434-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="0b434-114">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="0b434-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0b434-115">Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="0b434-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0b434-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0b434-116">Remarks</span></span>

<span data-ttu-id="0b434-117">Cet événement est envoyé par le récepteur de flux du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="0b434-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="0b434-118">L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à DisconnectReasonSessionDisconnected.</span><span class="sxs-lookup"><span data-stu-id="0b434-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to DisconnectReasonSessionDisconnected.</span></span>

<span data-ttu-id="0b434-119">Le pointeur [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , s’il est défini, n’est pas utile, car le flux audio n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="0b434-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b434-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b434-120">Requirements</span></span>



| <span data-ttu-id="0b434-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b434-121">Requirement</span></span> | <span data-ttu-id="0b434-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b434-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b434-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b434-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0b434-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b434-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b434-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b434-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0b434-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b434-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b434-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b434-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b434-128"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b434-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b434-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b434-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b434-130">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b434-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0b434-131">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="0b434-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
