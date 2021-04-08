---
description: 'Déclenché lorsque la méthode IMFMediaSession :: Start se termine de façon asynchrone.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Événement MESessionStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034216"
---
# <a name="mesessionstarted-event"></a><span data-ttu-id="844c7-103">Événement MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="844c7-103">MESessionStarted event</span></span>

<span data-ttu-id="844c7-104">Déclenché lorsque la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="844c7-104">Raised when the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="844c7-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="844c7-105">Event values</span></span>

<span data-ttu-id="844c7-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="844c7-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="844c7-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="844c7-107">VARTYPE</span></span>              | <span data-ttu-id="844c7-108">Description</span><span class="sxs-lookup"><span data-stu-id="844c7-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="844c7-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="844c7-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="844c7-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="844c7-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="844c7-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="844c7-111">Attributes</span></span>

<span data-ttu-id="844c7-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="844c7-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="844c7-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="844c7-113">Attribute</span></span>                                                                                               | <span data-ttu-id="844c7-114">Description</span><span class="sxs-lookup"><span data-stu-id="844c7-114">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="844c7-115">**décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="844c7-115">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/> | <span data-ttu-id="844c7-116">Décalage entre l’heure de présentation et les horodatages de la source du média.</span><span class="sxs-lookup"><span data-stu-id="844c7-116">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="844c7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="844c7-117">Requirements</span></span>



| <span data-ttu-id="844c7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="844c7-118">Requirement</span></span> | <span data-ttu-id="844c7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="844c7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="844c7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="844c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="844c7-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="844c7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="844c7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="844c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="844c7-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="844c7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="844c7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="844c7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="844c7-125"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="844c7-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="844c7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="844c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="844c7-127">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="844c7-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




