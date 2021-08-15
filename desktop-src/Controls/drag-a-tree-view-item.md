---
title: Comment faire glisser un élément de Tree-View
description: Cette rubrique montre le code permettant de gérer le glissement et la suppression d’éléments d’arborescence.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ee7cfc9d4fa7a6e73abd042df583ae9175de8583b050ff9621b7d2789e0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413113"
---
# <a name="how-to-drag-a-tree-view-item"></a>Comment faire glisser un élément de Tree-View

Cette rubrique montre le code permettant de gérer le glissement et la suppression d’éléments d’arborescence. L’exemple de code se compose de trois fonctions. La première fonction commence l’opération glisser, la deuxième fonction fait glisser l’image et la troisième fonction termine l’opération glisser.

> [!Note]  
> Le fait de faire glisser un élément d’arborescence implique généralement le traitement du code de notification [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)), du message de [**\_ désouris WM**](/windows/desktop/inputdev/wm-mousemove) et du message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (ou [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)). Elle implique également l’utilisation des fonctions des [listes d’images](image-lists.md) pour dessiner l’élément au fur et à mesure de son déplacement.

 

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Étape 1 : démarrage de l’opération glisser-afficher l’arborescence

Un contrôle Tree-View envoie à la fenêtre parente un code de notification [TVN \_ BEGINDRAG](tvn-begindrag.md) (ou [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) chaque fois que l’utilisateur commence à faire glisser un élément. La fenêtre parente reçoit la notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) dont le paramètre *lParam* est l’adresse d’une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Les membres de cette structure incluent les coordonnées d’écran du pointeur de la souris et une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations sur l’élément à faire glisser.

L’exemple suivant montre comment traiter le message [**WM \_ Notify**](wm-notify.md) pour obtenir [TVN \_ BEGINDRAG](tvn-begindrag.md).


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



Le démarrage de l’opération glisser implique l’utilisation de la fonction [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) . Les paramètres de la fonction incluent le handle de la liste d’images qui contient l’image à utiliser pendant l’opération glisser et l’index de l’image. Vous pouvez fournir votre propre liste d’images et votre propre image, ou vous pouvez faire en sorte que le contrôle d’arborescence les crée pour vous à l’aide du message [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) .

Étant donné que l’image de glissement remplace le pointeur de la souris pendant la durée de l’opération glisser, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) vous oblige à spécifier une zone réactive dans l’image. Les coordonnées de la zone réactive sont relatives au coin supérieur gauche de l’image. **ImageList \_ BeginDrag** requiert également que vous spécifiiez l’emplacement initial de l’image de glissement. Une application définit généralement l’emplacement initial afin que la zone réactive de l’image de glissement corresponde à celle du pointeur de la souris au moment où l’utilisateur a commencé l’opération glisser.

La fonction suivante montre comment commencer à faire glisser un élément d’arborescence. Elle utilise l’image de glissement fournie par le contrôle Tree-View et obtient le rectangle englobant de l’élément pour déterminer le point approprié pour la zone réactive. Les dimensions du rectangle englobant sont les mêmes que celles de l’image.

La fonction capture l’entrée de la souris, ce qui entraîne l’envoi des messages de la souris à la fenêtre parente. La fenêtre parente a besoin des messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) suivants pour déterminer où faire glisser l’image et le message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) pour déterminer quand arrêter l’opération glisser.


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



### <a name="step-2-dragging-the-tree-view-item"></a>Étape 2 : déplacement de l’élément d’affichage de l’arborescence

Vous faites glisser un élément d’arborescence en appelant la fonction [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) quand la fenêtre parente reçoit un message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , comme le montre l’exemple suivant. L’exemple montre également comment effectuer un test de positionnement pendant l’opération glisser pour déterminer s’il faut mettre en surbrillance d’autres éléments de l’arborescence en tant que cibles d’une opération de glisser-déplacer.


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Étape 3 : fin de l’opération de glissement d’arborescence

L’exemple suivant montre comment mettre fin à une opération glisser. La [**fonction \_ EndDrag ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) est appelée lorsque la fenêtre parente reçoit un message [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) . Le handle du contrôle Tree-View est passé à la fonction.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles Tree-View](using-treeview.md)
</dt> <dt>

[L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 