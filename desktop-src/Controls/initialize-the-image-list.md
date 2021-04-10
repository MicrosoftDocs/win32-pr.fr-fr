---
title: Comment initialiser la liste d’images
description: Chaque élément d’un contrôle Tree-View peut avoir deux images qui lui sont associées.
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011d789da4eec39febae9d93436e23c23fa59507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101285"
---
# <a name="how-to-initialize-the-image-list"></a><span data-ttu-id="cef98-103">Comment initialiser la liste d’images</span><span class="sxs-lookup"><span data-stu-id="cef98-103">How to Initialize the Image List</span></span>

<span data-ttu-id="cef98-104">Chaque élément d’un contrôle Tree-View peut avoir deux images qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="cef98-104">Every item in a tree-view control can have two images associated with it.</span></span> <span data-ttu-id="cef98-105">Un élément affiche une image lorsqu’elle est sélectionnée et l’autre quand elle ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="cef98-105">An item displays one image when it is selected and the other when it is not.</span></span> <span data-ttu-id="cef98-106">Pour inclure des images avec des éléments d’arborescence, utilisez d’abord les fonctions des [listes d’images](image-lists.md) pour créer une liste d’images et y ajouter des images.</span><span class="sxs-lookup"><span data-stu-id="cef98-106">To include images with tree-view items, first use the [Image Lists](image-lists.md) functions to create an image list and add images to it.</span></span> <span data-ttu-id="cef98-107">Associez ensuite la liste d’images au contrôle Tree-View à l’aide du message de [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="cef98-107">Then associate the image list with the tree-view control by using the [**TVM\_SETIMAGELIST**](tvm-setimagelist.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cef98-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="cef98-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cef98-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="cef98-109">Technologies</span></span>

-   [<span data-ttu-id="cef98-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="cef98-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cef98-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="cef98-111">Prerequisites</span></span>

-   <span data-ttu-id="cef98-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="cef98-112">C/C++</span></span>
-   <span data-ttu-id="cef98-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="cef98-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cef98-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="cef98-114">Instructions</span></span>

### <a name="initialize-the-image-list"></a><span data-ttu-id="cef98-115">Initialiser la liste d’images</span><span class="sxs-lookup"><span data-stu-id="cef98-115">Initialize the Image List</span></span>

<span data-ttu-id="cef98-116">L’exemple suivant crée une liste d’images, ajoute trois bitmaps à la liste et associe la liste d’images à un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="cef98-116">The following example creates an image list, adds three bitmaps to the list, and associates the image list with a tree-view control.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cef98-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cef98-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cef98-118">Utilisation de contrôles Tree-View</span><span class="sxs-lookup"><span data-stu-id="cef98-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="cef98-119">L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="cef98-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




