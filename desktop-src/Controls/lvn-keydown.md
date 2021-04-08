---
title: LVN_KEYDOWN le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’une touche a été enfoncée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- Contrôles Windows de code de notification LVN_KEYDOWN
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942919"
---
# <a name="lvn_keydown-notification-code"></a><span data-ttu-id="387ae-105">Code de notification KeyOut LVN \_</span><span class="sxs-lookup"><span data-stu-id="387ae-105">LVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="387ae-106">Avertit une fenêtre parente d’un contrôle List-View qu’une touche a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="387ae-106">Notifies a list-view control's parent window that a key has been pressed.</span></span> <span data-ttu-id="387ae-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="387ae-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="387ae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="387ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="387ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="387ae-110">Pointeur vers une structure [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="387ae-110">Pointer to an [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="387ae-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="387ae-111">Return value</span></span>

<span data-ttu-id="387ae-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="387ae-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="387ae-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="387ae-113">Requirements</span></span>



| <span data-ttu-id="387ae-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="387ae-114">Requirement</span></span> | <span data-ttu-id="387ae-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="387ae-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="387ae-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="387ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="387ae-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="387ae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="387ae-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="387ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="387ae-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="387ae-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="387ae-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="387ae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="387ae-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="387ae-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





