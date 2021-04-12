---
title: Code de notification WM_VSCROLL (TrackBar. h)
description: Le \_ message WM VSCROLL est envoyé au propriétaire d’un contrôle TrackBar vertical lorsque le curseur change de position. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- Contrôles Windows du code de notification WM_VSCROLL (TrackBar)
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
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104416"
---
# <a name="wm_vscroll-trackbar-notification-code"></a><span data-ttu-id="16298-105">\_Code de notification WM VSCROLL (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="16298-105">WM\_VSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="16298-106">Le message **WM \_ VSCROLL** est envoyé au propriétaire d’un contrôle TrackBar vertical lorsque le curseur change de position.</span><span class="sxs-lookup"><span data-stu-id="16298-106">The **WM\_VSCROLL** message is sent to the owner of a vertical trackbar control when the slider changes position.</span></span>

<span data-ttu-id="16298-107">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="16298-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="16298-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16298-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16298-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16298-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16298-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle du curseur si le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est to \_ THUMBPOSITION ou to \_ THUMBTRACK.</span><span class="sxs-lookup"><span data-stu-id="16298-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="16298-111">Pour tous les autres codes de notification, le mot de poids fort est zéro ; Envoyez le message [**TBM \_ GETPOS**](tbm-getpos.md) pour déterminer la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="16298-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="16298-112">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie un code de notification qui indique l’interaction de l’utilisateur avec le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="16298-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="16298-113">Ce mot peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="16298-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="16298-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="16298-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="16298-115">Signification</span><span class="sxs-lookup"><span data-stu-id="16298-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="16298-116"><dt>**TO \_ bas**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="16298-117">L’utilisateur a appuyé sur la touche fin ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="16298-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="16298-118"><dt>**TO \_ ENDTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="16298-119">Le TrackBar a reçu [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), ce qui signifie que l’utilisateur a publié une clé qui a envoyé un code de clé virtuelle pertinent.</span><span class="sxs-lookup"><span data-stu-id="16298-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="16298-120"><dt>**TO \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="16298-121">L’utilisateur a appuyé sur la flèche droite ([**VK à \_ droite**](/windows/desktop/inputdev/virtual-key-codes)) ou sur la touche flèche bas ([**VK \_**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="16298-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="16298-122"><dt>**\_programmation to**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="16298-123">L’utilisateur a appuyé sur la touche de direction gauche ([**VK \_ gauche**](/windows/desktop/inputdev/virtual-key-codes)) ou flèche vers le haut (VK vers le haut).[**\_**](/windows/desktop/inputdev/virtual-key-codes)</span><span class="sxs-lookup"><span data-stu-id="16298-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="16298-124"><dt>**TO \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="16298-125">L’utilisateur a cliqué sur le canal en dessous ou à droite du curseur ([**VK \_ Next**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="16298-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="16298-126"><dt>**TO \_ PG PRÉC**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="16298-127">L’utilisateur a cliqué sur le canal au-dessus ou à gauche du curseur ([**VK \_**](/windows/desktop/inputdev/virtual-key-codes)précédemment).</span><span class="sxs-lookup"><span data-stu-id="16298-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="16298-128"><dt>**TO \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="16298-129">Le TrackBar a reçu le [**\_ LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup) qui suit un \_ Code de notification to THUMBTRACK.</span><span class="sxs-lookup"><span data-stu-id="16298-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="16298-130"><dt>**TO \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="16298-131">L’utilisateur a fait glisser le curseur.</span><span class="sxs-lookup"><span data-stu-id="16298-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="16298-132"><dt>**TO \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="16298-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="16298-133">L’utilisateur a appuyé sur la touche début ([**VK \_**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="16298-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="16298-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16298-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16298-135">Handle du contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="16298-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16298-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16298-136">Return value</span></span>

<span data-ttu-id="16298-137">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="16298-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="16298-138">Notes</span><span class="sxs-lookup"><span data-stu-id="16298-138">Remarks</span></span>

<span data-ttu-id="16298-139">Le \_ code THUMBTRACK to est généralement utilisé par les applications qui fournissent des commentaires au fur et à mesure que l’utilisateur fait glisser la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="16298-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="16298-140">Notez que le message **WM \_ VSCROLL** contient uniquement 16 bits de données de position.</span><span class="sxs-lookup"><span data-stu-id="16298-140">Note that the **WM\_VSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="16298-141">Ainsi, les applications qui reposent uniquement sur **WM \_ VSCROLL** (et [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) pour les données de position de curseur ont une valeur de position maximale pratique de 65 535.</span><span class="sxs-lookup"><span data-stu-id="16298-141">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="16298-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16298-142">Requirements</span></span>



| <span data-ttu-id="16298-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16298-143">Requirement</span></span> | <span data-ttu-id="16298-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="16298-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16298-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16298-145">Minimum supported client</span></span><br/> | <span data-ttu-id="16298-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16298-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="16298-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16298-147">Minimum supported server</span></span><br/> | <span data-ttu-id="16298-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16298-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16298-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="16298-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="16298-150"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16298-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16298-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16298-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="16298-152">**Référence**</span><span class="sxs-lookup"><span data-stu-id="16298-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="16298-153">**\_HSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="16298-153">**WM\_HSCROLL**</span></span>](wm-hscroll--trackbar-.md)
</dt> </dl>

 

