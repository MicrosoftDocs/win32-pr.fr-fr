---
title: Message TVM_ENSUREVISIBLE (commctrl. h)
description: Garantit qu’un élément d’arborescence est visible, en développant l’élément parent ou en faisant défiler le contrôle d’arborescence, si nécessaire. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro EnsureVisible TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941941"
---
# <a name="tvm_ensurevisible-message"></a><span data-ttu-id="83ba7-105">TVM \_ ENSUREVISIBLE message</span><span class="sxs-lookup"><span data-stu-id="83ba7-105">TVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="83ba7-106">Garantit qu’un élément d’arborescence est visible, en développant l’élément parent ou en faisant défiler le contrôle d’arborescence, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="83ba7-106">Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary.</span></span> <span data-ttu-id="83ba7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ EnsureVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="83ba7-107">You can send this message explicitly or by using the [**TreeView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="83ba7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83ba7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83ba7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83ba7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="83ba7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="83ba7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="83ba7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83ba7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83ba7-112">Handle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="83ba7-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83ba7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83ba7-113">Return value</span></span>

<span data-ttu-id="83ba7-114">Retourne une valeur différente de zéro si le système a fait défiler les éléments dans le contrôle Tree-View et qu’aucun élément n’a été développé.</span><span class="sxs-lookup"><span data-stu-id="83ba7-114">Returns nonzero if the system scrolled the items in the tree-view control and no items were expanded.</span></span> <span data-ttu-id="83ba7-115">Dans le cas contraire, le message retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="83ba7-115">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="83ba7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="83ba7-116">Remarks</span></span>

<span data-ttu-id="83ba7-117">Si le \_ message TVM ENSUREVISIBLE développe l’élément parent, la fenêtre parente reçoit les codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="83ba7-117">If the TVM\_ENSUREVISIBLE message expands the parent item, the parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="83ba7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83ba7-118">Requirements</span></span>



| <span data-ttu-id="83ba7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83ba7-119">Requirement</span></span> | <span data-ttu-id="83ba7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="83ba7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83ba7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83ba7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="83ba7-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83ba7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83ba7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83ba7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="83ba7-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83ba7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83ba7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="83ba7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="83ba7-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83ba7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





