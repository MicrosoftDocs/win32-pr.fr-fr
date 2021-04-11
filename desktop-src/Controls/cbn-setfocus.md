---
title: CBN_SETFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’une zone de liste déroulante reçoit le focus clavier. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 8072edc6-aedc-4daf-80df-d3acd82fcffa
keywords:
- Contrôles Windows de code de notification CBN_SETFOCUS
topic_type:
- apiref
api_name:
- CBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885bbaebac0a79fc600cbcc2b7864cbdfd19ea93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317529"
---
# <a name="cbn_setfocus-notification-code"></a><span data-ttu-id="ca817-105">\_Code de notification CBN SetFocus</span><span class="sxs-lookup"><span data-stu-id="ca817-105">CBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="ca817-106">Envoyé lorsqu’une zone de liste déroulante reçoit le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="ca817-106">Sent when a combo box receives the keyboard focus.</span></span> <span data-ttu-id="ca817-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="ca817-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ca817-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca817-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca817-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca817-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca817-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ca817-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="ca817-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="ca817-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ca817-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca817-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca817-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ca817-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca817-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca817-114">Requirements</span></span>



| <span data-ttu-id="ca817-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca817-115">Requirement</span></span> | <span data-ttu-id="ca817-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca817-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca817-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca817-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ca817-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca817-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ca817-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca817-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ca817-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca817-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ca817-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca817-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca817-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca817-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca817-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca817-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca817-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ca817-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ca817-125">CBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="ca817-125">CBN\_KILLFOCUS</span></span>](cbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="ca817-126">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="ca817-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ca817-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca817-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ca817-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca817-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca817-129">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="ca817-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

