---
title: Utilisation des affichages en mosaïque
description: Cette rubrique montre comment définir l’affichage en mosaïque pour un contrôle List View.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941480"
---
# <a name="how-to-use-tile-views"></a><span data-ttu-id="e0d58-103">Utilisation des affichages en mosaïque</span><span class="sxs-lookup"><span data-stu-id="e0d58-103">How to Use Tile Views</span></span>

<span data-ttu-id="e0d58-104">Cette rubrique montre comment définir l’affichage en mosaïque pour un contrôle List View.</span><span class="sxs-lookup"><span data-stu-id="e0d58-104">This topic demonstrates how to set the tile view for a list-view control.</span></span> <span data-ttu-id="e0d58-105">En mode mosaïque, chaque élément est représenté par une grande icône avec une ou plusieurs lignes de texte d’accompagnement.</span><span class="sxs-lookup"><span data-stu-id="e0d58-105">In tile view, each item is represented by a large icon with one or more lines of accompanying text.</span></span> <span data-ttu-id="e0d58-106">Pour obtenir une illustration, consultez [à propos des contrôles de List-View](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e0d58-106">For an illustration, see [About List-View Controls](list-view-controls-overview.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e0d58-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="e0d58-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e0d58-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="e0d58-108">Technologies</span></span>

-   [<span data-ttu-id="e0d58-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="e0d58-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e0d58-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e0d58-110">Prerequisites</span></span>

-   <span data-ttu-id="e0d58-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="e0d58-111">C/C++</span></span>
-   <span data-ttu-id="e0d58-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="e0d58-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e0d58-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="e0d58-113">Instructions</span></span>


<span data-ttu-id="e0d58-114">Définissez les paramètres d’affichage généraux pour l’affichage en mosaïque à l’aide de la macro [**ListView \_ SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) .</span><span class="sxs-lookup"><span data-stu-id="e0d58-114">Set the general display parameters for tile view by using the [**ListView\_SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) macro.</span></span> <span data-ttu-id="e0d58-115">Utilisez la structure [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) qui est passée à cette macro pour spécifier la position du texte par rapport à l’icône, la taille de chaque vignette (y compris le texte d’accompagnement) et le nombre maximal de lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="e0d58-115">Use the [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) structure that is passed to this macro to specify the position of the text in relation to the icon, the size of each tile (including accompanying text), and the maximum number of lines of text.</span></span>

<span data-ttu-id="e0d58-116">Si vous ne souhaitez pas que les vignettes soient automatiquement dimensionnées, vous devez définir **LVTVIF \_ FIXEDSIZE** dans le membre **dwFlags** et **LVTVIM \_ Tile** dans le membre **dwMask** de [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), ainsi que fournir les dimensions dans le membre **sizeTile** .</span><span class="sxs-lookup"><span data-stu-id="e0d58-116">If you do not want tiles to be automatically sized, you must set **LVTVIF\_FIXEDSIZE** in the **dwFlags** member and **LVTVIM\_TILESIZE** in the **dwMask** member of [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), as well as providing the dimensions in the **sizeTile** member.</span></span>

<span data-ttu-id="e0d58-117">L’exemple de code C++ suivant définit les informations d’affichage en mosaïque pour un contrôle d’affichage de liste afin qu’un maximum de deux sous-éléments s’affiche pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="e0d58-117">The following C++ code example sets the tile view info for a list-view control so that a maximum of two subitems are displayed for each item.</span></span> <span data-ttu-id="e0d58-118">Il définit également la taille de chaque vignette.</span><span class="sxs-lookup"><span data-stu-id="e0d58-118">It also sets the size of each tile.</span></span>


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



<span data-ttu-id="e0d58-119">Pour chaque élément de la liste, vous pouvez définir d’autres paramètres lorsque l’élément est inséré dans la liste, ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e0d58-119">For each item in the list, you can set further parameters when the item is inserted in the list, or later.</span></span> <span data-ttu-id="e0d58-120">La structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) utilisée avec [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contient des membres qui spécifient les colonnes de données à afficher sous l’élément, ainsi que leur alignement.</span><span class="sxs-lookup"><span data-stu-id="e0d58-120">The [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that is used with [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contains members that specify which columns of data to display below the item, and their alignment.</span></span> <span data-ttu-id="e0d58-121">Ces mêmes paramètres d’affichage se trouvent également dans la structure [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) utilisée avec [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span><span class="sxs-lookup"><span data-stu-id="e0d58-121">These same display parameters are also found in the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure used with [**ListView\_SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span></span>

> [!Note]  
> <span data-ttu-id="e0d58-122">Ici, « Columns » fait référence à l’affichage des colonnes dans l’affichage en mosaïque mais plutôt aux sous-éléments qui sont affichés dans les colonnes en mode Détails.</span><span class="sxs-lookup"><span data-stu-id="e0d58-122">"Columns" here refers not to display columns in tile view but rather to subitems, which are displayed in columns in details view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0d58-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0d58-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0d58-124">Référence du contrôle List-View</span><span class="sxs-lookup"><span data-stu-id="e0d58-124">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e0d58-125">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="e0d58-125">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="e0d58-126">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="e0d58-126">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




