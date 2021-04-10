---
description: Déclenché par une source de média lors de la mise à jour de ses métadonnées.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Événement MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951300"
---
# <a name="mesourcemetadatachanged-event"></a><span data-ttu-id="4f243-103">Événement MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="4f243-103">MESourceMetadataChanged event</span></span>

<span data-ttu-id="4f243-104">Déclenché par une source de média lors de la mise à jour de ses métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4f243-104">Raised by a media source when it updates its metadata.</span></span>

## <a name="event-values"></a><span data-ttu-id="4f243-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="4f243-105">Event values</span></span>

<span data-ttu-id="4f243-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f243-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4f243-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4f243-107">VARTYPE</span></span>              | <span data-ttu-id="4f243-108">Description</span><span class="sxs-lookup"><span data-stu-id="4f243-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4f243-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="4f243-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4f243-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="4f243-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4f243-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4f243-111">Remarks</span></span>

<span data-ttu-id="4f243-112">Si la source du média ne peut pas fournir toutes les métadonnées lorsque la source est créée pour la première fois, elle doit déclencher cet événement une fois que les métadonnées sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="4f243-112">If the media source cannot provide all of the metadata when the source is first created, it should raise this event after the metadata is available.</span></span>

<span data-ttu-id="4f243-113">La source du média doit créer un nouveau descripteur de présentation et copier tous les attributs du descripteur de présentation (PD) vers l’objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="4f243-113">The media source should create a new presentation descriptor and copy all of the attributes from the presentation descriptor (PD) to the event object.</span></span> <span data-ttu-id="4f243-114">L’application peut utiliser l’objet d’événement pour énumérer les nouveaux attributs PD.</span><span class="sxs-lookup"><span data-stu-id="4f243-114">The application can use the event object to enumerate the new PD attributes.</span></span> <span data-ttu-id="4f243-115">En particulier, les valeurs pour [MF \_ PD \_ Duration](mf-pd-duration-attribute.md) et [MF \_ PD \_ total \_ file \_ Size](mf-pd-total-file-size-attribute.md) peuvent être inconnues jusqu’à ce que le fichier soit complètement téléchargé.</span><span class="sxs-lookup"><span data-stu-id="4f243-115">In particular, the values for [MF\_PD\_DURATION](mf-pd-duration-attribute.md) and [MF\_PD\_TOTAL\_FILE\_SIZE](mf-pd-total-file-size-attribute.md) might be unknown until the file is completely downloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f243-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f243-116">Requirements</span></span>



| <span data-ttu-id="4f243-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f243-117">Requirement</span></span> | <span data-ttu-id="4f243-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f243-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f243-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f243-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f243-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f243-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4f243-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f243-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f243-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f243-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f243-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f243-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f243-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f243-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f243-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f243-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f243-126">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f243-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4f243-127">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="4f243-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




