---
title: Message TVM_DELETEITEM (commctrl. h)
description: Supprime un élément et tous ses enfants d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView DeleteItem.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465466"
---
# <a name="tvm_deleteitem-message"></a><span data-ttu-id="518c1-105">TVM- \_ message DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="518c1-105">TVM\_DELETEITEM message</span></span>

<span data-ttu-id="518c1-106">Supprime un élément et tous ses enfants d’un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="518c1-106">Removes an item and all its children from a tree-view control.</span></span> <span data-ttu-id="518c1-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="518c1-107">You can send this message explicitly or by using the [**TreeView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="518c1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="518c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="518c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="518c1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="518c1-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="518c1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="518c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="518c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="518c1-112">**HTREEITEM** handle de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="518c1-112">**HTREEITEM** handle to the item to delete.</span></span> <span data-ttu-id="518c1-113">Si *lParam* a la valeur \_ root TVI ou la **valeur null**, tous les éléments sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="518c1-113">If *lParam* is set to TVI\_ROOT or to **NULL**, all items are deleted.</span></span> <span data-ttu-id="518c1-114">Vous pouvez également utiliser la [**macro \_ DeleteAllItems TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) pour supprimer tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="518c1-114">You can also use the [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) macro to delete all items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="518c1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="518c1-115">Return value</span></span>

<span data-ttu-id="518c1-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="518c1-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="518c1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="518c1-117">Remarks</span></span>

<span data-ttu-id="518c1-118">Il n’est pas possible de supprimer des éléments en réponse à une notification telle que [TVN \_ SELCHANGING](tvn-selchanging.md).</span><span class="sxs-lookup"><span data-stu-id="518c1-118">It is not safe to delete items in response to a notification such as [TVN\_SELCHANGING](tvn-selchanging.md).</span></span>

<span data-ttu-id="518c1-119">Une fois qu’un élément est supprimé, son handle n’est pas valide et ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="518c1-119">Once an item is deleted, its handle is invalid and cannot be used.</span></span>

<span data-ttu-id="518c1-120">La fenêtre parente reçoit un code de notification [TVN \_ DELETEITEM](tvn-deleteitem.md) lorsque chaque élément est supprimé.</span><span class="sxs-lookup"><span data-stu-id="518c1-120">The parent window receives a [TVN\_DELETEITEM](tvn-deleteitem.md) notification code when each item is removed.</span></span>

<span data-ttu-id="518c1-121">Si l’étiquette de l’élément est en cours de modification, l’opération de modification est annulée et la fenêtre parente reçoit le code de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="518c1-121">If the item label is being edited, the edit operation is canceled and the parent window receives the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

<span data-ttu-id="518c1-122">Si vous supprimez tous les éléments d’un contrôle Tree-View qui a le style de [**\_ défilement TV**](tree-view-control-window-styles.md) , les éléments ajoutés ultérieurement peuvent ne pas s’afficher correctement.</span><span class="sxs-lookup"><span data-stu-id="518c1-122">If you delete all items in a tree-view control that has the [**TVS\_NOSCROLL**](tree-view-control-window-styles.md) style, items subsequently added may not display properly.</span></span> <span data-ttu-id="518c1-123">Pour plus d’informations, consultez [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span><span class="sxs-lookup"><span data-stu-id="518c1-123">For more information, see [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span></span>

## <a name="requirements"></a><span data-ttu-id="518c1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="518c1-124">Requirements</span></span>



| <span data-ttu-id="518c1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="518c1-125">Requirement</span></span> | <span data-ttu-id="518c1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="518c1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="518c1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="518c1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="518c1-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="518c1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="518c1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="518c1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="518c1-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="518c1-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="518c1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="518c1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="518c1-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="518c1-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





