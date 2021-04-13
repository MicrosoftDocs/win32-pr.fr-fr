---
title: Message WM_DWMWINDOWMAXIMIZEDCHANGE (winuser. h)
description: Envoyé lorsqu’une fenêtre composée de Gestionnaire de fenêtrage (DWM) est agrandie.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Message de WM_DWMWINDOWMAXIMIZEDCHANGE Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384732"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a><span data-ttu-id="6bdba-104">\_Message WM DWMWINDOWMAXIMIZEDCHANGE</span><span class="sxs-lookup"><span data-stu-id="6bdba-104">WM\_DWMWINDOWMAXIMIZEDCHANGE message</span></span>

<span data-ttu-id="6bdba-105">Envoyé lorsqu’une fenêtre composée de Gestionnaire de fenêtrage (DWM) est agrandie.</span><span class="sxs-lookup"><span data-stu-id="6bdba-105">Sent when a Desktop Window Manager (DWM) composed window is maximized.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bdba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bdba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bdba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bdba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bdba-108">Affectez la valeur true pour spécifier que la fenêtre a été agrandie.</span><span class="sxs-lookup"><span data-stu-id="6bdba-108">Set to true to specify that the window has been maximized.</span></span>

</dd> <dt>

<span data-ttu-id="6bdba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bdba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bdba-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6bdba-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bdba-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6bdba-111">Return value</span></span>

<span data-ttu-id="6bdba-112">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6bdba-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bdba-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6bdba-113">Remarks</span></span>

<span data-ttu-id="6bdba-114">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6bdba-114">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bdba-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bdba-115">Requirements</span></span>



| <span data-ttu-id="6bdba-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bdba-116">Requirement</span></span> | <span data-ttu-id="6bdba-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bdba-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdba-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bdba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6bdba-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bdba-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6bdba-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bdba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6bdba-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bdba-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6bdba-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6bdba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bdba-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bdba-123"><dt>Winuser.h</dt></span></span> </dl> |



 

