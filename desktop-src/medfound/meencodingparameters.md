---
description: Envoyé par le pipeline à l’encodeur MFTs en série avec des exemples de supports via IMFTransform ::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Événement MEEncodingParameters (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202008"
---
# <a name="meencodingparameters-event"></a><span data-ttu-id="a911c-103">Événement MEEncodingParameters</span><span class="sxs-lookup"><span data-stu-id="a911c-103">MEEncodingParameters event</span></span>

<span data-ttu-id="a911c-104">Envoyé par le pipeline à l’encodeur MFTs en série avec des exemples de supports via [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="a911c-104">Sent by the pipeline to encoder MFTs serially with media samples via [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="event-values"></a><span data-ttu-id="a911c-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="a911c-105">Event values</span></span>

<span data-ttu-id="a911c-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a911c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a911c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a911c-107">VARTYPE</span></span>              | <span data-ttu-id="a911c-108">Description</span><span class="sxs-lookup"><span data-stu-id="a911c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a911c-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="a911c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a911c-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="a911c-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="a911c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="a911c-111">Attributes</span></span>

<span data-ttu-id="a911c-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="a911c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="a911c-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a911c-113">Attribute</span></span>                                         | <span data-ttu-id="a911c-114">Description</span><span class="sxs-lookup"><span data-stu-id="a911c-114">Description</span></span>                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a911c-115">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="a911c-115">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | <span data-ttu-id="a911c-116">Contient les nouveaux paramètres basés sur un ICodecAPI que l’encodeur doit appliquer aux exemples entrants suivants.</span><span class="sxs-lookup"><span data-stu-id="a911c-116">Contains the new ICodecAPI-based settings that the encoder should apply on subsequent incoming samples.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a911c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a911c-117">Remarks</span></span>

<span data-ttu-id="a911c-118">La charge utile d’événement est un magasin d’attributs (pointeur IMFAttributes) qui contient les nouveaux paramètres basés sur ICodecAPI///que l’encodeur doit appliquer aux exemples entrants suivants.</span><span class="sxs-lookup"><span data-stu-id="a911c-118">Event payload is an attribute store (IMFAttributes pointer) that contains the new ICodecAPI-based /// settings that the encoder should apply on subsequent incoming samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="a911c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a911c-119">Requirements</span></span>



| <span data-ttu-id="a911c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a911c-120">Requirement</span></span> | <span data-ttu-id="a911c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a911c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a911c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a911c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a911c-123">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a911c-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a911c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a911c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a911c-125">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a911c-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="a911c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a911c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a911c-127"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a911c-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a911c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a911c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a911c-129">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a911c-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




