---
description: 'Déclenché lorsque la méthode IMFMediaSession :: STOP se termine de façon asynchrone.'
ms.assetid: 9cac9040-f652-4509-bbab-f2a41959d836
title: Événement MESessionStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1bd74c168931cc4ac68ae3c990a156664e4b9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320749"
---
# <a name="mesessionstopped-event"></a><span data-ttu-id="ee17d-103">Événement MESessionStopped</span><span class="sxs-lookup"><span data-stu-id="ee17d-103">MESessionStopped event</span></span>

<span data-ttu-id="ee17d-104">Déclenché lorsque la méthode [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ee17d-104">Raised when the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ee17d-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="ee17d-105">Event values</span></span>

<span data-ttu-id="ee17d-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee17d-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ee17d-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ee17d-107">VARTYPE</span></span>              | <span data-ttu-id="ee17d-108">Description</span><span class="sxs-lookup"><span data-stu-id="ee17d-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ee17d-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="ee17d-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ee17d-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="ee17d-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ee17d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee17d-111">Requirements</span></span>



| <span data-ttu-id="ee17d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee17d-112">Requirement</span></span> | <span data-ttu-id="ee17d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee17d-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee17d-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee17d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ee17d-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee17d-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ee17d-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee17d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ee17d-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee17d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ee17d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee17d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee17d-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee17d-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee17d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee17d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee17d-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee17d-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




