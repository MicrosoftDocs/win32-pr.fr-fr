---
title: LBN_DBLCLK le code de notification (winuser. h)
description: Indique à l’application que l’utilisateur a double-cliqué sur un élément dans une zone de liste. La fenêtre parente de la zone de liste reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- Contrôles Windows de code de notification LBN_DBLCLK
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60623aafb287f2006d9e27da49d0df34c05b05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743012"
---
# <a name="lbn_dblclk-notification-code"></a><span data-ttu-id="d8b92-105">\_Code de notification LBN DBLCLK</span><span class="sxs-lookup"><span data-stu-id="d8b92-105">LBN\_DBLCLK notification code</span></span>

<span data-ttu-id="d8b92-106">Indique à l’application que l’utilisateur a double-cliqué sur un élément dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="d8b92-106">Notifies the application that the user has double-clicked an item in a list box.</span></span> <span data-ttu-id="d8b92-107">La fenêtre parente de la zone de liste reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d8b92-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d8b92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8b92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b92-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8b92-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8b92-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="d8b92-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="d8b92-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="d8b92-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d8b92-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8b92-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8b92-113">Handle vers la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="d8b92-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8b92-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d8b92-114">Remarks</span></span>

<span data-ttu-id="d8b92-115">Ce code de notification est envoyé uniquement par une zone de liste dont le style de notification est L [**BS \_**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b92-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b92-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8b92-116">Requirements</span></span>



| <span data-ttu-id="d8b92-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8b92-117">Requirement</span></span> | <span data-ttu-id="d8b92-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8b92-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b92-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b92-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b92-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8b92-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8b92-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b92-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b92-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8b92-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d8b92-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8b92-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b92-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8b92-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b92-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b92-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8b92-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d8b92-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d8b92-127">LBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="d8b92-127">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="d8b92-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d8b92-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d8b92-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8b92-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d8b92-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8b92-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d8b92-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="d8b92-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

