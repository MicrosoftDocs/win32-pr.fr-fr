---
description: Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état suspendu.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Événement MEStreamSinkPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533998"
---
# <a name="mestreamsinkpaused-event"></a><span data-ttu-id="e8697-103">Événement MEStreamSinkPaused</span><span class="sxs-lookup"><span data-stu-id="e8697-103">MEStreamSinkPaused event</span></span>

<span data-ttu-id="e8697-104">Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="e8697-104">Raised by a stream sink when it completes the transition to the paused state.</span></span> <span data-ttu-id="e8697-105">La transition à suspendre se produit lorsque la méthode [**IMFPresentationClock ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) est appelée sur l’horloge de présentation du récepteur.</span><span class="sxs-lookup"><span data-stu-id="e8697-105">The transition to paused occurs when the [**IMFPresentationClock::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="e8697-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="e8697-106">Event values</span></span>

<span data-ttu-id="e8697-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8697-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e8697-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e8697-108">VARTYPE</span></span>              | <span data-ttu-id="e8697-109">Description</span><span class="sxs-lookup"><span data-stu-id="e8697-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e8697-110">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="e8697-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e8697-111">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="e8697-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e8697-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8697-112">Requirements</span></span>



| <span data-ttu-id="e8697-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8697-113">Requirement</span></span> | <span data-ttu-id="e8697-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8697-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8697-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8697-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e8697-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8697-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8697-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8697-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e8697-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8697-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8697-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8697-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8697-120"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8697-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8697-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8697-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8697-122">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8697-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e8697-123">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="e8697-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




