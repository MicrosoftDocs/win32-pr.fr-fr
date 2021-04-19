---
description: Déclenché par les récepteurs de flux du convertisseur vidéo amélioré (EVR) si le périphérique vidéo change.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Événement MEStreamSinkDeviceChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516917"
---
# <a name="mestreamsinkdevicechanged-event"></a><span data-ttu-id="dc494-103">Événement MEStreamSinkDeviceChanged</span><span class="sxs-lookup"><span data-stu-id="dc494-103">MEStreamSinkDeviceChanged event</span></span>

<span data-ttu-id="dc494-104">Déclenché par les récepteurs de flux du convertisseur vidéo amélioré (EVR) si le périphérique vidéo change.</span><span class="sxs-lookup"><span data-stu-id="dc494-104">Raised by the stream sinks of the enhanced video renderer (EVR) if the video device changes.</span></span> <span data-ttu-id="dc494-105">Par exemple, le EVR déclenche cet événement lorsqu’il reçoit un événement de [**\_ \_ modification d’affichage EC**](../directshow/ec-display-changed.md) .</span><span class="sxs-lookup"><span data-stu-id="dc494-105">For example, the EVR raises this event when it receives an [**EC\_DISPLAY\_CHANGED**](../directshow/ec-display-changed.md) event.</span></span>

<span data-ttu-id="dc494-106">Le pipeline Media Foundation répond à cet événement en renvoyant tous les exemples de demandes qui ont échoué pendant la modification de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dc494-106">The Media Foundation pipeline responds to this event by resubmitting all sample requests that failed while the device was changing.</span></span>

## <a name="event-values"></a><span data-ttu-id="dc494-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="dc494-107">Event values</span></span>

<span data-ttu-id="dc494-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="dc494-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dc494-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dc494-109">VARTYPE</span></span>              | <span data-ttu-id="dc494-110">Description</span><span class="sxs-lookup"><span data-stu-id="dc494-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="dc494-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="dc494-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="dc494-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="dc494-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="dc494-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc494-113">Requirements</span></span>



| <span data-ttu-id="dc494-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc494-114">Requirement</span></span> | <span data-ttu-id="dc494-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc494-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc494-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc494-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc494-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc494-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc494-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc494-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc494-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc494-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc494-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc494-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc494-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc494-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc494-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc494-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc494-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc494-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="dc494-124">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="dc494-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 
