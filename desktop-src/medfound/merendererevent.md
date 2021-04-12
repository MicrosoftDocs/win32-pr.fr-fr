---
description: Signale un événement à partir d’un récepteur multimédia qui restitue des données multimédias.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Événement MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202004"
---
# <a name="merendererevent-event"></a><span data-ttu-id="385b6-103">Événement MERendererEvent</span><span class="sxs-lookup"><span data-stu-id="385b6-103">MERendererEvent event</span></span>

<span data-ttu-id="385b6-104">Signale un événement à partir d’un récepteur multimédia qui restitue des données multimédias.</span><span class="sxs-lookup"><span data-stu-id="385b6-104">Signals an event from a media sink that renders media data.</span></span>

<span data-ttu-id="385b6-105">Le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) envoie cet événement lorsqu’il reçoit un événement utilisateur du présentateur EVR.</span><span class="sxs-lookup"><span data-stu-id="385b6-105">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) sends this event when it receives a user event from the EVR presenter.</span></span>

## <a name="event-values"></a><span data-ttu-id="385b6-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="385b6-106">Event values</span></span>

<span data-ttu-id="385b6-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="385b6-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="385b6-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="385b6-108">VARTYPE</span></span>           | <span data-ttu-id="385b6-109">Description</span><span class="sxs-lookup"><span data-stu-id="385b6-109">Description</span></span>                        |
|-------------------|------------------------------------|
| <span data-ttu-id="385b6-110">VT \_</span><span class="sxs-lookup"><span data-stu-id="385b6-110">VT\_I4</span></span><br/> | <span data-ttu-id="385b6-111">Code d’événement.</span><span class="sxs-lookup"><span data-stu-id="385b6-111">Event code.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="385b6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="385b6-112">Remarks</span></span>

<span data-ttu-id="385b6-113">Si le présenteur appelle la méthode **IMediaEventSink :: Notify** du EVR à l’aide d’un code d’événement dans la plage EC \_ ou supérieure, le EVR envoie cet événement.</span><span class="sxs-lookup"><span data-stu-id="385b6-113">If the presenter calls the EVR's **IMediaEventSink::Notify** method with an event code in the range EC\_USER or higher, the EVR sends this event.</span></span> <span data-ttu-id="385b6-114">Les données d’événement sont le code d’événement qui a été passé à la méthode **Notify** .</span><span class="sxs-lookup"><span data-stu-id="385b6-114">The event data is the event code that was passed to the **Notify** method.</span></span>

<span data-ttu-id="385b6-115">Les paramètres d’événement d’origine (*EventParam1* et *EventParam2* dans la méthode **IMediaEventSink :: Notify** ) sont ignorés, donc le présenteur doit définir ces valeurs sur **null**.</span><span class="sxs-lookup"><span data-stu-id="385b6-115">The original event parameters (*EventParam1* and *EventParam2* in the **IMediaEventSink::Notify** method) are ignored, so the presenter should set these values to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="385b6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="385b6-116">Requirements</span></span>



| <span data-ttu-id="385b6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="385b6-117">Requirement</span></span> | <span data-ttu-id="385b6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="385b6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="385b6-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="385b6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="385b6-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="385b6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="385b6-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="385b6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="385b6-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="385b6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="385b6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="385b6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="385b6-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="385b6-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="385b6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="385b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="385b6-126">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="385b6-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




