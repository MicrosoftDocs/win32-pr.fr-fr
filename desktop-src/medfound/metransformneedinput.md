---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) pour demander un nouvel exemple d’entrée.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Événement METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113690"
---
# <a name="metransformneedinput-event"></a><span data-ttu-id="91732-103">Événement METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="91732-103">METransformNeedInput event</span></span>

<span data-ttu-id="91732-104">Envoyé par une transformation de Media Foundation asynchrone (MFT) pour demander un nouvel exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="91732-104">Sent by an asynchronous Media Foundation transform (MFT) to request a new input sample.</span></span>

## <a name="event-values"></a><span data-ttu-id="91732-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="91732-105">Event values</span></span>

<span data-ttu-id="91732-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="91732-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="91732-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="91732-107">VARTYPE</span></span>              | <span data-ttu-id="91732-108">Description</span><span class="sxs-lookup"><span data-stu-id="91732-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="91732-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="91732-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="91732-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="91732-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="91732-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="91732-111">Attributes</span></span>

<span data-ttu-id="91732-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="91732-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="91732-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="91732-113">Attribute</span></span>                                                                        | <span data-ttu-id="91732-114">Description</span><span class="sxs-lookup"><span data-stu-id="91732-114">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="91732-115">\_ID de \_ \_ flux d’entrée MFT \_ \_ de l’événement MF</span><span class="sxs-lookup"><span data-stu-id="91732-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="91732-116">Identificateur du flux qui a besoin de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="91732-116">The identifier of the stream that needs input data.</span></span><br/><span data-ttu-id="91732-117">*Souhaitée*</span><span class="sxs-lookup"><span data-stu-id="91732-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91732-118">Notes</span><span class="sxs-lookup"><span data-stu-id="91732-118">Remarks</span></span>

<span data-ttu-id="91732-119">Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="91732-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="91732-120">Les MFTs synchrones n’envoient jamais cet événement.</span><span class="sxs-lookup"><span data-stu-id="91732-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="91732-121">Lorsque le client de la MFT reçoit cet événement, il doit appeler [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) pour fournir l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="91732-121">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) to deliver the next sample.</span></span> <span data-ttu-id="91732-122">L’attribut d' [ \_ \_ \_ \_ \_ ID de flux d’entrée MFT de l’événement MF](mf-event-mft-input-stream-id.md) de l’objet d’événement spécifie le flux d’entrée qui requiert des données.</span><span class="sxs-lookup"><span data-stu-id="91732-122">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event object specifies which input stream requires data.</span></span>

## <a name="requirements"></a><span data-ttu-id="91732-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91732-123">Requirements</span></span>



| <span data-ttu-id="91732-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91732-124">Requirement</span></span> | <span data-ttu-id="91732-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="91732-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91732-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91732-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91732-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91732-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="91732-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91732-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91732-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91732-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="91732-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="91732-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="91732-131"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91732-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91732-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91732-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91732-133">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91732-133">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="91732-134">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="91732-134">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




