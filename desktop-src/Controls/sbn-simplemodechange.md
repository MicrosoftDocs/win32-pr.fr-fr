---
title: SBN_SIMPLEMODECHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle de barre d’État lorsque le mode simple change en raison d’un \_ message SB simple. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- Contrôles Windows de code de notification SBN_SIMPLEMODECHANGE
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509735"
---
# <a name="sbn_simplemodechange-notification-code"></a><span data-ttu-id="e25de-105">\_Code de notification SBN SIMPLEMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="e25de-105">SBN\_SIMPLEMODECHANGE notification code</span></span>

<span data-ttu-id="e25de-106">Envoyé par un contrôle de barre d’État lorsque le mode simple change en raison d’un message [**SB \_ simple**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="e25de-106">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="e25de-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e25de-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e25de-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e25de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e25de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e25de-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e25de-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="e25de-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e25de-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e25de-111">Return value</span></span>

<span data-ttu-id="e25de-112">La valeur de retour est ignorée par la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="e25de-112">The return value is ignored by the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="e25de-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e25de-113">Requirements</span></span>



| <span data-ttu-id="e25de-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e25de-114">Requirement</span></span> | <span data-ttu-id="e25de-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e25de-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e25de-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e25de-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e25de-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e25de-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e25de-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e25de-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e25de-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e25de-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e25de-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e25de-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e25de-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e25de-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





