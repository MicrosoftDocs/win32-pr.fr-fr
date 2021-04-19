---
description: 'Envoyé lorsqu’un flux de média remet un nouvel exemple en réponse à un appel à IMFMediaStream :: RequestSample.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Événement MEMediaSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524771"
---
# <a name="memediasample-event"></a><span data-ttu-id="4d303-103">Événement MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="4d303-103">MEMediaSample event</span></span>

<span data-ttu-id="4d303-104">Envoyé lorsqu’un flux de média remet un nouvel exemple en réponse à un appel à [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="4d303-104">Sent when a media stream delivers a new sample in response to a call to [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span>

## <a name="event-values"></a><span data-ttu-id="4d303-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="4d303-105">Event values</span></span>

<span data-ttu-id="4d303-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d303-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4d303-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4d303-107">VARTYPE</span></span>                | <span data-ttu-id="4d303-108">Description</span><span class="sxs-lookup"><span data-stu-id="4d303-108">Description</span></span>                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d303-109">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="4d303-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="4d303-110">Pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="4d303-110">Pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of the sample.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="4d303-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d303-111">Requirements</span></span>



| <span data-ttu-id="4d303-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d303-112">Requirement</span></span> | <span data-ttu-id="4d303-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d303-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d303-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d303-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4d303-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d303-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4d303-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d303-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4d303-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d303-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4d303-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d303-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d303-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d303-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d303-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d303-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d303-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4d303-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4d303-122">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="4d303-122">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 




