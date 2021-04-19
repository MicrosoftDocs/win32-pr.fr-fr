---
title: Message WM_KEYDOWN (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’une touche non-système est enfoncée. Une touche non-système est une touche qui est enfoncée lorsque la touche ALT n’est pas enfoncée.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538153"
---
# <a name="wm_keydown-message"></a><span data-ttu-id="cca33-105">\_Message KEYverse WM</span><span class="sxs-lookup"><span data-stu-id="cca33-105">WM\_KEYDOWN message</span></span>

<span data-ttu-id="cca33-106">Publié dans la fenêtre qui a le focus clavier lorsqu’une touche non-système est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="cca33-106">Posted to the window with the keyboard focus when a nonsystem key is pressed.</span></span> <span data-ttu-id="cca33-107">Une touche non-système est une touche qui est enfoncée lorsque la touche ALT n’est pas enfoncée.</span><span class="sxs-lookup"><span data-stu-id="cca33-107">A nonsystem key is a key that is pressed when the ALT key is not pressed.</span></span>


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a><span data-ttu-id="cca33-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cca33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cca33-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cca33-110">Code de la clé virtuelle de la clé non-système.</span><span class="sxs-lookup"><span data-stu-id="cca33-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="cca33-111">Consultez [codes de clé virtuelle](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cca33-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="cca33-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cca33-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cca33-113">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cca33-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown following.</span></span>



| <span data-ttu-id="cca33-114">Bits</span><span class="sxs-lookup"><span data-stu-id="cca33-114">Bits</span></span>  | <span data-ttu-id="cca33-115">Signification</span><span class="sxs-lookup"><span data-stu-id="cca33-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca33-116">0-15</span><span class="sxs-lookup"><span data-stu-id="cca33-116">0-15</span></span>  | <span data-ttu-id="cca33-117">Nombre de répétitions du message en cours.</span><span class="sxs-lookup"><span data-stu-id="cca33-117">The repeat count for the current message.</span></span> <span data-ttu-id="cca33-118">La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="cca33-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="cca33-119">Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="cca33-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="cca33-120">Toutefois, le nombre de répétitions n’est pas cumulatif.</span><span class="sxs-lookup"><span data-stu-id="cca33-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="cca33-121">16-23</span><span class="sxs-lookup"><span data-stu-id="cca33-121">16-23</span></span> | <span data-ttu-id="cca33-122">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="cca33-122">The scan code.</span></span> <span data-ttu-id="cca33-123">La valeur dépend du fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="cca33-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="cca33-124">24</span><span class="sxs-lookup"><span data-stu-id="cca33-124">24</span></span>    | <span data-ttu-id="cca33-125">Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches.</span><span class="sxs-lookup"><span data-stu-id="cca33-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="cca33-126">La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="cca33-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="cca33-127">25-28</span><span class="sxs-lookup"><span data-stu-id="cca33-127">25-28</span></span> | <span data-ttu-id="cca33-128">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="cca33-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cca33-129">29</span><span class="sxs-lookup"><span data-stu-id="cca33-129">29</span></span>    | <span data-ttu-id="cca33-130">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="cca33-130">The context code.</span></span> <span data-ttu-id="cca33-131">La valeur est toujours 0 pour un message de **\_ keyversion WM** .</span><span class="sxs-lookup"><span data-stu-id="cca33-131">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="cca33-132">30</span><span class="sxs-lookup"><span data-stu-id="cca33-132">30</span></span>    | <span data-ttu-id="cca33-133">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="cca33-133">The previous key state.</span></span> <span data-ttu-id="cca33-134">La valeur est 1 si la touche est enfoncée avant l’envoi du message ou zéro si la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="cca33-134">The value is 1 if the key is down before the message is sent, or it is zero if the key is up.</span></span>                                                                                                                                                 |
| <span data-ttu-id="cca33-135">31</span><span class="sxs-lookup"><span data-stu-id="cca33-135">31</span></span>    | <span data-ttu-id="cca33-136">État de transition.</span><span class="sxs-lookup"><span data-stu-id="cca33-136">The transition state.</span></span> <span data-ttu-id="cca33-137">La valeur est toujours 0 pour un message de **\_ keyversion WM** .</span><span class="sxs-lookup"><span data-stu-id="cca33-137">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                            |

<span data-ttu-id="cca33-138">Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="cca33-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca33-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cca33-139">Return value</span></span>

<span data-ttu-id="cca33-140">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="cca33-140">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="cca33-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="cca33-141">Example</span></span>

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

<span data-ttu-id="cca33-142">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="cca33-142">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="cca33-143">Notes</span><span class="sxs-lookup"><span data-stu-id="cca33-143">Remarks</span></span>

<span data-ttu-id="cca33-144">Si la touche F10 est enfoncée, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) définit un indicateur interne.</span><span class="sxs-lookup"><span data-stu-id="cca33-144">If the F10 key is pressed, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets an internal flag.</span></span> <span data-ttu-id="cca33-145">Quand **DefWindowProc** reçoit le message [**WM \_ KEYUP**](wm-keyup.md) , la fonction vérifie si l’indicateur interne est défini et, si tel est le cas, envoie un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="cca33-145">When **DefWindowProc** receives the [**WM\_KEYUP**](wm-keyup.md) message, the function checks whether the internal flag is set and, if so, sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window.</span></span> <span data-ttu-id="cca33-146">Le paramètre **WM \_ SYSCOMMAND** du message est défini sur SC \_ keymenu.</span><span class="sxs-lookup"><span data-stu-id="cca33-146">The **WM\_SYSCOMMAND** parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="cca33-147">En raison de la fonctionnalité de répétition, plusieurs messages **WM \_** KeyOut peuvent être publiés avant la publication d’un message [**WM \_ KEYUP**](wm-keyup.md) .</span><span class="sxs-lookup"><span data-stu-id="cca33-147">Because of the autorepeat feature, more than one **WM\_KEYDOWN** message may be posted before a [**WM\_KEYUP**](wm-keyup.md) message is posted.</span></span> <span data-ttu-id="cca33-148">L’état de clé précédent (bit 30) peut être utilisé pour déterminer si le message WM KeyOut indique la première transition vers le haut ou une transition répétée. **\_**</span><span class="sxs-lookup"><span data-stu-id="cca33-148">The previous key state (bit 30) can be used to determine whether the **WM\_KEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="cca33-149">Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="cca33-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="cca33-150">D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cca33-150">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="cca33-151">Les applications doivent passer *wParam* à [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="cca33-151">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="cca33-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cca33-152">Requirements</span></span>



| <span data-ttu-id="cca33-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cca33-153">Requirement</span></span> | <span data-ttu-id="cca33-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="cca33-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca33-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cca33-155">Minimum supported client</span></span><br/> | <span data-ttu-id="cca33-156">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cca33-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cca33-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cca33-157">Minimum supported server</span></span><br/> | <span data-ttu-id="cca33-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cca33-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cca33-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="cca33-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="cca33-160"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cca33-160"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca33-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cca33-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="cca33-162">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cca33-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cca33-163">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="cca33-163">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="cca33-164">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="cca33-164">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="cca33-165">**\_caractère WM**</span><span class="sxs-lookup"><span data-stu-id="cca33-165">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="cca33-166">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="cca33-166">**WM\_KEYUP**</span></span>](wm-keyup.md)
</dt> <dt>

[<span data-ttu-id="cca33-167">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="cca33-167">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="cca33-168">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="cca33-168">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cca33-169">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="cca33-169">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

