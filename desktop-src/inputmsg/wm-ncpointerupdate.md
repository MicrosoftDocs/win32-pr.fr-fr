---
title: Message WM_NCPOINTERUPDATE
description: Publié pour fournir une mise à jour sur un pointeur qui a effectué un contact sur la zone non cliente d’une fenêtre ou lorsqu’un contact de pointage non capturé se déplace au-dessus de la zone non cliente d’une fenêtre.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUPDATE les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 09ef5fd6f3b7378a963be4278f1fabdf0f6ab351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384412"
---
# <a name="wm_ncpointerupdate-message"></a><span data-ttu-id="f4775-104">Message WM_NCPOINTERUPDATE</span><span class="sxs-lookup"><span data-stu-id="f4775-104">WM_NCPOINTERUPDATE message</span></span>

<span data-ttu-id="f4775-105">Publié pour fournir une mise à jour sur un pointeur qui a effectué un contact sur la zone non cliente d’une fenêtre ou lorsqu’un contact de pointage non capturé se déplace au-dessus de la zone non cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f4775-105">Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window.</span></span> <span data-ttu-id="f4775-106">Pendant que le pointeur pointe, le message cible la fenêtre sur laquelle le pointeur se trouve.</span><span class="sxs-lookup"><span data-stu-id="f4775-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="f4775-107">Tandis que le pointeur est en contact avec la surface, le pointeur est capturé implicitement dans la fenêtre sur laquelle le pointeur a été contacté et cette fenêtre continue à recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact.</span><span class="sxs-lookup"><span data-stu-id="f4775-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="f4775-108">Si une fenêtre a capturé ce pointeur, ce message n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="f4775-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="f4775-109">Au lieu de cela, un [**WM_POINTERUPDATE**](wm-pointerupdate.md) est publié dans la fenêtre qui a capturé ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="f4775-109">Instead, a [**WM_POINTERUPDATE**](wm-pointerupdate.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="f4775-110">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="f4775-110">\[!Important\]</span></span>  
> <span data-ttu-id="f4775-111">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="f4775-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="f4775-112">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="f4775-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="f4775-113">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="f4775-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="f4775-114">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f4775-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a><span data-ttu-id="f4775-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4775-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4775-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4775-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4775-117">Contient l’identificateur du pointeur et des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f4775-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="f4775-118">Utilisez les macros suivantes pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="f4775-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="f4775-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur de pointeur</span><span class="sxs-lookup"><span data-stu-id="f4775-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="f4775-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam) : valeur de test de positionnement retournée par le traitement du message de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="f4775-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="f4775-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4775-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4775-122">Contient l’emplacement du point du pointeur.</span><span class="sxs-lookup"><span data-stu-id="f4775-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="f4775-123">Étant donné que le pointeur peut établir un contact avec l’appareil sur une zone non triviale, cet emplacement de point peut être une simplification d’une zone de pointeur plus complexe.</span><span class="sxs-lookup"><span data-stu-id="f4775-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="f4775-124">Dans la mesure du possible, une application doit utiliser les informations complètes de la zone du pointeur à la place de l’emplacement du point.</span><span class="sxs-lookup"><span data-stu-id="f4775-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="f4775-125">Utilisez les macros suivantes pour récupérer les coordonnées d’écran physiques du point.</span><span class="sxs-lookup"><span data-stu-id="f4775-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="f4775-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam) : coordonnée X (point horizontal).</span><span class="sxs-lookup"><span data-stu-id="f4775-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="f4775-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam) : coordonnée Y (point vertical).</span><span class="sxs-lookup"><span data-stu-id="f4775-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4775-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4775-128">Return value</span></span>

<span data-ttu-id="f4775-129">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="f4775-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="f4775-130">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="f4775-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4775-131">Notes</span><span class="sxs-lookup"><span data-stu-id="f4775-131">Remarks</span></span>

<span data-ttu-id="f4775-132">Si l’application ne traite pas ce message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) peut effectuer une ou plusieurs actions système en fonction du résultat du test de positionnement inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="f4775-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="f4775-133">En règle générale, les applications ne doivent pas avoir à gérer ce message.</span><span class="sxs-lookup"><span data-stu-id="f4775-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4775-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4775-134">Requirements</span></span>



| <span data-ttu-id="f4775-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4775-135">Requirement</span></span> | <span data-ttu-id="f4775-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4775-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4775-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4775-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f4775-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4775-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f4775-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4775-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f4775-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4775-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f4775-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4775-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4775-142"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4775-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4775-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4775-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4775-144">Messages</span><span class="sxs-lookup"><span data-stu-id="f4775-144">Messages</span></span>](messages.md)
</dt> </dl>

 

