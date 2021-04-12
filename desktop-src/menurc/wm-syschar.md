---
title: Message WM_SYSCHAR (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’un \_ message WM SYSKEYDOWN est traduit par la fonction TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519194"
---
# <a name="wm_syschar-message"></a><span data-ttu-id="ff448-104">\_Message WM SYSCHAR</span><span class="sxs-lookup"><span data-stu-id="ff448-104">WM\_SYSCHAR message</span></span>

<span data-ttu-id="ff448-105">Publié dans la fenêtre qui a le focus clavier lorsqu’un message [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) est traduit par la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="ff448-105">Posted to the window with the keyboard focus when a [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="ff448-106">Elle spécifie le code de caractère d’une touche de caractère système, c’est-à-dire une touche de caractère qui est enfoncée pendant que la touche ALT est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ff448-106">It specifies the character code of a system character key   that is, a character key that is pressed while the ALT key is down.</span></span>


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a><span data-ttu-id="ff448-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff448-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff448-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff448-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff448-109">Code de caractère de la touche de menu de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ff448-109">The character code of the window menu key.</span></span>

</dd> <dt>

<span data-ttu-id="ff448-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff448-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff448-111">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ff448-111">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="ff448-112">Bits</span><span class="sxs-lookup"><span data-stu-id="ff448-112">Bits</span></span>                                                                             | <span data-ttu-id="ff448-113">Signification</span><span class="sxs-lookup"><span data-stu-id="ff448-113">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff448-114"><dt>0 15</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-114"><dt>0 15</dt></span></span> </dl>  | <span data-ttu-id="ff448-115">Nombre de répétitions du message en cours.</span><span class="sxs-lookup"><span data-stu-id="ff448-115">The repeat count for the current message.</span></span> <span data-ttu-id="ff448-116">La valeur est le nombre de fois que la frappe a été répétée automatiquement à la suite de l’utilisateur qui maintient la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ff448-116">The value is the number of times the keystroke was auto-repeated as a result of the user holding down the key.</span></span> <span data-ttu-id="ff448-117">Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="ff448-117">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="ff448-118">Toutefois, le nombre de répétitions n’est pas cumulatif.</span><span class="sxs-lookup"><span data-stu-id="ff448-118">However, the repeat count is not cumulative.</span></span><br/> |
| <dl> <span data-ttu-id="ff448-119"><dt>16 23</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-119"><dt>16 23</dt></span></span> </dl> | <span data-ttu-id="ff448-120">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="ff448-120">The scan code.</span></span> <span data-ttu-id="ff448-121">La valeur dépend du fabricant d’ordinateurs OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="ff448-121">The value depends on the original equipment manufacturer (OEM).</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="ff448-122"><dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-122"><dt>24</dt></span></span> </dl>    | <span data-ttu-id="ff448-123">Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches.</span><span class="sxs-lookup"><span data-stu-id="ff448-123">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="ff448-124">La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="ff448-124">The value is 1 if it is an extended key; otherwise, it is 0.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ff448-125"><dt>25 28</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-125"><dt>25 28</dt></span></span> </dl> | <span data-ttu-id="ff448-126">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ff448-126">Reserved; do not use.</span></span><br/>                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="ff448-127"><dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-127"><dt>29</dt></span></span> </dl>    | <span data-ttu-id="ff448-128">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="ff448-128">The context code.</span></span> <span data-ttu-id="ff448-129">La valeur est 1 si la touche ALT est maintenue enfoncée pendant que la touche est enfoncée ; dans le cas contraire, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="ff448-129">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="ff448-130"><dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-130"><dt>30</dt></span></span> </dl>    | <span data-ttu-id="ff448-131">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="ff448-131">The previous key state.</span></span> <span data-ttu-id="ff448-132">La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.</span><span class="sxs-lookup"><span data-stu-id="ff448-132">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span><br/>                                                                                                                                                      |
| <dl> <span data-ttu-id="ff448-133"><dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-133"><dt>31</dt></span></span> </dl>    | <span data-ttu-id="ff448-134">État de transition.</span><span class="sxs-lookup"><span data-stu-id="ff448-134">The transition state.</span></span> <span data-ttu-id="ff448-135">La valeur est 1 si la touche est relâchée, ou 0 si la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ff448-135">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span><br/>                                                                                                                                                              |

<span data-ttu-id="ff448-136">Pour plus d’informations, consultez [indicateurs de message de frappe](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="ff448-136">For more detail, see [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff448-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff448-137">Return value</span></span>

<span data-ttu-id="ff448-138">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="ff448-138">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff448-139">Notes</span><span class="sxs-lookup"><span data-stu-id="ff448-139">Remarks</span></span>

<span data-ttu-id="ff448-140">Lorsque le code de contexte est égal à zéro, le message peut être passé à la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , qui le gère comme s’il s’agissait d’un message de clé standard au lieu d’un message de touche de caractère système.</span><span class="sxs-lookup"><span data-stu-id="ff448-140">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a standard key message instead of a system character-key message.</span></span> <span data-ttu-id="ff448-141">Cela permet d’utiliser les touches d’accès rapide avec la fenêtre active, même si la fenêtre active n’a pas le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="ff448-141">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="ff448-142">Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; touche Impr. SCRN. touche Attn ; touche VERR. num ; et les touches de division (/) et de saisie dans le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="ff448-142">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; the PRINT SCRN key; the BREAK key; the NUMLOCK key; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="ff448-143">D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre.</span><span class="sxs-lookup"><span data-stu-id="ff448-143">Other keyboards may support the extended-key bit in the parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff448-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff448-144">Requirements</span></span>



| <span data-ttu-id="ff448-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff448-145">Requirement</span></span> | <span data-ttu-id="ff448-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff448-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff448-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff448-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ff448-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff448-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ff448-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff448-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ff448-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff448-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff448-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff448-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff448-152"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff448-152"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff448-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff448-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff448-154">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ff448-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff448-155">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="ff448-155">**TranslateAccelerator**</span></span>](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="ff448-156">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="ff448-156">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="ff448-157">**\_SYSKEYDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="ff448-157">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

<span data-ttu-id="ff448-158">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ff448-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff448-159">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="ff448-159">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

