---
title: NM_HOVER le code de notification (commctrl. h)
description: Envoyé par un contrôle lorsque la souris pointe sur un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- Contrôles Windows de code de notification NM_HOVER
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739925"
---
# <a name="nm_hover-notification-code"></a><span data-ttu-id="26357-105">\_Code de notification de pointage nm</span><span class="sxs-lookup"><span data-stu-id="26357-105">NM\_HOVER notification code</span></span>

<span data-ttu-id="26357-106">Envoyé par un contrôle lorsque la souris pointe sur un élément.</span><span class="sxs-lookup"><span data-stu-id="26357-106">Sent by a control when the mouse hovers over an item.</span></span> <span data-ttu-id="26357-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="26357-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="26357-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26357-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26357-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26357-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26357-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="26357-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26357-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26357-111">Return value</span></span>

<span data-ttu-id="26357-112">Sauf spécification contraire, retourne zéro pour permettre au contrôle de traiter le pointage normalement, ou une valeur différente de zéro pour empêcher le pointage d’être traité.</span><span class="sxs-lookup"><span data-stu-id="26357-112">Unless otherwise specified, return zero to allow the control to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="26357-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26357-113">Requirements</span></span>



| <span data-ttu-id="26357-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26357-114">Requirement</span></span> | <span data-ttu-id="26357-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="26357-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26357-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26357-116">Minimum supported client</span></span><br/> | <span data-ttu-id="26357-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26357-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26357-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26357-118">Minimum supported server</span></span><br/> | <span data-ttu-id="26357-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26357-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26357-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="26357-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="26357-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26357-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





