---
description: Déclenché par le convertisseur audio lorsque l’icône de session audio change.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Événement MEAudioSessionIconChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538653"
---
# <a name="meaudiosessioniconchanged-event"></a><span data-ttu-id="e0807-103">Événement MEAudioSessionIconChanged</span><span class="sxs-lookup"><span data-stu-id="e0807-103">MEAudioSessionIconChanged event</span></span>

<span data-ttu-id="e0807-104">Déclenché par le convertisseur audio lorsque l’icône de session audio change.</span><span class="sxs-lookup"><span data-stu-id="e0807-104">Raised by the audio renderer when the audio session icon changes.</span></span>

<span data-ttu-id="e0807-105">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="e0807-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="e0807-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="e0807-106">Event values</span></span>

<span data-ttu-id="e0807-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0807-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e0807-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e0807-108">VARTYPE</span></span>                | <span data-ttu-id="e0807-109">Description</span><span class="sxs-lookup"><span data-stu-id="e0807-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0807-110">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="e0807-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="e0807-111">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="e0807-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="e0807-112">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="e0807-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="e0807-113">Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="e0807-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e0807-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e0807-114">Remarks</span></span>

<span data-ttu-id="e0807-115">Cet événement est envoyé par le récepteur de flux du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="e0807-115">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="e0807-116">L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) à partir de la session audio.</span><span class="sxs-lookup"><span data-stu-id="e0807-116">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) event from the audio session.</span></span>

<span data-ttu-id="e0807-117">Pour afficher la nouvelle icône, appelez [**IMFAudioPolicy :: GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span><span class="sxs-lookup"><span data-stu-id="e0807-117">To get the new icon, call [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0807-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0807-118">Requirements</span></span>



| <span data-ttu-id="e0807-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0807-119">Requirement</span></span> | <span data-ttu-id="e0807-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0807-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0807-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0807-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e0807-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0807-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0807-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0807-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e0807-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0807-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e0807-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0807-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0807-126"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0807-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0807-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0807-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0807-128">**IMFAudioPolicy::GetIconPath**</span><span class="sxs-lookup"><span data-stu-id="e0807-128">**IMFAudioPolicy::GetIconPath**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[<span data-ttu-id="e0807-129">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0807-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e0807-130">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="e0807-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
