---
title: LVN_ITEMCHANGING le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un élément est en modification. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- Contrôles Windows de code de notification LVN_ITEMCHANGING
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942920"
---
# <a name="lvn_itemchanging-notification-code"></a><span data-ttu-id="6e74f-105">\_Code de notification LVN ITEMCHANGING</span><span class="sxs-lookup"><span data-stu-id="6e74f-105">LVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="6e74f-106">Avertit la fenêtre parente d’un contrôle List-View qu’un élément est en modification.</span><span class="sxs-lookup"><span data-stu-id="6e74f-106">Notifies a list-view control's parent window that an item is changing.</span></span> <span data-ttu-id="6e74f-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6e74f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6e74f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e74f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e74f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e74f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e74f-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui identifie l’élément et spécifie les attributs modifiés.</span><span class="sxs-lookup"><span data-stu-id="6e74f-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes are changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e74f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e74f-111">Return value</span></span>

<span data-ttu-id="6e74f-112">Retourne la **valeur true** pour empêcher la modification, ou **false** pour autoriser la modification.</span><span class="sxs-lookup"><span data-stu-id="6e74f-112">Returns **TRUE** to prevent the change, or **FALSE** to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e74f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6e74f-113">Remarks</span></span>

<span data-ttu-id="6e74f-114">Si le contrôle List-View a le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) , les \_ codes de notification LVN ITEMCHANGING ne sont pas envoyés.</span><span class="sxs-lookup"><span data-stu-id="6e74f-114">If the list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, LVN\_ITEMCHANGING notification codes are not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e74f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e74f-115">Requirements</span></span>



| <span data-ttu-id="6e74f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e74f-116">Requirement</span></span> | <span data-ttu-id="6e74f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e74f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e74f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e74f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e74f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e74f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e74f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e74f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e74f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e74f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e74f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e74f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e74f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e74f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





