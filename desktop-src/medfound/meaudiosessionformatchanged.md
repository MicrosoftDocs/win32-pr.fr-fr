---
description: Déclenché par le convertisseur audio lorsque le format audio par défaut pour le périphérique audio change. Le convertisseur audio n’est plus valide.
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: Événement MEAudioSessionFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1faddc73622c65d1eb32e0d723f576b9410d978b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863070"
---
# <a name="meaudiosessionformatchanged-event"></a><span data-ttu-id="6085b-104">Événement MEAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="6085b-104">MEAudioSessionFormatChanged event</span></span>

<span data-ttu-id="6085b-105">Déclenché par le convertisseur audio lorsque le format audio par défaut pour le périphérique audio change.</span><span class="sxs-lookup"><span data-stu-id="6085b-105">Raised by the audio renderer when the default audio format for the audio device changes.</span></span> <span data-ttu-id="6085b-106">Le convertisseur audio n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="6085b-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="6085b-107">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="6085b-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="6085b-108">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="6085b-108">Event values</span></span>

<span data-ttu-id="6085b-109">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="6085b-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6085b-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6085b-110">VARTYPE</span></span>                | <span data-ttu-id="6085b-111">Description</span><span class="sxs-lookup"><span data-stu-id="6085b-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6085b-112">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="6085b-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="6085b-113">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="6085b-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="6085b-114">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="6085b-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="6085b-115">Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="6085b-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6085b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6085b-116">Remarks</span></span>

<span data-ttu-id="6085b-117">Cet événement est envoyé par le récepteur de flux du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="6085b-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="6085b-118">L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio en mode utilisateur et que la raison de la déconnexion est égale à **DisconnectReasonFormatChanged**.</span><span class="sxs-lookup"><span data-stu-id="6085b-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the user-mode audio session with the disconnection reason equal to **DisconnectReasonFormatChanged**.</span></span>

<span data-ttu-id="6085b-119">Le pointeur [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , s’il est défini, n’est pas utile, car le flux audio n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="6085b-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="6085b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6085b-120">Requirements</span></span>



| <span data-ttu-id="6085b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6085b-121">Requirement</span></span> | <span data-ttu-id="6085b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6085b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6085b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6085b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6085b-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6085b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6085b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6085b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6085b-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6085b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6085b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6085b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6085b-128"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6085b-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6085b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6085b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6085b-130">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6085b-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="6085b-131">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="6085b-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
