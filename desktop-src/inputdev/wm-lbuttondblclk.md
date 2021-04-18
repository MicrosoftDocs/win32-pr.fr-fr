---
title: Message WM_LBUTTONDBLCLK (winuser. h)
description: Publié lorsque l’utilisateur double-clique sur le bouton gauche de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: 370aa19e-4939-4ac3-9c0b-137a9792e52a
keywords:
- WM_LBUTTONDBLCLK l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_LBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd91eef026ae027e183b4f304211915e7bbbd95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106522641"
---
# <a name="wm_lbuttondblclk-message"></a><span data-ttu-id="4610d-104">\_Message WM LBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="4610d-104">WM\_LBUTTONDBLCLK message</span></span>

<span data-ttu-id="4610d-105">Publié lorsque l’utilisateur double-clique sur le bouton gauche de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4610d-105">Posted when the user double-clicks the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="4610d-106">Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="4610d-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="4610d-107">Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="4610d-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="4610d-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4610d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDBLCLK                0x0203
```



## <a name="parameters"></a><span data-ttu-id="4610d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4610d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4610d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4610d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4610d-111">Indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="4610d-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="4610d-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4610d-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="4610d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4610d-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="4610d-114">Signification</span><span class="sxs-lookup"><span data-stu-id="4610d-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="4610d-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="4610d-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="4610d-116">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="4610d-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="4610d-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="4610d-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="4610d-118">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="4610d-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="4610d-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="4610d-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="4610d-120">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="4610d-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="4610d-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="4610d-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="4610d-122">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="4610d-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="4610d-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="4610d-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="4610d-124">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="4610d-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="4610d-125"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="4610d-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="4610d-126">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="4610d-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="4610d-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="4610d-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="4610d-128">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="4610d-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="4610d-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4610d-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4610d-130">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="4610d-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="4610d-131">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="4610d-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="4610d-132">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="4610d-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="4610d-133">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="4610d-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4610d-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4610d-134">Return value</span></span>

<span data-ttu-id="4610d-135">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="4610d-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4610d-136">Notes</span><span class="sxs-lookup"><span data-stu-id="4610d-136">Remarks</span></span>

<span data-ttu-id="4610d-137">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="4610d-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="4610d-138">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="4610d-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="4610d-139">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4610d-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="4610d-140">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="4610d-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4610d-141">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="4610d-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="4610d-142">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="4610d-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="4610d-143">Seules les fenêtres qui ont le style **cs \_ DBLCLKS** peuvent recevoir des messages **WM \_ LBUTTONDBLCLK** , que le système génère chaque fois que l’utilisateur appuie sur, relâche, puis appuie encore sur le bouton gauche de la souris dans le délai imparti pour le double-clic du système.</span><span class="sxs-lookup"><span data-stu-id="4610d-143">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_LBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="4610d-144">Un double-clic sur le bouton gauche de la souris génère en fait une séquence de quatre messages : [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md), [**WM \_ LBUTTONUP**](wm-lbuttonup.md), **WM \_ LBUTTONDBLCLK** et **WM \_ LBUTTONUP**.</span><span class="sxs-lookup"><span data-stu-id="4610d-144">Double-clicking the left mouse button actually generates a sequence of four messages: [**WM\_LBUTTONDOWN**](wm-lbuttondown.md), [**WM\_LBUTTONUP**](wm-lbuttonup.md), **WM\_LBUTTONDBLCLK**, and **WM\_LBUTTONUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4610d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4610d-145">Requirements</span></span>



| <span data-ttu-id="4610d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4610d-146">Requirement</span></span> | <span data-ttu-id="4610d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="4610d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4610d-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4610d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4610d-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4610d-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4610d-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4610d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4610d-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4610d-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4610d-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="4610d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="4610d-153"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4610d-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4610d-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4610d-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="4610d-155">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4610d-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4610d-156">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="4610d-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="4610d-157">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="4610d-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="4610d-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="4610d-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="4610d-159">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="4610d-159">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="4610d-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="4610d-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="4610d-161">**SetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="4610d-161">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="4610d-162">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="4610d-162">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="4610d-163">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="4610d-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="4610d-164">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4610d-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4610d-165">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="4610d-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="4610d-166">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="4610d-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4610d-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="4610d-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="4610d-168">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4610d-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

