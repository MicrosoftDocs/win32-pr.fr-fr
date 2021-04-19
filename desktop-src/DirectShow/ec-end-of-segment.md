---
description: La fin d’un segment a été atteinte.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534986"
---
# <a name="ec_end_of_segment"></a><span data-ttu-id="b8710-103">\_fin \_ de \_ segment ce</span><span class="sxs-lookup"><span data-stu-id="b8710-103">EC\_END\_OF\_SEGMENT</span></span>

<span data-ttu-id="b8710-104">La fin d’un segment a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="b8710-104">The end of a segment was reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8710-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8710-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8710-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b8710-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b8710-107">(**const** **Reference \_ Time** \* ) pointeur vers une valeur de **\_ temps de référence** qui spécifie le temps de flux cumulé depuis le début du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="b8710-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="b8710-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b8710-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b8710-109">(**DWORD**) Numéro de segment (de base zéro).</span><span class="sxs-lookup"><span data-stu-id="b8710-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b8710-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="b8710-110">Default Action</span></span>

<span data-ttu-id="b8710-111">Le gestionnaire de graphes de filtre vérifie le nombre d’événements de la **\_ fin ce \_ du \_ segment** par rapport au nombre d’événements de [**\_ \_ début de segment EC**](ec-segment-started.md) .</span><span class="sxs-lookup"><span data-stu-id="b8710-111">The filter graph manager checks the number of **EC\_END\_OF\_SEGMENT** events against the number of [**EC\_SEGMENT\_STARTED**](ec-segment-started.md) events.</span></span> <span data-ttu-id="b8710-112">S’ils correspondent, il transfère l’événement **\_ de fin \_ de \_ segment EC** à l’application.</span><span class="sxs-lookup"><span data-stu-id="b8710-112">If they match, it forwards the **EC\_END\_OF\_SEGMENT** event to the application.</span></span> <span data-ttu-id="b8710-113">Les applications ne peuvent pas remplacer l’action par défaut pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="b8710-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8710-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b8710-114">Remarks</span></span>

<span data-ttu-id="b8710-115">Ce code d’événement prend en charge le bouclage transparent.</span><span class="sxs-lookup"><span data-stu-id="b8710-115">This event code supports seamless looping.</span></span> <span data-ttu-id="b8710-116">Lorsqu’un appel à la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) comprend l' \_ indicateur AM chercher le \_ segment, le filtre source envoie ce code d’événement au lieu d’appeler [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span><span class="sxs-lookup"><span data-stu-id="b8710-116">When a call to the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method includes the AM\_SEEKING\_Segment flag, the source filter sends this event code instead of calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8710-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8710-117">Requirements</span></span>



| <span data-ttu-id="b8710-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8710-118">Requirement</span></span> | <span data-ttu-id="b8710-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8710-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8710-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8710-120">Header</span></span><br/> | <dl> <span data-ttu-id="b8710-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8710-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8710-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8710-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8710-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="b8710-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b8710-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="b8710-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




