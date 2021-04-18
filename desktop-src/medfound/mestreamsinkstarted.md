---
description: Déclenché par un récepteur de flux lorsqu’il termine la transition à l’État en cours d’exécution.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Événement MEStreamSinkStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533801"
---
# <a name="mestreamsinkstarted-event"></a><span data-ttu-id="49f8d-103">Événement MEStreamSinkStarted</span><span class="sxs-lookup"><span data-stu-id="49f8d-103">MEStreamSinkStarted event</span></span>

<span data-ttu-id="49f8d-104">Déclenché par un récepteur de flux lorsqu’il termine la transition à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="49f8d-104">Raised by a stream sink when it completes the transition to the running state.</span></span> <span data-ttu-id="49f8d-105">La transition vers l’exécution se produit lorsque la méthode [**IMFPresentationClock :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) est appelée sur l’horloge de présentation du récepteur.</span><span class="sxs-lookup"><span data-stu-id="49f8d-105">The transition to running occurs when the [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) method is called on the sink's presentation clock.</span></span> <span data-ttu-id="49f8d-106">Le récepteur multimédia reçoit la notification par le biais de sa méthode [**IMFClockStateSink :: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou [**IMFClockStateSink :: OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) .</span><span class="sxs-lookup"><span data-stu-id="49f8d-106">The media sink receives the notification through its [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="49f8d-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="49f8d-107">Event values</span></span>

<span data-ttu-id="49f8d-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="49f8d-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="49f8d-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="49f8d-109">VARTYPE</span></span>              | <span data-ttu-id="49f8d-110">Description</span><span class="sxs-lookup"><span data-stu-id="49f8d-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="49f8d-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="49f8d-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="49f8d-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="49f8d-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="49f8d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49f8d-113">Requirements</span></span>



| <span data-ttu-id="49f8d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49f8d-114">Requirement</span></span> | <span data-ttu-id="49f8d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="49f8d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f8d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49f8d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49f8d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49f8d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49f8d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49f8d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49f8d-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49f8d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49f8d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="49f8d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49f8d-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49f8d-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f8d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49f8d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f8d-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="49f8d-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="49f8d-124">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="49f8d-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




