---
description: 'Déclenché par une source de média lorsque la méthode IMFMediaSource :: STOP se termine de façon asynchrone.'
ms.assetid: 0eda9aa1-3aad-43ac-9d87-ab96e4ac319d
title: Événement MESourceStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08909a95cf1c867c5d8392425f25565b5a2728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545794"
---
# <a name="mesourcestopped-event"></a><span data-ttu-id="2cc78-103">Événement MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="2cc78-103">MESourceStopped event</span></span>

<span data-ttu-id="2cc78-104">Déclenché par une source de média lorsque la méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2cc78-104">Raised by a media source when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="2cc78-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="2cc78-105">Event values</span></span>

<span data-ttu-id="2cc78-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="2cc78-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2cc78-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2cc78-107">VARTYPE</span></span>              | <span data-ttu-id="2cc78-108">Description</span><span class="sxs-lookup"><span data-stu-id="2cc78-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2cc78-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="2cc78-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2cc78-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="2cc78-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="2cc78-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cc78-111">Requirements</span></span>



| <span data-ttu-id="2cc78-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cc78-112">Requirement</span></span> | <span data-ttu-id="2cc78-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cc78-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc78-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cc78-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc78-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cc78-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cc78-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cc78-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc78-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cc78-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2cc78-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2cc78-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc78-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cc78-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc78-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cc78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc78-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2cc78-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




