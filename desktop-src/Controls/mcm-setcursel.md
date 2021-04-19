---
title: Message MCM_SETCURSEL (commctrl. h)
description: Définit la date actuellement sélectionnée pour un contrôle Month Calendar. Si la date spécifiée n’est pas affichée, le contrôle met à jour l’affichage pour l’afficher. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCurSel.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511593"
---
# <a name="mcm_setcursel-message"></a><span data-ttu-id="4495e-106">\_Message SETCURSEL MCM</span><span class="sxs-lookup"><span data-stu-id="4495e-106">MCM\_SETCURSEL message</span></span>

<span data-ttu-id="4495e-107">Définit la date actuellement sélectionnée pour un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="4495e-107">Sets the currently selected date for a month calendar control.</span></span> <span data-ttu-id="4495e-108">Si la date spécifiée n’est pas affichée, le contrôle met à jour l’affichage pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="4495e-108">If the specified date is not in view, the control updates the display to bring it into view.</span></span> <span data-ttu-id="4495e-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="4495e-109">You can send this message explicitly or by using the [**MonthCal\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4495e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4495e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4495e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4495e-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4495e-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4495e-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4495e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4495e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4495e-114">Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contient la date à définir comme sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="4495e-114">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the current selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4495e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4495e-115">Return value</span></span>

<span data-ttu-id="4495e-116">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4495e-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="4495e-117">Ce message échouera s’il est appliqué à un contrôle Month Calendar qui utilise le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4495e-117">This message will fail if applied to a month calendar control that uses the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4495e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4495e-118">Requirements</span></span>



| <span data-ttu-id="4495e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4495e-119">Requirement</span></span> | <span data-ttu-id="4495e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4495e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4495e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4495e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4495e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4495e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4495e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4495e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4495e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4495e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4495e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4495e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4495e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4495e-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4495e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4495e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4495e-128">Heures dans le contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="4495e-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

