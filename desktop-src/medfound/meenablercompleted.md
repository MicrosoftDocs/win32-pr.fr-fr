---
description: Déclenché par un objet activateur de contenu lorsque les objets qui activent l’action sont terminés.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Événement MEEnablerCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114630"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="a7527-103">Événement MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="a7527-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="a7527-104">Déclenché par un objet activateur de contenu lorsque l’action d’activation de l’objet est terminée.</span><span class="sxs-lookup"><span data-stu-id="a7527-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="a7527-105">Les objets qui exposent l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) peuvent déclencher cet événement.</span><span class="sxs-lookup"><span data-stu-id="a7527-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="a7527-106">L’événement est déclenché si l’un des événements suivants se produit :</span><span class="sxs-lookup"><span data-stu-id="a7527-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="a7527-107">La méthode [**IMFContentEnabler :: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a7527-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="a7527-108">L’application appelle [**IMFContentEnabler :: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), puis l’application termine la requête http après, comme décrit dans la méthode **MonitorEnable** .</span><span class="sxs-lookup"><span data-stu-id="a7527-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="a7527-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="a7527-109">Event values</span></span>

<span data-ttu-id="a7527-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7527-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a7527-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a7527-111">VARTYPE</span></span>              | <span data-ttu-id="a7527-112">Description</span><span class="sxs-lookup"><span data-stu-id="a7527-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a7527-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="a7527-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a7527-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="a7527-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a7527-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a7527-115">Remarks</span></span>

<span data-ttu-id="a7527-116">Le code d’état de l’événement peut contenir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7527-116">The status code from the event may contain one of the following values.</span></span>



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7527-117">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="a7527-117">**S\_OK**</span></span>                            | <span data-ttu-id="a7527-118">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a7527-118">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="a7527-119">**\_NOTACQUIRED de \_ \_ licence DRM \_ E**</span><span class="sxs-lookup"><span data-stu-id="a7527-119">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="a7527-120">La licence DRM n’a pas été acquise.</span><span class="sxs-lookup"><span data-stu-id="a7527-120">The DRM license was not acquired.</span></span> <span data-ttu-id="a7527-121">Si la tentative précédente a utilisé [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), l’application doit essayer une acquisition non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="a7527-121">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="a7527-122">**\_analyse DRM de NS S \_ \_ \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="a7527-122">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="a7527-123">L’opération [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) a été annulée.</span><span class="sxs-lookup"><span data-stu-id="a7527-123">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="a7527-124">Pour recevoir cet événement, interrogez l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="a7527-124">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="a7527-125">Appelez ensuite [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), comme décrit dans la rubrique [Media Event Generators](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="a7527-125">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7527-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7527-126">Requirements</span></span>



| <span data-ttu-id="a7527-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7527-127">Requirement</span></span> | <span data-ttu-id="a7527-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7527-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7527-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7527-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a7527-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7527-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a7527-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7527-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a7527-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7527-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7527-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7527-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7527-134"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7527-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7527-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7527-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7527-136">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="a7527-136">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="a7527-137">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="a7527-137">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="a7527-138">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7527-138">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




