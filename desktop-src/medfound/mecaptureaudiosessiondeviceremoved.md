---
description: Envoyé par une source de capture audio lorsque l’appareil est supprimé.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: Événement MECaptureAudioSessionDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0cf1b9a7536affed5a4665f6f2e364e1f872e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521394"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a><span data-ttu-id="0c47c-103">Événement MECaptureAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="0c47c-103">MECaptureAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="0c47c-104">Envoyé par une source de capture audio lorsque l’appareil est supprimé.</span><span class="sxs-lookup"><span data-stu-id="0c47c-104">Sent by an audio capture source when the device is removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="0c47c-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="0c47c-105">Event values</span></span>

<span data-ttu-id="0c47c-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0c47c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0c47c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c47c-107">VARTYPE</span></span>               | <span data-ttu-id="0c47c-108">Description</span><span class="sxs-lookup"><span data-stu-id="0c47c-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="0c47c-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="0c47c-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="0c47c-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="0c47c-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0c47c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0c47c-111">Remarks</span></span>

<span data-ttu-id="0c47c-112">Cet événement est envoyé par le flux multimédia de la source de capture audio.</span><span class="sxs-lookup"><span data-stu-id="0c47c-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="0c47c-113">La source de capture envoie cet événement lorsqu’il reçoit un événement [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) à partir de la session audio avec la raison de la déconnexion égale à **DisconnectReasonDeviceRemoval**.</span><span class="sxs-lookup"><span data-stu-id="0c47c-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c47c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c47c-114">Requirements</span></span>



| <span data-ttu-id="0c47c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c47c-115">Requirement</span></span> | <span data-ttu-id="0c47c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c47c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c47c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c47c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c47c-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c47c-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="0c47c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c47c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c47c-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c47c-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c47c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c47c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c47c-122"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c47c-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c47c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c47c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c47c-124">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c47c-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
