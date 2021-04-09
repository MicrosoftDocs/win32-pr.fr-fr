---
title: Message MCM_GETTODAY (commctrl. h)
description: Récupère les informations de date pour la date spécifiée sous la forme \ 0034 ; Today \ 0034 ; pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942199"
---
# <a name="mcm_gettoday-message"></a><span data-ttu-id="958f4-105">\_Message GETTODAY MCM</span><span class="sxs-lookup"><span data-stu-id="958f4-105">MCM\_GETTODAY message</span></span>

<span data-ttu-id="958f4-106">Récupère les informations de date pour la date spécifiée comme « Today » pour un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="958f4-106">Retrieves the date information for the date specified as "today" for a month calendar control.</span></span> <span data-ttu-id="958f4-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .</span><span class="sxs-lookup"><span data-stu-id="958f4-107">You can send this message explicitly or by using the [**MonthCal\_GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="958f4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="958f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="958f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="958f4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="958f4-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="958f4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="958f4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="958f4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="958f4-112">Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les informations de date.</span><span class="sxs-lookup"><span data-stu-id="958f4-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the date information.</span></span> <span data-ttu-id="958f4-113">Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="958f4-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="958f4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="958f4-114">Return value</span></span>

<span data-ttu-id="958f4-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="958f4-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="958f4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="958f4-116">Requirements</span></span>



| <span data-ttu-id="958f4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="958f4-117">Requirement</span></span> | <span data-ttu-id="958f4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="958f4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="958f4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="958f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="958f4-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="958f4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="958f4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="958f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="958f4-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="958f4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="958f4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="958f4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="958f4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="958f4-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="958f4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="958f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958f4-126">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="958f4-126">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

