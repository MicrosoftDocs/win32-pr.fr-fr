---
title: Comment utiliser List-View zones de travail
description: Cette rubrique montre comment utiliser les zones de travail d’affichage de liste. Les zones de travail sont des zones virtuelles rectangulaires qui peuvent être utilisées pour organiser des éléments dans un contrôle List-affichage États.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6898603df0ce86d6b5da5e6e178ceaa85a9e3842925ca77fa90bbda990ba3085
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132069"
---
# <a name="how-to-use-list-view-working-areas"></a>Comment utiliser List-View zones de travail

Cette rubrique montre comment utiliser les zones de travail d’affichage de liste. Les zones de travail sont des zones virtuelles rectangulaires qui peuvent être utilisées pour organiser des éléments dans un contrôle List-affichage États. Une zone de travail n’est pas une fenêtre et ne peut pas avoir de bordure visible. Par défaut, le contrôle d’affichage de liste n’a pas de zones de travail. En créant une zone de travail, vous pouvez créer une bordure vide à gauche, en haut ou à droite des éléments ou provoquer l’affichage d’une barre de défilement horizontale quand il n’y en a pas normalement.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-working-area"></a>Créer une zone de travail

L’exemple de code C++ suivant montre comment créer une zone de travail avec une bordure vide de 25 pixels sur ses côtés supérieur, gauche et droit.


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



### <a name="create-multiple-working-areas"></a>Créer plusieurs zones de travail

L’exemple de code C++ suivant montre comment créer deux zones de travail dans un contrôle. Chaque zone de travail utilise environ la moitié de la zone cliente et est entourée d’une bordure vide de 25 pixels.


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



### <a name="determine-the-working-area-to-which-an-item-belongs"></a>Déterminer la zone de travail à laquelle un élément appartient

Pour déterminer l’espace de travail auquel appartient un élément, vous pouvez effectuer les opérations suivantes :

-   Récupérez la liste des coordonnées de toutes les zones de travail dans le contrôle List-View.
-   Récupérez les coordonnées de l’élément.
-   Déterminez si les coordonnées de l’élément se trouvent dans les coordonnées de l’une des zones de travail.

La fonction définie par l’application dans l’exemple de code C++ suivant retourne l’index de la zone de travail à laquelle l’élément appartient. Si la fonction échoue, elle retourne-1. Si la fonction s’exécute correctement, mais que l’élément ne se trouve pas dans les zones de travail, la fonction retourne 0, car tous les éléments qui ne se trouvent pas à l’intérieur d’une zone de travail deviennent automatiquement membres de la zone de travail zéro.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[À propos des contrôles List-View](list-view-controls-overview.md)
</dt> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

 




