---
description: Envoyé par un récepteur de flux lorsque le format en aval est devenu invalidé et qu’il doit être renégocié.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Événement MEStreamSinkFormatInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536976"
---
# <a name="mestreamsinkformatinvalidated-event"></a><span data-ttu-id="d2183-103">Événement MEStreamSinkFormatInvalidated</span><span class="sxs-lookup"><span data-stu-id="d2183-103">MEStreamSinkFormatInvalidated event</span></span>

<span data-ttu-id="d2183-104">Envoyé par un récepteur de flux lorsque le format en aval est devenu invalidé et qu’il doit être renégocié.</span><span class="sxs-lookup"><span data-stu-id="d2183-104">Sent by a stream sink when the downstream format has become invalidated and it needs to be renegotiated.</span></span>

## <a name="event-values"></a><span data-ttu-id="d2183-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="d2183-105">Event values</span></span>

<span data-ttu-id="d2183-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2183-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d2183-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d2183-107">VARTYPE</span></span>              | <span data-ttu-id="d2183-108">Description</span><span class="sxs-lookup"><span data-stu-id="d2183-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d2183-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="d2183-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d2183-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="d2183-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d2183-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d2183-111">Remarks</span></span>

<span data-ttu-id="d2183-112">Les données qui ont été mises en file d’attente dans le récepteur, après la position de lecture actuelle, doivent être renvoyées.</span><span class="sxs-lookup"><span data-stu-id="d2183-112">Data that was queued to the sink, past the current playback position, should be resent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2183-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2183-113">Requirements</span></span>



| <span data-ttu-id="d2183-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2183-114">Requirement</span></span> | <span data-ttu-id="d2183-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2183-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2183-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2183-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d2183-117">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2183-117">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                                      |
| <span data-ttu-id="d2183-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2183-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d2183-119">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2183-119">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="d2183-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2183-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2183-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2183-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2183-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2183-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2183-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2183-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




