---
title: Message WM_VSCROLL (winuser. h)
description: Le \_ message WM VSCROLL est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement verticale standard de la fenêtre.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106153"
---
# <a name="wm_vscroll-message"></a><span data-ttu-id="52d34-104">\_Message WM VSCROLL</span><span class="sxs-lookup"><span data-stu-id="52d34-104">WM\_VSCROLL message</span></span>

<span data-ttu-id="52d34-105">Le message **WM \_ VSCROLL** est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement verticale standard de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="52d34-105">The **WM\_VSCROLL** message is sent to a window when a scroll event occurs in the window's standard vertical scroll bar.</span></span> <span data-ttu-id="52d34-106">Ce message est également envoyé au propriétaire d’un contrôle de barre de défilement vertical lorsqu’un événement de défilement se produit dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="52d34-106">This message is also sent to the owner of a vertical scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="52d34-107">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="52d34-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="52d34-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52d34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d34-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52d34-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52d34-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle de la case de défilement si le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est SB \_ THUMBPOSITION ou SB \_ THUMBTRACK ; dans le cas contraire, ce mot n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="52d34-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="52d34-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie une valeur de barre de défilement qui indique la requête de défilement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52d34-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="52d34-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="52d34-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="52d34-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d34-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="52d34-114">Signification</span><span class="sxs-lookup"><span data-stu-id="52d34-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="52d34-115"><dt>**\_bord inférieur SB**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-115"><dt>**SB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="52d34-116">Fait défiler vers le bas à droite.</span><span class="sxs-lookup"><span data-stu-id="52d34-116">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="52d34-117"><dt>**\_ENDSCROLL SB**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-117"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="52d34-118">Termine le défilement.</span><span class="sxs-lookup"><span data-stu-id="52d34-118">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="52d34-119"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-119"><dt>**SB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="52d34-120">Fait défiler d’une ligne vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="52d34-120">Scrolls one line down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="52d34-121"><dt>**\_gamme SB**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-121"><dt>**SB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="52d34-122">Fait défiler d’une ligne vers le haut.</span><span class="sxs-lookup"><span data-stu-id="52d34-122">Scrolls one line up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="52d34-123"><dt>**SB \_ PG.**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-123"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="52d34-124">Fait défiler une page vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="52d34-124">Scrolls one page down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="52d34-125"><dt>**SB \_ PG PRÉC**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-125"><dt>**SB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="52d34-126">Fait défiler d’une page vers le haut.</span><span class="sxs-lookup"><span data-stu-id="52d34-126">Scrolls one page up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="52d34-127"><dt>**\_THUMBPOSITION SB**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-127"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="52d34-128">L’utilisateur a fait glisser la case de défilement (Thumb) et relâché le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="52d34-128">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="52d34-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position de la case de défilement à la fin de l’opération glisser.</span><span class="sxs-lookup"><span data-stu-id="52d34-129">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="52d34-130"><dt>**\_THUMBTRACK SB**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-130"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="52d34-131">L’utilisateur fait glisser la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="52d34-131">The user is dragging the scroll box.</span></span> <span data-ttu-id="52d34-132">Ce message est envoyé à plusieurs reprises jusqu’à ce que l’utilisateur relâche le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="52d34-132">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="52d34-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position vers laquelle la case de défilement a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="52d34-133">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="52d34-134"><dt>**haut de la SB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-134"><dt>**SB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="52d34-135">Fait défiler vers le haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="52d34-135">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="52d34-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52d34-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52d34-137">Si le message est envoyé par un contrôle de barre de défilement, ce paramètre est le handle du contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="52d34-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="52d34-138">Si le message est envoyé par une barre de défilement standard, ce paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="52d34-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d34-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52d34-139">Return value</span></span>

<span data-ttu-id="52d34-140">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="52d34-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d34-141">Notes</span><span class="sxs-lookup"><span data-stu-id="52d34-141">Remarks</span></span>

<span data-ttu-id="52d34-142">Le \_ Code de demande SB THUMBTRACK est généralement utilisé par les applications qui fournissent des commentaires au fur et à mesure que l’utilisateur fait glisser la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="52d34-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="52d34-143">Si une application fait défiler le contenu de la fenêtre, elle doit également réinitialiser la position de la case de défilement à l’aide de la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="52d34-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="52d34-144">Notez que le message **WM \_ VSCROLL** contient uniquement 16 bits de données de position de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="52d34-144">Note that the **WM\_VSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="52d34-145">Ainsi, les applications qui reposent uniquement sur **WM \_ VSCROLL** (et [**WM \_ HSCROLL**](wm-hscroll.md)) pour les données de position de défilement ont une valeur de position maximale pratique de 65 535.</span><span class="sxs-lookup"><span data-stu-id="52d34-145">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="52d34-146">Toutefois, étant donné que les fonctions [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)et [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) prennent en charge les données de position de la barre de défilement 32 bits, il existe un moyen de contourner la barrière de 16 bits des messages [**WM \_ HSCROLL**](wm-hscroll.md) et **WM \_ VSCROLL** .</span><span class="sxs-lookup"><span data-stu-id="52d34-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the [**WM\_HSCROLL**](wm-hscroll.md) and **WM\_VSCROLL** messages.</span></span> <span data-ttu-id="52d34-147">Pour obtenir une description de la technique, consultez **GetScrollInfo** .</span><span class="sxs-lookup"><span data-stu-id="52d34-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d34-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52d34-148">Requirements</span></span>



| <span data-ttu-id="52d34-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52d34-149">Requirement</span></span> | <span data-ttu-id="52d34-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d34-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52d34-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d34-151">Minimum supported client</span></span><br/> | <span data-ttu-id="52d34-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d34-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52d34-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d34-153">Minimum supported server</span></span><br/> | <span data-ttu-id="52d34-154">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d34-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52d34-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="52d34-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d34-156"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52d34-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d34-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52d34-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="52d34-158">**Référence**</span><span class="sxs-lookup"><span data-stu-id="52d34-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52d34-159">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="52d34-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="52d34-160">**GetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="52d34-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="52d34-161">**GetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="52d34-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="52d34-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="52d34-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="52d34-163">**SetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="52d34-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="52d34-164">**SetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="52d34-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="52d34-165">**\_HSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="52d34-165">**WM\_HSCROLL**</span></span>](wm-hscroll.md)
</dt> <dt>

[<span data-ttu-id="52d34-166">**WM \_ VSCROLL (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="52d34-166">**WM\_VSCROLL (Trackbar)**</span></span>](wm-vscroll--trackbar-.md)
</dt> </dl>

 

