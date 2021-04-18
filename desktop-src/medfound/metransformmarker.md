---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) en réponse à un \_ message de marque de commande de message MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Événement METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533800"
---
# <a name="metransformmarker-event"></a><span data-ttu-id="cc51c-103">Événement METransformMarker</span><span class="sxs-lookup"><span data-stu-id="cc51c-103">METransformMarker event</span></span>

<span data-ttu-id="cc51c-104">Envoyé par une transformation de Media Foundation asynchrone (MFT) en réponse à un message de **\_ marque de \_ commande \_ de message MFT** .</span><span class="sxs-lookup"><span data-stu-id="cc51c-104">Sent by an asynchronous Media Foundation transform (MFT) in response to an **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span>

## <a name="event-values"></a><span data-ttu-id="cc51c-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="cc51c-105">Event values</span></span>

<span data-ttu-id="cc51c-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc51c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cc51c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc51c-107">VARTYPE</span></span>              | <span data-ttu-id="cc51c-108">Description</span><span class="sxs-lookup"><span data-stu-id="cc51c-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="cc51c-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="cc51c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="cc51c-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="cc51c-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="cc51c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="cc51c-111">Attributes</span></span>

<span data-ttu-id="cc51c-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="cc51c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="cc51c-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="cc51c-113">Attribute</span></span>                                                      | <span data-ttu-id="cc51c-114">Description</span><span class="sxs-lookup"><span data-stu-id="cc51c-114">Description</span></span>                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc51c-115">\_ \_ contexte MFT de l’événement MF \_</span><span class="sxs-lookup"><span data-stu-id="cc51c-115">MF\_EVENT\_MFT\_CONTEXT</span></span>](mf-event-mft-context.md)<br/> | <span data-ttu-id="cc51c-116">Valeur du paramètre *ulParam* du message de **\_ \_ \_ marqueur de commande du message MFT** .</span><span class="sxs-lookup"><span data-stu-id="cc51c-116">The value of the *ulParam* parameter from the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span><br/><span data-ttu-id="cc51c-117">*Souhaitée*</span><span class="sxs-lookup"><span data-stu-id="cc51c-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cc51c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cc51c-118">Remarks</span></span>

<span data-ttu-id="cc51c-119">Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="cc51c-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="cc51c-120">Les MFTs synchrones n’envoient jamais cet événement.</span><span class="sxs-lookup"><span data-stu-id="cc51c-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="cc51c-121">Le client d’une table MFT asynchrone peut placer un marqueur dans le flux en appelant [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de **\_ \_ \_ marqueur de commande de message MFT** .</span><span class="sxs-lookup"><span data-stu-id="cc51c-121">The client of an asynchronous MFT can place a marker in the stream by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span> <span data-ttu-id="cc51c-122">Le paramètre *ulParam* contient des données définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="cc51c-122">The *ulParam* parameter contains application-defined data.</span></span>

<span data-ttu-id="cc51c-123">Lorsque la table MFT termine le traitement de toutes les données d’entrée qui étaient disponibles au moment de l’appel de [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , la MFT met en file d’attente un événement METransformMarker.</span><span class="sxs-lookup"><span data-stu-id="cc51c-123">When the MFT finishes processing all of the input data that was available at the time of the [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) call, the MFT queues an METransformMarker event.</span></span> <span data-ttu-id="cc51c-124">L’attribut de [ \_ \_ \_ contexte MFT](mf-event-mft-context.md) de l’événement MF de l’événement contient la valeur du paramètre *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="cc51c-124">The [MF\_EVENT\_MFT\_CONTEXT](mf-event-mft-context.md) attribute of the event contains the value of the *ulParam* parameter.</span></span> <span data-ttu-id="cc51c-125">Pour plus d’informations, consultez [MFTS asynchrone](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="cc51c-125">For more information, see [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc51c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc51c-126">Requirements</span></span>



| <span data-ttu-id="cc51c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc51c-127">Requirement</span></span> | <span data-ttu-id="cc51c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc51c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc51c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc51c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cc51c-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc51c-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="cc51c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc51c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cc51c-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc51c-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="cc51c-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc51c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc51c-134"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc51c-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc51c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc51c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc51c-136">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc51c-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="cc51c-137">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="cc51c-137">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




