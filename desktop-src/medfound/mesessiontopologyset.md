---
description: 'Déclenché après la fin asynchrone de la méthode IMFMediaSession :: SetTopology. La session multimédia déclenche cet événement après la résolution de la topologie en une topologie complète et la mise en file d’attente de la topologie pour la lecture.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Événement MESessionTopologySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951548"
---
# <a name="mesessiontopologyset-event"></a><span data-ttu-id="dfcb8-104">Événement MESessionTopologySet</span><span class="sxs-lookup"><span data-stu-id="dfcb8-104">MESessionTopologySet event</span></span>

<span data-ttu-id="dfcb8-105">Déclenché après la fin asynchrone de la méthode [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .</span><span class="sxs-lookup"><span data-stu-id="dfcb8-105">Raised after the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="dfcb8-106">La session multimédia déclenche cet événement après la résolution de la topologie en une topologie complète et la mise en file d’attente de la topologie pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-106">The Media Session raises this event after it resolves the topology into a full topology and queues the topology for playback.</span></span>

## <a name="event-values"></a><span data-ttu-id="dfcb8-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="dfcb8-107">Event values</span></span>

<span data-ttu-id="dfcb8-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dfcb8-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dfcb8-109">VARTYPE</span></span>                | <span data-ttu-id="dfcb8-110">Description</span><span class="sxs-lookup"><span data-stu-id="dfcb8-110">Description</span></span>                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcb8-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="dfcb8-111">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="dfcb8-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-112">No event data.</span></span><br/> <br/>                                                                    |
| <span data-ttu-id="dfcb8-113">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="dfcb8-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="dfcb8-114">Pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie complète.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-114">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the full topology.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="dfcb8-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="dfcb8-115">Examples</span></span>

<span data-ttu-id="dfcb8-116">L’exemple suivant récupère le pointeur [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) à partir d’un événement MESessionTopologySet.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-116">The following example retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from an MESessionTopologySet event.</span></span>


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="dfcb8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfcb8-117">Requirements</span></span>



| <span data-ttu-id="dfcb8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfcb8-118">Requirement</span></span> | <span data-ttu-id="dfcb8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcb8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcb8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfcb8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dfcb8-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfcb8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dfcb8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfcb8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dfcb8-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfcb8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dfcb8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfcb8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfcb8-125"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfcb8-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfcb8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfcb8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfcb8-127">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dfcb8-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




