---
title: LBN_SELCHANGE le code de notification (winuser. h)
description: Indique à l’application que la sélection dans une zone de liste a été modifiée suite à une entrée de l’utilisateur. La fenêtre parente de la zone de liste reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- Contrôles Windows de code de notification LBN_SELCHANGE
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741572"
---
# <a name="lbn_selchange-notification-code"></a><span data-ttu-id="e54d5-105">\_Code de notification LBN selChange</span><span class="sxs-lookup"><span data-stu-id="e54d5-105">LBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="e54d5-106">Indique à l’application que la sélection dans une zone de liste a été modifiée suite à une entrée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e54d5-106">Notifies the application that the selection in a list box has changed as a result of user input.</span></span> <span data-ttu-id="e54d5-107">La fenêtre parente de la zone de liste reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e54d5-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e54d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e54d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e54d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e54d5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e54d5-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="e54d5-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="e54d5-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="e54d5-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e54d5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e54d5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e54d5-113">Handle vers la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="e54d5-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e54d5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e54d5-114">Remarks</span></span>

<span data-ttu-id="e54d5-115">Ce code de notification est envoyé uniquement par une zone de liste dont le style de [**\_ notification est lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e54d5-115">This notification code is sent only by a list box that has the [**LBS\_NOTIFY**](list-box-styles.md) style.</span></span>

<span data-ttu-id="e54d5-116">Ce code de notification n’est pas envoyé si le message [**lb \_ SETSEL**](lb-setsel.md), [**lb \_ SETCURSEL**](lb-setcursel.md), [**lb \_ SELECTSTRING**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) ou [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) modifie la sélection.</span><span class="sxs-lookup"><span data-stu-id="e54d5-116">This notification code is not sent if the [**LB\_SETSEL**](lb-setsel.md), [**LB\_SETCURSEL**](lb-setcursel.md), [**LB\_SELECTSTRING**](lb-selectstring.md), [**LB\_SELITEMRANGE**](lb-selitemrange.md) or [**LB\_SELITEMRANGEEX**](lb-selitemrangeex.md) message changes the selection.</span></span>

<span data-ttu-id="e54d5-117">Pour une zone de liste à sélection multiple, le \_ Code de notification LBN selChange est envoyé chaque fois que l’utilisateur appuie sur une touche de direction, même si la sélection ne change pas.</span><span class="sxs-lookup"><span data-stu-id="e54d5-117">For a multiple-selection list box, the LBN\_SELCHANGE notification code is sent whenever the user presses an arrow key, even if the selection does not change.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54d5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e54d5-118">Requirements</span></span>



| <span data-ttu-id="e54d5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e54d5-119">Requirement</span></span> | <span data-ttu-id="e54d5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e54d5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e54d5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e54d5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e54d5-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e54d5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e54d5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e54d5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e54d5-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e54d5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e54d5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e54d5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e54d5-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e54d5-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e54d5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e54d5-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e54d5-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e54d5-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e54d5-129">**\_SETCURSEL lb**</span><span class="sxs-lookup"><span data-stu-id="e54d5-129">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="e54d5-130">LBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="e54d5-130">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="e54d5-131">LBN \_ SELCANCEL</span><span class="sxs-lookup"><span data-stu-id="e54d5-131">LBN\_SELCANCEL</span></span>](lbn-selcancel.md)
</dt> <dt>

<span data-ttu-id="e54d5-132">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="e54d5-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e54d5-133">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="e54d5-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

