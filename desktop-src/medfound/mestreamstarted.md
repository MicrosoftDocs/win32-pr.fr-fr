---
description: Déclenché par un flux de média lorsque la source démarre sans recherche. Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Événement MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538659"
---
# <a name="mestreamstarted-event"></a><span data-ttu-id="0b3ca-104">Événement MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="0b3ca-104">MEStreamStarted event</span></span>

<span data-ttu-id="0b3ca-105">Déclenché par un flux de média lorsque la source démarre sans recherche.</span><span class="sxs-lookup"><span data-stu-id="0b3ca-105">Raised by a media stream when the source starts without seeking.</span></span> <span data-ttu-id="0b3ca-106">Un flux de média déclenche cet événement lorsque la source du média déclenche l’événement [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="0b3ca-106">A media stream raises this event when the media source raises the [MESourceStarted](mesourcestarted.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="0b3ca-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="0b3ca-107">Event values</span></span>

<span data-ttu-id="0b3ca-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0b3ca-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0b3ca-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0b3ca-109">VARTYPE</span></span>              | <span data-ttu-id="0b3ca-110">Description</span><span class="sxs-lookup"><span data-stu-id="0b3ca-110">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3ca-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="0b3ca-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0b3ca-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="0b3ca-112">No event data.</span></span><br/> <br/>                                                                          |
| <span data-ttu-id="0b3ca-113">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="0b3ca-113">VT\_I8</span></span><br/>    | <span data-ttu-id="0b3ca-114">Heure de début, en unités de 100 nanosecondes, par rapport aux horodatages sur les échantillons.</span><span class="sxs-lookup"><span data-stu-id="0b3ca-114">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0b3ca-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b3ca-115">Requirements</span></span>



| <span data-ttu-id="0b3ca-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b3ca-116">Requirement</span></span> | <span data-ttu-id="0b3ca-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b3ca-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3ca-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b3ca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b3ca-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b3ca-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b3ca-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b3ca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b3ca-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b3ca-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b3ca-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b3ca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b3ca-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b3ca-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b3ca-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b3ca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3ca-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b3ca-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




