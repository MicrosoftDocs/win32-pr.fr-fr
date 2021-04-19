---
title: Message WM_RBUTTONDOWN (winuser. h)
description: Publié lorsque l’utilisateur appuie sur le bouton droit de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: da1a7d7c-6e49-4097-8b43-dcee7bd5fb3f
keywords:
- WM_RBUTTONDOWN l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_RBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfebe1330b5c37758dc3d9486633510fdce62049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510157"
---
# <a name="wm_rbuttondown-message"></a><span data-ttu-id="f8cfc-104">\_Message WM RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="f8cfc-104">WM\_RBUTTONDOWN message</span></span>

<span data-ttu-id="f8cfc-105">Publié lorsque l’utilisateur appuie sur le bouton droit de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-105">Posted when the user presses the right mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="f8cfc-106">Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="f8cfc-107">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="f8cfc-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f8cfc-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RBUTTONDOWN                  0x0204
```



## <a name="parameters"></a><span data-ttu-id="f8cfc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8cfc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8cfc-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8cfc-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8cfc-111">Indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="f8cfc-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="f8cfc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8cfc-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="f8cfc-114">Signification</span><span class="sxs-lookup"><span data-stu-id="f8cfc-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="f8cfc-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="f8cfc-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="f8cfc-116">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="f8cfc-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f8cfc-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="f8cfc-118">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="f8cfc-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="f8cfc-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="f8cfc-120">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="f8cfc-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f8cfc-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="f8cfc-122">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="f8cfc-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="f8cfc-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="f8cfc-124">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="f8cfc-125"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="f8cfc-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="f8cfc-126">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="f8cfc-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="f8cfc-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="f8cfc-128">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="f8cfc-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8cfc-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8cfc-130">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="f8cfc-131">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="f8cfc-132">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="f8cfc-133">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8cfc-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8cfc-134">Return value</span></span>

<span data-ttu-id="f8cfc-135">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8cfc-136">Notes</span><span class="sxs-lookup"><span data-stu-id="f8cfc-136">Remarks</span></span>

<span data-ttu-id="f8cfc-137">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="f8cfc-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="f8cfc-138">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="f8cfc-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="f8cfc-139">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="f8cfc-140">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8cfc-141">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="f8cfc-142">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="f8cfc-143">Pour détecter que la touche ALT a été enfoncée, vérifiez si [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) avec le **\_ menu VK** < 0.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-143">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="f8cfc-144">Notez qu’il ne doit pas s’agir de [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="f8cfc-144">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8cfc-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8cfc-145">Requirements</span></span>



| <span data-ttu-id="f8cfc-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8cfc-146">Requirement</span></span> | <span data-ttu-id="f8cfc-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8cfc-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cfc-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8cfc-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f8cfc-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8cfc-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8cfc-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8cfc-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f8cfc-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8cfc-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8cfc-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8cfc-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8cfc-153"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8cfc-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8cfc-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8cfc-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8cfc-155">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8cfc-156">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="f8cfc-157">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="f8cfc-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="f8cfc-159">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-159">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="f8cfc-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="f8cfc-161">**\_RBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-161">**WM\_RBUTTONDBLCLK**</span></span>](wm-rbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="f8cfc-162">**\_RBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-162">**WM\_RBUTTONUP**</span></span>](wm-rbuttonup.md)
</dt> <dt>

<span data-ttu-id="f8cfc-163">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8cfc-164">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="f8cfc-164">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="f8cfc-165">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-165">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f8cfc-166">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="f8cfc-166">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="f8cfc-167">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8cfc-167">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

