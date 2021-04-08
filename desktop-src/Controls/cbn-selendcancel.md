---
title: CBN_SELENDCANCEL le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur sélectionne un élément, mais sélectionne un autre contrôle ou ferme la boîte de dialogue. Elle indique que la sélection initiale de l’utilisateur doit être ignorée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- Contrôles Windows de code de notification CBN_SELENDCANCEL
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743045"
---
# <a name="cbn_selendcancel-notification-code"></a><span data-ttu-id="e7e71-106">\_Code de notification CBN SELENDCANCEL</span><span class="sxs-lookup"><span data-stu-id="e7e71-106">CBN\_SELENDCANCEL notification code</span></span>

<span data-ttu-id="e7e71-107">Envoyé lorsque l’utilisateur sélectionne un élément, mais sélectionne un autre contrôle ou ferme la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e7e71-107">Sent when the user selects an item, but then selects another control or closes the dialog box.</span></span> <span data-ttu-id="e7e71-108">Elle indique que la sélection initiale de l’utilisateur doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="e7e71-108">It indicates the user's initial selection is to be ignored.</span></span> <span data-ttu-id="e7e71-109">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e7e71-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e7e71-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7e71-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e71-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7e71-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7e71-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e7e71-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="e7e71-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="e7e71-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e7e71-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7e71-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7e71-115">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e7e71-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7e71-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e7e71-116">Remarks</span></span>

<span data-ttu-id="e7e71-117">Dans une zone de liste modifiable avec le style [**CBS \_ simple**](combo-box-styles.md) , le \_ Code de notification CBN SELENDCANCEL n’est pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="e7e71-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDCANCEL notification code is not sent.</span></span> <span data-ttu-id="e7e71-118">Le code de notification [CBN \_ SELENDOK](cbn-selendok.md) est envoyé immédiatement avant chaque code de notification [CBN \_ selChange](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e71-118">The [CBN\_SELENDOK](cbn-selendok.md) notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e71-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7e71-119">Requirements</span></span>



| <span data-ttu-id="e7e71-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7e71-120">Requirement</span></span> | <span data-ttu-id="e7e71-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7e71-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e71-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7e71-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e71-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7e71-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7e71-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7e71-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e71-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7e71-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7e71-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7e71-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7e71-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7e71-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e71-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7e71-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7e71-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e7e71-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e7e71-130">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="e7e71-130">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="e7e71-131">CBN \_ SELENDOK</span><span class="sxs-lookup"><span data-stu-id="e7e71-131">CBN\_SELENDOK</span></span>](cbn-selendok.md)
</dt> <dt>

<span data-ttu-id="e7e71-132">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="e7e71-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e7e71-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7e71-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e7e71-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7e71-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e7e71-135">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="e7e71-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

