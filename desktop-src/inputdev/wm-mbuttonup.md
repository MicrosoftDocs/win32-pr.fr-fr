---
title: Message WM_MBUTTONUP (winuser. h)
description: Publié lorsque l’utilisateur relâche le bouton central de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: fb8dee71-11bd-4405-855d-a5d120442271
keywords:
- WM_MBUTTONUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce7eb6b84c227934b5351a27ff8884fa78946ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032721"
---
# <a name="wm_mbuttonup-message"></a><span data-ttu-id="b950d-104">\_Message WM MBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="b950d-104">WM\_MBUTTONUP message</span></span>

<span data-ttu-id="b950d-105">Publié lorsque l’utilisateur relâche le bouton central de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b950d-105">Posted when the user releases the middle mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="b950d-106">Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="b950d-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="b950d-107">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="b950d-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="b950d-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b950d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MBUTTONUP                    0x0208
```



## <a name="parameters"></a><span data-ttu-id="b950d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b950d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b950d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b950d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b950d-111">Indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="b950d-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="b950d-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b950d-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b950d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b950d-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="b950d-114">Signification</span><span class="sxs-lookup"><span data-stu-id="b950d-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="b950d-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="b950d-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="b950d-116">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="b950d-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="b950d-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="b950d-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="b950d-118">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b950d-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="b950d-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="b950d-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="b950d-120">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b950d-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="b950d-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="b950d-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="b950d-122">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b950d-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="b950d-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="b950d-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="b950d-124">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="b950d-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="b950d-125"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="b950d-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="b950d-126">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b950d-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="b950d-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="b950d-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="b950d-128">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b950d-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="b950d-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b950d-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b950d-130">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="b950d-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="b950d-131">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b950d-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="b950d-132">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="b950d-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="b950d-133">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b950d-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="b950d-134">Notez que lorsqu’un menu contextuel est présent (affiché), les coordonnées sont relatives à l’écran, et non à la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b950d-134">Note that when a shortcut menu is present (displayed), coordinates are relative to the screen, not the client area.</span></span> <span data-ttu-id="b950d-135">Étant donné que [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) est un appel asynchrone et que la notification **WM \_ MBUTTONUP** n’a pas d’indicateur spécial indiquant une dérivation de coordonnée, une application ne peut pas déterminer si les coordonnées x, y contenues dans *lParam* sont relatives à l’écran ou à la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b950d-135">Because [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) is an asynchronous call and the **WM\_MBUTTONUP** notification does not have a special flag indicating coordinate derivation, an application cannot tell if the x,y coordinates contained in *lParam* are relative to the screen or the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b950d-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b950d-136">Return value</span></span>

<span data-ttu-id="b950d-137">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b950d-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b950d-138">Notes</span><span class="sxs-lookup"><span data-stu-id="b950d-138">Remarks</span></span>

<span data-ttu-id="b950d-139">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="b950d-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="b950d-140">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="b950d-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="b950d-141">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b950d-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="b950d-142">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="b950d-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b950d-143">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="b950d-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="b950d-144">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="b950d-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b950d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b950d-145">Requirements</span></span>



| <span data-ttu-id="b950d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b950d-146">Requirement</span></span> | <span data-ttu-id="b950d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="b950d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b950d-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b950d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b950d-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b950d-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b950d-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b950d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b950d-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b950d-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b950d-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="b950d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="b950d-153"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b950d-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b950d-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b950d-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="b950d-155">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b950d-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b950d-156">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b950d-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b950d-157">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="b950d-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b950d-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="b950d-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="b950d-159">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="b950d-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="b950d-160">**\_MBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="b950d-160">**WM\_MBUTTONDBLCLK**</span></span>](wm-mbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="b950d-161">**\_MBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="b950d-161">**WM\_MBUTTONDOWN**</span></span>](wm-mbuttondown.md)
</dt> <dt>

<span data-ttu-id="b950d-162">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b950d-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b950d-163">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="b950d-163">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="b950d-164">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="b950d-164">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b950d-165">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="b950d-165">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="b950d-166">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b950d-166">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

