---
description: Déclenché par le convertisseur audio lorsque le nom d’affichage de la session audio change.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Événement MEAudioSessionNameChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752877"
---
# <a name="meaudiosessionnamechanged-event"></a><span data-ttu-id="ca612-103">Événement MEAudioSessionNameChanged</span><span class="sxs-lookup"><span data-stu-id="ca612-103">MEAudioSessionNameChanged event</span></span>

<span data-ttu-id="ca612-104">Déclenché par le convertisseur audio lorsque le nom d’affichage de la session audio change.</span><span class="sxs-lookup"><span data-stu-id="ca612-104">Raised by the audio renderer when the audio session display name changes.</span></span>

<span data-ttu-id="ca612-105">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="ca612-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="ca612-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="ca612-106">Event values</span></span>

<span data-ttu-id="ca612-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca612-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ca612-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ca612-108">VARTYPE</span></span>                | <span data-ttu-id="ca612-109">Description</span><span class="sxs-lookup"><span data-stu-id="ca612-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca612-110">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="ca612-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="ca612-111">Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="ca612-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ca612-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ca612-112">Remarks</span></span>

<span data-ttu-id="ca612-113">Cet événement est envoyé par le récepteur de flux du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="ca612-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="ca612-114">L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) à partir de la session audio.</span><span class="sxs-lookup"><span data-stu-id="ca612-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) event from the audio session.</span></span>

<span data-ttu-id="ca612-115">Pour obtenir le nouveau nom d’affichage, appelez [**IMFAudioPolicy :: GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span><span class="sxs-lookup"><span data-stu-id="ca612-115">To get the new display name, call [**IMFAudioPolicy::GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca612-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca612-116">Requirements</span></span>



| <span data-ttu-id="ca612-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca612-117">Requirement</span></span> | <span data-ttu-id="ca612-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca612-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca612-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca612-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ca612-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca612-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ca612-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca612-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ca612-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca612-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ca612-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca612-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca612-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca612-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca612-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca612-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca612-126">**IMFAudioPolicy :: GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="ca612-126">**IMFAudioPolicy::GetDisplayName**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[<span data-ttu-id="ca612-127">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca612-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ca612-128">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="ca612-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
