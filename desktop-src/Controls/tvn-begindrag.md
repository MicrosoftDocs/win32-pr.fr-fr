---
title: TVN_BEGINDRAG le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View qu’une opération de glisser-déplacer impliquant le bouton gauche de la souris est en cours d’initialisation. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- Contrôles Windows de code de notification TVN_BEGINDRAG
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843654"
---
# <a name="tvn_begindrag-notification-code"></a><span data-ttu-id="835bb-105">\_Code de notification TVN BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="835bb-105">TVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="835bb-106">Avertit une fenêtre parente d’un contrôle Tree-View qu’une opération de glisser-déplacer impliquant le bouton gauche de la souris est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="835bb-106">Notifies a tree-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="835bb-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="835bb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="835bb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="835bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="835bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="835bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="835bb-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="835bb-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="835bb-111">Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément déplacé dans les membres **hitem**, **State** et **lParam** .</span><span class="sxs-lookup"><span data-stu-id="835bb-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being dragged in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="835bb-112">Le membre **ptDrag** spécifie les coordonnées d’écran actuelles de la souris.</span><span class="sxs-lookup"><span data-stu-id="835bb-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="835bb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="835bb-113">Return value</span></span>

<span data-ttu-id="835bb-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="835bb-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="835bb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="835bb-115">Remarks</span></span>

<span data-ttu-id="835bb-116">Un contrôle d’arborescence avec le style [**TV \_ DISABLEDRAGDROP**](tree-view-control-window-styles.md) style n’envoie pas ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="835bb-116">A tree-view control that has the [**TVS\_DISABLEDRAGDROP**](tree-view-control-window-styles.md) style does not send this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="835bb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="835bb-117">Requirements</span></span>



| <span data-ttu-id="835bb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="835bb-118">Requirement</span></span> | <span data-ttu-id="835bb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="835bb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="835bb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="835bb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="835bb-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="835bb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="835bb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="835bb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="835bb-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="835bb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="835bb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="835bb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="835bb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="835bb-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="835bb-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="835bb-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="835bb-127">**TVN \_ BEGINDRAGW** (Unicode) et **TVN \_ BEGINDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="835bb-127">**TVN\_BEGINDRAGW** (Unicode) and **TVN\_BEGINDRAGA** (ANSI)</span></span><br/>               |



 

 





