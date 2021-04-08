---
title: Comment créer des contrôles Rebar
description: Une application crée un contrôle rebar en appelant la fonction CreateWindowEx, en spécifiant REBARCLASSNAME comme classe de fenêtre.
ms.assetid: F17CC2A4-BDC6-48A6-9AF5-19FCF65CC39A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b38cd49e8e6016dafad5ec07c77be570a5a430
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730444"
---
# <a name="how-to-create-rebar-controls"></a><span data-ttu-id="88726-103">Comment créer des contrôles Rebar</span><span class="sxs-lookup"><span data-stu-id="88726-103">How to Create Rebar Controls</span></span>

<span data-ttu-id="88726-104">Une application crée un contrôle rebar en appelant la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant [**REBARCLASSNAME**](common-control-window-classes.md) comme classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="88726-104">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="88726-105">L’application doit tout d’abord inscrire la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , en spécifiant le \_ bit des classes cool ICC \_ dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="88726-105">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="88726-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="88726-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="88726-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="88726-107">Technologies</span></span>

-   [<span data-ttu-id="88726-108">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="88726-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="88726-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="88726-109">Prerequisites</span></span>

-   <span data-ttu-id="88726-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="88726-110">C/C++</span></span>
-   <span data-ttu-id="88726-111">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="88726-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="88726-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="88726-112">Instructions</span></span>

### <a name="create-a-rebar-control"></a><span data-ttu-id="88726-113">Créer un contrôle rebar</span><span class="sxs-lookup"><span data-stu-id="88726-113">Create a Rebar Control</span></span>

<span data-ttu-id="88726-114">L’exemple suivant crée un contrôle rebar avec deux bandes : une qui contient une zone de liste modifiable et une autre qui contient une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="88726-114">The following example creates a rebar control with two bands—one that contains a combo box, and another one that contains a toolbar.</span></span> <span data-ttu-id="88726-115">(Voir l’illustration dans [à propos des contrôles Rebar](rebar-controls.md).) Ces contrôles sont créés séparément et sont passés à l’exemple de fonction en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="88726-115">(See the illustration in [About Rebar Controls](rebar-controls.md).) These controls are created separately, and are passed to the example function as parameters.</span></span>


```C++
#define NUMBUTTONS 3

HWND CreateRebar(HWND hwndOwner, HWND hwndToolbar, HWND hwndCombo)
{
    // Check parameters.
    if ((hwndToolbar == NULL) || (hwndCombo == NULL))
    {
        return NULL;
    }

    // Initialize common controls.
    INITCOMMONCONTROLSEX icex;
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC   = ICC_COOL_CLASSES | ICC_BAR_CLASSES;
    InitCommonControlsEx(&icex);

    // Create the rebar.
    HWND hwndRebar = CreateWindowEx(WS_EX_TOOLWINDOW,
        REBARCLASSNAME,
        NULL,
        WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS |
        WS_CLIPCHILDREN | RBS_VARHEIGHT |
        CCS_NODIVIDER | RBS_BANDBORDERS,
        0,0,0,0,
        hwndOwner,
        NULL,
        g_hInst, // global instance handle
        NULL);

    if(!hwndRebar)
    {
        return NULL;
    }

    // Initialize band info used by both bands.
    REBARBANDINFO rbBand = { sizeof(REBARBANDINFO) };
    rbBand.fMask  = 
          RBBIM_STYLE       // fStyle is valid.
        | RBBIM_TEXT        // lpText is valid.
        | RBBIM_CHILD       // hwndChild is valid.
        | RBBIM_CHILDSIZE   // child size members are valid.
        | RBBIM_SIZE;       // cx is valid
    rbBand.fStyle = RBBS_CHILDEDGE | RBBS_GRIPPERALWAYS;  

    // Get the height of the toolbar.
    DWORD dwBtnSize = (DWORD)SendMessage(hwndToolbar, TB_GETBUTTONSIZE, 0,0);

    // Set values unique to the band with the toolbar.
    rbBand.lpText = TEXT("");
    rbBand.hwndChild = hwndToolbar;
    rbBand.cyChild = LOWORD(dwBtnSize);
    rbBand.cxMinChild = NUMBUTTONS * HIWORD(dwBtnSize);
    rbBand.cyMinChild = LOWORD(dwBtnSize);
    // The default width is the width of the buttons.
    rbBand.cx = 0;

    // Add the band that has the toolbar.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);

    // Set values unique to the band with the combo box.
    RECT rc;
    GetWindowRect(hwndCombo, &rc);
    rbBand.lpText = TEXT("Font");
    rbBand.hwndChild = hwndCombo;
    rbBand.cxMinChild = 0;
    rbBand.cyMinChild = rc.bottom - rc.top;
    // The default width should be set to some value wider than the text. The combo 
    // box itself will expand to fill the band.
    rbBand.cx = 100;

    // Add the band that has the combo box.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);
    
    return (hwndRebar);
}
```



## <a name="related-topics"></a><span data-ttu-id="88726-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88726-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88726-117">Utilisation des contrôles Rebar</span><span class="sxs-lookup"><span data-stu-id="88726-117">Using Rebar Controls</span></span>](using-rebar-controls.md)
</dt> <dt>

[<span data-ttu-id="88726-118">À propos des contrôles Rebar</span><span class="sxs-lookup"><span data-stu-id="88726-118">About Rebar Controls</span></span>](rebar-controls.md)
</dt> <dt>

<span data-ttu-id="88726-119">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="88726-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 