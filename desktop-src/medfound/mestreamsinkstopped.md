---
description: Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état arrêté. La transition à Stopped se produit lorsque la méthode Stop IMFPresentationClock est appelée sur l’horloge de présentation des récepteurs.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Événement MEStreamSinkStopped (Mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034832"
---
# <a name="mestreamsinkstopped-event"></a><span data-ttu-id="95e15-104">Événement MEStreamSinkStopped</span><span class="sxs-lookup"><span data-stu-id="95e15-104">MEStreamSinkStopped event</span></span>

<span data-ttu-id="95e15-105">Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="95e15-105">Raised by a stream sink when it completes the transition to the stopped state.</span></span> <span data-ttu-id="95e15-106">La transition à Stopped se produit lorsque la méthode [**IMFPresentationClock :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) est appelée sur l’horloge de présentation du récepteur.</span><span class="sxs-lookup"><span data-stu-id="95e15-106">The transition to stopped occurs when the [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="95e15-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="95e15-107">Event values</span></span>

<span data-ttu-id="95e15-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="95e15-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="95e15-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="95e15-109">VARTYPE</span></span>              | <span data-ttu-id="95e15-110">Description</span><span class="sxs-lookup"><span data-stu-id="95e15-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="95e15-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="95e15-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="95e15-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="95e15-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="95e15-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95e15-113">Requirements</span></span>



| <span data-ttu-id="95e15-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95e15-114">Requirement</span></span> | <span data-ttu-id="95e15-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="95e15-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e15-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95e15-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95e15-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95e15-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95e15-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95e15-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95e15-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95e15-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95e15-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="95e15-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e15-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95e15-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e15-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95e15-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e15-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95e15-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="95e15-124">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="95e15-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




