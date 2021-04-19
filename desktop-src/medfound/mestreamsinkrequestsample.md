---
description: Déclenché par un récepteur de flux pour demander un nouvel échantillon de média à partir du pipeline.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Événement MEStreamSinkRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519809"
---
# <a name="mestreamsinkrequestsample-event"></a><span data-ttu-id="ba998-103">Événement MEStreamSinkRequestSample</span><span class="sxs-lookup"><span data-stu-id="ba998-103">MEStreamSinkRequestSample event</span></span>

<span data-ttu-id="ba998-104">Déclenché par un récepteur de flux pour demander un nouvel échantillon de média à partir du pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba998-104">Raised by a stream sink to request a new media sample from the pipeline.</span></span> <span data-ttu-id="ba998-105">Pour chaque événement MEStreamSinkRequestSample, le pipeline demande des données à partir du composant en amont suivant.</span><span class="sxs-lookup"><span data-stu-id="ba998-105">For each MEStreamSinkRequestSample event, the pipeline requests data from the next upstream component.</span></span>

## <a name="event-values"></a><span data-ttu-id="ba998-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="ba998-106">Event values</span></span>

<span data-ttu-id="ba998-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba998-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ba998-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ba998-108">VARTYPE</span></span>              | <span data-ttu-id="ba998-109">Description</span><span class="sxs-lookup"><span data-stu-id="ba998-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ba998-110">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="ba998-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ba998-111">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="ba998-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ba998-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba998-112">Requirements</span></span>



| <span data-ttu-id="ba998-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba998-113">Requirement</span></span> | <span data-ttu-id="ba998-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba998-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba998-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba998-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ba998-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba998-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ba998-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba998-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ba998-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba998-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ba998-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba998-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba998-120"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba998-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba998-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba998-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba998-122">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba998-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ba998-123">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="ba998-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




