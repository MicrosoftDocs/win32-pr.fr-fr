---
title: CBN_ERRSPACE le code de notification (winuser. h)
description: Envoyé lorsqu’une zone de liste déroulante ne peut pas allouer suffisamment de mémoire pour répondre à une demande spécifique. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: c1c19c40-fc88-47d0-9676-7a267a48ae98
keywords:
- Contrôles Windows de code de notification CBN_ERRSPACE
topic_type:
- apiref
api_name:
- CBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74e46e4435a03a0233ce6591d3c36cefb4d880a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106282"
---
# <a name="cbn_errspace-notification-code"></a><span data-ttu-id="c0460-105">\_Code de notification CBN ERRSPACE</span><span class="sxs-lookup"><span data-stu-id="c0460-105">CBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="c0460-106">Envoyé lorsqu’une zone de liste déroulante ne peut pas allouer suffisamment de mémoire pour répondre à une demande spécifique.</span><span class="sxs-lookup"><span data-stu-id="c0460-106">Sent when a combo box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="c0460-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c0460-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c0460-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0460-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0460-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0460-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0460-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c0460-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="c0460-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="c0460-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c0460-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0460-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0460-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c0460-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0460-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0460-114">Requirements</span></span>



| <span data-ttu-id="c0460-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0460-115">Requirement</span></span> | <span data-ttu-id="c0460-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0460-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0460-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0460-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0460-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0460-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0460-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0460-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0460-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0460-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c0460-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0460-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0460-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0460-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0460-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0460-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0460-124">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="c0460-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c0460-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0460-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c0460-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0460-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c0460-127">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="c0460-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

