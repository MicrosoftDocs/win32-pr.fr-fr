---
title: Opérations de souris diverses
description: Les sections précédentes ont abordé les clics de souris et le mouvement de la souris. Voici d’autres opérations qui peuvent être effectuées avec la souris.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315066"
---
# <a name="miscellaneous-mouse-operations"></a><span data-ttu-id="2657d-104">Opérations de souris diverses</span><span class="sxs-lookup"><span data-stu-id="2657d-104">Miscellaneous Mouse Operations</span></span>

<span data-ttu-id="2657d-105">Les sections précédentes ont abordé les clics de souris et le mouvement de la souris.</span><span class="sxs-lookup"><span data-stu-id="2657d-105">The previous sections have discussed mouse clicks and mouse movement.</span></span> <span data-ttu-id="2657d-106">Voici d’autres opérations qui peuvent être effectuées avec la souris.</span><span class="sxs-lookup"><span data-stu-id="2657d-106">Here are some other operations that can be performed with the mouse.</span></span>

## <a name="dragging-ui-elements"></a><span data-ttu-id="2657d-107">Faire glisser des éléments d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="2657d-107">Dragging UI Elements</span></span>

<span data-ttu-id="2657d-108">Si votre interface utilisateur prend en charge l’opération de glisser-déplacer des éléments d’interface utilisateur, vous devez appeler une autre fonction dans le gestionnaire de messages de la souris : [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span><span class="sxs-lookup"><span data-stu-id="2657d-108">If your UI supports dragging of UI elements, there is one other function that you should call in your mouse-down message handler: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span></span> <span data-ttu-id="2657d-109">La fonction **DragDetect** retourne la **valeur true** si l’utilisateur lance un mouvement de souris qui doit être interprété comme faisant glisser.</span><span class="sxs-lookup"><span data-stu-id="2657d-109">The **DragDetect** function returns **TRUE** if the user initiates a mouse gesture that should be interpreted as dragging.</span></span> <span data-ttu-id="2657d-110">Le code suivant illustre l’utilisation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="2657d-110">The following code shows how to use this function.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



<span data-ttu-id="2657d-111">Voici l’idée : lorsqu’un programme prend en charge le glisser-déplacer, vous ne voulez pas que chaque clic de souris soit interprété comme un glissement.</span><span class="sxs-lookup"><span data-stu-id="2657d-111">Here's the idea: When a program supports drag and drop, you don't want every mouse click to be interpreted as a drag.</span></span> <span data-ttu-id="2657d-112">Dans le cas contraire, l’utilisateur peut faire glisser accidentellement un événement lorsqu’il veut simplement cliquer dessus (par exemple, pour le sélectionner).</span><span class="sxs-lookup"><span data-stu-id="2657d-112">Otherwise, the user might accidentally drag something when he or she simply meant to click on it (for example, to select it).</span></span> <span data-ttu-id="2657d-113">Toutefois, si une souris est particulièrement sensible, il peut être difficile de garder la souris toujours tout en cliquant.</span><span class="sxs-lookup"><span data-stu-id="2657d-113">But if a mouse is particularly sensitive, it can be hard to keep the mouse perfectly still while clicking.</span></span> <span data-ttu-id="2657d-114">Par conséquent, Windows définit un seuil de glissement de quelques pixels.</span><span class="sxs-lookup"><span data-stu-id="2657d-114">Therefore, Windows defines a drag threshold of a few pixels.</span></span> <span data-ttu-id="2657d-115">Quand l’utilisateur appuie sur le bouton de la souris, il n’est pas considéré comme un glissement, sauf si la souris franchit ce seuil.</span><span class="sxs-lookup"><span data-stu-id="2657d-115">When the user presses the mouse button, it is not considered a drag unless the mouse crosses this threshold.</span></span> <span data-ttu-id="2657d-116">La fonction [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) teste si ce seuil est atteint.</span><span class="sxs-lookup"><span data-stu-id="2657d-116">The [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function tests whether this threshold is reached.</span></span> <span data-ttu-id="2657d-117">Si la fonction retourne la **valeur true**, vous pouvez interpréter le clic de souris comme un glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="2657d-117">If the function returns **TRUE**, you can interpret the mouse click as a drag.</span></span> <span data-ttu-id="2657d-118">Sinon, ne le faites pas.</span><span class="sxs-lookup"><span data-stu-id="2657d-118">Otherwise, do not.</span></span>

> [!Note]  
> <span data-ttu-id="2657d-119">Si [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) retourne la **valeur false**, Windows supprime le message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) lorsque l’utilisateur relâche le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="2657d-119">If [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) returns **FALSE**, Windows suppresses the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message when the user releases the mouse button.</span></span> <span data-ttu-id="2657d-120">Par conséquent, n’appelez pas **DragDetect** , sauf si votre programme est actuellement en mode qui prend en charge le glissement.</span><span class="sxs-lookup"><span data-stu-id="2657d-120">Therefore, do not call **DragDetect** unless your program is currently in a mode that supports dragging.</span></span> <span data-ttu-id="2657d-121">(Par exemple, si un élément d’interface utilisateur qui peut être déplacé est déjà sélectionné.) À la fin de ce module, nous verrons un exemple de code plus long qui utilise la fonction **DragDetect** .</span><span class="sxs-lookup"><span data-stu-id="2657d-121">(For example, if a draggable UI element is already selected.) At the end of this module, we will see a longer code example that uses the **DragDetect** function.</span></span>

 

## <a name="confining-the-cursor"></a><span data-ttu-id="2657d-122">Affinage du curseur</span><span class="sxs-lookup"><span data-stu-id="2657d-122">Confining the Cursor</span></span>

<span data-ttu-id="2657d-123">Parfois, vous souhaiterez peut-être limiter le curseur à la zone cliente ou à une partie de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="2657d-123">Sometimes you might want to restrict the cursor to the client area or a portion of the client area.</span></span> <span data-ttu-id="2657d-124">La fonction [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restreint le déplacement du curseur dans un rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="2657d-124">The [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function restricts the movement of the cursor to a specified rectangle.</span></span> <span data-ttu-id="2657d-125">Ce rectangle étant donné en coordonnées d’écran, plutôt qu’en coordonnées clientes, le point (0,0) correspond au coin supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2657d-125">This rectangle is given in screen coordinates, rather than client coordinates, so the point (0, 0) means the upper left corner of the screen.</span></span> <span data-ttu-id="2657d-126">Pour traduire les coordonnées clientes en coordonnées d’écran, appelez la fonction [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span><span class="sxs-lookup"><span data-stu-id="2657d-126">To translate client coordinates into screen coordinates, call the function [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span></span>

<span data-ttu-id="2657d-127">Le code suivant permet d’affiner le curseur dans la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2657d-127">The following code confines the cursor to the client area of the window.</span></span>


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



<span data-ttu-id="2657d-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) prend une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) , mais [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) prend une structure [**point**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2657d-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) takes a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure, but [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) takes a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="2657d-129">Un rectangle est défini par ses points supérieur gauche et inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="2657d-129">A rectangle is defined by its top-left and bottom-right points.</span></span> <span data-ttu-id="2657d-130">Vous pouvez confiner le curseur sur n’importe quelle zone rectangulaire, y compris les zones en dehors de la fenêtre, mais le fait d’affiner le curseur dans la zone cliente est un moyen classique d’utiliser la fonction.</span><span class="sxs-lookup"><span data-stu-id="2657d-130">You can confine the cursor to any rectangular area, including areas outside the window, but confining the cursor to the client area is a typical way to use the function.</span></span> <span data-ttu-id="2657d-131">L’affinement du curseur sur une région en dehors de votre fenêtre serait inhabituel, et les utilisateurs le percevront probablement comme un bogue.</span><span class="sxs-lookup"><span data-stu-id="2657d-131">Confining the cursor to a region entirely outside your window would be unusual, and users would probably perceive it as a bug.</span></span>

<span data-ttu-id="2657d-132">Pour supprimer la restriction, appelez [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) avec la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="2657d-132">To remove the restriction, call [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) with the value **NULL**.</span></span>


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a><span data-ttu-id="2657d-133">Événements de suivi de la souris : pointage et départ</span><span class="sxs-lookup"><span data-stu-id="2657d-133">Mouse Tracking Events: Hover and Leave</span></span>

<span data-ttu-id="2657d-134">Deux autres messages de la souris sont désactivés par défaut, mais peuvent être utiles pour certaines applications :</span><span class="sxs-lookup"><span data-stu-id="2657d-134">Two other mouse messages are disabled by default, but may be useful for some applications:</span></span>

-   <span data-ttu-id="2657d-135">[**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): le curseur a pointé sur la zone cliente pendant une période fixe.</span><span class="sxs-lookup"><span data-stu-id="2657d-135">[**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): The cursor has hovered over the client area for a fixed period of time.</span></span>
-   <span data-ttu-id="2657d-136">[**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): le curseur a quitté la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="2657d-136">[**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): The cursor has left the client area.</span></span>

<span data-ttu-id="2657d-137">Pour activer ces messages, appelez la fonction [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="2657d-137">To enable these messages, call the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function.</span></span>


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



<span data-ttu-id="2657d-138">La structure [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contient les paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2657d-138">The [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) structure contains the parameters for the function.</span></span> <span data-ttu-id="2657d-139">Le membre **dwFlags** de la structure contient des indicateurs binaires qui spécifient les messages de suivi qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="2657d-139">The **dwFlags** member of the structure contains bit flags that specify which tracking messages you are interested in.</span></span> <span data-ttu-id="2657d-140">Vous pouvez choisir d’utiliser [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) et [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), comme illustré ici, ou simplement l’un des deux.</span><span class="sxs-lookup"><span data-stu-id="2657d-140">You can choose to get both [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) and [**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), as shown here, or just one of the two.</span></span> <span data-ttu-id="2657d-141">Le membre **dwHoverTime** spécifie la durée pendant laquelle la souris doit pointer avant que le système génère un message de pointage.</span><span class="sxs-lookup"><span data-stu-id="2657d-141">The **dwHoverTime** member specifies how long the mouse needs to hover before the system generates a hover message.</span></span> <span data-ttu-id="2657d-142">Cette valeur est exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2657d-142">This value is given in milliseconds.</span></span> <span data-ttu-id="2657d-143">La **\_ valeur par défaut de survol** constante signifie utiliser la valeur système par défaut.</span><span class="sxs-lookup"><span data-stu-id="2657d-143">The constant **HOVER\_DEFAULT** means to use the system default.</span></span>

<span data-ttu-id="2657d-144">Une fois que vous avez obtenu l’un des messages que vous avez demandés, la fonction [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) se réinitialise.</span><span class="sxs-lookup"><span data-stu-id="2657d-144">After you get one of the messages that you requested, the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function resets.</span></span> <span data-ttu-id="2657d-145">Vous devez l’appeler à nouveau pour recevoir un autre message de suivi.</span><span class="sxs-lookup"><span data-stu-id="2657d-145">You must call it again to get another tracking message.</span></span> <span data-ttu-id="2657d-146">Toutefois, vous devez attendre le prochain message de déplacement de la souris avant d’appeler à nouveau **TrackMouseEvent** .</span><span class="sxs-lookup"><span data-stu-id="2657d-146">However, you should wait until the next mouse-move message before calling **TrackMouseEvent** again.</span></span> <span data-ttu-id="2657d-147">Dans le cas contraire, votre fenêtre peut être inondée de messages de suivi.</span><span class="sxs-lookup"><span data-stu-id="2657d-147">Otherwise, your window might be flooded with tracking messages.</span></span> <span data-ttu-id="2657d-148">Par exemple, si la souris pointe, le système continue à générer un flux de messages [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) alors que la souris est immobile.</span><span class="sxs-lookup"><span data-stu-id="2657d-148">For example, if the mouse is hovering, the system would continue to generate a stream of [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) messages while the mouse is stationary.</span></span> <span data-ttu-id="2657d-149">Vous ne voulez pas vraiment un autre message **WM \_ MOUSEHOVER** tant que la souris n’est pas déplacée vers un autre emplacement et pointé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2657d-149">You don't actually want another **WM\_MOUSEHOVER** message until the mouse moves to another spot and hovers again.</span></span>

<span data-ttu-id="2657d-150">Voici une petite classe d’assistance que vous pouvez utiliser pour gérer les événements de suivi de la souris.</span><span class="sxs-lookup"><span data-stu-id="2657d-150">Here is a small helper class that you can use to manage mouse-tracking events.</span></span>


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



<span data-ttu-id="2657d-151">L’exemple suivant montre comment utiliser cette classe dans votre procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2657d-151">The next example shows how to use this class in your window procedure.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="2657d-152">Les événements de suivi de la souris requièrent un traitement supplémentaire par le système. laissez-les désactivés si vous n’en avez pas besoin.</span><span class="sxs-lookup"><span data-stu-id="2657d-152">Mouse tracking events require additional processing by the system, so leave them disabled if you do not need them.</span></span>

<span data-ttu-id="2657d-153">À des fins d’exhaustivité, voici une fonction qui interroge le système à la recherche du délai d’expiration du pointage par défaut.</span><span class="sxs-lookup"><span data-stu-id="2657d-153">For completeness, here is a function that queries the system for the default hover timeout.</span></span>


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a><span data-ttu-id="2657d-154">Roulette de la souris</span><span class="sxs-lookup"><span data-stu-id="2657d-154">Mouse Wheel</span></span>

<span data-ttu-id="2657d-155">La fonction suivante vérifie si une roulette de souris est présente.</span><span class="sxs-lookup"><span data-stu-id="2657d-155">The following function checks if a mouse wheel is present.</span></span>


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



<span data-ttu-id="2657d-156">Si l’utilisateur fait tourner la roulette de la souris, la fenêtre qui a le focus reçoit un message [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) .</span><span class="sxs-lookup"><span data-stu-id="2657d-156">If the user rotates the mouse wheel, the window with focus receives a [**WM\_MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) message.</span></span> <span data-ttu-id="2657d-157">Le paramètre *wParam* de ce message contient une valeur entière appelée *Delta* qui mesure le degré de rotation de la roulette.</span><span class="sxs-lookup"><span data-stu-id="2657d-157">The *wParam* parameter of this message contains an integer value called the *delta* that measures how far the wheel was rotated.</span></span> <span data-ttu-id="2657d-158">Le delta utilise des unités arbitraires, où 120 unités est définie comme la rotation nécessaire pour effectuer une « action ».</span><span class="sxs-lookup"><span data-stu-id="2657d-158">The delta uses arbitrary units, where 120 units is defined as the rotation needed to perform one "action."</span></span> <span data-ttu-id="2657d-159">Bien entendu, la définition d’une action dépend de votre programme.</span><span class="sxs-lookup"><span data-stu-id="2657d-159">Of course, the definition of an action depends on your program.</span></span> <span data-ttu-id="2657d-160">Par exemple, si la roulette de la souris est utilisée pour faire défiler le texte, chaque unité de rotation 120 fait défiler une ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="2657d-160">For example, if the mouse wheel is used to scroll text, each 120 units of rotation would scroll one line of text.</span></span>

<span data-ttu-id="2657d-161">Le signe du Delta indique le sens de la rotation :</span><span class="sxs-lookup"><span data-stu-id="2657d-161">The sign of the delta indicates the direction of rotation:</span></span>

-   <span data-ttu-id="2657d-162">Positif : faire pivoter vers l’avant, en dehors de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2657d-162">Positive: Rotate forward, away from the user.</span></span>
-   <span data-ttu-id="2657d-163">Négatif : faire pivoter vers l’arrière, vers l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2657d-163">Negative: Rotate backward, toward the user.</span></span>

<span data-ttu-id="2657d-164">La valeur du Delta est placée dans *wParam* avec quelques indicateurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2657d-164">The value of the delta is placed in *wParam* along with some additional flags.</span></span> <span data-ttu-id="2657d-165">Utilisez la macro [**Obtient \_ Wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) pour récupérer la valeur du delta.</span><span class="sxs-lookup"><span data-stu-id="2657d-165">Use the [**GET\_WHEEL\_DELTA\_WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) macro to get the value of the delta.</span></span>


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="2657d-166">Si la roulette de la souris a une haute résolution, la valeur absolue du Delta peut être inférieure à 120.</span><span class="sxs-lookup"><span data-stu-id="2657d-166">If the mouse wheel has a high resolution, the absolute value of the delta might be less than 120.</span></span> <span data-ttu-id="2657d-167">Dans ce cas, s’il est logique que l’action se produise dans des incréments plus petits, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="2657d-167">In that case, if it makes sense for the action to occur in smaller increments, you can do so.</span></span> <span data-ttu-id="2657d-168">Par exemple, le texte peut faire défiler par incréments de moins d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="2657d-168">For example, text could scroll by increments of less than one line.</span></span> <span data-ttu-id="2657d-169">Dans le cas contraire, accumulez le delta total jusqu’à ce que la roue tourne suffisamment pour effectuer l’action.</span><span class="sxs-lookup"><span data-stu-id="2657d-169">Otherwise, accumulate the total delta until the wheel rotates enough to perform the action.</span></span> <span data-ttu-id="2657d-170">Stockez le delta inutilisé dans une variable et, lorsque 120 unités s’accumulent (soit positif, soit négatif), effectuez l’action.</span><span class="sxs-lookup"><span data-stu-id="2657d-170">Store the unused delta in a variable, and when 120 units accumulate (either positive or negative), perform the action.</span></span>

## <a name="next"></a><span data-ttu-id="2657d-171">Suivant</span><span class="sxs-lookup"><span data-stu-id="2657d-171">Next</span></span>

[<span data-ttu-id="2657d-172">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="2657d-172">Keyboard Input</span></span>](keyboard-input.md)

 

 