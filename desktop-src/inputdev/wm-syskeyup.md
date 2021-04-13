---
title: Message WM_SYSKEYUP (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur relâche une touche qui a été enfoncée alors que la touche ALT était maintenue enfoncée.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321798"
---
# <a name="wm_syskeyup-message"></a><span data-ttu-id="c88d0-104">\_Message WM SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="c88d0-104">WM\_SYSKEYUP message</span></span>

<span data-ttu-id="c88d0-105">Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur relâche une touche qui a été enfoncée alors que la touche ALT était maintenue enfoncée.</span><span class="sxs-lookup"><span data-stu-id="c88d0-105">Posted to the window with the keyboard focus when the user releases a key that was pressed while the ALT key was held down.</span></span> <span data-ttu-id="c88d0-106">Elle se produit également lorsqu’aucune fenêtre n’a actuellement le focus clavier. dans ce cas, le message **WM \_ SYSKEYUP** est envoyé à la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="c88d0-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYUP** message is sent to the active window.</span></span> <span data-ttu-id="c88d0-107">La fenêtre qui reçoit le message peut faire la distinction entre ces deux contextes en vérifiant le code de contexte dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c88d0-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>

<span data-ttu-id="c88d0-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c88d0-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a><span data-ttu-id="c88d0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c88d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c88d0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c88d0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c88d0-111">Code de la touche virtuelle de la touche en cours de publication.</span><span class="sxs-lookup"><span data-stu-id="c88d0-111">The virtual-key code of the key being released.</span></span> <span data-ttu-id="c88d0-112">Consultez [**codes de clé virtuelle**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c88d0-112">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="c88d0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c88d0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c88d0-114">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c88d0-114">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="c88d0-115">Bits</span><span class="sxs-lookup"><span data-stu-id="c88d0-115">Bits</span></span>  | <span data-ttu-id="c88d0-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c88d0-116">Meaning</span></span>                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88d0-117">0-15</span><span class="sxs-lookup"><span data-stu-id="c88d0-117">0-15</span></span>  | <span data-ttu-id="c88d0-118">Nombre de répétitions du message en cours.</span><span class="sxs-lookup"><span data-stu-id="c88d0-118">The repeat count for the current message.</span></span> <span data-ttu-id="c88d0-119">La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="c88d0-119">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="c88d0-120">Le compteur REPEAT est toujours un pour un message **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="c88d0-120">The repeat count is always one for a **WM\_SYSKEYUP** message.</span></span>         |
| <span data-ttu-id="c88d0-121">16-23</span><span class="sxs-lookup"><span data-stu-id="c88d0-121">16-23</span></span> | <span data-ttu-id="c88d0-122">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="c88d0-122">The scan code.</span></span> <span data-ttu-id="c88d0-123">La valeur dépend du fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="c88d0-123">The value depends on the OEM.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="c88d0-124">24</span><span class="sxs-lookup"><span data-stu-id="c88d0-124">24</span></span>    | <span data-ttu-id="c88d0-125">Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches.</span><span class="sxs-lookup"><span data-stu-id="c88d0-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="c88d0-126">La valeur est 1 s’il s’agit d’une clé étendue ; dans le cas contraire, il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c88d0-126">The value is 1 if it is an extended key; otherwise, it is zero.</span></span>                   |
| <span data-ttu-id="c88d0-127">25-28</span><span class="sxs-lookup"><span data-stu-id="c88d0-127">25-28</span></span> | <span data-ttu-id="c88d0-128">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="c88d0-128">Reserved; do not use.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="c88d0-129">29</span><span class="sxs-lookup"><span data-stu-id="c88d0-129">29</span></span>    | <span data-ttu-id="c88d0-130">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="c88d0-130">The context code.</span></span> <span data-ttu-id="c88d0-131">La valeur est 1 si la touche ALT est enfoncée pendant que la touche est relâchée ; elle est égale à zéro si le message **\_ SYSKEYUP WM** est publié dans la fenêtre active, car aucune fenêtre n’a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="c88d0-131">The value is 1 if the ALT key is down while the key is released; it is zero if the **WM\_SYSKEYUP** message is posted to the active window because no window has the keyboard focus.</span></span> |
| <span data-ttu-id="c88d0-132">30</span><span class="sxs-lookup"><span data-stu-id="c88d0-132">30</span></span>    | <span data-ttu-id="c88d0-133">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="c88d0-133">The previous key state.</span></span> <span data-ttu-id="c88d0-134">La valeur est toujours 1 pour un message **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="c88d0-134">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                 |
| <span data-ttu-id="c88d0-135">31</span><span class="sxs-lookup"><span data-stu-id="c88d0-135">31</span></span>    | <span data-ttu-id="c88d0-136">État de transition.</span><span class="sxs-lookup"><span data-stu-id="c88d0-136">The transition state.</span></span> <span data-ttu-id="c88d0-137">La valeur est toujours 1 pour un message **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="c88d0-137">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                   |

<span data-ttu-id="c88d0-138">Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="c88d0-138">For more details, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c88d0-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c88d0-139">Return value</span></span>

<span data-ttu-id="c88d0-140">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="c88d0-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88d0-141">Notes</span><span class="sxs-lookup"><span data-stu-id="c88d0-141">Remarks</span></span>

<span data-ttu-id="c88d0-142">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre de niveau supérieur si la touche F10 ou la touche Alt a été relâchée.</span><span class="sxs-lookup"><span data-stu-id="c88d0-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="c88d0-143">Le paramètre *wParam* du message est défini sur **SC \_ keymenu**.</span><span class="sxs-lookup"><span data-stu-id="c88d0-143">The *wParam* parameter of the message is set to **SC\_KEYMENU**.</span></span>

<span data-ttu-id="c88d0-144">Lorsque le code de contexte est égal à zéro, le message peut être passé à la fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , qui le gère comme s’il s’agissait d’un message de clé normal au lieu d’un message de touche de caractère.</span><span class="sxs-lookup"><span data-stu-id="c88d0-144">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="c88d0-145">Cela permet d’utiliser les touches d’accès rapide avec la fenêtre active, même si la fenêtre active n’a pas le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="c88d0-145">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="c88d0-146">Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="c88d0-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="c88d0-147">D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c88d0-147">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="c88d0-148">Pour les non-U. S. clavier amélioré 102 touches, la touche ALT de droite est gérée comme une touche CTRL + ALT.</span><span class="sxs-lookup"><span data-stu-id="c88d0-148">For non-U.S. enhanced 102-key keyboards, the right ALT key is handled as a CTRL+ALT key.</span></span> <span data-ttu-id="c88d0-149">Le tableau suivant présente la séquence de messages qui se produit lorsque l’utilisateur appuie sur cette touche et la relâche.</span><span class="sxs-lookup"><span data-stu-id="c88d0-149">The following table shows the sequence of messages that result when the user presses and releases this key.</span></span>



| <span data-ttu-id="c88d0-150">Message</span><span class="sxs-lookup"><span data-stu-id="c88d0-150">Message</span></span>                           | <span data-ttu-id="c88d0-151">Code de la touche virtuelle</span><span class="sxs-lookup"><span data-stu-id="c88d0-151">Virtual-key code</span></span> |
|-----------------------------------|------------------|
| [<span data-ttu-id="c88d0-152">**WM- \_ touche**</span><span class="sxs-lookup"><span data-stu-id="c88d0-152">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="c88d0-153">**\_contrôle VK**</span><span class="sxs-lookup"><span data-stu-id="c88d0-153">**VK\_CONTROL**</span></span>  |
| [<span data-ttu-id="c88d0-154">**WM- \_ touche**</span><span class="sxs-lookup"><span data-stu-id="c88d0-154">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="c88d0-155">**\_menu VK**</span><span class="sxs-lookup"><span data-stu-id="c88d0-155">**VK\_MENU**</span></span>     |
| [<span data-ttu-id="c88d0-156">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="c88d0-156">**WM\_KEYUP**</span></span>](wm-keyup.md)     | <span data-ttu-id="c88d0-157">**\_contrôle VK**</span><span class="sxs-lookup"><span data-stu-id="c88d0-157">**VK\_CONTROL**</span></span>  |
| <span data-ttu-id="c88d0-158">**\_SYSKEYUP WM**</span><span class="sxs-lookup"><span data-stu-id="c88d0-158">**WM\_SYSKEYUP**</span></span>                  | <span data-ttu-id="c88d0-159">**\_menu VK**</span><span class="sxs-lookup"><span data-stu-id="c88d0-159">**VK\_MENU**</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="c88d0-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c88d0-160">Requirements</span></span>



| <span data-ttu-id="c88d0-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c88d0-161">Requirement</span></span> | <span data-ttu-id="c88d0-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="c88d0-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88d0-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c88d0-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c88d0-164">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c88d0-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c88d0-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c88d0-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c88d0-166">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c88d0-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c88d0-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="c88d0-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="c88d0-168"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c88d0-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c88d0-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c88d0-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="c88d0-170">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c88d0-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c88d0-171">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c88d0-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c88d0-172">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="c88d0-172">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="c88d0-173">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="c88d0-173">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="c88d0-174">**\_SYSKEYDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="c88d0-174">**WM\_SYSKEYDOWN**</span></span>](wm-syskeydown.md)
</dt> <dt>

<span data-ttu-id="c88d0-175">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c88d0-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c88d0-176">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="c88d0-176">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

