---
title: LBN_ERRSPACE le code de notification (winuser. h)
description: Indique à l’application que la zone de liste ne peut pas allouer suffisamment de mémoire pour répondre à une demande spécifique. La fenêtre parente de la zone de liste reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- Contrôles Windows de code de notification LBN_ERRSPACE
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200569"
---
# <a name="lbn_errspace-notification-code"></a><span data-ttu-id="56833-105">\_Code de notification LBN ERRSPACE</span><span class="sxs-lookup"><span data-stu-id="56833-105">LBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="56833-106">Indique à l’application que la zone de liste ne peut pas allouer suffisamment de mémoire pour répondre à une demande spécifique.</span><span class="sxs-lookup"><span data-stu-id="56833-106">Notifies the application that the list box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="56833-107">La fenêtre parente de la zone de liste reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="56833-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="56833-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56833-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56833-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56833-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56833-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="56833-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="56833-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="56833-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="56833-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56833-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56833-113">Handle vers la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="56833-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56833-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56833-114">Requirements</span></span>



| <span data-ttu-id="56833-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56833-115">Requirement</span></span> | <span data-ttu-id="56833-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="56833-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56833-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56833-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56833-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56833-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="56833-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56833-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56833-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56833-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56833-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="56833-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="56833-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56833-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56833-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56833-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="56833-124">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="56833-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="56833-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56833-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="56833-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56833-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="56833-127">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="56833-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

