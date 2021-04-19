---
title: Message MCM_SETRANGE (commctrl. h)
description: Définit les dates minimale et maximale autorisées pour un contrôle Month Calendar. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la \_ macro SetRange calendrier monthcal.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510350"
---
# <a name="mcm_setrange-message"></a><span data-ttu-id="42d13-105">\_Message de SEtrange MCM</span><span class="sxs-lookup"><span data-stu-id="42d13-105">MCM\_SETRANGE message</span></span>

<span data-ttu-id="42d13-106">Définit les dates minimale et maximale autorisées pour un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="42d13-106">Sets the minimum and maximum allowable dates for a month calendar control.</span></span> <span data-ttu-id="42d13-107">Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro [**\_ SetRange calendrier monthcal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .</span><span class="sxs-lookup"><span data-stu-id="42d13-107">You can send this message explicitly or by using the [**MonthCal\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="42d13-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42d13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d13-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42d13-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42d13-110">Valeurs d’indicateur qui spécifient quelles limites de date sont définies.</span><span class="sxs-lookup"><span data-stu-id="42d13-110">Flag values that specify which date limits are being set.</span></span> <span data-ttu-id="42d13-111">Cette valeur doit être l’une des valeurs suivantes, ou les deux :</span><span class="sxs-lookup"><span data-stu-id="42d13-111">This value must be one or both of the following:</span></span>



| <span data-ttu-id="42d13-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="42d13-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="42d13-113">Signification</span><span class="sxs-lookup"><span data-stu-id="42d13-113">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="42d13-114"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="42d13-114"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="42d13-115">La date maximale autorisée est définie.</span><span class="sxs-lookup"><span data-stu-id="42d13-115">The maximum allowable date is being set.</span></span> <span data-ttu-id="42d13-116">La structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) à *lpSysTimeArray* \[ 1 \] doit contenir des informations de date.</span><span class="sxs-lookup"><span data-stu-id="42d13-116">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[1\] must contain date information.</span></span> <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="42d13-117"><dt>**GDTR \_ min.**</dt></span><span class="sxs-lookup"><span data-stu-id="42d13-117"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="42d13-118">La date minimale autorisée est définie.</span><span class="sxs-lookup"><span data-stu-id="42d13-118">The minimum allowable date is being set.</span></span> <span data-ttu-id="42d13-119">La structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) à *lpSysTimeArray* \[ 0 \] doit contenir des informations de date.</span><span class="sxs-lookup"><span data-stu-id="42d13-119">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[0\] must contain date information.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="42d13-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42d13-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42d13-121">Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contiennent les limites de date.</span><span class="sxs-lookup"><span data-stu-id="42d13-121">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain the date limits.</span></span> <span data-ttu-id="42d13-122">La limite maximale doit être comprise dans *lpSysTimeArray* \[ 1 \] si GDTR \_ Max est spécifié, et *lpSysTimeArray* \[ 0 \] doit contenir la limite minimale si GDTR \_ min est spécifié.</span><span class="sxs-lookup"><span data-stu-id="42d13-122">The maximum limit must be in *lpSysTimeArray*\[1\] if GDTR\_MAX is specified, and *lpSysTimeArray*\[0\] must contain the minimum limit if GDTR\_MIN is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d13-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42d13-123">Return value</span></span>

<span data-ttu-id="42d13-124">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="42d13-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d13-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42d13-125">Requirements</span></span>



| <span data-ttu-id="42d13-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42d13-126">Requirement</span></span> | <span data-ttu-id="42d13-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="42d13-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42d13-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42d13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="42d13-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42d13-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42d13-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42d13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="42d13-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42d13-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42d13-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="42d13-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d13-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d13-133"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42d13-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42d13-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d13-135">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="42d13-135">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

