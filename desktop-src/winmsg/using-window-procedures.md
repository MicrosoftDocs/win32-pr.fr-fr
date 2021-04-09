---
description: Cette section explique comment effectuer les tâches suivantes associées aux procédures de fenêtre.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Utilisation des procédures de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867990"
---
# <a name="using-window-procedures"></a>Utilisation des procédures de fenêtre

Cette section explique comment effectuer les tâches suivantes associées aux procédures de fenêtre.

-   [Conception d’une procédure de fenêtre](#designing-a-window-procedure)
-   [Association d’une procédure de fenêtre à une classe de fenêtre](#associating-a-window-procedure-with-a-window-class)
-   [Sous-classement d’une fenêtre](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Conception d’une procédure de fenêtre

L’exemple suivant illustre la structure d’une procédure de fenêtre classique. La procédure de fenêtre utilise l’argument message dans une instruction **switch** avec des messages individuels gérés par des instructions **case** distinctes. Notez que chaque cas retourne une valeur spécifique pour chaque message. Pour les messages qu’il ne traite pas, la procédure de fenêtre appelle la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



Le message [**WM \_ NCCREATE**](wm-nccreate.md) est envoyé juste après la création de votre fenêtre, mais si une application répond à ce message en renvoyant **false**, la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) échoue. Le message [**WM \_ Create**](wm-create.md) est envoyé une fois que votre fenêtre a déjà été créée.

Le message [**WM \_ Destroy**](wm-destroy.md) est envoyé lorsque votre fenêtre est sur le lieu d’être détruite. La fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) s’occupe de détruire les fenêtres enfants de la fenêtre en cours de destruction. Le message [**WM \_ NCDESTROY**](wm-ncdestroy.md) est envoyé juste avant la destruction d’une fenêtre.

Au minimum, une procédure de fenêtre doit traiter le message [**de \_ peinture WM**](../gdi/wm-paint.md) pour se dessiner lui-même. En règle générale, il doit également gérer les messages de souris et de clavier. Consultez les descriptions des messages individuels pour déterminer si votre procédure de fenêtre doit les gérer.

Votre application peut appeler la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dans le cadre du traitement d’un message. Dans ce cas, l’application peut modifier les paramètres de message avant de transmettre le message à **DefWindowProc**, ou elle peut poursuivre le traitement par défaut après avoir effectué ses propres opérations.

Une procédure de boîte de dialogue reçoit un message [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) au lieu d’un message [**WM \_ Create**](wm-create.md) et ne passe pas de messages non traités à la fonction [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) . Dans le cas contraire, une procédure de boîte de dialogue est exactement la même qu’une procédure de fenêtre.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Association d’une procédure de fenêtre à une classe de fenêtre

Vous associez une procédure de fenêtre à une classe de fenêtre lors de l’inscription de la classe. Vous devez remplir une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) avec des informations sur la classe, et le membre **lpfnWndProc** doit spécifier l’adresse de la procédure de fenêtre. Pour inscrire la classe, transmettez l’adresse de la structure **WNDCLASS** à la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . Une fois la classe de fenêtre inscrite, la procédure de fenêtre est automatiquement associée à chaque nouvelle fenêtre créée avec cette classe.

L’exemple suivant montre comment associer la procédure de fenêtre de l’exemple précédent à une classe de fenêtre.


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a>Sous-classement d’une fenêtre

Pour sous-classer une instance d’une fenêtre, appelez la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) et spécifiez le descripteur de la fenêtre pour sous-classer l' \_ indicateur WNDPROC GWL et un pointeur vers la procédure de sous-classe. **SetWindowLong** retourne un pointeur vers la procédure de fenêtre d’origine ; Utilisez ce pointeur pour passer des messages à la procédure d’origine. La procédure de fenêtre de la sous-classe doit utiliser la fonction [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) pour appeler la procédure de fenêtre d’origine.

> [!Note]  
> Pour écrire du code compatible avec les versions 32 bits et 64 bits de Windows, utilisez la fonction [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .

 

L’exemple suivant montre comment sous-classer une instance d’un contrôle d’édition dans une boîte de dialogue. La procédure de fenêtre de la sous-classe permet au contrôle d’édition de recevoir toutes les entrées au clavier, y compris les touches entrée et tabulation, chaque fois que le contrôle a le focus d’entrée.


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
