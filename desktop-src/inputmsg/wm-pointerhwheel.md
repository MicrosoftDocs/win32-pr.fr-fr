---
title: Message WM_POINTERHWHEEL
description: Publié dans la fenêtre avec le focus clavier de premier plan quand une roulette de défilement horizontale est pivotée.
ms.assetid: 6eec37da-2200-4be1-bf0b-44504caa1320
keywords:
- WM_POINTERHWHEEL les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_NCPOINTERCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5817d5ed243363c82038dc3df2d8f1e337079076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385028"
---
# <a name="wm_pointerhwheel-message"></a><span data-ttu-id="d67ce-104">Message WM_POINTERHWHEEL</span><span class="sxs-lookup"><span data-stu-id="d67ce-104">WM_POINTERHWHEEL message</span></span>

<span data-ttu-id="d67ce-105">Publié dans la fenêtre avec le focus clavier de premier plan quand une roulette de défilement horizontale est pivotée.</span><span class="sxs-lookup"><span data-stu-id="d67ce-105">Posted to the window with foreground keyboard focus when a horizontal scroll wheel is rotated.</span></span>

<span data-ttu-id="d67ce-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d67ce-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="d67ce-107">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="d67ce-107">\[!Important\]</span></span>  
> <span data-ttu-id="d67ce-108">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="d67ce-108">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="d67ce-109">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="d67ce-109">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="d67ce-110">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="d67ce-110">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="d67ce-111">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d67ce-111">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERHWHEEL            0x024F
```



## <a name="parameters"></a><span data-ttu-id="d67ce-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d67ce-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d67ce-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d67ce-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d67ce-114">Contient l’identificateur du pointeur et le delta du volant.</span><span class="sxs-lookup"><span data-stu-id="d67ce-114">Contains the pointer identifier and wheel delta.</span></span> <span data-ttu-id="d67ce-115">Utilisez les macros suivantes pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="d67ce-115">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="d67ce-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="d67ce-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="d67ce-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam) : roue Delta comme valeur abrégée signée.</span><span class="sxs-lookup"><span data-stu-id="d67ce-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): wheel delta as signed short value.</span></span>

</dd> <dt>

<span data-ttu-id="d67ce-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d67ce-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d67ce-119">Contient l’emplacement du point du pointeur.</span><span class="sxs-lookup"><span data-stu-id="d67ce-119">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="d67ce-120">Étant donné que le pointeur peut établir un contact avec l’appareil sur une zone non triviale, cet emplacement de point peut être une simplification d’une zone de pointeur plus complexe.</span><span class="sxs-lookup"><span data-stu-id="d67ce-120">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="d67ce-121">Dans la mesure du possible, une application doit utiliser les informations complètes de la zone du pointeur à la place de l’emplacement du point.</span><span class="sxs-lookup"><span data-stu-id="d67ce-121">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="d67ce-122">Utilisez les macros suivantes pour récupérer les coordonnées d’écran physiques du point.</span><span class="sxs-lookup"><span data-stu-id="d67ce-122">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="d67ce-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam) : coordonnée X (point horizontal).</span><span class="sxs-lookup"><span data-stu-id="d67ce-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="d67ce-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam) : coordonnée Y (point vertical).</span><span class="sxs-lookup"><span data-stu-id="d67ce-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d67ce-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d67ce-125">Return value</span></span>

<span data-ttu-id="d67ce-126">Si l’application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="d67ce-126">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="d67ce-127">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="d67ce-127">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="d67ce-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d67ce-128">Remarks</span></span>

<span data-ttu-id="d67ce-129">Pour récupérer les unités de défilement de la roue, utilisez le **inputData** de la structure retournée par l’appel de [**POINTER_INFO**](/previous-versions/windows/desktop/api) la fonction [**GetPointerInfo**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d67ce-129">To retrieve the wheel scroll units, use the **inputData** filed of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure returned by calling [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span> <span data-ttu-id="d67ce-130">Ce champ contient une valeur signée et est exprimé dans un multiple de **WHEEL_DELTA**.</span><span class="sxs-lookup"><span data-stu-id="d67ce-130">This field contains a signed value and is expressed in a multiple of **WHEEL_DELTA**.</span></span> <span data-ttu-id="d67ce-131">Une valeur positive indique une rotation vers l’avant et une valeur négative indique une rotation vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="d67ce-131">A positive value indicates a rotation forward and a negative value indicates a rotation backward.</span></span>

<span data-ttu-id="d67ce-132">Notez que les entrées de la roue peuvent être remises même si le curseur de la souris se trouve en dehors de la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="d67ce-132">Note that the wheel inputs may be delivered even if the mouse cursor is located outside of application s window.</span></span> <span data-ttu-id="d67ce-133">Les messages de roulette sont remis de manière très similaire aux entrées du clavier.</span><span class="sxs-lookup"><span data-stu-id="d67ce-133">The wheel messages are delivered in a way very similar to the keyboard inputs.</span></span> <span data-ttu-id="d67ce-134">La fenêtre de focus de la file d’attente de messages foregournd reçoit les messages de roulette.</span><span class="sxs-lookup"><span data-stu-id="d67ce-134">The focus window of the foregournd message queue receives the wheel messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="d67ce-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d67ce-135">Requirements</span></span>



| <span data-ttu-id="d67ce-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d67ce-136">Requirement</span></span> | <span data-ttu-id="d67ce-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d67ce-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d67ce-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d67ce-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d67ce-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d67ce-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d67ce-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d67ce-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d67ce-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d67ce-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d67ce-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="d67ce-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d67ce-143"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d67ce-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d67ce-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d67ce-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d67ce-145">Messages</span><span class="sxs-lookup"><span data-stu-id="d67ce-145">Messages</span></span>](messages.md)
</dt> </dl>

 

