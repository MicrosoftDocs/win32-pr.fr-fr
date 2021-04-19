---
description: Signale le début de tout toujours (PGC, Cell ou VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520828"
---
# <a name="ec_dvd_still_on"></a><span data-ttu-id="d10d7-103">\_DVD EC \_ toujours \_ allumé</span><span class="sxs-lookup"><span data-stu-id="d10d7-103">EC\_DVD\_STILL\_ON</span></span>

<span data-ttu-id="d10d7-104">Signale le début de tout toujours (PGC, Cell ou VOBU).</span><span class="sxs-lookup"><span data-stu-id="d10d7-104">Signals the beginning of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="d10d7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d10d7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d10d7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d10d7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d10d7-107">Valeur booléenne (**bool**) indiquant si des boutons sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="d10d7-107">Boolean (**BOOL**) value indicating whether buttons are available.</span></span> <span data-ttu-id="d10d7-108">Zéro (0) indique que les boutons sont disponibles, de sorte que la méthode [**IDvdControl2 :: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="d10d7-108">Zero (0) indicates buttons are available so the [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) method won't work.</span></span> <span data-ttu-id="d10d7-109">Un (1) indique qu’aucun bouton n’est disponible. par conséquent, **IDvdControl2 :: StillOff** fonctionne.</span><span class="sxs-lookup"><span data-stu-id="d10d7-109">One (1) indicates no buttons are available, so **IDvdControl2::StillOff** will work.</span></span>

</dd> <dt>

<span data-ttu-id="d10d7-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d10d7-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d10d7-111">Valeur **DWORD** indiquant le nombre de secondes restantes de la dernière opération.</span><span class="sxs-lookup"><span data-stu-id="d10d7-111">**DWORD** value indicating the number of seconds the still will last.</span></span> <span data-ttu-id="d10d7-112">0xFFFFFFFF indique qu’il s’agit toujours d’un infini, ce qui signifie que l’utilisateur appuie sur un bouton ou jusqu’à ce que l’application appelle [**IDvdControl2 :: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span><span class="sxs-lookup"><span data-stu-id="d10d7-112">0xFFFFFFFF indicates an infinite still, meaning wait until the user presses a button or until the application calls [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d10d7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d10d7-113">Remarks</span></span>

<span data-ttu-id="d10d7-114">Toutes les combinaisons de boutons et sont toujours possibles (les boutons activés sont toujours activés, les boutons activés sont toujours désactivés, le bouton désactivé est toujours activé et le bouton désactivé est désactivé).</span><span class="sxs-lookup"><span data-stu-id="d10d7-114">All combinations of buttons and still are possible (buttons on with still on, buttons on with still off, button off with still on, button off with still off).</span></span>

<span data-ttu-id="d10d7-115">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="d10d7-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10d7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d10d7-116">Requirements</span></span>



| <span data-ttu-id="d10d7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d10d7-117">Requirement</span></span> | <span data-ttu-id="d10d7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d10d7-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10d7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d10d7-119">Header</span></span><br/> | <dl> <span data-ttu-id="d10d7-120"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d10d7-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10d7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d10d7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10d7-122">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="d10d7-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d10d7-123">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="d10d7-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d10d7-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="d10d7-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




