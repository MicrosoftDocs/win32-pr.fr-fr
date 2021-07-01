---
description: Déclenché par un objet activateur de contenu lorsque les objets qui activent l’action sont terminés.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Événement MEEnablerCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119444"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="c157f-103">Événement MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="c157f-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="c157f-104">Déclenché par un objet activateur de contenu lorsque l’action d’activation de l’objet est terminée.</span><span class="sxs-lookup"><span data-stu-id="c157f-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="c157f-105">Les objets qui exposent l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) peuvent déclencher cet événement.</span><span class="sxs-lookup"><span data-stu-id="c157f-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="c157f-106">L’événement est déclenché si l’un des événements suivants se produit :</span><span class="sxs-lookup"><span data-stu-id="c157f-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="c157f-107">La méthode [**IMFContentEnabler :: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c157f-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="c157f-108">L’application appelle [**IMFContentEnabler :: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), puis l’application termine la requête http après, comme décrit dans la méthode **MonitorEnable** .</span><span class="sxs-lookup"><span data-stu-id="c157f-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="c157f-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="c157f-109">Event values</span></span>

<span data-ttu-id="c157f-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="c157f-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c157f-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c157f-111">VARTYPE</span></span>              | <span data-ttu-id="c157f-112">Description</span><span class="sxs-lookup"><span data-stu-id="c157f-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c157f-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="c157f-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c157f-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="c157f-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c157f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="c157f-115">Remarks</span></span>

<span data-ttu-id="c157f-116">Le code d’état de l’événement peut contenir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c157f-116">The status code from the event may contain one of the following values.</span></span>



| <span data-ttu-id="c157f-117">Value</span><span class="sxs-lookup"><span data-stu-id="c157f-117">Value</span></span>                                     | <span data-ttu-id="c157f-118">Description</span><span class="sxs-lookup"><span data-stu-id="c157f-118">Description</span></span>                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c157f-119">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="c157f-119">**S\_OK**</span></span>                            | <span data-ttu-id="c157f-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c157f-120">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="c157f-121">**\_NOTACQUIRED de \_ \_ licence DRM \_ E**</span><span class="sxs-lookup"><span data-stu-id="c157f-121">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="c157f-122">La licence DRM n’a pas été acquise.</span><span class="sxs-lookup"><span data-stu-id="c157f-122">The DRM license was not acquired.</span></span> <span data-ttu-id="c157f-123">Si la tentative précédente a utilisé [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), l’application doit essayer une acquisition non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="c157f-123">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="c157f-124">**\_analyse DRM de NS S \_ \_ \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="c157f-124">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="c157f-125">L’opération [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) a été annulée.</span><span class="sxs-lookup"><span data-stu-id="c157f-125">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="c157f-126">Pour recevoir cet événement, interrogez l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="c157f-126">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="c157f-127">Appelez ensuite [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), comme décrit dans la rubrique [Media Event Generators](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="c157f-127">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c157f-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c157f-128">Requirements</span></span>



| <span data-ttu-id="c157f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c157f-129">Requirement</span></span> | <span data-ttu-id="c157f-130">Value</span><span class="sxs-lookup"><span data-stu-id="c157f-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c157f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c157f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c157f-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c157f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c157f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c157f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c157f-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c157f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c157f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="c157f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c157f-136"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c157f-136"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c157f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c157f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c157f-138">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="c157f-138">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="c157f-139">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="c157f-139">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="c157f-140">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c157f-140">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




