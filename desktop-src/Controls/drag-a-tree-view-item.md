---
title: Comment faire glisser un élément de Tree-View
description: Cette rubrique montre le code permettant de gérer le glissement et la suppression d’éléments d’arborescence.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463826"
---
# <a name="how-to-drag-a-tree-view-item"></a><span data-ttu-id="e04a4-103">Comment faire glisser un élément de Tree-View</span><span class="sxs-lookup"><span data-stu-id="e04a4-103">How to Drag a Tree-View Item</span></span>

<span data-ttu-id="e04a4-104">Cette rubrique montre le code permettant de gérer le glissement et la suppression d’éléments d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="e04a4-104">This topic demonstrates code for handling dragging and dropping of tree-view items.</span></span> <span data-ttu-id="e04a4-105">L’exemple de code se compose de trois fonctions.</span><span class="sxs-lookup"><span data-stu-id="e04a4-105">The sample code consists of three functions.</span></span> <span data-ttu-id="e04a4-106">La première fonction commence l’opération glisser, la deuxième fonction fait glisser l’image et la troisième fonction termine l’opération glisser.</span><span class="sxs-lookup"><span data-stu-id="e04a4-106">The first function begins the drag operation, the second function drags the image, and the third function ends the drag operation.</span></span>

> [!Note]  
> <span data-ttu-id="e04a4-107">Le fait de faire glisser un élément d’arborescence implique généralement le traitement du code de notification [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)), du message de [**\_ désouris WM**](/windows/desktop/inputdev/wm-mousemove) et du message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (ou [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)).</span><span class="sxs-lookup"><span data-stu-id="e04a4-107">Dragging a tree-view item typically involves processing the [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code, the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (or [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) message.</span></span> <span data-ttu-id="e04a4-108">Elle implique également l’utilisation des fonctions des [listes d’images](image-lists.md) pour dessiner l’élément au fur et à mesure de son déplacement.</span><span class="sxs-lookup"><span data-stu-id="e04a4-108">It also involves using the [Image Lists](image-lists.md) functions to draw the item as it is being dragged.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="e04a4-109">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="e04a4-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e04a4-110">Technologies</span><span class="sxs-lookup"><span data-stu-id="e04a4-110">Technologies</span></span>

-   [<span data-ttu-id="e04a4-111">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="e04a4-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e04a4-112">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e04a4-112">Prerequisites</span></span>

-   <span data-ttu-id="e04a4-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="e04a4-113">C/C++</span></span>
-   <span data-ttu-id="e04a4-114">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="e04a4-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e04a4-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="e04a4-115">Instructions</span></span>

### <a name="step-1-beginning-the-tree-view-drag-operation"></a><span data-ttu-id="e04a4-116">Étape 1 : démarrage de l’opération glisser-afficher l’arborescence</span><span class="sxs-lookup"><span data-stu-id="e04a4-116">Step 1: Beginning the tree-view drag operation</span></span>

<span data-ttu-id="e04a4-117">Un contrôle Tree-View envoie à la fenêtre parente un code de notification [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) chaque fois que l’utilisateur commence à faire glisser un élément.</span><span class="sxs-lookup"><span data-stu-id="e04a4-117">A tree-view control sends the parent window a [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code whenever the user starts to drag an item.</span></span> <span data-ttu-id="e04a4-118">La fenêtre parente reçoit la notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) dont le paramètre *lParam* est l’adresse d’une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="e04a4-118">The parent window receives the notification in the form of a [**WM\_NOTIFY**](wm-notify.md) message whose *lParam* parameter is the address of an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="e04a4-119">Les membres de cette structure incluent les coordonnées d’écran du pointeur de la souris et une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations sur l’élément à faire glisser.</span><span class="sxs-lookup"><span data-stu-id="e04a4-119">The members of this structure include the screen coordinates of the mouse pointer and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains information about the item to be dragged.</span></span>

<span data-ttu-id="e04a4-120">L’exemple suivant montre comment traiter le message [**WM \_ Notify**](wm-notify.md) pour obtenir [TVN \_ BEGINDRAG](tvn-begindrag.md).</span><span class="sxs-lookup"><span data-stu-id="e04a4-120">The following example shows how to process the [**WM\_NOTIFY**](wm-notify.md) message to obtain [TVN\_BEGINDRAG](tvn-begindrag.md).</span></span>


```C++
    case WM_NOTIFY: 
        switch (((LPNMHDR)lParam)->code) 
        {
            case TVN_BEGINDRAG:
                Main_OnBeginDrag(((LPNMHDR)lParam)->hwndFrom, (LPNMTREEVIEW)lParam);
                break;
        
            // Handle other cases here. 
        }
        break; 
```



<span data-ttu-id="e04a4-121">Le démarrage de l’opération glisser implique l’utilisation de la fonction [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) .</span><span class="sxs-lookup"><span data-stu-id="e04a4-121">Beginning the drag operation involves using the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function.</span></span> <span data-ttu-id="e04a4-122">Les paramètres de la fonction incluent le handle de la liste d’images qui contient l’image à utiliser pendant l’opération glisser et l’index de l’image.</span><span class="sxs-lookup"><span data-stu-id="e04a4-122">The function's parameters include the handle to the image list that contains the image to use during the drag operation and the index of the image.</span></span> <span data-ttu-id="e04a4-123">Vous pouvez fournir votre propre liste d’images et votre propre image, ou vous pouvez faire en sorte que le contrôle d’arborescence les crée pour vous à l’aide du message [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) .</span><span class="sxs-lookup"><span data-stu-id="e04a4-123">You can either provide your own image list and image, or you can have the tree-view control create them for you by using the [**TVM\_CREATEDRAGIMAGE**](tvm-createdragimage.md) message.</span></span>

<span data-ttu-id="e04a4-124">Étant donné que l’image de glissement remplace le pointeur de la souris pendant la durée de l’opération glisser, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) vous oblige à spécifier une zone réactive dans l’image.</span><span class="sxs-lookup"><span data-stu-id="e04a4-124">Because the drag image replaces the mouse pointer for the duration of the drag operation, [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requires you to specify a hot spot within the image.</span></span> <span data-ttu-id="e04a4-125">Les coordonnées de la zone réactive sont relatives au coin supérieur gauche de l’image.</span><span class="sxs-lookup"><span data-stu-id="e04a4-125">The coordinates of the hot spot are relative to the upper left corner of the image.</span></span> <span data-ttu-id="e04a4-126">**ImageList \_ BeginDrag** requiert également que vous spécifiiez l’emplacement initial de l’image de glissement.</span><span class="sxs-lookup"><span data-stu-id="e04a4-126">**ImageList\_BeginDrag** also requires you to specify the initial location of the drag image.</span></span> <span data-ttu-id="e04a4-127">Une application définit généralement l’emplacement initial afin que la zone réactive de l’image de glissement corresponde à celle du pointeur de la souris au moment où l’utilisateur a commencé l’opération glisser.</span><span class="sxs-lookup"><span data-stu-id="e04a4-127">An application typically sets the initial location so that the hot spot of the drag image corresponds to that of the mouse pointer at the time the user began the drag operation.</span></span>

<span data-ttu-id="e04a4-128">La fonction suivante montre comment commencer à faire glisser un élément d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="e04a4-128">The following function demonstrates how to begin dragging a tree-view item.</span></span> <span data-ttu-id="e04a4-129">Elle utilise l’image de glissement fournie par le contrôle Tree-View et obtient le rectangle englobant de l’élément pour déterminer le point approprié pour la zone réactive.</span><span class="sxs-lookup"><span data-stu-id="e04a4-129">It uses the drag image provided by the tree-view control and obtains the bounding rectangle of the item to determine the appropriate point for the hot spot.</span></span> <span data-ttu-id="e04a4-130">Les dimensions du rectangle englobant sont les mêmes que celles de l’image.</span><span class="sxs-lookup"><span data-stu-id="e04a4-130">The dimensions of the bounding rectangle are the same as those of the image.</span></span>

<span data-ttu-id="e04a4-131">La fonction capture l’entrée de la souris, ce qui entraîne l’envoi des messages de la souris à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="e04a4-131">The function captures mouse input, causing mouse messages to be sent to the parent window.</span></span> <span data-ttu-id="e04a4-132">La fenêtre parente a besoin des messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) suivants pour déterminer où faire glisser l’image et le message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) pour déterminer quand arrêter l’opération glisser.</span><span class="sxs-lookup"><span data-stu-id="e04a4-132">The parent window needs the subsequent [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to determine where to drag the image and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message to determine when to end the drag operation.</span></span>


```C++
// Begin dragging an item in a tree-view control. 
// hwndTV - handle to the image list. 
// lpnmtv - address of information about the item being dragged.
//
// g_fDragging -- global BOOL that specifies whether dragging is underway.

void Main_OnBeginDrag(HWND hwndTV, LPNMTREEVIEW lpnmtv)
{ 
    HIMAGELIST himl;    // handle to image list 
    RECT rcItem;        // bounding rectangle of item 

    // Tell the tree-view control to create an image to use 
    // for dragging. 
    himl = TreeView_CreateDragImage(hwndTV, lpnmtv->itemNew.hItem); 

    // Get the bounding rectangle of the item being dragged. 
    TreeView_GetItemRect(hwndTV, lpnmtv->itemNew.hItem, &rcItem, TRUE); 

    // Start the drag operation. 
    ImageList_BeginDrag(himl, 0, 0, 0);
    ImageList_DragEnter(hwndTV, lpnmtv->ptDrag.x, lpnmtv->ptDrag.x); 

    // Hide the mouse pointer, and direct mouse input to the 
    // parent window. 
    ShowCursor(FALSE); 
    SetCapture(GetParent(hwndTV)); 
    g_fDragging = TRUE; 

    return; 

} 
```



### <a name="step-2-dragging-the-tree-view-item"></a><span data-ttu-id="e04a4-133">Étape 2 : déplacement de l’élément d’affichage de l’arborescence</span><span class="sxs-lookup"><span data-stu-id="e04a4-133">Step 2: Dragging the tree-view item</span></span>

<span data-ttu-id="e04a4-134">Vous faites glisser un élément d’arborescence en appelant la fonction [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) quand la fenêtre parente reçoit un message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e04a4-134">You drag a tree-view item by calling the [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function when the parent window receives a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, as the following example shows.</span></span> <span data-ttu-id="e04a4-135">L’exemple montre également comment effectuer un test de positionnement pendant l’opération glisser pour déterminer s’il faut mettre en surbrillance d’autres éléments de l’arborescence en tant que cibles d’une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="e04a4-135">The example also demonstrates how to perform hit testing during the drag operation to determine whether to highlight other items in the tree view as targets of a drag-and-drop operation.</span></span>


```C++
// Drag an item in a tree-view control, 
// highlighting the item that is the target. 
// hwndParent - handle to the parent window. 
// hwndTV - handle to the tree-view control.
// xCur and yCur - coordinates of the mouse pointer,
//     relative to the parent window. 
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnMouseMove(HWND hwndParent, HWND hwndTV, LONG xCur, LONG yCur) 
{ 
    HTREEITEM htiTarget;  // Handle to target item. 
    TVHITTESTINFO tvht;   // Hit test information. 

    if (g_fDragging) 
    { 
       // Drag the item to the current position of the mouse pointer. 
       // First convert the dialog coordinates to control coordinates. 
       POINT point;
       point.x = xCur;
       point.y = yCur;
       ClientToScreen(hwndParent, &point);
       ScreenToClient(hwndTV, &point);
       ImageList_DragMove(point.x, point.y);
       // Turn off the dragged image so the background can be refreshed.
       ImageList_DragShowNolock(FALSE); 
                
        // Find out if the pointer is on the item. If it is, 
        // highlight the item as a drop target. 
        tvht.pt.x = point.x; 
        tvht.pt.y = point.y; 
        if ((htiTarget = TreeView_HitTest(hwndTV, &tvht)) != NULL) 
        { 
            TreeView_SelectDropTarget(hwndTV, htiTarget); 
        } 
        ImageList_DragShowNolock(TRUE);
    } 
    return; 
}
```



### <a name="step-3-ending-the-tree-view-drag-operation"></a><span data-ttu-id="e04a4-136">Étape 3 : fin de l’opération de glissement d’arborescence</span><span class="sxs-lookup"><span data-stu-id="e04a4-136">Step 3: Ending the tree-view drag operation</span></span>

<span data-ttu-id="e04a4-137">L’exemple suivant montre comment mettre fin à une opération glisser.</span><span class="sxs-lookup"><span data-stu-id="e04a4-137">The following example shows how to end a drag operation.</span></span> <span data-ttu-id="e04a4-138">La [**fonction \_ EndDrag ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) est appelée lorsque la fenêtre parente reçoit un message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="e04a4-138">The [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function is called when the parent window receives a [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message.</span></span> <span data-ttu-id="e04a4-139">Le handle du contrôle Tree-View est passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="e04a4-139">The handle of the tree-view control is passed to the function.</span></span>


```C++
// Stops dragging a tree-view item, releases the 
// mouse capture, and shows the mouse pointer.
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnLButtonUp(HWND hwndTV) 
{ 
    if (g_fDragging) 
    { 
        // Get destination item.
        HTREEITEM htiDest = TreeView_GetDropHilight(hwndTV);
        if (htiDest != NULL)
        {
            // To do: handle the actual moving of the dragged node.
        }
        ImageList_EndDrag(); 
        TreeView_SelectDropTarget(hwndTV, NULL);
        ReleaseCapture(); 
        ShowCursor(TRUE); 
        g_fDragging = FALSE; 
    } 
    return; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="e04a4-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e04a4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e04a4-141">Utilisation de contrôles Tree-View</span><span class="sxs-lookup"><span data-stu-id="e04a4-141">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="e04a4-142">L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="e04a4-142">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 