---
description: Déclenché par une source de média lors du redémarrage ou de la recherche d’un flux déjà actif.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Événement MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529602"
---
# <a name="meupdatedstream-event"></a><span data-ttu-id="db454-103">Événement MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="db454-103">MEUpdatedStream event</span></span>

<span data-ttu-id="db454-104">Déclenché par une source de média lors du redémarrage ou de la recherche d’un flux déjà actif.</span><span class="sxs-lookup"><span data-stu-id="db454-104">Raised by a media source when it restarts or seeks a stream that is already active.</span></span>

<span data-ttu-id="db454-105">Quand la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) est appelée sur une source de média, la source du média envoie un événement pour chaque flux sélectionné :</span><span class="sxs-lookup"><span data-stu-id="db454-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="db454-106">La source envoie l’événement [MENewStream](menewstream.md) si le flux n’a pas été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou il s’agit du tout premier appel à **Start** sur cette source de média.</span><span class="sxs-lookup"><span data-stu-id="db454-106">The source sends the [MENewStream](menewstream.md) event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="db454-107">La source envoie l’événement MEUpdatedStream si le flux a déjà été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="db454-107">The source sends the MEUpdatedStream event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="db454-108">Aucun événement n’est envoyé pour les flux non sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="db454-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="db454-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="db454-109">Event values</span></span>

<span data-ttu-id="db454-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="db454-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="db454-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="db454-111">VARTYPE</span></span>                | <span data-ttu-id="db454-112">Description</span><span class="sxs-lookup"><span data-stu-id="db454-112">Description</span></span>                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db454-113">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="db454-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="db454-114">Pointeur vers l’interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) du flux.</span><span class="sxs-lookup"><span data-stu-id="db454-114">Pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="db454-115">Notes</span><span class="sxs-lookup"><span data-stu-id="db454-115">Remarks</span></span>

<span data-ttu-id="db454-116">Lors du premier appel à [**Démarrer**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) dans lequel un flux devient actif, la source du média envoie un événement [MENewStream](menewstream.md) pour le flux.</span><span class="sxs-lookup"><span data-stu-id="db454-116">On the first call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in which a stream becomes active, the media source sends an [MENewStream](menewstream.md) event for the stream.</span></span> <span data-ttu-id="db454-117">Lors des appels suivants à **Start**, la source du média envoie un événement MEUpdatedStream, jusqu’à ce que le flux soit désélectionné.</span><span class="sxs-lookup"><span data-stu-id="db454-117">On subsequent calls to **Start**, the media source sends an MEUpdatedStream event, until the stream is deselected.</span></span>

## <a name="requirements"></a><span data-ttu-id="db454-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db454-118">Requirements</span></span>



| <span data-ttu-id="db454-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db454-119">Requirement</span></span> | <span data-ttu-id="db454-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="db454-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db454-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db454-121">Minimum supported client</span></span><br/> | <span data-ttu-id="db454-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db454-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db454-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db454-123">Minimum supported server</span></span><br/> | <span data-ttu-id="db454-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db454-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db454-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="db454-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="db454-126"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db454-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db454-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db454-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db454-128">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db454-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




