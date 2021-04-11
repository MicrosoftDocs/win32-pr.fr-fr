---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) lorsqu’une opération de drainage est terminée.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Événement METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320474"
---
# <a name="metransformdraincomplete-event"></a><span data-ttu-id="2fa29-103">Événement METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="2fa29-103">METransformDrainComplete event</span></span>

<span data-ttu-id="2fa29-104">Envoyé par une transformation de Media Foundation asynchrone (MFT) lorsqu’une opération de drainage est terminée.</span><span class="sxs-lookup"><span data-stu-id="2fa29-104">Sent by an asynchronous Media Foundation transform (MFT) when a drain operation is complete.</span></span>

## <a name="event-values"></a><span data-ttu-id="2fa29-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="2fa29-105">Event values</span></span>

<span data-ttu-id="2fa29-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="2fa29-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2fa29-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2fa29-107">VARTYPE</span></span>              | <span data-ttu-id="2fa29-108">Description</span><span class="sxs-lookup"><span data-stu-id="2fa29-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="2fa29-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="2fa29-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2fa29-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="2fa29-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="2fa29-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="2fa29-111">Attributes</span></span>

<span data-ttu-id="2fa29-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="2fa29-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="2fa29-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="2fa29-113">Attribute</span></span>                                                                        | <span data-ttu-id="2fa29-114">Description</span><span class="sxs-lookup"><span data-stu-id="2fa29-114">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="2fa29-115">\_ID de \_ \_ flux d’entrée MFT \_ \_ de l’événement MF</span><span class="sxs-lookup"><span data-stu-id="2fa29-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="2fa29-116">Identificateur du flux qui a été vidé.</span><span class="sxs-lookup"><span data-stu-id="2fa29-116">The identifier of the stream that was drained.</span></span><br/><span data-ttu-id="2fa29-117">*Souhaitée*</span><span class="sxs-lookup"><span data-stu-id="2fa29-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2fa29-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2fa29-118">Remarks</span></span>

<span data-ttu-id="2fa29-119">Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="2fa29-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="2fa29-120">Les MFTs synchrones n’envoient jamais cet événement.</span><span class="sxs-lookup"><span data-stu-id="2fa29-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="2fa29-121">Pour vider une table MFT, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de **drainage de \_ \_ commande \_ de message MFT** .</span><span class="sxs-lookup"><span data-stu-id="2fa29-121">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_DRAIN** message.</span></span> <span data-ttu-id="2fa29-122">Spécifiez le flux d’entrée à purger dans le paramètre *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="2fa29-122">Specify the input stream to drain in the *ulParam* parameter.</span></span> <span data-ttu-id="2fa29-123">Lorsque l’opération de drainage est terminée, une table MFT asynchrone envoie l’événement METransformDrainComplete.</span><span class="sxs-lookup"><span data-stu-id="2fa29-123">When the drain operation is completed, an asynchronous MFT sends the METransformDrainComplete event.</span></span> <span data-ttu-id="2fa29-124">L’attribut d' [ \_ \_ \_ \_ \_ ID de flux d’entrée MFT d’événement MF](mf-event-mft-input-stream-id.md) de l’événement contient l’identificateur de flux fourni dans le paramètre *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="2fa29-124">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event contains the stream identifier given in the *ulParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa29-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fa29-125">Requirements</span></span>



| <span data-ttu-id="2fa29-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fa29-126">Requirement</span></span> | <span data-ttu-id="2fa29-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fa29-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa29-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fa29-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa29-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fa29-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="2fa29-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fa29-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa29-131">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fa29-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="2fa29-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fa29-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fa29-133"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fa29-133"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa29-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fa29-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa29-135">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2fa29-135">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="2fa29-136">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="2fa29-136">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




