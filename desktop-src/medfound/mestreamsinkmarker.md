---
description: Déclenché par un récepteur de flux après l’appel de la méthode IMFStreamSink ::P laceMarker.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Événement MEStreamSinkMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071d6e5b25873739c176d1c808929c26e1e338bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754293"
---
# <a name="mestreamsinkmarker-event"></a><span data-ttu-id="943b8-103">Événement MEStreamSinkMarker</span><span class="sxs-lookup"><span data-stu-id="943b8-103">MEStreamSinkMarker event</span></span>

<span data-ttu-id="943b8-104">Déclenché par un récepteur de flux après l’appel de la méthode [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="943b8-104">Raised by a stream sink after the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="943b8-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="943b8-105">Event values</span></span>

<span data-ttu-id="943b8-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="943b8-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="943b8-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="943b8-107">VARTYPE</span></span>            | <span data-ttu-id="943b8-108">Description</span><span class="sxs-lookup"><span data-stu-id="943b8-108">Description</span></span>                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943b8-109">>n’importe laquelle</span><span class="sxs-lookup"><span data-stu-id="943b8-109">>Any</span></span><br/> | <span data-ttu-id="943b8-110">La valeur de l’événement est une copie du **PROPVARIANT** que l’appelant a spécifié dans le paramètre *pvarContextValue* de la méthode [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="943b8-110">The event value is a copy of the **PROPVARIANT** that the caller specified in the *pvarContextValue* parameter of the [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="943b8-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="943b8-111">Requirements</span></span>



| <span data-ttu-id="943b8-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="943b8-112">Requirement</span></span> | <span data-ttu-id="943b8-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="943b8-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943b8-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="943b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="943b8-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="943b8-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="943b8-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="943b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="943b8-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="943b8-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="943b8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="943b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="943b8-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="943b8-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943b8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="943b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943b8-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="943b8-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="943b8-122">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="943b8-122">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




