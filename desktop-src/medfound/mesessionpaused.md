---
description: Déclenché lorsque la méthode IMFMediaSession ::P ause se termine de façon asynchrone.
ms.assetid: 72546082-83ec-4481-a24f-e82bd6c88859
title: Événement MESessionPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3e8ef60426f83203cfffae3a75febfdf7032d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114622"
---
# <a name="mesessionpaused-event"></a><span data-ttu-id="cd18b-103">Événement MESessionPaused</span><span class="sxs-lookup"><span data-stu-id="cd18b-103">MESessionPaused event</span></span>

<span data-ttu-id="cd18b-104">Déclenché lorsque la méthode [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="cd18b-104">Raised when the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="cd18b-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="cd18b-105">Event values</span></span>

<span data-ttu-id="cd18b-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="cd18b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cd18b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cd18b-107">VARTYPE</span></span>              | <span data-ttu-id="cd18b-108">Description</span><span class="sxs-lookup"><span data-stu-id="cd18b-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="cd18b-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="cd18b-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="cd18b-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="cd18b-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="cd18b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd18b-111">Requirements</span></span>



| <span data-ttu-id="cd18b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd18b-112">Requirement</span></span> | <span data-ttu-id="cd18b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd18b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd18b-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd18b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cd18b-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd18b-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd18b-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd18b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cd18b-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd18b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd18b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd18b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd18b-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd18b-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd18b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd18b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd18b-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cd18b-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




