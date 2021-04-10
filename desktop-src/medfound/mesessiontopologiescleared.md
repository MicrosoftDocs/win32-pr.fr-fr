---
description: 'Déclenché par la session multimédia lorsque la méthode IMFMediaSession :: ClearTopologies se termine de façon asynchrone.'
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: Événement MESessionTopologiesCleared (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551e98607a8d23d9333527337bbd7d038ed0b340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114618"
---
# <a name="mesessiontopologiescleared-event"></a><span data-ttu-id="ca603-103">Événement MESessionTopologiesCleared</span><span class="sxs-lookup"><span data-stu-id="ca603-103">MESessionTopologiesCleared event</span></span>

<span data-ttu-id="ca603-104">Déclenché par la session multimédia lorsque la méthode [**IMFMediaSession :: ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ca603-104">Raised by the Media Session when the [**IMFMediaSession::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ca603-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="ca603-105">Event values</span></span>

<span data-ttu-id="ca603-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca603-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ca603-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ca603-107">VARTYPE</span></span>              | <span data-ttu-id="ca603-108">Description</span><span class="sxs-lookup"><span data-stu-id="ca603-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ca603-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="ca603-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ca603-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="ca603-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ca603-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca603-111">Requirements</span></span>



| <span data-ttu-id="ca603-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca603-112">Requirement</span></span> | <span data-ttu-id="ca603-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca603-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca603-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca603-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ca603-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca603-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ca603-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca603-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ca603-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca603-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ca603-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca603-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca603-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca603-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca603-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca603-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca603-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca603-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




