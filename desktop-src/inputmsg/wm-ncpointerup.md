---
title: Message WM_NCPOINTERUP
description: Publié lorsqu’un pointeur qui a effectué le contact sur la zone non cliente d’une fenêtre interrompt le contact.
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUP les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742573"
---
# <a name="wm_ncpointerup-message"></a><span data-ttu-id="44410-104">Message WM_NCPOINTERUP</span><span class="sxs-lookup"><span data-stu-id="44410-104">WM_NCPOINTERUP message</span></span>

<span data-ttu-id="44410-105">Publié lorsqu’un pointeur qui a effectué le contact sur la zone non cliente d’une fenêtre interrompt le contact.</span><span class="sxs-lookup"><span data-stu-id="44410-105">Posted when a pointer that made contact over the non-client area of a window breaks contact.</span></span> <span data-ttu-id="44410-106">Le message cible la fenêtre sur laquelle le pointeur crée un contact et le pointeur est, à ce stade, capturé implicitement dans la fenêtre afin que la fenêtre continue de recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact, y compris la notification **WM_NCPOINTERUP** .</span><span class="sxs-lookup"><span data-stu-id="44410-106">The message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact, including the **WM_NCPOINTERUP** notification.</span></span>

<span data-ttu-id="44410-107">Si une fenêtre a capturé ce pointeur, ce message n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="44410-107">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="44410-108">Au lieu de cela, un [**WM_POINTERUP**](wm-pointerup.md) est publié dans la fenêtre qui a capturé ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="44410-108">Instead, a [**WM_POINTERUP**](wm-pointerup.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="44410-109">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="44410-109">\[!Important\]</span></span>  
> <span data-ttu-id="44410-110">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="44410-110">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="44410-111">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="44410-111">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="44410-112">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="44410-112">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="44410-113">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44410-113">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a><span data-ttu-id="44410-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44410-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44410-115">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44410-115">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44410-116">Contient l’identificateur du pointeur et des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="44410-116">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="44410-117">Utilisez les macros suivantes pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="44410-117">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="44410-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur de pointeur</span><span class="sxs-lookup"><span data-stu-id="44410-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="44410-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam) : valeur de test de positionnement retournée par le traitement du message de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="44410-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="44410-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44410-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44410-121">Contient l’emplacement du point du pointeur.</span><span class="sxs-lookup"><span data-stu-id="44410-121">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="44410-122">Étant donné que le pointeur peut établir un contact avec l’appareil sur une zone non triviale, cet emplacement de point peut être une simplification d’une zone de pointeur plus complexe.</span><span class="sxs-lookup"><span data-stu-id="44410-122">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="44410-123">Dans la mesure du possible, une application doit utiliser les informations complètes de la zone du pointeur à la place de l’emplacement du point.</span><span class="sxs-lookup"><span data-stu-id="44410-123">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="44410-124">Utilisez les macros suivantes pour récupérer les coordonnées d’écran physiques du point.</span><span class="sxs-lookup"><span data-stu-id="44410-124">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="44410-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam) : coordonnée X (point horizontal).</span><span class="sxs-lookup"><span data-stu-id="44410-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="44410-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam) : coordonnée Y (point vertical).</span><span class="sxs-lookup"><span data-stu-id="44410-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44410-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44410-127">Return value</span></span>

<span data-ttu-id="44410-128">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="44410-128">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="44410-129">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="44410-129">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="44410-130">Notes</span><span class="sxs-lookup"><span data-stu-id="44410-130">Remarks</span></span>

<span data-ttu-id="44410-131">Si l’application ne traite pas ce message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) peut effectuer une ou plusieurs actions système en fonction du résultat du test de positionnement inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="44410-131">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="44410-132">En règle générale, les applications ne doivent pas avoir à gérer ce message.</span><span class="sxs-lookup"><span data-stu-id="44410-132">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="44410-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44410-133">Requirements</span></span>



| <span data-ttu-id="44410-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44410-134">Requirement</span></span> | <span data-ttu-id="44410-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="44410-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44410-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44410-136">Minimum supported client</span></span><br/> | <span data-ttu-id="44410-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44410-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="44410-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44410-138">Minimum supported server</span></span><br/> | <span data-ttu-id="44410-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44410-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44410-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="44410-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="44410-141"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44410-141"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44410-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44410-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44410-143">Messages</span><span class="sxs-lookup"><span data-stu-id="44410-143">Messages</span></span>](messages.md)
</dt> </dl>

 

