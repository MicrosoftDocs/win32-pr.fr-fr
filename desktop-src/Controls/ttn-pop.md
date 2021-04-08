---
title: TTN_POP le code de notification (commctrl. h)
description: Informe la fenêtre propriétaire qu’une info-bulle va être masquée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- Contrôles Windows de code de notification TTN_POP
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576aa382f571fb6ded7205d2df3b0abd938c704d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741445"
---
# <a name="ttn_pop-notification-code"></a><span data-ttu-id="d88de-105">\_Code de notification pop ttn</span><span class="sxs-lookup"><span data-stu-id="d88de-105">TTN\_POP notification code</span></span>

<span data-ttu-id="d88de-106">Informe la fenêtre propriétaire qu’une info-bulle va être masquée.</span><span class="sxs-lookup"><span data-stu-id="d88de-106">Notifies the owner window that a tooltip is about to be hidden.</span></span> <span data-ttu-id="d88de-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d88de-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d88de-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d88de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d88de-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d88de-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="d88de-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d88de-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d88de-111">Return value</span></span>

<span data-ttu-id="d88de-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="d88de-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88de-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d88de-113">Requirements</span></span>



| <span data-ttu-id="d88de-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d88de-114">Requirement</span></span> | <span data-ttu-id="d88de-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d88de-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d88de-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d88de-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d88de-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d88de-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d88de-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d88de-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d88de-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d88de-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d88de-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d88de-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88de-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d88de-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





