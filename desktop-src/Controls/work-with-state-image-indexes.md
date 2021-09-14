---
title: Utilisation des index d’images d’État
description: Il existe souvent une confusion quant à la façon de définir et de récupérer l’index d’images d’État dans un contrôle d’arborescence.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115121"
---
# <a name="how-to-work-with-state-image-indexes"></a>Utilisation des index d’images d’État

Il existe souvent une confusion quant à la façon de définir et de récupérer l’index d’images d’État dans un contrôle d’arborescence. Les exemples suivants illustrent la méthode appropriée pour définir et récupérer l’index d’images d’État. Les exemples partent du principe qu’il n’y a que deux index d’images d’État dans le contrôle Tree-View, désactivés et activés. Si votre application en contient plus de deux, ces fonctions devront être modifiées pour gérer ce cas.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="set-a-tree-view-items-check-state"></a>Définir l’état d’activation d’un élément de Tree-View

L’exemple suivant montre comment définir l’état d’activation d’un élément d’affichage d’arborescence.


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a>Récupérer l’état d’activation d’un élément de Tree-View

L’exemple suivant montre comment récupérer l’état d’activation d’un élément d’affichage d’arborescence.


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles Tree-View](using-treeview.md)
</dt> <dt>

[L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




