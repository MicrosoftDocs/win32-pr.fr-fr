---
title: Message TVM_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip enfant utilisé par un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetToolTips TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- TVM_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464762"
---
# <a name="tvm_gettooltips-message"></a><span data-ttu-id="c7204-105">TVM \_ GETTOOLTIPS message</span><span class="sxs-lookup"><span data-stu-id="c7204-105">TVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="c7204-106">Récupère le handle du contrôle ToolTip enfant utilisé par un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="c7204-106">Retrieves the handle to the child tooltip control used by a tree-view control.</span></span> <span data-ttu-id="c7204-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetToolTips TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="c7204-107">You can send this message explicitly or by using the [**TreeView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7204-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7204-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7204-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7204-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c7204-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c7204-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c7204-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7204-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c7204-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c7204-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7204-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7204-113">Return value</span></span>

<span data-ttu-id="c7204-114">Retourne le handle du contrôle ToolTip enfant, ou **null** si le contrôle n’utilise pas d’info-bulles.</span><span class="sxs-lookup"><span data-stu-id="c7204-114">Returns the handle to the child tooltip control, or **NULL** if the control is not using tooltips.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7204-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c7204-115">Remarks</span></span>

<span data-ttu-id="c7204-116">En cas de création, les contrôles d’arborescence créent automatiquement un contrôle ToolTip enfant.</span><span class="sxs-lookup"><span data-stu-id="c7204-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="c7204-117">Pour faire en sorte qu’un contrôle d’arborescence n’utilise pas les info-bulles, créez le contrôle avec le style [**TV \_ noInfos**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c7204-117">To cause a tree-view control not to use tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7204-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7204-118">Requirements</span></span>



| <span data-ttu-id="c7204-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7204-119">Requirement</span></span> | <span data-ttu-id="c7204-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7204-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7204-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7204-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7204-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7204-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7204-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7204-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7204-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7204-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7204-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7204-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7204-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7204-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7204-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7204-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7204-128">**TVM \_ SETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="c7204-128">**TVM\_SETTOOLTIPS**</span></span>](tvm-settooltips.md)
</dt> </dl>

 

 





