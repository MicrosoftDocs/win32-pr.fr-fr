---
description: Déclenché par un récepteur de flux lorsque le flux a reçu suffisamment de données de pré-roll pour commencer le rendu. Cet événement est déclenché par les récepteurs multimédias qui prennent en charge l’interface IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Événement MEStreamSinkPrerolled (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754292"
---
# <a name="mestreamsinkprerolled-event"></a><span data-ttu-id="685b8-104">Événement MEStreamSinkPrerolled</span><span class="sxs-lookup"><span data-stu-id="685b8-104">MEStreamSinkPrerolled event</span></span>

<span data-ttu-id="685b8-105">Déclenché par un récepteur de flux lorsque le flux a reçu suffisamment de données de pré-roll pour commencer le rendu.</span><span class="sxs-lookup"><span data-stu-id="685b8-105">Raised by a stream sink when the stream has received enough pre-roll data to begin rendering.</span></span> <span data-ttu-id="685b8-106">Cet événement est déclenché par les récepteurs multimédias qui prennent en charge l’interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="685b8-106">This event is raised by media sinks that support the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="685b8-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="685b8-107">Event values</span></span>

<span data-ttu-id="685b8-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="685b8-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="685b8-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="685b8-109">VARTYPE</span></span>              | <span data-ttu-id="685b8-110">Description</span><span class="sxs-lookup"><span data-stu-id="685b8-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="685b8-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="685b8-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="685b8-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="685b8-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="685b8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="685b8-113">Requirements</span></span>



| <span data-ttu-id="685b8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="685b8-114">Requirement</span></span> | <span data-ttu-id="685b8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="685b8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685b8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="685b8-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685b8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="685b8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="685b8-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685b8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="685b8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="685b8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="685b8-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="685b8-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685b8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="685b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685b8-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="685b8-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="685b8-124">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="685b8-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




