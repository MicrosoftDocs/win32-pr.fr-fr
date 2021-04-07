---
title: Utilisation des index d’images d’État
description: Il existe souvent une confusion quant à la façon de définir et de récupérer l’index d’images d’État dans un contrôle d’arborescence.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723683"
---
# <a name="how-to-work-with-state-image-indexes"></a><span data-ttu-id="5e3ef-103">Utilisation des index d’images d’État</span><span class="sxs-lookup"><span data-stu-id="5e3ef-103">How to Work With State Image Indexes</span></span>

<span data-ttu-id="5e3ef-104">Il existe souvent une confusion quant à la façon de définir et de récupérer l’index d’images d’État dans un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="5e3ef-104">There is often confusion about how to set and retrieve the state image index in a tree-view control.</span></span> <span data-ttu-id="5e3ef-105">Les exemples suivants illustrent la méthode appropriée pour définir et récupérer l’index d’images d’État.</span><span class="sxs-lookup"><span data-stu-id="5e3ef-105">The following examples demonstrate the proper method for setting and retrieving the state image index.</span></span> <span data-ttu-id="5e3ef-106">Les exemples partent du principe qu’il n’y a que deux index d’images d’État dans le contrôle Tree-View, désactivés et activés.</span><span class="sxs-lookup"><span data-stu-id="5e3ef-106">The examples assume that there are only two state image indexes in the tree-view control, unchecked and checked.</span></span> <span data-ttu-id="5e3ef-107">Si votre application en contient plus de deux, ces fonctions devront être modifiées pour gérer ce cas.</span><span class="sxs-lookup"><span data-stu-id="5e3ef-107">If your application contains more than two, these functions will need to be modified to handle that case.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5e3ef-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="5e3ef-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5e3ef-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="5e3ef-109">Technologies</span></span>

-   [<span data-ttu-id="5e3ef-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="5e3ef-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5e3ef-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="5e3ef-111">Prerequisites</span></span>

-   <span data-ttu-id="5e3ef-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="5e3ef-112">C/C++</span></span>
-   <span data-ttu-id="5e3ef-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="5e3ef-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5e3ef-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="5e3ef-114">Instructions</span></span>

### <a name="set-a-tree-view-items-check-state"></a><span data-ttu-id="5e3ef-115">Définir l’état d’activation d’un élément de Tree-View</span><span class="sxs-lookup"><span data-stu-id="5e3ef-115">Set a Tree-View Item's Check State</span></span>

<span data-ttu-id="5e3ef-116">L’exemple suivant montre comment définir l’état d’activation d’un élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="5e3ef-116">The following example demonstrates how to set a tree-view item's check state.</span></span>


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



### <a name="retrieve-a-tree-view-items-check-state"></a><span data-ttu-id="5e3ef-117">Récupérer l’état d’activation d’un élément de Tree-View</span><span class="sxs-lookup"><span data-stu-id="5e3ef-117">Retrieve a Tree-View Item's Check State</span></span>

<span data-ttu-id="5e3ef-118">L’exemple suivant montre comment récupérer l’état d’activation d’un élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="5e3ef-118">The following example demonstrates how to retrieve a tree-view item's check state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5e3ef-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e3ef-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e3ef-120">Utilisation de contrôles Tree-View</span><span class="sxs-lookup"><span data-stu-id="5e3ef-120">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="5e3ef-121">L’exemple CustDTv illustre un dessin personnalisé dans un contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="5e3ef-121">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




