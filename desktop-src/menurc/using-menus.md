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
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726749"
---
# <a name="using-menus"></a><span data-ttu-id="3fee9-121">Utilisation des menus</span><span class="sxs-lookup"><span data-stu-id="3fee9-121">Using Menus</span></span>

<span data-ttu-id="3fee9-122">Cette section décrit les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3fee9-122">This section describes the following tasks:</span></span>

-   [<span data-ttu-id="3fee9-123">Utilisation d’une ressource Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-123">Using a Menu-Template Resource</span></span>](#using-a-menu-template-resource)
    -   [<span data-ttu-id="3fee9-124">Format de Menu-Template étendu</span><span class="sxs-lookup"><span data-stu-id="3fee9-124">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
    -   [<span data-ttu-id="3fee9-125">Ancien format de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-125">Old Menu-Template Format</span></span>](#old-menu-template-format)
    -   [<span data-ttu-id="3fee9-126">Chargement d’une ressource Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-126">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
    -   [<span data-ttu-id="3fee9-127">Création d’un menu classe</span><span class="sxs-lookup"><span data-stu-id="3fee9-127">Creating a Class Menu</span></span>](#creating-a-class-menu)
-   [<span data-ttu-id="3fee9-128">Création d’un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="3fee9-128">Creating a Shortcut Menu</span></span>](#creating-a-shortcut-menu)
    -   [<span data-ttu-id="3fee9-129">Traitement du \_ message WM CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="3fee9-129">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
    -   [<span data-ttu-id="3fee9-130">Création d’un menu contextuel Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="3fee9-130">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
    -   [<span data-ttu-id="3fee9-131">Affichage d’un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="3fee9-131">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)
-   [<span data-ttu-id="3fee9-132">Utilisation de Menu-Item bitmaps</span><span class="sxs-lookup"><span data-stu-id="3fee9-132">Using Menu-Item Bitmaps</span></span>](#using-menu-item-bitmaps)
    -   [<span data-ttu-id="3fee9-133">Définition de l’indicateur de type bitmap</span><span class="sxs-lookup"><span data-stu-id="3fee9-133">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
    -   [<span data-ttu-id="3fee9-134">Création de l’image bitmap</span><span class="sxs-lookup"><span data-stu-id="3fee9-134">Creating the Bitmap</span></span>](#creating-the-bitmap)
    -   [<span data-ttu-id="3fee9-135">Ajout de lignes et de graphiques à un menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-135">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
    -   [<span data-ttu-id="3fee9-136">Exemple de bitmaps Menu-Item</span><span class="sxs-lookup"><span data-stu-id="3fee9-136">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)
-   [<span data-ttu-id="3fee9-137">Créer des éléments de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-137">Creating Owner-Drawn Menu Items</span></span>](#creating-owner-drawn-menu-items)
    -   [<span data-ttu-id="3fee9-138">Définition de l’indicateur Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-138">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
    -   [<span data-ttu-id="3fee9-139">Menus owner-drawn et le \_ message WM MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="3fee9-139">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="3fee9-140">Menus owner-drawn et le \_ message WM DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="3fee9-140">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="3fee9-141">Menus owner-drawn et le \_ message WM MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="3fee9-141">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
    -   [<span data-ttu-id="3fee9-142">Définition des polices pour les chaînes de texte Menu-Item</span><span class="sxs-lookup"><span data-stu-id="3fee9-142">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
    -   [<span data-ttu-id="3fee9-143">Exemple d’éléments de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-143">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)
-   [<span data-ttu-id="3fee9-144">Utilisation de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-144">Using Custom Check Mark Bitmaps</span></span>](#using-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="3fee9-145">Création de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-145">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="3fee9-146">Association de bitmaps à un élément de menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-146">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
    -   [<span data-ttu-id="3fee9-147">Définition de l’attribut coche</span><span class="sxs-lookup"><span data-stu-id="3fee9-147">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
    -   [<span data-ttu-id="3fee9-148">Simulation de cases à cocher dans un menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-148">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
    -   [<span data-ttu-id="3fee9-149">Exemple d’utilisation de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-149">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a><span data-ttu-id="3fee9-150">Utilisation d’une ressource Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-150">Using a Menu-Template Resource</span></span>

<span data-ttu-id="3fee9-151">Vous incluez généralement un menu dans une application en créant une ressource de modèle de menu, puis en chargeant le menu au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3fee9-151">You typically include a menu in an application by creating a menu-template resource and then loading the menu at run time.</span></span> <span data-ttu-id="3fee9-152">Cette section décrit le format d’un modèle de menu et explique comment charger une ressource de modèle de menu et l’utiliser dans votre application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-152">This section describes the format of a menu template, and explains how to load a menu-template resource and use it in your application.</span></span> <span data-ttu-id="3fee9-153">Pour plus d’informations sur la création d’une ressource de modèle de menu, consultez la documentation fournie avec vos outils de développement.</span><span class="sxs-lookup"><span data-stu-id="3fee9-153">For information about creating a menu-template resource, see the documentation included with your development tools.</span></span>

-   [<span data-ttu-id="3fee9-154">Format de Menu-Template étendu</span><span class="sxs-lookup"><span data-stu-id="3fee9-154">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
-   [<span data-ttu-id="3fee9-155">Ancien format de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-155">Old Menu-Template Format</span></span>](#old-menu-template-format)
-   [<span data-ttu-id="3fee9-156">Chargement d’une ressource Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-156">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
-   [<span data-ttu-id="3fee9-157">Création d’un menu classe</span><span class="sxs-lookup"><span data-stu-id="3fee9-157">Creating a Class Menu</span></span>](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a><span data-ttu-id="3fee9-158">Format de Menu-Template étendu</span><span class="sxs-lookup"><span data-stu-id="3fee9-158">Extended Menu-Template Format</span></span>

<span data-ttu-id="3fee9-159">Le format de modèle de menu étendu prend en charge des fonctionnalités de menu supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3fee9-159">The extended menu-template format supports additional menu functionality.</span></span> <span data-ttu-id="3fee9-160">Comme les ressources de modèle de menu standard, les ressources de modèle de menu étendues ont le type de ressource de **\_ menu RT** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-160">Like standard menu-template resources, extended menu-template resources have the **RT\_MENU** resource type.</span></span> <span data-ttu-id="3fee9-161">Le système distingue les deux formats de ressources par le numéro de version, qui est le premier membre de l’en-tête de ressource.</span><span class="sxs-lookup"><span data-stu-id="3fee9-161">The system distinguishes the two resource formats by the version number, which is the first member of the resource header.</span></span>

<span data-ttu-id="3fee9-162">Un modèle de menu étendu se compose d’une structure d' [**\_ \_ en-tête de modèle menuex**](menuex-template-header.md) , suivie d’un plus grand nombre de structures de définition d’élément de [**\_ modèle \_ menuex**](menuex-template-item.md) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-162">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one more [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) item definition structures.</span></span>

### <a name="old-menu-template-format"></a><span data-ttu-id="3fee9-163">Ancien format de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-163">Old Menu-Template Format</span></span>

<span data-ttu-id="3fee9-164">Un ancien modèle de menu (Microsoft Windows NT 3,51 et versions antérieures) définit un menu, mais ne prend pas en charge les nouvelles fonctionnalités de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-164">An old menu template (Microsoft Windows NT 3.51 and earlier) defines a menu, but does not support the new menu functionality.</span></span> <span data-ttu-id="3fee9-165">Une ancienne ressource de modèle de menu a le type de ressource de **\_ menu RT** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-165">An old menu-template resource has the **RT\_MENU** resource type.</span></span>

<span data-ttu-id="3fee9-166">Un ancien modèle de menu se compose d’une structure [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) suivie d’une ou de plusieurs structures [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-166">An old menu template consists of a [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) structure followed by one or more [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) structures.</span></span>

### <a name="loading-a-menu-template-resource"></a><span data-ttu-id="3fee9-167">Chargement d’une ressource Menu-Template</span><span class="sxs-lookup"><span data-stu-id="3fee9-167">Loading a Menu-Template Resource</span></span>

<span data-ttu-id="3fee9-168">Pour charger une ressource de modèle de menu, utilisez la fonction [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , en spécifiant un handle pour le module qui contient la ressource et l’identificateur du modèle de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-168">To load a menu-template resource, use the [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) function, specifying a handle to the module that contains the resource and the menu template's identifier.</span></span> <span data-ttu-id="3fee9-169">La fonction **LoadMenu** retourne un handle de menu que vous pouvez utiliser pour assigner le menu à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-169">The **LoadMenu** function returns a menu handle that you can use to assign the menu to a window.</span></span> <span data-ttu-id="3fee9-170">Cette fenêtre devient la fenêtre propriétaire du menu, qui reçoit tous les messages générés par le menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-170">This window becomes the menu's owner window, receiving all the messages generated by the menu.</span></span>

<span data-ttu-id="3fee9-171">Pour créer un menu à partir d’un modèle de menu qui est déjà en mémoire, utilisez la fonction [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-171">To create a menu from a menu template that is already in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span> <span data-ttu-id="3fee9-172">Cela est utile si votre application génère des modèles de menu de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="3fee9-172">This is useful if your application generates menu templates dynamically.</span></span>

<span data-ttu-id="3fee9-173">Pour assigner un menu à une fenêtre, utilisez la fonction [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) ou spécifiez le handle du menu dans le paramètre *HMENU* de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) lors de la création d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-173">To assign a menu to a window, use the [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) function or specify the menu's handle in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function when creating a window.</span></span> <span data-ttu-id="3fee9-174">Vous pouvez également assigner un menu à une fenêtre en spécifiant un modèle de menu lorsque vous inscrivez une classe de fenêtre. le modèle identifie le menu spécifié comme le menu classe pour cette classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-174">Another way you can assign a menu to a window is to specify a menu template when you register a window class; the template identifies the specified menu as the class menu for that window class.</span></span>

<span data-ttu-id="3fee9-175">Pour que le système affecte automatiquement un menu spécifique à une fenêtre, spécifiez le modèle du menu lorsque vous inscrivez la classe de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-175">To have the system automatically assign a specific menu to a window, specify the menu's template when you register the window's class.</span></span> <span data-ttu-id="3fee9-176">Le modèle identifie le menu spécifié comme le menu classe pour cette classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-176">The template identifies the specified menu as the class menu for that window class.</span></span> <span data-ttu-id="3fee9-177">Ensuite, lorsque vous créez une fenêtre de la classe spécifiée, le système affecte automatiquement le menu spécifié à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-177">Then, when you create a window of the specified class, the system automatically assigns the specified menu to the window.</span></span>

<span data-ttu-id="3fee9-178">Vous ne pouvez pas assigner un menu à une fenêtre qui est une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="3fee9-178">You cannot assign a menu to a window that is a child window.</span></span>

<span data-ttu-id="3fee9-179">Pour créer un menu de classe, incluez l’identificateur de la ressource de modèle de menu en tant que membre **lpszMenuName** d’une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , puis transmettez un pointeur vers la structure à la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-179">To create a class menu, include the identifier of the menu-template resource as the **lpszMenuName** member of a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure and then pass a pointer to the structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span>

### <a name="creating-a-class-menu"></a><span data-ttu-id="3fee9-180">Création d’un menu classe</span><span class="sxs-lookup"><span data-stu-id="3fee9-180">Creating a Class Menu</span></span>

<span data-ttu-id="3fee9-181">L’exemple suivant montre comment créer un menu de classe pour une application, créer une fenêtre qui utilise le menu classe et traiter les commandes de menu dans la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-181">The following example shows how to create a class menu for an application, create a window that uses the class menu, and process menu commands in the window procedure.</span></span>

<span data-ttu-id="3fee9-182">Voici la partie pertinente du fichier d’en-tête de l’application :</span><span class="sxs-lookup"><span data-stu-id="3fee9-182">Following is the relevant portion of the application's header file:</span></span>


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



<span data-ttu-id="3fee9-183">Voici les parties pertinentes de l’application elle-même :</span><span class="sxs-lookup"><span data-stu-id="3fee9-183">Following are the relevant portions of the application itself:</span></span>


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



## <a name="creating-a-shortcut-menu"></a><span data-ttu-id="3fee9-184">Création d’un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="3fee9-184">Creating a Shortcut Menu</span></span>

<span data-ttu-id="3fee9-185">Pour utiliser un menu contextuel dans une application, transmettez son handle à la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-185">To use a shortcut menu in an application, pass its handle to the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="3fee9-186">Une application appelle généralement **TrackPopupMenuEx** dans une procédure de fenêtre en réponse à un message généré par l’utilisateur, tel que [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) ou WM keyoff. [**\_**](/windows/desktop/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="3fee9-186">An application typically calls **TrackPopupMenuEx** in a window procedure in response to a user-generated message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span></span>

<span data-ttu-id="3fee9-187">En plus du handle de menu contextuel, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) nécessite que vous spécifiiez un handle vers la fenêtre propriétaire, la position du menu contextuel (en coordonnées d’écran) et le bouton de la souris que l’utilisateur peut utiliser pour choisir un élément.</span><span class="sxs-lookup"><span data-stu-id="3fee9-187">In addition to the pop-up menu handle, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requires that you specify a handle to the owner window, the position of the shortcut menu (in screen coordinates), and the mouse button that the user can use to choose an item.</span></span>

<span data-ttu-id="3fee9-188">L’ancienne fonction [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) est toujours prise en charge, mais les nouvelles applications doivent utiliser la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-188">The older [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function is still supported, but new applications should use the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="3fee9-189">La fonction **TrackPopupMenuEx** requiert les mêmes paramètres que **TrackPopupMenu**, mais elle vous permet également de spécifier une partie de l’écran que le menu ne doit pas masquer.</span><span class="sxs-lookup"><span data-stu-id="3fee9-189">The **TrackPopupMenuEx** function requires the same parameters as **TrackPopupMenu**, but also lets you specify a portion of the screen that the menu should not obscure.</span></span> <span data-ttu-id="3fee9-190">Une application appelle généralement ces fonctions dans une procédure de fenêtre lors du traitement du message [**WM \_ CONTEXTMENU**](wm-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-190">An application typically calls these functions in a window procedure when processing the [**WM\_CONTEXTMENU**](wm-contextmenu.md) message.</span></span>

<span data-ttu-id="3fee9-191">Vous pouvez spécifier la position d’un menu contextuel en fournissant des coordonnées x et y, ainsi que l’indicateur **TPM \_ CENTERALIGN**, **TPM \_ LEFTALIGN** ou **TPM \_ RIGHTALIGN** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-191">You can specify the position of a shortcut menu by providing x- and y-coordinates along with the **TPM\_CENTERALIGN**, **TPM\_LEFTALIGN**, or **TPM\_RIGHTALIGN** flag.</span></span> <span data-ttu-id="3fee9-192">L’indicateur spécifie la position du menu contextuel par rapport aux coordonnées x et y.</span><span class="sxs-lookup"><span data-stu-id="3fee9-192">The flag specifies the position of the shortcut menu relative to the x- and y-coordinates.</span></span>

<span data-ttu-id="3fee9-193">Vous devez autoriser l’utilisateur à choisir un élément dans un menu contextuel en utilisant le même bouton de souris que celui utilisé pour afficher le menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-193">You should permit the user to choose an item from a shortcut menu by using the same mouse button used to display the menu.</span></span> <span data-ttu-id="3fee9-194">Pour ce faire, spécifiez l’indicateur **TPM \_ LEFTBUTTON** ou **TPM \_ RIGHTBUTTON** pour indiquer le bouton de la souris que l’utilisateur peut utiliser pour choisir un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-194">To do this, specify either **TPM\_LEFTBUTTON** or **TPM\_RIGHTBUTTON** flag to indicate which mouse button the user can use to choose a menu item.</span></span>

-   [<span data-ttu-id="3fee9-195">Traitement du \_ message WM CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="3fee9-195">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
-   [<span data-ttu-id="3fee9-196">Création d’un menu contextuel Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="3fee9-196">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
-   [<span data-ttu-id="3fee9-197">Affichage d’un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="3fee9-197">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a><span data-ttu-id="3fee9-198">Traitement du \_ message WM CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="3fee9-198">Processing the WM\_CONTEXTMENU Message</span></span>

<span data-ttu-id="3fee9-199">Le [**message \_ WM CONTEXTMENU**](wm-contextmenu.md) est généré quand une procédure de fenêtre d’application transmet le message [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-199">The [**WM\_CONTEXTMENU**](wm-contextmenu.md) message is generated when an application's window procedure passes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="3fee9-200">L’application peut traiter ce message pour afficher un menu contextuel adapté à une partie spécifique de l’écran.</span><span class="sxs-lookup"><span data-stu-id="3fee9-200">The application can process this message to display a shortcut menu appropriate to a specific portion of its screen.</span></span> <span data-ttu-id="3fee9-201">Si l’application n’affiche pas de menu contextuel, elle doit transmettre le message à **DefWindowProc** pour la gestion par défaut.</span><span class="sxs-lookup"><span data-stu-id="3fee9-201">If the application does not display a shortcut menu, it should pass the message to **DefWindowProc** for default handling.</span></span>

<span data-ttu-id="3fee9-202">Voici un exemple de traitement des messages [**WM \_ CONTEXTMENU**](wm-contextmenu.md) , tel qu’il peut apparaître dans la procédure de fenêtre d’une application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-202">Following is an example of [**WM\_CONTEXTMENU**](wm-contextmenu.md) message processing as it might appear in an application's window procedure.</span></span> <span data-ttu-id="3fee9-203">Les mots de poids fort et de poids fort du paramètre *lParam* spécifient les coordonnées d’écran de la souris lorsque le bouton droit de la souris est relâché (Notez que ces coordonnées peuvent prendre des valeurs négatives sur les systèmes avec plusieurs moniteurs).</span><span class="sxs-lookup"><span data-stu-id="3fee9-203">The low-order and high-order words of the *lParam* parameter specify the screen coordinates of the mouse when the right mouse button is released (note that these coordinates can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="3fee9-204">La fonction **OnContextMenu** définie par l’application retourne la **valeur true** si elle affiche un menu contextuel, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3fee9-204">The application-defined **OnContextMenu** function returns **TRUE** if it displays a context menu, or **FALSE** if it does not.</span></span>


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



<span data-ttu-id="3fee9-205">La fonction OnContextMenu définie par l’application suivante affiche un menu contextuel si la position spécifiée de la souris se trouve dans la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-205">The following application-defined OnContextMenu function displays a shortcut menu if the specified mouse position is within the window's client area.</span></span> <span data-ttu-id="3fee9-206">Une fonction plus sophistiquée peut afficher l’un des différents menus, en fonction de la partie de la zone cliente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3fee9-206">A more sophisticated function might display one of several different menus, depending on which portion of the client area is specified.</span></span> <span data-ttu-id="3fee9-207">Pour afficher réellement le menu contextuel, cet exemple appelle une fonction définie par l’application appelée DisplayContextMenu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-207">To actually display the shortcut menu, this example calls an application-defined function called DisplayContextMenu.</span></span> <span data-ttu-id="3fee9-208">Pour obtenir une description de cette fonction, consultez [affichage d’un menu contextuel](#displaying-a-shortcut-menu).</span><span class="sxs-lookup"><span data-stu-id="3fee9-208">For a description of this function, see [Displaying a Shortcut Menu](#displaying-a-shortcut-menu).</span></span>


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



### <a name="creating-a-shortcut-font-attributes-menu"></a><span data-ttu-id="3fee9-209">Création d’un menu contextuel Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="3fee9-209">Creating a Shortcut Font-Attributes Menu</span></span>

<span data-ttu-id="3fee9-210">L’exemple de cette section contient des portions de code d’une application qui crée et affiche un menu contextuel qui permet à l’utilisateur de définir des polices et des attributs de police.</span><span class="sxs-lookup"><span data-stu-id="3fee9-210">The example in this section contains portions of code from an application that creates and displays a shortcut menu that enables the user to set fonts and font attributes.</span></span> <span data-ttu-id="3fee9-211">L’application affiche le menu dans la zone cliente de sa fenêtre principale chaque fois que l’utilisateur clique avec le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="3fee9-211">The application displays the menu in the client area of its main window whenever the user clicks the left mouse button.</span></span>

<span data-ttu-id="3fee9-212">Voici le modèle de menu du menu contextuel fourni dans le fichier de définition de ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-212">Here is the menu template for the shortcut menu that is provided in the application's resource-definition file.</span></span>


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



<span data-ttu-id="3fee9-213">L’exemple suivant donne la procédure de fenêtre et les fonctions de prise en charge utilisées pour créer et afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="3fee9-213">The following example gives the window procedure and supporting functions used to create and display the shortcut menu.</span></span>


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



### <a name="displaying-a-shortcut-menu"></a><span data-ttu-id="3fee9-214">Affichage d’un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="3fee9-214">Displaying a Shortcut Menu</span></span>

<span data-ttu-id="3fee9-215">La fonction illustrée dans l’exemple suivant affiche un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="3fee9-215">The function shown in the following example displays a shortcut menu.</span></span>

<span data-ttu-id="3fee9-216">L’application comprend une ressource de menu identifiée par la chaîne « ShortcutExample ».</span><span class="sxs-lookup"><span data-stu-id="3fee9-216">The application includes a menu resource identified by the string "ShortcutExample."</span></span> <span data-ttu-id="3fee9-217">La barre de menus contient simplement un nom de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-217">The menu bar simply contains a menu name.</span></span> <span data-ttu-id="3fee9-218">L’application utilise la fonction [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) pour afficher le menu associé à cet élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-218">The application uses the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function to display the menu associated with this menu item.</span></span> <span data-ttu-id="3fee9-219">(La barre de menus elle-même n’est pas affichée, car **TrackPopupMenu** requiert un handle vers un menu, un sous-menu ou un menu contextuel.)</span><span class="sxs-lookup"><span data-stu-id="3fee9-219">(The menu bar itself is not displayed because **TrackPopupMenu** requires a handle to a menu, submenu, or shortcut menu.)</span></span>


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



## <a name="using-menu-item-bitmaps"></a><span data-ttu-id="3fee9-220">Utilisation de Menu-Item bitmaps</span><span class="sxs-lookup"><span data-stu-id="3fee9-220">Using Menu-Item Bitmaps</span></span>

<span data-ttu-id="3fee9-221">Le système peut utiliser une bitmap au lieu d’une chaîne de texte pour afficher un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-221">The system can use a bitmap instead of a text string to display a menu item.</span></span> <span data-ttu-id="3fee9-222">Pour utiliser une image bitmap, vous devez définir l’indicateur de **\_ bitmap miim** pour l’élément de menu et spécifier un handle vers le bitmap que le système doit afficher pour l’élément de menu dans le membre **HbmpItem** de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-222">To use a bitmap, you must set the **MIIM\_BITMAP** flag for the menu item and specify a handle to the bitmap that the system should display for the menu item in the **hbmpItem** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="3fee9-223">Cette section décrit comment utiliser des bitmaps pour les éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-223">This section describes how to use bitmaps for menu items.</span></span>

-   [<span data-ttu-id="3fee9-224">Définition de l’indicateur de type bitmap</span><span class="sxs-lookup"><span data-stu-id="3fee9-224">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
-   [<span data-ttu-id="3fee9-225">Création de l’image bitmap</span><span class="sxs-lookup"><span data-stu-id="3fee9-225">Creating the Bitmap</span></span>](#creating-the-bitmap)
-   [<span data-ttu-id="3fee9-226">Ajout de lignes et de graphiques à un menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-226">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
-   [<span data-ttu-id="3fee9-227">Exemple de bitmaps Menu-Item</span><span class="sxs-lookup"><span data-stu-id="3fee9-227">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a><span data-ttu-id="3fee9-228">Définition de l’indicateur de type bitmap</span><span class="sxs-lookup"><span data-stu-id="3fee9-228">Setting the Bitmap Type Flag</span></span>

<span data-ttu-id="3fee9-229">La **\_ bitmap miim** ou l’indicateur de **\_ bitmap MF** indique au système d’utiliser une image bitmap plutôt qu’une chaîne de texte pour afficher un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-229">The **MIIM\_BITMAP** or **MF\_BITMAP** flag tells the system to use a bitmap rather than a text string to display a menu item.</span></span> <span data-ttu-id="3fee9-230">La **\_ bitmap miim** d’un élément de menu ou l’indicateur **\_ bitmap MF** doit être défini au moment de l’exécution ; vous ne pouvez pas le définir dans le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="3fee9-230">A menu item's **MIIM\_BITMAP** or **MF\_BITMAP** flag must be set at run time; you cannot set it in the resource-definition file.</span></span>

<span data-ttu-id="3fee9-231">Pour les nouvelles applications, vous pouvez utiliser la fonction [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) ou [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) pour définir l’indicateur de type de **\_ bitmap miim** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-231">For new applications, you can use the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) or [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) function to set the **MIIM\_BITMAP** type flag.</span></span> <span data-ttu-id="3fee9-232">Pour modifier un élément de menu d’un élément de texte en élément bitmap, utilisez **SetMenuItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="3fee9-232">To change a menu item from a text item to a bitmap item, use **SetMenuItemInfo**.</span></span> <span data-ttu-id="3fee9-233">Pour ajouter un nouvel élément bitmap à un menu, utilisez la fonction **InsertMenuItem** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-233">To add a new bitmap item to a menu, use the **InsertMenuItem** function.</span></span>

<span data-ttu-id="3fee9-234">Les applications écrites pour des versions antérieures du système peuvent continuer à utiliser les fonctions [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) pour définir l’indicateur de **\_ bitmap MF** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-234">Applications written for earlier versions of the system can continue to use the [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to set the **MF\_BITMAP** flag.</span></span> <span data-ttu-id="3fee9-235">Pour modifier un élément de menu d’un élément de chaîne de texte en élément bitmap, utilisez **ModifyMenu**.</span><span class="sxs-lookup"><span data-stu-id="3fee9-235">To change a menu item from a text string item to a bitmap item, use **ModifyMenu**.</span></span> <span data-ttu-id="3fee9-236">Pour ajouter un nouvel élément bitmap à un menu, utilisez l’indicateur de **\_ bitmap MF** avec la fonction **InsertMenu** ou **AppendMenu** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-236">To add a new bitmap item to a menu, use the **MF\_BITMAP** flag with the **InsertMenu** or **AppendMenu** function.</span></span>

### <a name="creating-the-bitmap"></a><span data-ttu-id="3fee9-237">Création de l’image bitmap</span><span class="sxs-lookup"><span data-stu-id="3fee9-237">Creating the Bitmap</span></span>

<span data-ttu-id="3fee9-238">Lorsque vous définissez l’indicateur de type bitmap **miim \_** ou **MF \_** pour un élément de menu, vous devez également spécifier un handle vers le bitmap que le système doit afficher pour l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-238">When you set the **MIIM\_BITMAP** or **MF\_BITMAP** type flag for a menu item, you must also specify a handle to the bitmap that the system should display for the menu item.</span></span> <span data-ttu-id="3fee9-239">Vous pouvez fournir la bitmap en tant que ressource bitmap ou créer l’image bitmap au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3fee9-239">You can provide the bitmap as a bitmap resource or create the bitmap at run time.</span></span> <span data-ttu-id="3fee9-240">Si vous utilisez une ressource bitmap, vous pouvez utiliser la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) pour charger la bitmap et obtenir son handle.</span><span class="sxs-lookup"><span data-stu-id="3fee9-240">If you use a bitmap resource, you can use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap and obtain its handle.</span></span>

<span data-ttu-id="3fee9-241">Pour créer l’image bitmap au moment de l’exécution, utilisez les fonctions Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="3fee9-241">To create the bitmap at run time, use Windows Graphics Device Interface (GDI) functions.</span></span> <span data-ttu-id="3fee9-242">GDI offre plusieurs moyens de créer une bitmap au moment de l’exécution, mais les développeurs utilisent généralement la méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="3fee9-242">GDI provides several ways to create a bitmap at run time, but developers typically use the following method:</span></span>

1.  <span data-ttu-id="3fee9-243">Utilisez la fonction [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) pour créer un contexte de périphérique compatible avec le contexte de périphérique utilisé par la fenêtre principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-243">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the device context used by the application's main window.</span></span>
2.  <span data-ttu-id="3fee9-244">Utilisez la fonction [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) pour créer une bitmap compatible avec la fenêtre principale de l’application ou utilisez la fonction [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) pour créer une image bitmap monochrome.</span><span class="sxs-lookup"><span data-stu-id="3fee9-244">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window or use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>
3.  <span data-ttu-id="3fee9-245">Utilisez la fonction [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) pour sélectionner la bitmap dans le contexte de périphérique compatible.</span><span class="sxs-lookup"><span data-stu-id="3fee9-245">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="3fee9-246">Utilisez les fonctions de dessin GDI, telles que [**ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) et [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), pour dessiner une image dans le bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fee9-246">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap.</span></span>

<span data-ttu-id="3fee9-247">Pour plus d’informations, consultez [bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="3fee9-247">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="adding-lines-and-graphs-to-a-menu"></a><span data-ttu-id="3fee9-248">Ajout de lignes et de graphiques à un menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-248">Adding Lines and Graphs to a Menu</span></span>

<span data-ttu-id="3fee9-249">L’exemple de code suivant montre comment créer un menu qui contient des bitmaps d’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-249">The following code sample shows how to create a menu that contains menu-item bitmaps.</span></span> <span data-ttu-id="3fee9-250">Il crée deux menus.</span><span class="sxs-lookup"><span data-stu-id="3fee9-250">It creates two menus.</span></span> <span data-ttu-id="3fee9-251">Le premier est un menu de graphique qui contient trois bitmaps d’élément de menu : un graphique à secteurs, un graphique en courbes et un graphique à barres.</span><span class="sxs-lookup"><span data-stu-id="3fee9-251">The first is a Chart menu that contains three menu-item bitmaps: a pie chart, a line chart, and a bar chart.</span></span> <span data-ttu-id="3fee9-252">L’exemple montre comment charger ces bitmaps à partir du fichier de ressources de l’application, puis utiliser les fonctions [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) et [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) pour créer les éléments de menu et de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-252">The example demonstrates how to load these bitmaps from the application's resource file, and then use the [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) and [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to create the menu and menu items.</span></span>

<span data-ttu-id="3fee9-253">Le deuxième menu est un menu lignes.</span><span class="sxs-lookup"><span data-stu-id="3fee9-253">The second menu is a Lines menu.</span></span> <span data-ttu-id="3fee9-254">Elle contient des bitmaps qui indiquent les styles de ligne fournis par le stylet prédéfini dans le système.</span><span class="sxs-lookup"><span data-stu-id="3fee9-254">It contains bitmaps showing the line styles provided by the predefined pen in the system.</span></span> <span data-ttu-id="3fee9-255">Les bitmaps de style ligne sont créées au moment de l’exécution à l’aide des fonctions GDI.</span><span class="sxs-lookup"><span data-stu-id="3fee9-255">The line-style bitmaps are created at run time by using GDI functions.</span></span>

<span data-ttu-id="3fee9-256">Voici les définitions des ressources bitmap dans le fichier de définition de ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-256">Here are the definitions of the bitmap resources in the application's resource-definition file.</span></span>


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



<span data-ttu-id="3fee9-257">Voici les parties pertinentes du fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-257">Here are the relevant portions of the application's header file.</span></span>


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



<span data-ttu-id="3fee9-258">L’exemple suivant montre comment les menus et les bitmaps d’élément de menu sont créés dans une application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-258">The following example shows how menus and menu-item bitmaps are created in an application.</span></span>


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



### <a name="example-of-menu-item-bitmaps"></a><span data-ttu-id="3fee9-259">Exemple de bitmaps Menu-Item</span><span class="sxs-lookup"><span data-stu-id="3fee9-259">Example of Menu-Item Bitmaps</span></span>

<span data-ttu-id="3fee9-260">L’exemple de cette rubrique crée deux menus, chacun contenant plusieurs éléments de menu bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fee9-260">The example in this topic creates two menus, each containing several bitmap menu items.</span></span> <span data-ttu-id="3fee9-261">Pour chaque menu, l’application ajoute un nom de menu correspondant à la barre de menus de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="3fee9-261">For each menu, the application adds a corresponding menu name to the main window's menu bar.</span></span>

<span data-ttu-id="3fee9-262">Le premier menu contient des éléments de menu présentant chacun des trois types de graphiques suivants : secteurs, courbes et barres.</span><span class="sxs-lookup"><span data-stu-id="3fee9-262">The first menu contains menu items showing each of three chart types: pie, line, and bar.</span></span> <span data-ttu-id="3fee9-263">Les bitmaps de ces éléments de menu sont définis en tant que ressources et sont chargés à l’aide de la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-263">The bitmaps for these menu items are defined as resources and are loaded by using the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function.</span></span> <span data-ttu-id="3fee9-264">Le nom du menu « graphique » est associé à ce menu dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="3fee9-264">Associated with this menu is a "Chart" menu name on the menu bar.</span></span>

<span data-ttu-id="3fee9-265">Le deuxième menu contient des éléments de menu présentant chacun des cinq styles de ligne utilisés avec la fonction [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) : **PS \_ Solid**, **PS \_ Dash**, **PS \_ dot**, **PS \_ tiret point** et **PS \_ tiret point point**.</span><span class="sxs-lookup"><span data-stu-id="3fee9-265">The second menu contains menu items showing each of the five line styles used with the [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) function: **PS\_SOLID**, **PS\_DASH**, **PS\_DOT**, **PS\_DASHDOT**, and **PS\_DASHDOTDOT**.</span></span> <span data-ttu-id="3fee9-266">L’application crée les bitmaps pour ces éléments de menu au moment de l’exécution à l’aide des fonctions de dessin GDI.</span><span class="sxs-lookup"><span data-stu-id="3fee9-266">The application creates the bitmaps for these menu items at run time using GDI drawing functions.</span></span> <span data-ttu-id="3fee9-267">Le nom du menu **lignes** de la barre de menus est associé à ce menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-267">Associated with this menu is a **Lines** menu name on the menu bar.</span></span>

<span data-ttu-id="3fee9-268">Défini dans la procédure de fenêtre de l’application se trouvent deux tableaux statiques de handles de bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fee9-268">Defined in the application's window procedure are two static arrays of bitmap handles.</span></span> <span data-ttu-id="3fee9-269">Un tableau contient les descripteurs des trois bitmaps utilisés pour le menu **graphique** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-269">One array contains the handles of the three bitmaps used for the **Chart** menu.</span></span> <span data-ttu-id="3fee9-270">L’autre contient les descripteurs des cinq bitmaps utilisés pour le menu **lignes** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-270">The other contains the handles of the five bitmaps used for the **Lines** menu.</span></span> <span data-ttu-id="3fee9-271">Lors du traitement du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , la procédure de fenêtre charge les bitmaps de graphique, crée les bitmaps de ligne, puis ajoute les éléments de menu correspondants.</span><span class="sxs-lookup"><span data-stu-id="3fee9-271">When processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure loads the chart bitmaps, creates the line bitmaps, and then adds the corresponding menu items.</span></span> <span data-ttu-id="3fee9-272">Lors du traitement du message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , la procédure de fenêtre supprime toutes les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="3fee9-272">When processing the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the window procedure deletes all of the bitmaps.</span></span>

<span data-ttu-id="3fee9-273">Voici les parties pertinentes du fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-273">Following are the relevant portions of the application's header file.</span></span>


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



<span data-ttu-id="3fee9-274">Voici les parties pertinentes de la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3fee9-274">Following are the relevant portions of the window procedure.</span></span> <span data-ttu-id="3fee9-275">La procédure de fenêtre exécute la majeure partie de son initialisation en appelant les fonctions LoadChartBitmaps, CreateLineBitmaps et AddBitmapMenu définies par l’application, décrites plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="3fee9-275">The window procedure performs most of its initialization by calling the application-defined LoadChartBitmaps, CreateLineBitmaps, and AddBitmapMenu functions, described later in this topic.</span></span>


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



<span data-ttu-id="3fee9-276">La fonction LoadChartBitmaps définie par l’application charge les ressources bitmap pour le menu graphique en appelant la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , comme suit.</span><span class="sxs-lookup"><span data-stu-id="3fee9-276">The application-defined LoadChartBitmaps function loads the bitmap resources for the chart menu by calling the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, as follows.</span></span>


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



<span data-ttu-id="3fee9-277">La fonction CreateLineBitmaps définie par l’application crée les bitmaps pour le menu lignes à l’aide des fonctions de dessin GDI.</span><span class="sxs-lookup"><span data-stu-id="3fee9-277">The application-defined CreateLineBitmaps function creates the bitmaps for the Lines menu by using GDI drawing functions.</span></span> <span data-ttu-id="3fee9-278">La fonction crée un contexte de périphérique (DC) de mémoire avec les mêmes propriétés que le DC de la fenêtre du bureau.</span><span class="sxs-lookup"><span data-stu-id="3fee9-278">The function creates a memory device context (DC) with the same properties as the desktop window's DC.</span></span> <span data-ttu-id="3fee9-279">Pour chaque style de ligne, la fonction crée une image bitmap, la sélectionne dans le DC de mémoire et la dessine.</span><span class="sxs-lookup"><span data-stu-id="3fee9-279">For each line style, the function creates a bitmap, selects it into the memory DC, and draws in it.</span></span>


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



<span data-ttu-id="3fee9-280">La fonction AddBitmapMenu définie par l’application crée un menu et lui ajoute le nombre spécifié d’éléments de menu bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fee9-280">The application-defined AddBitmapMenu function creates a menu and adds the specified number of bitmap menu items to it.</span></span> <span data-ttu-id="3fee9-281">Ensuite, il ajoute un nom de menu correspondant à la barre de menus de la fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3fee9-281">Then it adds a corresponding menu name to the specified window's menu bar.</span></span>


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



## <a name="creating-owner-drawn-menu-items"></a><span data-ttu-id="3fee9-282">Créer des éléments de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-282">Creating Owner-Drawn Menu Items</span></span>

<span data-ttu-id="3fee9-283">Si vous avez besoin d’un contrôle total sur l’apparence d’un élément de menu, vous pouvez utiliser un élément de menu owner-drawn dans votre application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-283">If you need complete control over the appearance of a menu item, you can use an owner-drawn menu item in your application.</span></span> <span data-ttu-id="3fee9-284">Cette section décrit les étapes nécessaires à la création et à l’utilisation d’un élément de menu owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="3fee9-284">This section describes the steps involved in creating and using an owner-drawn menu item.</span></span>

-   [<span data-ttu-id="3fee9-285">Définition de l’indicateur Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-285">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
-   [<span data-ttu-id="3fee9-286">Menus owner-drawn et le \_ message WM MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="3fee9-286">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
-   [<span data-ttu-id="3fee9-287">Menus owner-drawn et le \_ message WM DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="3fee9-287">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
-   [<span data-ttu-id="3fee9-288">Menus owner-drawn et le \_ message WM MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="3fee9-288">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
-   [<span data-ttu-id="3fee9-289">Définition des polices pour les chaînes de texte Menu-Item</span><span class="sxs-lookup"><span data-stu-id="3fee9-289">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
-   [<span data-ttu-id="3fee9-290">Exemple d’éléments de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-290">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a><span data-ttu-id="3fee9-291">Définition de l’indicateur Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-291">Setting the Owner-Drawn Flag</span></span>

<span data-ttu-id="3fee9-292">Vous ne pouvez pas définir un élément de menu owner-drawn dans le fichier de définition de ressource de votre application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-292">You cannot define an owner-drawn menu item in your application's resource-definition file.</span></span> <span data-ttu-id="3fee9-293">Au lieu de cela, vous devez créer un nouvel élément de menu ou en modifier un à l’aide de l’indicateur de menu de la **MFT \_** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-293">Instead, you must create a new menu item or modify an existing one by using the **MFT\_OWNERDRAW** menu flag.</span></span>

<span data-ttu-id="3fee9-294">Vous pouvez utiliser la fonction [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) ou [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) pour spécifier un élément de menu owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="3fee9-294">You can use the [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) or [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function to specify an owner-drawn menu item.</span></span> <span data-ttu-id="3fee9-295">Utilisez **InsertMenuItem** pour insérer un nouvel élément de menu à la position spécifiée dans une barre de menus ou un menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-295">Use **InsertMenuItem** to insert a new menu item at the specified position in a menu bar or menu.</span></span> <span data-ttu-id="3fee9-296">Utilisez **SetMenuItemInfo** pour modifier le contenu d’un menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-296">Use **SetMenuItemInfo** to change the contents of a menu.</span></span>

<span data-ttu-id="3fee9-297">Lors de l’appel de ces deux fonctions, vous devez spécifier un pointeur vers une structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , qui spécifie les propriétés du nouvel élément de menu ou les propriétés que vous souhaitez modifier pour un élément de menu existant.</span><span class="sxs-lookup"><span data-stu-id="3fee9-297">When calling these two functions, you must specify a pointer to a [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, which specifies the properties of the new menu item or the properties you want to change for an existing menu item.</span></span> <span data-ttu-id="3fee9-298">Pour transformer un élément en élément owner-drawn, spécifiez la valeur **\_ ftype miim** pour le membre **fmask** et la valeur de la **table MFT \_** dans le membre **ftype** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-298">To make an item an owner-drawn item, specify the **MIIM\_FTYPE** value for the **fMask** member and the **MFT\_OWNERDRAW** value for the **fType** member.</span></span>

<span data-ttu-id="3fee9-299">En définissant les membres appropriés de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , vous pouvez associer une valeur définie par l’application, appelée **données d’élément**, à chaque élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-299">By setting the appropriate members of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, you can associate an application-defined value, which is called **item data**, with each menu item.</span></span> <span data-ttu-id="3fee9-300">Pour ce faire, spécifiez la valeur de **\_ données miim** pour le membre **fmask** et la valeur définie par l’application pour le membre **dwItemData** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-300">To do so, specify the **MIIM\_DATA** value for the **fMask** member and the application-defined value for the **dwItemData** member.</span></span>

<span data-ttu-id="3fee9-301">Vous pouvez utiliser des données d’élément avec n’importe quel type d’élément de menu, mais cela est particulièrement utile pour les éléments owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="3fee9-301">You can use item data with any type of menu item, but it is particularly useful for owner-drawn items.</span></span> <span data-ttu-id="3fee9-302">Supposons, par exemple, qu’une structure contient des informations utilisées pour dessiner un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-302">For example, suppose a structure contains information used to draw a menu item.</span></span> <span data-ttu-id="3fee9-303">Une application peut utiliser les données d’élément pour un élément de menu pour stocker un pointeur vers la structure.</span><span class="sxs-lookup"><span data-stu-id="3fee9-303">An application might use the item data for a menu item to store a pointer to the structure.</span></span> <span data-ttu-id="3fee9-304">Les données de l’élément sont envoyées à la fenêtre propriétaire du menu avec les messages [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) et [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-304">The item data is sent to the menu's owner window with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages.</span></span> <span data-ttu-id="3fee9-305">Pour récupérer les données d’un menu à tout moment, utilisez la fonction [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-305">To retrieve the item data for a menu at any time, use the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function.</span></span>

<span data-ttu-id="3fee9-306">Les applications écrites pour des versions antérieures du système peuvent continuer à appeler [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) pour assigner l’indicateur de **\_ OwnerDraw OwnerDraw** à un élément de menu owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="3fee9-306">Applications written for earlier versions of the system can continue to call [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) to assign the **MF\_OWNERDRAW** flag to an owner-drawn menu item.</span></span>

<span data-ttu-id="3fee9-307">Lorsque vous appelez l’une de ces trois fonctions, vous pouvez passer une valeur en tant que paramètre *lpNewItem* .</span><span class="sxs-lookup"><span data-stu-id="3fee9-307">When you call any of these three functions, you can pass a value as the *lpNewItem* parameter.</span></span> <span data-ttu-id="3fee9-308">Cette valeur peut représenter toutes les informations significatives pour votre application et qui seront disponibles pour votre application lorsque l’élément sera affiché.</span><span class="sxs-lookup"><span data-stu-id="3fee9-308">This value can represent any information that is meaningful to your application, and that will be available to your application when the item is to be displayed.</span></span> <span data-ttu-id="3fee9-309">Par exemple, la valeur peut contenir un pointeur vers une structure ; la structure peut, à son tour, contenir une chaîne de texte et un handle vers la police logique que votre application utilisera pour dessiner la chaîne.</span><span class="sxs-lookup"><span data-stu-id="3fee9-309">For example, the value could contain a pointer to a structure; the structure, in turn, might contain a text string and a handle to the logical font your application will use to draw the string.</span></span>

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a><span data-ttu-id="3fee9-310">Owner-Drawn les menus et le \_ message WM MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="3fee9-310">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>

<span data-ttu-id="3fee9-311">Avant que le système n’affiche un élément de menu owner-drawn pour la première fois, il envoie le message [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) à la procédure de fenêtre de la fenêtre qui possède le menu de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3fee9-311">Before the system displays an owner-drawn menu item for the first time, it sends the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message to the window procedure of the window that owns the item's menu.</span></span> <span data-ttu-id="3fee9-312">Ce message contient un pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui identifie l’élément et contient les données d’élément qu’une application peut avoir affectées.</span><span class="sxs-lookup"><span data-stu-id="3fee9-312">This message contains a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the item and contains the item data that an application may have assigned to it.</span></span> <span data-ttu-id="3fee9-313">La procédure de fenêtre doit remplir les membres **itemWidth** et **ItemHeight** de la structure avant de retourner du traitement du message.</span><span class="sxs-lookup"><span data-stu-id="3fee9-313">The window procedure must fill the **itemWidth** and **itemHeight** members of the structure before returning from processing the message.</span></span> <span data-ttu-id="3fee9-314">Le système utilise les informations contenues dans ces membres lors de la création du rectangle englobant dans lequel une application dessine l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-314">The system uses the information in these members when creating the bounding rectangle in which an application draws the menu item.</span></span> <span data-ttu-id="3fee9-315">Il utilise également les informations pour détecter quand l’utilisateur choisit l’élément.</span><span class="sxs-lookup"><span data-stu-id="3fee9-315">It also uses the information to detect when the user chooses the item.</span></span>

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a><span data-ttu-id="3fee9-316">Owner-Drawn les menus et le \_ message WM DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="3fee9-316">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>

<span data-ttu-id="3fee9-317">Chaque fois que l’élément doit être dessiné (par exemple, lorsqu’il est affiché pour la première fois ou lorsque l’utilisateur le sélectionne), le système envoie le message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) à la procédure de fenêtre de la fenêtre propriétaire du menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-317">Whenever the item must be drawn (for example, when it is first displayed or when the user selects it), the system sends the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message to the window procedure of the menu's owner window.</span></span> <span data-ttu-id="3fee9-318">Ce message contient un pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , qui contient des informations sur l’élément, y compris les données d’élément qu’une application peut avoir affectées.</span><span class="sxs-lookup"><span data-stu-id="3fee9-318">This message contains a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure, which contains information about the item, including the item data that an application may have assigned to it.</span></span> <span data-ttu-id="3fee9-319">En outre, **drawitemstruct,** contient des indicateurs qui indiquent l’état de l’élément (par exemple s’il est grisé ou sélectionné), ainsi qu’un rectangle englobant et un contexte de périphérique que l’application utilise pour dessiner l’élément.</span><span class="sxs-lookup"><span data-stu-id="3fee9-319">In addition, **DRAWITEMSTRUCT** contains flags that indicate the state of the item (such as whether it is grayed or selected) as well as a bounding rectangle and a device context that the application uses to draw the item.</span></span>

<span data-ttu-id="3fee9-320">Une application doit effectuer les opérations suivantes lors du traitement du message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) :</span><span class="sxs-lookup"><span data-stu-id="3fee9-320">An application must do the following while processing the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message:</span></span>

-   <span data-ttu-id="3fee9-321">Déterminez le type de dessin nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3fee9-321">Determine the type of drawing that is necessary.</span></span> <span data-ttu-id="3fee9-322">Pour ce faire, vérifiez le membre **itemAction** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-322">To do so, check the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span>
-   <span data-ttu-id="3fee9-323">Dessinez l’élément de menu de manière appropriée, à l’aide du rectangle englobant et du contexte de périphérique obtenu à partir de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-323">Draw the menu item appropriately, using the bounding rectangle and device context obtained from the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="3fee9-324">L’application doit dessiner uniquement dans le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="3fee9-324">The application must draw only within the bounding rectangle.</span></span> <span data-ttu-id="3fee9-325">Pour des raisons de performances, le système ne découpe pas les portions de l’image qui sont dessinées en dehors du rectangle.</span><span class="sxs-lookup"><span data-stu-id="3fee9-325">For performance reasons, the system does not clip portions of the image that are drawn outside the rectangle.</span></span>
-   <span data-ttu-id="3fee9-326">Restaurez tous les objets GDI sélectionnés pour le contexte de périphérique de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-326">Restore all GDI objects selected for the menu item's device context.</span></span>

<span data-ttu-id="3fee9-327">Si l’utilisateur sélectionne l’élément de menu, le système définit le membre **itemAction** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sur la valeur **Oda \_ Select** et définit la valeur **ODS \_ Selected** dans le membre **ItemState** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-327">If the user selects the menu item, the system sets the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure to the **ODA\_SELECT** value and sets the **ODS\_SELECTED** value in the **itemState** member.</span></span> <span data-ttu-id="3fee9-328">Il s’agit de la pile d’une application qui permet de redessiner l’élément de menu pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3fee9-328">This is an application's cue to redraw the menu item to indicate that it is selected.</span></span>

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a><span data-ttu-id="3fee9-329">Owner-Drawn les menus et le \_ message WM MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="3fee9-329">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>

<span data-ttu-id="3fee9-330">Les menus autres que les menus owner-drawn peuvent spécifier un mnémonique de menu en insérant un trait de soulignement à côté d’un caractère dans la chaîne de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-330">Menus other than owner-drawn menus can specify a menu mnemonic by inserting an underscore next to a character in the menu string.</span></span> <span data-ttu-id="3fee9-331">Cela permet à l’utilisateur de sélectionner le menu en appuyant sur ALT et en appuyant sur le caractère mnémonique du menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-331">This allows the user to select the menu by pressing ALT and pressing the menu mnemonic character.</span></span> <span data-ttu-id="3fee9-332">Toutefois, dans les menus owner-drawn, vous ne pouvez pas spécifier un mnémonique de menu de cette manière.</span><span class="sxs-lookup"><span data-stu-id="3fee9-332">In owner-drawn menus, however, you cannot specify a menu mnemonic in this manner.</span></span> <span data-ttu-id="3fee9-333">Au lieu de cela, votre application doit traiter le message [**WM \_ MENUCHAR**](wm-menuchar.md) pour fournir des menus owner-drawn avec des mnémoniques de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-333">Instead, your application must process the [**WM\_MENUCHAR**](wm-menuchar.md) message to provide owner-drawn menus with menu mnemonics.</span></span>

<span data-ttu-id="3fee9-334">Le message [**WM \_ MENUCHAR**](wm-menuchar.md) est envoyé lorsque l’utilisateur tape un mnémonique de menu qui ne correspond à aucun des mnémoniques prédéfinis du menu actuel.</span><span class="sxs-lookup"><span data-stu-id="3fee9-334">The [**WM\_MENUCHAR**](wm-menuchar.md) message is sent when the user types a menu mnemonic that does not match any of the predefined mnemonics of the current menu.</span></span> <span data-ttu-id="3fee9-335">La valeur contenue dans *wParam* spécifie le caractère ASCII qui correspond à la touche sur laquelle l’utilisateur a appuyé avec la touche Alt.</span><span class="sxs-lookup"><span data-stu-id="3fee9-335">The value contained in *wParam* specifies the ASCII character that corresponds to the key the user pressed with the ALT key.</span></span> <span data-ttu-id="3fee9-336">Le mot de poids faible de *wParam* spécifie le type du menu sélectionné et peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3fee9-336">The low-order word of *wParam* specifies the type of the selected menu and can be one of the following values:</span></span>

-   <span data-ttu-id="3fee9-337">**MF \_ POPUP** si le menu actuel est un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-337">**MF\_POPUP** if the current menu is a submenu.</span></span>
-   <span data-ttu-id="3fee9-338">**MF \_ SYSMENU** si le menu est le menu système.</span><span class="sxs-lookup"><span data-stu-id="3fee9-338">**MF\_SYSMENU** if the menu is the system menu.</span></span>

<span data-ttu-id="3fee9-339">Le mot de poids fort de *wParam* contient le handle de menu du menu actuel.</span><span class="sxs-lookup"><span data-stu-id="3fee9-339">The high-order word of *wParam* contains the menu handle to the current menu.</span></span> <span data-ttu-id="3fee9-340">La fenêtre avec les menus owner-drawn peut traiter [**WM \_ MENUCHAR**](wm-menuchar.md) comme suit :</span><span class="sxs-lookup"><span data-stu-id="3fee9-340">The window with the owner-drawn menus can process [**WM\_MENUCHAR**](wm-menuchar.md) as follows:</span></span>


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



<span data-ttu-id="3fee9-341">Les deux dans le mot de poids fort de la valeur de retour informent le système que le mot de poids faible de la valeur de retour contient l’index de base zéro de l’élément de menu à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="3fee9-341">The two in the high-order word of the return value informs the system that the low-order word of the return value contains the zero-based index of the menu item to be selected.</span></span>

<span data-ttu-id="3fee9-342">Les constantes suivantes correspondent aux valeurs de retour possibles du message [**WM \_ MENUCHAR**](wm-menuchar.md) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-342">The following constants correspond to the possible return values from the [**WM\_MENUCHAR**](wm-menuchar.md) message.</span></span>



| <span data-ttu-id="3fee9-343">Constante</span><span class="sxs-lookup"><span data-stu-id="3fee9-343">Constant</span></span>         | <span data-ttu-id="3fee9-344">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fee9-344">Value</span></span> | <span data-ttu-id="3fee9-345">Signification</span><span class="sxs-lookup"><span data-stu-id="3fee9-345">Meaning</span></span>                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fee9-346">**MNC \_ Ignorer**</span><span class="sxs-lookup"><span data-stu-id="3fee9-346">**MNC\_IGNORE**</span></span>  | <span data-ttu-id="3fee9-347">0</span><span class="sxs-lookup"><span data-stu-id="3fee9-347">0</span></span>     | <span data-ttu-id="3fee9-348">Le système doit ignorer le caractère que l’utilisateur a appuyé et créer un bref signal sonore sur le haut-parleur du système.</span><span class="sxs-lookup"><span data-stu-id="3fee9-348">The system should discard the character the user pressed and create a short beep on the system speaker.</span></span>                                                       |
| <span data-ttu-id="3fee9-349">**MNC \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="3fee9-349">**MNC\_CLOSE**</span></span>   | <span data-ttu-id="3fee9-350">1</span><span class="sxs-lookup"><span data-stu-id="3fee9-350">1</span></span>     | <span data-ttu-id="3fee9-351">Le système doit fermer le menu actif.</span><span class="sxs-lookup"><span data-stu-id="3fee9-351">The system should close the active menu.</span></span>                                                                                                                      |
| <span data-ttu-id="3fee9-352">**exécution de MNC \_**</span><span class="sxs-lookup"><span data-stu-id="3fee9-352">**MNC\_EXECUTE**</span></span> | <span data-ttu-id="3fee9-353">2</span><span class="sxs-lookup"><span data-stu-id="3fee9-353">2</span></span>     | <span data-ttu-id="3fee9-354">Le système doit choisir l’élément spécifié dans le mot de poids faible de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="3fee9-354">The system should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="3fee9-355">La fenêtre propriétaire reçoit un message de [**\_ commande WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-355">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span> |
| <span data-ttu-id="3fee9-356">**MNC \_ Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="3fee9-356">**MNC\_SELECT**</span></span>  | <span data-ttu-id="3fee9-357">3</span><span class="sxs-lookup"><span data-stu-id="3fee9-357">3</span></span>     | <span data-ttu-id="3fee9-358">Le système doit sélectionner l’élément spécifié dans le mot de poids faible de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="3fee9-358">The system should select the item specified in the low-order word of the return value.</span></span>                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a><span data-ttu-id="3fee9-359">Définition des polices pour les chaînes de texte Menu-Item</span><span class="sxs-lookup"><span data-stu-id="3fee9-359">Setting Fonts for Menu-Item Text Strings</span></span>

<span data-ttu-id="3fee9-360">Cette rubrique contient un exemple d’une application qui utilise des éléments de menu owner-drawn dans un menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-360">This topic contains an example from an application that uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="3fee9-361">Le menu contient des éléments qui définissent les attributs de la police actuelle, et les éléments sont affichés à l’aide de l’attribut de police approprié.</span><span class="sxs-lookup"><span data-stu-id="3fee9-361">The menu contains items that set the attributes of the current font, and the items are displayed using the appropriate font attribute.</span></span>

<span data-ttu-id="3fee9-362">Voici comment le menu est défini dans le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="3fee9-362">Here is how the menu is defined in the resource-definition file.</span></span> <span data-ttu-id="3fee9-363">Notez que les chaînes pour les éléments de menu normal, gras, italique et souligné sont assignées au moment de l’exécution, de sorte que leurs chaînes sont vides dans le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="3fee9-363">Note that the strings for the Regular, Bold, Italic, and Underline menu items are assigned at run time, so their strings are empty in the resource-definition file.</span></span>


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



<span data-ttu-id="3fee9-364">La procédure de fenêtre de l’application traite les messages impliqués dans l’utilisation d’éléments de menu owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="3fee9-364">The application's window procedure processes the messages involved in using owner-drawn menu items.</span></span> <span data-ttu-id="3fee9-365">L’application utilise le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3fee9-365">The application uses the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to do the following:</span></span>

-   <span data-ttu-id="3fee9-366">Définissez l’indicateur de **\_ OwnerDraw OwnerDraw** pour les éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-366">Set the **MF\_OWNERDRAW** flag for the menu items.</span></span>
-   <span data-ttu-id="3fee9-367">Définissez les chaînes de texte pour les éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-367">Set the text strings for the menu items.</span></span>
-   <span data-ttu-id="3fee9-368">Obtient les handles des polices utilisées pour dessiner les éléments.</span><span class="sxs-lookup"><span data-stu-id="3fee9-368">Obtain handles of the fonts used to draw the items.</span></span>
-   <span data-ttu-id="3fee9-369">Obtient les valeurs de couleur de texte et d’arrière-plan pour les éléments de menu sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="3fee9-369">Obtain the text and background color values for selected menu items.</span></span>

<span data-ttu-id="3fee9-370">Les chaînes de texte et les poignées de police sont stockées dans un tableau de structures MYITEM définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-370">The text strings and font handles are stored in an array of application-defined MYITEM structures.</span></span> <span data-ttu-id="3fee9-371">La fonction GetAFont définie par l’application crée une police qui correspond à l’attribut de police spécifié et retourne un handle à la police.</span><span class="sxs-lookup"><span data-stu-id="3fee9-371">The application-defined GetAFont function creates a font that corresponds to the specified font attribute and returns a handle to the font.</span></span> <span data-ttu-id="3fee9-372">Les descripteurs sont détruits pendant le traitement du message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-372">The handles are destroyed during the processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>

<span data-ttu-id="3fee9-373">Pendant le traitement du message [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) , l’exemple obtient la largeur et la hauteur d’une chaîne d’élément de menu et copie ces valeurs dans la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-373">During the processing of the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message, the example gets the width and height of a menu-item string and copies these values into the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure.</span></span> <span data-ttu-id="3fee9-374">Le système utilise les valeurs de largeur et de hauteur pour calculer la taille du menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-374">The system uses the width and height values to calculate the size of the menu.</span></span>

<span data-ttu-id="3fee9-375">Pendant le traitement du message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) , la chaîne de l’élément de menu est dessinée avec l’espace à gauche en regard de la chaîne pour la bitmap de coche.</span><span class="sxs-lookup"><span data-stu-id="3fee9-375">During the processing of the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message, the menu item's string is drawn with room left next to the string for the check-mark bitmap.</span></span> <span data-ttu-id="3fee9-376">Si l’utilisateur sélectionne l’élément, le texte et les couleurs d’arrière-plan sélectionnés sont utilisés pour dessiner l’élément.</span><span class="sxs-lookup"><span data-stu-id="3fee9-376">If the user selects the item, the selected text and background colors are used to draw the item.</span></span>


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



### <a name="example-of-owner-drawn-menu-items"></a><span data-ttu-id="3fee9-377">Exemple d’éléments de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="3fee9-377">Example of Owner-Drawn Menu Items</span></span>

<span data-ttu-id="3fee9-378">L’exemple de cette rubrique utilise des éléments de menu owner-drawn dans un menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-378">The example in this topic uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="3fee9-379">Les éléments de menu sélectionnent des attributs de police spécifiques et l’application affiche chaque élément de menu à l’aide d’une police qui a l’attribut correspondant.</span><span class="sxs-lookup"><span data-stu-id="3fee9-379">The menu items select specific font attributes, and the application displays each menu item using a font that has the corresponding attribute.</span></span> <span data-ttu-id="3fee9-380">Par exemple, l’élément de menu **italique** s’affiche dans une police en italique.</span><span class="sxs-lookup"><span data-stu-id="3fee9-380">For example, the **Italic** menu item is displayed in an italic font.</span></span> <span data-ttu-id="3fee9-381">Le nom du menu **caractère** dans la barre de menus ouvre le menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-381">The **Character** menu name on the menu bar opens the menu.</span></span>

<span data-ttu-id="3fee9-382">La barre de menus et le menu déroulant sont initialement définis par une ressource de modèle de menu étendue.</span><span class="sxs-lookup"><span data-stu-id="3fee9-382">The menu bar and drop-down menu are defined initially by an extended menu-template resource.</span></span> <span data-ttu-id="3fee9-383">Étant donné qu’un modèle de menu ne peut pas spécifier d’éléments owner-drawn, le menu contient initialement quatre éléments de menu texte avec les chaînes suivantes : « Regular », « Bold », « Italic » et « Underline ».</span><span class="sxs-lookup"><span data-stu-id="3fee9-383">Because a menu template cannot specify owner-drawn items, the menu initially contains four text menu items with the following strings: "Regular," "Bold," "Italic," and "Underline."</span></span> <span data-ttu-id="3fee9-384">La procédure de fenêtre de l’application les remplace par des éléments owner-drawn lors du traitement du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-384">The application's window procedure changes these to owner-drawn items when it processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="3fee9-385">Lorsqu’il reçoit le message **WM \_ Create** , la procédure de fenêtre appelle la fonction OnCreate définie par l’application, qui effectue les étapes suivantes pour chaque élément de menu :</span><span class="sxs-lookup"><span data-stu-id="3fee9-385">When it receives the **WM\_CREATE** message, the window procedure calls the application-defined OnCreate function, which performs the following steps for each menu item:</span></span>

-   <span data-ttu-id="3fee9-386">Alloue une structure MYITEM définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-386">Allocates an application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="3fee9-387">Obtient le texte de l’élément de menu et l’enregistre dans la structure MYITEM définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-387">Gets the text of the menu item and saves it in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="3fee9-388">Crée la police utilisée pour afficher l’élément de menu et enregistre son handle dans la structure MYITEM définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-388">Creates the font used to display the menu item and saves its handle in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="3fee9-389">Remplace le type d’élément de menu par **MFT \_ OwnerDraw** et enregistre un pointeur vers la structure MYITEM définie par l’application en tant que données d’élément.</span><span class="sxs-lookup"><span data-stu-id="3fee9-389">Changes the menu item type to **MFT\_OWNERDRAW** and saves a pointer to the application-defined MYITEM structure as item data.</span></span>

<span data-ttu-id="3fee9-390">Étant donné qu’un pointeur vers chaque structure MYITEM définie par l’application est enregistré en tant que données d’élément, il est passé à la procédure de fenêtre conjointement aux messages [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) et [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) pour l’élément de menu correspondant.</span><span class="sxs-lookup"><span data-stu-id="3fee9-390">Because a pointer to each application-defined MYITEM structure is saved as item data, it is passed to the window procedure in conjunction with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages for the corresponding menu item.</span></span> <span data-ttu-id="3fee9-391">Le pointeur est contenu dans le membre **ItemData** des structures [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) et [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-391">The pointer is contained in the **itemData** member of both the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) and [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structures.</span></span>

<span data-ttu-id="3fee9-392">Un message [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) est envoyé pour chaque élément de menu owner-drawn la première fois qu’il est affiché.</span><span class="sxs-lookup"><span data-stu-id="3fee9-392">A [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message is sent for each owner-drawn menu item the first time it is displayed.</span></span> <span data-ttu-id="3fee9-393">L’application traite ce message en sélectionnant la police de l’élément de menu dans un contexte de périphérique, puis en déterminant l’espace requis pour afficher le texte de l’élément de menu dans cette police.</span><span class="sxs-lookup"><span data-stu-id="3fee9-393">The application processes this message by selecting the font for the menu item into a device context and then determining the space required to display the menu item text in that font.</span></span> <span data-ttu-id="3fee9-394">La police et le texte des éléments de menu sont spécifiés par la structure de l’élément de menu `MYITEM` (la structure définie par l’application).</span><span class="sxs-lookup"><span data-stu-id="3fee9-394">The font and menu item text are both specified by the menu item's `MYITEM` structure (the structure defined by the application).</span></span> <span data-ttu-id="3fee9-395">L’application détermine la taille du texte à l’aide de la fonction [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-395">The application determines the size of the text by using the [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) function.</span></span>

<span data-ttu-id="3fee9-396">La procédure de fenêtre traite le message [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) en affichant le texte de l’élément de menu dans la police appropriée.</span><span class="sxs-lookup"><span data-stu-id="3fee9-396">The window procedure processes the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message by displaying the menu item text in the appropriate font.</span></span> <span data-ttu-id="3fee9-397">La police et le texte des éléments de menu sont spécifiés par la structure de l’élément de menu `MYITEM` .</span><span class="sxs-lookup"><span data-stu-id="3fee9-397">The font and menu item text are both specified by the menu item's `MYITEM` structure.</span></span> <span data-ttu-id="3fee9-398">L’application sélectionne le texte et les couleurs d’arrière-plan appropriés à l’état de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-398">The application selects text and background colors appropriate to the menu item's state.</span></span>

<span data-ttu-id="3fee9-399">La procédure de fenêtre traite le message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) pour détruire les polices et libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3fee9-399">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message to destroy fonts and free memory.</span></span> <span data-ttu-id="3fee9-400">L’application supprime la police et libère la structure MYITEM définie par l’application pour chaque élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-400">The application deletes the font and frees the application-defined MYITEM structure for each menu item.</span></span>

<span data-ttu-id="3fee9-401">Voici les parties pertinentes du fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-401">The following are the relevant portions of the application's header file.</span></span>


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



<span data-ttu-id="3fee9-402">Voici les parties pertinentes de la procédure de fenêtre de l’application et de ses fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="3fee9-402">The following are the relevant portions of the application's window procedure and its associated functions.</span></span>


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



## <a name="using-custom-check-mark-bitmaps"></a><span data-ttu-id="3fee9-403">Utilisation de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-403">Using Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="3fee9-404">Le système fournit une image bitmap de coche par défaut pour l’affichage à côté d’un élément de menu sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3fee9-404">The system provides a default check-mark bitmap for displaying next to a menu item that is selected.</span></span> <span data-ttu-id="3fee9-405">Vous pouvez personnaliser un élément de menu individuel en fournissant une paire de bitmaps pour remplacer la bitmap de coche par défaut.</span><span class="sxs-lookup"><span data-stu-id="3fee9-405">You can customize an individual menu item by providing a pair of bitmaps to replace the default check-mark bitmap.</span></span> <span data-ttu-id="3fee9-406">Le système affiche une image bitmap lorsque l’élément est sélectionné et l’autre quand il est clair.</span><span class="sxs-lookup"><span data-stu-id="3fee9-406">The system displays one bitmap when the item is selected and the other when it is clear.</span></span> <span data-ttu-id="3fee9-407">Cette section décrit les étapes nécessaires à la création et à l’utilisation de bitmaps de coche personnalisées.</span><span class="sxs-lookup"><span data-stu-id="3fee9-407">This section describes the steps involved in creating and using custom check-mark bitmaps.</span></span>

-   [<span data-ttu-id="3fee9-408">Création de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-408">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
-   [<span data-ttu-id="3fee9-409">Association de bitmaps à un élément de menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-409">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
-   [<span data-ttu-id="3fee9-410">Définition de l’attribut coche</span><span class="sxs-lookup"><span data-stu-id="3fee9-410">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
-   [<span data-ttu-id="3fee9-411">Simulation de cases à cocher dans un menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-411">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
-   [<span data-ttu-id="3fee9-412">Exemple d’utilisation de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-412">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a><span data-ttu-id="3fee9-413">Création de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-413">Creating Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="3fee9-414">Une bitmap de coche personnalisée doit avoir la même taille que la bitmap de coche par défaut.</span><span class="sxs-lookup"><span data-stu-id="3fee9-414">A custom check-mark bitmap must be the same size as the default check-mark bitmap.</span></span> <span data-ttu-id="3fee9-415">Vous pouvez récupérer la taille de coche par défaut de la bitmap en appelant la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-415">You can retrieve the default check-mark size of the bitmap by calling the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="3fee9-416">Le mot de poids faible de la valeur de retour de cette fonction spécifie la largeur ; le mot de poids fort spécifie la hauteur.</span><span class="sxs-lookup"><span data-stu-id="3fee9-416">The low-order word of this function's return value specifies the width; the high-order word specifies the height.</span></span>

<span data-ttu-id="3fee9-417">Vous pouvez utiliser des ressources bitmap pour fournir des bitmaps de coche.</span><span class="sxs-lookup"><span data-stu-id="3fee9-417">You can use bitmap resources to provide check-mark bitmaps.</span></span> <span data-ttu-id="3fee9-418">Toutefois, étant donné que la taille de bitmap requise varie selon le type d’affichage, vous devrez peut-être redimensionner l’image bitmap au moment de l’exécution à l’aide de la fonction [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-418">However, because the required bitmap size varies depending on the display type, you may need to resize the bitmap at run time by using the [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function.</span></span> <span data-ttu-id="3fee9-419">En fonction de la bitmap, la distorsion causée par le dimensionnement peut produire des résultats inacceptables.</span><span class="sxs-lookup"><span data-stu-id="3fee9-419">Depending on the bitmap, the distortion caused by sizing could produce unacceptable results.</span></span>

<span data-ttu-id="3fee9-420">Au lieu d’utiliser une ressource bitmap, vous pouvez créer une bitmap au moment de l’exécution à l’aide des fonctions GDI.</span><span class="sxs-lookup"><span data-stu-id="3fee9-420">Instead of using a bitmap resource, you can create a bitmap at run time by using GDI functions.</span></span>

<span data-ttu-id="3fee9-421">**Pour créer une bitmap au moment de l’exécution**</span><span class="sxs-lookup"><span data-stu-id="3fee9-421">**To create a bitmap at run time**</span></span>

1.  <span data-ttu-id="3fee9-422">Utilisez la fonction [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) pour créer un contexte de périphérique compatible avec celui utilisé par la fenêtre principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-422">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the one used by the application's main window.</span></span>

    <span data-ttu-id="3fee9-423">Le paramètre *HDC* de la fonction peut spécifier une valeur **null** ou la valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="3fee9-423">The function's *hdc* parameter can specify either **NULL** or the return value from the function.</span></span> <span data-ttu-id="3fee9-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) retourne un handle vers le contexte de périphérique (Device Context) compatible.</span><span class="sxs-lookup"><span data-stu-id="3fee9-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) returns a handle to the compatible device context.</span></span>

2.  <span data-ttu-id="3fee9-425">Utilisez la fonction [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) pour créer une image bitmap compatible avec la fenêtre principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-425">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window.</span></span>

    <span data-ttu-id="3fee9-426">Les paramètres *nWidth* et *nHeight* de cette fonction définissent la taille de l’image bitmap. ils doivent spécifier les informations de largeur et de hauteur retournées par la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-426">This function's *nWidth* and *nHeight* parameters set the size of the bitmap; they should specify the width and height information returned by the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="3fee9-427">Vous pouvez également utiliser la fonction [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) pour créer une image bitmap monochrome.</span><span class="sxs-lookup"><span data-stu-id="3fee9-427">You can also use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>

     

3.  <span data-ttu-id="3fee9-428">Utilisez la fonction [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) pour sélectionner la bitmap dans le contexte de périphérique compatible.</span><span class="sxs-lookup"><span data-stu-id="3fee9-428">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="3fee9-429">Utilisez les fonctions de dessin GDI, telles que [**ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) et [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), pour dessiner une image dans la bitmap, ou utilisez des fonctions telles que [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) et [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) pour copier une image dans la bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fee9-429">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap, or use functions such as [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) and [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) to copy an image into the bitmap.</span></span>

<span data-ttu-id="3fee9-430">Pour plus d’informations, consultez [bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="3fee9-430">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="associating-bitmaps-with-a-menu-item"></a><span data-ttu-id="3fee9-431">Association de bitmaps à un élément de menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-431">Associating Bitmaps with a Menu Item</span></span>

<span data-ttu-id="3fee9-432">Vous associez une paire de bitmaps de coche à un élément de menu en passant les descripteurs des bitmaps à la fonction [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-432">You associate a pair of check-mark bitmaps with a menu item by passing the handles of the bitmaps to the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span> <span data-ttu-id="3fee9-433">Le paramètre *hBitmapUnchecked* identifie l’image bitmap en clair et le paramètre *hBitmapChecked* identifie la bitmap sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="3fee9-433">The *hBitmapUnchecked* parameter identifies the clear bitmap, and the *hBitmapChecked* parameter identifies the selected bitmap.</span></span> <span data-ttu-id="3fee9-434">Si vous souhaitez supprimer une des deux cases à cocher d’un élément de menu, vous pouvez définir le paramètre *hBitmapUnchecked* ou *hBitmapChecked* , ou les deux, sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3fee9-434">If you want to remove one or both check marks from a menu item, you can set the *hBitmapUnchecked* or *hBitmapChecked* parameter, or both, to **NULL**.</span></span>

### <a name="setting-the-check-mark-attribute"></a><span data-ttu-id="3fee9-435">Définition de l’attribut coche</span><span class="sxs-lookup"><span data-stu-id="3fee9-435">Setting the Check-mark Attribute</span></span>

<span data-ttu-id="3fee9-436">La fonction [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) définit l’attribut coche d’un élément de menu sur sélectionné ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="3fee9-436">The [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) function sets a menu item's check-mark attribute to either selected or cleared.</span></span> <span data-ttu-id="3fee9-437">Vous pouvez spécifier la **valeur \_ activée MF** pour définir l’attribut case à cocher sur sélectionné et la valeur **MF \_ non vérifiée** pour le définir sur Clear.</span><span class="sxs-lookup"><span data-stu-id="3fee9-437">You can specify the **MF\_CHECKED** value to set the check-mark attribute to selected and the **MF\_UNCHECKED** value to set it to clear.</span></span>

<span data-ttu-id="3fee9-438">Vous pouvez également définir l’état d’activation d’un élément de menu à l’aide de la fonction [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-438">You can also set the check state of a menu item by using the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="3fee9-439">Parfois, un groupe d’éléments de menu représente un ensemble d’options s’excluant mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3fee9-439">Sometimes a group of menu items represents a set of mutually exclusive options.</span></span> <span data-ttu-id="3fee9-440">À l’aide de la fonction [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) , vous pouvez vérifier un élément de menu tout en supprimant simultanément la coche de tous les autres éléments de menu du groupe.</span><span class="sxs-lookup"><span data-stu-id="3fee9-440">By using the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function, you can check one menu item while simultaneously removing the check mark from all other menu items in the group.</span></span>

### <a name="simulating-check-boxes-in-a-menu"></a><span data-ttu-id="3fee9-441">Simulation de cases à cocher dans un menu</span><span class="sxs-lookup"><span data-stu-id="3fee9-441">Simulating Check Boxes in a Menu</span></span>

<span data-ttu-id="3fee9-442">Cette rubrique contient un exemple qui montre comment simuler des cases à cocher dans un menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-442">This topic contains an example that shows how to simulate check boxes in a menu.</span></span> <span data-ttu-id="3fee9-443">L’exemple contient un menu de caractères dont les éléments permettent à l’utilisateur de définir les attributs gras, italique et souligné de la police actuelle.</span><span class="sxs-lookup"><span data-stu-id="3fee9-443">The example contains a Character menu whose items allow the user to set the bold, italic, and underline attributes of the current font.</span></span> <span data-ttu-id="3fee9-444">Lorsqu’un attribut de police est activé, une coche s’affiche dans la case à cocher en regard de l’élément de menu correspondant. Sinon, une case à cocher vide est affichée en regard de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3fee9-444">When a font attribute is in effect, a check mark is displayed in the check box next to the corresponding menu item; otherwise, an empty check box is displayed next to the item.</span></span>

<span data-ttu-id="3fee9-445">L’exemple remplace le bitmap de coche par défaut par deux bitmaps : un bitmap avec une case à cocher activée et l’image bitmap avec une zone vide.</span><span class="sxs-lookup"><span data-stu-id="3fee9-445">The example replaces the default check-mark bitmap with two bitmaps: a bitmap with a selected check box and the bitmap with an empty box.</span></span> <span data-ttu-id="3fee9-446">La bitmap de case à cocher sélectionnée s’affiche en regard de l’élément de menu gras, italique ou souligné lorsque l’attribut coche de l’élément est défini sur **MF \_ activé**.</span><span class="sxs-lookup"><span data-stu-id="3fee9-446">The selected check box bitmap is displayed next to the Bold, Italic, or Underline menu item when the item's check-mark attribute is set to **MF\_CHECKED**.</span></span> <span data-ttu-id="3fee9-447">La case à cocher vide ou vide s’affiche lorsque l’attribut coche est défini sur **MF désactivé \_**.</span><span class="sxs-lookup"><span data-stu-id="3fee9-447">The clear or empty check box bitmap is displayed when the check-mark attribute is set to **MF\_UNCHECKED**.</span></span>

<span data-ttu-id="3fee9-448">Le système fournit une image bitmap prédéfinie qui contient les images utilisées pour les cases à cocher et les cases d’option.</span><span class="sxs-lookup"><span data-stu-id="3fee9-448">The system provides a predefined bitmap that contains the images used for check boxes and radio buttons.</span></span> <span data-ttu-id="3fee9-449">L’exemple isole les cases à cocher sélectionnées et vides, les copie dans deux bitmaps distinctes, puis les utilise comme images bitmap sélectionnées et effacées pour les éléments du menu **caractère** .</span><span class="sxs-lookup"><span data-stu-id="3fee9-449">The example isolates the selected and empty check boxes, copies them to two separate bitmaps, and then uses them as the selected and cleared bitmaps for items in the **Character** menu.</span></span>

<span data-ttu-id="3fee9-450">Pour récupérer un handle vers la bitmap de case à cocher définie par le système, l’exemple appelle la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , en spécifiant **null** comme paramètre *HINSTANCE* et **OBM \_ cases à cocher** comme paramètre *lpBitmapName* .</span><span class="sxs-lookup"><span data-stu-id="3fee9-450">To retrieve a handle to the system-defined check box bitmap, the example calls the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, specifying **NULL** as the *hInstance* parameter and **OBM\_CHECKBOXES** as the *lpBitmapName* parameter.</span></span> <span data-ttu-id="3fee9-451">Étant donné que les images de la bitmap ont la même taille, l’exemple peut les isoler en divisant la largeur et la hauteur de la bitmap par le nombre d’images dans ses lignes et colonnes.</span><span class="sxs-lookup"><span data-stu-id="3fee9-451">Because the images in the bitmap are all the same size, the example can isolate them by dividing the bitmap width and height by the number of images in its rows and columns.</span></span>

<span data-ttu-id="3fee9-452">La partie suivante d’un fichier de définition de ressource montre comment les éléments de menu du menu **caractère** sont définis.</span><span class="sxs-lookup"><span data-stu-id="3fee9-452">The following portion of a resource-definition file shows how the menu items in the **Character** menu are defined.</span></span> <span data-ttu-id="3fee9-453">Notez qu’aucun attribut de police n’est défini au départ. par conséquent, l’attribut coche de l’élément **normal** est défini sur sélectionné et, par défaut, l’attribut coche des éléments restants est défini sur Clear.</span><span class="sxs-lookup"><span data-stu-id="3fee9-453">Note that no font attributes are in effect initially, so the check-mark attribute for the **Regular** item is set to selected and, by default, the check-mark attribute of the remaining items is set to clear.</span></span>


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



<span data-ttu-id="3fee9-454">Voici le contenu pertinent du fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-454">Here are the relevant contents of the application's header file.</span></span>


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



<span data-ttu-id="3fee9-455">L’exemple suivant montre les parties de la procédure de fenêtre qui créent les bitmaps de coche. Définissez l’attribut coche des éléments de menu **gras**, **italique** et **souligné** . et détruisez les bitmaps de coche.</span><span class="sxs-lookup"><span data-stu-id="3fee9-455">The following example shows the portions of the window procedure that create the check-mark bitmaps; set the check-mark attribute of the **Bold**, **Italic**, and **Underline** menu items; and destroy check-mark bitmaps.</span></span>


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



### <a name="example-of-using-custom-check-mark-bitmaps"></a><span data-ttu-id="3fee9-456">Exemple d’utilisation de bitmaps de coche personnalisées</span><span class="sxs-lookup"><span data-stu-id="3fee9-456">Example of Using Custom Check-mark Bitmaps</span></span>

<span data-ttu-id="3fee9-457">L’exemple de cette rubrique assigne des bitmaps de coche personnalisée à des éléments de menu dans deux menus.</span><span class="sxs-lookup"><span data-stu-id="3fee9-457">The example in this topic assigns custom check-mark bitmaps to menu items in two menus.</span></span> <span data-ttu-id="3fee9-458">Les éléments de menu du premier menu spécifient des attributs de caractères : gras, italique et souligné.</span><span class="sxs-lookup"><span data-stu-id="3fee9-458">The menu items in the first menu specify character attributes: bold, italic, and underline.</span></span> <span data-ttu-id="3fee9-459">Chaque élément de menu peut être sélectionné ou effacé.</span><span class="sxs-lookup"><span data-stu-id="3fee9-459">Each menu item can be either selected or cleared.</span></span> <span data-ttu-id="3fee9-460">Pour ces éléments de menu, l’exemple utilise des bitmaps de coche qui ressemblent aux États sélectionnés et désactivés d’un contrôle de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="3fee9-460">For these menu items, the example uses check-mark bitmaps that resemble the selected and cleared states of a check box control.</span></span>

<span data-ttu-id="3fee9-461">Les éléments de menu du deuxième menu spécifient les paramètres d’alignement des paragraphes : gauche, Centre et droite.</span><span class="sxs-lookup"><span data-stu-id="3fee9-461">The menu items in the second menu specify paragraph alignment settings: left, centered, and right.</span></span> <span data-ttu-id="3fee9-462">Un seul de ces éléments de menu est sélectionné à tout moment.</span><span class="sxs-lookup"><span data-stu-id="3fee9-462">Only one of these menu items is selected at any time.</span></span> <span data-ttu-id="3fee9-463">Pour ces éléments de menu, l’exemple utilise des bitmaps de coche qui ressemblent aux États sélectionnés et clairs d’un contrôle de case d’option.</span><span class="sxs-lookup"><span data-stu-id="3fee9-463">For these menu items, the example uses check-mark bitmaps that resemble the selected and clear states of a radio button control.</span></span>

<span data-ttu-id="3fee9-464">La procédure de fenêtre traite le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) en appelant la fonction OnCreate définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-464">The window procedure processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message by calling the application-defined OnCreate function.</span></span> <span data-ttu-id="3fee9-465">`OnCreate` crée les quatre bitmaps de coche et les assigne à leurs éléments de menu appropriés à l’aide de la fonction [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-465">`OnCreate` creates the four check-mark bitmaps and then assigns them to their appropriate menu items by using the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span>

<span data-ttu-id="3fee9-466">Pour créer chaque bitmap, OnCreate appelle la fonction CreateMenuBitmaps définie par l’application, en spécifiant un pointeur vers une fonction de dessin spécifique à la bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fee9-466">To create each bitmap, OnCreate calls the application-defined CreateMenuBitmaps function, specifying a pointer to a bitmap-specific drawing function.</span></span> <span data-ttu-id="3fee9-467">CreateMenuBitmaps crée une image bitmap monochrome de la taille requise, la sélectionne dans un contexte de périphérique de mémoire et efface l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3fee9-467">CreateMenuBitmaps creates a monochrome bitmap of the required size, selects it into a memory device context, and erases the background.</span></span> <span data-ttu-id="3fee9-468">Ensuite, il appelle la fonction de dessin spécifiée pour remplir le premier plan.</span><span class="sxs-lookup"><span data-stu-id="3fee9-468">Then it calls the specified drawing function to fill in the foreground.</span></span>

<span data-ttu-id="3fee9-469">Les quatre fonctions de dessin définies par l’application sont DrawCheck, DrawUncheck, **DrawRadioCheck** et DrawRadioUncheck.</span><span class="sxs-lookup"><span data-stu-id="3fee9-469">The four application-defined drawing functions are DrawCheck, DrawUncheck, **DrawRadioCheck**, and DrawRadioUncheck.</span></span> <span data-ttu-id="3fee9-470">Ils dessinent un rectangle avec un X, un rectangle vide, une ellipse contenant une Ellipse remplie plus petite et une ellipse vide, respectivement.</span><span class="sxs-lookup"><span data-stu-id="3fee9-470">They draw a rectangle with an X, an empty rectangle, an ellipse containing a smaller filled ellipse, and an empty ellipse, respectively.</span></span>

<span data-ttu-id="3fee9-471">La procédure de fenêtre traite le message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) en supprimant les bitmaps de coche.</span><span class="sxs-lookup"><span data-stu-id="3fee9-471">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message by deleting the check-mark bitmaps.</span></span> <span data-ttu-id="3fee9-472">Il récupère chaque handle de bitmap à l’aide de la fonction [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) , puis passe un handle à la fonction.</span><span class="sxs-lookup"><span data-stu-id="3fee9-472">It retrieves each bitmap handle by using the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function and then passes a handle to the function.</span></span>

<span data-ttu-id="3fee9-473">Quand l’utilisateur choisit un élément de menu, un message de [**\_ commande WM**](wm-command.md) est envoyé à la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="3fee9-473">When the user chooses a menu item, a [**WM\_COMMAND**](wm-command.md) message is sent to the owner window.</span></span> <span data-ttu-id="3fee9-474">Pour les éléments de menu du menu **caractère** , la procédure de fenêtre appelle la fonction CheckCharacterItem définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-474">For menu items on the **Character** menu, the window procedure calls the application-defined CheckCharacterItem function.</span></span> <span data-ttu-id="3fee9-475">Pour les éléments du menu **paragraphe** , la procédure de fenêtre appelle la fonction CheckParagraphItem définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-475">For items on the **Paragraph** menu, the window procedure calls the application-defined CheckParagraphItem function.</span></span>

<span data-ttu-id="3fee9-476">Chaque élément du menu **caractère** peut être sélectionné et effacé indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3fee9-476">Each item on the **Character** menu can be selected and cleared independently.</span></span> <span data-ttu-id="3fee9-477">Par conséquent, CheckCharacterItem bascule simplement l’état d’activation de l’élément de menu spécifié.</span><span class="sxs-lookup"><span data-stu-id="3fee9-477">Therefore, CheckCharacterItem simply switches the specified menu item's check state.</span></span> <span data-ttu-id="3fee9-478">Tout d’abord, la fonction appelle la fonction [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) pour récupérer l’état actuel de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-478">First, the function calls the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function to get the current menu item state.</span></span> <span data-ttu-id="3fee9-479">Ensuite, il bascule l’indicateur d’état **\_ activé MFS** et définit le nouvel État en appelant la fonction [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-479">Then it switches the **MFS\_CHECKED** state flag and sets the new state by calling the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="3fee9-480">Contrairement aux attributs de caractères, un seul alignement de paragraphe peut être sélectionné à la fois.</span><span class="sxs-lookup"><span data-stu-id="3fee9-480">Unlike character attributes, only one paragraph alignment can be selected at a time.</span></span> <span data-ttu-id="3fee9-481">Par conséquent, CheckParagraphItem vérifie l’élément de menu spécifié et supprime la coche de tous les autres éléments du menu.</span><span class="sxs-lookup"><span data-stu-id="3fee9-481">Therefore, CheckParagraphItem checks the specified menu item and removes the check mark from all other items on the menu.</span></span> <span data-ttu-id="3fee9-482">Pour ce faire, il appelle la fonction [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .</span><span class="sxs-lookup"><span data-stu-id="3fee9-482">To do so, it calls the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function.</span></span>

<span data-ttu-id="3fee9-483">Voici les parties pertinentes du fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="3fee9-483">Following are the relevant portions of the application's header file.</span></span>


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



<span data-ttu-id="3fee9-484">Voici les parties pertinentes de la procédure de fenêtre de l’application et des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="3fee9-484">The following are the relevant portions of the application's window procedure and related functions.</span></span>


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



 

 