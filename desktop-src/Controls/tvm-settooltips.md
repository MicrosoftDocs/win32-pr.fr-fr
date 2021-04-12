---
title: Message TVM_SETTOOLTIPS (commctrl. h)
description: Définit le contrôle d’info-bulle enfant d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetToolTips TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103624"
---
# <a name="tvm_settooltips-message"></a><span data-ttu-id="5786d-105">TVM \_ SETTOOLTIPS message</span><span class="sxs-lookup"><span data-stu-id="5786d-105">TVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="5786d-106">Définit le contrôle d’info-bulle enfant d’un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="5786d-106">Sets a tree-view control's child tooltip control.</span></span> <span data-ttu-id="5786d-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetToolTips TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="5786d-107">You can send this message explicitly or by using the [**TreeView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5786d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5786d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5786d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5786d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5786d-110">Handle d’un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="5786d-110">Handle to a tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="5786d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5786d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5786d-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5786d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5786d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5786d-113">Return value</span></span>

<span data-ttu-id="5786d-114">Retourne le handle du contrôle ToolTip précédemment défini pour le contrôle Tree-View, ou **null** si les info-bulles n’ont pas été utilisées précédemment.</span><span class="sxs-lookup"><span data-stu-id="5786d-114">Returns the handle to tooltip control previously set for the tree-view control, or **NULL** if tooltips were not previously used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5786d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5786d-115">Remarks</span></span>

<span data-ttu-id="5786d-116">En cas de création, les contrôles d’arborescence créent automatiquement un contrôle ToolTip enfant.</span><span class="sxs-lookup"><span data-stu-id="5786d-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="5786d-117">Pour empêcher l’affichage d’un contrôle d’arborescence à l’aide d’info-bulles, créez le contrôle avec le style [**TV \_ noInfos**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5786d-117">To prevent a tree-view control from using tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5786d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5786d-118">Requirements</span></span>



| <span data-ttu-id="5786d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5786d-119">Requirement</span></span> | <span data-ttu-id="5786d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5786d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5786d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5786d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5786d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5786d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5786d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5786d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5786d-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5786d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5786d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5786d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5786d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5786d-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5786d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5786d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5786d-128">**TVM \_ GETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="5786d-128">**TVM\_GETTOOLTIPS**</span></span>](tvm-gettooltips.md)
</dt> </dl>

 

 





