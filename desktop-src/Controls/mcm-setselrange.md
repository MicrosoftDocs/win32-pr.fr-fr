---
title: Message MCM_SETSELRANGE (commctrl. h)
description: Définit la sélection d’un contrôle Month Calendar sur une plage de dates donnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- MCM_SETSELRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032421"
---
# <a name="mcm_setselrange-message"></a><span data-ttu-id="ba0e7-105">\_Message SETSELRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="ba0e7-105">MCM\_SETSELRANGE message</span></span>

<span data-ttu-id="ba0e7-106">Définit la sélection d’un contrôle Month Calendar sur une plage de dates donnée.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-106">Sets the selection for a month calendar control to a given date range.</span></span> <span data-ttu-id="ba0e7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .</span><span class="sxs-lookup"><span data-stu-id="ba0e7-107">You can send this message explicitly or by using the [**MonthCal\_SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba0e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba0e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba0e7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ba0e7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ba0e7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba0e7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba0e7-112">Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contiennent des informations de date représentant les limites de sélection.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain date information representing the selection limits.</span></span> <span data-ttu-id="ba0e7-113">La première date sélectionnée doit être spécifiée dans *lpSysTimeArray* \[ 0 \] et la dernière date sélectionnée doit être spécifiée dans *lpSysTimeArray* \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ba0e7-113">The first selected date must be specified in *lpSysTimeArray*\[0\], and the last selected date must be specified in *lpSysTimeArray*\[1\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0e7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba0e7-114">Return value</span></span>

<span data-ttu-id="ba0e7-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="ba0e7-116">Ce message échouera s’il est appliqué à un contrôle Month Calendar qui n’utilise pas le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ba0e7-116">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0e7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba0e7-117">Requirements</span></span>



| <span data-ttu-id="ba0e7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba0e7-118">Requirement</span></span> | <span data-ttu-id="ba0e7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba0e7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0e7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba0e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0e7-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba0e7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba0e7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba0e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0e7-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba0e7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba0e7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba0e7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba0e7-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba0e7-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0e7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba0e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0e7-127">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="ba0e7-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

