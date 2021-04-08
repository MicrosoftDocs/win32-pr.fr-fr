---
title: TVN_ITEMCHANGED le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément ont été modifiés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- Contrôles Windows de code de notification TVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843653"
---
# <a name="tvn_itemchanged-notification-code"></a><span data-ttu-id="5e2ee-105">\_Code de notification TVN ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="5e2ee-105">TVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="5e2ee-106">Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-106">Notifies a tree-view control's parent window that item attributes have changed.</span></span> <span data-ttu-id="5e2ee-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e2ee-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5e2ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e2ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2ee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e2ee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e2ee-110">Pointeur vers une structure [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) décrivant l’élément qui a changé.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-110">Pointer to a [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that changed.</span></span> <span data-ttu-id="5e2ee-111">Le membre **uChanged** est défini sur l' \_ État TVIF.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2ee-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e2ee-112">Return value</span></span>

<span data-ttu-id="5e2ee-113">Retourne **false** pour accepter la modification, ou **true** pour empêcher la modification.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2ee-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e2ee-114">Requirements</span></span>



| <span data-ttu-id="5e2ee-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e2ee-115">Requirement</span></span> | <span data-ttu-id="5e2ee-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e2ee-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2ee-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e2ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2ee-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e2ee-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e2ee-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e2ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2ee-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e2ee-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e2ee-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e2ee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e2ee-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e2ee-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5e2ee-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="5e2ee-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5e2ee-124">**TVN \_ ITEMCHANGEDW** (Unicode) et **TVN \_ ITEMCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5e2ee-124">**TVN\_ITEMCHANGEDW** (Unicode) and **TVN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5e2ee-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e2ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2ee-126">TVN \_ ITEMCHANGING</span><span class="sxs-lookup"><span data-stu-id="5e2ee-126">TVN\_ITEMCHANGING</span></span>](tvn-itemchanging.md)
</dt> </dl>

 

 





