---
description: Envoyé par une source de capture audio lorsque le volume change.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Événement MECaptureAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527618"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a><span data-ttu-id="3646c-103">Événement MECaptureAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="3646c-103">MECaptureAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="3646c-104">Envoyé par une source de capture audio lorsque le volume change.</span><span class="sxs-lookup"><span data-stu-id="3646c-104">Sent by an audio capture source when the volume changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="3646c-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="3646c-105">Event values</span></span>

<span data-ttu-id="3646c-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="3646c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3646c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3646c-107">VARTYPE</span></span>               | <span data-ttu-id="3646c-108">Description</span><span class="sxs-lookup"><span data-stu-id="3646c-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="3646c-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="3646c-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="3646c-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="3646c-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3646c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3646c-111">Remarks</span></span>

<span data-ttu-id="3646c-112">Cet événement est envoyé par le flux multimédia de la source de capture audio.</span><span class="sxs-lookup"><span data-stu-id="3646c-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="3646c-113">La source de capture audio envoie cet événement si une action externe modifie le volume, par exemple, si l’utilisateur modifie le volume par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="3646c-113">The audio capture source sends this event if an external action changes the volume—for example, if the user changes the volume through the Control Panel.</span></span> <span data-ttu-id="3646c-114">La source de capture n’envoie pas l’événement si l’application modifie le volume directement sur la source.</span><span class="sxs-lookup"><span data-stu-id="3646c-114">The capture source does not send the event if the application changes the volume directly on the source.</span></span>

## <a name="requirements"></a><span data-ttu-id="3646c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3646c-115">Requirements</span></span>



| <span data-ttu-id="3646c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3646c-116">Requirement</span></span> | <span data-ttu-id="3646c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3646c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3646c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3646c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3646c-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3646c-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3646c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3646c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3646c-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3646c-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3646c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3646c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3646c-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3646c-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3646c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3646c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3646c-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3646c-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




