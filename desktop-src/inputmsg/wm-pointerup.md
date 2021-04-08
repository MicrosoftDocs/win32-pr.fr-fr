---
title: WM_POINTERUP, message
description: Publié lorsqu’un pointeur qui a effectué le contact sur la zone cliente d’une fenêtre interrompt le contact.
ms.assetid: 3bdc38da-227c-4be1-bf0b-99704b8a0111
keywords:
- WM_POINTERUP les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f6c23b810b7ec5a7f60ae7e52ddbb5b535ab0503
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103953299"
---
# <a name="wm_pointerup-message"></a><span data-ttu-id="f7971-104">WM_POINTERUP, message</span><span class="sxs-lookup"><span data-stu-id="f7971-104">WM_POINTERUP message</span></span>

<span data-ttu-id="f7971-105">Publié lorsqu’un pointeur qui a effectué le contact sur la zone cliente d’une fenêtre interrompt le contact.</span><span class="sxs-lookup"><span data-stu-id="f7971-105">Posted when a pointer that made contact over the client area of a window breaks contact.</span></span> <span data-ttu-id="f7971-106">Ce message d’entrée cible la fenêtre sur laquelle le pointeur crée un contact et le pointeur est, à ce stade, capturé implicitement dans la fenêtre afin que la fenêtre continue à recevoir des messages d’entrée, y compris le **WM_POINTERUP** notification pour le pointeur, jusqu’à ce qu’il interrompe le contact.</span><span class="sxs-lookup"><span data-stu-id="f7971-106">This input message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input messages including the **WM_POINTERUP** notification for the pointer until it breaks contact.</span></span>

<span data-ttu-id="f7971-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f7971-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="f7971-108">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="f7971-108">\[!Important\]</span></span>  
> <span data-ttu-id="f7971-109">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="f7971-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="f7971-110">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="f7971-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="f7971-111">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="f7971-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="f7971-112">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f7971-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERUP                  0x0247
```



## <a name="parameters"></a><span data-ttu-id="f7971-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7971-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7971-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7971-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7971-115">Contient des informations sur le pointeur.</span><span class="sxs-lookup"><span data-stu-id="f7971-115">Contains information about the pointer.</span></span> <span data-ttu-id="f7971-116">Utilisez les macros suivantes pour récupérer des informations à partir du paramètre wParam.</span><span class="sxs-lookup"><span data-stu-id="f7971-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="f7971-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur du pointeur.</span><span class="sxs-lookup"><span data-stu-id="f7971-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="f7971-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si ce message représente la première entrée générée par un nouveau pointeur.</span><span class="sxs-lookup"><span data-stu-id="f7971-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="f7971-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si ce message a été généré par un pointeur pendant sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="f7971-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="f7971-120">Cet indicateur n’est pas défini sur les messages qui indiquent que le pointeur a quitté la plage de détection</span><span class="sxs-lookup"><span data-stu-id="f7971-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="f7971-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si ce message a été généré par un pointeur qui est en contact avec l’aire de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f7971-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="f7971-122">Cet indicateur n’est pas défini sur les messages qui indiquent un pointeur de pointage.</span><span class="sxs-lookup"><span data-stu-id="f7971-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="f7971-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indique que ce pointeur a été désigné comme principal.</span><span class="sxs-lookup"><span data-stu-id="f7971-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="f7971-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique s’il existe une action principale.</span><span class="sxs-lookup"><span data-stu-id="f7971-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="f7971-125">Cela équivaut à un bouton gauche de la souris enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f7971-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="f7971-126">Un pointeur tactile aura cet ensemble lorsqu’il est en contact avec la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="f7971-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="f7971-127">Un pointeur de stylet aura cet ensemble lorsqu’il est en contact avec la surface du digitaliseur sans bouton enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f7971-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="f7971-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique s’il existe une action secondaire.</span><span class="sxs-lookup"><span data-stu-id="f7971-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="f7971-129">Cela est similaire au bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="f7971-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="f7971-130">Un pointeur de stylet aura cet ensemble lorsqu’il est en contact avec la surface du digitaliseur avec le bouton du stylet du stylet enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f7971-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="f7971-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique s’il existe une ou plusieurs actions tertiaires en fonction du type de pointeur ; les applications qui souhaitent répondre à des actions tertiaires doivent récupérer des informations spécifiques au type pointeur pour déterminer quels boutons tertiaires sont enfoncés.</span><span class="sxs-lookup"><span data-stu-id="f7971-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="f7971-132">Par exemple, une application peut déterminer les États des boutons d’un stylet en appelant [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) et en examinant les indicateurs qui spécifient des États de bouton.</span><span class="sxs-lookup"><span data-stu-id="f7971-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="f7971-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si le pointeur spécifié a pris la quatrième action.</span><span class="sxs-lookup"><span data-stu-id="f7971-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="f7971-134">Les applications qui souhaitent répondre aux quatrièmes actions doivent récupérer des informations spécifiques au type de pointeur pour déterminer si le bouton de la première souris étendue (le bouton XButton1) est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f7971-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="f7971-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : [**indicateur**](pointer-flags-contants.md) qui indique si le pointeur spécifié a pris la cinquième mesure.</span><span class="sxs-lookup"><span data-stu-id="f7971-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="f7971-136">Les applications qui souhaitent répondre aux cinquièmes actions doivent récupérer des informations spécifiques au type de pointeur pour déterminer si le bouton de la souris étendue (XButton2) est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f7971-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="f7971-137">Pour plus d’informations, consultez [**indicateurs de pointeur**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="f7971-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="f7971-138">Aucun indicateur de bouton n’est défini pour un pointeur de pointage.</span><span class="sxs-lookup"><span data-stu-id="f7971-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="f7971-139">Cela est analogue au déplacement de la souris, sans aucun bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="f7971-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="f7971-140">Une application peut déterminer les États des boutons d’un stylet de pointage, par exemple, en appelant [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) et en examinant les indicateurs qui spécifient des États de bouton.</span><span class="sxs-lookup"><span data-stu-id="f7971-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="f7971-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7971-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7971-142">Contient l’emplacement du point du pointeur.</span><span class="sxs-lookup"><span data-stu-id="f7971-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="f7971-143">Étant donné que le pointeur peut établir un contact avec l’appareil sur une zone non triviale, cet emplacement de point peut être une simplification d’une zone de pointeur plus complexe.</span><span class="sxs-lookup"><span data-stu-id="f7971-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="f7971-144">Dans la mesure du possible, une application doit utiliser les informations complètes de la zone du pointeur à la place de l’emplacement du point.</span><span class="sxs-lookup"><span data-stu-id="f7971-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="f7971-145">Utilisez les macros suivantes pour récupérer les coordonnées d’écran physiques du point.</span><span class="sxs-lookup"><span data-stu-id="f7971-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="f7971-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam) : coordonnée X (point horizontal).</span><span class="sxs-lookup"><span data-stu-id="f7971-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="f7971-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam) : coordonnée Y (point vertical).</span><span class="sxs-lookup"><span data-stu-id="f7971-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7971-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7971-148">Return value</span></span>

<span data-ttu-id="f7971-149">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="f7971-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="f7971-150">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="f7971-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7971-151">Notes</span><span class="sxs-lookup"><span data-stu-id="f7971-151">Remarks</span></span>

> <span data-ttu-id="f7971-152">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="f7971-152">\[!Important\]</span></span>  
> <span data-ttu-id="f7971-153">Quand une fenêtre perd la capture d’un pointeur et qu’elle reçoit la notification [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , elle ne reçoit généralement pas de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f7971-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="f7971-154">Pour cette raison, il est important de ne pas faire de suppositions basées sur des notifications égales [**WM_POINTERDOWN**](wm-pointerdown.md) / **WM_POINTERUP** ou de [**WM_POINTERENTER**](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) des notifications.</span><span class="sxs-lookup"><span data-stu-id="f7971-154">For this reason, it is important that you not make any assumptions based on evenly paired [**WM_POINTERDOWN**](wm-pointerdown.md)/**WM_POINTERUP** or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="f7971-155">Chaque pointeur a un identificateur de pointeur unique pendant sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="f7971-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="f7971-156">La durée de vie d’un pointeur commence lorsqu’il est détecté pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="f7971-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="f7971-157">Un message de [**WM_POINTERENTER**](wm-pointerenter.md) est généré si un pointeur de pointage est détecté.</span><span class="sxs-lookup"><span data-stu-id="f7971-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="f7971-158">Un [**WM_POINTERDOWN**](wm-pointerdown.md) message suivi d’un message **WM_POINTERENTER** est généré si un pointeur sans pointage est détecté.</span><span class="sxs-lookup"><span data-stu-id="f7971-158">A [**WM_POINTERDOWN**](wm-pointerdown.md) message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="f7971-159">Pendant sa durée de vie, un pointeur peut générer une série de messages [**WM_POINTERUPDATE**](wm-pointerupdate.md) pendant qu’il pointe ou en contact.</span><span class="sxs-lookup"><span data-stu-id="f7971-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="f7971-160">La durée de vie d’un pointeur se termine lorsqu’il n’est plus détecté.</span><span class="sxs-lookup"><span data-stu-id="f7971-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="f7971-161">Cela génère un message de [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="f7971-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="f7971-162">Lorsqu’un pointeur est abandonné, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="f7971-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="f7971-163">Un message [**WM_POINTERLEAVE**](wm-pointerleave.md) peut également être généré lorsqu’un pointeur non capturé se déplace en dehors des limites d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f7971-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="f7971-164">Pour obtenir la position horizontale et verticale d’un pointeur, utilisez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="f7971-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>

<span data-ttu-id="f7971-165">Utilisez le code suivant pour obtenir la position horizontale et verticale :</span><span class="sxs-lookup"><span data-stu-id="f7971-165">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="f7971-166">La macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) peut également être utilisée pour convertir le paramètre lParam en une structure [**points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f7971-166">The [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro can also be used to convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="f7971-167">La fonction [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) peut être utilisée pour déterminer les États des touches de modification du clavier associées à ce message.</span><span class="sxs-lookup"><span data-stu-id="f7971-167">The [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function can be used to determine the keyboard modifier key states associated with this message.</span></span> <span data-ttu-id="f7971-168">Par exemple, pour détecter que la touche ALT a été enfoncée, vérifiez si **GetKeyState**(VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f7971-168">For example, to detect that the ALT key was pressed, check whether **GetKeyState**(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="f7971-169">Si l’application ne traite pas ce message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) peut générer un ou plusieurs messages [**WM_GESTURE**](../wintouch/wm-gesture.md)si la séquence d’entrée de ce et, éventuellement, d’autres pointeurs est reconnue comme un geste.</span><span class="sxs-lookup"><span data-stu-id="f7971-169">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md)messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="f7971-170">Si un mouvement n’est pas reconnu, **DefWindowProc** peut générer une entrée de souris.</span><span class="sxs-lookup"><span data-stu-id="f7971-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="f7971-171">Si une application consomme de manière sélective une entrée de pointeur et passe le reste à [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), le comportement résultant n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f7971-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="f7971-172">Utilisez la fonction [**GetPointerInfo**](/previous-versions/windows/desktop/api) pour récupérer des informations supplémentaires relatives à ce message.</span><span class="sxs-lookup"><span data-stu-id="f7971-172">Use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function to retrieve further information related to this message.</span></span>

## <a name="examples"></a><span data-ttu-id="f7971-173">Exemples</span><span class="sxs-lookup"><span data-stu-id="f7971-173">Examples</span></span>

<span data-ttu-id="f7971-174">L’exemple de code suivant montre comment récupérer la position x et y du pointeur associé à ce message.</span><span class="sxs-lookup"><span data-stu-id="f7971-174">The following code example shows how to retrieve the x and y position of the pointer associated witht this message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

// process pointer up, similar to mouse button up
```



<span data-ttu-id="f7971-175">L’exemple de code suivant montre comment obtenir l’ID de pointeur associé à ce message.</span><span class="sxs-lookup"><span data-stu-id="f7971-175">The following code example shows how to obtain the pointer id associated with this message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    
// failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}


```



<span data-ttu-id="f7971-176">L’exemple de code suivant montre comment gérer différents types de pointeur associés à ce message.</span><span class="sxs-lookup"><span data-stu-id="f7971-176">The following code example shows how to handle different pointer types associated with this message.</span></span>


```c++
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a><span data-ttu-id="f7971-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7971-177">Requirements</span></span>



| <span data-ttu-id="f7971-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7971-178">Requirement</span></span> | <span data-ttu-id="f7971-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7971-179">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7971-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7971-180">Minimum supported client</span></span><br/> | <span data-ttu-id="f7971-181">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7971-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f7971-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7971-182">Minimum supported server</span></span><br/> | <span data-ttu-id="f7971-183">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7971-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7971-184">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7971-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7971-185"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7971-185"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7971-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7971-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7971-187">Messages</span><span class="sxs-lookup"><span data-stu-id="f7971-187">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="f7971-188">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f7971-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7971-189">**Indicateurs de pointeur**</span><span class="sxs-lookup"><span data-stu-id="f7971-189">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="f7971-190">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-190">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-191">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-191">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-192">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-192">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-193">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-193">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-194">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-194">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-195">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-195">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-196">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-196">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-197">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-197">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-198">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-198">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="f7971-199">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="f7971-199">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>
