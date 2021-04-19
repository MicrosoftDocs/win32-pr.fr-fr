---
description: 'Déclenché quand une source multimédia cherche à une nouvelle position. Une source de média déclenche cet événement si la source est en cours d’exécution ou en pause et que l’application appelle IMFMediaSource :: Start avec une heure de début qui n’est pas égale à la position actuelle.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Événement MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524481"
---
# <a name="mesourceseeked-event"></a><span data-ttu-id="d735a-104">Événement MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="d735a-104">MESourceSeeked event</span></span>

<span data-ttu-id="d735a-105">Déclenché quand une source multimédia cherche à une nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="d735a-105">Raised when a media source seeks to a new position.</span></span> <span data-ttu-id="d735a-106">Une source de média déclenche cet événement si la source est en cours d’exécution ou en pause et que l’application appelle [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) avec une heure de début qui n’est pas égale à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d735a-106">A media source raises this event if the source is running or paused and the application calls [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) with a start time that does not equal the current position.</span></span>

## <a name="event-values"></a><span data-ttu-id="d735a-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="d735a-107">Event values</span></span>

<span data-ttu-id="d735a-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="d735a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d735a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d735a-109">VARTYPE</span></span>           | <span data-ttu-id="d735a-110">Description</span><span class="sxs-lookup"><span data-stu-id="d735a-110">Description</span></span>                                                                |
|-------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="d735a-111">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="d735a-111">VT\_I8</span></span><br/> | <span data-ttu-id="d735a-112">Nouvelle position de départ, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="d735a-112">The new starting position, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d735a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d735a-113">Requirements</span></span>



| <span data-ttu-id="d735a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d735a-114">Requirement</span></span> | <span data-ttu-id="d735a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d735a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d735a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d735a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d735a-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d735a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d735a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d735a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d735a-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d735a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d735a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d735a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d735a-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d735a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d735a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d735a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d735a-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d735a-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




