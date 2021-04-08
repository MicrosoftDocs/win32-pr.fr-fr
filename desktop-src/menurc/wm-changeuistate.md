---
title: Message WM_CHANGEUISTATE (winuser. h)
description: Une application envoie le \_ message WM CHANGEUISTATE pour indiquer que l’état de l’interface utilisateur doit être modifié.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743581"
---
# <a name="wm_changeuistate-message"></a><span data-ttu-id="eafec-104">\_Message WM CHANGEUISTATE</span><span class="sxs-lookup"><span data-stu-id="eafec-104">WM\_CHANGEUISTATE message</span></span>

<span data-ttu-id="eafec-105">Une application envoie le message **WM \_ CHANGEUISTATE** pour indiquer que l’état de l’interface utilisateur doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="eafec-105">An application sends the **WM\_CHANGEUISTATE** message to indicate that the UI state should be changed.</span></span>


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a><span data-ttu-id="eafec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eafec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eafec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eafec-108">Le mot de poids faible spécifie l’action à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="eafec-108">The low-order word specifies the action to be taken.</span></span> <span data-ttu-id="eafec-109">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eafec-109">This member can be one of the following values.</span></span>



| <span data-ttu-id="eafec-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="eafec-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="eafec-111">Signification</span><span class="sxs-lookup"><span data-stu-id="eafec-111">Meaning</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="eafec-112"><dt>**Interfaces utilisateur \_ EFFACER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eafec-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="eafec-113">Les indicateurs d’état d’interface utilisateur spécifiés par le mot de poids fort doivent être effacés.</span><span class="sxs-lookup"><span data-stu-id="eafec-113">The UI state flags specified by the high-order word should be cleared.</span></span><br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="eafec-114"><dt>**Interfaces utilisateur \_ INITIALiser**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="eafec-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="eafec-115">Les indicateurs d’état d’interface utilisateur spécifiés par le mot de poids fort doivent être modifiés en fonction du dernier événement d’entrée.</span><span class="sxs-lookup"><span data-stu-id="eafec-115">The UI state flags specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="eafec-116">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="eafec-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="eafec-117"><dt>**Interfaces utilisateur \_ DÉFINIR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eafec-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="eafec-118">Les indicateurs d’état d’interface utilisateur spécifiés par le mot de poids fort doivent être définis.</span><span class="sxs-lookup"><span data-stu-id="eafec-118">The UI state flags specified by the high-order word should be set.</span></span><br/>                                                                      |



 

<span data-ttu-id="eafec-119">Le mot de poids fort spécifie les éléments d’état d’interface utilisateur qui sont affectés ou le style du contrôle.</span><span class="sxs-lookup"><span data-stu-id="eafec-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="eafec-120">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eafec-120">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="eafec-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eafec-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="eafec-122">Signification</span><span class="sxs-lookup"><span data-stu-id="eafec-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="eafec-123"><dt>**UISF \_**</dt> <dt>0x4</dt> actif</span><span class="sxs-lookup"><span data-stu-id="eafec-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="eafec-124">Un contrôle doit être dessiné dans le style utilisé pour les contrôles actifs.</span><span class="sxs-lookup"><span data-stu-id="eafec-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="eafec-125"><dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="eafec-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="eafec-126">Les accélérateurs clavier sont masqués.</span><span class="sxs-lookup"><span data-stu-id="eafec-126">Keyboard accelerators are hidden.</span></span><br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="eafec-127"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="eafec-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="eafec-128">Les indicateurs de focus sont masqués.</span><span class="sxs-lookup"><span data-stu-id="eafec-128">Focus indicators are hidden.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="eafec-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eafec-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eafec-130">Ce paramètre n’est pas utilisé et doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="eafec-130">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eafec-131">Notes</span><span class="sxs-lookup"><span data-stu-id="eafec-131">Remarks</span></span>

<span data-ttu-id="eafec-132">Une fenêtre doit envoyer ce message à lui-même ou à son parent lorsqu’il doit modifier les éléments d’état de l’interface utilisateur de toutes les fenêtres dans la même hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="eafec-132">A window should send this message to itself or its parent when it must change the UI state elements of all windows in the same hierarchy.</span></span> <span data-ttu-id="eafec-133">La procédure de fenêtre doit laisser [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traiter ce message afin que l’ensemble de l’arborescence de la fenêtre ait un état d’interface utilisateur cohérent.</span><span class="sxs-lookup"><span data-stu-id="eafec-133">The window procedure must let [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) process this message so that the entire window tree has a consistent UI state.</span></span> <span data-ttu-id="eafec-134">Lorsque la fenêtre de niveau supérieur reçoit le message **WM \_ CHANGEUISTATE** , elle envoie un message [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) avec les mêmes paramètres à toutes les fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="eafec-134">When the top-level window receives the **WM\_CHANGEUISTATE** message, it sends a [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with the same parameters to all child windows.</span></span> <span data-ttu-id="eafec-135">Lorsque le système traite le message **WM \_ UPDATEUISTATE** , il effectue la modification dans l’état de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eafec-135">When the system processes the **WM\_UPDATEUISTATE** message, it makes the change in the UI state.</span></span>

<span data-ttu-id="eafec-136">Si le mot de poids faible de *wParam* est \_ Initialize UIS, le système envoie le message [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) avec un état d’interface utilisateur basé sur le dernier événement d’entrée.</span><span class="sxs-lookup"><span data-stu-id="eafec-136">If the low-order word of *wParam* is UIS\_INITIALIZE, the system will send the [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with a UI state based on the last input event.</span></span> <span data-ttu-id="eafec-137">Par exemple, si la dernière entrée provient de la souris, le système masque les indications de clavier. Et, si la dernière entrée provient du clavier, le système affiche les indications de clavier. Si l’État qui résulte du traitement de **WM \_ CHANGEUISTATE** est le même que celui de l’ancien, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) n’envoie pas ce message.</span><span class="sxs-lookup"><span data-stu-id="eafec-137">For example, if the last input came from the mouse, the system will hide the keyboard cues. And, if the last input came from the keyboard, the system will show the keyboard cues. If the state that results from processing **WM\_CHANGEUISTATE** is the same as the old state, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not send this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eafec-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eafec-138">Requirements</span></span>



| <span data-ttu-id="eafec-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eafec-139">Requirement</span></span> | <span data-ttu-id="eafec-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="eafec-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eafec-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eafec-141">Minimum supported client</span></span><br/> | <span data-ttu-id="eafec-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eafec-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eafec-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eafec-143">Minimum supported server</span></span><br/> | <span data-ttu-id="eafec-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eafec-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eafec-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="eafec-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="eafec-146"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eafec-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eafec-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eafec-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="eafec-148">**Référence**</span><span class="sxs-lookup"><span data-stu-id="eafec-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="eafec-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eafec-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="eafec-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eafec-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eafec-151">**\_QUERYUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="eafec-151">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="eafec-152">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="eafec-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eafec-153">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="eafec-153">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

