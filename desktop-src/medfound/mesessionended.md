---
description: Déclenché par la session multimédia lorsqu’elle a fini de lire la dernière présentation dans la file d’attente de lecture.
ms.assetid: e593e51f-c239-49e9-bba8-c6d8238eff24
title: Événement MESessionEnded (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447b222be48dccc0f190329ab0bb6d56d09b266e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519811"
---
# <a name="mesessionended-event"></a><span data-ttu-id="55cdf-103">Événement MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="55cdf-103">MESessionEnded event</span></span>

<span data-ttu-id="55cdf-104">Déclenché par la session multimédia lorsqu’elle a fini de lire la dernière présentation dans la file d’attente de lecture.</span><span class="sxs-lookup"><span data-stu-id="55cdf-104">Raised by the Media Session when it has finished playing the last presentation in the playback queue.</span></span>

## <a name="event-values"></a><span data-ttu-id="55cdf-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="55cdf-105">Event values</span></span>

<span data-ttu-id="55cdf-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="55cdf-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="55cdf-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="55cdf-107">VARTYPE</span></span>              | <span data-ttu-id="55cdf-108">Description</span><span class="sxs-lookup"><span data-stu-id="55cdf-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="55cdf-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="55cdf-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="55cdf-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="55cdf-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="55cdf-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55cdf-111">Requirements</span></span>



| <span data-ttu-id="55cdf-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55cdf-112">Requirement</span></span> | <span data-ttu-id="55cdf-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="55cdf-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55cdf-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55cdf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="55cdf-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55cdf-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="55cdf-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55cdf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="55cdf-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55cdf-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="55cdf-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="55cdf-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="55cdf-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55cdf-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55cdf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55cdf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cdf-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55cdf-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




