---
description: Envoyé par une source de capture audio lorsque le format audio change.
ms.assetid: 8197BBAD-8102-43C3-BA61-8DC3BC13B7D6
title: Événement MECaptureAudioSessionFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfb260d186a9e4d8434669e6a8c3ef08078b93af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318650"
---
# <a name="mecaptureaudiosessionformatchanged-event"></a><span data-ttu-id="3db7a-103">Événement MECaptureAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="3db7a-103">MECaptureAudioSessionFormatChanged event</span></span>

<span data-ttu-id="3db7a-104">Envoyé par une source de capture audio lorsque le format audio change.</span><span class="sxs-lookup"><span data-stu-id="3db7a-104">Sent by an audio capture source when the audio format changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="3db7a-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="3db7a-105">Event values</span></span>

<span data-ttu-id="3db7a-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="3db7a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3db7a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3db7a-107">VARTYPE</span></span>               | <span data-ttu-id="3db7a-108">Description</span><span class="sxs-lookup"><span data-stu-id="3db7a-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="3db7a-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="3db7a-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="3db7a-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="3db7a-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3db7a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3db7a-111">Remarks</span></span>

<span data-ttu-id="3db7a-112">Cet événement est envoyé par le flux multimédia de la source de capture audio.</span><span class="sxs-lookup"><span data-stu-id="3db7a-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="3db7a-113">La source de capture envoie cet événement lorsqu’il reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à **DisconnectReasonFormatChanged**.</span><span class="sxs-lookup"><span data-stu-id="3db7a-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonFormatChanged**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db7a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3db7a-114">Requirements</span></span>



| <span data-ttu-id="3db7a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3db7a-115">Requirement</span></span> | <span data-ttu-id="3db7a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3db7a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db7a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3db7a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3db7a-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3db7a-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3db7a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3db7a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3db7a-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3db7a-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3db7a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3db7a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db7a-122"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3db7a-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db7a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3db7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db7a-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3db7a-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
