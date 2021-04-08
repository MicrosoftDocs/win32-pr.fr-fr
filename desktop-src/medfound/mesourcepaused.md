---
description: Déclenché par une source de média lorsque la méthode IMFMediaSource ::P ause se termine de façon asynchrone.
ms.assetid: cca03d60-47ae-4a11-b29d-81d749e24df9
title: Événement MESourcePaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac346e679eb3a82ca707a14f772f1a79e2a1e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863605"
---
# <a name="mesourcepaused-event"></a><span data-ttu-id="fe0f1-103">Événement MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="fe0f1-103">MESourcePaused event</span></span>

<span data-ttu-id="fe0f1-104">Déclenché par une source de média lorsque la méthode [**IMFMediaSource ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-104">Raised by a media source when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="fe0f1-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="fe0f1-105">Event values</span></span>

<span data-ttu-id="fe0f1-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fe0f1-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fe0f1-107">VARTYPE</span></span>              | <span data-ttu-id="fe0f1-108">Description</span><span class="sxs-lookup"><span data-stu-id="fe0f1-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="fe0f1-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="fe0f1-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="fe0f1-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="fe0f1-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="fe0f1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe0f1-111">Requirements</span></span>



| <span data-ttu-id="fe0f1-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe0f1-112">Requirement</span></span> | <span data-ttu-id="fe0f1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe0f1-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0f1-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe0f1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0f1-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe0f1-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe0f1-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe0f1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0f1-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe0f1-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe0f1-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe0f1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0f1-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe0f1-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0f1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe0f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0f1-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe0f1-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




