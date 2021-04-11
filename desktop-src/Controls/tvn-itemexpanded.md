---
title: TVN_ITEMEXPANDED le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent a été développée ou réduite. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- Contrôles Windows de code de notification TVN_ITEMEXPANDED
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105946"
---
# <a name="tvn_itemexpanded-notification-code"></a><span data-ttu-id="56c13-105">\_Code de notification TVN ITEMEXPANDED</span><span class="sxs-lookup"><span data-stu-id="56c13-105">TVN\_ITEMEXPANDED notification code</span></span>

<span data-ttu-id="56c13-106">Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent a été développée ou réduite.</span><span class="sxs-lookup"><span data-stu-id="56c13-106">Notifies a tree-view control's parent window that a parent item's list of child items has expanded or collapsed.</span></span> <span data-ttu-id="56c13-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="56c13-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="56c13-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56c13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56c13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56c13-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="56c13-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="56c13-111">Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément parent dans les membres **hitem**, **State** et **lParam** .</span><span class="sxs-lookup"><span data-stu-id="56c13-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="56c13-112">Le membre d' **action** indique si la liste a été développée ou réduite.</span><span class="sxs-lookup"><span data-stu-id="56c13-112">The **action** member indicates whether the list expanded or collapsed.</span></span> <span data-ttu-id="56c13-113">Pour obtenir la liste des valeurs possibles, consultez la description du message de [**\_ développement TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="56c13-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c13-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56c13-114">Return value</span></span>

<span data-ttu-id="56c13-115">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="56c13-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c13-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56c13-116">Requirements</span></span>



| <span data-ttu-id="56c13-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56c13-117">Requirement</span></span> | <span data-ttu-id="56c13-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="56c13-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56c13-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56c13-119">Minimum supported client</span></span><br/> | <span data-ttu-id="56c13-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56c13-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56c13-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56c13-121">Minimum supported server</span></span><br/> | <span data-ttu-id="56c13-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56c13-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56c13-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="56c13-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56c13-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56c13-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="56c13-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="56c13-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="56c13-126">**TVN \_ ITEMEXPANDEDW** (Unicode) et **TVN \_ ITEMEXPANDEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56c13-126">**TVN\_ITEMEXPANDEDW** (Unicode) and **TVN\_ITEMEXPANDEDA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="56c13-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56c13-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c13-128">TVN \_ ITEMEXPANDING</span><span class="sxs-lookup"><span data-stu-id="56c13-128">TVN\_ITEMEXPANDING</span></span>](tvn-itemexpanding.md)
</dt> </dl>

 

 





