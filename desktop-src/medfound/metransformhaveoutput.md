---
description: Envoyé par une transformation de Media Foundation asynchrone (MFT) quand de nouvelles données de sortie sont disponibles à partir de la table MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Événement METransformHaveOutput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517543"
---
# <a name="metransformhaveoutput-event"></a><span data-ttu-id="f795c-103">Événement METransformHaveOutput</span><span class="sxs-lookup"><span data-stu-id="f795c-103">METransformHaveOutput event</span></span>

<span data-ttu-id="f795c-104">Envoyé par une transformation de Media Foundation asynchrone (MFT) quand de nouvelles données de sortie sont disponibles à partir de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="f795c-104">Sent by an asynchronous Media Foundation transform (MFT) when new output data is available from the MFT.</span></span>

## <a name="event-values"></a><span data-ttu-id="f795c-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="f795c-105">Event values</span></span>

<span data-ttu-id="f795c-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="f795c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f795c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f795c-107">VARTYPE</span></span>              | <span data-ttu-id="f795c-108">Description</span><span class="sxs-lookup"><span data-stu-id="f795c-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="f795c-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="f795c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f795c-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="f795c-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="f795c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="f795c-111">Attributes</span></span>

<span data-ttu-id="f795c-112">Aucun attribut n’est défini pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="f795c-112">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="f795c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f795c-113">Remarks</span></span>

<span data-ttu-id="f795c-114">Les MFTs asynchrones envoient cet événement par le biais de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="f795c-114">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="f795c-115">Les MFTs synchrones n’envoient jamais cet événement.</span><span class="sxs-lookup"><span data-stu-id="f795c-115">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="f795c-116">Lorsque le client de la MFT reçoit cet événement, il doit appeler [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour récupérer la sortie.</span><span class="sxs-lookup"><span data-stu-id="f795c-116">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get the output.</span></span>

## <a name="requirements"></a><span data-ttu-id="f795c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f795c-117">Requirements</span></span>



| <span data-ttu-id="f795c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f795c-118">Requirement</span></span> | <span data-ttu-id="f795c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f795c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f795c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f795c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f795c-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f795c-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f795c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f795c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f795c-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f795c-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="f795c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f795c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f795c-125"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f795c-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f795c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f795c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f795c-127">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f795c-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f795c-128">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="f795c-128">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




