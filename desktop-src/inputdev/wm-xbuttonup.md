---
title: Message WM_XBUTTONUP (winuser. h)
description: Publié lorsque l’utilisateur relâche le premier ou le second bouton X lorsque le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: ad726859-368a-4603-bffa-4e639bc69a6a
keywords:
- WM_XBUTTONUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_XBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 08/23/2019
ms.openlocfilehash: 521faefb2e2a76e94a0517c28a5fa812ef34ef5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942500"
---
# <a name="wm_xbuttonup-message"></a><span data-ttu-id="97b6f-104">\_Message WM XBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="97b6f-104">WM\_XBUTTONUP message</span></span>

<span data-ttu-id="97b6f-105">Publié lorsque l’utilisateur relâche le premier ou le second bouton X lorsque le curseur se trouve dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="97b6f-105">Posted when the user releases the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="97b6f-106">Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="97b6f-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="97b6f-107">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="97b6f-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="97b6f-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="97b6f-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONUP                    0x020C
```



## <a name="parameters"></a><span data-ttu-id="97b6f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97b6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97b6f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97b6f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97b6f-111">Le mot de poids faible indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="97b6f-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="97b6f-112">Il peut s’agir d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="97b6f-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="97b6f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b6f-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="97b6f-114">Signification</span><span class="sxs-lookup"><span data-stu-id="97b6f-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="97b6f-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="97b6f-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="97b6f-116">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="97b6f-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="97b6f-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="97b6f-118">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="97b6f-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="97b6f-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="97b6f-120">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="97b6f-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="97b6f-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="97b6f-122">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="97b6f-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="97b6f-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="97b6f-124">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="97b6f-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="97b6f-125"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="97b6f-126">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="97b6f-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="97b6f-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="97b6f-128">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="97b6f-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="97b6f-129">Le mot de poids fort indique le bouton qui a été relâché.</span><span class="sxs-lookup"><span data-stu-id="97b6f-129">The high-order word indicates which button was released.</span></span> <span data-ttu-id="97b6f-130">Ce peut être l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="97b6f-130">It can be one of the following values:</span></span>



| <span data-ttu-id="97b6f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b6f-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="97b6f-132">Signification</span><span class="sxs-lookup"><span data-stu-id="97b6f-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="97b6f-133"><dt>**Le bouton XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="97b6f-134">Le premier bouton X a été relâché.</span><span class="sxs-lookup"><span data-stu-id="97b6f-134">The first X button was released.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="97b6f-135"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="97b6f-136">Le deuxième bouton X a été relâché.</span><span class="sxs-lookup"><span data-stu-id="97b6f-136">The second X button was released.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="97b6f-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97b6f-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97b6f-138">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="97b6f-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="97b6f-139">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="97b6f-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="97b6f-140">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="97b6f-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="97b6f-141">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="97b6f-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97b6f-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97b6f-142">Return value</span></span>

<span data-ttu-id="97b6f-143">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="97b6f-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="97b6f-144">Pour plus d’informations sur le traitement de la valeur de retour, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="97b6f-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="97b6f-145">Notes</span><span class="sxs-lookup"><span data-stu-id="97b6f-145">Remarks</span></span>

<span data-ttu-id="97b6f-146">Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* :</span><span class="sxs-lookup"><span data-stu-id="97b6f-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="97b6f-147">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="97b6f-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="97b6f-148">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="97b6f-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="97b6f-149">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="97b6f-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="97b6f-150">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="97b6f-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97b6f-151">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="97b6f-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="97b6f-152">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="97b6f-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="97b6f-153">Contrairement aux [**messages \_ WM LBUTTONUP**](wm-lbuttonup.md), [**WM \_ MBUTTONUP**](wm-mbuttonup.md)et [**WM \_ RBUTTONUP**](wm-rbuttonup.md) , une application doit retourner la **valeur true** à partir de ce message si elle le traite.</span><span class="sxs-lookup"><span data-stu-id="97b6f-153">Unlike the [**WM\_LBUTTONUP**](wm-lbuttonup.md), [**WM\_MBUTTONUP**](wm-mbuttonup.md), and [**WM\_RBUTTONUP**](wm-rbuttonup.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="97b6f-154">Cela permettra aux logiciels qui simulent ce message sur les systèmes Windows antérieurs à Windows 2000 de déterminer si la procédure de fenêtre a traité le message ou appelé [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traiter.</span><span class="sxs-lookup"><span data-stu-id="97b6f-154">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="97b6f-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97b6f-155">Requirements</span></span>



| <span data-ttu-id="97b6f-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97b6f-156">Requirement</span></span> | <span data-ttu-id="97b6f-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="97b6f-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97b6f-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97b6f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="97b6f-159">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97b6f-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="97b6f-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97b6f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="97b6f-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97b6f-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="97b6f-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="97b6f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="97b6f-163"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97b6f-163"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b6f-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97b6f-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="97b6f-165">**Référence**</span><span class="sxs-lookup"><span data-stu-id="97b6f-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97b6f-166">**Obtient le \_ wParam d’État KEYstate \_**</span><span class="sxs-lookup"><span data-stu-id="97b6f-166">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="97b6f-167">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="97b6f-167">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="97b6f-168">**Obtient \_ XBUTTON \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="97b6f-168">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="97b6f-169">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="97b6f-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="97b6f-170">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="97b6f-170">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="97b6f-171">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="97b6f-171">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="97b6f-172">**\_XBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="97b6f-172">**WM\_XBUTTONDBLCLK**</span></span>](wm-xbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="97b6f-173">**\_XBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="97b6f-173">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

<span data-ttu-id="97b6f-174">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="97b6f-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="97b6f-175">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="97b6f-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="97b6f-176">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="97b6f-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="97b6f-177">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="97b6f-177">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="97b6f-178">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97b6f-178">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

