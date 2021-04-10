---
description: Envoyé par une source de capture audio lorsque la dession audio est déconnectée, car l’utilisateur s’est déconnecté d’une session Windows Terminal Services (WTS).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Événement MECaptureAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113919"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a><span data-ttu-id="0a3f9-103">Événement MECaptureAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="0a3f9-103">MECaptureAudioSessionDisconnected event</span></span>

<span data-ttu-id="0a3f9-104">Envoyé par une source de capture audio lorsque la dession audio est déconnectée, car l’utilisateur s’est déconnecté d’une session Windows Terminal Services (WTS).</span><span class="sxs-lookup"><span data-stu-id="0a3f9-104">Sent by an audio capture source when the audio dession is disconnected because the user logged off from a Windows Terminal Services (WTS) session.</span></span>

## <a name="event-values"></a><span data-ttu-id="0a3f9-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="0a3f9-105">Event values</span></span>

<span data-ttu-id="0a3f9-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a3f9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0a3f9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a3f9-107">VARTYPE</span></span>               | <span data-ttu-id="0a3f9-108">Description</span><span class="sxs-lookup"><span data-stu-id="0a3f9-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="0a3f9-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="0a3f9-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="0a3f9-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="0a3f9-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0a3f9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0a3f9-111">Remarks</span></span>

<span data-ttu-id="0a3f9-112">Cet événement est envoyé par le flux multimédia de la source de capture audio.</span><span class="sxs-lookup"><span data-stu-id="0a3f9-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="0a3f9-113">La source de capture envoie cet événement lorsqu’il reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à **DisconnectReasonSessionDisconnected**.</span><span class="sxs-lookup"><span data-stu-id="0a3f9-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonSessionDisconnected**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3f9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a3f9-114">Requirements</span></span>



| <span data-ttu-id="0a3f9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a3f9-115">Requirement</span></span> | <span data-ttu-id="0a3f9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a3f9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3f9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a3f9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a3f9-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a3f9-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="0a3f9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a3f9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a3f9-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a3f9-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a3f9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a3f9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a3f9-122"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a3f9-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a3f9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a3f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3f9-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a3f9-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
