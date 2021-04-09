---
title: STN_DBLCLK le code de notification (winuser. h)
description: Le \_ Code de notification STN DBLCLK est envoyé lorsque l’utilisateur double-clique sur un contrôle statique avec le \_ style de notification SS. La fenêtre parente du contrôle reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- Contrôles Windows de code de notification STN_DBLCLK
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032561"
---
# <a name="stn_dblclk-notification-code"></a><span data-ttu-id="9d4c2-105">\_Code de notification STN DBLCLK</span><span class="sxs-lookup"><span data-stu-id="9d4c2-105">STN\_DBLCLK notification code</span></span>

<span data-ttu-id="9d4c2-106">Le \_ Code de notification STN DBLCLK est envoyé lorsque l’utilisateur double-clique sur un contrôle statique avec le style de [**\_ notification SS**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9d4c2-106">The STN\_DBLCLK notification code is sent when the user double-clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="9d4c2-107">La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="9d4c2-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9d4c2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d4c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d4c2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d4c2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d4c2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="9d4c2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="9d4c2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="9d4c2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9d4c2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d4c2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d4c2-113">Handle vers le contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="9d4c2-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d4c2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d4c2-114">Requirements</span></span>



| <span data-ttu-id="9d4c2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d4c2-115">Requirement</span></span> | <span data-ttu-id="9d4c2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d4c2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4c2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d4c2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d4c2-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d4c2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9d4c2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d4c2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d4c2-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d4c2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9d4c2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d4c2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d4c2-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d4c2-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d4c2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d4c2-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d4c2-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9d4c2-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9d4c2-125">STN \_ sur lequel l’utilisateur a cliqué</span><span class="sxs-lookup"><span data-stu-id="9d4c2-125">STN\_CLICKED</span></span>](stn-clicked.md)
</dt> <dt>

<span data-ttu-id="9d4c2-126">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9d4c2-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9d4c2-127">Contrôles statiques</span><span class="sxs-lookup"><span data-stu-id="9d4c2-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="9d4c2-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="9d4c2-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="9d4c2-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d4c2-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9d4c2-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d4c2-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9d4c2-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="9d4c2-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

