---
title: Utilisation des menus
description: Cette section fournit des exemples de code pour les tâches relatives aux menus.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- ressources, menus
- menus, création
- ressources de modèle de menu
- ressources, modèle de menu
- menu étendu-format de modèle
- ancien format de modèle de menu
- chargement des ressources de modèle de menu
- menus, classe
- menus, raccourci
- création de menus
- menus de la classe
- menus contextuels
- bitmaps d’élément de menu
- menus, owner-drawn
- menus owner-drawn
- bitmaps de coches personnalisées
- menus, cases à cocher
- menus, polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3a71a580a323fa2058613f8c9a14d9c2782bd3ba139e5d182750e5047fe74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971928"
---
# <a name="using-menus"></a>Utilisation des menus

Cette section décrit les tâches suivantes :

-   [Utilisation d’une ressource Menu-Template](#using-a-menu-template-resource)
    -   [Format de Menu-Template étendu](#extended-menu-template-format)
    -   [Ancien format de Menu-Template](#old-menu-template-format)
    -   [Chargement d’une ressource Menu-Template](#loading-a-menu-template-resource)
    -   [Création d’un menu classe](#creating-a-class-menu)
-   [Création d’un menu contextuel](#creating-a-shortcut-menu)
    -   [Traitement du \_ message WM CONTEXTMENU](/windows)
    -   [Création d’un menu contextuel Font-Attributes](#creating-a-shortcut-font-attributes-menu)
    -   [Affichage d’un menu contextuel](#displaying-a-shortcut-menu)
-   [Utilisation de Menu-Item bitmaps](#using-menu-item-bitmaps)
    -   [Définition de l’indicateur de type bitmap](#setting-the-bitmap-type-flag)
    -   [Création de l’image bitmap](#creating-the-bitmap)
    -   [Ajout de lignes et de graphiques à un menu](#adding-lines-and-graphs-to-a-menu)
    -   [Exemple de bitmaps Menu-Item](#example-of-menu-item-bitmaps)
-   [Créer des éléments de menu Owner-Drawn](#creating-owner-drawn-menu-items)
    -   [Définition de l’indicateur Owner-Drawn](#setting-the-owner-drawn-flag)
    -   [Menus owner-drawn et le \_ message WM MEASUREITEM](/windows)
    -   [Menus owner-drawn et le \_ message WM DRAWITEM](/windows)
    -   [Menus owner-drawn et le \_ message WM MENUCHAR](/windows)
    -   [Définition des polices pour les chaînes de texte Menu-Item](#setting-fonts-for-menu-item-text-strings)
    -   [Exemple d’éléments de menu Owner-Drawn](#example-of-owner-drawn-menu-items)
-   [Utilisation de bitmaps de coche personnalisées](#using-custom-check-mark-bitmaps)
    -   [Création de bitmaps de coche personnalisées](#creating-custom-check-mark-bitmaps)
    -   [Association de bitmaps à un élément de menu](#associating-bitmaps-with-a-menu-item)
    -   [Définition de l’attribut coche](#setting-the-check-mark-attribute)
    -   [Simulation de cases à cocher dans un menu](#simulating-check-boxes-in-a-menu)
    -   [Exemple d’utilisation de bitmaps de coche personnalisées](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a>Utilisation d’une ressource Menu-Template

Vous incluez généralement un menu dans une application en créant une ressource de modèle de menu, puis en chargeant le menu au moment de l’exécution. Cette section décrit le format d’un modèle de menu et explique comment charger une ressource de modèle de menu et l’utiliser dans votre application. Pour plus d’informations sur la création d’une ressource de modèle de menu, consultez la documentation fournie avec vos outils de développement.

-   [Format de Menu-Template étendu](#extended-menu-template-format)
-   [Ancien format de Menu-Template](#old-menu-template-format)
-   [Chargement d’une ressource Menu-Template](#loading-a-menu-template-resource)
-   [Création d’un menu classe](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a>Format de Menu-Template étendu

Le format de modèle de menu étendu prend en charge des fonctionnalités de menu supplémentaires. Comme les ressources de modèle de menu standard, les ressources de modèle de menu étendues ont le type de ressource de **\_ menu RT** . Le système distingue les deux formats de ressources par le numéro de version, qui est le premier membre de l’en-tête de ressource.

Un modèle de menu étendu se compose d’une structure d' [**\_ \_ en-tête de modèle menuex**](menuex-template-header.md) , suivie d’un plus grand nombre de structures de définition d’élément de [**\_ modèle \_ menuex**](menuex-template-item.md) .

### <a name="old-menu-template-format"></a>Ancien format de Menu-Template

Un ancien modèle de menu (Microsoft Windows NT 3,51 et versions antérieures) définit un menu, mais ne prend pas en charge les nouvelles fonctionnalités de menu. Une ancienne ressource de modèle de menu a le type de ressource de **\_ menu RT** .

Un ancien modèle de menu se compose d’une structure [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) suivie d’une ou de plusieurs structures [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .

### <a name="loading-a-menu-template-resource"></a>Chargement d’une ressource Menu-Template

Pour charger une ressource de modèle de menu, utilisez la fonction [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , en spécifiant un handle pour le module qui contient la ressource et l’identificateur du modèle de menu. La fonction **LoadMenu** retourne un handle de menu que vous pouvez utiliser pour assigner le menu à une fenêtre. Cette fenêtre devient la fenêtre propriétaire du menu, qui reçoit tous les messages générés par le menu.

Pour créer un menu à partir d’un modèle de menu qui est déjà en mémoire, utilisez la fonction [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) . Cela est utile si votre application génère des modèles de menu de manière dynamique.

Pour assigner un menu à une fenêtre, utilisez la fonction [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) ou spécifiez le handle du menu dans le paramètre *HMENU* de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) lors de la création d’une fenêtre. Vous pouvez également assigner un menu à une fenêtre en spécifiant un modèle de menu lorsque vous inscrivez une classe de fenêtre. le modèle identifie le menu spécifié comme le menu classe pour cette classe de fenêtre.

Pour que le système affecte automatiquement un menu spécifique à une fenêtre, spécifiez le modèle du menu lorsque vous inscrivez la classe de la fenêtre. Le modèle identifie le menu spécifié comme le menu classe pour cette classe de fenêtre. Ensuite, lorsque vous créez une fenêtre de la classe spécifiée, le système affecte automatiquement le menu spécifié à la fenêtre.

Vous ne pouvez pas assigner un menu à une fenêtre qui est une fenêtre enfant.

Pour créer un menu de classe, incluez l’identificateur de la ressource de modèle de menu en tant que membre **lpszMenuName** d’une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , puis transmettez un pointeur vers la structure à la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .

### <a name="creating-a-class-menu"></a>Création d’un menu classe

L’exemple suivant montre comment créer un menu de classe pour une application, créer une fenêtre qui utilise le menu classe et traiter les commandes de menu dans la procédure de fenêtre.

Voici la partie pertinente du fichier d’en-tête de l’application :


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



Voici les parties pertinentes de l’application elle-même :


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a>Création d’un menu contextuel

Pour utiliser un menu contextuel dans une application, transmettez son handle à la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Une application appelle généralement **TrackPopupMenuEx** dans une procédure de fenêtre en réponse à un message généré par l’utilisateur, tel que [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) ou WM keyoff. [**\_**](/windows/desktop/inputdev/wm-keydown)

En plus du handle de menu contextuel, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) nécessite que vous spécifiiez un handle vers la fenêtre propriétaire, la position du menu contextuel (en coordonnées d’écran) et le bouton de la souris que l’utilisateur peut utiliser pour choisir un élément.

L’ancienne fonction [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) est toujours prise en charge, mais les nouvelles applications doivent utiliser la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . La fonction **TrackPopupMenuEx** requiert les mêmes paramètres que **TrackPopupMenu**, mais elle vous permet également de spécifier une partie de l’écran que le menu ne doit pas masquer. Une application appelle généralement ces fonctions dans une procédure de fenêtre lors du traitement du message [**WM \_ CONTEXTMENU**](wm-contextmenu.md) .

Vous pouvez spécifier la position d’un menu contextuel en fournissant des coordonnées x et y, ainsi que l’indicateur **TPM \_ CENTERALIGN**, **TPM \_ LEFTALIGN** ou **TPM \_ RIGHTALIGN** . L’indicateur spécifie la position du menu contextuel par rapport aux coordonnées x et y.

Vous devez autoriser l’utilisateur à choisir un élément dans un menu contextuel en utilisant le même bouton de souris que celui utilisé pour afficher le menu. Pour ce faire, spécifiez l’indicateur **TPM \_ LEFTBUTTON** ou **TPM \_ RIGHTBUTTON** pour indiquer le bouton de la souris que l’utilisateur peut utiliser pour choisir un élément de menu.

-   [Traitement du \_ message WM CONTEXTMENU](/windows)
-   [Création d’un menu contextuel Font-Attributes](#creating-a-shortcut-font-attributes-menu)
-   [Affichage d’un menu contextuel](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a>Traitement du \_ message WM CONTEXTMENU

Le [**message \_ WM CONTEXTMENU**](wm-contextmenu.md) est généré quand une procédure de fenêtre d’application transmet le message [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . L’application peut traiter ce message pour afficher un menu contextuel adapté à une partie spécifique de l’écran. Si l’application n’affiche pas de menu contextuel, elle doit transmettre le message à **DefWindowProc** pour la gestion par défaut.

Voici un exemple de traitement des messages [**WM \_ CONTEXTMENU**](wm-contextmenu.md) , tel qu’il peut apparaître dans la procédure de fenêtre d’une application. Les mots de poids fort et de poids fort du paramètre *lParam* spécifient les coordonnées d’écran de la souris lorsque le bouton droit de la souris est relâché (Notez que ces coordonnées peuvent prendre des valeurs négatives sur les systèmes avec plusieurs moniteurs). La fonction **OnContextMenu** définie par l’application retourne la **valeur true** si elle affiche un menu contextuel, ou **false** dans le cas contraire.


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



La fonction OnContextMenu définie par l’application suivante affiche un menu contextuel si la position spécifiée de la souris se trouve dans la zone cliente de la fenêtre. Une fonction plus sophistiquée peut afficher l’un des différents menus, en fonction de la partie de la zone cliente spécifiée. Pour afficher réellement le menu contextuel, cet exemple appelle une fonction définie par l’application appelée DisplayContextMenu. Pour obtenir une description de cette fonction, consultez [affichage d’un menu contextuel](#displaying-a-shortcut-menu).


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a>Création d’un menu contextuel Font-Attributes

L’exemple de cette section contient des portions de code d’une application qui crée et affiche un menu contextuel qui permet à l’utilisateur de définir des polices et des attributs de police. L’application affiche le menu dans la zone cliente de sa fenêtre principale chaque fois que l’utilisateur clique avec le bouton gauche de la souris.

Voici le modèle de menu du menu contextuel fourni dans le fichier de définition de ressources de l’application.


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



L’exemple suivant donne la procédure de fenêtre et les fonctions de prise en charge utilisées pour créer et afficher le menu contextuel.


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a>Affichage d’un menu contextuel

La fonction illustrée dans l’exemple suivant affiche un menu contextuel.

L’application comprend une ressource de menu identifiée par la chaîne « ShortcutExample ». La barre de menus contient simplement un nom de menu. L’application utilise la fonction [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) pour afficher le menu associé à cet élément de menu. (La barre de menus elle-même n’est pas affichée, car **TrackPopupMenu** requiert un handle vers un menu, un sous-menu ou un menu contextuel.)


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a>Utilisation de Menu-Item bitmaps

Le système peut utiliser une bitmap au lieu d’une chaîne de texte pour afficher un élément de menu. Pour utiliser une image bitmap, vous devez définir l’indicateur de **\_ bitmap miim** pour l’élément de menu et spécifier un handle vers le bitmap que le système doit afficher pour l’élément de menu dans le membre **HbmpItem** de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Cette section décrit comment utiliser des bitmaps pour les éléments de menu.

-   [Définition de l’indicateur de type bitmap](#setting-the-bitmap-type-flag)
-   [Création de l’image bitmap](#creating-the-bitmap)
-   [Ajout de lignes et de graphiques à un menu](#adding-lines-and-graphs-to-a-menu)
-   [Exemple de bitmaps Menu-Item](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a>Définition de l’indicateur de type bitmap

La **\_ bitmap miim** ou l’indicateur de **\_ bitmap MF** indique au système d’utiliser une image bitmap plutôt qu’une chaîne de texte pour afficher un élément de menu. La **\_ bitmap miim** d’un élément de menu ou l’indicateur **\_ bitmap MF** doit être défini au moment de l’exécution ; vous ne pouvez pas le définir dans le fichier de définition de ressource.

Pour les nouvelles applications, vous pouvez utiliser la fonction [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) ou [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) pour définir l’indicateur de type de **\_ bitmap miim** . Pour modifier un élément de menu d’un élément de texte en élément bitmap, utilisez **SetMenuItemInfo**. Pour ajouter un nouvel élément bitmap à un menu, utilisez la fonction **InsertMenuItem** .

Les applications écrites pour des versions antérieures du système peuvent continuer à utiliser les fonctions [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) pour définir l’indicateur de **\_ bitmap MF** . Pour modifier un élément de menu d’un élément de chaîne de texte en élément bitmap, utilisez **ModifyMenu**. Pour ajouter un nouvel élément bitmap à un menu, utilisez l’indicateur de **\_ bitmap MF** avec la fonction **InsertMenu** ou **AppendMenu** .

### <a name="creating-the-bitmap"></a>Création de l’image bitmap

Lorsque vous définissez l’indicateur de type bitmap **miim \_** ou **MF \_** pour un élément de menu, vous devez également spécifier un handle vers le bitmap que le système doit afficher pour l’élément de menu. Vous pouvez fournir la bitmap en tant que ressource bitmap ou créer l’image bitmap au moment de l’exécution. Si vous utilisez une ressource bitmap, vous pouvez utiliser la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) pour charger la bitmap et obtenir son handle.

pour créer l’image bitmap au moment de l’exécution, utilisez les fonctions Windows Graphics Device Interface (GDI). GDI offre plusieurs moyens de créer une bitmap au moment de l’exécution, mais les développeurs utilisent généralement la méthode suivante :

1.  Utilisez la fonction [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) pour créer un contexte de périphérique compatible avec le contexte de périphérique utilisé par la fenêtre principale de l’application.
2.  Utilisez la fonction [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) pour créer une bitmap compatible avec la fenêtre principale de l’application ou utilisez la fonction [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) pour créer une image bitmap monochrome.
3.  Utilisez la fonction [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) pour sélectionner la bitmap dans le contexte de périphérique compatible.
4.  Utilisez les fonctions de dessin GDI, telles que [**ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) et [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), pour dessiner une image dans le bitmap.

Pour plus d’informations, consultez [bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="adding-lines-and-graphs-to-a-menu"></a>Ajout de lignes et de graphiques à un menu

L’exemple de code suivant montre comment créer un menu qui contient des bitmaps d’élément de menu. Il crée deux menus. Le premier est un menu de graphique qui contient trois bitmaps d’élément de menu : un graphique à secteurs, un graphique en courbes et un graphique à barres. L’exemple montre comment charger ces bitmaps à partir du fichier de ressources de l’application, puis utiliser les fonctions [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) et [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) pour créer les éléments de menu et de menu.

Le deuxième menu est un menu lignes. Elle contient des bitmaps qui indiquent les styles de ligne fournis par le stylet prédéfini dans le système. Les bitmaps de style ligne sont créées au moment de l’exécution à l’aide des fonctions GDI.

Voici les définitions des ressources bitmap dans le fichier de définition de ressources de l’application.


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



Voici les parties pertinentes du fichier d’en-tête de l’application.


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



L’exemple suivant montre comment les menus et les bitmaps d’élément de menu sont créés dans une application.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a>Exemple de bitmaps Menu-Item

L’exemple de cette rubrique crée deux menus, chacun contenant plusieurs éléments de menu bitmap. Pour chaque menu, l’application ajoute un nom de menu correspondant à la barre de menus de la fenêtre principale.

Le premier menu contient des éléments de menu présentant chacun des trois types de graphiques suivants : secteurs, courbes et barres. Les bitmaps de ces éléments de menu sont définis en tant que ressources et sont chargés à l’aide de la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) . Le nom du menu « graphique » est associé à ce menu dans la barre de menus.

Le deuxième menu contient des éléments de menu présentant chacun des cinq styles de ligne utilisés avec la fonction [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) : **PS \_ Solid**, **PS \_ Dash**, **PS \_ dot**, **PS \_ tiret point** et **PS \_ tiret point point**. L’application crée les bitmaps pour ces éléments de menu au moment de l’exécution à l’aide des fonctions de dessin GDI. Le nom du menu **lignes** de la barre de menus est associé à ce menu.

Défini dans la procédure de fenêtre de l’application se trouvent deux tableaux statiques de handles de bitmap. Un tableau contient les descripteurs des trois bitmaps utilisés pour le menu **graphique** . L’autre contient les descripteurs des cinq bitmaps utilisés pour le menu **lignes** . Lors du traitement du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , la procédure de fenêtre charge les bitmaps de graphique, crée les bitmaps de ligne, puis ajoute les éléments de menu correspondants. Lors du traitement du message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , la procédure de fenêtre supprime toutes les bitmaps.

Voici les parties pertinentes du fichier d’en-tête de l’application.


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



Voici les parties pertinentes de la procédure de fenêtre. La procédure de fenêtre exécute la majeure partie de son initialisation en appelant les fonctions LoadChartBitmaps, CreateLineBitmaps et AddBitmapMenu définies par l’application, décrites plus loin dans cette rubrique.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



La fonction LoadChartBitmaps définie par l’application charge les ressources bitmap pour le menu graphique en appelant la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , comme suit.


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



La fonction CreateLineBitmaps définie par l’application crée les bitmaps pour le menu lignes à l’aide des fonctions de dessin GDI. La fonction crée un contexte de périphérique (DC) de mémoire avec les mêmes propriétés que le DC de la fenêtre du bureau. Pour chaque style de ligne, la fonction crée une image bitmap, la sélectionne dans le DC de mémoire et la dessine.


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



La fonction AddBitmapMenu définie par l’application crée un menu et lui ajoute le nombre spécifié d’éléments de menu bitmap. Ensuite, il ajoute un nom de menu correspondant à la barre de menus de la fenêtre spécifiée.


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a>Créer des éléments de menu Owner-Drawn

Si vous avez besoin d’un contrôle total sur l’apparence d’un élément de menu, vous pouvez utiliser un élément de menu owner-drawn dans votre application. Cette section décrit les étapes nécessaires à la création et à l’utilisation d’un élément de menu owner-drawn.

-   [Définition de l’indicateur Owner-Drawn](#setting-the-owner-drawn-flag)
-   [Menus owner-drawn et le \_ message WM MEASUREITEM](/windows)
-   [Menus owner-drawn et le \_ message WM DRAWITEM](/windows)
-   [Menus owner-drawn et le \_ message WM MENUCHAR](/windows)
-   [Définition des polices pour les chaînes de texte Menu-Item](#setting-fonts-for-menu-item-text-strings)
-   [Exemple d’éléments de menu Owner-Drawn](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a>Définition de l’indicateur Owner-Drawn

Vous ne pouvez pas définir un élément de menu owner-drawn dans le fichier de définition de ressource de votre application. Au lieu de cela, vous devez créer un nouvel élément de menu ou en modifier un à l’aide de l’indicateur de menu de la **MFT \_** .

Vous pouvez utiliser la fonction [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) ou [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) pour spécifier un élément de menu owner-drawn. Utilisez **InsertMenuItem** pour insérer un nouvel élément de menu à la position spécifiée dans une barre de menus ou un menu. Utilisez **SetMenuItemInfo** pour modifier le contenu d’un menu.

Lors de l’appel de ces deux fonctions, vous devez spécifier un pointeur vers une structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , qui spécifie les propriétés du nouvel élément de menu ou les propriétés que vous souhaitez modifier pour un élément de menu existant. Pour transformer un élément en élément owner-drawn, spécifiez la valeur **\_ ftype miim** pour le membre **fmask** et la valeur de la **table MFT \_** dans le membre **ftype** .

En définissant les membres appropriés de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , vous pouvez associer une valeur définie par l’application, appelée **données d’élément**, à chaque élément de menu. Pour ce faire, spécifiez la valeur de **\_ données miim** pour le membre **fmask** et la valeur définie par l’application pour le membre **dwItemData** .

Vous pouvez utiliser des données d’élément avec n’importe quel type d’élément de menu, mais cela est particulièrement utile pour les éléments owner-drawn. Supposons, par exemple, qu’une structure contient des informations utilisées pour dessiner un élément de menu. Une application peut utiliser les données d’élément pour un élément de menu pour stocker un pointeur vers la structure. Les données de l’élément sont envoyées à la fenêtre propriétaire du menu avec les messages [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) et [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) . Pour récupérer les données d’un menu à tout moment, utilisez la fonction [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Les applications écrites pour des versions antérieures du système peuvent continuer à appeler [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) pour assigner l’indicateur de **\_ OwnerDraw OwnerDraw** à un élément de menu owner-drawn.

Lorsque vous appelez l’une de ces trois fonctions, vous pouvez passer une valeur en tant que paramètre *lpNewItem* . Cette valeur peut représenter toutes les informations significatives pour votre application et qui seront disponibles pour votre application lorsque l’élément sera affiché. Par exemple, la valeur peut contenir un pointeur vers une structure ; la structure peut, à son tour, contenir une chaîne de texte et un handle vers la police logique que votre application utilisera pour dessiner la chaîne.

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a>Owner-Drawn les menus et le \_ message WM MEASUREITEM

Avant que le système n’affiche un élément de menu owner-drawn pour la première fois, il envoie le message [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) à la procédure de fenêtre de la fenêtre qui possède le menu de l’élément. Ce message contient un pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui identifie l’élément et contient les données d’élément qu’une application peut avoir affectées. La procédure de fenêtre doit remplir les membres **itemWidth** et **ItemHeight** de la structure avant de retourner du traitement du message. Le système utilise les informations contenues dans ces membres lors de la création du rectangle englobant dans lequel une application dessine l’élément de menu. Il utilise également les informations pour détecter quand l’utilisateur choisit l’élément.

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a>Owner-Drawn les menus et le \_ message WM DRAWITEM

Chaque fois que l’élément doit être dessiné (par exemple, lorsqu’il est affiché pour la première fois ou lorsque l’utilisateur le sélectionne), le système envoie le message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) à la procédure de fenêtre de la fenêtre propriétaire du menu. Ce message contient un pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , qui contient des informations sur l’élément, y compris les données d’élément qu’une application peut avoir affectées. En outre, **drawitemstruct,** contient des indicateurs qui indiquent l’état de l’élément (par exemple s’il est grisé ou sélectionné), ainsi qu’un rectangle englobant et un contexte de périphérique que l’application utilise pour dessiner l’élément.

Une application doit effectuer les opérations suivantes lors du traitement du message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) :

-   Déterminez le type de dessin nécessaire. Pour ce faire, vérifiez le membre **itemAction** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .
-   Dessinez l’élément de menu de manière appropriée, à l’aide du rectangle englobant et du contexte de périphérique obtenu à partir de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . L’application doit dessiner uniquement dans le rectangle englobant. Pour des raisons de performances, le système ne découpe pas les portions de l’image qui sont dessinées en dehors du rectangle.
-   Restaurez tous les objets GDI sélectionnés pour le contexte de périphérique de l’élément de menu.

Si l’utilisateur sélectionne l’élément de menu, le système définit le membre **itemAction** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sur la valeur **Oda \_ Select** et définit la valeur **ODS \_ Selected** dans le membre **ItemState** . Il s’agit de la pile d’une application qui permet de redessiner l’élément de menu pour indiquer qu’il est sélectionné.

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a>Owner-Drawn les menus et le \_ message WM MENUCHAR

Les menus autres que les menus owner-drawn peuvent spécifier un mnémonique de menu en insérant un trait de soulignement à côté d’un caractère dans la chaîne de menu. Cela permet à l’utilisateur de sélectionner le menu en appuyant sur ALT et en appuyant sur le caractère mnémonique du menu. Toutefois, dans les menus owner-drawn, vous ne pouvez pas spécifier un mnémonique de menu de cette manière. Au lieu de cela, votre application doit traiter le message [**WM \_ MENUCHAR**](wm-menuchar.md) pour fournir des menus owner-drawn avec des mnémoniques de menu.

Le message [**WM \_ MENUCHAR**](wm-menuchar.md) est envoyé lorsque l’utilisateur tape un mnémonique de menu qui ne correspond à aucun des mnémoniques prédéfinis du menu actuel. La valeur contenue dans *wParam* spécifie le caractère ASCII qui correspond à la touche sur laquelle l’utilisateur a appuyé avec la touche Alt. Le mot de poids faible de *wParam* spécifie le type du menu sélectionné et peut prendre l’une des valeurs suivantes :

-   **MF \_ POPUP** si le menu actuel est un sous-menu.
-   **MF \_ SYSMENU** si le menu est le menu système.

Le mot de poids fort de *wParam* contient le handle de menu du menu actuel. La fenêtre avec les menus owner-drawn peut traiter [**WM \_ MENUCHAR**](wm-menuchar.md) comme suit :


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



Les deux dans le mot de poids fort de la valeur de retour informent le système que le mot de poids faible de la valeur de retour contient l’index de base zéro de l’élément de menu à sélectionner.

Les constantes suivantes correspondent aux valeurs de retour possibles du message [**WM \_ MENUCHAR**](wm-menuchar.md) .



| Constante         | Valeur | Signification                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MNC \_ Ignorer**  | 0     | Le système doit ignorer le caractère que l’utilisateur a appuyé et créer un bref signal sonore sur le haut-parleur du système.                                                       |
| **MNC \_ Fermer**   | 1     | Le système doit fermer le menu actif.                                                                                                                      |
| **exécution de MNC \_** | 2     | Le système doit choisir l’élément spécifié dans le mot de poids faible de la valeur de retour. La fenêtre propriétaire reçoit un message de [**\_ commande WM**](wm-command.md) . |
| **MNC \_ Sélectionner**  | 3     | Le système doit sélectionner l’élément spécifié dans le mot de poids faible de la valeur de retour.                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a>Définition des polices pour les chaînes de texte Menu-Item

Cette rubrique contient un exemple d’une application qui utilise des éléments de menu owner-drawn dans un menu. Le menu contient des éléments qui définissent les attributs de la police actuelle, et les éléments sont affichés à l’aide de l’attribut de police approprié.

Voici comment le menu est défini dans le fichier de définition de ressource. Notez que les chaînes pour les éléments de menu normal, gras, italique et souligné sont assignées au moment de l’exécution, de sorte que leurs chaînes sont vides dans le fichier de définition de ressource.


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



La procédure de fenêtre de l’application traite les messages impliqués dans l’utilisation d’éléments de menu owner-drawn. L’application utilise le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) pour effectuer les opérations suivantes :

-   Définissez l’indicateur de **\_ OwnerDraw OwnerDraw** pour les éléments de menu.
-   Définissez les chaînes de texte pour les éléments de menu.
-   Obtient les handles des polices utilisées pour dessiner les éléments.
-   Obtient les valeurs de couleur de texte et d’arrière-plan pour les éléments de menu sélectionnés.

Les chaînes de texte et les poignées de police sont stockées dans un tableau de structures MYITEM définies par l’application. La fonction GetAFont définie par l’application crée une police qui correspond à l’attribut de police spécifié et retourne un handle à la police. Les descripteurs sont détruits pendant le traitement du message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .

Pendant le traitement du message [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) , l’exemple obtient la largeur et la hauteur d’une chaîne d’élément de menu et copie ces valeurs dans la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) . Le système utilise les valeurs de largeur et de hauteur pour calculer la taille du menu.

Pendant le traitement du message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) , la chaîne de l’élément de menu est dessinée avec l’espace à gauche en regard de la chaîne pour la bitmap de coche. Si l’utilisateur sélectionne l’élément, le texte et les couleurs d’arrière-plan sélectionnés sont utilisés pour dessiner l’élément.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a>Exemple d’éléments de menu Owner-Drawn

L’exemple de cette rubrique utilise des éléments de menu owner-drawn dans un menu. Les éléments de menu sélectionnent des attributs de police spécifiques et l’application affiche chaque élément de menu à l’aide d’une police qui a l’attribut correspondant. Par exemple, l’élément de menu **italique** s’affiche dans une police en italique. Le nom du menu **caractère** dans la barre de menus ouvre le menu.

La barre de menus et le menu déroulant sont initialement définis par une ressource de modèle de menu étendue. Étant donné qu’un modèle de menu ne peut pas spécifier d’éléments owner-drawn, le menu contient initialement quatre éléments de menu texte avec les chaînes suivantes : « Regular », « Bold », « Italic » et « Underline ». La procédure de fenêtre de l’application les remplace par des éléments owner-drawn lors du traitement du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) . Lorsqu’il reçoit le message **WM \_ Create** , la procédure de fenêtre appelle la fonction OnCreate définie par l’application, qui effectue les étapes suivantes pour chaque élément de menu :

-   Alloue une structure MYITEM définie par l’application.
-   Obtient le texte de l’élément de menu et l’enregistre dans la structure MYITEM définie par l’application.
-   Crée la police utilisée pour afficher l’élément de menu et enregistre son handle dans la structure MYITEM définie par l’application.
-   Remplace le type d’élément de menu par **MFT \_ OwnerDraw** et enregistre un pointeur vers la structure MYITEM définie par l’application en tant que données d’élément.

Étant donné qu’un pointeur vers chaque structure MYITEM définie par l’application est enregistré en tant que données d’élément, il est passé à la procédure de fenêtre conjointement aux messages [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) et [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) pour l’élément de menu correspondant. Le pointeur est contenu dans le membre **ItemData** des structures [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) et [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

Un message [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) est envoyé pour chaque élément de menu owner-drawn la première fois qu’il est affiché. L’application traite ce message en sélectionnant la police de l’élément de menu dans un contexte de périphérique, puis en déterminant l’espace requis pour afficher le texte de l’élément de menu dans cette police. La police et le texte des éléments de menu sont spécifiés par la structure de l’élément de menu `MYITEM` (la structure définie par l’application). L’application détermine la taille du texte à l’aide de la fonction [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .

La procédure de fenêtre traite le message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) en affichant le texte de l’élément de menu dans la police appropriée. La police et le texte des éléments de menu sont spécifiés par la structure de l’élément de menu `MYITEM` . L’application sélectionne le texte et les couleurs d’arrière-plan appropriés à l’état de l’élément de menu.

La procédure de fenêtre traite le message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) pour détruire les polices et libérer de la mémoire. L’application supprime la police et libère la structure MYITEM définie par l’application pour chaque élément de menu.

Voici les parties pertinentes du fichier d’en-tête de l’application.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



Voici les parties pertinentes de la procédure de fenêtre de l’application et de ses fonctions associées.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a>Utilisation de bitmaps de coche personnalisées

Le système fournit une image bitmap de coche par défaut pour l’affichage à côté d’un élément de menu sélectionné. Vous pouvez personnaliser un élément de menu individuel en fournissant une paire de bitmaps pour remplacer la bitmap de coche par défaut. Le système affiche une image bitmap lorsque l’élément est sélectionné et l’autre quand il est clair. Cette section décrit les étapes nécessaires à la création et à l’utilisation de bitmaps de coche personnalisées.

-   [Création de bitmaps de coche personnalisées](#creating-custom-check-mark-bitmaps)
-   [Association de bitmaps à un élément de menu](#associating-bitmaps-with-a-menu-item)
-   [Définition de l’attribut coche](#setting-the-check-mark-attribute)
-   [Simulation de cases à cocher dans un menu](#simulating-check-boxes-in-a-menu)
-   [Exemple d’utilisation de bitmaps de coche personnalisées](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a>Création de bitmaps de coche personnalisées

Une bitmap de coche personnalisée doit avoir la même taille que la bitmap de coche par défaut. Vous pouvez récupérer la taille de coche par défaut de la bitmap en appelant la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Le mot de poids faible de la valeur de retour de cette fonction spécifie la largeur ; le mot de poids fort spécifie la hauteur.

Vous pouvez utiliser des ressources bitmap pour fournir des bitmaps de coche. Toutefois, étant donné que la taille de bitmap requise varie selon le type d’affichage, vous devrez peut-être redimensionner l’image bitmap au moment de l’exécution à l’aide de la fonction [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) . En fonction de la bitmap, la distorsion causée par le dimensionnement peut produire des résultats inacceptables.

Au lieu d’utiliser une ressource bitmap, vous pouvez créer une bitmap au moment de l’exécution à l’aide des fonctions GDI.

**Pour créer une bitmap au moment de l’exécution**

1.  Utilisez la fonction [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) pour créer un contexte de périphérique compatible avec celui utilisé par la fenêtre principale de l’application.

    Le paramètre *HDC* de la fonction peut spécifier une valeur **null** ou la valeur de retour de la fonction. [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) retourne un handle vers le contexte de périphérique (Device Context) compatible.

2.  Utilisez la fonction [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) pour créer une image bitmap compatible avec la fenêtre principale de l’application.

    Les paramètres *nWidth* et *nHeight* de cette fonction définissent la taille de l’image bitmap. ils doivent spécifier les informations de largeur et de hauteur retournées par la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .

    > [!Note]  
    > Vous pouvez également utiliser la fonction [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) pour créer une image bitmap monochrome.

     

3.  Utilisez la fonction [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) pour sélectionner la bitmap dans le contexte de périphérique compatible.
4.  Utilisez les fonctions de dessin GDI, telles que [**ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) et [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), pour dessiner une image dans la bitmap, ou utilisez des fonctions telles que [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) et [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) pour copier une image dans la bitmap.

Pour plus d’informations, consultez [bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="associating-bitmaps-with-a-menu-item"></a>Association de bitmaps à un élément de menu

Vous associez une paire de bitmaps de coche à un élément de menu en passant les descripteurs des bitmaps à la fonction [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) . Le paramètre *hBitmapUnchecked* identifie l’image bitmap en clair et le paramètre *hBitmapChecked* identifie la bitmap sélectionnée. Si vous souhaitez supprimer une des deux cases à cocher d’un élément de menu, vous pouvez définir le paramètre *hBitmapUnchecked* ou *hBitmapChecked* , ou les deux, sur la **valeur null**.

### <a name="setting-the-check-mark-attribute"></a>Définition de l’attribut coche

La fonction [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) définit l’attribut coche d’un élément de menu sur sélectionné ou désactivé. Vous pouvez spécifier la **valeur \_ activée MF** pour définir l’attribut case à cocher sur sélectionné et la valeur **MF \_ non vérifiée** pour le définir sur Clear.

Vous pouvez également définir l’état d’activation d’un élément de menu à l’aide de la fonction [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .

Parfois, un groupe d’éléments de menu représente un ensemble d’options s’excluant mutuellement. À l’aide de la fonction [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) , vous pouvez vérifier un élément de menu tout en supprimant simultanément la coche de tous les autres éléments de menu du groupe.

### <a name="simulating-check-boxes-in-a-menu"></a>Simulation de cases à cocher dans un menu

Cette rubrique contient un exemple qui montre comment simuler des cases à cocher dans un menu. L’exemple contient un menu de caractères dont les éléments permettent à l’utilisateur de définir les attributs gras, italique et souligné de la police actuelle. Lorsqu’un attribut de police est activé, une coche s’affiche dans la case à cocher en regard de l’élément de menu correspondant. Sinon, une case à cocher vide est affichée en regard de l’élément.

L’exemple remplace le bitmap de coche par défaut par deux bitmaps : un bitmap avec une case à cocher activée et l’image bitmap avec une zone vide. La bitmap de case à cocher sélectionnée s’affiche en regard de l’élément de menu gras, italique ou souligné lorsque l’attribut coche de l’élément est défini sur **MF \_ activé**. La case à cocher vide ou vide s’affiche lorsque l’attribut coche est défini sur **MF désactivé \_**.

Le système fournit une image bitmap prédéfinie qui contient les images utilisées pour les cases à cocher et les cases d’option. L’exemple isole les cases à cocher sélectionnées et vides, les copie dans deux bitmaps distinctes, puis les utilise comme images bitmap sélectionnées et effacées pour les éléments du menu **caractère** .

Pour récupérer un handle vers la bitmap de case à cocher définie par le système, l’exemple appelle la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , en spécifiant **null** comme paramètre *HINSTANCE* et **OBM \_ cases à cocher** comme paramètre *lpBitmapName* . Étant donné que les images de la bitmap ont la même taille, l’exemple peut les isoler en divisant la largeur et la hauteur de la bitmap par le nombre d’images dans ses lignes et colonnes.

La partie suivante d’un fichier de définition de ressource montre comment les éléments de menu du menu **caractère** sont définis. Notez qu’aucun attribut de police n’est défini au départ. par conséquent, l’attribut coche de l’élément **normal** est défini sur sélectionné et, par défaut, l’attribut coche des éléments restants est défini sur Clear.


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



Voici le contenu pertinent du fichier d’en-tête de l’application.


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



L’exemple suivant montre les parties de la procédure de fenêtre qui créent les bitmaps de coche. Définissez l’attribut coche des éléments de menu **gras**, **italique** et **souligné** . et détruisez les bitmaps de coche.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a>Exemple d’utilisation de bitmaps de coche personnalisées

L’exemple de cette rubrique assigne des bitmaps de coche personnalisée à des éléments de menu dans deux menus. Les éléments de menu du premier menu spécifient des attributs de caractères : gras, italique et souligné. Chaque élément de menu peut être sélectionné ou effacé. Pour ces éléments de menu, l’exemple utilise des bitmaps de coche qui ressemblent aux États sélectionnés et désactivés d’un contrôle de case à cocher.

Les éléments de menu du deuxième menu spécifient les paramètres d’alignement des paragraphes : gauche, Centre et droite. Un seul de ces éléments de menu est sélectionné à tout moment. Pour ces éléments de menu, l’exemple utilise des bitmaps de coche qui ressemblent aux États sélectionnés et clairs d’un contrôle de case d’option.

La procédure de fenêtre traite le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) en appelant la fonction OnCreate définie par l’application. `OnCreate` crée les quatre bitmaps de coche et les assigne à leurs éléments de menu appropriés à l’aide de la fonction [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .

Pour créer chaque bitmap, OnCreate appelle la fonction CreateMenuBitmaps définie par l’application, en spécifiant un pointeur vers une fonction de dessin spécifique à la bitmap. CreateMenuBitmaps crée une image bitmap monochrome de la taille requise, la sélectionne dans un contexte de périphérique de mémoire et efface l’arrière-plan. Ensuite, il appelle la fonction de dessin spécifiée pour remplir le premier plan.

Les quatre fonctions de dessin définies par l’application sont DrawCheck, DrawUncheck, **DrawRadioCheck** et DrawRadioUncheck. Ils dessinent un rectangle avec un X, un rectangle vide, une ellipse contenant une Ellipse remplie plus petite et une ellipse vide, respectivement.

La procédure de fenêtre traite le message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) en supprimant les bitmaps de coche. Il récupère chaque handle de bitmap à l’aide de la fonction [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) , puis passe un handle à la fonction.

Quand l’utilisateur choisit un élément de menu, un message de [**\_ commande WM**](wm-command.md) est envoyé à la fenêtre propriétaire. Pour les éléments de menu du menu **caractère** , la procédure de fenêtre appelle la fonction CheckCharacterItem définie par l’application. Pour les éléments du menu **paragraphe** , la procédure de fenêtre appelle la fonction CheckParagraphItem définie par l’application.

Chaque élément du menu **caractère** peut être sélectionné et effacé indépendamment. Par conséquent, CheckCharacterItem bascule simplement l’état d’activation de l’élément de menu spécifié. Tout d’abord, la fonction appelle la fonction [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) pour récupérer l’état actuel de l’élément de menu. Ensuite, il bascule l’indicateur d’état **\_ activé MFS** et définit le nouvel État en appelant la fonction [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .

Contrairement aux attributs de caractères, un seul alignement de paragraphe peut être sélectionné à la fois. Par conséquent, CheckParagraphItem vérifie l’élément de menu spécifié et supprime la coche de tous les autres éléments du menu. Pour ce faire, il appelle la fonction [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .

Voici les parties pertinentes du fichier d’en-tête de l’application.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



Voici les parties pertinentes de la procédure de fenêtre de l’application et des fonctions associées.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 