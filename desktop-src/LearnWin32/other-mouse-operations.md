---
title: Opérations de souris diverses
description: Les sections précédentes ont abordé les clics de souris et le mouvement de la souris. Voici d’autres opérations qui peuvent être effectuées avec la souris.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31877ab5a71819fa896fd1253e7391f9ed748dffff636ab9d3e8591669b7fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387965"
---
# <a name="miscellaneous-mouse-operations"></a>Opérations de souris diverses

Les sections précédentes ont abordé les clics de souris et le mouvement de la souris. Voici d’autres opérations qui peuvent être effectuées avec la souris.

## <a name="dragging-ui-elements"></a>Faire glisser des éléments d’interface utilisateur

Si votre interface utilisateur prend en charge l’opération de glisser-déplacer des éléments d’interface utilisateur, vous devez appeler une autre fonction dans le gestionnaire de messages de la souris : [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect). La fonction **DragDetect** retourne la **valeur true** si l’utilisateur lance un mouvement de souris qui doit être interprété comme faisant glisser. Le code suivant illustre l’utilisation de cette fonction.


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



Voici l’idée : lorsqu’un programme prend en charge le glisser-déplacer, vous ne voulez pas que chaque clic de souris soit interprété comme un glissement. Dans le cas contraire, l’utilisateur peut faire glisser accidentellement un événement lorsqu’il veut simplement cliquer dessus (par exemple, pour le sélectionner). Toutefois, si une souris est particulièrement sensible, il peut être difficile de garder la souris toujours tout en cliquant. par conséquent, Windows définit un seuil de glissement de quelques pixels. Quand l’utilisateur appuie sur le bouton de la souris, il n’est pas considéré comme un glissement, sauf si la souris franchit ce seuil. La fonction [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) teste si ce seuil est atteint. Si la fonction retourne la **valeur true**, vous pouvez interpréter le clic de souris comme un glisser-déplacer. Sinon, ne le faites pas.

> [!Note]  
> si [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) retourne la **valeur false**, Windows supprime le message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) lorsque l’utilisateur relâche le bouton de la souris. Par conséquent, n’appelez pas **DragDetect** , sauf si votre programme est actuellement en mode qui prend en charge le glissement. (Par exemple, si un élément d’interface utilisateur qui peut être déplacé est déjà sélectionné.) À la fin de ce module, nous verrons un exemple de code plus long qui utilise la fonction **DragDetect** .

 

## <a name="confining-the-cursor"></a>Affinage du curseur

Parfois, vous souhaiterez peut-être limiter le curseur à la zone cliente ou à une partie de la zone cliente. La fonction [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restreint le déplacement du curseur dans un rectangle spécifié. Ce rectangle étant donné en coordonnées d’écran, plutôt qu’en coordonnées clientes, le point (0,0) correspond au coin supérieur gauche de l’écran. Pour traduire les coordonnées clientes en coordonnées d’écran, appelez la fonction [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).

Le code suivant permet d’affiner le curseur dans la zone cliente de la fenêtre.


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



[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) prend une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) , mais [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) prend une structure [**point**](/previous-versions//dd162805(v=vs.85)) . Un rectangle est défini par ses points supérieur gauche et inférieur droit. Vous pouvez confiner le curseur sur n’importe quelle zone rectangulaire, y compris les zones en dehors de la fenêtre, mais le fait d’affiner le curseur dans la zone cliente est un moyen classique d’utiliser la fonction. L’affinement du curseur sur une région en dehors de votre fenêtre serait inhabituel, et les utilisateurs le percevront probablement comme un bogue.

Pour supprimer la restriction, appelez [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) avec la valeur **null**.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Événements de suivi de la souris : pointage et départ

Deux autres messages de la souris sont désactivés par défaut, mais peuvent être utiles pour certaines applications :

-   [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): le curseur a pointé sur la zone cliente pendant une période fixe.
-   [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): le curseur a quitté la zone cliente.

Pour activer ces messages, appelez la fonction [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



La structure [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contient les paramètres de la fonction. Le membre **dwFlags** de la structure contient des indicateurs binaires qui spécifient les messages de suivi qui vous intéressent. Vous pouvez choisir d’utiliser [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) et [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), comme illustré ici, ou simplement l’un des deux. Le membre **dwHoverTime** spécifie la durée pendant laquelle la souris doit pointer avant que le système génère un message de pointage. Cette valeur est exprimée en millisecondes. La **\_ valeur par défaut de survol** constante signifie utiliser la valeur système par défaut.

Une fois que vous avez obtenu l’un des messages que vous avez demandés, la fonction [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) se réinitialise. Vous devez l’appeler à nouveau pour recevoir un autre message de suivi. Toutefois, vous devez attendre le prochain message de déplacement de la souris avant d’appeler à nouveau **TrackMouseEvent** . Dans le cas contraire, votre fenêtre peut être inondée de messages de suivi. Par exemple, si la souris pointe, le système continue à générer un flux de messages [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) alors que la souris est immobile. Vous ne voulez pas vraiment un autre message **WM \_ MOUSEHOVER** tant que la souris n’est pas déplacée vers un autre emplacement et pointé à nouveau.

Voici une petite classe d’assistance que vous pouvez utiliser pour gérer les événements de suivi de la souris.


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



L’exemple suivant montre comment utiliser cette classe dans votre procédure de fenêtre.


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



Les événements de suivi de la souris requièrent un traitement supplémentaire par le système. laissez-les désactivés si vous n’en avez pas besoin.

À des fins d’exhaustivité, voici une fonction qui interroge le système à la recherche du délai d’expiration du pointage par défaut.


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



## <a name="mouse-wheel"></a>Roulette de la souris

La fonction suivante vérifie si une roulette de souris est présente.


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



Si l’utilisateur fait tourner la roulette de la souris, la fenêtre qui a le focus reçoit un message [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) . Le paramètre *wParam* de ce message contient une valeur entière appelée *Delta* qui mesure le degré de rotation de la roulette. Le delta utilise des unités arbitraires, où 120 unités est définie comme la rotation nécessaire pour effectuer une « action ». Bien entendu, la définition d’une action dépend de votre programme. Par exemple, si la roulette de la souris est utilisée pour faire défiler le texte, chaque unité de rotation 120 fait défiler une ligne de texte.

Le signe du Delta indique le sens de la rotation :

-   Positif : faire pivoter vers l’avant, en dehors de l’utilisateur.
-   Négatif : faire pivoter vers l’arrière, vers l’utilisateur.

La valeur du Delta est placée dans *wParam* avec quelques indicateurs supplémentaires. Utilisez la macro [**Obtient \_ Wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) pour récupérer la valeur du delta.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Si la roulette de la souris a une haute résolution, la valeur absolue du Delta peut être inférieure à 120. Dans ce cas, s’il est logique que l’action se produise dans des incréments plus petits, vous pouvez le faire. Par exemple, le texte peut faire défiler par incréments de moins d’une ligne. Dans le cas contraire, accumulez le delta total jusqu’à ce que la roue tourne suffisamment pour effectuer l’action. Stockez le delta inutilisé dans une variable et, lorsque 120 unités s’accumulent (soit positif, soit négatif), effectuez l’action.

## <a name="next"></a>Suivant

[Entrée au clavier](keyboard-input.md)

 

 