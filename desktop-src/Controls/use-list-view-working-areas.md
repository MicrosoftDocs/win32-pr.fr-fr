---
title: Comment utiliser List-View zones de travail
description: Cette rubrique montre comment utiliser les zones de travail d’affichage de liste. Les zones de travail sont des zones virtuelles rectangulaires qui peuvent être utilisées pour organiser des éléments dans un contrôle List-affichage États.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029042"
---
# <a name="how-to-use-list-view-working-areas"></a><span data-ttu-id="a3220-104">Comment utiliser List-View zones de travail</span><span class="sxs-lookup"><span data-stu-id="a3220-104">How to Use List-View Working Areas</span></span>

<span data-ttu-id="a3220-105">Cette rubrique montre comment utiliser les zones de travail d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="a3220-105">This topic demonstrates how to work with list-view working areas.</span></span> <span data-ttu-id="a3220-106">Les zones de travail sont des zones virtuelles rectangulaires qui peuvent être utilisées pour organiser des éléments dans un contrôle List-affichage États.</span><span class="sxs-lookup"><span data-stu-id="a3220-106">Working areas are rectangular virtual areas that can be used to arrange items in a list-vew control.</span></span> <span data-ttu-id="a3220-107">Une zone de travail n’est pas une fenêtre et ne peut pas avoir de bordure visible.</span><span class="sxs-lookup"><span data-stu-id="a3220-107">A working area is not a window and cannot have a visible border.</span></span> <span data-ttu-id="a3220-108">Par défaut, le contrôle d’affichage de liste n’a pas de zones de travail.</span><span class="sxs-lookup"><span data-stu-id="a3220-108">By default, the list-view control has no working areas.</span></span> <span data-ttu-id="a3220-109">En créant une zone de travail, vous pouvez créer une bordure vide à gauche, en haut ou à droite des éléments ou provoquer l’affichage d’une barre de défilement horizontale quand il n’y en a pas normalement.</span><span class="sxs-lookup"><span data-stu-id="a3220-109">By creating a working area, you can create an empty border on the left, top, or right of the items or cause a horizontal scroll bar to be displayed when there normally would not be one.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a3220-110">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="a3220-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a3220-111">Technologies</span><span class="sxs-lookup"><span data-stu-id="a3220-111">Technologies</span></span>

-   [<span data-ttu-id="a3220-112">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="a3220-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a3220-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="a3220-113">Prerequisites</span></span>

-   <span data-ttu-id="a3220-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="a3220-114">C/C++</span></span>
-   <span data-ttu-id="a3220-115">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="a3220-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a3220-116">Instructions</span><span class="sxs-lookup"><span data-stu-id="a3220-116">Instructions</span></span>

### <a name="create-a-working-area"></a><span data-ttu-id="a3220-117">Créer une zone de travail</span><span class="sxs-lookup"><span data-stu-id="a3220-117">Create a Working Area</span></span>

<span data-ttu-id="a3220-118">L’exemple de code C++ suivant montre comment créer une zone de travail avec une bordure vide de 25 pixels sur ses côtés supérieur, gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="a3220-118">The following C++ code example demonstrates how to create a working area with a 25-pixel empty border on its top, left, and right sides.</span></span>


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a><span data-ttu-id="a3220-119">Créer plusieurs zones de travail</span><span class="sxs-lookup"><span data-stu-id="a3220-119">Create Multiple Working Areas</span></span>

<span data-ttu-id="a3220-120">L’exemple de code C++ suivant montre comment créer deux zones de travail dans un contrôle.</span><span class="sxs-lookup"><span data-stu-id="a3220-120">The following C++ code example demonstrates how to create two working areas in a control.</span></span> <span data-ttu-id="a3220-121">Chaque zone de travail utilise environ la moitié de la zone cliente et est entourée d’une bordure vide de 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="a3220-121">Each working area uses about half of the client area, and is surrounded by a 25-pixel empty border.</span></span>


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a><span data-ttu-id="a3220-122">Déterminer la zone de travail à laquelle un élément appartient</span><span class="sxs-lookup"><span data-stu-id="a3220-122">Determine the Working Area to Which an Item Belongs</span></span>

<span data-ttu-id="a3220-123">Pour déterminer l’espace de travail auquel appartient un élément, vous pouvez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3220-123">One way to determine which working area an item belongs is to do the following:</span></span>

-   <span data-ttu-id="a3220-124">Récupérez la liste des coordonnées de toutes les zones de travail dans le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="a3220-124">Retrieve the list of coordinates of all of the working areas in the list-view control.</span></span>
-   <span data-ttu-id="a3220-125">Récupérez les coordonnées de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a3220-125">Retrieve the coordinates of the item.</span></span>
-   <span data-ttu-id="a3220-126">Déterminez si les coordonnées de l’élément se trouvent dans les coordonnées de l’une des zones de travail.</span><span class="sxs-lookup"><span data-stu-id="a3220-126">Determine whether the item coordinates lie within the coordinates of one of the working areas.</span></span>

<span data-ttu-id="a3220-127">La fonction définie par l’application dans l’exemple de code C++ suivant retourne l’index de la zone de travail à laquelle l’élément appartient.</span><span class="sxs-lookup"><span data-stu-id="a3220-127">The application-defined function in the following C++ code example returns the index of the working area to which the item belongs.</span></span> <span data-ttu-id="a3220-128">Si la fonction échoue, elle retourne-1.</span><span class="sxs-lookup"><span data-stu-id="a3220-128">If the function fails, it returns –1.</span></span> <span data-ttu-id="a3220-129">Si la fonction s’exécute correctement, mais que l’élément ne se trouve pas dans les zones de travail, la fonction retourne 0, car tous les éléments qui ne se trouvent pas à l’intérieur d’une zone de travail deviennent automatiquement membres de la zone de travail zéro.</span><span class="sxs-lookup"><span data-stu-id="a3220-129">If the function succeeds, but the item is not inside any of the working areas, the function returns 0, because all items that are not inside a working area automatically become a member of working area zero.</span></span>


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a><span data-ttu-id="a3220-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3220-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3220-131">Référence du contrôle List-View</span><span class="sxs-lookup"><span data-stu-id="a3220-131">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a3220-132">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="a3220-132">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="a3220-133">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="a3220-133">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




