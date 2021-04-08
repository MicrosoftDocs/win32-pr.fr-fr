---
title: Message MCM_GETRANGE (commctrl. h)
description: Récupère les dates minimales et maximales autorisées définies pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetRange.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844286"
---
# <a name="mcm_getrange-message"></a><span data-ttu-id="25c62-105">\_Message GETRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="25c62-105">MCM\_GETRANGE message</span></span>

<span data-ttu-id="25c62-106">Récupère les dates minimales et maximales autorisées définies pour un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="25c62-106">Retrieves the minimum and maximum allowable dates set for a month calendar control.</span></span> <span data-ttu-id="25c62-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .</span><span class="sxs-lookup"><span data-stu-id="25c62-107">You can send this message explicitly or by using the [**MonthCal\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="25c62-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25c62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c62-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25c62-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25c62-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="25c62-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25c62-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25c62-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25c62-112">Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les informations de limite de date.</span><span class="sxs-lookup"><span data-stu-id="25c62-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the date limit information.</span></span> <span data-ttu-id="25c62-113">La limite minimale est définie dans *lprgSysTimeArray* \[ 0 \] et *lprgSysTimeArray* \[ 1 \] reçoit la limite maximale.</span><span class="sxs-lookup"><span data-stu-id="25c62-113">The minimum limit is set in *lprgSysTimeArray*\[0\], and *lprgSysTimeArray*\[1\] receives the maximum limit.</span></span> <span data-ttu-id="25c62-114">Si l’un des éléments a la valeur tous les zéros, aucune limite correspondante n’est définie pour le contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="25c62-114">If either element is set to all zeros, then no corresponding limit is set for the month calendar control.</span></span> <span data-ttu-id="25c62-115">Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="25c62-115">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c62-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25c62-116">Return value</span></span>

<span data-ttu-id="25c62-117">Retourne une **valeur DWORD** qui peut être égale à zéro (aucune limite n’est définie) ou une combinaison des valeurs suivantes qui spécifient des informations de limite :</span><span class="sxs-lookup"><span data-stu-id="25c62-117">Returns a **DWORD** that can be zero (no limits are set) or a combination of the following values that specify limit information:</span></span>



| <span data-ttu-id="25c62-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="25c62-118">Return code</span></span>                                                                              | <span data-ttu-id="25c62-119">Description</span><span class="sxs-lookup"><span data-stu-id="25c62-119">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25c62-120"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="25c62-120"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="25c62-121">Une limite maximale est définie pour le contrôle ; *lprgSysTimeArray* \[ 0 \] est valide et contient les informations de date applicables.</span><span class="sxs-lookup"><span data-stu-id="25c62-121">A maximum limit is set for the control; *lprgSysTimeArray*\[0\] is valid and contains the applicable date information.</span></span> <br/> |
| <dl> <span data-ttu-id="25c62-122"><dt>**GDTR \_ min.**</dt></span><span class="sxs-lookup"><span data-stu-id="25c62-122"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="25c62-123">Une limite minimale est définie pour le contrôle ; *lprgSysTimeArray* \[ 1 \] est valide et contient les informations de date applicables.</span><span class="sxs-lookup"><span data-stu-id="25c62-123">A minimum limit is set for the control; *lprgSysTimeArray*\[1\] is valid and contains the applicable date information.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="25c62-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25c62-124">Requirements</span></span>



| <span data-ttu-id="25c62-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25c62-125">Requirement</span></span> | <span data-ttu-id="25c62-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="25c62-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25c62-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25c62-127">Minimum supported client</span></span><br/> | <span data-ttu-id="25c62-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25c62-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25c62-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25c62-129">Minimum supported server</span></span><br/> | <span data-ttu-id="25c62-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25c62-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25c62-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="25c62-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="25c62-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25c62-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c62-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25c62-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c62-134">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="25c62-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

