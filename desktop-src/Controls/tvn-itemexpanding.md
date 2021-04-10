---
title: TVN_ITEMEXPANDING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent est sur le point d’être développée ou réduite. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- Contrôles Windows de code de notification TVN_ITEMEXPANDING
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942751"
---
# <a name="tvn_itemexpanding-notification-code"></a><span data-ttu-id="905ab-105">\_Code de notification TVN ITEMEXPANDING</span><span class="sxs-lookup"><span data-stu-id="905ab-105">TVN\_ITEMEXPANDING notification code</span></span>

<span data-ttu-id="905ab-106">Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent est sur le point d’être développée ou réduite.</span><span class="sxs-lookup"><span data-stu-id="905ab-106">Notifies a tree-view control's parent window that a parent item's list of child items is about to expand or collapse.</span></span> <span data-ttu-id="905ab-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="905ab-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="905ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="905ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="905ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="905ab-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="905ab-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="905ab-111">Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément parent dans les membres **hitem**, **State** et **lParam** .</span><span class="sxs-lookup"><span data-stu-id="905ab-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="905ab-112">Le membre d' **action** indique si la liste doit être développée ou réduite.</span><span class="sxs-lookup"><span data-stu-id="905ab-112">The **action** member indicates whether the list is to expand or collapse.</span></span> <span data-ttu-id="905ab-113">Pour obtenir la liste des valeurs possibles, consultez la description du message de [**\_ développement TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="905ab-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="905ab-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="905ab-114">Return value</span></span>

<span data-ttu-id="905ab-115">Retourne la **valeur true** pour empêcher le développement ou la réduction de la liste.</span><span class="sxs-lookup"><span data-stu-id="905ab-115">Returns **TRUE** to prevent the list from expanding or collapsing.</span></span>

## <a name="requirements"></a><span data-ttu-id="905ab-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="905ab-116">Requirements</span></span>



| <span data-ttu-id="905ab-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="905ab-117">Requirement</span></span> | <span data-ttu-id="905ab-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="905ab-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="905ab-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="905ab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="905ab-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="905ab-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="905ab-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="905ab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="905ab-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="905ab-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="905ab-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="905ab-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="905ab-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="905ab-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="905ab-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="905ab-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="905ab-126">**TVN \_ ITEMEXPANDINGW** (Unicode) et **TVN \_ ITEMEXPANDINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="905ab-126">**TVN\_ITEMEXPANDINGW** (Unicode) and **TVN\_ITEMEXPANDINGA** (ANSI)</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="905ab-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="905ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905ab-128">TVN \_ ITEMEXPANDED</span><span class="sxs-lookup"><span data-stu-id="905ab-128">TVN\_ITEMEXPANDED</span></span>](tvn-itemexpanded.md)
</dt> </dl>

 

 





