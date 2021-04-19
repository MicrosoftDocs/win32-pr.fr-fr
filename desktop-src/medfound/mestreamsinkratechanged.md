---
description: Déclenché par un récepteur de flux lorsque le taux a changé.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Événement MEStreamSinkRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532135"
---
# <a name="mestreamsinkratechanged-event"></a><span data-ttu-id="da0bb-103">Événement MEStreamSinkRateChanged</span><span class="sxs-lookup"><span data-stu-id="da0bb-103">MEStreamSinkRateChanged event</span></span>

<span data-ttu-id="da0bb-104">Déclenché par un récepteur de flux lorsque le taux a changé.</span><span class="sxs-lookup"><span data-stu-id="da0bb-104">Raised by a stream sink when the rate has changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="da0bb-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="da0bb-105">Event values</span></span>

<span data-ttu-id="da0bb-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="da0bb-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="da0bb-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="da0bb-107">VARTYPE</span></span>              | <span data-ttu-id="da0bb-108">Description</span><span class="sxs-lookup"><span data-stu-id="da0bb-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="da0bb-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="da0bb-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="da0bb-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="da0bb-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="da0bb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="da0bb-111">Remarks</span></span>

<span data-ttu-id="da0bb-112">Si un récepteur de flux prend en charge les changements de taux, il envoie cet événement une fois que la modification du taux est terminée.</span><span class="sxs-lookup"><span data-stu-id="da0bb-112">If a stream sink supports rate changes, it sends this event after the rate change is complete.</span></span> <span data-ttu-id="da0bb-113">L’événement est envoyé une fois pour chaque appel à la méthode [**IMFClockStateSink :: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) du récepteur.</span><span class="sxs-lookup"><span data-stu-id="da0bb-113">The event is sent once for each call to the sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span> <span data-ttu-id="da0bb-114">Si la modification du taux échoue, la valeur de l’état de l’événement est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="da0bb-114">If the rate change is not successful, the event status value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0bb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da0bb-115">Requirements</span></span>



| <span data-ttu-id="da0bb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da0bb-116">Requirement</span></span> | <span data-ttu-id="da0bb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="da0bb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da0bb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da0bb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da0bb-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da0bb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da0bb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da0bb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da0bb-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da0bb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da0bb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="da0bb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="da0bb-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da0bb-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da0bb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da0bb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0bb-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da0bb-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="da0bb-126">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="da0bb-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




