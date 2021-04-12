---
title: Comment ajouter des listes d’images List-View
description: Cette rubrique montre comment ajouter des listes d’images à un contrôle List-View.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f6f5b483ea80b412ab7638c9aceafcac4c5e6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316782"
---
# <a name="how-to-add-list-view-image-lists"></a><span data-ttu-id="90b7b-103">Comment ajouter des listes d’images List-View</span><span class="sxs-lookup"><span data-stu-id="90b7b-103">How to Add List-View Image Lists</span></span>

<span data-ttu-id="90b7b-104">Cette rubrique montre comment ajouter des listes d’images à un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="90b7b-104">This topic demonstrates how to add image lists to a list-view control.</span></span>

<span data-ttu-id="90b7b-105">Vous créez uniquement les listes d’images que le contrôle utilise.</span><span class="sxs-lookup"><span data-stu-id="90b7b-105">You create only the image lists that the control uses.</span></span> <span data-ttu-id="90b7b-106">Par exemple, si votre application n’autorise pas l’utilisateur à basculer vers la vue icône, vous n’avez pas besoin de créer et d’affecter une grande liste d’icônes.</span><span class="sxs-lookup"><span data-stu-id="90b7b-106">For example, if your application does not allow the user to switch to icon view, you do not need to create and assign a large icon list.</span></span> <span data-ttu-id="90b7b-107">Si vous créez des listes de grandes et petites images, elles doivent contenir les mêmes images dans le même ordre, car une seule valeur est utilisée pour identifier l’icône d’un élément d’affichage de liste dans les deux listes d’images.</span><span class="sxs-lookup"><span data-stu-id="90b7b-107">If you create both large and small image lists, they must contain the same images in the same order, because a single value is used to identify a list-view item's icon in both image lists.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="90b7b-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="90b7b-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="90b7b-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="90b7b-109">Technologies</span></span>

-   [<span data-ttu-id="90b7b-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="90b7b-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="90b7b-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="90b7b-111">Prerequisites</span></span>

-   <span data-ttu-id="90b7b-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="90b7b-112">C/C++</span></span>
-   <span data-ttu-id="90b7b-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="90b7b-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="90b7b-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="90b7b-114">Instructions</span></span>


<span data-ttu-id="90b7b-115">Pour afficher des images d’élément, vous devez assigner une liste d’images au contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="90b7b-115">To display item images, you must assign an image list to the list-view control.</span></span> <span data-ttu-id="90b7b-116">Pour ce faire, utilisez le message [**LVM \_ SETIMAGELIST**](lvm-setimagelist.md) ou le [**\_ SETIMAGELIST**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)de la macro ListView correspondant, en spécifiant si la liste d’images contient des icônes en taille réelle, des petites icônes ou des images d’État.</span><span class="sxs-lookup"><span data-stu-id="90b7b-116">To do this, use the [**LVM\_SETIMAGELIST**](lvm-setimagelist.md) message or the corresponding macro [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), specifying whether the image list contains full-sized icons, small icons, or state images.</span></span> <span data-ttu-id="90b7b-117">Pour récupérer le handle d’une liste d’images actuellement assignée à un contrôle List View, utilisez le message [**LVM \_ GETIMAGELIST**](lvm-getimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="90b7b-117">To retrieve the handle to an image list that is currently assigned to a list-view control, use the [**LVM\_GETIMAGELIST**](lvm-getimagelist.md) message.</span></span> <span data-ttu-id="90b7b-118">Vous pouvez utiliser la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) pour déterminer les dimensions appropriées pour les petites icônes et tailles.</span><span class="sxs-lookup"><span data-stu-id="90b7b-118">You can use the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to determine appropriate dimensions for the full-sized and small icons.</span></span>

<span data-ttu-id="90b7b-119">Dans l’exemple de code C++ suivant, la fonction définie par l’application crée d’abord des listes d’images, puis les assigne à un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="90b7b-119">In the following C++ code example, the application-defined function first creates image lists and then assigns them to a list-view control.</span></span>


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="90b7b-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90b7b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90b7b-121">Référence du contrôle List-View</span><span class="sxs-lookup"><span data-stu-id="90b7b-121">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="90b7b-122">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="90b7b-122">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="90b7b-123">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="90b7b-123">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 