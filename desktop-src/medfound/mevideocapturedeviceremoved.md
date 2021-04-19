---
description: Envoyé par le IMFMediaSource qui encapsule l’appareil pour indiquer que l’appareil a été supprimé.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Événement MEVideoCaptureDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529321"
---
# <a name="mevideocapturedeviceremoved-event"></a><span data-ttu-id="7b3d6-103">Événement MEVideoCaptureDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="7b3d6-103">MEVideoCaptureDeviceRemoved event</span></span>

<span data-ttu-id="7b3d6-104">Envoyé par le [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) qui encapsule l’appareil pour indiquer que l’appareil a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="7b3d6-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="7b3d6-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="7b3d6-105">Event values</span></span>

<span data-ttu-id="7b3d6-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b3d6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7b3d6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7b3d6-107">VARTYPE</span></span>               | <span data-ttu-id="7b3d6-108">Description</span><span class="sxs-lookup"><span data-stu-id="7b3d6-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="7b3d6-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="7b3d6-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="7b3d6-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="7b3d6-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7b3d6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7b3d6-111">Remarks</span></span>

<span data-ttu-id="7b3d6-112">Cet événement est envoyé par le [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) qui encapsule l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7b3d6-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3d6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b3d6-113">Requirements</span></span>



| <span data-ttu-id="7b3d6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b3d6-114">Requirement</span></span> | <span data-ttu-id="7b3d6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b3d6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3d6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b3d6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7b3d6-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b3d6-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="7b3d6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b3d6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7b3d6-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b3d6-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b3d6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b3d6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b3d6-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d6-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3d6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b3d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3d6-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b3d6-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




