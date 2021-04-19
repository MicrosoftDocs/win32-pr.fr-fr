---
title: Message WM_SYSKEYDOWN (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur appuie sur la touche F10 (qui active la barre de menus) ou maintient la touche ALT enfoncée, puis appuie sur une autre touche.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511363"
---
# <a name="wm_syskeydown-message"></a><span data-ttu-id="3bb84-104">\_Message WM SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="3bb84-104">WM\_SYSKEYDOWN message</span></span>

<span data-ttu-id="3bb84-105">Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur appuie sur la touche F10 (qui active la barre de menus) ou maintient la touche ALT enfoncée, puis appuie sur une autre touche.</span><span class="sxs-lookup"><span data-stu-id="3bb84-105">Posted to the window with the keyboard focus when the user presses the F10 key (which activates the menu bar) or holds down the ALT key and then presses another key.</span></span> <span data-ttu-id="3bb84-106">Elle se produit également lorsqu’aucune fenêtre n’a actuellement le focus clavier. dans ce cas, le message **WM \_ SYSKEYDOWN** est envoyé à la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="3bb84-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYDOWN** message is sent to the active window.</span></span> <span data-ttu-id="3bb84-107">La fenêtre qui reçoit le message peut faire la distinction entre ces deux contextes en vérifiant le code de contexte dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3bb84-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a><span data-ttu-id="3bb84-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bb84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb84-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3bb84-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb84-110">Code de la touche virtuelle de la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="3bb84-110">The virtual-key code of the key being pressed.</span></span> <span data-ttu-id="3bb84-111">Consultez [**codes de clé virtuelle**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3bb84-111">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bb84-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3bb84-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb84-113">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3bb84-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="3bb84-114">Bits</span><span class="sxs-lookup"><span data-stu-id="3bb84-114">Bits</span></span>  | <span data-ttu-id="3bb84-115">Signification</span><span class="sxs-lookup"><span data-stu-id="3bb84-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb84-116">0-15</span><span class="sxs-lookup"><span data-stu-id="3bb84-116">0-15</span></span>  | <span data-ttu-id="3bb84-117">Nombre de répétitions du message en cours.</span><span class="sxs-lookup"><span data-stu-id="3bb84-117">The repeat count for the current message.</span></span> <span data-ttu-id="3bb84-118">La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="3bb84-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="3bb84-119">Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="3bb84-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="3bb84-120">Toutefois, le nombre de répétitions n’est pas cumulatif.</span><span class="sxs-lookup"><span data-stu-id="3bb84-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="3bb84-121">16-23</span><span class="sxs-lookup"><span data-stu-id="3bb84-121">16-23</span></span> | <span data-ttu-id="3bb84-122">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="3bb84-122">The scan code.</span></span> <span data-ttu-id="3bb84-123">La valeur dépend du fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="3bb84-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="3bb84-124">24</span><span class="sxs-lookup"><span data-stu-id="3bb84-124">24</span></span>    | <span data-ttu-id="3bb84-125">Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches.</span><span class="sxs-lookup"><span data-stu-id="3bb84-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="3bb84-126">La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="3bb84-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="3bb84-127">25-28</span><span class="sxs-lookup"><span data-stu-id="3bb84-127">25-28</span></span> | <span data-ttu-id="3bb84-128">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="3bb84-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3bb84-129">29</span><span class="sxs-lookup"><span data-stu-id="3bb84-129">29</span></span>    | <span data-ttu-id="3bb84-130">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="3bb84-130">The context code.</span></span> <span data-ttu-id="3bb84-131">La valeur est 1 si la touche ALT est enfoncée pendant que la touche est enfoncée ; elle est égale à 0 si le message **\_ SYSKEYDOWN WM** est publié dans la fenêtre active, car aucune fenêtre n’a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="3bb84-131">The value is 1 if the ALT key is down while the key is pressed; it is 0 if the **WM\_SYSKEYDOWN** message is posted to the active window because no window has the keyboard focus.</span></span>                                                                  |
| <span data-ttu-id="3bb84-132">30</span><span class="sxs-lookup"><span data-stu-id="3bb84-132">30</span></span>    | <span data-ttu-id="3bb84-133">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="3bb84-133">The previous key state.</span></span> <span data-ttu-id="3bb84-134">La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.</span><span class="sxs-lookup"><span data-stu-id="3bb84-134">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="3bb84-135">31</span><span class="sxs-lookup"><span data-stu-id="3bb84-135">31</span></span>    | <span data-ttu-id="3bb84-136">État de transition.</span><span class="sxs-lookup"><span data-stu-id="3bb84-136">The transition state.</span></span> <span data-ttu-id="3bb84-137">La valeur est toujours 0 pour un message **WM \_ SYSKEYDOWN** .</span><span class="sxs-lookup"><span data-stu-id="3bb84-137">The value is always 0 for a **WM\_SYSKEYDOWN** message.</span></span>                                                                                                                                                                                         |

<span data-ttu-id="3bb84-138">Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="3bb84-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb84-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bb84-139">Return value</span></span>

<span data-ttu-id="3bb84-140">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="3bb84-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bb84-141">Notes</span><span class="sxs-lookup"><span data-stu-id="3bb84-141">Remarks</span></span>

<span data-ttu-id="3bb84-142">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examine la clé spécifiée et génère un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) si la clé est de type Tab ou entrée.</span><span class="sxs-lookup"><span data-stu-id="3bb84-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function examines the specified key and generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message if the key is either TAB or ENTER.</span></span>

<span data-ttu-id="3bb84-143">Lorsque le code de contexte est égal à zéro, le message peut être passé à la fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , qui le gère comme s’il s’agissait d’un message de clé normal au lieu d’un message de touche de caractère.</span><span class="sxs-lookup"><span data-stu-id="3bb84-143">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="3bb84-144">Cela permet d’utiliser les touches d’accès rapide avec la fenêtre active, même si la fenêtre active n’a pas le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="3bb84-144">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="3bb84-145">En raison de la répétition automatique, plusieurs messages **WM \_ SYSKEYDOWN** peuvent se produire avant l’envoi d’un message [**\_ SYSKEYUP WM**](wm-syskeyup.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb84-145">Because of automatic repeat, more than one **WM\_SYSKEYDOWN** message may occur before a [**WM\_SYSKEYUP**](wm-syskeyup.md) message is sent.</span></span> <span data-ttu-id="3bb84-146">L’état de clé précédent (bit 30) peut être utilisé pour déterminer si le message **WM \_ SYSKEYDOWN** indique la première transition vers le haut ou une transition répétée.</span><span class="sxs-lookup"><span data-stu-id="3bb84-146">The previous key state (bit 30) can be used to determine whether the **WM\_SYSKEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="3bb84-147">Pour les claviers à touche 101 et 102 améliorés, les touches améliorées sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="3bb84-147">For enhanced 101- and 102-key keyboards, enhanced keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="3bb84-148">D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3bb84-148">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="3bb84-149">Ce message est également envoyé chaque fois que l’utilisateur appuie sur la touche F10 sans la touche ALT.</span><span class="sxs-lookup"><span data-stu-id="3bb84-149">This message is also sent whenever the user presses the F10 key without the ALT key.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb84-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bb84-150">Requirements</span></span>



| <span data-ttu-id="3bb84-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bb84-151">Requirement</span></span> | <span data-ttu-id="3bb84-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bb84-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb84-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bb84-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb84-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bb84-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3bb84-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bb84-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb84-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bb84-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3bb84-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bb84-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb84-158"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bb84-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb84-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bb84-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="3bb84-160">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3bb84-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3bb84-161">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3bb84-161">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3bb84-162">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="3bb84-162">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="3bb84-163">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="3bb84-163">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="3bb84-164">**\_SYSKEYUP WM**</span><span class="sxs-lookup"><span data-stu-id="3bb84-164">**WM\_SYSKEYUP**</span></span>](wm-syskeyup.md)
</dt> <dt>

<span data-ttu-id="3bb84-165">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3bb84-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3bb84-166">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="3bb84-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

