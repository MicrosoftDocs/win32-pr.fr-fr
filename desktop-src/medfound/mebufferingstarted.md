---
description: Signale qu’une source de média a commencé à mettre des données en mémoire tampon.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Événement MEBufferingStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518577"
---
# <a name="mebufferingstarted-event"></a><span data-ttu-id="eb8e0-103">Événement MEBufferingStarted</span><span class="sxs-lookup"><span data-stu-id="eb8e0-103">MEBufferingStarted event</span></span>

<span data-ttu-id="eb8e0-104">Signale qu’une source de média a commencé à mettre des données en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-104">Signals that a media source has started to buffer data.</span></span>

<span data-ttu-id="eb8e0-105">Une source de média peut envoyer cet événement si la source met en mémoire tampon des données pendant que la session multimédia est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-105">A media source can send this event if the source buffers data while the Media Session is running.</span></span> <span data-ttu-id="eb8e0-106">Lorsque la session multimédia reçoit cet événement, elle interrompt l’horloge de la présentation jusqu’à ce que la source du média envoie l’événement [MEBufferingStopped](mebufferingstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="eb8e0-106">When the Media Session receives this event, it pauses the presentation clock until the media source sends the [MEBufferingStopped](mebufferingstopped.md) event.</span></span> <span data-ttu-id="eb8e0-107">La session multimédia transmet également l’événement MEBufferingStarted à l’application.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-107">The Media Session also forwards the MEBufferingStarted event to the application.</span></span>

<span data-ttu-id="eb8e0-108">Les flux d’octets qui implémentent l’interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) envoient également cet événement.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-108">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="eb8e0-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="eb8e0-109">Event values</span></span>

<span data-ttu-id="eb8e0-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="eb8e0-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="eb8e0-111">VARTYPE</span></span>              | <span data-ttu-id="eb8e0-112">Description</span><span class="sxs-lookup"><span data-stu-id="eb8e0-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="eb8e0-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="eb8e0-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="eb8e0-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="eb8e0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="eb8e0-115">Remarks</span></span>

<span data-ttu-id="eb8e0-116">Si une source de média envoie l’événement MEBufferingStarted, elle doit envoyer l’événement [MEBufferingStopped](mebufferingstopped.md) lorsqu’elle arrête la mise en mémoire tampon des données.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-116">If a media source sends the MEBufferingStarted event, it must send the [MEBufferingStopped](mebufferingstopped.md) event when it stops buffering data.</span></span> <span data-ttu-id="eb8e0-117">La source du média doit envoyer un événement MEBufferingStopped correspondant pour chaque événement MEBufferingStarted.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-117">The media source must send a matching MEBufferingStopped event for every MEBufferingStarted event.</span></span> <span data-ttu-id="eb8e0-118">La source du média ne doit pas transférer ces événements avant l’appel de la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) de la source, ou après l’appel de la méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) de la source.</span><span class="sxs-lookup"><span data-stu-id="eb8e0-118">The media source should not forward these events before the source's [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called, or after the source's [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method is called.</span></span>

<span data-ttu-id="eb8e0-119">Si vous diffusez en continu à partir de la source réseau Media Foundation, vous pouvez obtenir la progression de la mise en mémoire tampon en interrogeant les statistiques **MFNETSOURCE \_ BUFFERPROGRESS \_ ID** .</span><span class="sxs-lookup"><span data-stu-id="eb8e0-119">If you are streaming from the Media Foundation network source, you can get the buffering progress by querying the **MFNETSOURCE\_BUFFERPROGRESS\_ID** statistic.</span></span> <span data-ttu-id="eb8e0-120">Pour plus d’informations, consultez [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="eb8e0-120">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="examples"></a><span data-ttu-id="eb8e0-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb8e0-121">Examples</span></span>


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="eb8e0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb8e0-122">Requirements</span></span>



| <span data-ttu-id="eb8e0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb8e0-123">Requirement</span></span> | <span data-ttu-id="eb8e0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb8e0-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8e0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb8e0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8e0-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb8e0-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eb8e0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb8e0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8e0-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb8e0-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb8e0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb8e0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb8e0-130"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb8e0-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb8e0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb8e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8e0-132">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb8e0-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="eb8e0-133">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb8e0-133">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




