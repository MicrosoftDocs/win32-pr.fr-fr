---
title: Message MCM_GETMONTHRANGE (commctrl. h)
description: Récupère des informations de date (à l’aide de structures SYSTEMTIME) qui représentent les limites haute et basse de l’affichage d’un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532056"
---
# <a name="mcm_getmonthrange-message"></a><span data-ttu-id="cc3df-105">\_Message GETMONTHRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="cc3df-105">MCM\_GETMONTHRANGE message</span></span>

<span data-ttu-id="cc3df-106">Récupère des informations de date (à l’aide de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) qui représentent les limites haute et basse de l’affichage d’un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="cc3df-106">Retrieves date information (using [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures) that represents the high and low limits of a month calendar control's display.</span></span> <span data-ttu-id="cc3df-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .</span><span class="sxs-lookup"><span data-stu-id="cc3df-107">You can send this message explicitly or by using the [**MonthCal\_GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc3df-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc3df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3df-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc3df-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc3df-110">Valeur spécifiant l’étendue des limites de plage à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cc3df-110">Value specifying the scope of the range limits to be retrieved.</span></span> <span data-ttu-id="cc3df-111">Cette valeur doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc3df-111">This value must be one of the following:</span></span>



| <span data-ttu-id="cc3df-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc3df-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="cc3df-113">Signification</span><span class="sxs-lookup"><span data-stu-id="cc3df-113">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <span data-ttu-id="cc3df-114"><dt>**GMR \_ DAYSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="cc3df-114"><dt>**GMR\_DAYSTATE**</dt></span></span> </dl> | <span data-ttu-id="cc3df-115">Inclut les mois précédents et de fin de la plage visible qui ne sont affichés que partiellement.</span><span class="sxs-lookup"><span data-stu-id="cc3df-115">Include preceding and trailing months of visible range that are only partially displayed.</span></span> <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <span data-ttu-id="cc3df-116"><dt>**GMR \_ visible**</dt></span><span class="sxs-lookup"><span data-stu-id="cc3df-116"><dt>**GMR\_VISIBLE**</dt></span></span> </dl>    | <span data-ttu-id="cc3df-117">Inclut uniquement les mois qui sont entièrement affichés.</span><span class="sxs-lookup"><span data-stu-id="cc3df-117">Include only those months that are entirely displayed.</span></span> <br/>                                    |



 

</dd> <dt>

<span data-ttu-id="cc3df-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc3df-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc3df-119">Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les limites inférieure et supérieure de la portée spécifiée par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="cc3df-119">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the scope specified by *wParam*.</span></span> <span data-ttu-id="cc3df-120">Les limites inférieure et supérieure sont placées dans *lprgSysTimeArray* \[ 0 \] et *lprgSysTimeArray* \[ 1 \] , respectivement.</span><span class="sxs-lookup"><span data-stu-id="cc3df-120">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="cc3df-121">Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cc3df-121">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3df-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc3df-122">Return value</span></span>

<span data-ttu-id="cc3df-123">Retourne une valeur INT qui représente la plage, en mois, fractionnée par les deux limites retournées à *lParam*.</span><span class="sxs-lookup"><span data-stu-id="cc3df-123">Returns an INT value that represents the range, in months, spanned by the two limits returned at *lParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc3df-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc3df-124">Requirements</span></span>



| <span data-ttu-id="cc3df-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc3df-125">Requirement</span></span> | <span data-ttu-id="cc3df-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc3df-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3df-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc3df-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3df-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc3df-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc3df-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc3df-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3df-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc3df-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc3df-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc3df-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc3df-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc3df-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc3df-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc3df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3df-134">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="cc3df-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

