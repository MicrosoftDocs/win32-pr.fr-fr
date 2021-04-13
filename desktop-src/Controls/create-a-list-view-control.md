---
title: Comment créer un contrôle de List-View
description: Cette rubrique montre comment créer un contrôle List-View. Pour créer un contrôle List-View, utilisez la fonction CreateWindow ou CreateWindowEx et spécifiez la classe de fenêtre de la vue ListView de WC \_ .
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463943"
---
# <a name="how-to-create-a-list-view-control"></a><span data-ttu-id="bdf61-104">Comment créer un contrôle de List-View</span><span class="sxs-lookup"><span data-stu-id="bdf61-104">How to Create a List-View Control</span></span>

<span data-ttu-id="bdf61-105">Cette rubrique montre comment créer un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="bdf61-105">This topic demonstrates how to create a list-view control.</span></span> <span data-ttu-id="bdf61-106">Pour créer un contrôle List-View, utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et spécifiez la classe de fenêtre de la vue [**\_ ListView de WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="bdf61-106">To create a list-view control, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="bdf61-107">Un contrôle List-View peut également être créé dans le cadre d’un modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="bdf61-107">A list-view control can also be created as part of a dialog box template.</span></span> <span data-ttu-id="bdf61-108">Vous devez spécifier [**WC \_ ListView**](common-control-window-classes.md) comme nom de classe.</span><span class="sxs-lookup"><span data-stu-id="bdf61-108">You must specify [**WC\_LISTVIEW**](common-control-window-classes.md) as the class name.</span></span> <span data-ttu-id="bdf61-109">Pour utiliser un contrôle List-View dans le cadre d’un modèle de boîte de dialogue, vous devez appeler [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) ou [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) avant de créer une instance de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="bdf61-109">To use a list-view control as part of a dialog box template, you must call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) or [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) before you create an instance of the dialog box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bdf61-110">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="bdf61-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bdf61-111">Technologies</span><span class="sxs-lookup"><span data-stu-id="bdf61-111">Technologies</span></span>

-   [<span data-ttu-id="bdf61-112">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="bdf61-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bdf61-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bdf61-113">Prerequisites</span></span>

-   <span data-ttu-id="bdf61-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="bdf61-114">C/C++</span></span>
-   <span data-ttu-id="bdf61-115">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="bdf61-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bdf61-116">Instructions</span><span class="sxs-lookup"><span data-stu-id="bdf61-116">Instructions</span></span>


<span data-ttu-id="bdf61-117">Inscrivez d’abord la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) et en spécifiant le bit des [**\_ \_ classes ListView ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) dans la structure **InitCommonControlsEx** qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="bdf61-117">First register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the [**ICC\_LISTVIEW\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) bit in the accompanying **INITCOMMONCONTROLSEX** structure.</span></span> <span data-ttu-id="bdf61-118">Cela permet de s’assurer que la DLL de contrôles communs est chargée.</span><span class="sxs-lookup"><span data-stu-id="bdf61-118">This ensures that the common controls DLL is loaded.</span></span> <span data-ttu-id="bdf61-119">Ensuite, utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et spécifiez la classe de fenêtre du [**\_ ListView de WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="bdf61-119">Next, use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

> [!Note]  
> <span data-ttu-id="bdf61-120">Par défaut, un contrôle List-View utilise la police du titre de l’icône.</span><span class="sxs-lookup"><span data-stu-id="bdf61-120">By default, a list-view control uses the icon title font.</span></span> <span data-ttu-id="bdf61-121">Toutefois, vous pouvez utiliser un message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) pour spécifier la police à utiliser pour le texte.</span><span class="sxs-lookup"><span data-stu-id="bdf61-121">However, you can use a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to specify the font to be used for the text.</span></span> <span data-ttu-id="bdf61-122">Vous devez envoyer ce message avant d’insérer des éléments.</span><span class="sxs-lookup"><span data-stu-id="bdf61-122">You should send this message before inserting any items.</span></span> <span data-ttu-id="bdf61-123">Le contrôle utilise les dimensions de la police spécifiée par le message **WM \_ SetFont** pour déterminer l’espacement et la mise en page.</span><span class="sxs-lookup"><span data-stu-id="bdf61-123">The control uses the dimensions of the font that is specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span> <span data-ttu-id="bdf61-124">Vous pouvez également personnaliser la police pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="bdf61-124">You can also customize the font for each item.</span></span> <span data-ttu-id="bdf61-125">Pour plus d’informations, consultez [dessin personnalisé](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="bdf61-125">For more information, see [Custom Draw](custom-draw.md).</span></span>

 

<span data-ttu-id="bdf61-126">L’exemple de code C++ suivant crée un contrôle de liste en mode rapport.</span><span class="sxs-lookup"><span data-stu-id="bdf61-126">The following C++ code example creates a list-view control in report view.</span></span>


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




<span data-ttu-id="bdf61-127">En règle générale, les applications de vue de liste permettent à l’utilisateur de passer d’une vue à une autre.</span><span class="sxs-lookup"><span data-stu-id="bdf61-127">Typically, list-view applications enable the user to change from one view to another.</span></span>

<span data-ttu-id="bdf61-128">L’exemple de code C++ suivant modifie le style de fenêtre de l’affichage de liste, qui modifie à son tour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="bdf61-128">The following C++ code example changes the list-view's window style, which in turn changes the view.</span></span>


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a><span data-ttu-id="bdf61-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdf61-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdf61-130">Référence du contrôle List-View</span><span class="sxs-lookup"><span data-stu-id="bdf61-130">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="bdf61-131">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="bdf61-131">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="bdf61-132">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="bdf61-132">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 