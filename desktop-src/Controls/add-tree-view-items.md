---
title: Comment ajouter des éléments de Tree-View
description: Vous ajoutez un élément à un contrôle Tree-View en envoyant le \_ message TVM INSERTITEM au contrôle.
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010173"
---
# <a name="how-to-add-tree-view-items"></a>Comment ajouter des éléments de Tree-View

Vous ajoutez un élément à un contrôle Tree-View en envoyant le message [**TVM \_ INSERTITEM**](tvm-insertitem.md) au contrôle. Le message comprend l’adresse d’une structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , en spécifiant l’élément parent, l’élément après lequel le nouvel élément est inséré et une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui définit les attributs de l’élément. Les attributs incluent l’étiquette de l’élément, ses images sélectionnées et non sélectionnées, ainsi qu’une valeur 32 bits définie par l’application.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="add-items-to-the-tree-view"></a>Ajouter des éléments au Tree-View

L’exemple de cette section montre comment créer une table des matières basée sur les informations d’en-tête de document fournies dans un tableau défini par l’application. Chaque élément de tableau se compose d’une chaîne de titre et d’un entier qui indique le niveau de titre. L’exemple prend en charge trois niveaux d’en-tête (1, 2 et 3).

L’exemple comprend deux fonctions. La première fonction extrait chaque titre et le niveau de titre qui l’accompagne, puis les passe à la deuxième fonction.

La deuxième fonction ajoute un élément à un contrôle Tree-View. Elle utilise le texte d’en-tête comme étiquette de l’élément et utilise le niveau de titre pour déterminer l’élément parent du nouvel élément. Un titre de niveau un est ajouté à la racine du contrôle Tree-View, un titre de niveau 2 est ajouté en tant qu’élément enfant de l’élément de niveau précédent, et ainsi de suite. La fonction assigne une image à un élément selon qu’elle possède des éléments enfants. Si un élément a des éléments enfants, il obtient une image qui représente un dossier fermé. Sinon, elle obtient une image qui représente un document. Un élément utilise la même image pour les États sélectionnés et non sélectionnés.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles Tree-View](using-treeview.md)
</dt> <dt>

[L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




