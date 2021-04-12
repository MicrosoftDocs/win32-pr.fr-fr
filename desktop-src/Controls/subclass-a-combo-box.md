---
title: Comment sous-classe une zone de liste déroulante
description: Cette rubrique montre comment sous-classer des zones de liste déroulante.
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b48301309597c53f02ca87d1d1748ab1fe05139
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031957"
---
# <a name="how-to-subclass-a-combo-box"></a><span data-ttu-id="1472d-103">Comment sous-classe une zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="1472d-103">How to Subclass a Combo Box</span></span>

<span data-ttu-id="1472d-104">Cette rubrique montre comment sous-classer des zones de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="1472d-104">This topic demonstrates how to subclass combo boxes.</span></span> <span data-ttu-id="1472d-105">L’exemple d’application C++ crée une fenêtre de barre d’outils qui contient deux zones de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="1472d-105">The C++ example application creates a toolbar window that contains two combo boxes.</span></span> <span data-ttu-id="1472d-106">En sous-classant les contrôles d’édition dans les zones de liste déroulante, la fenêtre de barre d’outils intercepte les touches TAB, entrée et Échap qui, sinon, seraient ignorées.</span><span class="sxs-lookup"><span data-stu-id="1472d-106">By subclassing the edit controls within the combo boxes, the toolbar window intercepts TAB, ENTER, and ESC keys that would otherwise be ignored.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1472d-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="1472d-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1472d-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="1472d-108">Technologies</span></span>

-   [<span data-ttu-id="1472d-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="1472d-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1472d-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="1472d-110">Prerequisites</span></span>

-   <span data-ttu-id="1472d-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="1472d-111">C/C++</span></span>
-   <span data-ttu-id="1472d-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="1472d-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1472d-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="1472d-113">Instructions</span></span>

### <a name="process-the-wm_create-message"></a><span data-ttu-id="1472d-114">Traiter le \_ message WM Create</span><span class="sxs-lookup"><span data-stu-id="1472d-114">Process the WM\_CREATE Message</span></span>

<span data-ttu-id="1472d-115">L’application traite le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) pour créer deux contrôles de zone de liste déroulante sous la forme de fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="1472d-115">The application processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to create two combo box controls as child windows.</span></span>


```C++
//  Create two combo box child windows. 
dwBaseUnits = GetDialogBaseUnits(); 
 
hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (6 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, NULL, NULL);  
 
hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (112 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, hInst, NULL); 
```



<span data-ttu-id="1472d-116">L’application sous-classe ensuite les contrôles d’édition (champs de sélection) dans chaque zone de liste déroulante, car ils reçoivent l’entrée de caractères pour une zone de liste modifiable simple et déroulante.</span><span class="sxs-lookup"><span data-stu-id="1472d-116">The application then subclasses the edit controls (selection fields) in each combo box, because they receive the character input for simple and drop-down combo box.</span></span> <span data-ttu-id="1472d-117">Enfin, il appelle la fonction [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) pour récupérer le handle de chaque contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="1472d-117">Finally, it calls the [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) function to retrieve the handle to each edit control.</span></span>

<span data-ttu-id="1472d-118">Pour sous-classer les contrôles d’édition, l’application appelle la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , en remplaçant le pointeur vers la procédure de fenêtre de classe par un pointeur vers la fonction **SubClassProc** définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="1472d-118">To subclass the edit controls, the application calls the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function, replacing the pointer to the class window procedure with a pointer to the application-defined **SubClassProc** function.</span></span> <span data-ttu-id="1472d-119">Le pointeur vers la procédure de fenêtre d’origine est enregistré dans la variable globale *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="1472d-119">The pointer to the original window procedure is saved in the global variable *lpfnEditWndProc*.</span></span>

<span data-ttu-id="1472d-120">**SubClassProc** intercepte les touches Tab, entrée et ÉCHAP et avertit la fenêtre de la barre d’outils en envoyant des messages définis par l’application ( \_ onglet WM, WM \_ ESC et WM \_ Enter).</span><span class="sxs-lookup"><span data-stu-id="1472d-120">**SubClassProc** intercepts TAB, ENTER, and ESC keys and notifies the toolbar window by sending application-defined messages (WM\_TAB, WM\_ESC, and WM\_ENTER).</span></span> <span data-ttu-id="1472d-121">**SubClassProc** utilise la fonction [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) pour transmettre la plupart des messages à la procédure de fenêtre d’origine, *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="1472d-121">**SubClassProc** uses the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function to pass most messages to the original window procedure, *lpfnEditWndProc*.</span></span>


```C++
//  Get the edit window handle to each combo box. 
pt.x = 1; 
pt.y = 1; 
hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
//  Change the window procedure for both edit windows 
//  to the subclass procedure. 
lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
    GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
```



### <a name="process-the-wm_setfocus-message"></a><span data-ttu-id="1472d-122">Traiter le \_ message WM SetFocus</span><span class="sxs-lookup"><span data-stu-id="1472d-122">Process the WM\_SETFOCUS Message</span></span>

<span data-ttu-id="1472d-123">Quand la fenêtre de barre d’outils reçoit le focus d’entrée, elle définit immédiatement le focus sur la première zone de liste déroulante de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1472d-123">When the toolbar window receives the input focus, it immediately sets the focus to the first combo box in the toolbar.</span></span> <span data-ttu-id="1472d-124">Pour ce faire, l’exemple appelle la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) en réponse au message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="1472d-124">To do this, the example calls the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function in response to the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span>


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a><span data-ttu-id="1472d-125">Traiter les messages de Application-Defined</span><span class="sxs-lookup"><span data-stu-id="1472d-125">Process Application-Defined Messages</span></span>

<span data-ttu-id="1472d-126">La fonction **SubClassProc** envoie des messages définis par l’application à la fenêtre de la barre d’outils lorsque l’utilisateur appuie sur la touche Tab, entrée ou ÉCHAP dans une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="1472d-126">The **SubClassProc** function sends application-defined messages to the toolbar window when the user presses the TAB, ENTER, or ESC key in a combo box.</span></span> <span data-ttu-id="1472d-127">Le message de l' **\_ onglet WM** est envoyé pour la touche Tab, le message « **WM \_ ESC** » pour la touche ÉCHAP et le message **WM \_ Enter** pour la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="1472d-127">The **WM\_TAB** message is sent for the TAB key, the **WM\_ESC** message for the ESC key, and the **WM\_ENTER** message for the ENTER key.</span></span>

<span data-ttu-id="1472d-128">L’exemple traite le message de l' **\_ onglet WM** en définissant le focus sur la zone de liste déroulante suivante dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1472d-128">The example processes the **WM\_TAB** message by setting the focus to the next combo box in the toolbar.</span></span> <span data-ttu-id="1472d-129">Il traite le message **WM \_ ESC** en définissant le focus sur la fenêtre d’application principale.</span><span class="sxs-lookup"><span data-stu-id="1472d-129">It processes the **WM\_ESC** message by setting the focus to the main application window.</span></span>


```C++
  case WM_TAB: 
      if (GetFocus() == hwndEdit1) 
          SetFocus(hwndCombo2); 
      else 
          SetFocus(hwndCombo1); 
      break; 
 
  case WM_ESC: 
       hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
       // Clear the current selection. 
       SendMessage(hwndCombo, CB_SETCURSEL, 
          (WPARAM) (-1), 0); 
 
      //  Set the focus to the main window. 
      SetFocus(hwndMain); 
      break;
```



<span data-ttu-id="1472d-130">En réponse au message **WM \_ Enter** , l’exemple vérifie que la sélection actuelle de la zone de liste déroulante est valide, puis définit le focus sur la fenêtre d’application principale.</span><span class="sxs-lookup"><span data-stu-id="1472d-130">In response to the **WM\_ENTER** message, the example ensures that the current selection for the combo box is valid and then sets the focus to the main application window.</span></span> <span data-ttu-id="1472d-131">Si la zone de liste déroulante ne contient aucune sélection actuelle, l’exemple utilise le message [**CB \_ FindExactString**](cb-findstringexact.md) pour rechercher un élément de liste qui correspond au contenu du champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="1472d-131">If the combo box contains no current selection, the example uses the [**CB\_FINDSTRINGEXACT**](cb-findstringexact.md) message to search for a list item that matches the contents of the selection field.</span></span> <span data-ttu-id="1472d-132">En cas de correspondance, l’exemple définit la sélection actuelle ; dans le cas contraire, il ajoute un nouvel élément de liste.</span><span class="sxs-lookup"><span data-stu-id="1472d-132">If there is a match, the example sets the current selection; otherwise, it adds a new list item.</span></span>


```C++
case WM_ENTER: 
    hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
    SetFocus(hwndMain); 
 
    //  If there is no current selection, set one. 
    if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
            == CB_ERR) 
    { 
        if (SendMessage(hwndCombo, WM_GETTEXT, 
                sizeof(achTemp), (LPARAM) achTemp) == 0) 
            break;      //  Empty selection field 
        dwIndex = SendMessage(hwndCombo, 
            CB_FINDSTRINGEXACT, (WPARAM) (-1), 
            (LPARAM) achTemp); 
 
        //  Add the string, if necessary, and select it. 
        if (dwIndex == CB_ERR) 
            dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                0, (LPARAM) achTemp); 
        if (dwIndex != CB_ERR) 
            SendMessage(hwndCombo, CB_SETCURSEL, 
                dwIndex, 0); 
    } 
    break; 
       
    // . 
    // .  Process additional messages. 
    // . 
 
default: 
    return DefWindowProc(hwnd, msg, wParam, lParam); 
```



## <a name="complete-example"></a><span data-ttu-id="1472d-133">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="1472d-133">Complete example</span></span>

<span data-ttu-id="1472d-134">Voici la procédure de fenêtre pour la barre d’outils et la procédure de sous-classe pour les deux zones de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="1472d-134">Following are the window procedure for the toolbar and the subclass procedure for the two combo boxes.</span></span>


```C++
#define WM_TAB (WM_USER) 
#define WM_ESC (WM_USER + 1) 
#define WM_ENTER (WM_USER + 2) 

//  Global variables
HWND    hwndMain; 
WNDPROC lpfnEditWndProc; //  Original wndproc for the combo box 

//  Prototypes
LRESULT CALLBACK SubClassProc( HWND, UINT, WPARAM, LPARAM );
 
/******************************************************** 
 
    FUNCTION:   ToolbarWindowProc 
 
    PURPOSE:    Window procedure for the toolbar window 
 
*********************************************************/ 
 
LRESULT CALLBACK ToolbarWindowProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    static HWND   hwndEdit1; 
    static HWND   hwndEdit2; 
    static HWND   hwndCombo1; 
    static HWND   hwndCombo2; 
    POINT       pt; 
    DWORD       dwBaseUnits; 
    HWND        hwndCombo; 
    DWORD       dwIndex; 
    char achTemp[256];       //  Temporary buffer 
 
    switch (msg) 
    { 
        case WM_CREATE: 
            //  Create two combo box child windows. 
            dwBaseUnits = GetDialogBaseUnits(); 
 
            hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (6 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, NULL, NULL);  
 
            hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (112 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, hInst, NULL); 
            
            //  Get the edit window handle to each combo box. 
            pt.x = 1; 
            pt.y = 1; 
            hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
            hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
            //  Change the window procedure for both edit windows 
            //  to the subclass procedure. 
            lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
                GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
            SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 

            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndCombo1); 
            break; 

        case WM_TAB: 
            if (GetFocus() == hwndEdit1) 
                SetFocus(hwndCombo2); 
            else 
                SetFocus(hwndCombo1); 
            break; 
 
        case WM_ESC: 
             hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
             // Clear the current selection. 
             SendMessage(hwndCombo, CB_SETCURSEL, 
                (WPARAM) (-1), 0); 
 
            //  Set the focus to the main window. 
            SetFocus(hwndMain); 
            break;

        case WM_ENTER: 
            hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
            SetFocus(hwndMain); 
 
            //  If there is no current selection, set one. 
            if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
                    == CB_ERR) 
            { 
                if (SendMessage(hwndCombo, WM_GETTEXT, 
                        sizeof(achTemp), (LPARAM) achTemp) == 0) 
                    break;      //  Empty selection field 
                dwIndex = SendMessage(hwndCombo, 
                    CB_FINDSTRINGEXACT, (WPARAM) (-1), 
                    (LPARAM) achTemp); 
 
                //  Add the string, if necessary, and select it. 
                if (dwIndex == CB_ERR) 
                    dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                        0, (LPARAM) achTemp); 
                if (dwIndex != CB_ERR) 
                    SendMessage(hwndCombo, CB_SETCURSEL, 
                        dwIndex, 0); 
            } 
            break; 
       
            // . 
            // .  Process additional messages. 
            // . 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
/******************************************************** 
 
    FUNCTION:   SubClassProc 
 
    PURPOSE:    Process TAB and ESCAPE keys, and pass all 
                other messages to the class window 
                procedure. 
 
*********************************************************/ 
LRESULT CALLBACK SubClassProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (msg) 
    { 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_TAB: 
                    SendMessage(hwndMain, WM_TAB, 0, 0); 
                    return 0; 
                case VK_ESCAPE: 
                    SendMessage(hwndMain, WM_ESC, 0, 0); 
                    return 0; 
                case VK_RETURN: 
                    SendMessage(hwndMain, WM_ENTER, 0, 0); 
                    return 0; 
            } 
            break; 
 
        case WM_KEYUP: 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case VK_TAB: 
                case VK_ESCAPE: 
                case VK_RETURN: 
                    return 0; 
            } 
    } 
 
    //  Call the original window procedure for default processing. 
     return CallWindowProc(lpfnEditWndProc, hwnd, msg, wParam, lParam); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="1472d-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1472d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1472d-136">À propos des zones de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="1472d-136">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="1472d-137">Référence du contrôle ComboBox</span><span class="sxs-lookup"><span data-stu-id="1472d-137">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1472d-138">Utilisation de zones de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="1472d-138">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="1472d-139">ComboBox</span><span class="sxs-lookup"><span data-stu-id="1472d-139">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 