---
title: Utilisation de Tree-View info-bulles
description: Lorsque vous appliquez le \_ style de l’info-bulle du téléviseur à un contrôle d’arborescence, il génère \_ des notifications GETINFOTIP TVN lorsque le curseur se trouve sur un élément dans l’arborescence. En répondant à cette notification, vous pouvez définir le texte qui apparaît dans l’info-bulle.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "106511062"
---
# <a name="how-to-use-tree-view-infotips"></a>Utilisation de Tree-View info-bulles

Lorsque vous appliquez le style de l' [**\_ info-bulle du téléviseur**](tree-view-control-window-styles.md) à un contrôle d’arborescence, il génère des notifications [ \_ GETINFOTIP TVN](tvn-getinfotip.md) lorsque le curseur se trouve sur un élément dans l’arborescence. En répondant à cette notification, vous pouvez définir le texte qui apparaît dans l’info-bulle.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="use-tree-view-infotips"></a>Utiliser Tree-View info-bulles

L’exemple de code suivant montre comment une application peut répondre à la notification. Par souci de simplicité, l’exemple copie simplement le texte de l’élément dans l’info-bulle.


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles Tree-View](using-treeview.md)
</dt> <dt>

[L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




