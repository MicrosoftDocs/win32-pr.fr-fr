---
description: Les exemples de cette section décrivent comment effectuer des tâches associées à l’utilisation de Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Utilisation de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196067"
---
# <a name="using-windows"></a>Utilisation de Windows

Les exemples de cette section décrivent comment effectuer les tâches suivantes :

-   [Création d’une fenêtre principale](#creating-a-main-window)
-   [Création, énumération et dimensionnement des Windows enfants](#creating-enumerating-and-sizing-child-windows)
-   [Destruction d’une fenêtre](#destroying-a-window)
-   [Utilisation de Windows en couches](#using-layered-windows)

## <a name="creating-a-main-window"></a>Création d’une fenêtre principale

La première fenêtre créée par une application est généralement la fenêtre principale. Vous créez la fenêtre principale à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre, le nom de la fenêtre, les styles de fenêtre, la taille, la position, le handle de menu, le handle d’instance et les données de création. Une fenêtre principale appartient à une classe de fenêtre définie par l’application. vous devez donc inscrire la classe de fenêtre et fournir une procédure de fenêtre pour la classe avant de créer la fenêtre principale.

La plupart des applications utilisent généralement le style [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) pour créer la fenêtre principale. Ce style donne à la fenêtre une barre de titre, un menu fenêtre, une bordure de redimensionnement et des boutons réduire et agrandir. La fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retourne un handle qui identifie de façon unique la fenêtre.

L’exemple suivant crée une fenêtre principale appartenant à une classe de fenêtre définie par l’application. Le nom de la fenêtre, **fenêtre principale**, s’affiche dans la barre de titre de la fenêtre. En combinant les [**styles \_ WS VSCROLL**](window-styles.md) et **WS \_ HSCROLL** avec le style **WS \_ OVERLAPPEDWINDOW** , l’application crée une fenêtre principale avec des barres de défilement horizontale et verticale en plus des composants fournis par le style **WS \_ OVERLAPPEDWINDOW** . Les quatre occurrences de la **constante \_ usedefault en PV** définissent la taille initiale et la position de la fenêtre en fonction des valeurs par défaut définies par le système. En spécifiant la **valeur null** au lieu d’un handle de menu, le menu est défini pour la classe de fenêtre.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



Notez que l’exemple précédent appelle la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) après la création de la fenêtre principale. Cela est dû au fait que le système n’affiche pas automatiquement la fenêtre principale après l’avoir créée. En passant l’indicateur **SW \_ SHOWDEFAULT** à **ShowWindow**, l’application autorise le programme qui a démarré l’application à définir l’état d’affichage initial de la fenêtre principale. La fonction [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) envoie la fenêtre à son premier message [**WM \_ Paint**](../gdi/wm-paint.md) .

## <a name="creating-enumerating-and-sizing-child-windows"></a>Création, énumération et dimensionnement des Windows enfants

Vous pouvez diviser la zone cliente d’une fenêtre en différentes zones fonctionnelles à l’aide de fenêtres enfants. La création d’une fenêtre enfant est semblable à la création d’une fenêtre principale : vous utilisez la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Pour créer une fenêtre d’une classe de fenêtre définie par l’application, vous devez inscrire la classe de fenêtre et fournir une procédure de fenêtre avant de créer la fenêtre enfant. Vous devez attribuer à la fenêtre enfant le style [**WS \_ Child**](window-styles.md) et spécifier une fenêtre parente pour la fenêtre enfant lorsque vous la créez.

L’exemple suivant divise la zone cliente de la fenêtre principale d’une application en trois zones fonctionnelles en créant trois fenêtres enfants de taille égale. Chaque fenêtre enfant a la même hauteur que la zone cliente de la fenêtre principale, mais la largeur de chaque fenêtre est égale à un tiers. La fenêtre principale crée les fenêtres enfants en réponse au message [**WM \_ Create**](wm-create.md) , que la fenêtre principale reçoit au cours de son propre processus de création de fenêtre. Étant donné que chaque fenêtre enfant a le style de [**\_ bordure WS**](window-styles.md) , chacun a une bordure de trait fine. En outre, étant donné que le style **\_ visible de WS** n’est pas spécifié, chaque fenêtre enfant est initialement masquée. Notez également que chaque fenêtre enfant est assignée à un identificateur de fenêtre enfant.

La fenêtre principale dimensionne et positionne les fenêtres enfants en réponse au message [**de \_ taille WM**](wm-size.md) , que la fenêtre principale reçoit lorsque sa taille change. En réponse à **la \_ taille de WM**, la fenêtre principale récupère les dimensions de sa zone cliente à l’aide de la fonction [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) , puis passe les dimensions à la fonction [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) . **EnumChildWindows** transmet le descripteur à chaque fenêtre enfant, à son tour, à la fonction de rappel [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) définie par l’application. Cette fonction dimensionne et positionne chaque fenêtre enfant en appelant la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) ; la taille et la position sont basées sur les dimensions de la zone cliente de la fenêtre principale et l’identificateur de la fenêtre enfant. Ensuite, **EnumChildProc** appelle la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) pour rendre la fenêtre visible.


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a>Destruction d’une fenêtre

Vous pouvez utiliser la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) pour détruire une fenêtre. En règle générale, une application envoie le message de [**\_ fermeture WM**](wm-close.md) avant de détruire une fenêtre, donnant à la fenêtre la possibilité de demander confirmation à l’utilisateur avant la destruction de la fenêtre. Une fenêtre qui comprend un menu fenêtre reçoit automatiquement le message **WM \_ Close** quand l’utilisateur clique sur **Fermer** dans le menu fenêtre. Si l’utilisateur confirme que la fenêtre doit être détruite, l’application appelle **DestroyWindow**. Le système envoie le message de [**\_ destruction WM**](wm-destroy.md) à la fenêtre après l’avoir supprimé de l’écran. En réponse à **la \_ destruction de WM**, la fenêtre enregistre ses données et libère toutes les ressources qu’elle a allouées. Une fenêtre principale conclut son traitement de **WM \_ Destroy** en appelant la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) pour quitter l’application.

L’exemple suivant montre comment demander la confirmation de l’utilisateur avant de détruire une fenêtre. En réponse à [**la \_ fermeture de WM**](wm-close.md), l’exemple affiche une boîte de dialogue qui contient les boutons **Oui**, **non** et **Annuler** . Si l’utilisateur clique sur **Oui**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) est appelé ; dans le cas contraire, la fenêtre n’est pas détruite. Étant donné que la fenêtre en cours de destruction est une fenêtre principale, l’exemple appelle [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) en réponse à [**WM \_ Destroy**](wm-destroy.md).


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a>Utilisation de Windows en couches

Pour qu’une boîte de dialogue s’impose en tant que fenêtre translucide, commencez par créer la boîte de dialogue comme d’habitude. Ensuite, sur [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), définissez le bit de couche du style étendu de la fenêtre et appelez [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) avec la valeur alpha souhaitée. Le code peut se présenter comme suit :


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Notez que le troisième paramètre de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) est une valeur comprise entre 0 et 255, avec 0 pour rendre la fenêtre complètement transparente et 255 la rendre entièrement opaque. Ce paramètre imite le [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) plus polyvalent de la fonction [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .

Pour que cette fenêtre soit complètement opaque, supprimez le bit de **\_ \_ couche WS ex** en appelant [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , puis demandez à la fenêtre de repeindre. La suppression du bit est souhaitée pour permettre au système de savoir qu’il peut libérer de la mémoire associée à la superposition et à la redirection. Le code peut se présenter comme suit :


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



pour pouvoir utiliser des fenêtres enfants superposées, l’application doit déclarer elle-même Windows 8 prise en charge dans le manifeste.

 

 
