---
description: Déclenché par un récepteur de flux lorsque le type de média récepteur n’est plus valide.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Événement MEStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201996"
---
# <a name="mestreamsinkformatchanged-event"></a><span data-ttu-id="c0614-103">Événement MEStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="c0614-103">MEStreamSinkFormatChanged event</span></span>

<span data-ttu-id="c0614-104">Déclenché par un récepteur de flux lorsque le type de média du récepteur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="c0614-104">Raised by a stream sink when the sink's media type is no longer valid.</span></span>

## <a name="event-values"></a><span data-ttu-id="c0614-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="c0614-105">Event values</span></span>

<span data-ttu-id="c0614-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0614-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c0614-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c0614-107">VARTYPE</span></span>              | <span data-ttu-id="c0614-108">Description</span><span class="sxs-lookup"><span data-stu-id="c0614-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c0614-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="c0614-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c0614-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="c0614-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c0614-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c0614-111">Remarks</span></span>

<span data-ttu-id="c0614-112">Un récepteur de flux peut déclencher cela même si un événement invalide le type de média du récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="c0614-112">A stream sink can raise this even if something happens that invalidates the stream sink's media type.</span></span> <span data-ttu-id="c0614-113">Par exemple, le convertisseur vidéo amélioré (EVR) envoie cet événement lorsque l’affichage change.</span><span class="sxs-lookup"><span data-stu-id="c0614-113">For example, the enhanced video renderer (EVR) sends this event when the display changes.</span></span>

<span data-ttu-id="c0614-114">La valeur **HRESULT** récupérée par [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) peut indiquer la raison pour laquelle le type de média n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="c0614-114">The **HRESULT** value retrieved by [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) might indicate why the media type is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0614-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0614-115">Requirements</span></span>



| <span data-ttu-id="c0614-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0614-116">Requirement</span></span> | <span data-ttu-id="c0614-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0614-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0614-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0614-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0614-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0614-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0614-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0614-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0614-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0614-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c0614-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0614-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0614-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0614-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0614-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0614-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0614-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0614-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="c0614-126">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="c0614-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




