---
title: Message LVM_REDRAWITEMS (commctrl. h)
description: Force un contrôle List-View à redessiner une plage d’éléments. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView RedrawItems.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032841"
---
# <a name="lvm_redrawitems-message"></a><span data-ttu-id="dc308-105">\_Message REDRAWITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="dc308-105">LVM\_REDRAWITEMS message</span></span>

<span data-ttu-id="dc308-106">Force un contrôle List-View à redessiner une plage d’éléments.</span><span class="sxs-lookup"><span data-stu-id="dc308-106">Forces a list-view control to redraw a range of items.</span></span> <span data-ttu-id="dc308-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .</span><span class="sxs-lookup"><span data-stu-id="dc308-107">You can send this message explicitly or by using the [**ListView\_RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc308-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc308-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc308-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc308-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc308-110">Index du premier élément à redessiner.</span><span class="sxs-lookup"><span data-stu-id="dc308-110">Index of the first item to redraw.</span></span>

</dd> <dt>

<span data-ttu-id="dc308-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc308-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc308-112">Index du dernier élément à redessiner.</span><span class="sxs-lookup"><span data-stu-id="dc308-112">Index of the last item to redraw.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc308-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc308-113">Return value</span></span>

<span data-ttu-id="dc308-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dc308-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc308-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dc308-115">Remarks</span></span>

<span data-ttu-id="dc308-116">Les éléments spécifiés ne sont pas réellement redessinés tant que la fenêtre de vue liste n’a pas reçu de message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) à redessiner.</span><span class="sxs-lookup"><span data-stu-id="dc308-116">The specified items are not actually redrawn until the list-view window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message to repaint.</span></span> <span data-ttu-id="dc308-117">Pour redessiner immédiatement, appelez la fonction [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) après avoir utilisé cette macro.</span><span class="sxs-lookup"><span data-stu-id="dc308-117">To repaint immediately, call the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function after using this macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc308-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc308-118">Requirements</span></span>



| <span data-ttu-id="dc308-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc308-119">Requirement</span></span> | <span data-ttu-id="dc308-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc308-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc308-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc308-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc308-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc308-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc308-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc308-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc308-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc308-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc308-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc308-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc308-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc308-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

