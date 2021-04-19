---
description: Signale le début de chaque unité d’objet vidéo (VOBU), un segment vidéo d’une longueur de 0,4 à 1,0 secondes.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532604"
---
# <a name="ec_dvd_current_time"></a><span data-ttu-id="0a9e4-103">\_ \_ heure actuelle du DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="0a9e4-103">EC\_DVD\_CURRENT\_TIME</span></span>

<span data-ttu-id="0a9e4-104">Signale le début de chaque unité d’objet vidéo (VOBU), un segment vidéo d’une longueur de 0,4 à 1,0 secondes.</span><span class="sxs-lookup"><span data-stu-id="0a9e4-104">Signals the beginning of every video object unit (VOBU), a video segment which is 0.4 to 1.0 seconds in length.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a9e4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a9e4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a9e4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0a9e4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0a9e4-107">Valeur **DWORD** qui indique le code temporel de lecture actuel dans une mise en forme binaire codée binaire (BCD), minutes, secondes, frames (hh : mm : SS : FF).</span><span class="sxs-lookup"><span data-stu-id="0a9e4-107">**DWORD** value indicating the current playback timecode in a binary coded decimal (BCD) hours, minutes, seconds, frames (HH:MM:SS:FF) format.</span></span> <span data-ttu-id="0a9e4-108">Membre de la structure du [**\_ code temporel du DVD**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .</span><span class="sxs-lookup"><span data-stu-id="0a9e4-108">Member of the [**DVD\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a9e4-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0a9e4-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0a9e4-110">Valeur booléenne (**bool**) indiquant le code temporel.</span><span class="sxs-lookup"><span data-stu-id="0a9e4-110">Boolean (**BOOL**) value indicating the timecode.</span></span> <span data-ttu-id="0a9e4-111">Zéro (0) indique 25 images par seconde, tandis que 1 indique 30 images par seconde (non supprimées).</span><span class="sxs-lookup"><span data-stu-id="0a9e4-111">Zero (0) indicates 25 frames per second while 1 indicates 30 frames per second (nondropped).</span></span> <span data-ttu-id="0a9e4-112">La valeur 2 indique que l’heure de lecture ne peut pas être déterminée.</span><span class="sxs-lookup"><span data-stu-id="0a9e4-112">A value of 2 indicates the playback time cannot be determined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a9e4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0a9e4-113">Remarks</span></span>

<span data-ttu-id="0a9e4-114">Seuls les films linéaires simples signalent cet événement.</span><span class="sxs-lookup"><span data-stu-id="0a9e4-114">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="0a9e4-115">Cet événement est déclenché dans le domaine de titre.</span><span class="sxs-lookup"><span data-stu-id="0a9e4-115">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9e4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a9e4-116">Requirements</span></span>



| <span data-ttu-id="0a9e4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a9e4-117">Requirement</span></span> | <span data-ttu-id="0a9e4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a9e4-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9e4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a9e4-119">Header</span></span><br/> | <dl> <span data-ttu-id="0a9e4-120"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a9e4-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a9e4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a9e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9e4-122">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="0a9e4-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="0a9e4-123">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="0a9e4-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0a9e4-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a9e4-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




