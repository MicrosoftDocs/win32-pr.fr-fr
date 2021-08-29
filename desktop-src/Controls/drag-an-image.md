---
title: Comment faire glisser une image
description: Cette rubrique montre comment faire glisser une image à l’écran. Les fonctions Glisser-déplacer déplacent une image en douceur, en couleurs, sans aucun clignotement du curseur. Les images masquées et démasquées peuvent être glissées.
ms.assetid: 84AFA770-F495-4312-9631-3335BA8CC799
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdcbc5af1ad148dafc77a775e7ee901ce8c4d07221ab1e55fca251e51241fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062939"
---
# <a name="how-to-drag-an-image"></a>Comment faire glisser une image

Cette rubrique montre comment faire glisser une image à l’écran. Les fonctions Glisser-déplacer déplacent une image en douceur, en couleurs, sans aucun clignotement du curseur. Les images masquées et démasquées peuvent être glissées.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="step-1-begin-the-drag-operation"></a>Étape 1 : commencer l’opération glisser.

Utilisez la fonction [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) pour commencer une opération glisser.

La fonction définie par l’utilisateur dans l’exemple de code C++ suivant est destinée à être appelée en réponse à un message de bouton de la souris, tel que [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). La fonction détermine si l’utilisateur a cliqué dans le rectangle englobant de l’image. Si l’utilisateur clique sur l’utilisateur, la fonction capture l’entrée de la souris, efface l’image de la zone cliente et calcule la position de la zone réactive dans l’image. La fonction définit la zone réactive pour coïncider avec la zone réactive du curseur de la souris. Ensuite, la fonction commence l’opération glisser en appelant [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).


```C++
// StartDragging - begins dragging a bitmap. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// ptCur - coordinates of the cursor. 
// himl - handle to the image list. 
// 
// Global variables 
//     g_rcImage - bounding rectangle of the image to drag. 
//     g_nImage - index of the image. 
//     g_ptHotSpot - location of the image's hot spot. 
//     g_cxBorder and g_cyBorder - width and height of border. 
//     g_cyCaption and g_cyMenu - height of title bar and menu bar. 
extern RECT g_rcImage; 
extern int g_nImage; 
extern POINT g_ptHotSpot; 
 
BOOL StartDragging(HWND hwnd, POINT ptCur, HIMAGELIST himl) 
{ 
    // Return if the cursor is not in the bounding rectangle of 
    // the image. 
    if (!PtInRect(&g_rcImage, ptCur)) 
        return FALSE; 
 
    // Capture the mouse input. 
    SetCapture(hwnd); 
 
    // Erase the image from the client area. 
    InvalidateRect(hwnd, &g_rcImage, TRUE); 
    UpdateWindow(hwnd); 
 
    // Calculate the location of the hot spot, and save it. 
    g_ptHotSpot.x = ptCur.x - g_rcImage.left; 
    g_ptHotSpot.y = ptCur.y - g_rcImage.top; 
 
    // Begin the drag operation. 
    if (!ImageList_BeginDrag(himl, g_nImage, 
            g_ptHotSpot.x, g_ptHotSpot.y)) 
        return FALSE; 
 
    // Set the initial location of the image, and make it visible. 
    // Because the ImageList_DragEnter function expects coordinates to 
    // be relative to the upper-left corner of the given window, the 
    // width of the border, title bar, and menu bar need to be taken 
    // into account. 
    
    ImageList_DragEnter(hwnd, ptCur.x + g_cxBorder, 
        ptCur.y + g_cyBorder + g_cyCaption + g_cyMenu); 
 
    g_fDragging = TRUE; 
 
    return TRUE; 
} 
```



### <a name="step-2-move-the-image"></a>Étape 2 : déplacer l’image.

La [**fonction \_ DragMove ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) déplace l’image vers un nouvel emplacement.

La fonction définie par l’utilisateur dans l’exemple de code C++ suivant est destinée à être appelée en réponse au message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Il fait glisser l’image vers un nouvel emplacement.


```C++
// MoveTheImage - drags an image to the specified coordinates. 
// Returns TRUE if successful, or FALSE otherwise. 
// ptCur - new coordinates for the image. 
BOOL MoveTheImage(POINT ptCur) 
{ 
    if (!ImageList_DragMove(ptCur.x, ptCur.y)) 
        return FALSE; 
 
    return TRUE; 
} 

```



### <a name="step-3-end-the-drag-operation"></a>Étape 3 : terminer l’opération glisser.

La fonction définie par l’utilisateur dans l’exemple de code C++ suivant appelle la fonction [**ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) pour terminer l’opération glisser. Il appelle ensuite la fonction [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) pour déverrouiller la fenêtre et masquer l’image de glissement, ce qui permet la mise à jour de la fenêtre.


```C++
// StopDragging - ends a drag operation and draws the image 
// at its final location. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// himl - handle to the image list. 
// ptCur - coordinates of the cursor. 
// 
// Global variable 
//     g_ptHotSpot - location of the image's hot spot. 
 
extern POINT g_ptHotSpot; 
 
BOOL StopDragging(HWND hwnd, HIMAGELIST himl, POINT ptCur) 
{ 
    ImageList_EndDrag(); 
    ImageList_DragLeave(hwnd); 
 
    g_fDragging = FALSE; 
 
    DrawTheImage(hwnd, himl, ptCur.x - g_ptHotSpot.x, 
        ptCur.y - g_ptHotSpot.y); 
 
    ReleaseCapture(); 
    return TRUE; 
} 

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les listes d’images](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[À propos des listes d’images](image-lists.md)
</dt> <dt>

[Utilisation de listes d’images](using-image-lists.md)
</dt> </dl>

 

 