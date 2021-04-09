---
description: Les exemples de cette section décrivent comment effectuer des tâches associées à l’utilisation de Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Utilisation de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867989"
---
# <a name="using-windows"></a><span data-ttu-id="5a8a5-103">Utilisation de Windows</span><span class="sxs-lookup"><span data-stu-id="5a8a5-103">Using Windows</span></span>

<span data-ttu-id="5a8a5-104">Les exemples de cette section décrivent comment effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a8a5-104">The examples in this section describe how to perform the following tasks:</span></span>

-   [<span data-ttu-id="5a8a5-105">Création d’une fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="5a8a5-105">Creating a Main Window</span></span>](#creating-a-main-window)
-   [<span data-ttu-id="5a8a5-106">Création, énumération et dimensionnement des fenêtres enfants</span><span class="sxs-lookup"><span data-stu-id="5a8a5-106">Creating, Enumerating, and Sizing Child Windows</span></span>](#creating-enumerating-and-sizing-child-windows)
-   [<span data-ttu-id="5a8a5-107">Destruction d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="5a8a5-107">Destroying a Window</span></span>](#destroying-a-window)
-   [<span data-ttu-id="5a8a5-108">Utilisation des fenêtres superposées</span><span class="sxs-lookup"><span data-stu-id="5a8a5-108">Using Layered Windows</span></span>](#using-layered-windows)

## <a name="creating-a-main-window"></a><span data-ttu-id="5a8a5-109">Création d’une fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="5a8a5-109">Creating a Main Window</span></span>

<span data-ttu-id="5a8a5-110">La première fenêtre créée par une application est généralement la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-110">The first window an application creates is typically the main window.</span></span> <span data-ttu-id="5a8a5-111">Vous créez la fenêtre principale à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre, le nom de la fenêtre, les styles de fenêtre, la taille, la position, le handle de menu, le handle d’instance et les données de création.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-111">You create the main window by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function, specifying the window class, window name, window styles, size, position, menu handle, instance handle, and creation data.</span></span> <span data-ttu-id="5a8a5-112">Une fenêtre principale appartient à une classe de fenêtre définie par l’application. vous devez donc inscrire la classe de fenêtre et fournir une procédure de fenêtre pour la classe avant de créer la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-112">A main window belongs to an application-defined window class, so you must register the window class and provide a window procedure for the class before creating the main window.</span></span>

<span data-ttu-id="5a8a5-113">La plupart des applications utilisent généralement le style [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) pour créer la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-113">Most applications typically use the [**WS\_OVERLAPPEDWINDOW**](window-styles.md) style to create the main window.</span></span> <span data-ttu-id="5a8a5-114">Ce style donne à la fenêtre une barre de titre, un menu fenêtre, une bordure de redimensionnement et des boutons réduire et agrandir.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-114">This style gives the window a title bar, a window menu, a sizing border, and minimize and maximize buttons.</span></span> <span data-ttu-id="5a8a5-115">La fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retourne un handle qui identifie de façon unique la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-115">The [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function returns a handle that uniquely identifies the window.</span></span>

<span data-ttu-id="5a8a5-116">L’exemple suivant crée une fenêtre principale appartenant à une classe de fenêtre définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-116">The following example creates a main window belonging to an application-defined window class.</span></span> <span data-ttu-id="5a8a5-117">Le nom de la fenêtre, **fenêtre principale**, s’affiche dans la barre de titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-117">The window name, **Main Window**, will appear in the window's title bar.</span></span> <span data-ttu-id="5a8a5-118">En combinant les [**styles \_ WS VSCROLL**](window-styles.md) et **WS \_ HSCROLL** avec le style **WS \_ OVERLAPPEDWINDOW** , l’application crée une fenêtre principale avec des barres de défilement horizontale et verticale en plus des composants fournis par le style **WS \_ OVERLAPPEDWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="5a8a5-118">By combining the [**WS\_VSCROLL**](window-styles.md) and **WS\_HSCROLL** styles with the **WS\_OVERLAPPEDWINDOW** style, the application creates a main window with horizontal and vertical scroll bars in addition to the components provided by the **WS\_OVERLAPPEDWINDOW** style.</span></span> <span data-ttu-id="5a8a5-119">Les quatre occurrences de la **constante \_ usedefault en PV** définissent la taille initiale et la position de la fenêtre en fonction des valeurs par défaut définies par le système.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-119">The four occurrences of the **CW\_USEDEFAULT** constant set the initial size and position of the window to the system-defined default values.</span></span> <span data-ttu-id="5a8a5-120">En spécifiant la **valeur null** au lieu d’un handle de menu, le menu est défini pour la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-120">By specifying **NULL** instead of a menu handle, the window will have the menu defined for the window class.</span></span>


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



<span data-ttu-id="5a8a5-121">Notez que l’exemple précédent appelle la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) après la création de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-121">Notice that the preceding example calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function after creating the main window.</span></span> <span data-ttu-id="5a8a5-122">Cela est dû au fait que le système n’affiche pas automatiquement la fenêtre principale après l’avoir créée.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-122">This is done because the system does not automatically display the main window after creating it.</span></span> <span data-ttu-id="5a8a5-123">En passant l’indicateur **SW \_ SHOWDEFAULT** à **ShowWindow**, l’application autorise le programme qui a démarré l’application à définir l’état d’affichage initial de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-123">By passing the **SW\_SHOWDEFAULT** flag to **ShowWindow**, the application allows the program that started the application to set the initial show state of the main window.</span></span> <span data-ttu-id="5a8a5-124">La fonction [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) envoie la fenêtre à son premier message [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="5a8a5-124">The [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) function sends the window its first [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span>

## <a name="creating-enumerating-and-sizing-child-windows"></a><span data-ttu-id="5a8a5-125">Création, énumération et dimensionnement des fenêtres enfants</span><span class="sxs-lookup"><span data-stu-id="5a8a5-125">Creating, Enumerating, and Sizing Child Windows</span></span>

<span data-ttu-id="5a8a5-126">Vous pouvez diviser la zone cliente d’une fenêtre en différentes zones fonctionnelles à l’aide de fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-126">You can divide a window's client area into different functional areas by using child windows.</span></span> <span data-ttu-id="5a8a5-127">La création d’une fenêtre enfant est semblable à la création d’une fenêtre principale : vous utilisez la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="5a8a5-127">Creating a child window is like creating a main window—you use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="5a8a5-128">Pour créer une fenêtre d’une classe de fenêtre définie par l’application, vous devez inscrire la classe de fenêtre et fournir une procédure de fenêtre avant de créer la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-128">To create a window of an application-defined window class, you must register the window class and provide a window procedure before creating the child window.</span></span> <span data-ttu-id="5a8a5-129">Vous devez attribuer à la fenêtre enfant le style [**WS \_ Child**](window-styles.md) et spécifier une fenêtre parente pour la fenêtre enfant lorsque vous la créez.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-129">You must give the child window the [**WS\_CHILD**](window-styles.md) style and specify a parent window for the child window when you create it.</span></span>

<span data-ttu-id="5a8a5-130">L’exemple suivant divise la zone cliente de la fenêtre principale d’une application en trois zones fonctionnelles en créant trois fenêtres enfants de taille égale.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-130">The following example divides the client area of an application's main window into three functional areas by creating three child windows of equal size.</span></span> <span data-ttu-id="5a8a5-131">Chaque fenêtre enfant a la même hauteur que la zone cliente de la fenêtre principale, mais la largeur de chaque fenêtre est égale à un tiers.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-131">Each child window is the same height as the main window's client area, but each is one-third its width.</span></span> <span data-ttu-id="5a8a5-132">La fenêtre principale crée les fenêtres enfants en réponse au message [**WM \_ Create**](wm-create.md) , que la fenêtre principale reçoit au cours de son propre processus de création de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-132">The main window creates the child windows in response to the [**WM\_CREATE**](wm-create.md) message, which the main window receives during its own window-creation process.</span></span> <span data-ttu-id="5a8a5-133">Étant donné que chaque fenêtre enfant a le style de [**\_ bordure WS**](window-styles.md) , chacun a une bordure de trait fine.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-133">Because each child window has the [**WS\_BORDER**](window-styles.md) style, each has a thin line border.</span></span> <span data-ttu-id="5a8a5-134">En outre, étant donné que le style **\_ visible de WS** n’est pas spécifié, chaque fenêtre enfant est initialement masquée.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-134">Also, because the **WS\_VISIBLE** style is not specified, each child window is initially hidden.</span></span> <span data-ttu-id="5a8a5-135">Notez également que chaque fenêtre enfant est assignée à un identificateur de fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-135">Notice also that each child window is assigned a child-window identifier.</span></span>

<span data-ttu-id="5a8a5-136">La fenêtre principale dimensionne et positionne les fenêtres enfants en réponse au message [**de \_ taille WM**](wm-size.md) , que la fenêtre principale reçoit lorsque sa taille change.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-136">The main window sizes and positions the child windows in response to the [**WM\_SIZE**](wm-size.md) message, which the main window receives when its size changes.</span></span> <span data-ttu-id="5a8a5-137">En réponse à **la \_ taille de WM**, la fenêtre principale récupère les dimensions de sa zone cliente à l’aide de la fonction [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) , puis passe les dimensions à la fonction [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) .</span><span class="sxs-lookup"><span data-stu-id="5a8a5-137">In response to **WM\_SIZE**, the main window retrieves the dimensions of its client area by using the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function and then passes the dimensions to the [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) function.</span></span> <span data-ttu-id="5a8a5-138">**EnumChildWindows** transmet le descripteur à chaque fenêtre enfant, à son tour, à la fonction de rappel [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-138">**EnumChildWindows** passes the handle to each child window, in turn, to the application-defined [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) callback function.</span></span> <span data-ttu-id="5a8a5-139">Cette fonction dimensionne et positionne chaque fenêtre enfant en appelant la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) ; la taille et la position sont basées sur les dimensions de la zone cliente de la fenêtre principale et l’identificateur de la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-139">This function sizes and positions each child window by calling the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function; the size and position are based on the dimensions of the main window's client area and the identifier of the child window.</span></span> <span data-ttu-id="5a8a5-140">Ensuite, **EnumChildProc** appelle la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) pour rendre la fenêtre visible.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-140">Afterward, **EnumChildProc** calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function to make the window visible.</span></span>


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



## <a name="destroying-a-window"></a><span data-ttu-id="5a8a5-141">Destruction d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="5a8a5-141">Destroying a Window</span></span>

<span data-ttu-id="5a8a5-142">Vous pouvez utiliser la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) pour détruire une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-142">You can use the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy a window.</span></span> <span data-ttu-id="5a8a5-143">En règle générale, une application envoie le message de [**\_ fermeture WM**](wm-close.md) avant de détruire une fenêtre, donnant à la fenêtre la possibilité de demander confirmation à l’utilisateur avant la destruction de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-143">Typically, an application sends the [**WM\_CLOSE**](wm-close.md) message before destroying a window, giving the window the opportunity to prompt the user for confirmation before the window is destroyed.</span></span> <span data-ttu-id="5a8a5-144">Une fenêtre qui comprend un menu fenêtre reçoit automatiquement le message **WM \_ Close** quand l’utilisateur clique sur **Fermer** dans le menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-144">A window that includes a window menu automatically receives the **WM\_CLOSE** message when the user clicks **Close** from the window menu.</span></span> <span data-ttu-id="5a8a5-145">Si l’utilisateur confirme que la fenêtre doit être détruite, l’application appelle **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-145">If the user confirms that the window should be destroyed, the application calls **DestroyWindow**.</span></span> <span data-ttu-id="5a8a5-146">Le système envoie le message de [**\_ destruction WM**](wm-destroy.md) à la fenêtre après l’avoir supprimé de l’écran.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-146">The system sends the [**WM\_DESTROY**](wm-destroy.md) message to the window after removing it from the screen.</span></span> <span data-ttu-id="5a8a5-147">En réponse à **la \_ destruction de WM**, la fenêtre enregistre ses données et libère toutes les ressources qu’elle a allouées.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-147">In response to **WM\_DESTROY**, the window saves its data and frees any resources it allocated.</span></span> <span data-ttu-id="5a8a5-148">Une fenêtre principale conclut son traitement de **WM \_ Destroy** en appelant la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) pour quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-148">A main window concludes its processing of **WM\_DESTROY** by calling the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to quit the application.</span></span>

<span data-ttu-id="5a8a5-149">L’exemple suivant montre comment demander la confirmation de l’utilisateur avant de détruire une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-149">The following example shows how to prompt for user confirmation before destroying a window.</span></span> <span data-ttu-id="5a8a5-150">En réponse à [**la \_ fermeture de WM**](wm-close.md), l’exemple affiche une boîte de dialogue qui contient les boutons **Oui**, **non** et **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="5a8a5-150">In response to [**WM\_CLOSE**](wm-close.md), the example displays a dialog box that contains **Yes**, **No**, and **Cancel** buttons.</span></span> <span data-ttu-id="5a8a5-151">Si l’utilisateur clique sur **Oui**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) est appelé ; dans le cas contraire, la fenêtre n’est pas détruite.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-151">If the user clicks **Yes**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) is called; otherwise, the window is not destroyed.</span></span> <span data-ttu-id="5a8a5-152">Étant donné que la fenêtre en cours de destruction est une fenêtre principale, l’exemple appelle [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) en réponse à [**WM \_ Destroy**](wm-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="5a8a5-152">Because the window being destroyed is a main window, the example calls [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in response to [**WM\_DESTROY**](wm-destroy.md).</span></span>


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



## <a name="using-layered-windows"></a><span data-ttu-id="5a8a5-153">Utilisation des fenêtres superposées</span><span class="sxs-lookup"><span data-stu-id="5a8a5-153">Using Layered Windows</span></span>

<span data-ttu-id="5a8a5-154">Pour qu’une boîte de dialogue s’impose en tant que fenêtre translucide, commencez par créer la boîte de dialogue comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-154">To have a dialog box come up as a translucent window, first create the dialog as usual.</span></span> <span data-ttu-id="5a8a5-155">Ensuite, sur [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), définissez le bit de couche du style étendu de la fenêtre et appelez [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) avec la valeur alpha souhaitée.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-155">Then, on [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md), set the layered bit of the window's extended style and call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) with the desired alpha value.</span></span> <span data-ttu-id="5a8a5-156">Le code peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="5a8a5-156">The code might look like this:</span></span>


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



<span data-ttu-id="5a8a5-157">Notez que le troisième paramètre de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) est une valeur comprise entre 0 et 255, avec 0 pour rendre la fenêtre complètement transparente et 255 la rendre entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-157">Note that the third parameter of [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) is a value that ranges from 0 to 255, with 0 making the window completely transparent and 255 making it completely opaque.</span></span> <span data-ttu-id="5a8a5-158">Ce paramètre imite le [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) plus polyvalent de la fonction [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="5a8a5-158">This parameter mimics the more versatile [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) of the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>

<span data-ttu-id="5a8a5-159">Pour que cette fenêtre soit complètement opaque, supprimez le bit de **\_ \_ couche WS ex** en appelant [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , puis demandez à la fenêtre de repeindre.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-159">To make this window completely opaque again, remove the **WS\_EX\_LAYERED** bit by calling [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) and then ask the window to repaint.</span></span> <span data-ttu-id="5a8a5-160">La suppression du bit est souhaitée pour permettre au système de savoir qu’il peut libérer de la mémoire associée à la superposition et à la redirection.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-160">Removing the bit is desired to let the system know that it can free up some memory associated with layering and redirection.</span></span> <span data-ttu-id="5a8a5-161">Le code peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="5a8a5-161">The code might look like this:</span></span>


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



<span data-ttu-id="5a8a5-162">Pour pouvoir utiliser des fenêtres enfants superposées, l’application doit déclarer elle-même Windows 8 dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="5a8a5-162">In order to use layered child windows, the application has to declare itself Windows 8-aware in the manifest.</span></span>

 

 
