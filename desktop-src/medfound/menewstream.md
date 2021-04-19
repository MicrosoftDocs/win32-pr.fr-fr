---
description: Déclenché par une source de média lorsqu’elle démarre un nouveau flux.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Événement MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524964"
---
# <a name="menewstream-event"></a><span data-ttu-id="dbb16-103">Événement MENewStream</span><span class="sxs-lookup"><span data-stu-id="dbb16-103">MENewStream event</span></span>

<span data-ttu-id="dbb16-104">Déclenché par une source de média lorsqu’elle démarre un nouveau flux.</span><span class="sxs-lookup"><span data-stu-id="dbb16-104">Raised by a media source when it starts a new stream.</span></span>

<span data-ttu-id="dbb16-105">Quand la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) est appelée sur une source de média, la source du média envoie un événement pour chaque flux sélectionné :</span><span class="sxs-lookup"><span data-stu-id="dbb16-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="dbb16-106">La source envoie l’événement MENewStream si le flux n’a pas été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou il s’agit du tout premier appel à **Start** sur cette source de média.</span><span class="sxs-lookup"><span data-stu-id="dbb16-106">The source sends the MENewStream event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="dbb16-107">La source envoie l’événement [MEUpdatedStream](meupdatedstream.md) si le flux a déjà été sélectionné dans l’appel précédent à [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="dbb16-107">The source sends the [MEUpdatedStream](meupdatedstream.md) event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="dbb16-108">Aucun événement n’est envoyé pour les flux non sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="dbb16-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="dbb16-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="dbb16-109">Event values</span></span>

<span data-ttu-id="dbb16-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="dbb16-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dbb16-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dbb16-111">VARTYPE</span></span>                | <span data-ttu-id="dbb16-112">Description</span><span class="sxs-lookup"><span data-stu-id="dbb16-112">Description</span></span>                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb16-113">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="dbb16-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="dbb16-114">Contient un pointeur vers l’interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) du flux.</span><span class="sxs-lookup"><span data-stu-id="dbb16-114">Contains a pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="dbb16-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbb16-115">Requirements</span></span>



| <span data-ttu-id="dbb16-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbb16-116">Requirement</span></span> | <span data-ttu-id="dbb16-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbb16-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb16-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbb16-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb16-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbb16-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dbb16-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbb16-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb16-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbb16-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dbb16-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbb16-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb16-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbb16-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb16-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb16-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dbb16-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




