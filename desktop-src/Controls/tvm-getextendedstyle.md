---
title: Message TVM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère le style étendu pour un contrôle Tree-View. Envoyez ce message explicitement ou à l’aide de la \_ macro GetExtendedStyle TreeView.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844253"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a><span data-ttu-id="26e98-105">Message TVM_GETEXTENDEDSTYLE (commctrl. h)</span><span class="sxs-lookup"><span data-stu-id="26e98-105">TVM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="26e98-106">Récupère le style étendu pour un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="26e98-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="26e98-107">Envoyez ce message explicitement ou à l’aide de la macro [**\_ GetExtendedStyle TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="26e98-107">Send this message explicitly or by using the [**TreeView\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="26e98-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26e98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e98-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26e98-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="26e98-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="26e98-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="26e98-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26e98-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="26e98-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="26e98-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e98-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26e98-113">Return value</span></span>

<span data-ttu-id="26e98-114">Retourne la valeur du style étendu. Pour plus d’informations sur les styles, consultez [styles étendus de contrôle d’arborescence](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="26e98-114">Returns the value of extended style.For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26e98-115">Notes</span><span class="sxs-lookup"><span data-stu-id="26e98-115">Remarks</span></span>

<span data-ttu-id="26e98-116">Les styles étendus pour un contrôle d’arborescence n’ont rien à voir avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="26e98-116">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="26e98-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26e98-117">Requirements</span></span>



| <span data-ttu-id="26e98-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26e98-118">Requirement</span></span> | <span data-ttu-id="26e98-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="26e98-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26e98-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26e98-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26e98-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26e98-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26e98-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26e98-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26e98-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26e98-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26e98-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="26e98-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e98-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e98-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

