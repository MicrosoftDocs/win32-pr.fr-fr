---
title: Comment ajouter un élément à un contrôle header
description: Cette rubrique montre comment ajouter un élément à un contrôle header.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4face974c1b04021afdc9e26976c023e1287439eb3d6d63c7ea7f9f34c5b27f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922051"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Comment ajouter un élément à un contrôle header

Cette rubrique montre comment ajouter un élément à un contrôle header. Un contrôle header contient généralement plusieurs éléments d’en-tête qui définissent les colonnes du contrôle. Vous pouvez ajouter un élément à un contrôle header en envoyant le message [**HDM \_ INSERTITEM**](hdm-insertitem.md) au contrôle.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Utilisez le message [**HDM \_ INSERTITEM**](hdm-insertitem.md) pour ajouter un élément au contrôle header. Le message doit inclure l’adresse d’une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Cette structure définit les propriétés de l’élément d’en-tête, qui peut inclure une chaîne, une image bitmap, une taille initiale et une valeur 32 bits définie par l’application.

L’exemple suivant illustre l’utilisation du message [**HDM \_ INSERTITEM**](hdm-insertitem.md) et de la structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) pour ajouter un élément à un contrôle header. Le nouvel élément est constitué d’une chaîne qui est alignée à gauche dans le rectangle de l’élément.



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles Header](header-controls.md)
</dt> <dt>

[Référence de contrôle header](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Utilisation des contrôles Header](using-header-controls.md)
</dt> </dl>

 

 




