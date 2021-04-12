---
description: Envoyé lorsque l’arrière-plan de la fenêtre doit être effacé (par exemple, lorsqu’une fenêtre est redimensionnée). Le message est envoyé pour préparer une partie invalidée d’une fenêtre pour la peinture.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Message WM_ERASEBKGND (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203797"
---
# <a name="wm_erasebkgnd-message"></a><span data-ttu-id="ccc92-104">\_Message WM ERASEBKGND</span><span class="sxs-lookup"><span data-stu-id="ccc92-104">WM\_ERASEBKGND message</span></span>

<span data-ttu-id="ccc92-105">Envoyé lorsque l’arrière-plan de la fenêtre doit être effacé (par exemple, lorsqu’une fenêtre est redimensionnée).</span><span class="sxs-lookup"><span data-stu-id="ccc92-105">Sent when the window background must be erased (for example, when a window is resized).</span></span> <span data-ttu-id="ccc92-106">Le message est envoyé pour préparer une partie invalidée d’une fenêtre pour la peinture.</span><span class="sxs-lookup"><span data-stu-id="ccc92-106">The message is sent to prepare an invalidated portion of a window for painting.</span></span>


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a><span data-ttu-id="ccc92-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccc92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc92-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccc92-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc92-109">Handle vers le contexte de périphérique (Device Context).</span><span class="sxs-lookup"><span data-stu-id="ccc92-109">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="ccc92-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccc92-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc92-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ccc92-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc92-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ccc92-112">Return value</span></span>

<span data-ttu-id="ccc92-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ccc92-113">Type: **LRESULT**</span></span>

<span data-ttu-id="ccc92-114">Une application doit retourner une valeur différente de zéro si elle efface l’arrière-plan ; Sinon, elle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="ccc92-114">An application should return nonzero if it erases the background; otherwise, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc92-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ccc92-115">Remarks</span></span>

<span data-ttu-id="ccc92-116">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) efface l’arrière-plan à l’aide du pinceau d’arrière-plan de classe spécifié par le membre **hbrBackground** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) .</span><span class="sxs-lookup"><span data-stu-id="ccc92-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function erases the background by using the class background brush specified by the **hbrBackground** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="ccc92-117">Si **hbrBackground** a la **valeur null**, l’application doit traiter le message **WM \_ ERASEBKGND** et effacer l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ccc92-117">If **hbrBackground** is **NULL**, the application should process the **WM\_ERASEBKGND** message and erase the background.</span></span>

<span data-ttu-id="ccc92-118">Une application doit retourner une valeur différente de zéro en réponse à **WM \_ ERASEBKGND** si elle traite le message et efface l’arrière-plan. cela indique qu’aucune suppression supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="ccc92-118">An application should return nonzero in response to **WM\_ERASEBKGND** if it processes the message and erases the background; this indicates that no further erasing is required.</span></span> <span data-ttu-id="ccc92-119">Si l’application retourne la valeur zéro, la fenêtre reste marquée pour l’effacement.</span><span class="sxs-lookup"><span data-stu-id="ccc92-119">If the application returns zero, the window will remain marked for erasing.</span></span> <span data-ttu-id="ccc92-120">(En général, cela indique que le membre **fErase** de la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) est **true**.)</span><span class="sxs-lookup"><span data-stu-id="ccc92-120">(Typically, this indicates that the **fErase** member of the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure will be **TRUE**.)</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc92-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccc92-121">Requirements</span></span>



| <span data-ttu-id="ccc92-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccc92-122">Requirement</span></span> | <span data-ttu-id="ccc92-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccc92-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc92-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccc92-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc92-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccc92-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ccc92-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccc92-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc92-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccc92-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccc92-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccc92-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc92-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccc92-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc92-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccc92-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccc92-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ccc92-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ccc92-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ccc92-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ccc92-133">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="ccc92-133">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

<span data-ttu-id="ccc92-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ccc92-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ccc92-135">Icônes</span><span class="sxs-lookup"><span data-stu-id="ccc92-135">Icons</span></span>](../menurc/icons.md)
</dt> <dt>

<span data-ttu-id="ccc92-136">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="ccc92-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ccc92-137">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="ccc92-137">**BeginPaint**</span></span>](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="ccc92-138">**PAINTSTRUCT,**</span><span class="sxs-lookup"><span data-stu-id="ccc92-138">**PAINTSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
