---
title: Création d’un contrôle d’édition multiligne
description: Cette rubrique montre comment implémenter un traitement de texte simple en ajoutant un contrôle d’édition multiligne à la zone cliente d’une fenêtre.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115386"
---
# <a name="how-to-create-a-multiline-edit-control"></a>Création d’un contrôle d’édition multiligne

Cette rubrique montre comment implémenter un traitement de texte simple en ajoutant un contrôle d’édition multiligne à la zone cliente d’une fenêtre. À l’aide du contrôle d’édition multiligne, l’utilisateur peut sélectionner Modifier les commandes dans un menu. Ces commandes permettent à l’utilisateur d’effectuer des opérations de modification simples, telles que l’annulation d’une action précédente, de couper ou copier des sélections dans le presse-papiers, de coller du texte à partir du presse-papiers et de supprimer la sélection actuelle.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Votre application doit inclure du code pour créer une instance de et initialiser un contrôle d’édition multiligne, puis traiter des commandes d’édition utilisateur.

L’exemple de code C++ suivant implémente la plupart des fonctionnalités d’un traitement de texte simple en ajoutant un contrôle d’édition multiligne à la zone cliente d’une fenêtre. Le système effectue automatiquement des opérations de retour automatique à la commande pour le contrôle d’édition et gère également le traitement de la barre de défilement verticale (créé en spécifiant [**es \_ AUTOVSCROLL**](edit-control-styles.md) dans l’appel à la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).

Les commandes de modification de l’utilisateur sont envoyées au processus de fenêtre via des messages de notification de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .

> [!Note]  
> si la fenêtre comprend le ruban Windows, la taille du contrôle d’édition doit être ajustée pour s’adapter à la hauteur du ruban. pour plus d’informations, consultez [Windows infrastructure du ruban](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles d’édition](about-edit-controls.md)
</dt> <dt>

[Modifier la référence de contrôle](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Utilisation des contrôles d’édition](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Modifier le contrôle](edit-controls.md)
</dt> </dl>

 

 