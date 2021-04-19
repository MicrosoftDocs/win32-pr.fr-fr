---
title: États de l’élément de contrôle Tree-View (CommCtrl. h)
description: Cette section répertorie les indicateurs d’état d’élément utilisés pour indiquer l’état d’un élément dans un contrôle Tree-View.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541070"
---
# <a name="tree-view-control-item-states"></a><span data-ttu-id="7b669-103">États des éléments de contrôle Tree-View</span><span class="sxs-lookup"><span data-stu-id="7b669-103">Tree-View Control Item States</span></span>

<span data-ttu-id="7b669-104">Cette section répertorie les indicateurs d’état d’élément utilisés pour indiquer l’état d’un élément dans un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="7b669-104">This section lists the item state flags used to indicate the state of an item in a tree-view control.</span></span>



| <span data-ttu-id="7b669-105">Constante</span><span class="sxs-lookup"><span data-stu-id="7b669-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="7b669-106">Description</span><span class="sxs-lookup"><span data-stu-id="7b669-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <span data-ttu-id="7b669-107"><dt>**TVIS \_ gras**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-107"><dt>**TVIS\_BOLD**</dt></span></span> </dl>                               | <span data-ttu-id="7b669-108">L’élément est en gras.</span><span class="sxs-lookup"><span data-stu-id="7b669-108">The item is bold.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <span data-ttu-id="7b669-109"><dt>**TVIS \_ couper**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-109"><dt>**TVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="7b669-110">L’élément est sélectionné dans le cadre d’une opération de couper-coller.</span><span class="sxs-lookup"><span data-stu-id="7b669-110">The item is selected as part of a cut-and-paste operation.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <span data-ttu-id="7b669-111"><dt>**TVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-111"><dt>**TVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="7b669-112">L’élément est sélectionné comme cible de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="7b669-112">The item is selected as a drag-and-drop target.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <span data-ttu-id="7b669-113"><dt>**TVIS \_ développé**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-113"><dt>**TVIS\_EXPANDED**</dt></span></span> </dl>                   | <span data-ttu-id="7b669-114">La liste des éléments enfants de l’élément est actuellement développée ; autrement dit, les éléments enfants sont visibles.</span><span class="sxs-lookup"><span data-stu-id="7b669-114">The item's list of child items is currently expanded; that is, the child items are visible.</span></span> <span data-ttu-id="7b669-115">Cette valeur s’applique uniquement aux éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7b669-115">This value applies only to parent items.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <span data-ttu-id="7b669-116"><dt>**TVIS \_ EXPANDEDONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-116"><dt>**TVIS\_EXPANDEDONCE**</dt></span></span> </dl>       | <span data-ttu-id="7b669-117">La liste des éléments enfants de l’élément a été développée au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="7b669-117">The item's list of child items has been expanded at least once.</span></span> <span data-ttu-id="7b669-118">Les codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) ne sont pas générés pour les éléments parents pour lesquels cet État est défini en réponse à un message de [**\_ développement TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="7b669-118">The [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes are not generated for parent items that have this state set in response to a [**TVM\_EXPAND**](tvm-expand.md) message.</span></span> <span data-ttu-id="7b669-119">L’utilisation de TVE \_ Collapse et TVE \_ COLLAPSERESET avec **TVM \_ expand** entraîne la réinitialisation de cet État.</span><span class="sxs-lookup"><span data-stu-id="7b669-119">Using TVE\_COLLAPSE and TVE\_COLLAPSERESET with **TVM\_EXPAND** will cause this state to be reset.</span></span> <span data-ttu-id="7b669-120">Cette valeur s’applique uniquement aux éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7b669-120">This value applies only to parent items.</span></span> <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <span data-ttu-id="7b669-121"><dt>**TVIS \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-121"><dt>**TVIS\_EXPANDPARTIAL**</dt></span></span> </dl>    | <span data-ttu-id="7b669-122">**Version 4,70**.</span><span class="sxs-lookup"><span data-stu-id="7b669-122">**Version 4.70**.</span></span> <span data-ttu-id="7b669-123">Élément d’arborescence partiellement développé.</span><span class="sxs-lookup"><span data-stu-id="7b669-123">A partially expanded tree-view item.</span></span> <span data-ttu-id="7b669-124">Dans cet État, certains, mais pas tous, des éléments enfants sont visibles et le symbole plus du parent de l’élément est affiché.</span><span class="sxs-lookup"><span data-stu-id="7b669-124">In this state, some, but not all, of the child items are visible and the parent item's plus symbol is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <span data-ttu-id="7b669-125"><dt>**TVIS \_ sélectionné**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-125"><dt>**TVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="7b669-126">L'élément est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7b669-126">The item is selected.</span></span> <span data-ttu-id="7b669-127">Son apparence varie selon qu’elle a le focus.</span><span class="sxs-lookup"><span data-stu-id="7b669-127">Its appearance depends on whether it has the focus.</span></span> <span data-ttu-id="7b669-128">L’élément est dessiné à l’aide des couleurs système pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="7b669-128">The item will be drawn using the system colors for selection.</span></span> <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <span data-ttu-id="7b669-129"><dt>**TVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-129"><dt>**TVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="7b669-130">Masque pour les bits utilisés pour spécifier l’index d’image de superposition de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7b669-130">Mask for the bits used to specify the item's overlay image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <span data-ttu-id="7b669-131"><dt>**TVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-131"><dt>**TVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="7b669-132">Masque pour les bits utilisés pour spécifier l’index d’image d’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7b669-132">Mask for the bits used to specify the item's state image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <span data-ttu-id="7b669-133"><dt>**TVIS \_ USERMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-133"><dt>**TVIS\_USERMASK**</dt></span></span> </dl>                   | <span data-ttu-id="7b669-134">Identique à **Tvis \_ STATEIMAGEMASK**.</span><span class="sxs-lookup"><span data-stu-id="7b669-134">Same as **TVIS\_STATEIMAGEMASK**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="7b669-135">Notes</span><span class="sxs-lookup"><span data-stu-id="7b669-135">Remarks</span></span>

<span data-ttu-id="7b669-136">Lorsque vous définissez ou récupérez l’index d’image de superposition ou l’index d’images d’état d’un élément, vous devez spécifier les masques suivants dans le membre **stateMask** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :</span><span class="sxs-lookup"><span data-stu-id="7b669-136">When you set or retrieve an item's overlay image index or state image index, you must specify the following masks in the **stateMask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure:</span></span>

-   <span data-ttu-id="7b669-137">**TVIS \_ OVERLAYMASK**</span><span class="sxs-lookup"><span data-stu-id="7b669-137">**TVIS\_OVERLAYMASK**</span></span>
-   <span data-ttu-id="7b669-138">**TVIS \_ STATEIMAGEMASK**</span><span class="sxs-lookup"><span data-stu-id="7b669-138">**TVIS\_STATEIMAGEMASK**</span></span>
-   <span data-ttu-id="7b669-139">**TVIS \_ USERMASK**</span><span class="sxs-lookup"><span data-stu-id="7b669-139">**TVIS\_USERMASK**</span></span>

<span data-ttu-id="7b669-140">Ces valeurs peuvent également être utilisées pour masquer les bits d’État qui ne sont pas intéressants.</span><span class="sxs-lookup"><span data-stu-id="7b669-140">These values can also be used to mask off the state bits that are not of interest.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b669-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b669-141">Requirements</span></span>



| <span data-ttu-id="7b669-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b669-142">Requirement</span></span> | <span data-ttu-id="7b669-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b669-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b669-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b669-144">Header</span></span><br/> | <dl> <span data-ttu-id="7b669-145"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b669-145"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





