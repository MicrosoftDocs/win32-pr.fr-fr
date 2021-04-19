---
title: Message WM_UNICHAR (winuser. h)
description: Le \_ message WM UNICHAR peut être utilisé par une application pour envoyer une entrée à d’autres fenêtres.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- WM_UNICHAR l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510539"
---
# <a name="wm_unichar-message"></a><span data-ttu-id="98ffc-104">\_Message WM UNICHAR</span><span class="sxs-lookup"><span data-stu-id="98ffc-104">WM\_UNICHAR message</span></span>

<span data-ttu-id="98ffc-105">Le message **WM \_ UNICHAR** peut être utilisé par une application pour envoyer une entrée à d’autres fenêtres.</span><span class="sxs-lookup"><span data-stu-id="98ffc-105">The **WM\_UNICHAR** message can be used by an application to post input to other windows.</span></span> <span data-ttu-id="98ffc-106">Ce message contient le code de caractère de la touche qui a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="98ffc-106">This message contains the character code of the key that was pressed.</span></span> <span data-ttu-id="98ffc-107">(Tester si une application cible peut traiter les messages **WM \_ UNICHAR** en envoyant le message avec *wParam* défini sur **Unicode \_ nochar**.)</span><span class="sxs-lookup"><span data-stu-id="98ffc-107">(Test whether a target app can process **WM\_UNICHAR** messages by sending the message with *wParam* set to **UNICODE\_NOCHAR**.)</span></span>


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a><span data-ttu-id="98ffc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98ffc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ffc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98ffc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98ffc-110">Code de caractère de la clé.</span><span class="sxs-lookup"><span data-stu-id="98ffc-110">The character code of the key.</span></span>

<span data-ttu-id="98ffc-111">Si *wParam* est **un \_ nochar Unicode** et que l’application traite ce message, retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="98ffc-111">If *wParam* is **UNICODE\_NOCHAR** and the application processes this message, then return **TRUE**.</span></span> <span data-ttu-id="98ffc-112">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la **valeur false** (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="98ffc-112">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function will return **FALSE** (the default).</span></span>

<span data-ttu-id="98ffc-113">Si *wParam* n’est pas de **\_ type Unicode Nochar**, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="98ffc-113">If *wParam* is not **UNICODE\_NOCHAR**, return **FALSE**.</span></span> <span data-ttu-id="98ffc-114">Le  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Unicode publie un [**message \_ WM**](wm-char.md) avec les mêmes paramètres et la fonction **DefWindowProc** ANSI publie un ou deux messages **WM \_ char** avec le ou les caractères ANSI correspondants.</span><span class="sxs-lookup"><span data-stu-id="98ffc-114">The Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posts a [**WM\_CHAR**](wm-char.md) message with the same parameters and the ANSI **DefWindowProc** function posts either one or two **WM\_CHAR** messages with the corresponding ANSI character(s).</span></span>

</dd> <dt>

<span data-ttu-id="98ffc-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98ffc-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98ffc-116">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="98ffc-116">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="98ffc-117">Bits</span><span class="sxs-lookup"><span data-stu-id="98ffc-117">Bits</span></span>  | <span data-ttu-id="98ffc-118">Signification</span><span class="sxs-lookup"><span data-stu-id="98ffc-118">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ffc-119">0-15</span><span class="sxs-lookup"><span data-stu-id="98ffc-119">0-15</span></span>  | <span data-ttu-id="98ffc-120">Nombre de répétitions du message en cours.</span><span class="sxs-lookup"><span data-stu-id="98ffc-120">The repeat count for the current message.</span></span> <span data-ttu-id="98ffc-121">La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="98ffc-121">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="98ffc-122">Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="98ffc-122">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="98ffc-123">Toutefois, le nombre de répétitions n’est pas cumulatif.</span><span class="sxs-lookup"><span data-stu-id="98ffc-123">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="98ffc-124">16-23</span><span class="sxs-lookup"><span data-stu-id="98ffc-124">16-23</span></span> | <span data-ttu-id="98ffc-125">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="98ffc-125">The scan code.</span></span> <span data-ttu-id="98ffc-126">La valeur dépend du fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="98ffc-126">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="98ffc-127">24</span><span class="sxs-lookup"><span data-stu-id="98ffc-127">24</span></span>    | <span data-ttu-id="98ffc-128">Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches.</span><span class="sxs-lookup"><span data-stu-id="98ffc-128">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="98ffc-129">La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="98ffc-129">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="98ffc-130">25-28</span><span class="sxs-lookup"><span data-stu-id="98ffc-130">25-28</span></span> | <span data-ttu-id="98ffc-131">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="98ffc-131">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="98ffc-132">29</span><span class="sxs-lookup"><span data-stu-id="98ffc-132">29</span></span>    | <span data-ttu-id="98ffc-133">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="98ffc-133">The context code.</span></span> <span data-ttu-id="98ffc-134">La valeur est 1 si la touche ALT est maintenue enfoncée pendant que la touche est enfoncée ; dans le cas contraire, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="98ffc-134">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="98ffc-135">30</span><span class="sxs-lookup"><span data-stu-id="98ffc-135">30</span></span>    | <span data-ttu-id="98ffc-136">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="98ffc-136">The previous key state.</span></span> <span data-ttu-id="98ffc-137">La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.</span><span class="sxs-lookup"><span data-stu-id="98ffc-137">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="98ffc-138">31</span><span class="sxs-lookup"><span data-stu-id="98ffc-138">31</span></span>    | <span data-ttu-id="98ffc-139">État de transition.</span><span class="sxs-lookup"><span data-stu-id="98ffc-139">The transition state.</span></span> <span data-ttu-id="98ffc-140">La valeur est 1 si la touche est relâchée, ou 0 si la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="98ffc-140">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="98ffc-141">Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="98ffc-141">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ffc-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98ffc-142">Return value</span></span>

<span data-ttu-id="98ffc-143">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="98ffc-143">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ffc-144">Notes</span><span class="sxs-lookup"><span data-stu-id="98ffc-144">Remarks</span></span>

<span data-ttu-id="98ffc-145">Le message **WM \_ UNICHAR** est similaire à [**WM \_ char**](wm-char.md), mais il utilise le format UTF (Unicode Transformation Format)-32, alors que **WM \_ char** utilise UTF-16.</span><span class="sxs-lookup"><span data-stu-id="98ffc-145">The **WM\_UNICHAR** message is similar to [**WM\_CHAR**](wm-char.md), but it uses Unicode Transformation Format (UTF)-32, whereas **WM\_CHAR** uses UTF-16.</span></span>

<span data-ttu-id="98ffc-146">Ce message est conçu pour envoyer ou poster des caractères Unicode dans des fenêtres ANSI et peut gérer des caractères de plan supplémentaires Unicode.</span><span class="sxs-lookup"><span data-stu-id="98ffc-146">This message is designed to send or post Unicode characters to ANSI windows and can handle Unicode Supplementary Plane characters.</span></span>

<span data-ttu-id="98ffc-147">Étant donné qu’il n’y a pas nécessairement une correspondance un-à-un entre les touches enfoncées et les messages de caractères générés, les informations contenues dans le mot de poids fort du paramètre *lParam* ne sont généralement pas utiles aux applications.</span><span class="sxs-lookup"><span data-stu-id="98ffc-147">Because there is not necessarily a one-to-one correspondence between keys pressed and character messages generated, the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="98ffc-148">Les informations contenues dans le mot de poids fort ne s’appliquent qu’au dernier message de la [**\_ touche WM**](wm-keydown.md) qui précède la publication du message **WM \_ UNICHAR** .</span><span class="sxs-lookup"><span data-stu-id="98ffc-148">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_UNICHAR** message.</span></span>

<span data-ttu-id="98ffc-149">Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et droite de la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="98ffc-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="98ffc-150">D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="98ffc-150">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ffc-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98ffc-151">Requirements</span></span>



| <span data-ttu-id="98ffc-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98ffc-152">Requirement</span></span> | <span data-ttu-id="98ffc-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="98ffc-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ffc-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98ffc-154">Minimum supported client</span></span><br/> | <span data-ttu-id="98ffc-155">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98ffc-155">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="98ffc-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98ffc-156">Minimum supported server</span></span><br/> | <span data-ttu-id="98ffc-157">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98ffc-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98ffc-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="98ffc-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ffc-159"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98ffc-159"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ffc-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98ffc-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="98ffc-161">**Référence**</span><span class="sxs-lookup"><span data-stu-id="98ffc-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98ffc-162">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="98ffc-162">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="98ffc-163">**\_caractère WM**</span><span class="sxs-lookup"><span data-stu-id="98ffc-163">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="98ffc-164">**WM- \_ touche**</span><span class="sxs-lookup"><span data-stu-id="98ffc-164">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

<span data-ttu-id="98ffc-165">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="98ffc-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98ffc-166">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="98ffc-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

