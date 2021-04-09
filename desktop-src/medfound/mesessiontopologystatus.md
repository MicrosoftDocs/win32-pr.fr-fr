---
description: Déclenché par la session multimédia lorsque l’état d’une topologie change.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Événement MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951549"
---
# <a name="mesessiontopologystatus-event"></a><span data-ttu-id="cc53d-103">Événement MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="cc53d-103">MESessionTopologyStatus event</span></span>

<span data-ttu-id="cc53d-104">Déclenché par la session multimédia lorsque l’état d’une topologie change.</span><span class="sxs-lookup"><span data-stu-id="cc53d-104">Raised by the Media Session when the status of a topology changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="cc53d-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="cc53d-105">Event values</span></span>

<span data-ttu-id="cc53d-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc53d-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cc53d-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc53d-107">VARTYPE</span></span>                | <span data-ttu-id="cc53d-108">Description</span><span class="sxs-lookup"><span data-stu-id="cc53d-108">Description</span></span>                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc53d-109">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="cc53d-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="cc53d-110">Pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie.</span><span class="sxs-lookup"><span data-stu-id="cc53d-110">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="cc53d-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="cc53d-111">Attributes</span></span>

<span data-ttu-id="cc53d-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="cc53d-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="cc53d-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="cc53d-113">Attribute</span></span>                                                                            | <span data-ttu-id="cc53d-114">Description</span><span class="sxs-lookup"><span data-stu-id="cc53d-114">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="cc53d-115">**État de la \_ topologie des événements MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc53d-115">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)<br/> | <span data-ttu-id="cc53d-116">Spécifie le nouvel état de la topologie.</span><span class="sxs-lookup"><span data-stu-id="cc53d-116">Specifies the new status of the topology.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cc53d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cc53d-117">Remarks</span></span>

<span data-ttu-id="cc53d-118">Pour obtenir un exemple de code qui récupère le pointeur [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) à partir de l’événement, consultez événement [MESessionTopologySet](mesessiontopologyset.md) .</span><span class="sxs-lookup"><span data-stu-id="cc53d-118">For a code example that retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from the event, see [MESessionTopologySet](mesessiontopologyset.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc53d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc53d-119">Requirements</span></span>



| <span data-ttu-id="cc53d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc53d-120">Requirement</span></span> | <span data-ttu-id="cc53d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc53d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc53d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc53d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cc53d-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc53d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cc53d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc53d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cc53d-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc53d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cc53d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc53d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc53d-127"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc53d-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc53d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc53d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc53d-129">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc53d-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




