---
title: Message WM_LBUTTONDOWN (winuser. h)
description: Publié lorsque l’utilisateur appuie sur le bouton gauche de la souris lorsque le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: 2e43720a-98e6-407a-9430-34c288c3da51
keywords:
- WM_LBUTTONDOWN l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_LBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: c8ac54e813d622f47462b73b763534977ba0932f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531012"
---
# <a name="wm_lbuttondown-message"></a><span data-ttu-id="b495b-104">\_Message WM LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="b495b-104">WM\_LBUTTONDOWN message</span></span>

<span data-ttu-id="b495b-105">Publié lorsque l’utilisateur appuie sur le bouton gauche de la souris lorsque le curseur se trouve dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b495b-105">Posted when the user presses the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="b495b-106">Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="b495b-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="b495b-107">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="b495b-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="b495b-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b495b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDOWN                  0x0201
```



## <a name="parameters"></a><span data-ttu-id="b495b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b495b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b495b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b495b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b495b-111">Indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="b495b-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="b495b-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b495b-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b495b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b495b-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="b495b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="b495b-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="b495b-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="b495b-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="b495b-116">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="b495b-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="b495b-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="b495b-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="b495b-118">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b495b-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="b495b-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="b495b-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="b495b-120">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b495b-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="b495b-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="b495b-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="b495b-122">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b495b-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="b495b-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="b495b-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="b495b-124">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="b495b-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="b495b-125"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="b495b-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="b495b-126">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b495b-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="b495b-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="b495b-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="b495b-128">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b495b-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="b495b-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b495b-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b495b-130">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="b495b-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="b495b-131">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b495b-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="b495b-132">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="b495b-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="b495b-133">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b495b-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b495b-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b495b-134">Return value</span></span>

<span data-ttu-id="b495b-135">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b495b-135">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="b495b-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="b495b-136">Example</span></span>


```cpp
LRESULT CALLBACK WndProc(_In_ HWND hWnd, _In_ UINT msg, _In_ WPARAM wParam, _In_ LPARAM lParam)
{
    POINT pt;

    switch (msg)
    {

    case WM_LBUTTONDOWN:
            {
                pt.x = GET_X_LPARAM(lParam);
                pt.y = GET_Y_LPARAM(lParam);
            }
        }
        break;

    default:
        return DefWindowProc(hWnd, msg, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="b495b-137">Pour plus d’exemples, consultez [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="b495b-137">For more examples see [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="b495b-138">Notes</span><span class="sxs-lookup"><span data-stu-id="b495b-138">Remarks</span></span>

<span data-ttu-id="b495b-139">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="b495b-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="b495b-140">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b495b-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="b495b-141">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="b495b-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b495b-142">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="b495b-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="b495b-143">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="b495b-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="b495b-144">Pour détecter que la touche ALT a été enfoncée, vérifiez si [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) avec le **\_ menu VK** < 0.</span><span class="sxs-lookup"><span data-stu-id="b495b-144">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="b495b-145">Notez qu’il ne doit pas s’agir de [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="b495b-145">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="b495b-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b495b-146">Requirements</span></span>



| <span data-ttu-id="b495b-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b495b-147">Requirement</span></span> | <span data-ttu-id="b495b-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="b495b-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b495b-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b495b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b495b-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b495b-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b495b-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b495b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b495b-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b495b-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b495b-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="b495b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="b495b-154"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b495b-154"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b495b-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b495b-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="b495b-156">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b495b-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b495b-157">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b495b-157">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b495b-158">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="b495b-158">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b495b-159">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="b495b-159">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="b495b-160">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="b495b-160">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="b495b-161">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="b495b-161">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="b495b-162">**\_LBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="b495b-162">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="b495b-163">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="b495b-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="b495b-164">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b495b-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b495b-165">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="b495b-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="b495b-166">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="b495b-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b495b-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="b495b-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="b495b-168">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b495b-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

