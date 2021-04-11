---
title: Message WM_HSCROLL (winuser. h)
description: Le \_ message WM HSCROLL est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement horizontale standard de la fenêtre.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- WM_HSCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104422"
---
# <a name="wm_hscroll-message"></a><span data-ttu-id="9af88-104">\_Message WM HSCROLL</span><span class="sxs-lookup"><span data-stu-id="9af88-104">WM\_HSCROLL message</span></span>

<span data-ttu-id="9af88-105">Le message **WM \_ HSCROLL** est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement horizontale standard de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9af88-105">The **WM\_HSCROLL** message is sent to a window when a scroll event occurs in the window's standard horizontal scroll bar.</span></span> <span data-ttu-id="9af88-106">Ce message est également envoyé au propriétaire d’un contrôle de barre de défilement horizontale lorsqu’un événement de défilement se produit dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="9af88-106">This message is also sent to the owner of a horizontal scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="9af88-107">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9af88-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9af88-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9af88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9af88-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9af88-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle de la case de défilement si le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est SB \_ THUMBPOSITION ou SB \_ THUMBTRACK ; dans le cas contraire, ce mot n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9af88-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="9af88-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie une valeur de barre de défilement qui indique la requête de défilement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9af88-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="9af88-112">Ce mot peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9af88-112">This word can be one of the following values.</span></span>



| <span data-ttu-id="9af88-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9af88-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="9af88-114">Signification</span><span class="sxs-lookup"><span data-stu-id="9af88-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="9af88-115"><dt>**\_ENDSCROLL SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-115"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="9af88-116">Termine le défilement.</span><span class="sxs-lookup"><span data-stu-id="9af88-116">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="9af88-117"><dt>**SB \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-117"><dt>**SB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="9af88-118">Fait défiler vers le haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="9af88-118">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="9af88-119"><dt>**\_droit SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-119"><dt>**SB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="9af88-120">Fait défiler vers le bas à droite.</span><span class="sxs-lookup"><span data-stu-id="9af88-120">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="9af88-121"><dt>**\_LINELEFT SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-121"><dt>**SB\_LINELEFT**</dt></span></span> </dl>                | <span data-ttu-id="9af88-122">Fait défiler d’une unité vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="9af88-122">Scrolls left by one unit.</span></span><br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="9af88-123"><dt>**\_LINERIGHT SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-123"><dt>**SB\_LINERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="9af88-124">Fait défiler vers la droite d’une unité.</span><span class="sxs-lookup"><span data-stu-id="9af88-124">Scrolls right by one unit.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="9af88-125"><dt>**\_PAGELEFT SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-125"><dt>**SB\_PAGELEFT**</dt></span></span> </dl>                | <span data-ttu-id="9af88-126">Fait défiler vers la gauche de la largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9af88-126">Scrolls left by the width of the window.</span></span><br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="9af88-127"><dt>**\_ÉPINGLÉE SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-127"><dt>**SB\_PAGERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="9af88-128">Fait défiler la largeur de la fenêtre vers la droite.</span><span class="sxs-lookup"><span data-stu-id="9af88-128">Scrolls right by the width of the window.</span></span><br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="9af88-129"><dt>**\_THUMBPOSITION SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-129"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="9af88-130">L’utilisateur a fait glisser la case de défilement (Thumb) et relâché le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="9af88-130">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="9af88-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position de la case de défilement à la fin de l’opération glisser.</span><span class="sxs-lookup"><span data-stu-id="9af88-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="9af88-132"><dt>**\_THUMBTRACK SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-132"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="9af88-133">L’utilisateur fait glisser la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="9af88-133">The user is dragging the scroll box.</span></span> <span data-ttu-id="9af88-134">Ce message est envoyé à plusieurs reprises jusqu’à ce que l’utilisateur relâche le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="9af88-134">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="9af88-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position vers laquelle la case de défilement a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="9af88-135">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9af88-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9af88-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9af88-137">Si le message est envoyé par un contrôle de barre de défilement, ce paramètre est le handle du contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="9af88-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="9af88-138">Si le message est envoyé par une barre de défilement standard, ce paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9af88-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af88-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9af88-139">Return value</span></span>

<span data-ttu-id="9af88-140">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="9af88-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9af88-141">Notes</span><span class="sxs-lookup"><span data-stu-id="9af88-141">Remarks</span></span>

<span data-ttu-id="9af88-142">Le \_ Code de demande SB THUMBTRACK est généralement utilisé par les applications qui fournissent des commentaires au fur et à mesure que l’utilisateur fait glisser la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="9af88-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="9af88-143">Si une application fait défiler le contenu de la fenêtre, elle doit également réinitialiser la position de la case de défilement à l’aide de la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="9af88-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="9af88-144">Notez que le message **WM \_ HSCROLL** contient uniquement 16 bits de données de position de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="9af88-144">Note that the **WM\_HSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="9af88-145">Ainsi, les applications qui reposent uniquement sur **WM \_ HSCROLL** (et [**WM \_ VSCROLL**](wm-vscroll.md)) pour les données de position de défilement ont une valeur de position maximale pratique de 65 535.</span><span class="sxs-lookup"><span data-stu-id="9af88-145">Thus, applications that rely solely on **WM\_HSCROLL** (and [**WM\_VSCROLL**](wm-vscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="9af88-146">Toutefois, étant donné que les fonctions [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)et [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) prennent en charge les données de position de la barre de défilement 32 bits, il existe un moyen de contourner la barrière de 16 bits des messages **WM \_ HSCROLL** et [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="9af88-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the **WM\_HSCROLL** and [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span> <span data-ttu-id="9af88-147">Pour obtenir une description de la technique, consultez **GetScrollInfo** .</span><span class="sxs-lookup"><span data-stu-id="9af88-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="9af88-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9af88-148">Requirements</span></span>



| <span data-ttu-id="9af88-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9af88-149">Requirement</span></span> | <span data-ttu-id="9af88-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="9af88-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af88-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9af88-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9af88-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9af88-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9af88-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9af88-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9af88-154">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9af88-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9af88-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="9af88-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af88-156"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9af88-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af88-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9af88-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="9af88-158">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9af88-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9af88-159">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9af88-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="9af88-160">**GetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="9af88-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="9af88-161">**GetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="9af88-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="9af88-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9af88-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="9af88-163">**SetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="9af88-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="9af88-164">**SetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="9af88-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="9af88-165">**WM \_ HSCROLL (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="9af88-165">**WM\_HSCROLL (trackbar)**</span></span>](wm-hscroll--trackbar-.md)
</dt> <dt>

[<span data-ttu-id="9af88-166">**\_VSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="9af88-166">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

