---
title: LBN_SETFOCUS le code de notification (winuser. h)
description: Indique à l’application que la zone de liste a reçu le focus clavier. La fenêtre parente de la zone de liste reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: d9e5e035-98a5-4ece-ba40-6d341c101859
keywords:
- Contrôles Windows de code de notification LBN_SETFOCUS
topic_type:
- apiref
api_name:
- LBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e56043982cec6606f7c78d3469ab2583951f88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843610"
---
# <a name="lbn_setfocus-notification-code"></a><span data-ttu-id="b0b97-105">\_Code de notification LBN SetFocus</span><span class="sxs-lookup"><span data-stu-id="b0b97-105">LBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="b0b97-106">Indique à l’application que la zone de liste a reçu le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="b0b97-106">Notifies the application that the list box has received the keyboard focus.</span></span> <span data-ttu-id="b0b97-107">La fenêtre parente de la zone de liste reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b0b97-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b0b97-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0b97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b97-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0b97-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b97-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="b0b97-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="b0b97-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="b0b97-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b0b97-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0b97-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b97-113">Handle vers la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="b0b97-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0b97-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0b97-114">Requirements</span></span>



| <span data-ttu-id="b0b97-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0b97-115">Requirement</span></span> | <span data-ttu-id="b0b97-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b97-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b97-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0b97-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b97-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0b97-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b0b97-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0b97-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b97-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0b97-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b0b97-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0b97-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b97-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0b97-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b97-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0b97-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0b97-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b0b97-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0b97-125">LBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="b0b97-125">LBN\_KILLFOCUS</span></span>](lbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="b0b97-126">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="b0b97-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="b0b97-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b0b97-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b0b97-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b0b97-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b0b97-129">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="b0b97-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

