---
title: Message WM_XBUTTONDBLCLK (winuser. h)
description: Publié lorsque l’utilisateur double-clique sur le premier ou le second bouton X lorsque le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- WM_XBUTTONDBLCLK l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed0612c2850f784901f01313935145fc9d3d7910
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742341"
---
# <a name="wm_xbuttondblclk-message"></a><span data-ttu-id="f5c86-104">\_Message WM XBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="f5c86-104">WM\_XBUTTONDBLCLK message</span></span>

<span data-ttu-id="f5c86-105">Publié lorsque l’utilisateur double-clique sur le premier ou le second bouton X lorsque le curseur se trouve dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f5c86-105">Posted when the user double-clicks the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="f5c86-106">Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="f5c86-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="f5c86-107">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="f5c86-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="f5c86-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f5c86-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a><span data-ttu-id="f5c86-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5c86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c86-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5c86-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c86-111">Le mot de poids faible indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="f5c86-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="f5c86-112">Il peut s’agir d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5c86-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="f5c86-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5c86-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="f5c86-114">Signification</span><span class="sxs-lookup"><span data-stu-id="f5c86-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="f5c86-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="f5c86-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="f5c86-116">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="f5c86-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="f5c86-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="f5c86-118">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f5c86-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="f5c86-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="f5c86-120">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f5c86-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="f5c86-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="f5c86-122">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f5c86-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="f5c86-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="f5c86-124">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="f5c86-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="f5c86-125"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="f5c86-126">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f5c86-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="f5c86-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="f5c86-128">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f5c86-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="f5c86-129">Le mot de poids fort indique sur quel bouton l’utilisateur a double-cliqué.</span><span class="sxs-lookup"><span data-stu-id="f5c86-129">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="f5c86-130">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5c86-130">It can be one of the following values.</span></span>



| <span data-ttu-id="f5c86-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5c86-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="f5c86-132">Signification</span><span class="sxs-lookup"><span data-stu-id="f5c86-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="f5c86-133"><dt>**Le bouton XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="f5c86-134">L’utilisateur a double-cliqué sur le premier bouton X.</span><span class="sxs-lookup"><span data-stu-id="f5c86-134">The first X button was double-clicked.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="f5c86-135"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="f5c86-136">L’utilisateur a double-cliqué sur le deuxième bouton X.</span><span class="sxs-lookup"><span data-stu-id="f5c86-136">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f5c86-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5c86-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c86-138">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="f5c86-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="f5c86-139">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f5c86-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="f5c86-140">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="f5c86-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="f5c86-141">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f5c86-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c86-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5c86-142">Return value</span></span>

<span data-ttu-id="f5c86-143">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="f5c86-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="f5c86-144">Pour plus d’informations sur le traitement de la valeur de retour, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f5c86-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c86-145">Notes</span><span class="sxs-lookup"><span data-stu-id="f5c86-145">Remarks</span></span>

<span data-ttu-id="f5c86-146">Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* :</span><span class="sxs-lookup"><span data-stu-id="f5c86-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="f5c86-147">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="f5c86-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="f5c86-148">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="f5c86-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="f5c86-149">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f5c86-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="f5c86-150">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="f5c86-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5c86-151">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="f5c86-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="f5c86-152">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="f5c86-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="f5c86-153">Seules les fenêtres qui ont le style **cs \_ DBLCLKS** peuvent recevoir des messages **WM \_ XBUTTONDBLCLK** , que le système génère chaque fois que l’utilisateur appuie sur, relâche, puis appuie à nouveau sur un bouton X dans la limite de temps du double-clic du système.</span><span class="sxs-lookup"><span data-stu-id="f5c86-153">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_XBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="f5c86-154">Le fait de double-cliquer sur l’un de ces boutons génère en fait quatre messages : [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md), [**WM \_ XBUTTONUP**](wm-xbuttonup.md), **WM \_ XBUTTONDBLCLK** et **WM \_ XBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="f5c86-154">Double-clicking one of these buttons actually generates four messages: [**WM\_XBUTTONDOWN**](wm-xbuttondown.md), [**WM\_XBUTTONUP**](wm-xbuttonup.md), **WM\_XBUTTONDBLCLK**, and **WM\_XBUTTONUP** again.</span></span>

<span data-ttu-id="f5c86-155">Contrairement aux [**messages \_ WM LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)et [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) , une application doit retourner la **valeur true** à partir de ce message si elle le traite.</span><span class="sxs-lookup"><span data-stu-id="f5c86-155">Unlike the [**WM\_LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM\_MBUTTONDBLCLK**](wm-mbuttondblclk.md), and [**WM\_RBUTTONDBLCLK**](wm-rbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="f5c86-156">Cela permettra aux logiciels qui simulent ce message sur les systèmes Windows antérieurs à Windows 2000 de déterminer si la procédure de fenêtre a traité le message ou appelé [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traiter.</span><span class="sxs-lookup"><span data-stu-id="f5c86-156">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c86-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5c86-157">Requirements</span></span>



| <span data-ttu-id="f5c86-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5c86-158">Requirement</span></span> | <span data-ttu-id="f5c86-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5c86-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c86-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5c86-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c86-161">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5c86-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f5c86-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5c86-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c86-163">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5c86-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f5c86-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5c86-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c86-165"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5c86-165"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c86-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5c86-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5c86-167">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f5c86-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5c86-168">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f5c86-168">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f5c86-169">**Obtient le \_ wParam d’État KEYstate \_**</span><span class="sxs-lookup"><span data-stu-id="f5c86-169">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="f5c86-170">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="f5c86-170">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="f5c86-171">**Obtient \_ XBUTTON \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="f5c86-171">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="f5c86-172">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="f5c86-172">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="f5c86-173">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="f5c86-173">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="f5c86-174">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="f5c86-174">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="f5c86-175">**SetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="f5c86-175">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="f5c86-176">**\_XBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="f5c86-176">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f5c86-177">**\_XBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="f5c86-177">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)
</dt> <dt>

<span data-ttu-id="f5c86-178">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f5c86-178">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f5c86-179">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="f5c86-179">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="f5c86-180">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f5c86-180">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f5c86-181">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="f5c86-181">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="f5c86-182">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5c86-182">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

