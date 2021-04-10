---
title: Message MCM_GETSELRANGE (commctrl. h)
description: Récupère des informations de date qui représentent les limites supérieure et inférieure de la plage de dates actuellement sélectionnée par l’utilisateur. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941951"
---
# <a name="mcm_getselrange-message"></a><span data-ttu-id="358c0-105">\_Message GETSELRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="358c0-105">MCM\_GETSELRANGE message</span></span>

<span data-ttu-id="358c0-106">Récupère des informations de date qui représentent les limites supérieure et inférieure de la plage de dates actuellement sélectionnée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="358c0-106">Retrieves date information that represents the upper and lower limits of the date range currently selected by the user.</span></span> <span data-ttu-id="358c0-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .</span><span class="sxs-lookup"><span data-stu-id="358c0-107">You can send this message explicitly or by using the [**MonthCal\_GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="358c0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="358c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="358c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="358c0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="358c0-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="358c0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="358c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="358c0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="358c0-112">Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les limites inférieure et supérieure de la sélection de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="358c0-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the user's selection.</span></span> <span data-ttu-id="358c0-113">Les limites inférieure et supérieure sont placées dans *lprgSysTimeArray* \[ 0 \] et *lprgSysTimeArray* \[ 1 \] , respectivement.</span><span class="sxs-lookup"><span data-stu-id="358c0-113">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="358c0-114">Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="358c0-114">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="358c0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="358c0-115">Return value</span></span>

<span data-ttu-id="358c0-116">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="358c0-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="358c0-117">**MCM \_ GETSELRANGE** échouera s’il est appliqué à un contrôle Month Calendar qui n’utilise pas le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="358c0-117">**MCM\_GETSELRANGE** will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="358c0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="358c0-118">Requirements</span></span>



| <span data-ttu-id="358c0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="358c0-119">Requirement</span></span> | <span data-ttu-id="358c0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="358c0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="358c0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="358c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="358c0-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="358c0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="358c0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="358c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="358c0-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="358c0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="358c0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="358c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="358c0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="358c0-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="358c0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="358c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358c0-128">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="358c0-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

