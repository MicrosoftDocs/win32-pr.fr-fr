---
description: Une barre d’outils de bureau d’application (également appelée appbar) est une fenêtre similaire à la barre des tâches Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Utilisation des barres d’outils de l’application Desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112354"
---
# <a name="using-application-desktop-toolbars"></a>Utilisation des barres d’outils de l’application Desktop

Une *barre d’outils de bureau d’application* (également appelée appbar) est une fenêtre similaire à la barre des tâches Windows. Elle est ancrée à un bord de l’écran et contient généralement des boutons qui permettent à l’utilisateur d’accéder rapidement à d’autres applications et fenêtres. Le système empêche d’autres applications d’utiliser la zone de bureau utilisée par un appbar. Un nombre quelconque de barres peut exister sur le Bureau à un moment donné.

Cette rubrique contient les sections suivantes.

-   [À propos des barres d’outils application Desktop](#about-application-desktop-toolbars)
    -   [Envoi de messages](#sending-messages)
    -   [Inscription](#registration)
    -   [Taille et position de appbar](#appbar-size-and-position)
    -   [Masquer automatiquement les barres d’outils du Bureau d’application](#autohide-application-desktop-toolbars)
    -   [Messages de notification appbar](#appbar-notification-messages)
-   [Inscription d’une barre d’outils de bureau d’application](#registering-an-application-desktop-toolbar)
-   [Définition de la taille et de la position appbar](#setting-the-appbar-size-and-position)
-   [Traitement des messages de notification appbar](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>À propos des barres d’outils application Desktop

Windows fournit une API qui vous permet de tirer parti des services appbar fournis par le système. Les services permettent de s’assurer que les barres définis par l’application fonctionnent correctement les uns avec les autres et avec la barre des tâches. Le système gère les informations sur chaque appbar et envoie les messages barres pour les informer des événements qui peuvent affecter leur taille, leur position et leur apparence.

### <a name="sending-messages"></a>sending messages

Une application utilise un ensemble spécial de messages, appelés messages appbar, pour ajouter ou supprimer un appbar, définir la taille et la position d’un appbar et récupérer des informations sur la taille, la position et l’état de la barre des tâches. Pour envoyer un message appbar, une application doit utiliser la fonction [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) . Les paramètres de la fonction incluent un identificateur de message, tel que [**ABM \_ New**](abm-new.md), et l’adresse d’une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Les membres de structure contiennent les informations dont le système a besoin pour traiter le message donné.

Pour tout message appbar donné, le système utilise certains membres de la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) et ignore les autres. Toutefois, le système utilise toujours les membres **cbSize** et **HWND** , de sorte qu’une application doit remplir ces membres pour chaque message appbar. Le membre **cbSize** spécifie la taille de la structure, et le membre **HWND** est le handle de la fenêtre du appbar.

Certains messages appbar demandent des informations du système. Lors du traitement de ces messages, le système copie les informations demandées dans la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

### <a name="registration"></a>Inscription

Le système conserve une liste interne de barres et conserve des informations sur chaque barre de la liste. Le système utilise les informations pour gérer les barres, y effectuer des services et leur envoyer des messages de notification.

Une application doit inscrire un appbar (c’est-à-dire l’ajouter à la liste interne) avant de pouvoir recevoir des services appbar à partir du système. Pour inscrire un appbar, une application envoie le [**\_ nouveau message ABM**](abm-new.md) . La structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) associée comprend le descripteur de la fenêtre du appbar et un identificateur de message défini par l’application. Le système utilise l’identificateur de message pour envoyer des messages de notification à la procédure de fenêtre de la fenêtre appbar. Pour plus d’informations, consultez messages de notification appbar.

Une application annule l’inscription d’un appbar en envoyant le message [**ABM \_ Remove**](abm-remove.md) . L’annulation de l’inscription d’un appbar le supprime de la liste interne des barres du système. Le système n’envoie plus de messages de notification à appbar ou empêche d’autres applications d’utiliser la zone d’écran utilisée par le appbar. Une application doit toujours envoyer **ABM \_ supprimer** avant de détruire un appbar.

### <a name="appbar-size-and-position"></a>Taille et position de appbar

Une application doit définir la taille et la position d’un appbar afin qu’il n’interfère pas avec d’autres barres ou la barre des tâches. Chaque appbar doit être ancré à un bord particulier de l’écran, et plusieurs barres peuvent être ancrés à une arête. Toutefois, si un appbar est ancré sur le même bord que la barre des tâches, le système garantit que la barre des tâches est toujours sur le bord le plus à l’extérieur.

Pour définir la taille et la position d’un appbar, une application propose tout d’abord un bord d’écran et un rectangle englobant pour appbar en envoyant le message [**ABM \_ QUERYPOS**](abm-querypos.md) . Le système détermine si une partie de la zone d’écran dans le rectangle proposé est utilisée par la barre des tâches ou un autre appbar, ajuste le rectangle (si nécessaire) et retourne le rectangle ajusté à l’application.

Ensuite, l’application envoie le message [**ABM \_ SetPos**](abm-setpos.md) pour définir le nouveau rectangle englobant pour le appbar. Là encore, le système peut ajuster le rectangle avant de le renvoyer à l’application. Pour cette raison, l’application doit utiliser le rectangle ajusté retourné par **ABM \_ SetPos** pour définir la taille et la position finales. L’application peut utiliser la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) pour déplacer le appbar dans la position.

En utilisant un processus en deux étapes pour définir la taille et la position, le système permet à l’application de fournir des commentaires intermédiaires à l’utilisateur pendant l’opération de déplacement. Par exemple, si l’utilisateur fait glisser un appbar, l’application peut afficher un rectangle ombré indiquant la nouvelle position avant le déplacement réel du appbar.

Une application doit définir la taille et la position de son appbar après l’avoir inscrit et chaque fois que le appbar reçoit le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) . Un appbar reçoit ce message de notification chaque fois qu’une modification se produit dans la taille, la position ou l’état de visibilité de la barre des tâches et lorsqu’un autre appbar du même côté de l’écran est redimensionné, ajouté ou supprimé.

Chaque fois qu’un appbar reçoit le \_ message WM Activate, il doit envoyer le message d' [**\_ activation ABM**](abm-activate.md) . De même, lorsqu’un appbar reçoit un \_ message WM WINDOWPOSCHANGED, il doit appeler [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md). L’envoi de ces messages permet de s’assurer que le système définit correctement l’ordre de plan des barres de masquage automatique sur le même bord.

### <a name="autohide-application-desktop-toolbars"></a>Masquer automatiquement les barres d’outils du Bureau d’application

Un appbar de masquage automatique est normalement masqué mais devient visible lorsque l’utilisateur déplace le curseur de la souris sur le bord de l’écran auquel le appbar est associé. Le appbar se masque à nouveau lorsque l’utilisateur déplace le curseur de la souris hors du rectangle englobant de la barre.

Bien que le système autorise un certain nombre de barres différents à un moment donné, il n’autorise qu’un seul appbar de masquage automatique à la fois pour chaque bord d’écran, sur la base d’un premier arrivé, premier servi. Le système conserve automatiquement l’ordre de plan d’un appbar de masquage automatique (dans son groupe de l’ordre de plan uniquement).

Une application utilise le message [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) pour inscrire ou annuler l’inscription d’un appbar de masquage automatique. Le message spécifie le bord du appbar et un indicateur qui spécifie si le appbar doit être inscrit ou désinscrit. Le message échoue si un appbar de masquage automatique est en cours d’enregistrement mais qu’un est déjà associé à la périphérie spécifiée. Une application peut récupérer le descripteur du appbar de masquage automatique associé à une arête en envoyant le message [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) .

Un appbar à masquage automatique n’a pas besoin de s’inscrire en tant que appbar normal ; autrement dit, il n’a pas besoin d’être inscrit en envoyant [**le \_ nouveau message ABM**](abm-new.md) . Un appbar qui n’est pas inscrit par **ABM \_ New** recouvre tout barres ancré sur le même bord de l’écran.

### <a name="appbar-notification-messages"></a>Messages de notification appbar

Le système envoie des messages pour notifier un appbar sur les événements qui peuvent affecter sa position et son apparence. Les messages sont envoyés dans le contexte d’un message défini par l’application. L’application spécifie l’identificateur du message lorsqu’il envoie le [**\_ nouveau message ABM**](abm-new.md) pour inscrire le appbar. Le code de notification se trouve dans le paramètre *wParam* du message défini par l’application.

Un appbar reçoit le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) lorsque la taille, la position ou l’état de visibilité de la barre des tâches change, lorsqu’un autre appbar est ajouté au même bord de l’écran ou lorsqu’un autre appbar sur le même bord de l’écran est redimensionné ou supprimé. Un appbar doit répondre à ce message de notification en envoyant des messages [**ABM \_ QUERYPOS**](abm-querypos.md) et [**ABM \_ SetPos**](abm-setpos.md) . Si la position d’un appbar a changé, elle doit appeler la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) pour se déplacer vers la nouvelle position.

Le système envoie le message de notification [**ABN \_ STATECHANGE**](abn-statechange.md) chaque fois que l’état d’affichage automatique ou de masquage automatique de la barre des tâches a changé, c’est-à-dire lorsque l’utilisateur active ou désactive la case à cocher **toujours visible** ou **Masquer automatiquement** dans la feuille de propriétés de la barre des tâches. Un appbar peut utiliser ce message de notification pour définir son état sur conforme à celui de la barre des tâches, si vous le souhaitez.

Lors du démarrage d’une application en plein écran ou de la fermeture de la dernière application en plein écran, un appbar reçoit le message de notification [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) . Le paramètre *lParam* indique si l’application en plein écran est en mode d’ouverture ou de fermeture. S’il s’ouvre, le appbar doit se placer au bas de l’ordre de plan. Le appbar doit restaurer sa position d’ordre de plan lorsque la dernière application en plein écran a été fermée.

Un appbar reçoit le message de notification [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) lorsque l’utilisateur sélectionne la commande cascade, mosaïque horizontale ou Mosaïque verticale à partir du menu contextuel de la barre des tâches. Le système envoie le message deux fois, avant de réorganiser les fenêtres (*lParam* a la **valeur true**) et après avoir organisé les fenêtres (*lParam* a la **valeur false**).

Un appbar peut utiliser des messages [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) pour s’exclure de l’opération en cascade ou en mosaïque. Pour exclure lui-même, appbar doit se masquer quand *lParam* a la **valeur true** et s’afficher lui-même lorsque *lParam* a la **valeur false**. Si un appbar se masque lui-même en réponse à ce message, il n’a pas besoin d’envoyer les messages [**ABM \_ QUERYPOS**](abm-querypos.md) et [**ABM \_ SetPos**](abm-setpos.md) en réponse à l’opération en cascade ou en mosaïque.

## <a name="registering-an-application-desktop-toolbar"></a>Inscription d’une barre d’outils de bureau d’application

Une application doit inscrire un appbar en envoyant le [**\_ nouveau message ABM**](abm-new.md) . L’inscription d’un appbar l’ajoute à la liste interne du système et fournit au système un identificateur de message à utiliser pour envoyer des messages de notification à appbar. Avant de quitter, une application doit annuler l’inscription de la appbar en envoyant le message [**ABM \_ Remove**](abm-remove.md) . L’annulation de l’inscription supprime le appbar de la liste interne du système et empêche la barre de recevoir des messages de notification appbar.

La fonction dans l’exemple suivant enregistre ou annule l’enregistrement d’un appbar, en fonction de la valeur d’un paramètre d’indicateur booléen.


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a>Définition de la taille et de la position appbar

Une application doit définir la taille et la position d’un appbar après avoir inscrit le appbar, une fois que l’utilisateur utilisateur a déplacé ou dimensionné le appbar, et chaque fois que le appbar reçoit le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) . Avant de définir la taille et la position du appbar, l’application interroge le système pour obtenir un rectangle englobant approuvé en envoyant le message [**ABM \_ QUERYPOS**](abm-querypos.md) . Le système retourne un rectangle englobant qui n’interfère pas avec la barre des tâches ou tout autre appbar. Le système ajuste le rectangle simplement par soustraction de rectangle ; il ne fait aucun effort pour conserver la taille initiale du rectangle. Pour cette raison, le appbar doit réajuster le rectangle, si nécessaire, après l’envoi de **ABM \_ QUERYPOS**.

Ensuite, l’application transmet le rectangle englobant au système à l’aide du message [**ABM \_ SetPos**](abm-setpos.md) . Ensuite, il appelle la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) pour déplacer le appbar dans la position.

L’exemple suivant montre comment définir la taille et la position d’un appbar.


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a>Traitement des messages de notification appbar

Un appbar reçoit un message de notification lorsque l’état de la barre des tâches change, lorsqu’une application en plein écran démarre (ou lorsque la dernière se ferme), ou lorsqu’un événement peut affecter la taille et la position du appbar. L’exemple suivant montre comment traiter les différents messages de notification.


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



La fonction suivante ajuste le rectangle englobant d’un appbar, puis appelle la fonction AppBarQuerySetPos définie par l’application (incluse dans la section précédente) pour définir la taille et la position de la barre en conséquence.


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
