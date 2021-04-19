---
title: CBN_KILLFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’une zone de liste déroulante perd le focus clavier. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 0118a2ff-9811-4bf1-b3f6-1d00ca5c8dbe
keywords:
- Contrôles Windows de code de notification CBN_KILLFOCUS
topic_type:
- apiref
api_name:
- CBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e266824bf8bcdac1fb901d40ca2b15406fc79660
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515089"
---
# <a name="cbn_killfocus-notification-code"></a><span data-ttu-id="0427d-105">\_Code de notification CBN KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="0427d-105">CBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="0427d-106">Envoyé lorsqu’une zone de liste déroulante perd le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="0427d-106">Sent when a combo box loses the keyboard focus.</span></span> <span data-ttu-id="0427d-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0427d-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0427d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0427d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0427d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0427d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0427d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0427d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="0427d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="0427d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0427d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0427d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0427d-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0427d-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0427d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0427d-114">Requirements</span></span>



| <span data-ttu-id="0427d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0427d-115">Requirement</span></span> | <span data-ttu-id="0427d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0427d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0427d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0427d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0427d-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0427d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0427d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0427d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0427d-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0427d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0427d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0427d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0427d-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0427d-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0427d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0427d-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="0427d-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0427d-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0427d-125">CBN \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="0427d-125">CBN\_SETFOCUS</span></span>](cbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="0427d-126">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="0427d-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0427d-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0427d-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0427d-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0427d-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0427d-129">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="0427d-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

