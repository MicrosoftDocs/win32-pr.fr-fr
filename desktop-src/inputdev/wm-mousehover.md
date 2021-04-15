---
title: Message WM_MOUSEHOVER (winuser. h)
description: Publié dans une fenêtre lorsque le curseur pointe sur la zone cliente de la fenêtre pendant la période spécifiée dans un appel antérieur à TrackMouseEvent.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- WM_MOUSEHOVER l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65747ade6bd2ec9456281ac02711de18675a411e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464927"
---
# <a name="wm_mousehover-message"></a><span data-ttu-id="e6214-104">\_Message WM MOUSEHOVER</span><span class="sxs-lookup"><span data-stu-id="e6214-104">WM\_MOUSEHOVER message</span></span>

<span data-ttu-id="e6214-105">Publié dans une fenêtre lorsque le curseur pointe sur la zone cliente de la fenêtre pendant la période spécifiée dans un appel antérieur à [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="e6214-105">Posted to a window when the cursor hovers over the client area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="e6214-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e6214-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a><span data-ttu-id="e6214-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6214-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6214-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6214-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6214-109">Indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="e6214-109">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="e6214-110">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e6214-110">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e6214-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6214-111">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="e6214-112">Signification</span><span class="sxs-lookup"><span data-stu-id="e6214-112">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="e6214-113"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="e6214-113"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="e6214-114">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="e6214-114">The CTRL key is depressed.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="e6214-115"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="e6214-115"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="e6214-116">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e6214-116">The left mouse button is depressed.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="e6214-117"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="e6214-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="e6214-118">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e6214-118">The middle mouse button is depressed.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="e6214-119"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="e6214-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="e6214-120">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e6214-120">The right mouse button is depressed.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="e6214-121"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="e6214-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="e6214-122">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="e6214-122">The SHIFT key is depressed.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="e6214-123"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="e6214-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="e6214-124">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e6214-124">The first X button is down.</span></span><br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="e6214-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="e6214-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="e6214-126">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e6214-126">The second X button is down.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="e6214-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6214-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6214-128">Le mot de poids faible spécifie la coordonnée x du curseur.</span><span class="sxs-lookup"><span data-stu-id="e6214-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="e6214-129">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="e6214-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="e6214-130">Le mot de poids fort spécifie la coordonnée y du curseur.</span><span class="sxs-lookup"><span data-stu-id="e6214-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="e6214-131">La coordonnée est relative au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="e6214-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6214-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6214-132">Return value</span></span>

<span data-ttu-id="e6214-133">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="e6214-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6214-134">Notes</span><span class="sxs-lookup"><span data-stu-id="e6214-134">Remarks</span></span>

<span data-ttu-id="e6214-135">Le suivi de survol s’arrête quand **WM \_ MOUSEHOVER** est généré.</span><span class="sxs-lookup"><span data-stu-id="e6214-135">Hover tracking stops when **WM\_MOUSEHOVER** is generated.</span></span> <span data-ttu-id="e6214-136">L’application doit appeler à nouveau [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) si elle nécessite un suivi supplémentaire du comportement de pointage de la souris.</span><span class="sxs-lookup"><span data-stu-id="e6214-136">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="e6214-137">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="e6214-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="e6214-138">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="e6214-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="e6214-139">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e6214-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="e6214-140">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="e6214-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e6214-141">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="e6214-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="e6214-142">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="e6214-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6214-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6214-143">Requirements</span></span>



| <span data-ttu-id="e6214-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6214-144">Requirement</span></span> | <span data-ttu-id="e6214-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6214-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6214-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6214-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e6214-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6214-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e6214-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6214-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e6214-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6214-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e6214-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6214-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6214-151"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6214-151"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6214-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6214-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6214-153">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e6214-153">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6214-154">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="e6214-154">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="e6214-155">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="e6214-155">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="e6214-156">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="e6214-156">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="e6214-157">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="e6214-157">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="e6214-158">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="e6214-158">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="e6214-159">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="e6214-159">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

<span data-ttu-id="e6214-160">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e6214-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6214-161">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="e6214-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="e6214-162">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="e6214-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e6214-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="e6214-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="e6214-164">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6214-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

