---
title: Comment incorporer des contrôles autres que des boutons dans les barres d’outils
description: Les barres d’outils prennent uniquement en charge les boutons ; par conséquent, si votre application nécessite un type de contrôle différent, vous devez créer une fenêtre enfant. L’illustration suivante montre une barre d’outils avec un contrôle d’édition incorporé.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841989"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a><span data-ttu-id="1229b-104">Comment incorporer des contrôles autres que des boutons dans les barres d’outils</span><span class="sxs-lookup"><span data-stu-id="1229b-104">How to Embed Nonbutton Controls in Toolbars</span></span>

<span data-ttu-id="1229b-105">Les barres d’outils prennent uniquement en charge les boutons ; par conséquent, si votre application nécessite un type de contrôle différent, vous devez créer une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="1229b-105">Toolbars support only buttons; therefore, if your application requires a different kind of control, you must create a child window.</span></span> <span data-ttu-id="1229b-106">L’illustration suivante montre une barre d’outils avec un contrôle d’édition incorporé.</span><span class="sxs-lookup"><span data-stu-id="1229b-106">The following illustration shows a toolbar with an embedded edit control.</span></span>

![capture d’écran d’une boîte de dialogue avec un contrôle d’édition dans la barre d’outils, précédant trois icônes de barre d’outils](images/tb-withedit.png)

> [!Note]  
> <span data-ttu-id="1229b-108">Envisagez d’utiliser les [contrôles Rebar](rebar-controls.md) au lieu de placer des contrôles dans les barres d’outils.</span><span class="sxs-lookup"><span data-stu-id="1229b-108">Consider using [Rebar Controls](rebar-controls.md) instead of placing controls in toolbars.</span></span>

 

<span data-ttu-id="1229b-109">N’importe quel type de fenêtre peut être placé dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1229b-109">Any type of window can be placed on a toolbar.</span></span> <span data-ttu-id="1229b-110">L’exemple de code suivant ajoute un contrôle d’édition en tant qu’enfant de la fenêtre de contrôle de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1229b-110">The following example code adds an edit control as a child of the toolbar control window.</span></span> <span data-ttu-id="1229b-111">Étant donné que la barre d’outils est créée, puis que le contrôle d’édition est ajouté, vous devez fournir de l’espace pour le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="1229b-111">Because the toolbar is created and then the edit control added, you must provide space for the edit control.</span></span> <span data-ttu-id="1229b-112">Pour ce faire, vous pouvez ajouter un séparateur en tant qu’espace réservé dans la barre d’outils, en définissant la largeur du séparateur sur le nombre de pixels que vous souhaitez réserver.</span><span class="sxs-lookup"><span data-stu-id="1229b-112">One way to do this is to add a separator as a placeholder in the toolbar, setting the width of the separator to the number of pixels you want to reserve.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1229b-113">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="1229b-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1229b-114">Technologies</span><span class="sxs-lookup"><span data-stu-id="1229b-114">Technologies</span></span>

-   [<span data-ttu-id="1229b-115">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="1229b-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1229b-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="1229b-116">Prerequisites</span></span>

-   <span data-ttu-id="1229b-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="1229b-117">C/C++</span></span>
-   <span data-ttu-id="1229b-118">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="1229b-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1229b-119">Instructions</span><span class="sxs-lookup"><span data-stu-id="1229b-119">Instructions</span></span>

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a><span data-ttu-id="1229b-120">Incorporer un contrôle unbutton dans une barre d’outils</span><span class="sxs-lookup"><span data-stu-id="1229b-120">Embed a Nonbutton Control in a Toolbar</span></span>

<span data-ttu-id="1229b-121">L’extrait de code suivant crée la barre d’outils dans l’illustration précédente.</span><span class="sxs-lookup"><span data-stu-id="1229b-121">The following code snippet creates the toolbar in the preceding illustration.</span></span>


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



<span data-ttu-id="1229b-122">Cet exemple code en dur les dimensions de la fenêtre enfant ; Toutefois, pour créer une application plus robuste, déterminez la taille de la barre d’outils et rendez la fenêtre de contrôle d’édition adaptée.</span><span class="sxs-lookup"><span data-stu-id="1229b-122">This example hard-codes the dimensions of the child window; however, to make a more robust application, determine the size of the toolbar and make the edit control window to fit.</span></span>

<span data-ttu-id="1229b-123">Vous souhaiterez peut-être que les notifications du contrôle d’édition s’affichent dans une autre fenêtre, telle que le parent de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1229b-123">You might want the edit control notifications to go to another window, such as the toolbar's parent.</span></span> <span data-ttu-id="1229b-124">Pour ce faire, créez le contrôle d’édition en tant qu’enfant de la fenêtre parente de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1229b-124">To do this, create the edit control as a child of the toolbar's parent window.</span></span> <span data-ttu-id="1229b-125">Ensuite, remplacez le parent du contrôle d’édition par la barre d’outils comme suit.</span><span class="sxs-lookup"><span data-stu-id="1229b-125">Then change the parent of the edit control to the toolbar as follows.</span></span>


```
SetParent (hWndEdit, hWndToolbar);
```



<span data-ttu-id="1229b-126">Les notifications sont dirigées vers le parent d’origine.</span><span class="sxs-lookup"><span data-stu-id="1229b-126">Notifications go to the original parent.</span></span> <span data-ttu-id="1229b-127">Par conséquent, les messages de contrôle d’édition sont dirigés vers le parent de la barre d’outils, même si la fenêtre d’édition se trouve dans la fenêtre de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1229b-127">Therefore, the edit control messages go to the parent of the toolbar even though the edit window resides in the toolbar window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1229b-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1229b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1229b-129">Utilisation des contrôles ToolBar</span><span class="sxs-lookup"><span data-stu-id="1229b-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="1229b-130">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1229b-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




