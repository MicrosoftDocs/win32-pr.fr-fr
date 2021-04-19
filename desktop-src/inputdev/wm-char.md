---
title: Message WM_CHAR (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’un \_ message de KEYversion WM est traduit par la fonction TranslateMessage. Le \_ message WM char contient le code de caractère de la touche qui a été enfoncée.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544092"
---
# <a name="wm_char-message"></a><span data-ttu-id="2f902-105">\_Message WM char</span><span class="sxs-lookup"><span data-stu-id="2f902-105">WM\_CHAR message</span></span>

<span data-ttu-id="2f902-106">Publié dans la fenêtre qui a le focus clavier lorsqu’un message de [**\_ keyversion WM**](wm-keydown.md) est traduit par la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="2f902-106">Posted to the window with the keyboard focus when a [**WM\_KEYDOWN**](wm-keydown.md) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="2f902-107">Le message **WM \_ char** contient le code de caractère de la touche qui a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="2f902-107">The **WM\_CHAR** message contains the character code of the key that was pressed.</span></span>


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a><span data-ttu-id="2f902-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f902-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f902-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f902-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f902-110">Code de caractère de la clé.</span><span class="sxs-lookup"><span data-stu-id="2f902-110">The character code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="2f902-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f902-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f902-112">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2f902-112">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="2f902-113">Bits</span><span class="sxs-lookup"><span data-stu-id="2f902-113">Bits</span></span>  | <span data-ttu-id="2f902-114">Signification</span><span class="sxs-lookup"><span data-stu-id="2f902-114">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f902-115">0-15</span><span class="sxs-lookup"><span data-stu-id="2f902-115">0-15</span></span>  | <span data-ttu-id="2f902-116">Nombre de répétitions du message en cours.</span><span class="sxs-lookup"><span data-stu-id="2f902-116">The repeat count for the current message.</span></span> <span data-ttu-id="2f902-117">La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="2f902-117">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="2f902-118">Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="2f902-118">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="2f902-119">Toutefois, le nombre de répétitions n’est pas cumulatif.</span><span class="sxs-lookup"><span data-stu-id="2f902-119">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="2f902-120">16-23</span><span class="sxs-lookup"><span data-stu-id="2f902-120">16-23</span></span> | <span data-ttu-id="2f902-121">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2f902-121">The scan code.</span></span> <span data-ttu-id="2f902-122">La valeur dépend du fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="2f902-122">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="2f902-123">24</span><span class="sxs-lookup"><span data-stu-id="2f902-123">24</span></span>    | <span data-ttu-id="2f902-124">Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches.</span><span class="sxs-lookup"><span data-stu-id="2f902-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="2f902-125">La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="2f902-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="2f902-126">25-28</span><span class="sxs-lookup"><span data-stu-id="2f902-126">25-28</span></span> | <span data-ttu-id="2f902-127">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="2f902-127">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2f902-128">29</span><span class="sxs-lookup"><span data-stu-id="2f902-128">29</span></span>    | <span data-ttu-id="2f902-129">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="2f902-129">The context code.</span></span> <span data-ttu-id="2f902-130">La valeur est 1 si la touche ALT est maintenue enfoncée pendant que la touche est enfoncée ; dans le cas contraire, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="2f902-130">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="2f902-131">30</span><span class="sxs-lookup"><span data-stu-id="2f902-131">30</span></span>    | <span data-ttu-id="2f902-132">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="2f902-132">The previous key state.</span></span> <span data-ttu-id="2f902-133">La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.</span><span class="sxs-lookup"><span data-stu-id="2f902-133">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="2f902-134">31</span><span class="sxs-lookup"><span data-stu-id="2f902-134">31</span></span>    | <span data-ttu-id="2f902-135">État de transition.</span><span class="sxs-lookup"><span data-stu-id="2f902-135">The transition state.</span></span> <span data-ttu-id="2f902-136">La valeur est 1 si la touche est relâchée, ou 0 si la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="2f902-136">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="2f902-137">Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="2f902-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f902-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f902-138">Return value</span></span>

<span data-ttu-id="2f902-139">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="2f902-139">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="2f902-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="2f902-140">Example</span></span>

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
<span data-ttu-id="2f902-141">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="2f902-141">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f902-142">Notes</span><span class="sxs-lookup"><span data-stu-id="2f902-142">Remarks</span></span>

<span data-ttu-id="2f902-143">Le message **WM \_ char** utilise le format UTF (Unicode Transformation Format)-16.</span><span class="sxs-lookup"><span data-stu-id="2f902-143">The **WM\_CHAR** message uses Unicode Transformation Format (UTF)-16.</span></span>

<span data-ttu-id="2f902-144">Il n’existe pas nécessairement une correspondance un-à-un entre les touches enfoncées et les messages de caractères générés. par conséquent, les informations contenues dans le mot de poids fort du paramètre *lParam* ne sont généralement pas utiles aux applications.</span><span class="sxs-lookup"><span data-stu-id="2f902-144">There is not necessarily a one-to-one correspondence between keys pressed and character messages generated, and so the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="2f902-145">Les informations contenues dans le mot de poids fort ne s’appliquent qu’au dernier message de la [**\_ touche WM**](wm-keydown.md) qui précède la publication du message **WM \_ char** .</span><span class="sxs-lookup"><span data-stu-id="2f902-145">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_CHAR** message.</span></span>

<span data-ttu-id="2f902-146">Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et droite de la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="2f902-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="2f902-147">D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2f902-147">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="2f902-148">Le message [**WM \_ UNICHAR**](wm-unichar.md) est identique à **WM \_ char**, sauf qu’il utilise UTF-32.</span><span class="sxs-lookup"><span data-stu-id="2f902-148">The [**WM\_UNICHAR**](wm-unichar.md) message is the same as **WM\_CHAR**, except it uses UTF-32.</span></span> <span data-ttu-id="2f902-149">Il est conçu pour envoyer ou poster des caractères Unicode dans des fenêtres ANSI et peut gérer des caractères de plan supplémentaires Unicode.</span><span class="sxs-lookup"><span data-stu-id="2f902-149">It is designed to send or post Unicode characters to ANSI windows, and it can handle Unicode Supplementary Plane characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f902-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f902-150">Requirements</span></span>



| <span data-ttu-id="2f902-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f902-151">Requirement</span></span> | <span data-ttu-id="2f902-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f902-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f902-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f902-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2f902-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f902-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2f902-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f902-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2f902-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f902-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2f902-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f902-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f902-158"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f902-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f902-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f902-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f902-160">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2f902-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f902-161">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="2f902-161">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="2f902-162">**WM- \_ touche**</span><span class="sxs-lookup"><span data-stu-id="2f902-162">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="2f902-163">**\_UNICHAR WM**</span><span class="sxs-lookup"><span data-stu-id="2f902-163">**WM\_UNICHAR**</span></span>](wm-unichar.md)
</dt> <dt>

<span data-ttu-id="2f902-164">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="2f902-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f902-165">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="2f902-165">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

