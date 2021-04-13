---
title: Message MCM_GETCURSEL (commctrl. h)
description: Récupère la date actuellement sélectionnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465867"
---
# <a name="mcm_getcursel-message"></a><span data-ttu-id="eec5c-105">\_Message GETCURSEL MCM</span><span class="sxs-lookup"><span data-stu-id="eec5c-105">MCM\_GETCURSEL message</span></span>

<span data-ttu-id="eec5c-106">Récupère la date actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="eec5c-106">Retrieves the currently selected date.</span></span> <span data-ttu-id="eec5c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="eec5c-107">You can send this message explicitly or by using the [**MonthCal\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eec5c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eec5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec5c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eec5c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eec5c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eec5c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eec5c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eec5c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eec5c-112">Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les informations de date actuellement sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="eec5c-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the currently selected date information.</span></span> <span data-ttu-id="eec5c-113">Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="eec5c-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec5c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eec5c-114">Return value</span></span>

<span data-ttu-id="eec5c-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="eec5c-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="eec5c-116">Ce message échouera toujours lorsqu’il sera appliqué aux contrôles de calendrier mensuel définis sur le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="eec5c-116">This message will always fail when applied to month calendar controls set to the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec5c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eec5c-117">Requirements</span></span>



| <span data-ttu-id="eec5c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eec5c-118">Requirement</span></span> | <span data-ttu-id="eec5c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="eec5c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eec5c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eec5c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eec5c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eec5c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eec5c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eec5c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eec5c-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eec5c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eec5c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="eec5c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec5c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec5c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec5c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eec5c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec5c-127">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="eec5c-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

