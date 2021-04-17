---
title: Message TVM_EXPAND (commctrl. h)
description: La TVM \_ expand message développe ou réduit la liste des éléments enfants associés à l’élément parent spécifié, le cas échéant. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro Expand TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- TVM_EXPAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466487"
---
# <a name="tvm_expand-message"></a><span data-ttu-id="bce17-105">TVM- \_ développer le message</span><span class="sxs-lookup"><span data-stu-id="bce17-105">TVM\_EXPAND message</span></span>

<span data-ttu-id="bce17-106">La **TVM \_ expand** message développe ou réduit la liste des éléments enfants associés à l’élément parent spécifié, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bce17-106">The **TVM\_EXPAND** message expands or collapses the list of child items associated with the specified parent item, if any.</span></span> <span data-ttu-id="bce17-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ expand TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .</span><span class="sxs-lookup"><span data-stu-id="bce17-107">You can send this message explicitly or by using the [**TreeView\_Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bce17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bce17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce17-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bce17-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bce17-110">Indicateur d’action.</span><span class="sxs-lookup"><span data-stu-id="bce17-110">Action flag.</span></span> <span data-ttu-id="bce17-111">Ce paramètre peut être une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bce17-111">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="bce17-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bce17-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="bce17-113">Signification</span><span class="sxs-lookup"><span data-stu-id="bce17-113">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <span data-ttu-id="bce17-114"><dt>**TVE \_ réduire**</dt></span><span class="sxs-lookup"><span data-stu-id="bce17-114"><dt>**TVE\_COLLAPSE**</dt></span></span> </dl>                | <span data-ttu-id="bce17-115">Réduit la liste.</span><span class="sxs-lookup"><span data-stu-id="bce17-115">Collapses the list.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <span data-ttu-id="bce17-116"><dt>**TVE \_ COLLAPSERESET**</dt></span><span class="sxs-lookup"><span data-stu-id="bce17-116"><dt>**TVE\_COLLAPSERESET**</dt></span></span> </dl> | <span data-ttu-id="bce17-117">Réduit la liste et supprime les éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="bce17-117">Collapses the list and removes the child items.</span></span> <span data-ttu-id="bce17-118">L’indicateur d’état [**Tvis \_ EXPANDEDONCE**](tree-view-control-item-states.md) est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="bce17-118">The [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is reset.</span></span> <span data-ttu-id="bce17-119">Cet indicateur doit être utilisé avec l' \_ indicateur de réduction TVE.</span><span class="sxs-lookup"><span data-stu-id="bce17-119">This flag must be used with the TVE\_COLLAPSE flag.</span></span><br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <span data-ttu-id="bce17-120"><dt>**TVE \_ développer**</dt></span><span class="sxs-lookup"><span data-stu-id="bce17-120"><dt>**TVE\_EXPAND**</dt></span></span> </dl>                      | <span data-ttu-id="bce17-121">Développe la liste.</span><span class="sxs-lookup"><span data-stu-id="bce17-121">Expands the list.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <span data-ttu-id="bce17-122"><dt>**TVE \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="bce17-122"><dt>**TVE\_EXPANDPARTIAL**</dt></span></span> </dl> | <span data-ttu-id="bce17-123">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="bce17-123">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="bce17-124">Développe partiellement la liste.</span><span class="sxs-lookup"><span data-stu-id="bce17-124">Partially expands the list.</span></span> <span data-ttu-id="bce17-125">Dans cet État, les éléments enfants sont visibles et le signe plus (+) de l’élément parent, indiquant qu’il peut être développé, est affiché.</span><span class="sxs-lookup"><span data-stu-id="bce17-125">In this state the child items are visible and the parent item's plus sign (+), indicating that it can be expanded, is displayed.</span></span> <span data-ttu-id="bce17-126">Cet indicateur doit être utilisé en association avec l' \_ indicateur de développement TVE.</span><span class="sxs-lookup"><span data-stu-id="bce17-126">This flag must be used in combination with the TVE\_EXPAND flag.</span></span><br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <span data-ttu-id="bce17-127"><dt>**TVE \_ bascule**</dt></span><span class="sxs-lookup"><span data-stu-id="bce17-127"><dt>**TVE\_TOGGLE**</dt></span></span> </dl>                      | <span data-ttu-id="bce17-128">Réduit la liste si elle est développée ou développée si elle est réduite.</span><span class="sxs-lookup"><span data-stu-id="bce17-128">Collapses the list if it is expanded or expands it if it is collapsed.</span></span><br/>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="bce17-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bce17-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bce17-130">Handle vers l’élément parent à développer ou réduire.</span><span class="sxs-lookup"><span data-stu-id="bce17-130">Handle to the parent item to expand or collapse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce17-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bce17-131">Return value</span></span>

<span data-ttu-id="bce17-132">Retourne une valeur différente de zéro si l’opération a réussi, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bce17-132">Returns nonzero if the operation was successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bce17-133">Notes</span><span class="sxs-lookup"><span data-stu-id="bce17-133">Remarks</span></span>

<span data-ttu-id="bce17-134">Le développement d’un nœud déjà développé est considéré comme une opération réussie et [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bce17-134">Expanding a node that is already expanded is considered a successful operation and [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns a nonzero value.</span></span> <span data-ttu-id="bce17-135">La réduction d’un nœud retourne la valeur zéro si le nœud est déjà réduit ; Sinon, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bce17-135">Collapsing a node returns zero if the node is already collapsed; otherwise it returns nonzero.</span></span> <span data-ttu-id="bce17-136">Toute tentative de développement ou de réduction d’un nœud qui n’a pas d’enfants est considérée comme un échec et **SendMessage** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="bce17-136">Attempting to expand or collapse a node that has no children is considered a failure and **SendMessage** returns zero.</span></span>

<span data-ttu-id="bce17-137">Lorsqu’un élément est développé pour la première fois par un message de **\_ développement TVM** , l’action génère des codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) et l' [**indicateur d’État Tvis EXPANDEDONCE de \_**](tree-view-control-item-states.md) l’élément est défini.</span><span class="sxs-lookup"><span data-stu-id="bce17-137">When an item is first expanded by a **TVM\_EXPAND** message, the action generates [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes and the item's [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is set.</span></span> <span data-ttu-id="bce17-138">Tant que cet indicateur d’état reste défini, les messages de l' **\_ extension TVM** suivante ne génèrent pas de \_ notifications TVN ITEMEXPANDING ou TVN \_ ITEMEXPANDED.</span><span class="sxs-lookup"><span data-stu-id="bce17-138">As long as this state flag remains set, subsequent **TVM\_EXPAND** messages do not generate TVN\_ITEMEXPANDING or TVN\_ITEMEXPANDED notifications.</span></span> <span data-ttu-id="bce17-139">Pour réinitialiser l’indicateur d’état **Tvis \_ EXPANDEDONCE** , vous devez envoyer un message de **\_ développement TVM** avec les \_ indicateurs TVE Collapse et TVE \_ COLLAPSERESET définis.</span><span class="sxs-lookup"><span data-stu-id="bce17-139">To reset the **TVIS\_EXPANDEDONCE** state flag, you must send a **TVM\_EXPAND** message with the TVE\_COLLAPSE and TVE\_COLLAPSERESET flags set.</span></span> <span data-ttu-id="bce17-140">Toute tentative de définition explicite de **\_ EXPANDEDONCE Tvis** entraîne un comportement imprévisible.</span><span class="sxs-lookup"><span data-stu-id="bce17-140">Attempting to explicitly set **TVIS\_EXPANDEDONCE** will result in unpredictable behavior.</span></span>

<span data-ttu-id="bce17-141">L’opération de développement peut échouer si le propriétaire du contrôle TreeView refuse l’opération en réponse à une [notification \_ ITEMEXPANDING TVN](tvn-itemexpanding.md) .</span><span class="sxs-lookup"><span data-stu-id="bce17-141">The expand operation may fail if the owner of the treeview control denies the operation in response to a [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce17-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bce17-142">Requirements</span></span>



| <span data-ttu-id="bce17-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bce17-143">Requirement</span></span> | <span data-ttu-id="bce17-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="bce17-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bce17-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bce17-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bce17-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bce17-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bce17-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bce17-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bce17-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bce17-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bce17-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="bce17-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="bce17-150"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bce17-150"><dt>Commctrl.h</dt></span></span> </dl> |



 

