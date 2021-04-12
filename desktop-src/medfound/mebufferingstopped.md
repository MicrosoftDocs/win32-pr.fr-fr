---
description: Signale qu’une source de média a cessé de mettre en mémoire tampon des données.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Événement MEBufferingStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318697"
---
# <a name="mebufferingstopped-event"></a><span data-ttu-id="6707d-103">Événement MEBufferingStopped</span><span class="sxs-lookup"><span data-stu-id="6707d-103">MEBufferingStopped event</span></span>

<span data-ttu-id="6707d-104">Signale qu’une source de média a cessé de mettre en mémoire tampon des données.</span><span class="sxs-lookup"><span data-stu-id="6707d-104">Signals that a media source has stopped buffering data.</span></span>

<span data-ttu-id="6707d-105">Une source de média l’envoie lorsqu’elle arrête la mise en mémoire tampon des données après l’envoi de l’événement [MEBufferingStarted](mebufferingstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="6707d-105">A media source sends this when it stops buffering data after sending the [MEBufferingStarted](mebufferingstarted.md) event.</span></span>

<span data-ttu-id="6707d-106">Les flux d’octets qui implémentent l’interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) envoient également cet événement.</span><span class="sxs-lookup"><span data-stu-id="6707d-106">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="6707d-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="6707d-107">Event values</span></span>

<span data-ttu-id="6707d-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="6707d-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6707d-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6707d-109">VARTYPE</span></span>              | <span data-ttu-id="6707d-110">Description</span><span class="sxs-lookup"><span data-stu-id="6707d-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6707d-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="6707d-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6707d-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="6707d-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6707d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6707d-113">Remarks</span></span>

<span data-ttu-id="6707d-114">Lorsque la session multimédia reçoit cet événement, elle redémarre l’horloge de la présentation.</span><span class="sxs-lookup"><span data-stu-id="6707d-114">When the Media Session receives this event, it restarts the presentation clock.</span></span> <span data-ttu-id="6707d-115">La session multimédia transmet également l’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="6707d-115">The Media Session also forwards the event to the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="6707d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6707d-116">Requirements</span></span>



| <span data-ttu-id="6707d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6707d-117">Requirement</span></span> | <span data-ttu-id="6707d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6707d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6707d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6707d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6707d-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6707d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6707d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6707d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6707d-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6707d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6707d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6707d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6707d-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6707d-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6707d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6707d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6707d-126">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6707d-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




