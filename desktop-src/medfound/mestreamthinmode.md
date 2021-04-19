---
description: Déclenché par un flux multimédia lorsqu’il démarre ou arrête l’affinage du flux. Pour plus d’informations sur la réduction, consultez à propos du contrôle du taux.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Événement MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519602"
---
# <a name="mestreamthinmode-event"></a><span data-ttu-id="21fa5-104">Événement MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="21fa5-104">MEStreamThinMode event</span></span>

<span data-ttu-id="21fa5-105">Déclenché par un flux multimédia lorsqu’il démarre ou arrête l’affinage du flux.</span><span class="sxs-lookup"><span data-stu-id="21fa5-105">Raised by a media stream when it starts or stops thinning the stream.</span></span> <span data-ttu-id="21fa5-106">Pour plus d' *informations sur la réduction, consultez* [à propos du contrôle du taux](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="21fa5-106">For information about *thinning*, see [About Rate Control](about-rate-control.md).</span></span>

<span data-ttu-id="21fa5-107">Cet événement peut être envoyé en réponse à la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) seou à la méthode [**IMFQualityAdvise :: SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .</span><span class="sxs-lookup"><span data-stu-id="21fa5-107">This event can be sent in response to the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method or the [**IMFQualityAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="21fa5-108">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="21fa5-108">Event values</span></span>

<span data-ttu-id="21fa5-109">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="21fa5-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21fa5-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="21fa5-110">VARTYPE</span></span></th>
<th><span data-ttu-id="21fa5-111">Description</span><span class="sxs-lookup"><span data-stu-id="21fa5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21fa5-112">VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="21fa5-112">VT_BOOL</span></span><br/></td>
<td><span data-ttu-id="21fa5-113">Indique si l’affinage a démarré ou s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="21fa5-113">Indicates whether thinning has started or stopped.</span></span><br/>
<ul>
<li><span data-ttu-id="21fa5-114">VARIANT_TRUE : les exemples fournis après cet événement sont éclaircis.</span><span class="sxs-lookup"><span data-stu-id="21fa5-114">VARIANT_TRUE: Samples delivered after this event are thinned.</span></span></li>
<li><span data-ttu-id="21fa5-115">VARIANT_FALSE : les exemples fournis après cet événement ne sont pas éclaircis.</span><span class="sxs-lookup"><span data-stu-id="21fa5-115">VARIANT_FALSE: Samples delivered after this event are not thinned.</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="21fa5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21fa5-116">Requirements</span></span>



| <span data-ttu-id="21fa5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21fa5-117">Requirement</span></span> | <span data-ttu-id="21fa5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="21fa5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21fa5-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21fa5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="21fa5-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21fa5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="21fa5-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21fa5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="21fa5-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21fa5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21fa5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="21fa5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="21fa5-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21fa5-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21fa5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21fa5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21fa5-126">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21fa5-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




