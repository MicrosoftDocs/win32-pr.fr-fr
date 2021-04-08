---
title: TVN_SELCHANGED le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est passée d’un élément à l’autre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- Contrôles Windows de code de notification TVN_SELCHANGED
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844246"
---
# <a name="tvn_selchanged-notification-code"></a><span data-ttu-id="1987e-105">\_Code de notification TVN SELCHANGED</span><span class="sxs-lookup"><span data-stu-id="1987e-105">TVN\_SELCHANGED notification code</span></span>

<span data-ttu-id="1987e-106">Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est passée d’un élément à l’autre.</span><span class="sxs-lookup"><span data-stu-id="1987e-106">Notifies a tree-view control's parent window that the selection has changed from one item to another.</span></span> <span data-ttu-id="1987e-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1987e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="1987e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1987e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1987e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1987e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1987e-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="1987e-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="1987e-111">Les membres **itemOld** et **itemNew** de la structure **NMTREEVIEW** sont des structures [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contiennent des informations sur l’élément sélectionné précédemment et l’élément nouvellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1987e-111">The **itemOld** and **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item.</span></span> <span data-ttu-id="1987e-112">Seuls les membres **Mask**, **hitem**, **State** et **lParam** de ces structures sont valides.</span><span class="sxs-lookup"><span data-stu-id="1987e-112">Only the **mask**, **hItem**, **state**, and **lParam** members of these structures are valid.</span></span> <span data-ttu-id="1987e-113">Les membres **stateMask** des structures **TVITEM** spécifiées par **itemOld** et **itemNew** ne sont pas définis en entrée.</span><span class="sxs-lookup"><span data-stu-id="1987e-113">The **stateMask** members of the **TVITEM** structures specified by **itemOld** and **itemNew** are undefined on input.</span></span> <span data-ttu-id="1987e-114">Le membre **action** de la structure **NMTREEVIEW** indique le type d’action qui a entraîné la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="1987e-114">The **action** member of the **NMTREEVIEW** structure indicates the type of action that caused the selection to change.</span></span> <span data-ttu-id="1987e-115">Ce peut être l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1987e-115">It can be one of the following values:</span></span>



| <span data-ttu-id="1987e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1987e-116">Requirement</span></span> | <span data-ttu-id="1987e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1987e-117">Value</span></span> |
|-----------------|-------------------|
| <span data-ttu-id="1987e-118">TVC \_ BYKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="1987e-118">TVC\_BYKEYBOARD</span></span> | <span data-ttu-id="1987e-119">Par une séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="1987e-119">By a keystroke.</span></span>   |
| <span data-ttu-id="1987e-120">TVC \_ BYMOUSE</span><span class="sxs-lookup"><span data-stu-id="1987e-120">TVC\_BYMOUSE</span></span>    | <span data-ttu-id="1987e-121">Par un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="1987e-121">By a mouse click.</span></span> |
| <span data-ttu-id="1987e-122">TVC \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="1987e-122">TVC\_UNKNOWN</span></span>    | <span data-ttu-id="1987e-123">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="1987e-123">Unknown.</span></span>          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1987e-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1987e-124">Return value</span></span>

<span data-ttu-id="1987e-125">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1987e-125">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1987e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1987e-126">Requirements</span></span>



| <span data-ttu-id="1987e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1987e-127">Requirement</span></span> | <span data-ttu-id="1987e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1987e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1987e-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1987e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1987e-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1987e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1987e-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1987e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1987e-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1987e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1987e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="1987e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1987e-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1987e-134"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1987e-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1987e-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1987e-136">**TVN \_ SELCHANGEDW** (Unicode) et **TVN \_ SELCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1987e-136">**TVN\_SELCHANGEDW** (Unicode) and **TVN\_SELCHANGEDA** (ANSI)</span></span><br/>             |



 

 





