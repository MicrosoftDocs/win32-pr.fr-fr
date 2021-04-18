---
title: Message WM_MOUSEWHEEL (winuser. h)
description: Envoyé à la fenêtre de focus lorsque la roulette de la souris est pivotée.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- WM_MOUSEWHEEL l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509310"
---
# <a name="wm_mousewheel-message"></a><span data-ttu-id="86468-104">\_Message WM MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="86468-104">WM\_MOUSEWHEEL message</span></span>

<span data-ttu-id="86468-105">Envoyé à la fenêtre de focus lorsque la roulette de la souris est pivotée.</span><span class="sxs-lookup"><span data-stu-id="86468-105">Sent to the focus window when the mouse wheel is rotated.</span></span> <span data-ttu-id="86468-106">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propage le message au parent de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="86468-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="86468-107">Il ne doit y avoir aucun transfert interne du message, car **DefWindowProc** le propage vers le haut de la chaîne parente jusqu’à ce qu’il trouve une fenêtre qui le traite.</span><span class="sxs-lookup"><span data-stu-id="86468-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="86468-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="86468-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a><span data-ttu-id="86468-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86468-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86468-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86468-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86468-111">Le mot de poids fort indique la distance de rotation de la roue, exprimée en multiples ou divisions de la **roue \_ Delta**, qui est 120.</span><span class="sxs-lookup"><span data-stu-id="86468-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or divisions of **WHEEL\_DELTA**, which is 120.</span></span> <span data-ttu-id="86468-112">Une valeur positive indique que la roulette a été pivotée vers l’avant, en dehors de l’utilisateur ; une valeur négative indique que la roulette a été retournée vers l’arrière pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86468-112">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span>

<span data-ttu-id="86468-113">Le mot de poids faible indique si différentes clés virtuelles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="86468-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="86468-114">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="86468-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="86468-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="86468-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="86468-116">Signification</span><span class="sxs-lookup"><span data-stu-id="86468-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="86468-117"><dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle</span><span class="sxs-lookup"><span data-stu-id="86468-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="86468-118">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="86468-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="86468-119"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="86468-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="86468-120">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="86468-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="86468-121"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="86468-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="86468-122">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="86468-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="86468-123"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="86468-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="86468-124">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="86468-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="86468-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="86468-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="86468-126">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="86468-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="86468-127"><dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="86468-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="86468-128">Le premier bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="86468-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="86468-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="86468-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="86468-130">Le deuxième bouton X est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="86468-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="86468-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86468-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86468-132">Le mot de poids faible spécifie la coordonnée x du pointeur, par rapport à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="86468-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="86468-133">Le mot de poids fort spécifie la coordonnée y du pointeur, par rapport à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="86468-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86468-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86468-134">Return value</span></span>

<span data-ttu-id="86468-135">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="86468-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="86468-136">Notes</span><span class="sxs-lookup"><span data-stu-id="86468-136">Remarks</span></span>

<span data-ttu-id="86468-137">Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* :</span><span class="sxs-lookup"><span data-stu-id="86468-137">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="86468-138">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="86468-138">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="86468-139">Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses).</span><span class="sxs-lookup"><span data-stu-id="86468-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="86468-140">Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="86468-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="86468-141">Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.</span><span class="sxs-lookup"><span data-stu-id="86468-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86468-142">N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="86468-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="86468-143">Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.</span><span class="sxs-lookup"><span data-stu-id="86468-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="86468-144">La rotation de la roue est un multiple de la valeur **\_ Delta** de la roue, définie à 120.</span><span class="sxs-lookup"><span data-stu-id="86468-144">The wheel rotation will be a multiple of **WHEEL\_DELTA**, which is set at 120.</span></span> <span data-ttu-id="86468-145">Il s’agit du seuil d’action à entreprendre, et une telle action (par exemple, le défilement d’un incrément) doit se produire pour chaque Delta.</span><span class="sxs-lookup"><span data-stu-id="86468-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="86468-146">Le Delta a été défini sur 120 pour permettre à Microsoft ou à d’autres fournisseurs de créer des roues plus fines (une molette à rotation libre sans crans) pour envoyer plus de messages par rotation, mais avec une valeur inférieure dans chaque message.</span><span class="sxs-lookup"><span data-stu-id="86468-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="86468-147">Pour utiliser cette fonctionnalité, vous pouvez ajouter les valeurs Delta entrantes jusqu’à ce que le **\_ Delta** de la roue soit atteint (pour une rotation Delta, vous obteniez la même réponse), ou faire défiler les lignes partielles en réponse aux messages les plus fréquents.</span><span class="sxs-lookup"><span data-stu-id="86468-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages.</span></span> <span data-ttu-id="86468-148">Vous pouvez également choisir votre granularité de défilement et accumuler les deltas jusqu’à ce qu’il soit atteint.</span><span class="sxs-lookup"><span data-stu-id="86468-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

<span data-ttu-id="86468-149">Notez qu’il n’existe aucun *fwKeys* pour **MSH \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="86468-149">Note, there is no *fwKeys* for **MSH\_MOUSEWHEEL**.</span></span> <span data-ttu-id="86468-150">Dans le cas contraire, les paramètres sont exactement les mêmes que pour **WM \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="86468-150">Otherwise, the parameters are exactly the same as for **WM\_MOUSEWHEEL**.</span></span>

<span data-ttu-id="86468-151">Il revient à l’application de transférer **MSH \_ MOUSEWHEEL** à tous les objets ou contrôles incorporés.</span><span class="sxs-lookup"><span data-stu-id="86468-151">It is up to the application to forward **MSH\_MOUSEWHEEL** to any embedded objects or controls.</span></span> <span data-ttu-id="86468-152">L’application est requise pour envoyer le message à une application OLE incorporée active.</span><span class="sxs-lookup"><span data-stu-id="86468-152">The application is required to send the message to an active embedded OLE application.</span></span> <span data-ttu-id="86468-153">Il est facultatif que l’application l’envoie à un contrôle activé pour la roulette avec le focus.</span><span class="sxs-lookup"><span data-stu-id="86468-153">It is optional that the application sends it to a wheel-enabled control with focus.</span></span> <span data-ttu-id="86468-154">Si l’application envoie le message à un contrôle, elle peut vérifier la valeur de retour pour voir si le message a été traité.</span><span class="sxs-lookup"><span data-stu-id="86468-154">If the application does send the message to a control, it can check the return value to see if the message was processed.</span></span> <span data-ttu-id="86468-155">Les contrôles sont requis pour retourner la valeur **true** s’ils traitent le message.</span><span class="sxs-lookup"><span data-stu-id="86468-155">Controls are required to return a value of **TRUE** if they process the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="86468-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86468-156">Requirements</span></span>



| <span data-ttu-id="86468-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86468-157">Requirement</span></span> | <span data-ttu-id="86468-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="86468-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86468-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86468-159">Minimum supported client</span></span><br/> | <span data-ttu-id="86468-160">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86468-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="86468-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86468-161">Minimum supported server</span></span><br/> | <span data-ttu-id="86468-162">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86468-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="86468-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="86468-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="86468-164"><dt>Winuser. h (inclure Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86468-164"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86468-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86468-165">See also</span></span>

<dl> <dt>

<span data-ttu-id="86468-166">**Référence**</span><span class="sxs-lookup"><span data-stu-id="86468-166">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86468-167">**Obtient le \_ wParam d’État KEYstate \_**</span><span class="sxs-lookup"><span data-stu-id="86468-167">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="86468-168">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="86468-168">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="86468-169">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="86468-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="86468-170">**Obtient le wParam de la \_ roue \_ \_**</span><span class="sxs-lookup"><span data-stu-id="86468-170">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="86468-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86468-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="86468-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86468-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="86468-173">**événement de souris \_**</span><span class="sxs-lookup"><span data-stu-id="86468-173">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="86468-174">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="86468-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="86468-175">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="86468-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="86468-176">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="86468-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="86468-177">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="86468-177">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="86468-178">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="86468-178">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="86468-179">[**MOMENTS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86468-179">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="86468-180">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="86468-180">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

