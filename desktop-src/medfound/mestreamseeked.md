---
description: 'Déclenché par un flux de média après un appel à IMFMediaSource :: START provoque une recherche dans le flux. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement MESourceSeeked.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Événement MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201997"
---
# <a name="mestreamseeked-event"></a><span data-ttu-id="8a114-104">Événement MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="8a114-104">MEStreamSeeked event</span></span>

<span data-ttu-id="8a114-105">Déclenché par un flux de média après un appel à [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoque une recherche dans le flux.</span><span class="sxs-lookup"><span data-stu-id="8a114-105">Raised by a media stream after a call to [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causes a seek in the stream.</span></span> <span data-ttu-id="8a114-106">Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="8a114-106">A media stream raises this event when the media source raises the [MESourceSeeked](mesourceseeked.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="8a114-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="8a114-107">Event values</span></span>

<span data-ttu-id="8a114-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a114-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8a114-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8a114-109">VARTYPE</span></span>           | <span data-ttu-id="8a114-110">Description</span><span class="sxs-lookup"><span data-stu-id="8a114-110">Description</span></span>                                                        |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8a114-111">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="8a114-111">VT\_I8</span></span><br/> | <span data-ttu-id="8a114-112">Nouvelle heure de début, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="8a114-112">New starting time, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="8a114-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a114-113">Requirements</span></span>



| <span data-ttu-id="8a114-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a114-114">Requirement</span></span> | <span data-ttu-id="8a114-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a114-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a114-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a114-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8a114-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a114-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8a114-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a114-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8a114-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a114-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8a114-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a114-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a114-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a114-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a114-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a114-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a114-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a114-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




