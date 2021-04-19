---
description: Un nouveau segment a démarré.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528407"
---
# <a name="ec_segment_started"></a><span data-ttu-id="0b92f-103">\_segment EC \_ démarré</span><span class="sxs-lookup"><span data-stu-id="0b92f-103">EC\_SEGMENT\_STARTED</span></span>

<span data-ttu-id="0b92f-104">Un nouveau segment a démarré.</span><span class="sxs-lookup"><span data-stu-id="0b92f-104">A new segment has started.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b92f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b92f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b92f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0b92f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0b92f-107">(**const** **Reference \_ Time** \* ) pointeur vers une valeur de **\_ temps de référence** qui spécifie le temps de flux cumulé depuis le début du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="0b92f-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="0b92f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0b92f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0b92f-109">(**DWORD**) Numéro de segment (de base zéro).</span><span class="sxs-lookup"><span data-stu-id="0b92f-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0b92f-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="0b92f-110">Default Action</span></span>

<span data-ttu-id="0b92f-111">Cet événement n’est pas envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="0b92f-111">This event is not sent to the application.</span></span> <span data-ttu-id="0b92f-112">Les applications ne peuvent pas remplacer l’action par défaut pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="0b92f-112">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b92f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0b92f-113">Remarks</span></span>

<span data-ttu-id="0b92f-114">Si un filtre envoie une [**\_ fin \_ de \_ segment ce**](ec-end-of-segment.md) à la fin d’un segment, il envoie cet événement au début du segment.</span><span class="sxs-lookup"><span data-stu-id="0b92f-114">If a filter will send an [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) at the end of a segment, it sends this event at the start of the segment.</span></span> <span data-ttu-id="0b92f-115">Le gestionnaire de graphique de filtre utilise cette notification d’événement pour calculer le \_ nombre \_ de \_ notifications de la fin de segment qu’il doit attendre à la fin du segment.</span><span class="sxs-lookup"><span data-stu-id="0b92f-115">The filter graph manager uses this event notification to compute how many EC\_END\_OF\_SEGMENT notifications it should expect at the end of the segment.</span></span>

<span data-ttu-id="0b92f-116">Par défaut, les filtres n’envoient pas d’événements [**\_ \_ de fin de \_ segment EC**](ec-end-of-segment.md) à la fin des segments et ne doivent donc pas envoyer cet événement.</span><span class="sxs-lookup"><span data-stu-id="0b92f-116">By default, filters do not send [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) events at the end of segments, and therefore should not send this event.</span></span> <span data-ttu-id="0b92f-117">Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="0b92f-117">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b92f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b92f-118">Requirements</span></span>



| <span data-ttu-id="0b92f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b92f-119">Requirement</span></span> | <span data-ttu-id="0b92f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b92f-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b92f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b92f-121">Header</span></span><br/> | <dl> <span data-ttu-id="0b92f-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b92f-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b92f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b92f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b92f-124">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="0b92f-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0b92f-125">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="0b92f-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




