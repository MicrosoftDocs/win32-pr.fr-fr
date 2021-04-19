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
# <a name="how-to-use-tree-view-infotips"></a><span data-ttu-id="11c74-104">Utilisation de Tree-View info-bulles</span><span class="sxs-lookup"><span data-stu-id="11c74-104">How to Use Tree-View Infotips</span></span>

<span data-ttu-id="11c74-105">Lorsque vous appliquez le style de l' [**\_ info-bulle du téléviseur**](tree-view-control-window-styles.md) à un contrôle d’arborescence, il génère des notifications [ \_ GETINFOTIP TVN](tvn-getinfotip.md) lorsque le curseur se trouve sur un élément dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="11c74-105">When you apply the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style to a tree-view control, it generates [TVN\_GETINFOTIP](tvn-getinfotip.md) notifications when the cursor is over an item in the tree view.</span></span> <span data-ttu-id="11c74-106">En répondant à cette notification, vous pouvez définir le texte qui apparaît dans l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="11c74-106">By responding to this notification, you can set the text that appears in the infotip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="11c74-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="11c74-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="11c74-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="11c74-108">Technologies</span></span>

-   [<span data-ttu-id="11c74-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="11c74-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="11c74-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="11c74-110">Prerequisites</span></span>

-   <span data-ttu-id="11c74-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="11c74-111">C/C++</span></span>
-   <span data-ttu-id="11c74-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="11c74-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="11c74-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="11c74-113">Instructions</span></span>

### <a name="use-tree-view-infotips"></a><span data-ttu-id="11c74-114">Utiliser Tree-View info-bulles</span><span class="sxs-lookup"><span data-stu-id="11c74-114">Use Tree-View Infotips</span></span>

<span data-ttu-id="11c74-115">L’exemple de code suivant montre comment une application peut répondre à la notification.</span><span class="sxs-lookup"><span data-stu-id="11c74-115">The following example code shows how an application might respond to the notification.</span></span> <span data-ttu-id="11c74-116">Par souci de simplicité, l’exemple copie simplement le texte de l’élément dans l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="11c74-116">For simplicity, the example just copies the text for the item to the infotip.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="11c74-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11c74-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c74-118">Utilisation de contrôles Tree-View</span><span class="sxs-lookup"><span data-stu-id="11c74-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="11c74-119">L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="11c74-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




