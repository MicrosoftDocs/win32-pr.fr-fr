---
title: TVN_SELCHANGING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est sur le point de passer d’un élément à un autre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- Contrôles Windows de code de notification TVN_SELCHANGING
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032748"
---
# <a name="tvn_selchanging-notification-code"></a><span data-ttu-id="21bdf-105">\_Code de notification TVN SELCHANGING</span><span class="sxs-lookup"><span data-stu-id="21bdf-105">TVN\_SELCHANGING notification code</span></span>

<span data-ttu-id="21bdf-106">Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est sur le point de passer d’un élément à un autre.</span><span class="sxs-lookup"><span data-stu-id="21bdf-106">Notifies a tree-view control's parent window that the selection is about to change from one item to another.</span></span> <span data-ttu-id="21bdf-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="21bdf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="21bdf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21bdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21bdf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21bdf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21bdf-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="21bdf-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="21bdf-111">Les membres **itemOld** et **itemNew** contiennent des informations valides sur l’élément actuellement sélectionné et sur l’élément nouvellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="21bdf-111">The **itemOld** and **itemNew** members contain valid information about the currently selected item and the newly selected item.</span></span> <span data-ttu-id="21bdf-112">Le membre d' **action** indique si une action de la souris ou du clavier est à l’origine de la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="21bdf-112">The **action** member indicates whether a mouse or keyboard action is causing the selection to change.</span></span> <span data-ttu-id="21bdf-113">Pour obtenir la liste des valeurs possibles, consultez la description du code de notification [TVN \_ SELCHANGED](tvn-selchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="21bdf-113">For a list of possible values, see the description of the [TVN\_SELCHANGED](tvn-selchanged.md) notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21bdf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21bdf-114">Return value</span></span>

<span data-ttu-id="21bdf-115">Retourne la **valeur true** pour empêcher la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="21bdf-115">Returns **TRUE** to prevent the selection from changing.</span></span>

## <a name="remarks"></a><span data-ttu-id="21bdf-116">Notes</span><span class="sxs-lookup"><span data-stu-id="21bdf-116">Remarks</span></span>

<span data-ttu-id="21bdf-117">Lors de la réponse à ce code de notification, les applications ne doivent pas supprimer les éléments qui obtiennent ou perdent la sélection.</span><span class="sxs-lookup"><span data-stu-id="21bdf-117">When responding to this notification code, applications should not delete the items that are gaining or losing the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="21bdf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21bdf-118">Requirements</span></span>



| <span data-ttu-id="21bdf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21bdf-119">Requirement</span></span> | <span data-ttu-id="21bdf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="21bdf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21bdf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21bdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21bdf-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21bdf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21bdf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21bdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21bdf-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21bdf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21bdf-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="21bdf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="21bdf-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="21bdf-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="21bdf-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="21bdf-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="21bdf-128">**TVN \_ SELCHANGINGW** (Unicode) et **TVN \_ SELCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="21bdf-128">**TVN\_SELCHANGINGW** (Unicode) and **TVN\_SELCHANGINGA** (ANSI)</span></span><br/>           |



 

 





