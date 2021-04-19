---
description: Déclenché par un flux de média lorsque la méthode IMFMediaSource ::P ause se termine de façon asynchrone.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Événement MEStreamPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517308"
---
# <a name="mestreampaused-event"></a><span data-ttu-id="18afb-103">Événement MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="18afb-103">MEStreamPaused event</span></span>

<span data-ttu-id="18afb-104">Déclenché par un flux de média lorsque la méthode [**IMFMediaSource ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="18afb-104">Raised by a media stream when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="18afb-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="18afb-105">Event values</span></span>

<span data-ttu-id="18afb-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="18afb-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="18afb-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="18afb-107">VARTYPE</span></span>              | <span data-ttu-id="18afb-108">Description</span><span class="sxs-lookup"><span data-stu-id="18afb-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="18afb-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="18afb-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="18afb-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="18afb-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="18afb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="18afb-111">Remarks</span></span>

<span data-ttu-id="18afb-112">Chaque flux actif dans la présentation envoie cet événement.</span><span class="sxs-lookup"><span data-stu-id="18afb-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="18afb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18afb-113">Requirements</span></span>



| <span data-ttu-id="18afb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18afb-114">Requirement</span></span> | <span data-ttu-id="18afb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="18afb-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18afb-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18afb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="18afb-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18afb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="18afb-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18afb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="18afb-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18afb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18afb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="18afb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="18afb-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18afb-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18afb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18afb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18afb-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18afb-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




