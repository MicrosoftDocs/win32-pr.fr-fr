---
title: Message TVM_SORTCHILDREN (commctrl. h)
description: Trie les éléments enfants de l’élément parent spécifié dans un contrôle TreeView. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SortChildren TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033193"
---
# <a name="tvm_sortchildren-message"></a><span data-ttu-id="a784b-105">TVM \_ SORTCHILDREN message</span><span class="sxs-lookup"><span data-stu-id="a784b-105">TVM\_SORTCHILDREN message</span></span>

<span data-ttu-id="a784b-106">Trie les éléments enfants de l’élément parent spécifié dans un contrôle TreeView.</span><span class="sxs-lookup"><span data-stu-id="a784b-106">Sorts the child items of the specified parent item in a tree-view control.</span></span> <span data-ttu-id="a784b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SortChildren TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .</span><span class="sxs-lookup"><span data-stu-id="a784b-107">You can send this message explicitly or by using the [**TreeView\_SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a784b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a784b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a784b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a784b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a784b-110">Valeur qui spécifie si le tri est récursif.</span><span class="sxs-lookup"><span data-stu-id="a784b-110">Value that specifies whether the sorting is recursive.</span></span> <span data-ttu-id="a784b-111">Affectez à *wParam* la **valeur true** pour trier tous les niveaux d’éléments enfants au-dessous de l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="a784b-111">Set *wParam* to **TRUE** to sort all levels of child items below the parent item.</span></span> <span data-ttu-id="a784b-112">Dans le cas contraire, seuls les enfants immédiats du parent sont triés.</span><span class="sxs-lookup"><span data-stu-id="a784b-112">Otherwise, only the parent's immediate children are sorted.</span></span>

</dd> <dt>

<span data-ttu-id="a784b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a784b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a784b-114">Handle vers l’élément parent dont les éléments enfants doivent être triés.</span><span class="sxs-lookup"><span data-stu-id="a784b-114">Handle to the parent item whose child items are to be sorted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a784b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a784b-115">Return value</span></span>

<span data-ttu-id="a784b-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a784b-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a784b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a784b-117">Remarks</span></span>

<span data-ttu-id="a784b-118">Ce message alphabetizes les éléments d’arborescence à l’aide de [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) sur le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a784b-118">This message alphabetizes the tree items using [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) on the item name.</span></span> <span data-ttu-id="a784b-119">Vous pouvez utiliser le message [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) pour personnaliser le comportement de classement.</span><span class="sxs-lookup"><span data-stu-id="a784b-119">You can use the [**TVM\_SORTCHILDRENCB**](tvm-sortchildrencb.md) message to customize the ordering behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="a784b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a784b-120">Requirements</span></span>



| <span data-ttu-id="a784b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a784b-121">Requirement</span></span> | <span data-ttu-id="a784b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a784b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a784b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a784b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a784b-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a784b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a784b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a784b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a784b-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a784b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a784b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a784b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a784b-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a784b-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

