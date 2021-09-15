---
description: l’interface Windows comprend une barre d’outils de bureau d’application spéciale appelée barre des tâches. Vous pouvez utiliser la barre des tâches pour effectuer des tâches telles que le basculement entre des fenêtres ouvertes et le démarrage de nouvelles applications.
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: Barre des tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce37991c6265f02ab92ece62dbae341031d272a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522324"
---
# <a name="the-taskbar"></a>Barre des tâches

l’interface Windows comprend une [barre d’outils de bureau d’application](application-desktop-toolbars.md) spéciale appelée *barre des tâches*. Vous pouvez utiliser la barre des tâches pour effectuer des tâches telles que le basculement entre des fenêtres ouvertes et le démarrage de nouvelles applications.

> [!Note]  
> pour plus d’informations sur les modifications apportées à la barre des tâches à partir de Windows 7, consultez Extensions de la [barre des tâches](taskbar-extensions.md).

 

Cette rubrique contient les sections suivantes.

-   [À propos de la barre des tâches](#about-the-taskbar)
    -   [Options d’affichage de la barre des tâches](#taskbar-display-options)
    -   [Ajout de raccourcis au menu Démarrer](#adding-shortcuts-to-the-start-menu)
    -   [Gestion des boutons de la barre des tâches](#managing-taskbar-buttons)
    -   [Ajout, modification et suppression d’icônes dans la zone de notification](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [Notification de création de la barre des tâches](#taskbar-creation-notification)
-   [Utilisation de la barre des tâches](#using-the-taskbar)
    -   [Ajout et suppression d’icônes de la barre des tâches dans la zone de notification](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [Réception d’événements de souris](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>À propos de la barre des tâches

La barre des tâches comprend les éléments suivants :

-   Menu **Démarrer**
-   barre lancement rapide (Windows Vista et versions antérieures uniquement)
-   Boutons de la barre des tâches
-   Barres d’outils (facultatif)
-   Zone Notifications

Le menu **Démarrer** contient des commandes qui peuvent accéder à des programmes, des documents et des paramètres. Ces commandes incluent **l’ensemble des programmes**, des **documents**, **le panneau de configuration**, les **jeux**, **l’aide et le support, l'** arrêt et **la** **recherche de programmes et fichiers**.

le **début** dans les versions antérieures de Windows des éléments contenus tels que la **recherche** et l' **exécution**, qui étaient inclus dans les **programmes et les fichiers de recherche** dans Windows Vista et versions ultérieures.

la barre lancement rapide, disponible dans les versions de Windows antérieures à Windows 7, contient des raccourcis vers les applications. Windows fournit des entrées par défaut, telles que Windows Internet Explorer, et l’utilisateur peut ajouter les autres raccourcis qu’il choisit. Les icônes de cette zone répondent à un simple clic. dans Windows 7 et versions ultérieures, cette fonctionnalité est incluse dans les boutons de la barre des tâches.

L’interpréteur de commandes place un bouton sur la barre des tâches chaque fois qu’une application crée une fenêtre sans propriétaire, autrement dit une fenêtre qui n’a pas de parent et qui possède les bits de style étendu appropriés (consultez [gestion des boutons de la barre des tâches](#managing-taskbar-buttons), ci-dessous). Pour basculer vers une fenêtre, l’utilisateur clique sur son bouton de fenêtre. cette fonctionnalité a été développée à partir de Windows 7. Pour plus d’informations, consultez [extensions de la barre des tâches](taskbar-extensions.md).

Les applications peuvent placer des icônes dans la zone de notification pour indiquer l’état d’une opération ou pour notifier l’utilisateur d’un événement. Par exemple, une application peut placer une icône d’imprimante dans la zone de notification pour montrer qu’un travail d’impression est en cours. toutefois, dans Windows 7 et versions ultérieures, certaines des informations fournies précédemment par la zone de notification doivent être fournies par le biais du bouton de la barre des tâches d’une application. La zone de notification se trouve sur le bord droit de la barre des tâches (si la barre des tâches est horizontale) ou en bas (si la barre des tâches est verticale). Pour plus d’informations, consultez [notifications et la zone de notification](notification-area.md).

La zone de notification affiche également l’heure actuelle si cette option est sélectionnée. L’option se trouve comme suit :

-   **Windows 7 et versions ultérieures**: la liste déroulante **Clock** dans la page **activer ou désactiver les icônes système** de la **zone de notification icône** de l’application panneau de configuration (également accessible via les propriétés de la zone de notification).
-   **Windows Vista**: case à cocher **horloge** dans la page **zone de Notification** de la fenêtre propriétés de la **barre des tâches et du Menu démarrer** .
-   **Windows XP**: la case à cocher **afficher l’horloge** dans la **barre des tâches et** la fenêtre propriétés du Menu démarrer.

L’utilisateur peut cliquer avec le bouton droit sur la barre des tâches pour afficher le menu contextuel. Le menu contextuel comprend des commandes pour les fenêtres en cascade, les fenêtres de pile, les fenêtres afficher côte à côte, afficher le bureau, démarrer le gestionnaire des tâches et définir les propriétés de la barre des tâches. Le menu contextuel offre également la possibilité d’ajouter ou de supprimer un ensemble de barres d’outils à partir de la barre des tâches. Vous pouvez ajouter de nouvelles barres d’outils à ce menu en les inscrivant sous la \_ catégorie DESKBAND CATID. Pour plus d’informations, consultez [Implementing Band Objects](band-objects.md). notez que à partir de Windows 7, la barre des tâches et la zone de notification ont des menus contextuels distincts. Ces menus contextuels partagent des options, telles que la disposition des fenêtres, et en ajouter d’autres.

### <a name="taskbar-display-options"></a>Options d’affichage de la barre des tâches

la barre des tâches prend en charge deux options d’affichage : masquer automatiquement et, dans Windows Vista et les versions antérieures uniquement, Always On haut (la barre des tâches est toujours dans ce mode dans Windows 7 et versions ultérieures). Pour définir ces options, l’utilisateur doit ouvrir le menu contextuel de la barre des tâches, cliquer sur **Propriétés**, activer ou désactiver la case à cocher **Masquer automatiquement la barre des tâches** ou **conserver la barre des tâches au-dessus des autres fenêtres** . Pour récupérer l’état de ces options d’affichage, utilisez le message [**ABM \_ GETSTATE**](abm-getstate.md) . Si vous souhaitez être averti lorsque l’état de ces options d’affichage change, traitez le message de notification [**ABN \_ STATECHANGE**](abn-statechange.md) dans votre procédure de fenêtre. Pour modifier l’état de ces options d’affichage, utilisez le message [**ABM \_ SETSTATE**](abm-setstate.md) .

La *zone de travail* est la partie de l’écran qui n’est pas masquée par la barre des tâches. Pour récupérer la taille de la zone de travail, appelez la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec la valeur **SPI \_ GETWORKAREA** définie. Pour récupérer les coordonnées du rectangle qui décrivent l’emplacement de la barre des tâches, utilisez le message [**ABM \_ GETTASKBARPOS**](abm-gettaskbarpos.md) .

Il est possible de couvrir la barre des tâches en définissant explicitement la taille du rectangle de la fenêtre sur la taille de l’écran avec [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos). pour les systèmes Windows 2000 ou version ultérieure, la fenêtre ne doit pas avoir la valeur [**ws \_ CAPTION**](../winmsg/window-styles.md) ou [**ws \_ THICKFRAME**](../winmsg/window-styles.md), sinon la fenêtre doit être dimensionnée afin que la zone cliente couvre la totalité de l’écran. Plus particulièrement, si la barre des tâches est définie sur Always On Top, elle reste masquée uniquement lorsque l’application est l’application de premier plan.

### <a name="adding-shortcuts-to-the-start-menu"></a>Ajout de raccourcis au menu Démarrer

pour ajouter un élément au sous-menu **programmes** sur Microsoft Windows NT 4,0, Windows 2000 et versions ultérieures, ou Windows 95 ou version ultérieure, procédez comme suit.

1.  Créez un [lien de Shell](./links.md) à l’aide de l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .
2.  Obtenez le PIDL du dossier programmes à l’aide de [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation), en passant les [**\_ programmes CSIDL**](csidl.md).
3.  Ajoutez le lien de l’interpréteur de commandes au dossier programmes. Vous pouvez également créer un dossier dans le dossier programmes et ajouter le lien vers ce dossier.

### <a name="managing-taskbar-buttons"></a>Gestion des boutons de la barre des tâches

L’interpréteur de commandes crée un bouton sur la barre des tâches chaque fois qu’une application crée une fenêtre qui n’est pas propriétaire. Pour vous assurer que le bouton de la fenêtre est placé dans la barre des tâches, créez une fenêtre sans propriétaire avec le style étendu [**WS \_ ex \_ APPWINDOW**](../winmsg/extended-window-styles.md) . Pour empêcher le bouton de la fenêtre d’être placé dans la barre des tâches, créez la fenêtre sans propriétaire avec le style étendu [**WS \_ ex \_ TOOLWINDOW**](../winmsg/extended-window-styles.md) . Vous pouvez également créer une fenêtre masquée et faire de cette fenêtre masquée le propriétaire de votre fenêtre visible.

L’interpréteur de commandes ne supprime le bouton d’une fenêtre de la barre des tâches que si le style de la fenêtre prend en charge les boutons de barre des tâches visibles. Si vous souhaitez modifier dynamiquement le style d’une fenêtre pour qu’il ne prenne pas en charge les boutons visibles de la barre des tâches, vous devez d’abord masquer la fenêtre (en appelant la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) avec l’affichage **logiciel \_ masqué**), modifier le style de la fenêtre, puis afficher la fenêtre.

Le bouton de la fenêtre contient généralement l’icône et le titre de l’application. Toutefois, si l’application ne contient pas de menu système, le bouton de la fenêtre est créé sans l’icône.

Si vous souhaitez que votre application attire l’attention de l’utilisateur lorsque la fenêtre n’est pas active, utilisez la fonction [**flashwindow**](/windows/win32/api/winuser/nf-winuser-flashwindow) pour informer l’utilisateur qu’un message est en attente. Cette fonction clignote le bouton de la fenêtre. Une fois que l’utilisateur a cliqué sur le bouton de la fenêtre pour activer la fenêtre, votre application peut afficher le message.

### <a name="modifying-the-contents-of-the-taskbar"></a>Modification du contenu de la barre des tâches

La [Version 4,71 et les versions ultérieures](versions.md) de Shell32.dll ajoutent la possibilité de modifier le contenu de la barre des tâches. À partir d’une application, vous pouvez maintenant ajouter, supprimer et activer des boutons de la barre des tâches. L’activation de l’élément n’active pas la fenêtre ; il affiche l’élément tel qu’il est appuyé sur la barre des tâches.

Les fonctionnalités de modification de la barre des tâches sont implémentées dans un objet COM (Component Object Model) (CLSID \_ TaskbarList) qui expose l’interface [**ITASKBARLIST**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) (IID \_ ITaskbarList). Vous devez appeler la méthode [**ITaskbarList :: HrInit**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) pour initialiser l’objet. Vous pouvez ensuite utiliser les méthodes de l’interface [**ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) pour modifier le contenu de la barre des tâches.

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>Ajout, modification et suppression d’icônes dans la zone de notification

Utilisez la [**fonction \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes pour ajouter, modifier ou supprimer des icônes dans la zone de notification. Le paramètre *dwMessage* de l' **interface \_ NotifyIcon de l’interpréteur** de commandes est un message de la barre des tâches qui spécifie l’action à entreprendre. Le paramètre *pnid* est un pointeur vers une structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) qui permet d’identifier l’icône et de transmettre toutes les informations supplémentaires nécessaires au système pour traiter le message.

Vous pouvez effectuer les actions suivantes avec les icônes de la zone de notification.

-   Pour ajouter une icône à la zone de notification de la barre des tâches, appelez l' [**interface \_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) avec le paramètre *dwMessage* défini sur NIM \_ Add. La structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) est utilisée pour spécifier le handle et l’identificateur de l’icône, ainsi que tout texte info-bulle. Si l’utilisateur a activé la case à cocher **afficher l’horloge** dans les propriétés de la barre des tâches, le système place l’icône à gauche de l’horloge. Dans le cas contraire, l’icône apparaît sur le côté droit ou en bas de la barre des tâches. Toutes les icônes existantes sont décalées vers la gauche pour faire de la place pour la nouvelle icône.
-   Pour modifier les informations d’une icône, y compris son handle d’icône, le texte d’info-bulle et l’identificateur du message de rappel, appelez la fonction [**\_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes avec *dwMessage* défini sur NIM \_ modifier.
-   Pour supprimer une icône de la zone de notification, appelez la fonction NotifyIcon de l' [**interpréteur \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes avec le paramètre *dwMessage* défini sur NIM \_ Delete.

Lorsque vous avez terminé une opération d’interface utilisateur, retournez le focus à la zone de notification en appelant [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) avec *dwMessage* défini sur NIM \_ SetFocus. Par exemple, vous pouvez le faire quand une icône de la barre des tâches affiche un menu contextuel, mais que l’utilisateur l’annule en appuyant sur la touche ÉCHAP.

### <a name="receiving-notification-area-callback-messages"></a>Réception des messages de rappel de la zone de notification

Les applications placent généralement des icônes dans la zone de notification de la barre des tâches pour servir d’indicateurs d’État. Vous pouvez fournir des informations supplémentaires lorsque l’utilisateur effectue des actions de la souris, par exemple en déplaçant le pointeur de la souris sur l’icône ou en cliquant sur l’icône.

Le système vous avertit des événements de souris et de clavier en envoyant un message de rappel défini par l’application qui est associé à une icône particulière. De cette façon, le système peut notifier une application lorsque l’utilisateur, par exemple, clique sur l’icône ou la sélectionne en appuyant sur une touche.

Vous définissez le message de rappel d’une icône lorsque vous ajoutez l’icône à la barre des tâches. L’identificateur du message de rappel est spécifié dans le membre **uCallbackMessage** de la structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) passée avec NIM \_ Add. Lorsqu’un événement se produit, le système envoie le message de rappel à la procédure de fenêtre de la fenêtre spécifiée par le membre **HWND** . Le paramètre *wParam* du message contient l’identificateur de l’icône de la barre des tâches dans laquelle l’événement s’est produit. Le paramètre *lParam* contient le message de souris ou de clavier associé à l’événement. Par exemple, lorsque le pointeur de la souris se déplace sur une icône de barre des tâches, *lParam* contient [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md).

Les résultats de divers événements de souris peuvent être résumés comme suit :

-   Lorsque l’utilisateur déplace le pointeur de la souris sur l’icône, le système affiche le texte d’info-bulle qui a été spécifié dans [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa).
-   Quand l’utilisateur clique sur l’icône, votre application reçoit une notification [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) .
-   Quand l’utilisateur clique avec le bouton droit sur l’icône, votre application reçoit une notification [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) .
-   Lorsque l’utilisateur double-clique sur l’icône, votre application reçoit une notification [**WM \_ LBUTTONDBLCLK**](../inputdev/wm-lbuttondblclk.md) .

En règle générale, si vous cliquez sur l’icône, l’application affiche une fenêtre contenant des informations supplémentaires, clique avec le bouton droit sur affiche un menu contextuel, puis double-clique sur exécute la commande de menu contextuel par défaut.

Pour obtenir un exemple de modification du texte info-bulle associé à une icône de zone de notification, consultez [info-bulles Info-bulles pour les icônes de barre d’État](../controls/tooltip-controls.md).

les versions 5,0 et ultérieures du shell gèrent les événements de souris et de clavier de l' [**interpréteur \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes de l’interpréteur de commandes de la même façon que les versions antérieures du shell détectées sur Windows NT 4,0, Windows 95 et Windows 98. Les différences sont les suivantes :

-   Si un utilisateur demande le menu contextuel d’une icône de notification avec le clavier, la version 5,0 Shell envoie l’application associée à un message [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) . Les versions antérieures envoient les messages [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) et [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Si un utilisateur sélectionne une icône de notification avec le clavier et l’active avec la barre d’espace ou la touche entrée, le shell version 5,0 envoie à l’application associée une notification **nDans \_ keyselect** . Les versions antérieures envoient les messages [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) et [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Si un utilisateur sélectionne une icône Notify avec la souris et l’active avec la touche entrée, le shell version 5,0 envoie à l’application associée une **notification \_ Select nDans** . Les versions antérieures envoient les messages [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) et [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   si un utilisateur passe le pointeur de la souris sur une icône à laquelle une info-bulle est associée, la version 6,0 Shell (Windows XP) envoie les messages suivants.
    -   -   **NDans \_ BALLOONSHOW** : envoyé lorsque la bulle est affichée (les bulles sont mises en file d’attente).
        -   **NDans \_ BALLOONHIDE** : envoyé lorsque l’info-bulle disparaît, par exemple lorsque l’icône est supprimée. Ce message n’est pas envoyé si la bulle est fermée en raison d’un délai d’attente ou d’un clic de souris.
        -   **NDans \_ BALLOONTIMEOUT** : envoyé lorsque l’info-bulle est fermée en raison d’un dépassement de délai.
        -   **NDans \_ BALLOONUSERCLICK** : envoyé lorsque l’info-bulle est fermée en raison d’un clic de souris.

Vous pouvez sélectionner la façon dont l’interpréteur de commandes doit se comporter en appelant [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) avec *dwMessage* défini sur **NIM \_ SETVERSION**. Définissez le membre **uVersion** de la structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) pour indiquer si vous souhaitez une version 5,0 ou une version antérieure de 5,0.

### <a name="taskbar-creation-notification"></a>Notification de création de la barre des tâches

Avec Microsoft Internet Explorer 4,0 et versions ultérieures, l’interpréteur de commandes avertit les applications que la barre des tâches a été créée. Lorsque la barre des tâches est créée, elle enregistre un message avec la chaîne TaskbarCreated, puis diffuse ce message à toutes les fenêtres de niveau supérieur. Lorsque votre application de barre des tâches reçoit ce message, elle doit supposer que toutes les icônes de la barre des tâches qu’elle a ajoutées ont été supprimées et les rajouter. Cette fonctionnalité s’applique généralement uniquement aux services qui sont déjà en cours d’exécution au lancement de l’interpréteur de commandes. L’exemple suivant montre une méthode très simplifiée pour gérer ce cas.

sur Windows 10, la barre des tâches diffuse également ce message lorsque la résolution de l’affichage principal change.

```
LRESULT CALLBACK WndProc(HWND hWnd, 
                         UINT uMessage, 
                         WPARAM wParam, 
                         LPARAM lParam)
{
    static UINT s_uTaskbarRestart;

    switch(uMessage)
    {
        case WM_CREATE:
            s_uTaskbarRestart = RegisterWindowMessage(TEXT("TaskbarCreated"));
            break;
        
        default:
            if(uMessage == s_uTaskbarRestart)
                AddTaskbarIcons();
            break;
    }

    return DefWindowProc(hWnd, uMessage, wParam, lParam);
}
```



## <a name="using-the-taskbar"></a>Utilisation de la barre des tâches

Cette section contient des exemples qui montrent comment ajouter des icônes à la zone de notification de la barre des tâches et comment traiter les messages de rappel pour les icônes de la barre des tâches.

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>Ajout et suppression d’icônes de la barre des tâches dans la zone de notification

Vous ajoutez une icône à la zone de notification de la barre des tâches en remplissant une structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) , puis en passant la structure à l' [**interface \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes avec *dwMessage* défini sur **NIM \_ Add**. Les membres de structure doivent spécifier le handle de la fenêtre qui ajoute l’icône, ainsi que l’identificateur d’icône et le handle d’icône. Vous pouvez également spécifier le texte info-bulle pour l’icône. Si vous avez besoin de recevoir des messages de souris pour l’icône, spécifiez l’identificateur du message de rappel que le système doit utiliser pour envoyer le message à la procédure de fenêtre.

La fonction de l’exemple suivant montre comment ajouter une icône à la barre des tâches.


```
// MyTaskBarAddIcon - adds an icon to the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window to receive callback messages 
// uID - identifier of the icon 
// hicon - handle to the icon to add 
// lpszTip - tooltip text 

BOOL MyTaskBarAddIcon(HWND hwnd, UINT uID, HICON hicon, LPSTR lpszTip) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
    tnid.uFlags = NIF_MESSAGE | NIF_ICON | NIF_TIP; 
    tnid.uCallbackMessage = MYWM_NOTIFYICON; 
    tnid.hIcon = hicon; 
    if (lpszTip) 
        hr = StringCbCopyN(tnid.szTip, sizeof(tnid.szTip), lpszTip, 
                           sizeof(tnid.szTip));
        // TODO: Add error handling for the HRESULT.
    else 
        tnid.szTip[0] = (TCHAR)'\0'; 
 
    res = Shell_NotifyIcon(NIM_ADD, &tnid); 
 
    if (hicon) 
        DestroyIcon(hicon); 
 
    return res; 
}
```



Pour supprimer une icône de la zone de notification de la barre des tâches, remplissez une structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) et appelez l' [**interface \_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) avec *dwMessage* défini sur **NIM \_ Delete**. Lorsque vous supprimez une icône de barre des tâches, spécifiez uniquement les membres **cbSize**, **HWND** et **uID** de la structure. Par exemple :


```
// MyTaskBarDeleteIcon - deletes an icon from the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window that added the icon. 
// uID - identifier of the icon to delete. 

BOOL MyTaskBarDeleteIcon(HWND hwnd, UINT uID) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
         
    res = Shell_NotifyIcon(NIM_DELETE, &tnid); 
    return res; 
}
```



### <a name="receiving-mouse-events"></a>Réception d’événements de souris

Si vous spécifiez un message de rappel pour une icône de barre des tâches, le système envoie le message à votre application chaque fois qu’un événement de souris se produit dans le rectangle englobant de l’icône. Le paramètre *wParam* du message spécifie l’identificateur de l’icône de la barre des tâches, et le paramètre *lParam* du message spécifie le message généré par le système à la suite de l’événement de souris.

La fonction de l’exemple suivant provient d’une application qui ajoute les icônes de batterie et d’imprimante à la barre des tâches. L’application appelle la fonction lorsqu’elle reçoit un message de rappel. La fonction détermine si l’utilisateur a cliqué sur l’une des icônes et, si un clic s’est produit, appelle une fonction définie par l’application pour afficher les informations d’État.


```
// On_MYWM_NOTIFYICON - processes callback messages for taskbar icons. 
// wParam - first message parameter of the callback message. 
// lParam - second message parameter of the callback message. 

void On_MYWM_NOTIFYICON(WPARAM wParam, LPARAM lParam) 
{ 
    UINT uID; 
    UINT uMouseMsg; 
 
    uID = (UINT) wParam; 
    uMouseMsg = (UINT) lParam; 
 
    if (uMouseMsg == WM_LBUTTONDOWN) 
    { 
        switch (uID) 
        { 
            case IDI_MYBATTERYICON: 
 
                // The user clicked the battery icon. Display the 
                // battery status. 
                ShowBatteryStatus(); 
                break; 
 
            case IDI_MYPRINTERICON: 
 
                // The user clicked the printer icon. Display the 
                // status of the print job. 
                ShowJobStatus(); 
                break; 
 
            default: 
                break; 
        } 
     } 

     return; 
 }
```



 

 
