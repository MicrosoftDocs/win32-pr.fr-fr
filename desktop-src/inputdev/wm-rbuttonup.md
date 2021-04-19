---
title: Message WM_RBUTTONUP (winuser. h)
description: Publié lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: 12d148ba-9324-4db3-b537-b2cd4d0b8f32
keywords:
- WM_RBUTTONUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_RBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85a1426b92e8f3aa05c25b551b42ce271b35c673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517323"
---
# <a name="wm_rbuttonup-message"></a><span data-ttu-id="b2d13-104">\_Message WM RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="b2d13-104">WM\_RBUTTONUP message</span></span>

<span data-ttu-id="b2d13-105">Publié lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b2d13-105">Posted when the user releases the right mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="b2d13-106">Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="b2d13-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="b2d13-107">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="b2d13-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="b2d13-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b2d13-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RBUTTONUP                    0x0205
```



## <a name="parameters"></a><span data-ttu-id="b2d13-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2d13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d13-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2d13-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2d13-111">Indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="b2d13-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="b2d13-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2d13-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b2d13-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2d13-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="b2d13-114">Signification</span><span class="sxs-lookup"><span data-stu-id="b2d13-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="b2d13-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="b2d13-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="b2d13-116">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="b2d13-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="b2d13-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="b2d13-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="b2d13-118">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b2d13-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="b2d13-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="b2d13-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="b2d13-120">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b2d13-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="b2d13-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="b2d13-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="b2d13-122">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="b2d13-122">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="b2d13-123"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="b2d13-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="b2d13-124">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b2d13-124">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="b2d13-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="b2d13-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="b2d13-126">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b2d13-126">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="b2d13-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2d13-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2d13-128">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="b2d13-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="b2d13-129">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b2d13-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="b2d13-130">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="b2d13-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="b2d13-131">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b2d13-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d13-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2d13-132">Return value</span></span>

<span data-ttu-id="b2d13-133">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b2d13-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2d13-134">Notes</span><span class="sxs-lookup"><span data-stu-id="b2d13-134">Remarks</span></span>

<span data-ttu-id="b2d13-135">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="b2d13-135">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="b2d13-136">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="b2d13-136">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="b2d13-137">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b2d13-137">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="b2d13-138">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="b2d13-138">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2d13-139">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="b2d13-139">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="b2d13-140">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="b2d13-140">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2d13-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2d13-141">Requirements</span></span>



| <span data-ttu-id="b2d13-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2d13-142">Requirement</span></span> | <span data-ttu-id="b2d13-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2d13-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d13-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2d13-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d13-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2d13-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b2d13-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2d13-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d13-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2d13-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2d13-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2d13-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2d13-149"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2d13-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d13-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2d13-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2d13-151">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b2d13-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2d13-152">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b2d13-152">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b2d13-153">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="b2d13-153">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b2d13-154">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="b2d13-154">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="b2d13-155">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="b2d13-155">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="b2d13-156">**\_RBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="b2d13-156">**WM\_RBUTTONDBLCLK**</span></span>](wm-rbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="b2d13-157">**\_RBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="b2d13-157">**WM\_RBUTTONDOWN**</span></span>](wm-rbuttondown.md)
</dt> <dt>

<span data-ttu-id="b2d13-158">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b2d13-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2d13-159">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="b2d13-159">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="b2d13-160">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="b2d13-160">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b2d13-161">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="b2d13-161">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="b2d13-162">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2d13-162">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

