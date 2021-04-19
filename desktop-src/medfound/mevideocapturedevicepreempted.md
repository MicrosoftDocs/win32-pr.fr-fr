---
description: Envoyé par le IMFMediaSource qui encapsule l’appareil pour indiquer que l’appareil a été devancé.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Événement MEVideoCaptureDevicePreempted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529746"
---
# <a name="mevideocapturedevicepreempted-event"></a><span data-ttu-id="47e51-103">Événement MEVideoCaptureDevicePreempted</span><span class="sxs-lookup"><span data-stu-id="47e51-103">MEVideoCaptureDevicePreempted event</span></span>

<span data-ttu-id="47e51-104">Envoyé par le [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) qui encapsule l’appareil pour indiquer que l’appareil a été devancé.</span><span class="sxs-lookup"><span data-stu-id="47e51-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been preempted.</span></span>

## <a name="event-values"></a><span data-ttu-id="47e51-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="47e51-105">Event values</span></span>

<span data-ttu-id="47e51-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="47e51-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="47e51-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="47e51-107">VARTYPE</span></span>               | <span data-ttu-id="47e51-108">Description</span><span class="sxs-lookup"><span data-stu-id="47e51-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="47e51-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="47e51-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="47e51-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="47e51-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="47e51-111">Notes</span><span class="sxs-lookup"><span data-stu-id="47e51-111">Remarks</span></span>

<span data-ttu-id="47e51-112">Cet événement est envoyé par le [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) qui encapsule l’appareil.</span><span class="sxs-lookup"><span data-stu-id="47e51-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e51-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47e51-113">Requirements</span></span>



| <span data-ttu-id="47e51-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47e51-114">Requirement</span></span> | <span data-ttu-id="47e51-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47e51-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e51-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47e51-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47e51-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47e51-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="47e51-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47e51-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47e51-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47e51-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="47e51-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="47e51-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e51-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47e51-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47e51-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47e51-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e51-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47e51-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




