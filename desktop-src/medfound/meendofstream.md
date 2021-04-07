---
description: Déclenché par un flux de média lorsque le flux se termine.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Événement MEEndOfStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863618"
---
# <a name="meendofstream-event"></a><span data-ttu-id="5a13f-103">Événement MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="5a13f-103">MEEndOfStream event</span></span>

<span data-ttu-id="5a13f-104">Déclenché par un flux de média lorsque le flux se termine.</span><span class="sxs-lookup"><span data-stu-id="5a13f-104">Raised by a media stream when the stream ends.</span></span>

## <a name="event-values"></a><span data-ttu-id="5a13f-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="5a13f-105">Event values</span></span>

<span data-ttu-id="5a13f-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="5a13f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5a13f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5a13f-107">VARTYPE</span></span>              | <span data-ttu-id="5a13f-108">Description</span><span class="sxs-lookup"><span data-stu-id="5a13f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5a13f-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="5a13f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5a13f-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="5a13f-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5a13f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5a13f-111">Remarks</span></span>

<span data-ttu-id="5a13f-112">Lorsque la [session multimédia](media-session.md) reçoit l’événement MEEndOfStream, elle appelle [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) sur le récepteur multimédia correspondant, avec le type de marqueur **\_ \_ ENDOFSEGMENT** de marqueur MFSTREAMSINK.</span><span class="sxs-lookup"><span data-stu-id="5a13f-112">When the [Media Session](media-session.md) receives the MEEndOfStream event, it calls [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) on the corresponding media sink, with the **MFSTREAMSINK\_MARKER\_ENDOFSEGMENT** marker type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a13f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a13f-113">Requirements</span></span>



| <span data-ttu-id="5a13f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a13f-114">Requirement</span></span> | <span data-ttu-id="5a13f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a13f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a13f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a13f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a13f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a13f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a13f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a13f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a13f-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a13f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a13f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a13f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a13f-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a13f-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a13f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a13f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a13f-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a13f-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




