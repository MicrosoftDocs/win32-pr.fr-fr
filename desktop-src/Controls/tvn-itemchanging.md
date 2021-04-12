---
title: TVN_ITEMCHANGING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément sont sur le point de changer. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- Contrôles Windows de code de notification TVN_ITEMCHANGING
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508606"
---
# <a name="tvn_itemchanging-notification-code"></a><span data-ttu-id="81bd7-105">\_Code de notification TVN ITEMCHANGING</span><span class="sxs-lookup"><span data-stu-id="81bd7-105">TVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="81bd7-106">Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément sont sur le point de changer.</span><span class="sxs-lookup"><span data-stu-id="81bd7-106">Notifies a tree-view control's parent window that item attributes are about to change.</span></span> <span data-ttu-id="81bd7-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="81bd7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="81bd7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81bd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81bd7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81bd7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81bd7-110">Pointeur vers une structure [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) décrivant l’élément qui change.</span><span class="sxs-lookup"><span data-stu-id="81bd7-110">Pointer to an [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that is changing.</span></span> <span data-ttu-id="81bd7-111">Le membre **uChanged** est défini sur l' \_ État TVIF.</span><span class="sxs-lookup"><span data-stu-id="81bd7-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81bd7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81bd7-112">Return value</span></span>

<span data-ttu-id="81bd7-113">Retourne **false** pour accepter la modification, ou **true** pour empêcher la modification.</span><span class="sxs-lookup"><span data-stu-id="81bd7-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="81bd7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81bd7-114">Requirements</span></span>



| <span data-ttu-id="81bd7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81bd7-115">Requirement</span></span> | <span data-ttu-id="81bd7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="81bd7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81bd7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81bd7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81bd7-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81bd7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81bd7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81bd7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81bd7-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81bd7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81bd7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="81bd7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81bd7-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81bd7-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="81bd7-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="81bd7-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="81bd7-124">**TVN \_ ITEMCHANGINGW** (Unicode) et **TVN \_ ITEMCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="81bd7-124">**TVN\_ITEMCHANGINGW** (Unicode) and **TVN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="81bd7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81bd7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bd7-126">TVN \_ ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="81bd7-126">TVN\_ITEMCHANGED</span></span>](tvn-itemchanged.md)
</dt> </dl>

 

 





