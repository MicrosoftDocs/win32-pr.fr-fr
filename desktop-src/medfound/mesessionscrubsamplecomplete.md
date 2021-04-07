---
description: Déclenché par la session multimédia lorsqu’elle termine une demande de nettoyage.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Événement MESessionScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863610"
---
# <a name="mesessionscrubsamplecomplete-event"></a><span data-ttu-id="ed704-103">Événement MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="ed704-103">MESessionScrubSampleComplete event</span></span>

<span data-ttu-id="ed704-104">Déclenché par la session multimédia lorsqu’elle termine une demande de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="ed704-104">Raised by the Media Session when it completes a scrubbing request.</span></span>

<span data-ttu-id="ed704-105">Le nettoyage se produit lorsque la vitesse de lecture est égale à zéro et que l’application appelle [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="ed704-105">Scrubbing occurs when the playback rate is zero and the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="ed704-106">Cet événement est déclenché après la fin de la demande de nettoyage de chaque récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="ed704-106">This event is raised after every stream sink has completed the scrubbing request.</span></span>

## <a name="event-values"></a><span data-ttu-id="ed704-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="ed704-107">Event values</span></span>

<span data-ttu-id="ed704-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed704-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ed704-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ed704-109">VARTYPE</span></span>              | <span data-ttu-id="ed704-110">Description</span><span class="sxs-lookup"><span data-stu-id="ed704-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ed704-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="ed704-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ed704-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="ed704-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ed704-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed704-113">Requirements</span></span>



| <span data-ttu-id="ed704-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed704-114">Requirement</span></span> | <span data-ttu-id="ed704-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed704-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed704-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed704-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed704-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed704-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ed704-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed704-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed704-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed704-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed704-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed704-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed704-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed704-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed704-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed704-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed704-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed704-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ed704-124">MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="ed704-124">MEStreamSinkScrubSampleComplete</span></span>](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




