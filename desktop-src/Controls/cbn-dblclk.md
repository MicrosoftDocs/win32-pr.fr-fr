---
title: CBN_DBLCLK le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur double-clique sur une chaîne dans la zone de liste d’une zone de liste déroulante. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- Contrôles Windows de code de notification CBN_DBLCLK
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509951"
---
# <a name="cbn_dblclk-notification-code"></a><span data-ttu-id="f1d45-105">\_Code de notification CBN DBLCLK</span><span class="sxs-lookup"><span data-stu-id="f1d45-105">CBN\_DBLCLK notification code</span></span>

<span data-ttu-id="f1d45-106">Envoyé lorsque l’utilisateur double-clique sur une chaîne dans la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="f1d45-106">Sent when the user double-clicks a string in the list box of a combo box.</span></span> <span data-ttu-id="f1d45-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="f1d45-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f1d45-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1d45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1d45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1d45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1d45-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="f1d45-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="f1d45-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="f1d45-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f1d45-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1d45-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1d45-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="f1d45-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1d45-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f1d45-114">Remarks</span></span>

<span data-ttu-id="f1d45-115">Ce code de notification se produit uniquement pour une zone de liste modifiable avec le style [**CBS \_ simple**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f1d45-115">This notification code occurs only for a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="f1d45-116">Dans une zone de liste modifiable avec la [**\_ liste déroulante CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) , un double-clic ne peut pas se produire parce qu’un clic unique ferme la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="f1d45-116">In a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, a double-click cannot occur because a single click closes the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d45-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1d45-117">Requirements</span></span>



| <span data-ttu-id="f1d45-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1d45-118">Requirement</span></span> | <span data-ttu-id="f1d45-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d45-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d45-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1d45-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d45-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1d45-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1d45-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1d45-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d45-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1d45-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1d45-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1d45-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d45-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d45-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d45-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1d45-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1d45-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f1d45-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f1d45-128">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="f1d45-128">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="f1d45-129">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f1d45-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f1d45-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1d45-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f1d45-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1d45-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f1d45-132">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="f1d45-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

