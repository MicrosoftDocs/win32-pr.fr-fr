---
title: TCN_SELCHANGE le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que l’onglet actuellement sélectionné a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- Contrôles Windows de code de notification TCN_SELCHANGE
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739861"
---
# <a name="tcn_selchange-notification-code"></a><span data-ttu-id="c3545-105">\_Code de notification TCN selChange</span><span class="sxs-lookup"><span data-stu-id="c3545-105">TCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="c3545-106">Avertit une fenêtre parente d’un contrôle onglet que l’onglet actuellement sélectionné a changé.</span><span class="sxs-lookup"><span data-stu-id="c3545-106">Notifies a tab control's parent window that the currently selected tab has changed.</span></span> <span data-ttu-id="c3545-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c3545-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c3545-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3545-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3545-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3545-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3545-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="c3545-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3545-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3545-111">Return value</span></span>

<span data-ttu-id="c3545-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c3545-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3545-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c3545-113">Remarks</span></span>

<span data-ttu-id="c3545-114">Pour déterminer l’onglet actuellement sélectionné, utilisez la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="c3545-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3545-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3545-115">Requirements</span></span>



| <span data-ttu-id="c3545-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3545-116">Requirement</span></span> | <span data-ttu-id="c3545-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3545-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3545-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3545-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3545-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3545-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3545-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3545-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3545-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3545-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3545-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3545-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3545-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3545-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3545-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3545-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3545-125">TCN \_ SELCHANGING</span><span class="sxs-lookup"><span data-stu-id="c3545-125">TCN\_SELCHANGING</span></span>](tcn-selchanging.md)
</dt> </dl>

 

 





