---
description: 'Déclenché par une source de média pour demander un nouveau taux de lecture. L’application doit appeler IMFRateControl :: SEDE la vitesse demandée. Une source de média peut déclencher cet événement si elle ne peut pas continuer la lecture à la vitesse actuelle.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Événement MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201999"
---
# <a name="mesourceratechangerequested-event"></a><span data-ttu-id="1e5e4-105">Événement MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="1e5e4-105">MESourceRateChangeRequested event</span></span>

<span data-ttu-id="1e5e4-106">Déclenché par une source de média pour demander un nouveau taux de lecture.</span><span class="sxs-lookup"><span data-stu-id="1e5e4-106">Raised by a media source to request a new playback rate.</span></span> <span data-ttu-id="1e5e4-107">L’application doit appeler [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SEDE la vitesse demandée.</span><span class="sxs-lookup"><span data-stu-id="1e5e4-107">The application should call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) with the requested rate.</span></span> <span data-ttu-id="1e5e4-108">Une source de média peut déclencher cet événement si elle ne peut pas continuer la lecture à la vitesse actuelle.</span><span class="sxs-lookup"><span data-stu-id="1e5e4-108">A media source might raise this event if it cannot continue playback at the current rate.</span></span>

## <a name="event-values"></a><span data-ttu-id="1e5e4-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="1e5e4-109">Event values</span></span>

<span data-ttu-id="1e5e4-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e5e4-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1e5e4-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1e5e4-111">VARTYPE</span></span>           | <span data-ttu-id="1e5e4-112">Description</span><span class="sxs-lookup"><span data-stu-id="1e5e4-112">Description</span></span>                                             |
|-------------------|---------------------------------------------------------|
| <span data-ttu-id="1e5e4-113">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="1e5e4-113">VT\_R4</span></span><br/> | <span data-ttu-id="1e5e4-114">Nouveau taux de lecture demandé.</span><span class="sxs-lookup"><span data-stu-id="1e5e4-114">The requested new playback rate.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="1e5e4-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="1e5e4-115">Attributes</span></span>

<span data-ttu-id="1e5e4-116">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="1e5e4-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="1e5e4-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="1e5e4-117">Attribute</span></span>                                                                    | <span data-ttu-id="1e5e4-118">Description</span><span class="sxs-lookup"><span data-stu-id="1e5e4-118">Description</span></span>                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1e5e4-119">**\_événement MF \_ - \_ éclaircir**</span><span class="sxs-lookup"><span data-stu-id="1e5e4-119">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)<br/> | <span data-ttu-id="1e5e4-120">Spécifie si la source du média demande également une éclaircie.</span><span class="sxs-lookup"><span data-stu-id="1e5e4-120">Specifies whether the media source also requests thinning.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="1e5e4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e5e4-121">Requirements</span></span>



| <span data-ttu-id="1e5e4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e5e4-122">Requirement</span></span> | <span data-ttu-id="1e5e4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e5e4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5e4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e5e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5e4-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e5e4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e5e4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e5e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5e4-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e5e4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e5e4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e5e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e5e4-129"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e5e4-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e5e4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e5e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5e4-131">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e5e4-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




