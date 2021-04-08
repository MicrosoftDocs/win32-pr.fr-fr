---
title: Message MCM_SETTODAY (commctrl. h)
description: Définit le \ 0034 ; Today \ 0034 ; sélection pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetToday.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- MCM_SETTODAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743813"
---
# <a name="mcm_settoday-message"></a><span data-ttu-id="069f9-105">\_Message SETTODAY MCM</span><span class="sxs-lookup"><span data-stu-id="069f9-105">MCM\_SETTODAY message</span></span>

<span data-ttu-id="069f9-106">Définit la sélection « aujourd’hui » pour un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="069f9-106">Sets the "today" selection for a month calendar control.</span></span> <span data-ttu-id="069f9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .</span><span class="sxs-lookup"><span data-stu-id="069f9-107">You can send this message explicitly or by using the [**MonthCal\_SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="069f9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="069f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="069f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="069f9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="069f9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="069f9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="069f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="069f9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="069f9-112">Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contient la date à définir comme sélection « aujourd’hui » pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="069f9-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the "today" selection for the control.</span></span> <span data-ttu-id="069f9-113">Si ce paramètre a la valeur **null**, le contrôle retourne au paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="069f9-113">If this parameter is set to **NULL**, the control returns to the default setting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="069f9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="069f9-114">Return value</span></span>

<span data-ttu-id="069f9-115">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="069f9-115">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="069f9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="069f9-116">Remarks</span></span>

<span data-ttu-id="069f9-117">Si la sélection « aujourd’hui » est définie sur une autre date que la valeur par défaut, les conditions suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="069f9-117">If the "today" selection is set to any date other than the default, the following conditions apply:</span></span>

-   <span data-ttu-id="069f9-118">Le contrôle ne met pas à jour automatiquement la sélection « aujourd’hui » lorsque l’heure passe à minuit pour le jour actuel.</span><span class="sxs-lookup"><span data-stu-id="069f9-118">The control will not automatically update the "today" selection when the time passes midnight for the current day.</span></span>
-   <span data-ttu-id="069f9-119">Le contrôle ne met pas automatiquement à jour son affichage en fonction des modifications de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="069f9-119">The control will not automatically update its display based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="069f9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="069f9-120">Requirements</span></span>



| <span data-ttu-id="069f9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="069f9-121">Requirement</span></span> | <span data-ttu-id="069f9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="069f9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="069f9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="069f9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="069f9-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="069f9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="069f9-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="069f9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="069f9-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="069f9-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="069f9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="069f9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="069f9-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="069f9-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069f9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="069f9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069f9-130">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="069f9-130">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

