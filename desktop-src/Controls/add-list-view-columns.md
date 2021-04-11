---
title: Comment ajouter des colonnes List-View
description: Cette rubrique montre comment ajouter des colonnes à un contrôle List-View.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032109"
---
# <a name="how-to-add-list-view-columns"></a>Comment ajouter des colonnes List-View

Cette rubrique montre comment ajouter des colonnes à un contrôle List-View. Les colonnes sont utilisées pour afficher les éléments et les sous-éléments lorsqu’un contrôle de liste est en mode rapport (détails). Le texte des colonnes sélectionnées peut également être affiché en mode mosaïque.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Pour ajouter une colonne à un contrôle List-View, envoyez le message [**LVM \_ InsertColumn**](lvm-insertcolumn.md) ou utilisez la macro de [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) . Pour supprimer une colonne, utilisez le message [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .

L’exemple de code C++ suivant appelle la macro [**\_ webinsertcolumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) pour ajouter des colonnes à un contrôle List-View. Les en-têtes de colonne sont définis dans le fichier d’en-tête de l’application en tant que ressources de type chaîne, numérotées de façon consécutive à partir des ID \_ FIRSTCOLUMN. Le nombre de colonnes est défini dans le fichier d’en-tête en tant que **\_ colonnes C**.


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[À propos des contrôles List-View](list-view-controls-overview.md)
</dt> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

 




