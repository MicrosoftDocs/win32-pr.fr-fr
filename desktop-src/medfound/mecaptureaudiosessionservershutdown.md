---
description: Envoyé par une source de capture audio lorsque la session audio de capture est déconnectée en raison de l’arrêt du serveur audio.
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: Événement MECaptureAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad934f6d60868c1db7c5b5b7907ff720312ea439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521065"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a><span data-ttu-id="f0c65-103">Événement MECaptureAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="f0c65-103">MECaptureAudioSessionServerShutdown event</span></span>

<span data-ttu-id="f0c65-104">Envoyé par une source de capture audio lorsque la session audio de capture est déconnectée en raison de l’arrêt du serveur audio.</span><span class="sxs-lookup"><span data-stu-id="f0c65-104">Sent by an audio capture source when the capture audio session is disconnected due to the audio server being shutdown.</span></span>

## <a name="event-values"></a><span data-ttu-id="f0c65-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="f0c65-105">Event values</span></span>

<span data-ttu-id="f0c65-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0c65-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f0c65-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f0c65-107">VARTYPE</span></span>               | <span data-ttu-id="f0c65-108">Description</span><span class="sxs-lookup"><span data-stu-id="f0c65-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="f0c65-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="f0c65-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="f0c65-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="f0c65-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f0c65-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0c65-111">Requirements</span></span>



| <span data-ttu-id="f0c65-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0c65-112">Requirement</span></span> | <span data-ttu-id="f0c65-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0c65-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c65-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0c65-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c65-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0c65-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f0c65-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0c65-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c65-117">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0c65-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0c65-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0c65-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0c65-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0c65-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c65-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0c65-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c65-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0c65-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




