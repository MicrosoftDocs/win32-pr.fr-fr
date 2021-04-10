---
title: Comment créer un contrôle de Tree-View
description: Pour créer un contrôle Tree-View, utilisez la fonction CreateWindowEx, en spécifiant la valeur de l’arborescence WC \_ pour la classe Window.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102432"
---
# <a name="how-to-create-a-tree-view-control"></a><span data-ttu-id="c9bff-103">Comment créer un contrôle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="c9bff-103">How to Create a Tree-View Control</span></span>

<span data-ttu-id="c9bff-104">Pour créer un contrôle Tree-View, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la valeur de l’arborescence [**WC \_**](common-control-window-classes.md) pour la classe Window.</span><span class="sxs-lookup"><span data-stu-id="c9bff-104">To create a tree-view control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_TREEVIEW**](common-control-window-classes.md) value for the window class.</span></span> <span data-ttu-id="c9bff-105">La classe de fenêtre d’arborescence est inscrite dans l’espace d’adressage de l’application lors du chargement de la DLL de contrôle commune.</span><span class="sxs-lookup"><span data-stu-id="c9bff-105">The tree-view window class is registered in the application's address space when the common control DLL is loaded.</span></span> <span data-ttu-id="c9bff-106">Pour vous assurer que la DLL est chargée, utilisez la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .</span><span class="sxs-lookup"><span data-stu-id="c9bff-106">To ensure that the DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c9bff-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="c9bff-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c9bff-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="c9bff-108">Technologies</span></span>

-   [<span data-ttu-id="c9bff-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="c9bff-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c9bff-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c9bff-110">Prerequisites</span></span>

-   <span data-ttu-id="c9bff-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c9bff-111">C/C++</span></span>
-   <span data-ttu-id="c9bff-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="c9bff-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c9bff-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="c9bff-113">Instructions</span></span>

### <a name="create-an-instance-of-a-tree-view-control"></a><span data-ttu-id="c9bff-114">Créer une instance d’un contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="c9bff-114">Create an Instance of a Tree-View Control</span></span>

<span data-ttu-id="c9bff-115">L’exemple suivant crée un contrôle d’arborescence dimensionné pour s’ajuster à la zone cliente de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="c9bff-115">The following example creates a tree-view control that is sized to fit the client area of the parent window.</span></span> <span data-ttu-id="c9bff-116">Il utilise également des fonctions définies par l’application pour associer une liste d’images au contrôle et ajouter des éléments au contrôle.</span><span class="sxs-lookup"><span data-stu-id="c9bff-116">It also uses application-defined functions to associate an image list with the control and add items to the control.</span></span>


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a><span data-ttu-id="c9bff-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c9bff-117">Remarks</span></span>

<span data-ttu-id="c9bff-118">Lorsque vous créez un contrôle Tree-View, vous pouvez également lui envoyer un message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) pour définir la police à utiliser pour le texte.</span><span class="sxs-lookup"><span data-stu-id="c9bff-118">When you create a tree-view control, you can also send it a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to set the font to be used for the text.</span></span> <span data-ttu-id="c9bff-119">Vous devez envoyer ce message avant d’insérer des éléments.</span><span class="sxs-lookup"><span data-stu-id="c9bff-119">You should send this message before inserting any items.</span></span> <span data-ttu-id="c9bff-120">Par défaut, une arborescence utilise la police du titre de l’icône.</span><span class="sxs-lookup"><span data-stu-id="c9bff-120">By default, a tree view uses the icon title font.</span></span> <span data-ttu-id="c9bff-121">Bien que vous puissiez personnaliser la police par élément à l’aide d’un [dessin personnalisé](custom-draw.md), le contrôle d’arborescence utilise les dimensions de la police spécifiées par le message **WM \_ SetFont** pour déterminer l’espacement et la mise en page.</span><span class="sxs-lookup"><span data-stu-id="c9bff-121">Although you can customize the font per-item by using [Custom Draw](custom-draw.md), the tree-view control uses the dimensions of the font specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9bff-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9bff-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9bff-123">Utilisation de contrôles Tree-View</span><span class="sxs-lookup"><span data-stu-id="c9bff-123">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="c9bff-124">L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="c9bff-124">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 