---
description: Indique que la lecture du DVD a été arrêtée. Cet événement est envoyé lorsqu’un titre ou chapitre se termine et que le navigateur DVD ne trouve pas d’autres instructions de création de branche pour la lecture suivante. L’événement n’est pas envoyé lorsque l’application arrête la lecture.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545418"
---
# <a name="ec_dvd_playback_stopped"></a><span data-ttu-id="dae53-105">\_lecture du DVD EC \_ \_ arrêtée</span><span class="sxs-lookup"><span data-stu-id="dae53-105">EC\_DVD\_PLAYBACK\_STOPPED</span></span>

<span data-ttu-id="dae53-106">Indique que la lecture du DVD a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="dae53-106">Indicates that DVD playback has been stopped.</span></span> <span data-ttu-id="dae53-107">Cet événement est envoyé lorsqu’un titre ou chapitre se termine et que le [navigateur DVD](dvd-navigator-filter.md) ne trouve pas d’autres instructions de création de branche pour la lecture suivante.</span><span class="sxs-lookup"><span data-stu-id="dae53-107">This event is sent when a title or chapter completes and the [DVD Navigator](dvd-navigator-filter.md) does not find any other branching instruction for subsequent playback.</span></span> <span data-ttu-id="dae53-108">L’événement n’est pas envoyé lorsque l’application arrête la lecture.</span><span class="sxs-lookup"><span data-stu-id="dae53-108">The event is not sent when the application stops playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="dae53-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dae53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae53-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="dae53-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="dae53-111">Un membre de l’énumération [**DVD \_ PB s' \_ est arrêté**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) , indiquant la raison de l’arrêt de la lecture.</span><span class="sxs-lookup"><span data-stu-id="dae53-111">A member of the [**DVD\_PB\_STOPPED**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) enumeration, indicating why playback stopped.</span></span>

</dd> <dt>

<span data-ttu-id="dae53-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="dae53-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="dae53-113">Zéro.</span><span class="sxs-lookup"><span data-stu-id="dae53-113">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dae53-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dae53-114">Remarks</span></span>

<span data-ttu-id="dae53-115">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="dae53-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae53-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dae53-116">Requirements</span></span>



| <span data-ttu-id="dae53-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dae53-117">Requirement</span></span> | <span data-ttu-id="dae53-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dae53-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae53-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="dae53-119">Header</span></span><br/> | <dl> <span data-ttu-id="dae53-120"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dae53-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae53-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dae53-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae53-122">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="dae53-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="dae53-123">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="dae53-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="dae53-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="dae53-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




