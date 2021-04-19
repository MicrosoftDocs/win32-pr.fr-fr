---
title: CBN_SELENDOK le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur sélectionne un élément de liste, ou sélectionne un élément, puis ferme la liste. Elle indique que la sélection de l’utilisateur doit être traitée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- Contrôles Windows de code de notification CBN_SELENDOK
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510325"
---
# <a name="cbn_selendok-notification-code"></a><span data-ttu-id="6905e-106">\_Code de notification CBN SELENDOK</span><span class="sxs-lookup"><span data-stu-id="6905e-106">CBN\_SELENDOK notification code</span></span>

<span data-ttu-id="6905e-107">Envoyé lorsque l’utilisateur sélectionne un élément de liste, ou sélectionne un élément, puis ferme la liste.</span><span class="sxs-lookup"><span data-stu-id="6905e-107">Sent when the user selects a list item, or selects an item and then closes the list.</span></span> <span data-ttu-id="6905e-108">Elle indique que la sélection de l’utilisateur doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="6905e-108">It indicates that the user's selection is to be processed.</span></span> <span data-ttu-id="6905e-109">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6905e-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6905e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6905e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6905e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6905e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6905e-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6905e-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="6905e-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="6905e-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6905e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6905e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6905e-115">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6905e-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6905e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6905e-116">Remarks</span></span>

<span data-ttu-id="6905e-117">Dans une zone de liste modifiable avec le style [**CBS \_ simple**](combo-box-styles.md) , le \_ Code de notification CBN SELENDOK est envoyé immédiatement avant chaque code de notification [CBN \_ selChange](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="6905e-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDOK notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6905e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6905e-118">Requirements</span></span>



| <span data-ttu-id="6905e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6905e-119">Requirement</span></span> | <span data-ttu-id="6905e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6905e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6905e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6905e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6905e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6905e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6905e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6905e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6905e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6905e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6905e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6905e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6905e-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6905e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6905e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6905e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6905e-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6905e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6905e-129">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="6905e-129">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="6905e-130">CBN \_ SELENDCANCEL</span><span class="sxs-lookup"><span data-stu-id="6905e-130">CBN\_SELENDCANCEL</span></span>](cbn-selendcancel.md)
</dt> <dt>

<span data-ttu-id="6905e-131">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="6905e-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6905e-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6905e-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6905e-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6905e-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6905e-134">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="6905e-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

