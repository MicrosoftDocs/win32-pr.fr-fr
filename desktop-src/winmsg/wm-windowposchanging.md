---
description: Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan est sur le point de changer à la suite d’un appel à la fonction SetWindowPos ou à une autre fonction de gestion de fenêtre.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Message WM_WINDOWPOSCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758463"
---
# <a name="wm_windowposchanging-message"></a><span data-ttu-id="6c9a6-103">\_Message WM WINDOWPOSCHANGING</span><span class="sxs-lookup"><span data-stu-id="6c9a6-103">WM\_WINDOWPOSCHANGING message</span></span>

<span data-ttu-id="6c9a6-104">Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan est sur le point de changer à la suite d’un appel à la fonction [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou à une autre fonction de gestion de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-104">Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="6c9a6-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6c9a6-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a><span data-ttu-id="6c9a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c9a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c9a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c9a6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c9a6-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6c9a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c9a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c9a6-110">Pointeur vers une structure [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) qui contient des informations sur les nouvelles taille et position de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c9a6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c9a6-111">Return value</span></span>

<span data-ttu-id="6c9a6-112">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-112">Type: **LRESULT**</span></span>

<span data-ttu-id="6c9a6-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c9a6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6c9a6-114">Remarks</span></span>

<span data-ttu-id="6c9a6-115">Pour une fenêtre avec le [**style \_ WS Overlapped**](window-styles.md) ou **WS \_ THICKFRAME** , la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie le message [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-115">For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window.</span></span> <span data-ttu-id="6c9a6-116">Cela permet de valider la nouvelle taille et la position de la fenêtre et d’appliquer les styles du client [cs \_ BYTEALIGNCLIENT](about-window-classes.md) et CS \_ BYTEALIGNWINDOW.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-116">This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md) and CS\_BYTEALIGNWINDOW client styles.</span></span> <span data-ttu-id="6c9a6-117">Si vous ne transmettez pas le message **WM \_ WINDOWPOSCHANGING** à la fonction **DefWindowProc** , une application peut remplacer ces valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-117">By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.</span></span>

<span data-ttu-id="6c9a6-118">Pendant le traitement de ce message, la modification de l’une des valeurs dans [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affecte la nouvelle taille, la position ou l’emplacement de la fenêtre dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-118">While this message is being processed, modifying any of the values in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affects the window's new size, position, or place in the Z order.</span></span> <span data-ttu-id="6c9a6-119">Une application peut empêcher les modifications apportées à la fenêtre en définissant ou en effaçant les bits appropriés dans le membre **Flags** de **WINDOWPOS**.</span><span class="sxs-lookup"><span data-stu-id="6c9a6-119">An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c9a6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c9a6-120">Requirements</span></span>



| <span data-ttu-id="6c9a6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c9a6-121">Requirement</span></span> | <span data-ttu-id="6c9a6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c9a6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9a6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9a6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9a6-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c9a6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c9a6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9a6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9a6-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c9a6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c9a6-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c9a6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c9a6-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c9a6-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c9a6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c9a6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c9a6-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c9a6-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6c9a6-132">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-132">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="6c9a6-133">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-133">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="6c9a6-134">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-134">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="6c9a6-135">**\_GETMINMAXINFO WM**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-135">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md)
</dt> <dt>

[<span data-ttu-id="6c9a6-136">**déplacement de WM \_**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-136">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="6c9a6-137">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-137">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="6c9a6-138">**\_WINDOWPOSCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-138">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="6c9a6-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6c9a6-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c9a6-140">Windows</span><span class="sxs-lookup"><span data-stu-id="6c9a6-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
