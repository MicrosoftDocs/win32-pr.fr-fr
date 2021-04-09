---
description: Déclenché par une source de média qui fournit des topologies par le biais de l’interface IMFMediaSourceTopologyProvider, telle que la source de Sequencer. La source déclenche l’événement lorsqu’elle a une nouvelle présentation. La session multimédia transmet cet événement à l’application.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Événement MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202006"
---
# <a name="menewpresentation-event"></a><span data-ttu-id="9d917-105">Événement MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="9d917-105">MENewPresentation event</span></span>

<span data-ttu-id="9d917-106">Déclenché par une source de média qui fournit des topologies par le biais de l’interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , telle que la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="9d917-106">Raised by a media source that provides topologies through the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface, such as the sequencer source.</span></span> <span data-ttu-id="9d917-107">La source déclenche l’événement lorsqu’elle a une nouvelle présentation.</span><span class="sxs-lookup"><span data-stu-id="9d917-107">The source raises the event when it has a new presentation.</span></span> <span data-ttu-id="9d917-108">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="9d917-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="9d917-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="9d917-109">Event values</span></span>

<span data-ttu-id="9d917-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d917-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9d917-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9d917-111">VARTYPE</span></span>                | <span data-ttu-id="9d917-112">Description</span><span class="sxs-lookup"><span data-stu-id="9d917-112">Description</span></span>                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d917-113">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="9d917-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="9d917-114">Pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation pour la nouvelle présentation.</span><span class="sxs-lookup"><span data-stu-id="9d917-114">Pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor for the new presentation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9d917-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9d917-115">Remarks</span></span>

<span data-ttu-id="9d917-116">L’application peut récupérer la topologie qui correspond au descripteur de présentation en appelant [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="9d917-116">The application can get the topology that corresponds to the presentation descriptor by calling [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the media source.</span></span> <span data-ttu-id="9d917-117">L’application peut ensuite faire la file d’attente de la nouvelle topologie sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="9d917-117">The application can then queue the new topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d917-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d917-118">Requirements</span></span>



| <span data-ttu-id="9d917-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d917-119">Requirement</span></span> | <span data-ttu-id="9d917-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d917-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d917-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d917-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d917-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d917-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9d917-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d917-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d917-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d917-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9d917-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d917-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d917-126"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d917-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d917-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d917-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d917-128">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d917-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="9d917-129">Source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="9d917-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




