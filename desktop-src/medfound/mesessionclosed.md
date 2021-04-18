---
description: 'Déclenché lorsque la méthode IMFMediaSession :: Close se termine de façon asynchrone.'
ms.assetid: d1056ce7-5527-428a-8ace-e1c10a2124a5
title: Événement MESessionClosed (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49591e602c06a9beae616ff2a88a2a71241b6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519812"
---
# <a name="mesessionclosed-event"></a><span data-ttu-id="33f4e-103">Événement MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="33f4e-103">MESessionClosed event</span></span>

<span data-ttu-id="33f4e-104">Déclenché lorsque la méthode [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="33f4e-104">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="33f4e-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="33f4e-105">Event values</span></span>

<span data-ttu-id="33f4e-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="33f4e-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="33f4e-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="33f4e-107">VARTYPE</span></span>              | <span data-ttu-id="33f4e-108">Description</span><span class="sxs-lookup"><span data-stu-id="33f4e-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="33f4e-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="33f4e-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="33f4e-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="33f4e-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="33f4e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33f4e-111">Requirements</span></span>



| <span data-ttu-id="33f4e-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33f4e-112">Requirement</span></span> | <span data-ttu-id="33f4e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="33f4e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f4e-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33f4e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="33f4e-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33f4e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="33f4e-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33f4e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="33f4e-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33f4e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33f4e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="33f4e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="33f4e-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33f4e-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f4e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33f4e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f4e-121">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33f4e-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




