---
title: Comment créer un contrôle onglet dans la fenêtre principale
description: L’exemple de cette section montre comment créer un contrôle onglet et l’afficher dans la zone cliente de la fenêtre principale de l’application.
ms.assetid: 24157B8B-177B-471C-9DA0-548D09EA5F89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686a9a4fe4f6be95ccdcf3bbcb597c2c48ff3b2d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463770"
---
# <a name="how-to-create-a-tab-control-in-the-main-window"></a><span data-ttu-id="2ca59-103">Comment créer un contrôle onglet dans la fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="2ca59-103">How to Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="2ca59-104">L’exemple de cette section montre comment créer un contrôle onglet et l’afficher dans la zone cliente de la fenêtre principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="2ca59-104">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="2ca59-105">L’application affiche une troisième fenêtre (un contrôle statique) dans la zone d’affichage du contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="2ca59-105">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="2ca59-106">La fenêtre parente positionne et dimensionne le contrôle onglet et le contrôle statique lors du traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) .</span><span class="sxs-lookup"><span data-stu-id="2ca59-106">The parent window positions and sizes the tab control and static control when it processes the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

<span data-ttu-id="2ca59-107">Cet exemple comporte sept onglets, un pour chaque jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="2ca59-107">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="2ca59-108">Lorsque l’utilisateur sélectionne un onglet, l’application affiche le nom du jour correspondant dans le contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="2ca59-108">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2ca59-109">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="2ca59-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2ca59-110">Technologies</span><span class="sxs-lookup"><span data-stu-id="2ca59-110">Technologies</span></span>

-   [<span data-ttu-id="2ca59-111">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="2ca59-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2ca59-112">Prérequis</span><span class="sxs-lookup"><span data-stu-id="2ca59-112">Prerequisites</span></span>

-   <span data-ttu-id="2ca59-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="2ca59-113">C/C++</span></span>
-   <span data-ttu-id="2ca59-114">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="2ca59-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2ca59-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="2ca59-115">Instructions</span></span>

### <a name="create-a-tab-control-in-the-main-window"></a><span data-ttu-id="2ca59-116">Créer un contrôle onglet dans la fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="2ca59-116">Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="2ca59-117">La fonction suivante crée le contrôle onglet et ajoute un onglet pour chaque jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="2ca59-117">The following function creates the tab control and adds a tab for each day of the week.</span></span> <span data-ttu-id="2ca59-118">Les noms des jours sont définis en tant que ressources de type chaîne, numérotés de manière consécutive à partir de \_ l’ID dimanche (défini dans le fichier d’en-tête de ressource de l’application).</span><span class="sxs-lookup"><span data-stu-id="2ca59-118">The names of the days are defined as string resources, consecutively numbered starting with IDS\_SUNDAY (defined in the application's resource header file).</span></span> <span data-ttu-id="2ca59-119">La fenêtre parente et le contrôle onglet doivent avoir le style de fenêtre [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="2ca59-119">Both the parent window and the tab control must have the [**WS\_CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) window style.</span></span> <span data-ttu-id="2ca59-120">La fonction d’initialisation de l’application appelle cette fonction après la création de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="2ca59-120">The application's initialization function calls this function after creating the main window.</span></span>


```C++
#define DAYS_IN_WEEK 7

// Creates a tab control, sized to fit the specified parent window's client
//   area, and adds some tabs. 
// Returns the handle to the tab control. 
// hwndParent - parent window (the application's main window). 
// 
HWND DoCreateTabControl(HWND hwndParent) 
{ 
    RECT rcClient; 
    INITCOMMONCONTROLSEX icex;
    HWND hwndTab; 
    TCITEM tie; 
    int i; 
    TCHAR achTemp[256];  // Temporary buffer for strings.
 
    // Initialize common controls.
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&icex);
    
    // Get the dimensions of the parent window's client area, and 
    // create a tab control child window of that size. Note that g_hInst
    // is the global instance handle.
    GetClientRect(hwndParent, &rcClient); 
    hwndTab = CreateWindow(WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, rcClient.right, rcClient.bottom, 
        hwndParent, NULL, g_hInst, NULL); 
    if (hwndTab == NULL)
    { 
        return NULL; 
    }
 
    // Add tabs for each day of the week. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = achTemp; 
 
    for (i = 0; i < DAYS_IN_WEEK; i++) 
    { 
        // Load the day string from the string resources. Note that
        // g_hInst is the global instance handle.
        LoadString(g_hInst, IDS_SUNDAY + i, 
                achTemp, sizeof(achTemp) / sizeof(achTemp[0])); 
        if (TabCtrl_InsertItem(hwndTab, i, &tie) == -1) 
        { 
            DestroyWindow(hwndTab); 
            return NULL; 
        } 
    } 
    return hwndTab; 
} 
```



<span data-ttu-id="2ca59-121">La fonction suivante crée le contrôle statique qui réside dans la zone d’affichage du contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="2ca59-121">The following function creates the static control that resides in the tab control's display area.</span></span> <span data-ttu-id="2ca59-122">La fonction d’initialisation de l’application appelle cette fonction après la création de la fenêtre principale et du contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="2ca59-122">The application's initialization function calls this function after creating the main window and the tab control.</span></span>


```C++
// Creates a child window (a static control) to occupy the tab control's 
//   display area. 
// Returns the handle to the static control. 
// hwndTab - handle of the tab control. 
// 
HWND DoCreateDisplayWindow(HWND hwndTab) 
{ 
    HWND hwndStatic = CreateWindow(WC_STATIC, L"", 
        WS_CHILD | WS_VISIBLE | WS_BORDER, 
        100, 100, 100, 100,        // Position and dimensions; example only.
        hwndTab, NULL, g_hInst,    // g_hInst is the global instance handle
        NULL); 
    return hwndStatic; 
}
```



<span data-ttu-id="2ca59-123">Les exemples de fonctions suivants sont appelés à partir de la procédure de fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="2ca59-123">The following example functions are called from the application's window procedure.</span></span> <span data-ttu-id="2ca59-124">L’application appelle la `OnSize` fonction lors du traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) pour positionner et dimensionner le contrôle onglet pour l’adapter à la zone cliente de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="2ca59-124">The application calls the `OnSize` function when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to position and size the tab control to fit the main window's client area.</span></span>

<span data-ttu-id="2ca59-125">Lorsqu’un onglet est sélectionné, le contrôle onglet envoie un message [**WM \_ Notify**](wm-notify.md) , en spécifiant le code de notification [TCN \_ selChange](tcn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="2ca59-125">When a tab is selected, the tab control sends a [**WM\_NOTIFY**](wm-notify.md) message, specifying the [TCN\_SELCHANGE](tcn-selchange.md) notification code.</span></span> <span data-ttu-id="2ca59-126">La fonction de l’application `OnNotify` traite ce code de notification en définissant le texte du contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="2ca59-126">The application's `OnNotify` function processes this notification code by setting the text of the static control.</span></span>


```C++
// Handles the WM_SIZE message for the main window by resizing the 
//   tab control. 
// hwndTab - handle of the tab control.
// lParam - the lParam parameter of the WM_SIZE message.
//
HRESULT OnSize(HWND hwndTab, LPARAM lParam)
{
    RECT rc; 

    if (hwndTab == NULL)
        return E_INVALIDARG;

    // Resize the tab control to fit the client are of main window.
     if (!SetWindowPos(hwndTab, HWND_TOP, 0, 0, GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), SWP_SHOWWINDOW))
        return E_FAIL;

    return S_OK;
}

// Handles notifications from the tab control, as follows: 
//   TCN_SELCHANGING - always returns FALSE to allow the user to select a 
//     different tab.  
//   TCN_SELCHANGE - loads a string resource and displays it in a static 
//     control on the selected tab.
// hwndTab - handle of the tab control.
// hwndDisplay - handle of the static control. 
// lParam - the lParam parameter of the WM_NOTIFY message.
//
BOOL OnNotify(HWND hwndTab, HWND hwndDisplay, LPARAM lParam)
{
    TCHAR achTemp[256]; // temporary buffer for strings

    switch (((LPNMHDR)lParam)->code)
        {
            case TCN_SELCHANGING:
                {
                    // Return FALSE to allow the selection to change.
                    return FALSE;
                }

            case TCN_SELCHANGE:
                { 
                    int iPage = TabCtrl_GetCurSel(hwndTab); 

                    // Note that g_hInst is the global instance handle.
                    LoadString(g_hInst, IDS_SUNDAY + iPage, achTemp,
                        sizeof(achTemp) / sizeof(achTemp[0])); 
                    LRESULT result = SendMessage(hwndDisplay, WM_SETTEXT, 0,
                        (LPARAM) achTemp); 
                    break;
                } 
        }
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="2ca59-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ca59-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca59-128">Utilisation des contrôles Tab</span><span class="sxs-lookup"><span data-stu-id="2ca59-128">Using Tab Controls</span></span>](using-tab-controls.md)
</dt> <dt>

<span data-ttu-id="2ca59-129">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="2ca59-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 