---
title: Message WM_PARENTNOTIFY
description: Envoyé à une fenêtre lorsqu’une action importante se produit dans une fenêtre descendante.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508937"
---
# <a name="wm_parentnotify-message"></a><span data-ttu-id="43808-104">Message WM_PARENTNOTIFY</span><span class="sxs-lookup"><span data-stu-id="43808-104">WM_PARENTNOTIFY message</span></span>

<span data-ttu-id="43808-105">Envoyé à une fenêtre lorsqu’une action importante se produit dans une fenêtre descendante.</span><span class="sxs-lookup"><span data-stu-id="43808-105">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="43808-106">Ce message est maintenant étendu pour inclure l’événement [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="43808-106">This message is now extended to include the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span> <span data-ttu-id="43808-107">Lorsque la fenêtre enfant est créée, le système envoie [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) juste avant la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) qui crée la fenêtre retourne.</span><span class="sxs-lookup"><span data-stu-id="43808-107">When the child window is being created, the system sends [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="43808-108">Lorsque la fenêtre enfant est détruite, le système envoie le message avant tout traitement pour détruire la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="43808-108">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span>

<span data-ttu-id="43808-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="43808-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="43808-110">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="43808-110">\[!Important\]</span></span>  
> <span data-ttu-id="43808-111">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="43808-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="43808-112">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="43808-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="43808-113">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="43808-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="43808-114">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43808-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a><span data-ttu-id="43808-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43808-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43808-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43808-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43808-117">Le mot de poids faible de *wParam* spécifie l’événement pour lequel le parent est notifié.</span><span class="sxs-lookup"><span data-stu-id="43808-117">The low-order word of *wParam* specifies the event for which the parent is being notified.</span></span> <span data-ttu-id="43808-118">La valeur du mot de poids fort dépend de la valeur du mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="43808-118">The value of the high-order word depends on the value of the low-order word.</span></span> <span data-ttu-id="43808-119">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="43808-119">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="43808-120">LOWORD (*wParam*)</span><span class="sxs-lookup"><span data-stu-id="43808-120">LOWORD(*wParam*)</span></span>                                                                                                                                                                                                             | <span data-ttu-id="43808-121">Signification</span><span class="sxs-lookup"><span data-stu-id="43808-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <span data-ttu-id="43808-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="43808-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span></span> </dl>                | <span data-ttu-id="43808-123">La fenêtre enfant est en cours de création.</span><span class="sxs-lookup"><span data-stu-id="43808-123">The child window is being created.</span></span><br/> <span data-ttu-id="43808-124">HIWORD (*wParam*) est l’identificateur de la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="43808-124">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="43808-125">*lParam* est un handle de la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="43808-125">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <span data-ttu-id="43808-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="43808-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span></span> </dl>             | <span data-ttu-id="43808-127">La fenêtre enfant est en cours de destruction.</span><span class="sxs-lookup"><span data-stu-id="43808-127">The child window is being destroyed.</span></span><br/> <span data-ttu-id="43808-128">HIWORD (*wParam*) est l’identificateur de la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="43808-128">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="43808-129">*lParam* est un handle de la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="43808-129">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <span data-ttu-id="43808-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span><span class="sxs-lookup"><span data-stu-id="43808-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span></span> </dl> | <span data-ttu-id="43808-131">L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="43808-131">The user has placed the cursor over the child window and has clicked the left mouse button.</span></span><br/> <span data-ttu-id="43808-132">HIWORD (*wParam*) n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="43808-132">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="43808-133">*lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="43808-133">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <span data-ttu-id="43808-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span><span class="sxs-lookup"><span data-stu-id="43808-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span></span> </dl> | <span data-ttu-id="43808-135">L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le bouton central de la souris.</span><span class="sxs-lookup"><span data-stu-id="43808-135">The user has placed the cursor over the child window and has clicked the middle mouse button.</span></span><br/> <span data-ttu-id="43808-136">HIWORD (*wParam*) n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="43808-136">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="43808-137">*lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="43808-137">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <span data-ttu-id="43808-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span><span class="sxs-lookup"><span data-stu-id="43808-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span></span> </dl> | <span data-ttu-id="43808-139">L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="43808-139">The user has placed the cursor over the child window and has clicked the right mouse button.</span></span><br/> <span data-ttu-id="43808-140">HIWORD (*wParam*) n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="43808-140">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="43808-141">*lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="43808-141">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <span data-ttu-id="43808-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span><span class="sxs-lookup"><span data-stu-id="43808-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span></span> </dl> | <span data-ttu-id="43808-143">L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le premier ou le second bouton X.</span><span class="sxs-lookup"><span data-stu-id="43808-143">The user has placed the cursor over the child window and has clicked the first or second X button.</span></span><br/> <span data-ttu-id="43808-144">HIWORD (*wParam*) indique le bouton qui a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="43808-144">HIWORD(*wParam*) indicates which button was pressed.</span></span> <span data-ttu-id="43808-145">Ce paramètre peut prendre l’une des valeurs suivantes : le bouton XButton1 ou XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="43808-145">This parameter can be one of the following values: XBUTTON1 or XBUTTON2.</span></span><br/> <span data-ttu-id="43808-146">*lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="43808-146">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <span data-ttu-id="43808-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span><span class="sxs-lookup"><span data-stu-id="43808-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span></span> </dl> | <span data-ttu-id="43808-148">Un pointeur a effectué un contact avec la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="43808-148">A pointer has made contact with the child window.</span></span><br/> <span data-ttu-id="43808-149">HIWORD (*wParam*) contient l’identificateur du pointeur qui a généré l’événement [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="43808-149">HIWORD(*wParam*) contains the identifier of the pointer that generated the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span><br/>                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="43808-150">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43808-150">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43808-151">Contient l’emplacement du point du pointeur.</span><span class="sxs-lookup"><span data-stu-id="43808-151">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="43808-152">Étant donné que le pointeur peut établir un contact avec l’appareil sur une zone non triviale, cet emplacement de point peut être une simplification d’une zone de pointeur plus complexe.</span><span class="sxs-lookup"><span data-stu-id="43808-152">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="43808-153">Dans la mesure du possible, une application doit utiliser les informations complètes de la zone du pointeur à la place de l’emplacement du point.</span><span class="sxs-lookup"><span data-stu-id="43808-153">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="43808-154">Utilisez les macros suivantes pour récupérer les coordonnées d’écran physiques du point.</span><span class="sxs-lookup"><span data-stu-id="43808-154">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="43808-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam) : coordonnée X (point horizontal).</span><span class="sxs-lookup"><span data-stu-id="43808-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="43808-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam) : coordonnée Y (point vertical).</span><span class="sxs-lookup"><span data-stu-id="43808-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43808-157">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43808-157">Return value</span></span>

<span data-ttu-id="43808-158">Si l’application traite ce message, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="43808-158">If the application processes this message, it returns zero.</span></span>

<span data-ttu-id="43808-159">Si l’application ne traite pas ce message, elle appelle [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="43808-159">If the application does not process this message, it calls [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="43808-160">Notes</span><span class="sxs-lookup"><span data-stu-id="43808-160">Remarks</span></span>

<span data-ttu-id="43808-161">Ce message est également envoyé à toutes les fenêtres ancêtres de la fenêtre enfant, y compris la fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="43808-161">This message is also sent to all ancestor windows of the child window, including the top-level window.</span></span>

<span data-ttu-id="43808-162">Toutes les fenêtres enfants, à l’exception de celles qui ont le **WS_EX_NOPARENTNOTIFY** style de fenêtre étendu, envoient ce message à leurs fenêtres parentes.</span><span class="sxs-lookup"><span data-stu-id="43808-162">All child windows, except those that have the **WS_EX_NOPARENTNOTIFY** extended window style, send this message to their parent windows.</span></span> <span data-ttu-id="43808-163">Par défaut, les fenêtres enfants dans une boîte de dialogue ont le style **WS_EX_NOPARENTNOTIFY** , à moins que la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) soit appelée pour créer la fenêtre enfant sans ce style.</span><span class="sxs-lookup"><span data-stu-id="43808-163">By default, child windows in a dialog box have the **WS_EX_NOPARENTNOTIFY** style, unless the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function is called to create the child window without this style.</span></span>

<span data-ttu-id="43808-164">Cette notification fournit aux fenêtres ancêtres de la fenêtre enfant l’opportunité d’examiner les informations de pointeur et, si nécessaire, de capturer le pointeur à l’aide des fonctions de capture de pointeur.</span><span class="sxs-lookup"><span data-stu-id="43808-164">This notification provides the child window's ancestor windows an opportunity to examine the pointer information and, if required, capture the pointer using the pointer capture functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="43808-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43808-165">Requirements</span></span>



| <span data-ttu-id="43808-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43808-166">Requirement</span></span> | <span data-ttu-id="43808-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="43808-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43808-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43808-168">Minimum supported client</span></span><br/> | <span data-ttu-id="43808-169">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43808-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="43808-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43808-170">Minimum supported server</span></span><br/> | <span data-ttu-id="43808-171">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43808-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="43808-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="43808-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="43808-173"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43808-173"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43808-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43808-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43808-175">Messages</span><span class="sxs-lookup"><span data-stu-id="43808-175">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="43808-176">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="43808-176">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="43808-177">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="43808-177">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

<span data-ttu-id="43808-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43808-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="43808-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43808-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="43808-180">**WM_CREATE**</span><span class="sxs-lookup"><span data-stu-id="43808-180">**WM_CREATE**</span></span>](../winmsg/wm-create.md)
</dt> <dt>

[<span data-ttu-id="43808-181">**WM_DESTROY**</span><span class="sxs-lookup"><span data-stu-id="43808-181">**WM_DESTROY**</span></span>](../winmsg/wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="43808-182">**WM_LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="43808-182">**WM_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="43808-183">**WM_MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="43808-183">**WM_MBUTTONDOWN**</span></span>](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="43808-184">**WM_RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="43808-184">**WM_RBUTTONDOWN**</span></span>](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="43808-185">**WM_XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="43808-185">**WM_XBUTTONDOWN**</span></span>](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

