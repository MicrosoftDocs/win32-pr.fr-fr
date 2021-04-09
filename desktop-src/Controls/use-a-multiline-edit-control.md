---
title: Création d’un contrôle d’édition multiligne
description: Cette rubrique montre comment implémenter un traitement de texte simple en ajoutant un contrôle d’édition multiligne à la zone cliente d’une fenêtre.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941482"
---
# <a name="how-to-create-a-multiline-edit-control"></a><span data-ttu-id="934a6-103">Création d’un contrôle d’édition multiligne</span><span class="sxs-lookup"><span data-stu-id="934a6-103">How to Create a Multiline Edit Control</span></span>

<span data-ttu-id="934a6-104">Cette rubrique montre comment implémenter un traitement de texte simple en ajoutant un contrôle d’édition multiligne à la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="934a6-104">This topic demonstrates how to implement a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="934a6-105">À l’aide du contrôle d’édition multiligne, l’utilisateur peut sélectionner Modifier les commandes dans un menu.</span><span class="sxs-lookup"><span data-stu-id="934a6-105">By using the multiline edit control, the user can select edit commands from a menu.</span></span> <span data-ttu-id="934a6-106">Ces commandes permettent à l’utilisateur d’effectuer des opérations de modification simples, telles que l’annulation d’une action précédente, de couper ou copier des sélections dans le presse-papiers, de coller du texte à partir du presse-papiers et de supprimer la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="934a6-106">These commands enable the user to perform simple editing operations such as undo a previous action, cut or copy selections to the clipboard, paste text from the clipboard, and delete the current selection.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="934a6-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="934a6-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="934a6-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="934a6-108">Technologies</span></span>

-   [<span data-ttu-id="934a6-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="934a6-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="934a6-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="934a6-110">Prerequisites</span></span>

-   <span data-ttu-id="934a6-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="934a6-111">C/C++</span></span>
-   <span data-ttu-id="934a6-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="934a6-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="934a6-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="934a6-113">Instructions</span></span>


<span data-ttu-id="934a6-114">Votre application doit inclure du code pour créer une instance de et initialiser un contrôle d’édition multiligne, puis traiter des commandes d’édition utilisateur.</span><span class="sxs-lookup"><span data-stu-id="934a6-114">Your application must include code to create an instance of and initialize a multiline edit control and then process user edit commands.</span></span>

<span data-ttu-id="934a6-115">L’exemple de code C++ suivant implémente la plupart des fonctionnalités d’un traitement de texte simple en ajoutant un contrôle d’édition multiligne à la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="934a6-115">The following C++ code example implements much of the functionality of a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="934a6-116">Le système effectue automatiquement des opérations de retour automatique à la commande pour le contrôle d’édition et gère également le traitement de la barre de défilement verticale (créé en spécifiant [**es \_ AUTOVSCROLL**](edit-control-styles.md) dans l’appel à la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).</span><span class="sxs-lookup"><span data-stu-id="934a6-116">The system automatically performs wordwrap operations for the edit control and also handles the processing for the vertical scroll bar (created by specifying [**ES\_AUTOVSCROLL**](edit-control-styles.md) in the call to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function).</span></span>

<span data-ttu-id="934a6-117">Les commandes de modification de l’utilisateur sont envoyées au processus de fenêtre via des messages de notification de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="934a6-117">User edit commands are sent to the window process via [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages.</span></span>

> [!Note]  
> <span data-ttu-id="934a6-118">Si la fenêtre comprend le ruban Windows, la taille du contrôle d’édition doit être ajustée pour s’adapter à la hauteur du ruban.</span><span class="sxs-lookup"><span data-stu-id="934a6-118">If the window includes the Windows Ribbon, the size of the edit control must be adjusted to accommodate the height of the Ribbon.</span></span> <span data-ttu-id="934a6-119">Pour plus d’informations, consultez [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span><span class="sxs-lookup"><span data-stu-id="934a6-119">For more information, see [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span></span>

 



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



## <a name="related-topics"></a><span data-ttu-id="934a6-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="934a6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="934a6-121">À propos des contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="934a6-121">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="934a6-122">Modifier la référence de contrôle</span><span class="sxs-lookup"><span data-stu-id="934a6-122">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="934a6-123">Utilisation des contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="934a6-123">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="934a6-124">Modifier le contrôle</span><span class="sxs-lookup"><span data-stu-id="934a6-124">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 