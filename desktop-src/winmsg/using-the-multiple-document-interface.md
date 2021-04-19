---
description: Cette section explique comment effectuer des tâches associées à l’interface multidocument.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Utilisation de l’interface multidocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535579"
---
# <a name="using-the-multiple-document-interface"></a><span data-ttu-id="00cef-103">Utilisation de l’interface multidocument</span><span class="sxs-lookup"><span data-stu-id="00cef-103">Using the Multiple Document Interface</span></span>

<span data-ttu-id="00cef-104">Cette section explique comment effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="00cef-104">This section explains how to perform the following tasks:</span></span>

-   [<span data-ttu-id="00cef-105">Inscription des classes de fenêtre frame et enfant</span><span class="sxs-lookup"><span data-stu-id="00cef-105">Registering Child and Frame Window Classes</span></span>](#registering-child-and-frame-window-classes)
-   [<span data-ttu-id="00cef-106">Création de fenêtres Frame et enfants</span><span class="sxs-lookup"><span data-stu-id="00cef-106">Creating Frame and Child Windows</span></span>](#creating-frame-and-child-windows)
-   [<span data-ttu-id="00cef-107">Écriture de la boucle de message principale</span><span class="sxs-lookup"><span data-stu-id="00cef-107">Writing the Main Message Loop</span></span>](#writing-the-main-message-loop)
-   [<span data-ttu-id="00cef-108">Écriture de la procédure de fenêtre frame</span><span class="sxs-lookup"><span data-stu-id="00cef-108">Writing the Frame Window Procedure</span></span>](#writing-the-frame-window-procedure)
-   [<span data-ttu-id="00cef-109">Écriture de la procédure de fenêtre enfant</span><span class="sxs-lookup"><span data-stu-id="00cef-109">Writing the Child Window Procedure</span></span>](#writing-the-child-window-procedure)
-   [<span data-ttu-id="00cef-110">Création d’une fenêtre enfant</span><span class="sxs-lookup"><span data-stu-id="00cef-110">Creating a Child Window</span></span>](#creating-a-child-window)

<span data-ttu-id="00cef-111">Pour illustrer ces tâches, cette section comprend des exemples de MULTIPAD, une application classique d’interface multidocument (MDI, multiple-document interface).</span><span class="sxs-lookup"><span data-stu-id="00cef-111">To illustrate these tasks, this section includes examples from Multipad, a typical multiple-document interface (MDI) application.</span></span>

## <a name="registering-child-and-frame-window-classes"></a><span data-ttu-id="00cef-112">Inscription des classes de fenêtre frame et enfant</span><span class="sxs-lookup"><span data-stu-id="00cef-112">Registering Child and Frame Window Classes</span></span>

<span data-ttu-id="00cef-113">Une application MDI classique doit inscrire deux classes de fenêtres : une pour sa fenêtre frame et une pour ses fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="00cef-113">A typical MDI application must register two window classes: one for its frame window and one for its child windows.</span></span> <span data-ttu-id="00cef-114">Si une application prend en charge plusieurs types de document (par exemple, une feuille de calcul et un graphique), elle doit inscrire une classe de fenêtre pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="00cef-114">If an application supports more than one type of document (for example, a spreadsheet and a chart), it must register a window class for each type.</span></span>

<span data-ttu-id="00cef-115">La structure de classe de la fenêtre frame est semblable à celle de la fenêtre principale dans les applications non-MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-115">The class structure for the frame window is similar to the class structure for the main window in non–MDI applications.</span></span> <span data-ttu-id="00cef-116">La structure de la classe pour les fenêtres enfants MDI diffère légèrement de la structure des fenêtres enfants dans les applications non-MDI, comme suit :</span><span class="sxs-lookup"><span data-stu-id="00cef-116">The class structure for the MDI child windows differs slightly from the structure for child windows in non–MDI applications as follows:</span></span>

-   <span data-ttu-id="00cef-117">La structure de la classe doit avoir une icône, car l’utilisateur peut réduire une fenêtre enfant MDI comme s’il s’agissait d’une fenêtre d’application normale.</span><span class="sxs-lookup"><span data-stu-id="00cef-117">The class structure should have an icon, because the user can minimize an MDI child window as if it were a normal application window.</span></span>
-   <span data-ttu-id="00cef-118">Le nom du menu doit avoir la **valeur null**, car une fenêtre enfant MDI ne peut pas avoir son propre menu.</span><span class="sxs-lookup"><span data-stu-id="00cef-118">The menu name should be **NULL**, because an MDI child window cannot have its own menu.</span></span>
-   <span data-ttu-id="00cef-119">La structure de la classe doit réserver de l’espace supplémentaire dans la structure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00cef-119">The class structure should reserve extra space in the window structure.</span></span> <span data-ttu-id="00cef-120">Avec cet espace, l’application peut associer des données, telles qu’un nom de fichier, à une fenêtre enfant particulière.</span><span class="sxs-lookup"><span data-stu-id="00cef-120">With this space, the application can associate data, such as a filename, with a particular child window.</span></span>

<span data-ttu-id="00cef-121">L’exemple suivant montre comment MULTIPAD inscrit son frame et les classes de fenêtre enfants.</span><span class="sxs-lookup"><span data-stu-id="00cef-121">The following example shows how Multipad registers its frame and child window classes.</span></span>


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a><span data-ttu-id="00cef-122">Création de fenêtres Frame et enfants</span><span class="sxs-lookup"><span data-stu-id="00cef-122">Creating Frame and Child Windows</span></span>

<span data-ttu-id="00cef-123">Après avoir inscrit ses classes de fenêtre, une application MDI peut créer ses fenêtres.</span><span class="sxs-lookup"><span data-stu-id="00cef-123">After registering its window classes, an MDI application can create its windows.</span></span> <span data-ttu-id="00cef-124">Tout d’abord, elle crée sa fenêtre frame à l’aide de la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="00cef-124">First, it creates its frame window by using the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="00cef-125">Après avoir créé sa fenêtre frame, l’application crée à nouveau sa fenêtre cliente à l’aide de **CreateWindow** ou de **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="00cef-125">After creating its frame window, the application creates its client window, again by using **CreateWindow** or **CreateWindowEx**.</span></span> <span data-ttu-id="00cef-126">L’application doit spécifier MDICLIENT comme nom de classe de la fenêtre cliente ; **MdiClient** est une classe de fenêtre préinscrite définie par le système.</span><span class="sxs-lookup"><span data-stu-id="00cef-126">The application should specify MDICLIENT as the client window's class name; **MDICLIENT** is a preregistered window class defined by the system.</span></span> <span data-ttu-id="00cef-127">Le paramètre *lpvParam* de **CreateWindow** ou **CreateWindowEx** doit pointer vers une structure [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) .</span><span class="sxs-lookup"><span data-stu-id="00cef-127">The *lpvParam* parameter of **CreateWindow** or **CreateWindowEx** should point to a [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) structure.</span></span> <span data-ttu-id="00cef-128">Cette structure contient les membres décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="00cef-128">This structure contains the members described in the following table:</span></span>



| <span data-ttu-id="00cef-129">Membre</span><span class="sxs-lookup"><span data-stu-id="00cef-129">Member</span></span>           | <span data-ttu-id="00cef-130">Description</span><span class="sxs-lookup"><span data-stu-id="00cef-130">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00cef-131">**hWindowMenu**</span><span class="sxs-lookup"><span data-stu-id="00cef-131">**hWindowMenu**</span></span>  | <span data-ttu-id="00cef-132">Handle vers le menu fenêtre utilisé pour contrôler les fenêtres enfants MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-132">Handle to the window menu used for controlling MDI child windows.</span></span> <span data-ttu-id="00cef-133">Lorsque les fenêtres enfants sont créées, l’application ajoute leurs titres au menu fenêtre en tant qu’éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="00cef-133">As child windows are created, the application adds their titles to the window menu as menu items.</span></span> <span data-ttu-id="00cef-134">L’utilisateur peut ensuite activer une fenêtre enfant en cliquant sur son titre dans le menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00cef-134">The user can then activate a child window by clicking its title on the window menu.</span></span>                                                               |
| <span data-ttu-id="00cef-135">**idFirstChild**</span><span class="sxs-lookup"><span data-stu-id="00cef-135">**idFirstChild**</span></span> | <span data-ttu-id="00cef-136">Spécifie l’identificateur de la première fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-136">Specifies the identifier of the first MDI child window.</span></span> <span data-ttu-id="00cef-137">Cet identificateur est affecté à la première fenêtre enfant MDI créée.</span><span class="sxs-lookup"><span data-stu-id="00cef-137">The first MDI child window created is assigned this identifier.</span></span> <span data-ttu-id="00cef-138">Des fenêtres supplémentaires sont créées avec des identificateurs de fenêtre incrémentés.</span><span class="sxs-lookup"><span data-stu-id="00cef-138">Additional windows are created with incremented window identifiers.</span></span> <span data-ttu-id="00cef-139">Quand une fenêtre enfant est détruite, le système réaffecte immédiatement les identificateurs de fenêtre pour maintenir la plage contiguë.</span><span class="sxs-lookup"><span data-stu-id="00cef-139">When a child window is destroyed, the system immediately reassigns the window identifiers to keep their range contiguous.</span></span> |



 

<span data-ttu-id="00cef-140">Quand le titre d’une fenêtre enfant est ajouté au menu fenêtre, le système assigne un identificateur à la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="00cef-140">When a child window's title is added to the window menu, the system assigns an identifier to the child window.</span></span> <span data-ttu-id="00cef-141">Quand l’utilisateur clique sur le titre d’une fenêtre enfant, la fenêtre frame reçoit un message de [**\_ commande WM**](../menurc/wm-command.md) avec l’identificateur dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="00cef-141">When the user clicks a child window's title, the frame window receives a [**WM\_COMMAND**](../menurc/wm-command.md) message with the identifier in the *wParam* parameter.</span></span> <span data-ttu-id="00cef-142">Vous devez spécifier une valeur pour le membre **idFirstChild** qui n’est pas en conflit avec les identificateurs d’élément de menu dans le menu de la fenêtre frame.</span><span class="sxs-lookup"><span data-stu-id="00cef-142">You should specify a value for the **idFirstChild** member that does not conflict with menu-item identifiers in the frame window's menu.</span></span>

<span data-ttu-id="00cef-143">La procédure de fenêtre frame de MULTIPAD crée la fenêtre cliente MDI lors du traitement du message [**WM \_ Create**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="00cef-143">Multipad's frame window procedure creates the MDI client window while processing the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="00cef-144">L’exemple suivant montre comment la fenêtre cliente est créée.</span><span class="sxs-lookup"><span data-stu-id="00cef-144">The following example shows how the client window is created.</span></span>


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



<span data-ttu-id="00cef-145">Les titres des fenêtres enfants sont ajoutés au bas du menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00cef-145">Titles of child windows are added to the bottom of the window menu.</span></span> <span data-ttu-id="00cef-146">Si l’application ajoute des chaînes au menu fenêtre à l’aide de la fonction [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , ces chaînes peuvent être remplacées par les titres des fenêtres enfants lorsque le menu fenêtre est repeint (chaque fois qu’une fenêtre enfant est créée ou détruite).</span><span class="sxs-lookup"><span data-stu-id="00cef-146">If the application adds strings to the window menu by using the [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function, these strings can be overwritten by the titles of the child windows when the window menu is repainted (whenever a child window is created or destroyed).</span></span> <span data-ttu-id="00cef-147">Une application MDI qui ajoute des chaînes à son menu fenêtre doit utiliser la fonction [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) et vérifier que les titres des fenêtres enfants n’ont pas remplacé ces nouvelles chaînes.</span><span class="sxs-lookup"><span data-stu-id="00cef-147">An MDI application that adds strings to its window menu should use the [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) function and verify that the titles of child windows have not overwritten these new strings.</span></span>

<span data-ttu-id="00cef-148">Utilisez le style **WS \_ CLIPCHILDREN** pour créer la fenêtre cliente MDI afin d’empêcher la fenêtre de se peindre sur ses fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="00cef-148">Use the **WS\_CLIPCHILDREN** style to create the MDI client window to prevent the window from painting over its child windows.</span></span>

## <a name="writing-the-main-message-loop"></a><span data-ttu-id="00cef-149">Écriture de la boucle de message principale</span><span class="sxs-lookup"><span data-stu-id="00cef-149">Writing the Main Message Loop</span></span>

<span data-ttu-id="00cef-150">La boucle de messages principale d’une application MDI est semblable à celle des touches accélérateur de gestion d’applications non-MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-150">The main message loop of an MDI application is similar to that of a non-MDI application handling accelerator keys.</span></span> <span data-ttu-id="00cef-151">La différence est que la boucle de message MDI appelle la fonction [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) avant de vérifier les clés d’accélérateur définies par l’application ou avant de distribuer le message.</span><span class="sxs-lookup"><span data-stu-id="00cef-151">The difference is that the MDI message loop calls the [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function before checking for application-defined accelerator keys or before dispatching the message.</span></span>

<span data-ttu-id="00cef-152">L’exemple suivant illustre la boucle de message d’une application MDI classique.</span><span class="sxs-lookup"><span data-stu-id="00cef-152">The following example shows the message loop of a typical MDI application.</span></span> <span data-ttu-id="00cef-153">Notez que [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) peut retourner-1 en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="00cef-153">Note that [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) can return -1 if there is an error.</span></span>


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



<span data-ttu-id="00cef-154">La fonction [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) traduit les messages de KeyOut [**WM \_**](../inputdev/wm-keydown.md) en messages [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) et les envoie à la fenêtre enfant MDI active.</span><span class="sxs-lookup"><span data-stu-id="00cef-154">The [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function translates [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) messages into [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) messages and sends them to the active MDI child window.</span></span> <span data-ttu-id="00cef-155">Si le message n’est pas un message d’accélérateur MDI, la fonction retourne **false**. dans ce cas, l’application utilise la fonction [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) pour déterminer si l’une des touches accélérateur définies par l’application a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="00cef-155">If the message is not an MDI accelerator message, the function returns **FALSE**, in which case the application uses the [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function to determine whether any of the application-defined accelerator keys were pressed.</span></span> <span data-ttu-id="00cef-156">Si ce n’est pas le cas, la boucle distribue le message à la procédure de fenêtre appropriée.</span><span class="sxs-lookup"><span data-stu-id="00cef-156">If not, the loop dispatches the message to the appropriate window procedure.</span></span>

## <a name="writing-the-frame-window-procedure"></a><span data-ttu-id="00cef-157">Écriture de la procédure de fenêtre frame</span><span class="sxs-lookup"><span data-stu-id="00cef-157">Writing the Frame Window Procedure</span></span>

<span data-ttu-id="00cef-158">La procédure de fenêtre pour une fenêtre frame MDI est semblable à celle d’une fenêtre principale d’une application non-MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-158">The window procedure for an MDI frame window is similar to that of a non–MDI application's main window.</span></span> <span data-ttu-id="00cef-159">La différence est qu’une procédure de fenêtre frame transmet tous les messages qu’elle ne gère pas à la fonction [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) plutôt qu’à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="00cef-159">The difference is that a frame window procedure passes all messages it does not handle to the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="00cef-160">En outre, la procédure de fenêtre frame doit également transmettre certains messages qu’elle gère, y compris ceux qui sont listés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="00cef-160">In addition, the frame window procedure must also pass some messages that it does handle, including those listed in the following table.</span></span>



| <span data-ttu-id="00cef-161">Message</span><span class="sxs-lookup"><span data-stu-id="00cef-161">Message</span></span>                                  | <span data-ttu-id="00cef-162">response</span><span class="sxs-lookup"><span data-stu-id="00cef-162">Response</span></span>                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00cef-163">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="00cef-163">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)     | <span data-ttu-id="00cef-164">Active la fenêtre enfant MDI choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="00cef-164">Activates the MDI child window that the user chooses.</span></span> <span data-ttu-id="00cef-165">Ce message est envoyé lorsque l’utilisateur choisit une fenêtre enfant MDI dans le menu fenêtre de la fenêtre frame MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-165">This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window.</span></span> <span data-ttu-id="00cef-166">L’identificateur de fenêtre accompagnant ce message identifie la fenêtre enfant MDI à activer.</span><span class="sxs-lookup"><span data-stu-id="00cef-166">The window identifier accompanying this message identifies the MDI child window to be activated.</span></span> |
| [<span data-ttu-id="00cef-167">**\_MENUCHAR WM**</span><span class="sxs-lookup"><span data-stu-id="00cef-167">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)   | <span data-ttu-id="00cef-168">Ouvre le menu fenêtre de la fenêtre enfant MDI active quand l’utilisateur appuie sur la combinaison de touches ALT + – (moins).</span><span class="sxs-lookup"><span data-stu-id="00cef-168">Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="00cef-169">**WM \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="00cef-169">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md) | <span data-ttu-id="00cef-170">Passe le focus clavier à la fenêtre cliente MDI, qui à son tour la transmet à la fenêtre enfant MDI active.</span><span class="sxs-lookup"><span data-stu-id="00cef-170">Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="00cef-171">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="00cef-171">**WM\_SIZE**</span></span>](wm-size.md)              | <span data-ttu-id="00cef-172">Redimensionne la fenêtre du client MDI pour l’ajuster à la zone cliente de la nouvelle fenêtre frame.</span><span class="sxs-lookup"><span data-stu-id="00cef-172">Resizes the MDI client window to fit in the new frame window's client area.</span></span> <span data-ttu-id="00cef-173">Si la procédure de fenêtre frame dimensionne la fenêtre du client MDI à une taille différente, elle ne doit pas passer le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="00cef-173">If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>                   |



 

<span data-ttu-id="00cef-174">La procédure de fenêtre frame dans MULTIPAD est appelée MPFrameWndProc.</span><span class="sxs-lookup"><span data-stu-id="00cef-174">The frame window procedure in Multipad is called MPFrameWndProc.</span></span> <span data-ttu-id="00cef-175">La gestion d’autres messages par MPFrameWndProc est similaire à celle des applications non-MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-175">The handling of other messages by MPFrameWndProc is similar to that of non–MDI applications.</span></span> <span data-ttu-id="00cef-176">[**WM \_**](../menurc/wm-command.md) Les messages de commande dans MULTIPAD sont gérés par la fonction CommandHandler définie localement.</span><span class="sxs-lookup"><span data-stu-id="00cef-176">[**WM\_COMMAND**](../menurc/wm-command.md) messages in Multipad are handled by the locally defined CommandHandler function.</span></span> <span data-ttu-id="00cef-177">Pour les messages de commande MULTIPAD ne gère pas, CommandHandler appelle la fonction [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) .</span><span class="sxs-lookup"><span data-stu-id="00cef-177">For command messages Multipad does not handle, CommandHandler calls the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function.</span></span> <span data-ttu-id="00cef-178">Si MULTIPAD n’utilise pas **DefFrameProc** par défaut, l’utilisateur ne peut pas activer une fenêtre enfant à partir du menu fenêtre, car le message de **\_ commande WM** envoyé en cliquant sur l’élément de menu de la fenêtre est perdu.</span><span class="sxs-lookup"><span data-stu-id="00cef-178">If Multipad does not use **DefFrameProc** by default, the user can't activate a child window from the window menu, because the **WM\_COMMAND** message sent by clicking the window's menu item would be lost.</span></span>

## <a name="writing-the-child-window-procedure"></a><span data-ttu-id="00cef-179">Écriture de la procédure de fenêtre enfant</span><span class="sxs-lookup"><span data-stu-id="00cef-179">Writing the Child Window Procedure</span></span>

<span data-ttu-id="00cef-180">À l’instar de la procédure de fenêtre frame, une procédure de fenêtre enfant MDI utilise une fonction spéciale pour le traitement des messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="00cef-180">Like the frame window procedure, an MDI child window procedure uses a special function for processing messages by default.</span></span> <span data-ttu-id="00cef-181">Tous les messages que la procédure de fenêtre enfant ne gère pas doivent être passés à la fonction [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) plutôt qu’à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="00cef-181">All messages that the child window procedure does not handle must be passed to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="00cef-182">En outre, certains messages de gestion de fenêtre doivent être transmis à **DefMDIChildProc**, même si l’application gère le message, afin que l’interface MDI fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="00cef-182">In addition, some window-management messages must be passed to **DefMDIChildProc**, even if the application handles the message, in order for MDI to function correctly.</span></span> <span data-ttu-id="00cef-183">Voici les messages que l’application doit passer à **DefMDIChildProc**.</span><span class="sxs-lookup"><span data-stu-id="00cef-183">Following are the messages the application must pass to **DefMDIChildProc**.</span></span>



| <span data-ttu-id="00cef-184">Message</span><span class="sxs-lookup"><span data-stu-id="00cef-184">Message</span></span>                                       | <span data-ttu-id="00cef-185">response</span><span class="sxs-lookup"><span data-stu-id="00cef-185">Response</span></span>                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00cef-186">**\_CHILDACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="00cef-186">**WM\_CHILDACTIVATE**</span></span>](wm-childactivate.md) | <span data-ttu-id="00cef-187">Effectue le traitement de l’activation lorsque les fenêtres enfants MDI sont dimensionnées, déplacées ou affichées.</span><span class="sxs-lookup"><span data-stu-id="00cef-187">Performs activation processing when MDI child windows are sized, moved, or displayed.</span></span> <span data-ttu-id="00cef-188">Ce message doit être transmis.</span><span class="sxs-lookup"><span data-stu-id="00cef-188">This message must be passed.</span></span>                                                                                                                                        |
| [<span data-ttu-id="00cef-189">**\_GETMINMAXINFO WM**</span><span class="sxs-lookup"><span data-stu-id="00cef-189">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md) | <span data-ttu-id="00cef-190">Calcule la taille d’une fenêtre enfant MDI agrandie, en fonction de la taille actuelle de la fenêtre du client MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-190">Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="00cef-191">**\_MENUCHAR WM**</span><span class="sxs-lookup"><span data-stu-id="00cef-191">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)        | <span data-ttu-id="00cef-192">Transmet le message à la fenêtre frame MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-192">Passes the message to the MDI frame window.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="00cef-193">**déplacement de WM \_**</span><span class="sxs-lookup"><span data-stu-id="00cef-193">**WM\_MOVE**</span></span>](wm-move.md)                   | <span data-ttu-id="00cef-194">Recalcule les barres de défilement du client MDI, si elles sont présentes.</span><span class="sxs-lookup"><span data-stu-id="00cef-194">Recalculates MDI client scroll bars, if they are present.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="00cef-195">**WM \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="00cef-195">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)      | <span data-ttu-id="00cef-196">Active la fenêtre enfant, s’il ne s’agit pas de la fenêtre enfant MDI active.</span><span class="sxs-lookup"><span data-stu-id="00cef-196">Activates the child window, if it is not the active MDI child window.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="00cef-197">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="00cef-197">**WM\_SIZE**</span></span>](wm-size.md)                   | <span data-ttu-id="00cef-198">Effectue les opérations nécessaires pour modifier la taille d’une fenêtre, en particulier pour l’optimisation ou la restauration d’une fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-198">Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window.</span></span> <span data-ttu-id="00cef-199">L’échec de la transmission de ce message à la fonction [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) produit des résultats très indésirables.</span><span class="sxs-lookup"><span data-stu-id="00cef-199">Failing to pass this message to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function produces highly undesirable results.</span></span> |
| [<span data-ttu-id="00cef-200">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="00cef-200">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)    | <span data-ttu-id="00cef-201">Commandes de menu de la fenêtre Handles (anciennement « système ») : **SC \_ NEXTWINDOW**, **SC \_ PREVWINDOW**, **SC \_ Move**, **SC \_ Size** et **SC \_ Maximize**.</span><span class="sxs-lookup"><span data-stu-id="00cef-201">Handles window (formerly known as system) menu commands: **SC\_NEXTWINDOW**, **SC\_PREVWINDOW**, **SC\_MOVE**, **SC\_SIZE**, and **SC\_MAXIMIZE**.</span></span>                                                                                                        |



 

## <a name="creating-a-child-window"></a><span data-ttu-id="00cef-202">Création d’une fenêtre enfant</span><span class="sxs-lookup"><span data-stu-id="00cef-202">Creating a Child Window</span></span>

<span data-ttu-id="00cef-203">Pour créer une fenêtre enfant MDI, une application peut appeler la fonction [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) ou envoyer un message [**WM \_ MDICREATE**](wm-mdicreate.md) à la fenêtre cliente MDI.</span><span class="sxs-lookup"><span data-stu-id="00cef-203">To create an MDI child window, an application can either call the [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) function or send an [**WM\_MDICREATE**](wm-mdicreate.md) message to the MDI client window.</span></span> <span data-ttu-id="00cef-204">(L’application peut utiliser la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) avec le style **WS \_ ex \_ MDICHILD** pour créer des fenêtres enfants MDI.) Une application MDI à thread unique peut utiliser l’une ou l’autre méthode pour créer une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="00cef-204">(The application can use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function with the **WS\_EX\_MDICHILD** style to create MDI child windows.) A single-threaded MDI application can use either method to create a child window.</span></span> <span data-ttu-id="00cef-205">Un thread dans une application MDI multithread doit utiliser la fonction **CreateMDIWindow** ou **CreateWindowEx** pour créer une fenêtre enfant dans un thread différent.</span><span class="sxs-lookup"><span data-stu-id="00cef-205">A thread in a multithreaded MDI application must use the **CreateMDIWindow** or **CreateWindowEx** function to create a child window in a different thread.</span></span>

<span data-ttu-id="00cef-206">Le paramètre *lParam* d’un message [**WM \_ MDICREATE**](wm-mdicreate.md) est un pointeur lointain vers une structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="00cef-206">The *lParam* parameter of a [**WM\_MDICREATE**](wm-mdicreate.md) message is a far pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="00cef-207">La structure comprend quatre membres de dimension : **x** et **y**, qui indiquent les positions horizontale et verticale de la fenêtre, et **CX** et **CY**, qui indiquent les étendues horizontale et verticale de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00cef-207">The structure includes four dimension members: **x** and **y**, which indicate the horizontal and vertical positions of the window, and **cx** and **cy**, which indicate the horizontal and vertical extents of the window.</span></span> <span data-ttu-id="00cef-208">Ces membres peuvent être attribués explicitement par l’application, ou ils peuvent être définis sur **CW \_ usedefault**, auquel cas le système sélectionne une position, une taille ou les deux, en fonction d’un algorithme en cascade.</span><span class="sxs-lookup"><span data-stu-id="00cef-208">Any of these members may be assigned explicitly by the application, or they may be set to **CW\_USEDEFAULT**, in which case the system selects a position, size, or both, according to a cascading algorithm.</span></span> <span data-ttu-id="00cef-209">Dans tous les cas, les quatre membres doivent être initialisés.</span><span class="sxs-lookup"><span data-stu-id="00cef-209">In any case, all four members must be initialized.</span></span> <span data-ttu-id="00cef-210">MULTIPAD utilise **des \_ usedefault en PV** pour toutes les dimensions.</span><span class="sxs-lookup"><span data-stu-id="00cef-210">Multipad uses **CW\_USEDEFAULT** for all dimensions.</span></span>

<span data-ttu-id="00cef-211">Le dernier membre de la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) est le membre de **style** , qui peut contenir des bits de style pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00cef-211">The last member of the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure is the **style** member, which may contain style bits for the window.</span></span> <span data-ttu-id="00cef-212">Pour créer une fenêtre enfant MDI qui peut avoir n’importe quelle combinaison de styles de fenêtre, spécifiez le style de fenêtre **MDIs \_ ALLCHILDSTYLES** .</span><span class="sxs-lookup"><span data-stu-id="00cef-212">To create an MDI child window that can have any combination of window styles, specify the **MDIS\_ALLCHILDSTYLES** window style.</span></span> <span data-ttu-id="00cef-213">Quand ce style n’est pas spécifié, une fenêtre enfant MDI a les paramètres **WS \_ Minimize**, **WS \_ Maximize**, **WS \_ HSCROLL** et **WS \_ VSCROLL** comme paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="00cef-213">When this style is not specified, an MDI child window has the **WS\_MINIMIZE**, **WS\_MAXIMIZE**, **WS\_HSCROLL**, and **WS\_VSCROLL** styles as default settings.</span></span>

<span data-ttu-id="00cef-214">MULTIPAD crée ses fenêtres enfants MDI en utilisant sa fonction AddFile définie localement (située dans le fichier source MPFILE. C).</span><span class="sxs-lookup"><span data-stu-id="00cef-214">Multipad creates its MDI child windows by using its locally defined AddFile function (located in the source file MPFILE.C).</span></span> <span data-ttu-id="00cef-215">La fonction AddFile définit le titre de la fenêtre enfant en assignant le membre **szTitle** de la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) de la fenêtre au nom du fichier en cours de modification ou à « sans titre ».</span><span class="sxs-lookup"><span data-stu-id="00cef-215">The AddFile function sets the title of the child window by assigning the **szTitle** member of the window's [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure to either the name of the file being edited or to "Untitled."</span></span> <span data-ttu-id="00cef-216">Le membre **szClass** est défini sur le nom de la classe de fenêtre enfant MDI inscrite dans la fonction InitializeApplication de MULTIPAD.</span><span class="sxs-lookup"><span data-stu-id="00cef-216">The **szClass** member is set to the name of the MDI child window class registered in Multipad's InitializeApplication function.</span></span> <span data-ttu-id="00cef-217">Le membre **hOwner** est défini sur le handle d’instance de l’application.</span><span class="sxs-lookup"><span data-stu-id="00cef-217">The **hOwner** member is set to the application's instance handle.</span></span>

<span data-ttu-id="00cef-218">L’exemple suivant illustre la fonction AddFile dans MULTIPAD.</span><span class="sxs-lookup"><span data-stu-id="00cef-218">The following example shows the AddFile function in Multipad.</span></span>


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



<span data-ttu-id="00cef-219">Le pointeur passé dans le paramètre *lParam* du message [**WM \_ MDICREATE**](wm-mdicreate.md) est passé à la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) et apparaît en tant que premier membre de la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , passé dans le message [**WM \_ Create**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="00cef-219">The pointer passed in the *lParam* parameter of the [**WM\_MDICREATE**](wm-mdicreate.md) message is passed to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function and appears as the first member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure, passed in the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="00cef-220">Dans MULTIPAD, la fenêtre enfant s’initialise elle-même lors de la **\_ création** du traitement des messages par l’initialisation des variables de document dans ses données supplémentaires et en créant la fenêtre enfant du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="00cef-220">In Multipad, the child window initializes itself during **WM\_CREATE** message processing by initializing document variables in its extra data and by creating the edit control's child window.</span></span>

 

 
