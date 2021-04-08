---
title: Réponse aux clics de souris
description: Réponse aux clics de souris
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101620"
---
# <a name="responding-to-mouse-clicks"></a><span data-ttu-id="c972f-103">Réponse aux clics de souris</span><span class="sxs-lookup"><span data-stu-id="c972f-103">Responding to Mouse Clicks</span></span>

<span data-ttu-id="c972f-104">Si l’utilisateur clique sur un bouton de la souris alors que le curseur se trouve sur la zone cliente d’une fenêtre, la fenêtre reçoit l’un des messages suivants.</span><span class="sxs-lookup"><span data-stu-id="c972f-104">If the user clicks a mouse button while the cursor is over the client area of a window, the window receives one of the following messages.</span></span>



| <span data-ttu-id="c972f-105">Message</span><span class="sxs-lookup"><span data-stu-id="c972f-105">Message</span></span>                                        | <span data-ttu-id="c972f-106">Signification</span><span class="sxs-lookup"><span data-stu-id="c972f-106">Meaning</span></span>                   |
|------------------------------------------------|---------------------------|
| [<span data-ttu-id="c972f-107">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-107">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown) | <span data-ttu-id="c972f-108">Bouton gauche enfoncé</span><span class="sxs-lookup"><span data-stu-id="c972f-108">Left button down</span></span>          |
| [<span data-ttu-id="c972f-109">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-109">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)     | <span data-ttu-id="c972f-110">Bouton gauche vers le haut</span><span class="sxs-lookup"><span data-stu-id="c972f-110">Left button up</span></span>            |
| [<span data-ttu-id="c972f-111">**\_MBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-111">**WM\_MBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-mbuttondown) | <span data-ttu-id="c972f-112">Bouton central enfoncé</span><span class="sxs-lookup"><span data-stu-id="c972f-112">Middle button down</span></span>        |
| [<span data-ttu-id="c972f-113">**\_MBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-113">**WM\_MBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-mbuttonup)     | <span data-ttu-id="c972f-114">Bouton central vers le haut</span><span class="sxs-lookup"><span data-stu-id="c972f-114">Middle button up</span></span>          |
| [<span data-ttu-id="c972f-115">**\_RBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-115">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown) | <span data-ttu-id="c972f-116">Bouton droit enfoncé</span><span class="sxs-lookup"><span data-stu-id="c972f-116">Right button down</span></span>         |
| [<span data-ttu-id="c972f-117">**\_RBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-117">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)     | <span data-ttu-id="c972f-118">Bouton droit vers le haut</span><span class="sxs-lookup"><span data-stu-id="c972f-118">Right button up</span></span>           |
| [<span data-ttu-id="c972f-119">**\_XBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-119">**WM\_XBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-xbuttondown) | <span data-ttu-id="c972f-120">LE bouton XButton1 ou XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="c972f-120">XBUTTON1 or XBUTTON2 down</span></span> |
| [<span data-ttu-id="c972f-121">**\_XBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-121">**WM\_XBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-xbuttonup)     | <span data-ttu-id="c972f-122">LE bouton XButton1 ou XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="c972f-122">XBUTTON1 or XBUTTON2 up</span></span>   |



 

<span data-ttu-id="c972f-123">Souvenez-vous que la zone cliente est la partie de la fenêtre qui exclut le frame.</span><span class="sxs-lookup"><span data-stu-id="c972f-123">Recall that the client area is the portion of the window that excludes the frame.</span></span> <span data-ttu-id="c972f-124">Pour plus d’informations sur les zones clientes, consultez [qu’est-ce qu’une fenêtre ?](what-is-a-window-.md)</span><span class="sxs-lookup"><span data-stu-id="c972f-124">For more information about client areas, see [What Is a Window?](what-is-a-window-.md)</span></span>

### <a name="mouse-coordinates"></a><span data-ttu-id="c972f-125">Coordonnées de la souris</span><span class="sxs-lookup"><span data-stu-id="c972f-125">Mouse Coordinates</span></span>

<span data-ttu-id="c972f-126">Dans tous ces messages, le paramètre *lParam* contient les coordonnées x et y du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="c972f-126">In all of these messages, the *lParam* parameter contains the x- and y-coordinates of the mouse pointer.</span></span> <span data-ttu-id="c972f-127">Les 16 bits les plus bas de *lParam* contiennent la coordonnée x, et les 16 bits suivants contiennent la coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="c972f-127">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="c972f-128">Utilisez les macros [**obten \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour décompresser les coordonnées de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c972f-128">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="c972f-129">Ces macros sont définies dans le fichier d’en-tête WindowsX. h.</span><span class="sxs-lookup"><span data-stu-id="c972f-129">These macros are defined in the header file WindowsX.h.</span></span>

<span data-ttu-id="c972f-130">Sur Windows 64 bits, *lParam* est une valeur de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c972f-130">On 64-bit Windows, *lParam* is 64-bit value.</span></span> <span data-ttu-id="c972f-131">Les 32 bits supérieurs de *lParam* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="c972f-131">The upper 32 bits of *lParam* are not used.</span></span> <span data-ttu-id="c972f-132">La documentation MSDN mentionne le « mot de poids faible » et le « mot de poids fort » de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c972f-132">The MSDN documentation mentions the "low-order word" and "high-order word" of *lParam*.</span></span> <span data-ttu-id="c972f-133">Dans le cas 64 bits, cela signifie que les mots de poids fort et de poids fort des 32 bits inférieurs.</span><span class="sxs-lookup"><span data-stu-id="c972f-133">In the 64-bit case, this means the low- and high-order words of the lower 32 bits.</span></span> <span data-ttu-id="c972f-134">Les macros extraient les valeurs correctes. par conséquent, si vous les utilisez, vous en êtes sûr.</span><span class="sxs-lookup"><span data-stu-id="c972f-134">The macros extract the right values, so if you use them, you will be safe.</span></span>

<span data-ttu-id="c972f-135">Les coordonnées de la souris sont exprimées en pixels, et non en pixels indépendants du périphérique (DIP). elles sont mesurées par rapport à la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c972f-135">Mouse coordinates are given in pixels, not device-independent pixels (DIPs), and are measured relative to the client area of the window.</span></span> <span data-ttu-id="c972f-136">Les coordonnées sont des valeurs signées.</span><span class="sxs-lookup"><span data-stu-id="c972f-136">Coordinates are signed values.</span></span> <span data-ttu-id="c972f-137">Les positions au-dessus et à gauche de la zone cliente ont des coordonnées négatives, ce qui est important si vous effectuez le suivi de la position de la souris en dehors de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c972f-137">Positions above and to the left of the client area have negative coordinates, which is important if you track the mouse position outside the window.</span></span> <span data-ttu-id="c972f-138">Nous verrons comment le faire dans une rubrique ultérieure, en [capturant le mouvement de la souris en dehors de la fenêtre](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="c972f-138">We will see how to do that in a later topic, [Capturing Mouse Movement Outside the Window](mouse-movement.md).</span></span>

### <a name="additional-flags"></a><span data-ttu-id="c972f-139">Indicateurs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c972f-139">Additional Flags</span></span>

<span data-ttu-id="c972f-140">Le paramètre *wParam* contient une opération or au niveau du bit, indiquant l’état des autres **boutons de la** souris plus les touches Maj et Ctrl.</span><span class="sxs-lookup"><span data-stu-id="c972f-140">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span>



| <span data-ttu-id="c972f-141">Indicateur</span><span class="sxs-lookup"><span data-stu-id="c972f-141">Flag</span></span>             | <span data-ttu-id="c972f-142">Signification</span><span class="sxs-lookup"><span data-stu-id="c972f-142">Meaning</span></span>                          |
|------------------|----------------------------------|
| <span data-ttu-id="c972f-143">**\_contrôle MK**</span><span class="sxs-lookup"><span data-stu-id="c972f-143">**MK\_CONTROL**</span></span>  | <span data-ttu-id="c972f-144">La touche CTRL est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="c972f-144">The CTRL key is down.</span></span>            |
| <span data-ttu-id="c972f-145">**\_LBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="c972f-145">**MK\_LBUTTON**</span></span>  | <span data-ttu-id="c972f-146">Le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c972f-146">The left mouse button is down.</span></span>   |
| <span data-ttu-id="c972f-147">**\_MBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="c972f-147">**MK\_MBUTTON**</span></span>  | <span data-ttu-id="c972f-148">Le bouton central de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c972f-148">The middle mouse button is down.</span></span> |
| <span data-ttu-id="c972f-149">**\_RBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="c972f-149">**MK\_RBUTTON**</span></span>  | <span data-ttu-id="c972f-150">Le bouton droit de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c972f-150">The right mouse button is down.</span></span>  |
| <span data-ttu-id="c972f-151">**\_MAJ MK**</span><span class="sxs-lookup"><span data-stu-id="c972f-151">**MK\_SHIFT**</span></span>    | <span data-ttu-id="c972f-152">La touche Maj est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="c972f-152">The SHIFT key is down.</span></span>           |
| <span data-ttu-id="c972f-153">**\_Le bouton XButton1 MK**</span><span class="sxs-lookup"><span data-stu-id="c972f-153">**MK\_XBUTTON1**</span></span> | <span data-ttu-id="c972f-154">Le bouton le bouton XButton1 est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c972f-154">The XBUTTON1 button is down.</span></span>     |
| <span data-ttu-id="c972f-155">**\_XButton2 MK**</span><span class="sxs-lookup"><span data-stu-id="c972f-155">**MK\_XBUTTON2**</span></span> | <span data-ttu-id="c972f-156">Le bouton XBUTTON2 est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c972f-156">The XBUTTON2 button is down.</span></span>     |



 

<span data-ttu-id="c972f-157">L’absence d’un indicateur signifie que le bouton ou la touche correspondant n’a pas été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c972f-157">The absence of a flag means the corresponding button or key was not pressed.</span></span> <span data-ttu-id="c972f-158">Par exemple, pour tester si la touche CTRL est enfoncée :</span><span class="sxs-lookup"><span data-stu-id="c972f-158">For example, to test whether the CTRL key is down:</span></span>


```C++
if (wParam & MK_CONTROL) { ...
```



<span data-ttu-id="c972f-159">Si vous devez Rechercher l’état d’autres clés en plus de CTRL et Maj, utilisez la fonction [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , qui est décrite dans [entrée au clavier](keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="c972f-159">If you need to find the state of other keys besides CTRL and SHIFT, use the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function, which is described in [Keyboard Input](keyboard-input.md).</span></span>

<span data-ttu-id="c972f-160">Les messages de fenêtre [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) et [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) s’appliquent à le bouton XButton1 et XButton2.</span><span class="sxs-lookup"><span data-stu-id="c972f-160">The [**WM\_XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) and [**WM\_XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) window messages apply to both XBUTTON1 and XBUTTON2.</span></span> <span data-ttu-id="c972f-161">Le paramètre *wParam* indique le bouton sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="c972f-161">The *wParam* parameter indicates which button was clicked.</span></span>


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a><span data-ttu-id="c972f-162">Double-clic</span><span class="sxs-lookup"><span data-stu-id="c972f-162">Double Clicks</span></span>

<span data-ttu-id="c972f-163">Une fenêtre ne reçoit pas de notifications de double-clic par défaut.</span><span class="sxs-lookup"><span data-stu-id="c972f-163">A window does not receive double-click notifications by default.</span></span> <span data-ttu-id="c972f-164">Pour recevoir des doubles clics, définissez l’indicateur **cs \_ DBLCLKS** dans la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) lorsque vous inscrivez la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c972f-164">To receive double clicks, set the **CS\_DBLCLKS** flag in the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when you register the window class.</span></span>


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



<span data-ttu-id="c972f-165">Si vous définissez l’indicateur **cs \_ DBLCLKS** comme indiqué, la fenêtre recevra des notifications de double-clic.</span><span class="sxs-lookup"><span data-stu-id="c972f-165">If you set the **CS\_DBLCLKS** flag as shown, the window will receive double-click notifications.</span></span> <span data-ttu-id="c972f-166">Un double-clic est indiqué par un message de fenêtre avec « DBLCLK » dans le nom.</span><span class="sxs-lookup"><span data-stu-id="c972f-166">A double click is indicated by a window message with "DBLCLK" in the name.</span></span> <span data-ttu-id="c972f-167">Par exemple, un double-clic sur le bouton gauche de la souris produit la séquence de messages suivante :</span><span class="sxs-lookup"><span data-stu-id="c972f-167">For example, a double click on the left mouse button produces the following sequence of messages:</span></span>

<dl>

[<span data-ttu-id="c972f-168">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-168">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)  
[<span data-ttu-id="c972f-169">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-169">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
[<span data-ttu-id="c972f-170">**\_LBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-170">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)  
[<span data-ttu-id="c972f-171">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="c972f-171">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

<span data-ttu-id="c972f-172">En effet, le deuxième message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) qui devrait normalement être généré devient un message [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) .</span><span class="sxs-lookup"><span data-stu-id="c972f-172">In effect, the second [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message that would normally be generated becomes a [**WM\_LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) message.</span></span> <span data-ttu-id="c972f-173">Des messages équivalents sont définis pour les boutons droit, moyen et XBUTTON.</span><span class="sxs-lookup"><span data-stu-id="c972f-173">Equivalent messages are defined for right, middle, and XBUTTON buttons.</span></span>

<span data-ttu-id="c972f-174">Tant que vous n’avez pas obtenu le message de double-clic, il n’existe aucun moyen de savoir que le premier clic de souris est le début d’un double-clic.</span><span class="sxs-lookup"><span data-stu-id="c972f-174">Until you get the double-click message, there is no way to tell that the first mouse click is the start of a double click.</span></span> <span data-ttu-id="c972f-175">Par conséquent, une action de double-clic doit continuer une action qui commence par le premier clic de souris.</span><span class="sxs-lookup"><span data-stu-id="c972f-175">Therefore, a double-click action should continue an action that begins with the first mouse click.</span></span> <span data-ttu-id="c972f-176">Par exemple, dans le shell Windows, un seul clic sélectionne un dossier, tandis qu’un double-clic ouvre le dossier.</span><span class="sxs-lookup"><span data-stu-id="c972f-176">For example, in the Windows Shell, a single click selects a folder, while a double click opens the folder.</span></span>

## <a name="non-client-mouse-messages"></a><span data-ttu-id="c972f-177">Messages de souris non-client</span><span class="sxs-lookup"><span data-stu-id="c972f-177">Non-client Mouse Messages</span></span>

<span data-ttu-id="c972f-178">Un ensemble distinct de messages est défini pour les événements de souris qui se produisent dans la zone non cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c972f-178">A separate set of messages are defined for mouse events that occur within the non-client area of the window.</span></span> <span data-ttu-id="c972f-179">Ces messages contiennent les lettres « NC » dans le nom.</span><span class="sxs-lookup"><span data-stu-id="c972f-179">These messages have the letters "NC" in the name.</span></span> <span data-ttu-id="c972f-180">Par exemple, le [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) est l’équivalent non-client de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="c972f-180">For example, [**WM\_NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) is the non-client equivalent of [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="c972f-181">Une application classique n’intercepte pas ces messages, car la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gère ces messages correctement.</span><span class="sxs-lookup"><span data-stu-id="c972f-181">A typical application will not intercept these messages, because the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function handles these messages correctly.</span></span> <span data-ttu-id="c972f-182">Toutefois, elles peuvent être utiles pour certaines fonctions avancées.</span><span class="sxs-lookup"><span data-stu-id="c972f-182">However, they can be useful for certain advanced functions.</span></span> <span data-ttu-id="c972f-183">Par exemple, vous pouvez utiliser ces messages pour implémenter un comportement personnalisé dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="c972f-183">For example, you could use these messages to implement custom behavior in the title bar.</span></span> <span data-ttu-id="c972f-184">Si vous gérez ces messages, vous devez généralement les transmettre à **DefWindowProc** par la suite.</span><span class="sxs-lookup"><span data-stu-id="c972f-184">If you do handle these messages, you should generally pass them to **DefWindowProc** afterward.</span></span> <span data-ttu-id="c972f-185">Dans le cas contraire, votre application interrompt les fonctionnalités standard telles que le glisser-déplacer ou la minimisation de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c972f-185">Otherwise, your application will break standard functionality such as dragging or minimizing the window.</span></span>

## <a name="next"></a><span data-ttu-id="c972f-186">Suivant</span><span class="sxs-lookup"><span data-stu-id="c972f-186">Next</span></span>

[<span data-ttu-id="c972f-187">Mouvement de la souris</span><span class="sxs-lookup"><span data-stu-id="c972f-187">Mouse Movement</span></span>](mouse-movement.md)

 

 