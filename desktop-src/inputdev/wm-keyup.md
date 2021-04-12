---
title: Message WM_KEYUP (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’une touche non-système est relâchée. Une touche non-système est une touche qui est enfoncée lorsque la touche ALT n’est pas enfoncée ou une touche du clavier qui est enfoncée lorsqu’une fenêtre a le focus clavier.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384419"
---
# <a name="wm_keyup-message"></a><span data-ttu-id="7cc85-105">\_Message WM KEYUP</span><span class="sxs-lookup"><span data-stu-id="7cc85-105">WM\_KEYUP message</span></span>

<span data-ttu-id="7cc85-106">Publié dans la fenêtre qui a le focus clavier lorsqu’une touche non-système est relâchée.</span><span class="sxs-lookup"><span data-stu-id="7cc85-106">Posted to the window with the keyboard focus when a nonsystem key is released.</span></span> <span data-ttu-id="7cc85-107">Une touche non-système est une touche qui est enfoncée lorsque la touche ALT n’est *pas* enfoncée ou une touche du clavier qui est enfoncée lorsqu’une fenêtre a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="7cc85-107">A nonsystem key is a key that is pressed when the ALT key is *not* pressed, or a keyboard key that is pressed when a window has the keyboard focus.</span></span>


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a><span data-ttu-id="7cc85-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cc85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cc85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7cc85-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cc85-110">Code de la clé virtuelle de la clé non-système.</span><span class="sxs-lookup"><span data-stu-id="7cc85-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="7cc85-111">Consultez [codes de clé virtuelle](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7cc85-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc85-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7cc85-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cc85-113">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7cc85-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="7cc85-114">Bits</span><span class="sxs-lookup"><span data-stu-id="7cc85-114">Bits</span></span>  | <span data-ttu-id="7cc85-115">Signification</span><span class="sxs-lookup"><span data-stu-id="7cc85-115">Meaning</span></span>                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc85-116">0-15</span><span class="sxs-lookup"><span data-stu-id="7cc85-116">0-15</span></span>  | <span data-ttu-id="7cc85-117">Nombre de répétitions du message en cours.</span><span class="sxs-lookup"><span data-stu-id="7cc85-117">The repeat count for the current message.</span></span> <span data-ttu-id="7cc85-118">La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="7cc85-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="7cc85-119">Le nombre de répétitions est toujours 1 pour un message **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="7cc85-119">The repeat count is always 1 for a **WM\_KEYUP** message.</span></span> |
| <span data-ttu-id="7cc85-120">16-23</span><span class="sxs-lookup"><span data-stu-id="7cc85-120">16-23</span></span> | <span data-ttu-id="7cc85-121">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="7cc85-121">The scan code.</span></span> <span data-ttu-id="7cc85-122">La valeur dépend du fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="7cc85-122">The value depends on the OEM.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="7cc85-123">24</span><span class="sxs-lookup"><span data-stu-id="7cc85-123">24</span></span>    | <span data-ttu-id="7cc85-124">Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches.</span><span class="sxs-lookup"><span data-stu-id="7cc85-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="7cc85-125">La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="7cc85-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>         |
| <span data-ttu-id="7cc85-126">25-28</span><span class="sxs-lookup"><span data-stu-id="7cc85-126">25-28</span></span> | <span data-ttu-id="7cc85-127">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="7cc85-127">Reserved; do not use.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="7cc85-128">29</span><span class="sxs-lookup"><span data-stu-id="7cc85-128">29</span></span>    | <span data-ttu-id="7cc85-129">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="7cc85-129">The context code.</span></span> <span data-ttu-id="7cc85-130">La valeur est toujours 0 pour un message **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="7cc85-130">The value is always 0 for a **WM\_KEYUP** message.</span></span>                                                                                                                                             |
| <span data-ttu-id="7cc85-131">30</span><span class="sxs-lookup"><span data-stu-id="7cc85-131">30</span></span>    | <span data-ttu-id="7cc85-132">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="7cc85-132">The previous key state.</span></span> <span data-ttu-id="7cc85-133">La valeur est toujours 1 pour un message **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="7cc85-133">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                       |
| <span data-ttu-id="7cc85-134">31</span><span class="sxs-lookup"><span data-stu-id="7cc85-134">31</span></span>    | <span data-ttu-id="7cc85-135">État de transition.</span><span class="sxs-lookup"><span data-stu-id="7cc85-135">The transition state.</span></span> <span data-ttu-id="7cc85-136">La valeur est toujours 1 pour un message **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="7cc85-136">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                         |

<span data-ttu-id="7cc85-137">Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="7cc85-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cc85-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cc85-138">Return value</span></span>

<span data-ttu-id="7cc85-139">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="7cc85-139">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cc85-140">Notes</span><span class="sxs-lookup"><span data-stu-id="7cc85-140">Remarks</span></span>

<span data-ttu-id="7cc85-141">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre de niveau supérieur si la touche F10 ou la touche Alt a été relâchée.</span><span class="sxs-lookup"><span data-stu-id="7cc85-141">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="7cc85-142">Le paramètre *wParam* du message est défini sur SC \_ keymenu.</span><span class="sxs-lookup"><span data-stu-id="7cc85-142">The *wParam* parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="7cc85-143">Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="7cc85-143">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="7cc85-144">D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="7cc85-144">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="7cc85-145">Les applications doivent passer *wParam* à [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="7cc85-145">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cc85-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cc85-146">Requirements</span></span>



| <span data-ttu-id="7cc85-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cc85-147">Requirement</span></span> | <span data-ttu-id="7cc85-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cc85-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc85-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cc85-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc85-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cc85-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7cc85-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cc85-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc85-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cc85-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7cc85-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cc85-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cc85-154"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cc85-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cc85-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cc85-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="7cc85-156">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7cc85-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7cc85-157">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7cc85-157">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7cc85-158">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="7cc85-158">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="7cc85-159">**WM- \_ touche**</span><span class="sxs-lookup"><span data-stu-id="7cc85-159">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="7cc85-160">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="7cc85-160">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="7cc85-161">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="7cc85-161">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7cc85-162">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="7cc85-162">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

