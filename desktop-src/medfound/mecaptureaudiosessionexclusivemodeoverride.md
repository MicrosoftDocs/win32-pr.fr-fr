---
description: Envoyé par une source de capture audio lorsqu’un autre programme ouvre le périphérique audio en mode exclusif.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Événement MECaptureAudioSessionExclusiveModeOverride (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751277"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="7cb24-103">Événement MECaptureAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="7cb24-103">MECaptureAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="7cb24-104">Envoyé par une source de capture audio lorsqu’un autre programme ouvre le périphérique audio en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="7cb24-104">Sent by an audio capture source when another program opens the audio device in exclusive mode.</span></span>

## <a name="event-values"></a><span data-ttu-id="7cb24-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="7cb24-105">Event values</span></span>

<span data-ttu-id="7cb24-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7cb24-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7cb24-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7cb24-107">VARTYPE</span></span>               | <span data-ttu-id="7cb24-108">Description</span><span class="sxs-lookup"><span data-stu-id="7cb24-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="7cb24-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="7cb24-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="7cb24-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="7cb24-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7cb24-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7cb24-111">Remarks</span></span>

<span data-ttu-id="7cb24-112">Cet événement est envoyé par le flux multimédia de la source de capture audio.</span><span class="sxs-lookup"><span data-stu-id="7cb24-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="7cb24-113">La source de capture envoie cet événement lorsqu’il reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à **DisconnectReasonExclusiveModeOverride**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonExclusiveModeOverride**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb24-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cb24-114">Requirements</span></span>



| <span data-ttu-id="7cb24-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cb24-115">Requirement</span></span> | <span data-ttu-id="7cb24-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb24-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb24-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb24-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb24-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb24-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="7cb24-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb24-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb24-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb24-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7cb24-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cb24-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cb24-122"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cb24-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cb24-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cb24-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb24-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7cb24-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
