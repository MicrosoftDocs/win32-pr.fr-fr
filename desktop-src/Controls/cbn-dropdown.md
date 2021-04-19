---
title: CBN_DROPDOWN le code de notification (winuser. h)
description: Envoyé lorsque la zone de liste d’une zone de liste déroulante va être affichée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- Contrôles Windows de code de notification CBN_DROPDOWN
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511374"
---
# <a name="cbn_dropdown-notification-code"></a><span data-ttu-id="2decc-105">\_Code de notification de liste déroulante CBN</span><span class="sxs-lookup"><span data-stu-id="2decc-105">CBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="2decc-106">Envoyé lorsque la zone de liste d’une zone de liste déroulante va être affichée.</span><span class="sxs-lookup"><span data-stu-id="2decc-106">Sent when the list box of a combo box is about to be made visible.</span></span> <span data-ttu-id="2decc-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2decc-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2decc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2decc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2decc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2decc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2decc-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2decc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="2decc-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="2decc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2decc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2decc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2decc-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2decc-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2decc-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2decc-114">Remarks</span></span>

<span data-ttu-id="2decc-115">Ce code de notification n’est envoyé que si la zone de liste déroulante [**SCC \_**](combo-box-styles.md) ou le style [**\_ DropDownList CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2decc-115">This notification code is only sent if the combo box has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2decc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2decc-116">Requirements</span></span>



| <span data-ttu-id="2decc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2decc-117">Requirement</span></span> | <span data-ttu-id="2decc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2decc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2decc-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2decc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2decc-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2decc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2decc-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2decc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2decc-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2decc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2decc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2decc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2decc-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2decc-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2decc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2decc-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2decc-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2decc-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2decc-127">CBN \_ gros plan</span><span class="sxs-lookup"><span data-stu-id="2decc-127">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

<span data-ttu-id="2decc-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="2decc-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2decc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2decc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2decc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2decc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2decc-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="2decc-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

