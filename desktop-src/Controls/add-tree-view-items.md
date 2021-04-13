---
title: Comment ajouter des éléments de Tree-View
description: Vous ajoutez un élément à un contrôle Tree-View en envoyant le \_ message TVM INSERTITEM au contrôle.
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381573"
---
# <a name="how-to-add-tree-view-items"></a><span data-ttu-id="283a4-103">Comment ajouter des éléments de Tree-View</span><span class="sxs-lookup"><span data-stu-id="283a4-103">How to Add Tree-View Items</span></span>

<span data-ttu-id="283a4-104">Vous ajoutez un élément à un contrôle Tree-View en envoyant le message [**TVM \_ INSERTITEM**](tvm-insertitem.md) au contrôle.</span><span class="sxs-lookup"><span data-stu-id="283a4-104">You add an item to a tree-view control by sending the [**TVM\_INSERTITEM**](tvm-insertitem.md) message to the control.</span></span> <span data-ttu-id="283a4-105">Le message comprend l’adresse d’une structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , en spécifiant l’élément parent, l’élément après lequel le nouvel élément est inséré et une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui définit les attributs de l’élément.</span><span class="sxs-lookup"><span data-stu-id="283a4-105">The message includes the address of a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure, specifying the parent item, the item after which the new item is inserted, and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that defines the attributes of the item.</span></span> <span data-ttu-id="283a4-106">Les attributs incluent l’étiquette de l’élément, ses images sélectionnées et non sélectionnées, ainsi qu’une valeur 32 bits définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="283a4-106">The attributes include the item's label, its selected and nonselected images, and a 32-bit application-defined value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="283a4-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="283a4-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="283a4-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="283a4-108">Technologies</span></span>

-   [<span data-ttu-id="283a4-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="283a4-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="283a4-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="283a4-110">Prerequisites</span></span>

-   <span data-ttu-id="283a4-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="283a4-111">C/C++</span></span>
-   <span data-ttu-id="283a4-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="283a4-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="283a4-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="283a4-113">Instructions</span></span>

### <a name="add-items-to-the-tree-view"></a><span data-ttu-id="283a4-114">Ajouter des éléments au Tree-View</span><span class="sxs-lookup"><span data-stu-id="283a4-114">Add Items to the Tree-View</span></span>

<span data-ttu-id="283a4-115">L’exemple de cette section montre comment créer une table des matières basée sur les informations d’en-tête de document fournies dans un tableau défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="283a4-115">The example in this section demonstrates how to create a table of contents based on document heading information that is provided in an application-defined array.</span></span> <span data-ttu-id="283a4-116">Chaque élément de tableau se compose d’une chaîne de titre et d’un entier qui indique le niveau de titre.</span><span class="sxs-lookup"><span data-stu-id="283a4-116">Each array element consists of a heading string and an integer that indicates the heading level.</span></span> <span data-ttu-id="283a4-117">L’exemple prend en charge trois niveaux d’en-tête (1, 2 et 3).</span><span class="sxs-lookup"><span data-stu-id="283a4-117">The example supports three heading levels (1, 2, and 3).</span></span>

<span data-ttu-id="283a4-118">L’exemple comprend deux fonctions.</span><span class="sxs-lookup"><span data-stu-id="283a4-118">The example includes two functions.</span></span> <span data-ttu-id="283a4-119">La première fonction extrait chaque titre et le niveau de titre qui l’accompagne, puis les passe à la deuxième fonction.</span><span class="sxs-lookup"><span data-stu-id="283a4-119">The first function extracts each heading and accompanying heading level and then passes them to the second function.</span></span>

<span data-ttu-id="283a4-120">La deuxième fonction ajoute un élément à un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="283a4-120">The second function adds an item to a tree-view control.</span></span> <span data-ttu-id="283a4-121">Elle utilise le texte d’en-tête comme étiquette de l’élément et utilise le niveau de titre pour déterminer l’élément parent du nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="283a4-121">It uses the heading text as the item's label, and it uses the heading level to determine the parent item for the new item.</span></span> <span data-ttu-id="283a4-122">Un titre de niveau un est ajouté à la racine du contrôle Tree-View, un titre de niveau 2 est ajouté en tant qu’élément enfant de l’élément de niveau précédent, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="283a4-122">A level one heading is added to the root of the tree-view control, a level two heading is added as a child item of the previous level one item, and so on.</span></span> <span data-ttu-id="283a4-123">La fonction assigne une image à un élément selon qu’elle possède des éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="283a4-123">The function assigns an image to an item based on whether it has child items.</span></span> <span data-ttu-id="283a4-124">Si un élément a des éléments enfants, il obtient une image qui représente un dossier fermé.</span><span class="sxs-lookup"><span data-stu-id="283a4-124">If an item has child items, it gets an image that represents a closed folder.</span></span> <span data-ttu-id="283a4-125">Sinon, elle obtient une image qui représente un document.</span><span class="sxs-lookup"><span data-stu-id="283a4-125">Otherwise, it gets an image that represents a document.</span></span> <span data-ttu-id="283a4-126">Un élément utilise la même image pour les États sélectionnés et non sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="283a4-126">An item uses the same image for both the selected and nonselected states.</span></span>


```C++
// Adds items to a tree-view control. 
// Returns the handle to the newly added item. 
// hwndTV - handle to the tree-view control. 
// lpszItem - text of the item to add. 
// nLevel - level at which to add the item. 
//
// g_nClosed, and g_nDocument - global indexes of the images.

HTREEITEM AddItemToTree(HWND hwndTV, LPTSTR lpszItem, int nLevel)
{ 
    TVITEM tvi; 
    TVINSERTSTRUCT tvins; 
    static HTREEITEM hPrev = (HTREEITEM)TVI_FIRST; 
    static HTREEITEM hPrevRootItem = NULL; 
    static HTREEITEM hPrevLev2Item = NULL; 
    HTREEITEM hti; 

    tvi.mask = TVIF_TEXT | TVIF_IMAGE 
               | TVIF_SELECTEDIMAGE | TVIF_PARAM; 

    // Set the text of the item. 
    tvi.pszText = lpszItem; 
    tvi.cchTextMax = sizeof(tvi.pszText)/sizeof(tvi.pszText[0]); 

    // Assume the item is not a parent item, so give it a 
    // document image. 
    tvi.iImage = g_nDocument; 
    tvi.iSelectedImage = g_nDocument; 

    // Save the heading level in the item's application-defined 
    // data area. 
    tvi.lParam = (LPARAM)nLevel; 
    tvins.item = tvi; 
    tvins.hInsertAfter = hPrev; 

    // Set the parent item based on the specified level. 
    if (nLevel == 1) 
        tvins.hParent = TVI_ROOT; 
    else if (nLevel == 2) 
        tvins.hParent = hPrevRootItem; 
    else 
        tvins.hParent = hPrevLev2Item; 

    // Add the item to the tree-view control. 
    hPrev = (HTREEITEM)SendMessage(hwndTV, TVM_INSERTITEM, 
        0, (LPARAM)(LPTVINSERTSTRUCT)&tvins); 

    if (hPrev == NULL)
        return NULL;

    // Save the handle to the item. 
    if (nLevel == 1) 
        hPrevRootItem = hPrev; 
    else if (nLevel == 2) 
        hPrevLev2Item = hPrev; 

    // The new item is a child item. Give the parent item a 
    // closed folder bitmap to indicate it now has child items. 
    if (nLevel > 1)
    { 
        hti = TreeView_GetParent(hwndTV, hPrev); 
        tvi.mask = TVIF_IMAGE | TVIF_SELECTEDIMAGE; 
        tvi.hItem = hti; 
        tvi.iImage = g_nClosed; 
        tvi.iSelectedImage = g_nClosed; 
        TreeView_SetItem(hwndTV, &tvi); 
    } 

    return hPrev; 
} 

// Extracts heading text and heading levels from a global 
// array and passes them to a function that adds them as
// parent and child items to a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 

BOOL InitTreeViewItems(HWND hwndTV)
{ 
    HTREEITEM hti;

    // g_rgDocHeadings is an application-defined global array of 
    // the following structures: 
    //     typedef struct 
    //       { 
    //         TCHAR tchHeading[MAX_HEADING_LEN]; 
    //         int tchLevel; 
    //     } Heading; 
    for (int i = 0; i < ARRAYSIZE(g_rgDocHeadings); i++) 
    { 
        // Add the item to the tree-view control. 
        hti = AddItemToTree(hwndTV, g_rgDocHeadings[i].tchHeading, 
            g_rgDocHeadings[i].tchLevel); 

        if (hti == NULL)
            return FALSE;
    } 
           
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="283a4-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="283a4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="283a4-128">Utilisation de contrôles Tree-View</span><span class="sxs-lookup"><span data-stu-id="283a4-128">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="283a4-129">L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="283a4-129">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




