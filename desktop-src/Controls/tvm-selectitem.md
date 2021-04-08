---
title: Message TVM_SELECTITEM (commctrl. h)
description: Sélectionne l’élément d’affichage d’arborescence spécifié, fait défiler l’élément dans l’affichage ou redessine l’élément dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843245"
---
# <a name="tvm_selectitem-message"></a><span data-ttu-id="4c6f6-104">TVM \_ SELECTITEM message</span><span class="sxs-lookup"><span data-stu-id="4c6f6-104">TVM\_SELECTITEM message</span></span>

<span data-ttu-id="4c6f6-105">Sélectionne l’élément d’affichage d’arborescence spécifié, fait défiler l’élément dans l’affichage ou redessine l’élément dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-105">Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.</span></span> <span data-ttu-id="4c6f6-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)ou [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="4c6f6-106">You can send this message explicitly or by using the [**TreeView\_Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem), or [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c6f6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c6f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c6f6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c6f6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c6f6-109">Indicateur d’action.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-109">Action flag.</span></span> <span data-ttu-id="4c6f6-110">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c6f6-110">This parameter can be one of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c6f6-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c6f6-111">Value</span></span></th>
<th><span data-ttu-id="4c6f6-112">Signification</span><span class="sxs-lookup"><span data-stu-id="4c6f6-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="4c6f6-113"><dt><strong>TVGN_CARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4c6f6-113"><dt><strong>TVGN_CARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4c6f6-114">Définit la sélection sur l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-114">Sets the selection to the specified item.</span></span> <span data-ttu-id="4c6f6-115">La fenêtre parente du contrôle Tree-View reçoit les codes de notification <a href="tvn-selchanging.md">TVN_SELCHANGING</a> et <a href="tvn-selchanged.md">TVN_SELCHANGED</a> .</span><span class="sxs-lookup"><span data-stu-id="4c6f6-115">The tree-view control's parent window receives the <a href="tvn-selchanging.md">TVN_SELCHANGING</a> and <a href="tvn-selchanged.md">TVN_SELCHANGED</a> notification codes.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="4c6f6-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4c6f6-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4c6f6-117">Redessine l’élément spécifié dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-117">Redraws the specified item in the style used to indicate the target of a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="4c6f6-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4c6f6-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4c6f6-119">Garantit que l’élément spécifié est visible et, si possible, l’affiche en haut de la fenêtre du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-119">Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window.</span></span> <span data-ttu-id="4c6f6-120">Les contrôles d’arborescence affichent autant d’éléments que possible dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-120">Tree-view controls display as many items as will fit in the window.</span></span> <span data-ttu-id="4c6f6-121">Si l’élément spécifié est proche du bas de la hiérarchie d’éléments du contrôle, il peut ne pas devenir le premier élément visible, en fonction du nombre d’éléments qui tiennent dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-121">If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <span data-ttu-id="4c6f6-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4c6f6-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4c6f6-123">Lorsqu’un seul élément est sélectionné, vérifie que le TreeView ne développe pas les enfants de cet élément.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-123">When a single item is selected, ensures that the treeview does not expand the children of that item.</span></span> <span data-ttu-id="4c6f6-124">Cela n’est valide que s’il est utilisé avec l’indicateur TVGN_CARET.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-124">This is valid only if used with the TVGN_CARET flag.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c6f6-125">Pour utiliser cet indicateur, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-125">To use this flag, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4c6f6-126">Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-126">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="4c6f6-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c6f6-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c6f6-128">Handle vers un élément.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-128">Handle to an item.</span></span> <span data-ttu-id="4c6f6-129">Si *lParam* a la **valeur null**, le contrôle est défini sur ne pas avoir d’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-129">If *lParam* is **NULL**, the control is set to have no selected item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c6f6-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c6f6-130">Return value</span></span>

<span data-ttu-id="4c6f6-131">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c6f6-132">Notes</span><span class="sxs-lookup"><span data-stu-id="4c6f6-132">Remarks</span></span>

<span data-ttu-id="4c6f6-133">Si l’élément spécifié est l’enfant d’un élément parent réduit, la liste des éléments enfants du parent est développée pour révéler l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-133">If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item.</span></span> <span data-ttu-id="4c6f6-134">Dans ce cas, la fenêtre parente du contrôle reçoit les codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="4c6f6-134">In this case, the control's parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

<span data-ttu-id="4c6f6-135">L’utilisation de la macro [**\_ SelectItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) revient à envoyer le message **TVM \_ SelectItem** avec *wParam* défini sur la \_ valeur du signe insertion TVGN.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-135">Using the [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_CARET value.</span></span> <span data-ttu-id="4c6f6-136">L’utilisation de la macro [**\_ SelectDropTarget TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) revient à envoyer le message **TVM \_ SELECTITEM** avec *wParam* défini sur la \_ valeur DROPHILITE TVGN.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-136">Using the [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_DROPHILITE value.</span></span> <span data-ttu-id="4c6f6-137">L’utilisation de [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) revient à envoyer le message **TVM \_ SELECTITEM** avec *wParam* défini sur la \_ valeur FIRSTVISIBLE TVGN.</span><span class="sxs-lookup"><span data-stu-id="4c6f6-137">Using [**TreeView\_SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_FIRSTVISIBLE value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c6f6-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c6f6-138">Requirements</span></span>



| <span data-ttu-id="4c6f6-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c6f6-139">Requirement</span></span> | <span data-ttu-id="4c6f6-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c6f6-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6f6-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c6f6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4c6f6-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c6f6-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c6f6-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c6f6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4c6f6-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c6f6-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c6f6-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c6f6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c6f6-146"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c6f6-146"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





