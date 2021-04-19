---
description: 'Déclenché par un flux de média lorsque la méthode IMFMediaSource :: STOP se termine de façon asynchrone.'
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: Événement MEStreamStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541854"
---
# <a name="mestreamstopped-event"></a><span data-ttu-id="a3d4b-103">Événement MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="a3d4b-103">MEStreamStopped event</span></span>

<span data-ttu-id="a3d4b-104">Déclenché par un flux de média lorsque la méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a3d4b-104">Raised by a media stream when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="a3d4b-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="a3d4b-105">Event values</span></span>

<span data-ttu-id="a3d4b-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3d4b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a3d4b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a3d4b-107">VARTYPE</span></span>              | <span data-ttu-id="a3d4b-108">Description</span><span class="sxs-lookup"><span data-stu-id="a3d4b-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a3d4b-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="a3d4b-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a3d4b-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="a3d4b-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a3d4b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a3d4b-111">Remarks</span></span>

<span data-ttu-id="a3d4b-112">Chaque flux actif dans la présentation envoie cet événement.</span><span class="sxs-lookup"><span data-stu-id="a3d4b-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d4b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3d4b-113">Requirements</span></span>



| <span data-ttu-id="a3d4b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3d4b-114">Requirement</span></span> | <span data-ttu-id="a3d4b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3d4b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d4b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3d4b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a3d4b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3d4b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a3d4b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3d4b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a3d4b-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3d4b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3d4b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3d4b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3d4b-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3d4b-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d4b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3d4b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d4b-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3d4b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




