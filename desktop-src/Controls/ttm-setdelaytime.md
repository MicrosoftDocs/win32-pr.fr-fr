---
title: Message TTM_SETDELAYTIME (commctrl. h)
description: Définit les durées initiales, contextuelles et de réaffichage pour un contrôle ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- TTM_SETDELAYTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942143"
---
# <a name="ttm_setdelaytime-message"></a><span data-ttu-id="88ced-104">\_Message atténuation SETDELAYTIME</span><span class="sxs-lookup"><span data-stu-id="88ced-104">TTM\_SETDELAYTIME message</span></span>

<span data-ttu-id="88ced-105">Définit les durées initiales, contextuelles et de réaffichage pour un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="88ced-105">Sets the initial, pop-up, and reshow durations for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="88ced-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88ced-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ced-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88ced-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88ced-108">Indicateur qui spécifie la valeur de temps à définir.</span><span class="sxs-lookup"><span data-stu-id="88ced-108">Flag that specifies which time value to set.</span></span> <span data-ttu-id="88ced-109">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="88ced-109">This parameter can be one of the following values</span></span>



| <span data-ttu-id="88ced-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="88ced-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="88ced-111">Signification</span><span class="sxs-lookup"><span data-stu-id="88ced-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="88ced-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="88ced-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl>       | <span data-ttu-id="88ced-113">Définir la durée pendant laquelle une fenêtre d’info-bulle reste visible si le pointeur est immobile dans le rectangle englobant d’un outil.</span><span class="sxs-lookup"><span data-stu-id="88ced-113">Set the amount of time a tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span> <span data-ttu-id="88ced-114">Pour rétablir la valeur par défaut du délai autopop, affectez la valeur-1 à *lParam* .</span><span class="sxs-lookup"><span data-stu-id="88ced-114">To return the autopop delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="88ced-115"><dt>**TTDT \_ initial**</dt></span><span class="sxs-lookup"><span data-stu-id="88ced-115"><dt>**TTDT\_INITIAL**</dt></span></span> </dl>       | <span data-ttu-id="88ced-116">Définissez la durée pendant laquelle un pointeur doit rester immobile dans le rectangle englobant d’un outil avant que la fenêtre d’info-bulle ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="88ced-116">Set the amount of time a pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span> <span data-ttu-id="88ced-117">Pour rétablir la valeur par défaut du délai d’attente initial, affectez la valeur-1 à *lParam* .</span><span class="sxs-lookup"><span data-stu-id="88ced-117">To return the initial delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="88ced-118"><dt>**TTDT \_ RÉafficher**</dt></span><span class="sxs-lookup"><span data-stu-id="88ced-118"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>          | <span data-ttu-id="88ced-119">Définissez la durée nécessaire pour que les fenêtres d’info-bulle suivantes s’affichent lorsque le pointeur se déplace d’un outil à un autre.</span><span class="sxs-lookup"><span data-stu-id="88ced-119">Set the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span> <span data-ttu-id="88ced-120">Pour rétablir la valeur par défaut du délai de réaffichage, affectez la valeur-1 à *lParam* .</span><span class="sxs-lookup"><span data-stu-id="88ced-120">To return the reshow delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <span data-ttu-id="88ced-121"><dt>**TTDT \_ automatique**</dt></span><span class="sxs-lookup"><span data-stu-id="88ced-121"><dt>**TTDT\_AUTOMATIC**</dt></span></span> </dl> | <span data-ttu-id="88ced-122">Définissez les trois délais de temporisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="88ced-122">Set all three delay times to default proportions.</span></span> <span data-ttu-id="88ced-123">L’heure de autopop sera 10 fois supérieure à l’heure initiale et l’heure de réaffichage sera le cinquième de l’heure initiale.</span><span class="sxs-lookup"><span data-stu-id="88ced-123">The autopop time will be ten times the initial time and the reshow time will be one fifth the initial time.</span></span> <span data-ttu-id="88ced-124">Si cet indicateur est défini, utilisez une valeur positive de *lParam* pour spécifier l’heure initiale, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="88ced-124">If this flag is set, use a positive value of *lParam* to specify the initial time, in milliseconds.</span></span> <span data-ttu-id="88ced-125">Affectez une valeur négative à *lParam* pour retourner les valeurs par défaut des trois retards.</span><span class="sxs-lookup"><span data-stu-id="88ced-125">Set *lParam* to a negative value to return all three delay times to their default values.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="88ced-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88ced-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88ced-127">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le délai, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="88ced-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the delay time, in milliseconds.</span></span> <span data-ttu-id="88ced-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="88ced-128">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88ced-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88ced-129">Return value</span></span>

<span data-ttu-id="88ced-130">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="88ced-130">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ced-131">Notes</span><span class="sxs-lookup"><span data-stu-id="88ced-131">Remarks</span></span>

<span data-ttu-id="88ced-132">Les délais d’attente par défaut sont basés sur le temps de double-clic.</span><span class="sxs-lookup"><span data-stu-id="88ced-132">The default delay times are based on the double-click time.</span></span> <span data-ttu-id="88ced-133">Pour le double-clic par défaut de 500 ms, les temps de délai initial, autopop et de réaffichage sont de 500 ms, 5 000 MS et 100 ms respectivement.</span><span class="sxs-lookup"><span data-stu-id="88ced-133">For the default double-click time of 500 ms, the initial, autopop, and reshow delay times are 500ms, 5000ms, and 100ms respectively.</span></span> <span data-ttu-id="88ced-134">Le fragment de code suivant utilise la fonction [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) pour déterminer les trois délais pour tous les systèmes.</span><span class="sxs-lookup"><span data-stu-id="88ced-134">The following code fragment uses the [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) function to determine the three delay times for any system.</span></span>


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a><span data-ttu-id="88ced-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88ced-135">Requirements</span></span>



| <span data-ttu-id="88ced-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88ced-136">Requirement</span></span> | <span data-ttu-id="88ced-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="88ced-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88ced-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88ced-138">Minimum supported client</span></span><br/> | <span data-ttu-id="88ced-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88ced-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88ced-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88ced-140">Minimum supported server</span></span><br/> | <span data-ttu-id="88ced-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88ced-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88ced-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="88ced-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="88ced-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="88ced-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ced-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88ced-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ced-145">**ATTÉNUATION \_ GETDELAYTIME**</span><span class="sxs-lookup"><span data-stu-id="88ced-145">**TTM\_GETDELAYTIME**</span></span>](ttm-getdelaytime.md)
</dt> </dl>

 

