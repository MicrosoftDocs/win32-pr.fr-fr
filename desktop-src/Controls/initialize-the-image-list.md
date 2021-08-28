---
title: Comment initialiser la liste d’images
description: Chaque élément d’un contrôle Tree-View peut avoir deux images qui lui sont associées.
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b8edcff0d07f46aa6eb8612ddbbfa37145c5ab26ab463a7d57e9e6543430e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019347"
---
# <a name="how-to-initialize-the-image-list"></a>Comment initialiser la liste d’images

Chaque élément d’un contrôle Tree-View peut avoir deux images qui lui sont associées. Un élément affiche une image lorsqu’elle est sélectionnée et l’autre quand elle ne l’est pas. Pour inclure des images avec des éléments d’arborescence, utilisez d’abord les fonctions des [listes d’images](image-lists.md) pour créer une liste d’images et y ajouter des images. Associez ensuite la liste d’images au contrôle Tree-View à l’aide du message de [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="initialize-the-image-list"></a>Initialiser la liste d’images

L’exemple suivant crée une liste d’images, ajoute trois bitmaps à la liste et associe la liste d’images à un contrôle d’arborescence.


```C++
// InitTreeViewImageLists - creates an image list, adds three bitmaps 
// to it, and associates the image list with a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 
//
// Global variables and constants: 
// g_hInst - the global instance handle.
// g_nOpen, g_nClosed, and g_nDocument - global indexes of the images. 
// CX_BITMAP and CY_BITMAP - width and height of an icon. 
// NUM_BITMAPS - number of bitmaps to add to the image list. 
// IDB_OPEN_FILE, IDB_CLOSED_FILE, IDB_DOCUMENT -
//     resource identifiers of the bitmaps.

BOOL InitTreeViewImageLists(HWND hwndTV) 
{ 
    HIMAGELIST himl;  // handle to image list 
    HBITMAP hbmp;     // handle to bitmap 

    // Create the image list. 
    if ((himl = ImageList_Create(CX_BITMAP, 
                                 CY_BITMAP,
                                 FALSE, 
                                 NUM_BITMAPS, 0)) == NULL) 
        return FALSE; 

    // Add the open file, closed file, and document bitmaps. 
    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_OPEN_FILE)); 
    g_nOpen = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CLOSED_FILE)); 
    g_nClosed = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_DOCUMENT)); 
    g_nDocument = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    // Fail if not all of the images were added. 
    if (ImageList_GetImageCount(himl) < 3) 
        return FALSE; 

    // Associate the image list with the tree-view control. 
    TreeView_SetImageList(hwndTV, himl, TVSIL_NORMAL); 

    return TRUE; 
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles Tree-View](using-treeview.md)
</dt> <dt>

[L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




