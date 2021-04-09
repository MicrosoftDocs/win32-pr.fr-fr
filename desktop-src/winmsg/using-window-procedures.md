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
# <a name="using-window-procedures"></a><span data-ttu-id="32f43-103">Utilisation des procédures de fenêtre</span><span class="sxs-lookup"><span data-stu-id="32f43-103">Using Window Procedures</span></span>

<span data-ttu-id="32f43-104">Cette section explique comment effectuer les tâches suivantes associées aux procédures de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="32f43-104">This section explains how to perform the following tasks associated with window procedures.</span></span>

-   [<span data-ttu-id="32f43-105">Conception d’une procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="32f43-105">Designing a Window Procedure</span></span>](#designing-a-window-procedure)
-   [<span data-ttu-id="32f43-106">Association d’une procédure de fenêtre à une classe de fenêtre</span><span class="sxs-lookup"><span data-stu-id="32f43-106">Associating a Window Procedure with a Window Class</span></span>](#associating-a-window-procedure-with-a-window-class)
-   [<span data-ttu-id="32f43-107">Sous-classement d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="32f43-107">Subclassing a Window</span></span>](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a><span data-ttu-id="32f43-108">Conception d’une procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="32f43-108">Designing a Window Procedure</span></span>

<span data-ttu-id="32f43-109">L’exemple suivant illustre la structure d’une procédure de fenêtre classique.</span><span class="sxs-lookup"><span data-stu-id="32f43-109">The following example shows the structure of a typical window procedure.</span></span> <span data-ttu-id="32f43-110">La procédure de fenêtre utilise l’argument message dans une instruction **switch** avec des messages individuels gérés par des instructions **case** distinctes.</span><span class="sxs-lookup"><span data-stu-id="32f43-110">The window procedure uses the message argument in a **switch** statement with individual messages handled by separate **case** statements.</span></span> <span data-ttu-id="32f43-111">Notez que chaque cas retourne une valeur spécifique pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="32f43-111">Notice that each case returns a specific value for each message.</span></span> <span data-ttu-id="32f43-112">Pour les messages qu’il ne traite pas, la procédure de fenêtre appelle la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="32f43-112">For messages that it does not process, the window procedure calls the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>


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



<span data-ttu-id="32f43-113">Le message [**WM \_ NCCREATE**](wm-nccreate.md) est envoyé juste après la création de votre fenêtre, mais si une application répond à ce message en renvoyant **false**, la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) échoue.</span><span class="sxs-lookup"><span data-stu-id="32f43-113">The [**WM\_NCCREATE**](wm-nccreate.md) message is sent just after your window is created, but if an application responds to this message by returning **FALSE**, [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function fails.</span></span> <span data-ttu-id="32f43-114">Le message [**WM \_ Create**](wm-create.md) est envoyé une fois que votre fenêtre a déjà été créée.</span><span class="sxs-lookup"><span data-stu-id="32f43-114">The [**WM\_CREATE**](wm-create.md) message is sent after your window is already created.</span></span>

<span data-ttu-id="32f43-115">Le message [**WM \_ Destroy**](wm-destroy.md) est envoyé lorsque votre fenêtre est sur le lieu d’être détruite.</span><span class="sxs-lookup"><span data-stu-id="32f43-115">The [**WM\_DESTROY**](wm-destroy.md) message is sent when your window is about to be destroyed.</span></span> <span data-ttu-id="32f43-116">La fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) s’occupe de détruire les fenêtres enfants de la fenêtre en cours de destruction.</span><span class="sxs-lookup"><span data-stu-id="32f43-116">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function takes care of destroying any child windows of the window being destroyed.</span></span> <span data-ttu-id="32f43-117">Le message [**WM \_ NCDESTROY**](wm-ncdestroy.md) est envoyé juste avant la destruction d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="32f43-117">The [**WM\_NCDESTROY**](wm-ncdestroy.md) message is sent just before a window is destroyed.</span></span>

<span data-ttu-id="32f43-118">Au minimum, une procédure de fenêtre doit traiter le message [**de \_ peinture WM**](../gdi/wm-paint.md) pour se dessiner lui-même.</span><span class="sxs-lookup"><span data-stu-id="32f43-118">At the very least, a window procedure should process the [**WM\_PAINT**](../gdi/wm-paint.md) message to draw itself.</span></span> <span data-ttu-id="32f43-119">En règle générale, il doit également gérer les messages de souris et de clavier.</span><span class="sxs-lookup"><span data-stu-id="32f43-119">Typically, it should handle mouse and keyboard messages as well.</span></span> <span data-ttu-id="32f43-120">Consultez les descriptions des messages individuels pour déterminer si votre procédure de fenêtre doit les gérer.</span><span class="sxs-lookup"><span data-stu-id="32f43-120">Consult the descriptions of individual messages to determine whether your window procedure should handle them.</span></span>

<span data-ttu-id="32f43-121">Votre application peut appeler la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dans le cadre du traitement d’un message.</span><span class="sxs-lookup"><span data-stu-id="32f43-121">Your application can call the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as part of the processing of a message.</span></span> <span data-ttu-id="32f43-122">Dans ce cas, l’application peut modifier les paramètres de message avant de transmettre le message à **DefWindowProc**, ou elle peut poursuivre le traitement par défaut après avoir effectué ses propres opérations.</span><span class="sxs-lookup"><span data-stu-id="32f43-122">In such a case, the application can modify the message parameters before passing the message to **DefWindowProc**, or it can continue with the default processing after performing its own operations.</span></span>

<span data-ttu-id="32f43-123">Une procédure de boîte de dialogue reçoit un message [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) au lieu d’un message [**WM \_ Create**](wm-create.md) et ne passe pas de messages non traités à la fonction [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="32f43-123">A dialog box procedure receives a [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message instead of a [**WM\_CREATE**](wm-create.md) message and does not pass unprocessed messages to the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="32f43-124">Dans le cas contraire, une procédure de boîte de dialogue est exactement la même qu’une procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="32f43-124">Otherwise, a dialog box procedure is exactly the same as a window procedure.</span></span>

## <a name="associating-a-window-procedure-with-a-window-class"></a><span data-ttu-id="32f43-125">Association d’une procédure de fenêtre à une classe de fenêtre</span><span class="sxs-lookup"><span data-stu-id="32f43-125">Associating a Window Procedure with a Window Class</span></span>

<span data-ttu-id="32f43-126">Vous associez une procédure de fenêtre à une classe de fenêtre lors de l’inscription de la classe.</span><span class="sxs-lookup"><span data-stu-id="32f43-126">You associate a window procedure with a window class when registering the class.</span></span> <span data-ttu-id="32f43-127">Vous devez remplir une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) avec des informations sur la classe, et le membre **lpfnWndProc** doit spécifier l’adresse de la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="32f43-127">You must fill a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure with information about the class, and the **lpfnWndProc** member must specify the address of the window procedure.</span></span> <span data-ttu-id="32f43-128">Pour inscrire la classe, transmettez l’adresse de la structure **WNDCLASS** à la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="32f43-128">To register the class, pass the address of **WNDCLASS** structure to the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="32f43-129">Une fois la classe de fenêtre inscrite, la procédure de fenêtre est automatiquement associée à chaque nouvelle fenêtre créée avec cette classe.</span><span class="sxs-lookup"><span data-stu-id="32f43-129">After the window class has been registered, the window procedure is automatically associated with each new window created with that class.</span></span>

<span data-ttu-id="32f43-130">L’exemple suivant montre comment associer la procédure de fenêtre de l’exemple précédent à une classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="32f43-130">The following example shows how to associate the window procedure in the previous example with a window class.</span></span>


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



## <a name="subclassing-a-window"></a><span data-ttu-id="32f43-131">Sous-classement d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="32f43-131">Subclassing a Window</span></span>

<span data-ttu-id="32f43-132">Pour sous-classer une instance d’une fenêtre, appelez la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) et spécifiez le descripteur de la fenêtre pour sous-classer l' \_ indicateur WNDPROC GWL et un pointeur vers la procédure de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="32f43-132">To subclass an instance of a window, call the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function and specify the handle to the window to subclass the GWL\_WNDPROC flag and a pointer to the subclass procedure.</span></span> <span data-ttu-id="32f43-133">**SetWindowLong** retourne un pointeur vers la procédure de fenêtre d’origine ; Utilisez ce pointeur pour passer des messages à la procédure d’origine.</span><span class="sxs-lookup"><span data-stu-id="32f43-133">**SetWindowLong** returns a pointer to the original window procedure; use this pointer to pass messages to the original procedure.</span></span> <span data-ttu-id="32f43-134">La procédure de fenêtre de la sous-classe doit utiliser la fonction [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) pour appeler la procédure de fenêtre d’origine.</span><span class="sxs-lookup"><span data-stu-id="32f43-134">The subclass window procedure must use the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function to call the original window procedure.</span></span>

> [!Note]  
> <span data-ttu-id="32f43-135">Pour écrire du code compatible avec les versions 32 bits et 64 bits de Windows, utilisez la fonction [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .</span><span class="sxs-lookup"><span data-stu-id="32f43-135">To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function.</span></span>

 

<span data-ttu-id="32f43-136">L’exemple suivant montre comment sous-classer une instance d’un contrôle d’édition dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="32f43-136">The following example shows how to subclass an instance of an edit control in a dialog box.</span></span> <span data-ttu-id="32f43-137">La procédure de fenêtre de la sous-classe permet au contrôle d’édition de recevoir toutes les entrées au clavier, y compris les touches entrée et tabulation, chaque fois que le contrôle a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="32f43-137">The subclass window procedure enables the edit control to receive all keyboard input, including the ENTER and TAB keys, whenever the control has the input focus.</span></span>


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



 

 
