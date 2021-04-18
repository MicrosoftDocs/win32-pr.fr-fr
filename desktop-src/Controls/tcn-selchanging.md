---
title: TCN_SELCHANGING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que l’onglet actuellement sélectionné va être modifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- Contrôles Windows de code de notification TCN_SELCHANGING
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540767"
---
# <a name="tcn_selchanging-notification-code"></a><span data-ttu-id="513db-105">\_Code de notification TCN SELCHANGING</span><span class="sxs-lookup"><span data-stu-id="513db-105">TCN\_SELCHANGING notification code</span></span>

<span data-ttu-id="513db-106">Avertit une fenêtre parente d’un contrôle onglet que l’onglet actuellement sélectionné va être modifié.</span><span class="sxs-lookup"><span data-stu-id="513db-106">Notifies a tab control's parent window that the currently selected tab is about to change.</span></span> <span data-ttu-id="513db-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="513db-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="513db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="513db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="513db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="513db-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="513db-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="513db-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="513db-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="513db-111">Return value</span></span>

<span data-ttu-id="513db-112">Retourne la **valeur true** pour empêcher la modification de la sélection ou **false** pour permettre la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="513db-112">Returns **TRUE** to prevent the selection from changing, or **FALSE** to allow the selection to change.</span></span>

## <a name="remarks"></a><span data-ttu-id="513db-113">Notes</span><span class="sxs-lookup"><span data-stu-id="513db-113">Remarks</span></span>

<span data-ttu-id="513db-114">Pour déterminer l’onglet actuellement sélectionné, utilisez la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="513db-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="513db-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="513db-115">Requirements</span></span>



| <span data-ttu-id="513db-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="513db-116">Requirement</span></span> | <span data-ttu-id="513db-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="513db-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="513db-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="513db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="513db-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="513db-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="513db-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="513db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="513db-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="513db-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="513db-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="513db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="513db-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="513db-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="513db-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="513db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513db-125">TCN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="513db-125">TCN\_SELCHANGE</span></span>](tcn-selchange.md)
</dt> </dl>

 

 





