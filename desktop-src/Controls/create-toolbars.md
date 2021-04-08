---
title: Comment créer des barres d’outils
description: Pour créer une barre d’outils, utilisez la fonction CreateWindowEx, en spécifiant la classe de fenêtre TOOLBARCLASSNAME.
ms.assetid: 5D060291-6ACF-478C-97EC-CD8BD55D1FFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69cd40338eaebc0d9de852519dce34dc9bc8aa4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730413"
---
# <a name="how-to-create-toolbars"></a><span data-ttu-id="8ce3c-103">Comment créer des barres d’outils</span><span class="sxs-lookup"><span data-stu-id="8ce3c-103">How to Create Toolbars</span></span>

<span data-ttu-id="8ce3c-104">Pour créer une barre d’outils, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre [**TOOLBARCLASSNAME**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="8ce3c-104">To create a toolbar, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**TOOLBARCLASSNAME**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="8ce3c-105">La barre d’outils obtenue ne contient initialement aucun bouton.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-105">The resulting toolbar initially contains no buttons.</span></span> <span data-ttu-id="8ce3c-106">Ajoutez des boutons à la barre d’outils en utilisant le message [**to \_ ADDBUTTONS**](tb-addbuttons.md) ou [**to \_ INSERTBUTTON**](tb-insertbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="8ce3c-106">Add buttons to the toolbar by using the [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) message.</span></span> <span data-ttu-id="8ce3c-107">Vous devez envoyer le message de [**\_ taille automatique to**](tb-autosize.md) une fois que tous les éléments et chaînes ont été insérés dans le contrôle, afin que la barre d’outils recalcule sa taille en fonction de son contenu.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-107">You must send the [**TB\_AUTOSIZE**](tb-autosize.md) message after all the items and strings have been inserted into the control, to cause the toolbar to recalculate its size based on its content.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8ce3c-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="8ce3c-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8ce3c-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="8ce3c-109">Technologies</span></span>

-   [<span data-ttu-id="8ce3c-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="8ce3c-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8ce3c-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="8ce3c-111">Prerequisites</span></span>

-   <span data-ttu-id="8ce3c-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="8ce3c-112">C/C++</span></span>
-   <span data-ttu-id="8ce3c-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="8ce3c-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8ce3c-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="8ce3c-114">Instructions</span></span>

### <a name="create-a-toolbar"></a><span data-ttu-id="8ce3c-115">Créer une barre d’outils</span><span class="sxs-lookup"><span data-stu-id="8ce3c-115">Create a Toolbar</span></span>

<span data-ttu-id="8ce3c-116">L’exemple de code suivant crée la barre d’outils présentée dans l’illustration, à l’aide des icônes système standard.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-116">The following example code creates the toolbar shown in the illustration, using standard system icons.</span></span> <span data-ttu-id="8ce3c-117">Le bouton **Enregistrer** est initialement désactivé.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-117">The **Save** button is initially disabled.</span></span>

![capture d’écran montrant une boîte de dialogue avec trois éléments de barre d’outils disposés horizontalement, chacun d’entre eux ayant une icône et une étiquette de texte](images/tb-codesample1.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateSimpleToolbar(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0, 
                                      hWndParent, NULL, g_hInst, NULL);
        
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize,   // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, (INT_PTR)L"Save"}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



<span data-ttu-id="8ce3c-119">L’exemple suivant crée la même barre d’outils quasiment de la même façon, mais dans ce cas, les chaînes sont lues à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-119">The following example creates the same toolbar in much the same way, but in this case, the strings are read from a resource.</span></span>


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarFromResource(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK, // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Load the text from a resource.
    
    // In the string table, the text for all buttons is a single entry that 
    // appears as "~New~Open~Save~~". The separator character is arbitrary, 
    // but it must appear as the first character of the string. The message 
    // returns the index of the first item, and the items are numbered 
    // consecutively.
    
    int iNew = SendMessage(hWndToolbar, TB_ADDSTRING, 
                           (WPARAM)g_hInst, (LPARAM)IDS_NEW); 
 
    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew + 1},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, iNew + 2}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



## <a name="related-topics"></a><span data-ttu-id="8ce3c-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ce3c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ce3c-121">Utilisation des contrôles ToolBar</span><span class="sxs-lookup"><span data-stu-id="8ce3c-121">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="8ce3c-122">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="8ce3c-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 