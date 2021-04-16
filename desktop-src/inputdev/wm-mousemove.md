---
title: Message WM_MOUSEMOVE (winuser. h)
description: Publié dans une fenêtre lorsque le curseur se déplace. Si la souris n’est pas capturée, le message est publié dans la fenêtre qui contient le curseur. Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.
ms.assetid: 9b99387e-e176-4b20-a05a-bc75928a1367
keywords:
- WM_MOUSEMOVE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSEMOVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61ffd10edbd58d11c5667fbda9dc0408ea1d72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508461"
---
# <a name="wm_mousemove-message"></a><span data-ttu-id="ea17d-106">\_Message WM MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="ea17d-106">WM\_MOUSEMOVE message</span></span>

<span data-ttu-id="ea17d-107">Publié dans une fenêtre lorsque le curseur se déplace.</span><span class="sxs-lookup"><span data-stu-id="ea17d-107">Posted to a window when the cursor moves.</span></span> <span data-ttu-id="ea17d-108">Si la souris n’est pas capturée, le message est publié dans la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="ea17d-108">If the mouse is not captured, the message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="ea17d-109">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="ea17d-109">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="ea17d-110">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ea17d-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEMOVE                    0x0200
```



## <a name="parameters"></a><span data-ttu-id="ea17d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea17d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea17d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea17d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea17d-113">Indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="ea17d-113">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="ea17d-114">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea17d-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="ea17d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea17d-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="ea17d-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ea17d-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="ea17d-117"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="ea17d-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="ea17d-118">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ea17d-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="ea17d-119"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="ea17d-120">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ea17d-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="ea17d-121"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="ea17d-122">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ea17d-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="ea17d-123"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="ea17d-124">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ea17d-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="ea17d-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="ea17d-126">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ea17d-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="ea17d-127"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="ea17d-128">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ea17d-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="ea17d-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="ea17d-130">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ea17d-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="ea17d-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea17d-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea17d-132">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="ea17d-132">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="ea17d-133">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="ea17d-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="ea17d-134">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="ea17d-134">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="ea17d-135">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="ea17d-135">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea17d-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea17d-136">Return value</span></span>

<span data-ttu-id="ea17d-137">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ea17d-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea17d-138">Notes</span><span class="sxs-lookup"><span data-stu-id="ea17d-138">Remarks</span></span>

<span data-ttu-id="ea17d-139">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="ea17d-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="ea17d-140">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="ea17d-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="ea17d-141">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ea17d-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="ea17d-142">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="ea17d-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea17d-143">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="ea17d-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="ea17d-144">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="ea17d-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea17d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea17d-145">Requirements</span></span>



| <span data-ttu-id="ea17d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea17d-146">Requirement</span></span> | <span data-ttu-id="ea17d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea17d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea17d-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea17d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ea17d-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea17d-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea17d-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea17d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ea17d-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea17d-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea17d-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea17d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea17d-153"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea17d-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea17d-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea17d-155">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ea17d-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea17d-156">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="ea17d-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="ea17d-157">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="ea17d-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="ea17d-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="ea17d-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="ea17d-159">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="ea17d-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="ea17d-160">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ea17d-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea17d-161">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="ea17d-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="ea17d-162">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="ea17d-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ea17d-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="ea17d-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="ea17d-164">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea17d-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

