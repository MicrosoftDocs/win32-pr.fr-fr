---
description: Déclenché quand une source de média démarre sans rechercher.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Événement MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528263"
---
# <a name="mesourcestarted-event"></a><span data-ttu-id="251a0-103">Événement MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="251a0-103">MESourceStarted event</span></span>

<span data-ttu-id="251a0-104">Déclenché quand une source de média démarre sans rechercher.</span><span class="sxs-lookup"><span data-stu-id="251a0-104">Raised when a media source starts without seeking.</span></span>

## <a name="event-values"></a><span data-ttu-id="251a0-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="251a0-105">Event values</span></span>

<span data-ttu-id="251a0-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="251a0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="251a0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="251a0-107">VARTYPE</span></span>              | <span data-ttu-id="251a0-108">Description</span><span class="sxs-lookup"><span data-stu-id="251a0-108">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="251a0-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="251a0-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="251a0-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="251a0-110">No event data.</span></span> <span data-ttu-id="251a0-111">L’heure de début était à partir de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="251a0-111">The start time was from the current position.</span></span><br/> <br/>                            |
| <span data-ttu-id="251a0-112">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="251a0-112">VT\_I8</span></span><br/>    | <span data-ttu-id="251a0-113">Heure de début, en unités de 100 nanosecondes, par rapport aux horodatages sur les échantillons.</span><span class="sxs-lookup"><span data-stu-id="251a0-113">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="251a0-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="251a0-114">Attributes</span></span>

<span data-ttu-id="251a0-115">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="251a0-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="251a0-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="251a0-116">Attribute</span></span>                                                                                     | <span data-ttu-id="251a0-117">Description</span><span class="sxs-lookup"><span data-stu-id="251a0-117">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="251a0-118">**\_ \_ \_ début réel de la source de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="251a0-118">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)<br/> | <span data-ttu-id="251a0-119">Heure de début</span><span class="sxs-lookup"><span data-stu-id="251a0-119">Start time.</span></span> <span data-ttu-id="251a0-120">La source du média définit cet attribut si elle redémarre à partir de sa position actuelle.</span><span class="sxs-lookup"><span data-stu-id="251a0-120">The media source sets this attribute if it restarts from its current position.</span></span><br/> <br/>                     |
| [<span data-ttu-id="251a0-121">**début du substitut de la \_ source d’événement MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="251a0-121">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)<br/>     | <span data-ttu-id="251a0-122">Spécifie si la topologie du segment actuel est vide.</span><span class="sxs-lookup"><span data-stu-id="251a0-122">Specifies whether the current segment topology is empty.</span></span> <span data-ttu-id="251a0-123">La source Sequencer définit cet attribut.</span><span class="sxs-lookup"><span data-stu-id="251a0-123">The sequencer source sets this attribute.</span></span><br/> <br/>             |
| [<span data-ttu-id="251a0-124">**\_ \_ PROJECTSTART source de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="251a0-124">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)<br/>  | <span data-ttu-id="251a0-125">Heure de début d’un segment, par rapport au début de la présentation.</span><span class="sxs-lookup"><span data-stu-id="251a0-125">Start time for a segment, relative to the start of the presentation.</span></span> <span data-ttu-id="251a0-126">La source Sequencer définit cet attribut.</span><span class="sxs-lookup"><span data-stu-id="251a0-126">The sequencer source sets this attribute.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="251a0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="251a0-127">Remarks</span></span>

<span data-ttu-id="251a0-128">Une source de média déclenche cet événement lorsqu’elle démarre à partir de l’état arrêté ou qu’elle commence à partir d’un état suspendu à la même position dans la source.</span><span class="sxs-lookup"><span data-stu-id="251a0-128">A media source raises this event when it starts from a stopped state, or starts from a paused state at the same position in the source.</span></span> <span data-ttu-id="251a0-129">L’événement est déclenché si la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="251a0-129">The event is raised if the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method returns S\_OK.</span></span>

<span data-ttu-id="251a0-130">Si la source du média démarre à partir de la position actuelle et que l’état précédent de la source était en cours d’exécution ou suspendu, les données d’événement peuvent être vides (VT \_ vide).</span><span class="sxs-lookup"><span data-stu-id="251a0-130">If the media source starts from the current position and the source's previous state was running or paused, the event data can empty (VT\_EMPTY).</span></span> <span data-ttu-id="251a0-131">Si les données d’événement sont des données VT \_ vides, la source du média peut définir l’attribut de [**\_ \_ \_ \_ démarrage réel**](mf-event-source-actual-start-attribute.md) de la source de l’événement MF avec l’heure de début réelle.</span><span class="sxs-lookup"><span data-stu-id="251a0-131">If the event data is VT\_EMPTY, the media source might set the [**MF\_EVENT\_SOURCE\_ACTUAL\_START**](mf-event-source-actual-start-attribute.md) attribute with the actual starting time.</span></span>

<span data-ttu-id="251a0-132">Si la source du média démarre à partir d’une nouvelle position, ou si l’état précédent de la source a été arrêté, les données d’événement doivent être l’heure de début (VT \_ I8).</span><span class="sxs-lookup"><span data-stu-id="251a0-132">If the media source starts from a new position, or the source's previous state was stopped, the event data must be the starting time (VT\_I8).</span></span>

<span data-ttu-id="251a0-133">Si la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoque une recherche, la source du média envoie l’événement [MESourceSeeked](mesourceseeked.md) au lieu de MESourceStarted.</span><span class="sxs-lookup"><span data-stu-id="251a0-133">If the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method causes a seek, the media source sends the [MESourceSeeked](mesourceseeked.md) event instead of MESourceStarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="251a0-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="251a0-134">Requirements</span></span>



| <span data-ttu-id="251a0-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="251a0-135">Requirement</span></span> | <span data-ttu-id="251a0-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="251a0-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="251a0-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="251a0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="251a0-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="251a0-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="251a0-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="251a0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="251a0-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="251a0-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="251a0-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="251a0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="251a0-142"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="251a0-142"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="251a0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="251a0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251a0-144">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="251a0-144">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




