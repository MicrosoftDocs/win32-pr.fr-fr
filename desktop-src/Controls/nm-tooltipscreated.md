---
title: NM_TOOLTIPSCREATED le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle a créé un contrôle ToolTip. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- Contrôles Windows de code de notification NM_TOOLTIPSCREATED
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032687"
---
# <a name="nm_tooltipscreated-notification-code"></a><span data-ttu-id="f798a-105">\_Code de notification TOOLTIPSCREATED nm</span><span class="sxs-lookup"><span data-stu-id="f798a-105">NM\_TOOLTIPSCREATED notification code</span></span>

<span data-ttu-id="f798a-106">Avertit la fenêtre parente d’un contrôle que le contrôle a créé un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="f798a-106">Notifies a control's parent window that the control has created a tooltip control.</span></span> <span data-ttu-id="f798a-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f798a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f798a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f798a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f798a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f798a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f798a-110">Pointeur vers une structure [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="f798a-110">A pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f798a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f798a-111">Return value</span></span>

<span data-ttu-id="f798a-112">Sauf spécification contraire, le contrôle ignore la valeur de retour de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="f798a-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f798a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f798a-113">Requirements</span></span>



| <span data-ttu-id="f798a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f798a-114">Requirement</span></span> | <span data-ttu-id="f798a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f798a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f798a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f798a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f798a-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f798a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f798a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f798a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f798a-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f798a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f798a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f798a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f798a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f798a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





