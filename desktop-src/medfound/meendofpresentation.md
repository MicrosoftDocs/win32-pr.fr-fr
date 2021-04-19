---
description: Déclenché par une source de média lorsqu’une présentation se termine. Cet événement signale que tous les flux de la présentation sont terminés. La session multimédia transmet cet événement à l’application.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Événement MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544252"
---
# <a name="meendofpresentation-event"></a><span data-ttu-id="88267-105">Événement MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="88267-105">MEEndOfPresentation event</span></span>

<span data-ttu-id="88267-106">Déclenché par une source de média lorsqu’une présentation se termine.</span><span class="sxs-lookup"><span data-stu-id="88267-106">Raised by a media source when a presentation ends.</span></span> <span data-ttu-id="88267-107">Cet événement signale que tous les flux de la présentation sont terminés.</span><span class="sxs-lookup"><span data-stu-id="88267-107">This event signals that all streams in the presentation are complete.</span></span> <span data-ttu-id="88267-108">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="88267-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="88267-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="88267-109">Event values</span></span>

<span data-ttu-id="88267-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="88267-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="88267-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="88267-111">VARTYPE</span></span>              | <span data-ttu-id="88267-112">Description</span><span class="sxs-lookup"><span data-stu-id="88267-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="88267-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="88267-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="88267-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="88267-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="88267-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="88267-115">Attributes</span></span>

<span data-ttu-id="88267-116">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="88267-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="88267-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="88267-117">Attribute</span></span>                                                                                               | <span data-ttu-id="88267-118">Description</span><span class="sxs-lookup"><span data-stu-id="88267-118">Description</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88267-119">**TOPOLOGIE de la \_ source d’événements MF \_ \_ \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="88267-119">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="88267-120">Spécifie si la source de Sequencer a annulé cette présentation.</span><span class="sxs-lookup"><span data-stu-id="88267-120">Specifies whether the sequencer source canceled this presentation.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="88267-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88267-121">Requirements</span></span>



| <span data-ttu-id="88267-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88267-122">Requirement</span></span> | <span data-ttu-id="88267-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="88267-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88267-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88267-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88267-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88267-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="88267-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88267-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88267-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88267-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88267-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="88267-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="88267-129"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88267-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88267-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88267-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88267-131">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="88267-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




