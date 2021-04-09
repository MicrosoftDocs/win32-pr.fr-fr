---
description: Signale la progression d’un objet activateur de contenu. Les objets qui exposent l’interface IMFContentEnabler peuvent déclencher cet événement pour avertir l’application de la progression des actions des activateurs du contenu.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Événement MEEnablerProgress (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202009"
---
# <a name="meenablerprogress-event"></a><span data-ttu-id="25112-104">Événement MEEnablerProgress</span><span class="sxs-lookup"><span data-stu-id="25112-104">MEEnablerProgress event</span></span>

<span data-ttu-id="25112-105">Signale la progression d’un objet activateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="25112-105">Signals the progress of a content enabler object.</span></span> <span data-ttu-id="25112-106">Les objets qui exposent l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) peuvent déclencher cet événement pour avertir l’application de la progression des actions de l’activateur du contenu.</span><span class="sxs-lookup"><span data-stu-id="25112-106">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event to notify the application about the progress of the content enabler's actions.</span></span>

## <a name="event-values"></a><span data-ttu-id="25112-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="25112-107">Event values</span></span>

<span data-ttu-id="25112-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="25112-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="25112-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="25112-109">VARTYPE</span></span>               | <span data-ttu-id="25112-110">Description</span><span class="sxs-lookup"><span data-stu-id="25112-110">Description</span></span>                                                               |
|-----------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="25112-111">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="25112-111">VT\_LPWSTR</span></span><br/> | <span data-ttu-id="25112-112">Chaîne de caractères larges qui décrit la progression.</span><span class="sxs-lookup"><span data-stu-id="25112-112">Wide-character string that describes the progress.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="25112-113">Notes</span><span class="sxs-lookup"><span data-stu-id="25112-113">Remarks</span></span>

<span data-ttu-id="25112-114">Pour recevoir cet événement, interrogez l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="25112-114">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="25112-115">Appelez ensuite [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), comme décrit dans la rubrique [Media Event Generators](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="25112-115">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25112-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25112-116">Requirements</span></span>



| <span data-ttu-id="25112-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25112-117">Requirement</span></span> | <span data-ttu-id="25112-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="25112-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25112-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25112-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25112-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25112-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25112-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25112-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25112-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25112-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25112-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="25112-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="25112-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25112-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25112-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25112-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25112-126">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="25112-126">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="25112-127">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="25112-127">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="25112-128">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25112-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




