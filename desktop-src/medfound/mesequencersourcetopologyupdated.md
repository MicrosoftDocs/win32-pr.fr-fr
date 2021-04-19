---
description: 'Déclenché par la source de Sequencer lorsque la méthode IMFSequencerSource :: UpdateTopology se termine de façon asynchrone.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Événement MESequencerSourceTopologyUpdated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534421"
---
# <a name="mesequencersourcetopologyupdated-event"></a><span data-ttu-id="f5f16-103">Événement MESequencerSourceTopologyUpdated</span><span class="sxs-lookup"><span data-stu-id="f5f16-103">MESequencerSourceTopologyUpdated event</span></span>

<span data-ttu-id="f5f16-104">Déclenché par la source de Sequencer lorsque la méthode [**IMFSequencerSource :: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f5f16-104">Raised by the sequencer source when the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="f5f16-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="f5f16-105">Event values</span></span>

<span data-ttu-id="f5f16-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5f16-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f5f16-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f5f16-107">VARTYPE</span></span>            | <span data-ttu-id="f5f16-108">Description</span><span class="sxs-lookup"><span data-stu-id="f5f16-108">Description</span></span>                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f16-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f5f16-109">VT\_UI4</span></span><br/> | <span data-ttu-id="f5f16-110">Identificateur de l’élément de séquenceur de la topologie en cours de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f5f16-110">Sequencer element identifier of the topology that is being updated.</span></span> <span data-ttu-id="f5f16-111">L’application spécifie cette valeur dans le paramètre *dwId* de la méthode [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .</span><span class="sxs-lookup"><span data-stu-id="f5f16-111">The application specifies this value in the *dwId* parameter of the [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f5f16-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f5f16-112">Remarks</span></span>

<span data-ttu-id="f5f16-113">Cet événement signale que la source de Sequencer a mis à jour la topologie, mais ne signifie pas que la topologie est prête pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="f5f16-113">This event signals that the sequencer source has updated the topology, but does not mean that the topology is ready for playback.</span></span> <span data-ttu-id="f5f16-114">L’application doit attendre l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f16-114">The application should wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f16-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5f16-115">Requirements</span></span>



| <span data-ttu-id="f5f16-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5f16-116">Requirement</span></span> | <span data-ttu-id="f5f16-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f16-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f16-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5f16-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f16-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5f16-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f5f16-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5f16-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f16-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5f16-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5f16-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5f16-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f16-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5f16-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f16-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5f16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f16-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5f16-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f5f16-126">Source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="f5f16-126">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




