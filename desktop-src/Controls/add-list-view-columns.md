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
# <a name="how-to-add-list-view-columns"></a><span data-ttu-id="25bcc-103">Comment ajouter des colonnes List-View</span><span class="sxs-lookup"><span data-stu-id="25bcc-103">How to Add List-View Columns</span></span>

<span data-ttu-id="25bcc-104">Cette rubrique montre comment ajouter des colonnes à un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="25bcc-104">This topic demonstrates how to add columns to a list-view control.</span></span> <span data-ttu-id="25bcc-105">Les colonnes sont utilisées pour afficher les éléments et les sous-éléments lorsqu’un contrôle de liste est en mode rapport (détails).</span><span class="sxs-lookup"><span data-stu-id="25bcc-105">Columns are used to display the items and subitems when a list-view control is in report (details) view.</span></span> <span data-ttu-id="25bcc-106">Le texte des colonnes sélectionnées peut également être affiché en mode mosaïque.</span><span class="sxs-lookup"><span data-stu-id="25bcc-106">Text from selected columns can also be displayed in tile view.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="25bcc-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="25bcc-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="25bcc-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="25bcc-108">Technologies</span></span>

-   [<span data-ttu-id="25bcc-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="25bcc-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="25bcc-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="25bcc-110">Prerequisites</span></span>

-   <span data-ttu-id="25bcc-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="25bcc-111">C/C++</span></span>
-   <span data-ttu-id="25bcc-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="25bcc-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="25bcc-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="25bcc-113">Instructions</span></span>


<span data-ttu-id="25bcc-114">Pour ajouter une colonne à un contrôle List-View, envoyez le message [**LVM \_ InsertColumn**](lvm-insertcolumn.md) ou utilisez la macro de [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="25bcc-114">To add a column to a list-view control, send the [**LVM\_INSERTCOLUMN**](lvm-insertcolumn.md) message or use the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span> <span data-ttu-id="25bcc-115">Pour supprimer une colonne, utilisez le message [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .</span><span class="sxs-lookup"><span data-stu-id="25bcc-115">To delete a column, use the [**LVM\_DELETECOLUMN**](lvm-deletecolumn.md) message.</span></span>

<span data-ttu-id="25bcc-116">L’exemple de code C++ suivant appelle la macro [**\_ webinsertcolumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) pour ajouter des colonnes à un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="25bcc-116">The following C++ code example calls the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro to add columns to a list-view control.</span></span> <span data-ttu-id="25bcc-117">Les en-têtes de colonne sont définis dans le fichier d’en-tête de l’application en tant que ressources de type chaîne, numérotées de façon consécutive à partir des ID \_ FIRSTCOLUMN.</span><span class="sxs-lookup"><span data-stu-id="25bcc-117">The column headings are defined in the application's header file as string resources, which are numbered consecutively starting with IDS\_FIRSTCOLUMN.</span></span> <span data-ttu-id="25bcc-118">Le nombre de colonnes est défini dans le fichier d’en-tête en tant que **\_ colonnes C**.</span><span class="sxs-lookup"><span data-stu-id="25bcc-118">The number of columns is defined in the header file as **C\_COLUMNS**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="25bcc-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="25bcc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25bcc-120">Référence du contrôle List-View</span><span class="sxs-lookup"><span data-stu-id="25bcc-120">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="25bcc-121">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="25bcc-121">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="25bcc-122">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="25bcc-122">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




