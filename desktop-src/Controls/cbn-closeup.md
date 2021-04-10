---
title: CBN_CLOSEUP le code de notification (winuser. h)
description: Envoyé lorsque la zone de liste d’une zone de liste déroulante a été fermée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- Contrôles Windows de code de notification CBN_CLOSEUP
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106444"
---
# <a name="cbn_closeup-notification-code"></a><span data-ttu-id="d6667-105">\_Code de notification CBN gros plan</span><span class="sxs-lookup"><span data-stu-id="d6667-105">CBN\_CLOSEUP notification code</span></span>

<span data-ttu-id="d6667-106">Envoyé lorsque la zone de liste d’une zone de liste déroulante a été fermée.</span><span class="sxs-lookup"><span data-stu-id="d6667-106">Sent when the list box of a combo box has been closed.</span></span> <span data-ttu-id="d6667-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d6667-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d6667-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6667-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6667-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6667-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6667-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d6667-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d6667-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="d6667-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d6667-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6667-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6667-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d6667-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6667-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d6667-114">Remarks</span></span>

<span data-ttu-id="d6667-115">Si l’utilisateur a modifié la sélection actuelle, la zone de liste déroulante envoie également le code de notification [CBN \_ selChange](cbn-selchange.md) lorsque la liste déroulante se ferme.</span><span class="sxs-lookup"><span data-stu-id="d6667-115">If the user changed the current selection, the combo box also sends the [CBN\_SELCHANGE](cbn-selchange.md) notification code when the drop-down list closes.</span></span> <span data-ttu-id="d6667-116">En général, vous ne pouvez pas prédire l’ordre dans lequel les codes de notification seront envoyés.</span><span class="sxs-lookup"><span data-stu-id="d6667-116">In general, you cannot predict the order in which notification codes will be sent.</span></span> <span data-ttu-id="d6667-117">En particulier, un \_ Code de notification CBN selChange peut se produire avant ou après un \_ Code de notification CBN gros plan.</span><span class="sxs-lookup"><span data-stu-id="d6667-117">In particular, a CBN\_SELCHANGE notification code may occur either before or after a CBN\_CLOSEUP notification code.</span></span>

<span data-ttu-id="d6667-118">Pour exécuter un processus spécifique chaque fois que l’utilisateur sélectionne un élément de liste, vous pouvez gérer le code de notification [CBN \_ selChange](cbn-selchange.md) ou CBN \_ gros plan.</span><span class="sxs-lookup"><span data-stu-id="d6667-118">To execute a specific process each time the user selects a list item, you can handle either the [CBN\_SELCHANGE](cbn-selchange.md) or CBN\_CLOSEUP notification code.</span></span> <span data-ttu-id="d6667-119">En général, vous attendez le code de \_ notification CBN gros plan avant de traiter une modification dans la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="d6667-119">Typically, you would wait for the CBN\_CLOSEUP notification code before processing a change in the current selection.</span></span> <span data-ttu-id="d6667-120">Cela peut être particulièrement important si une quantité importante de traitement est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d6667-120">This can be particularly important if a significant amount of processing is required.</span></span>

<span data-ttu-id="d6667-121">Ce code de notification n’est pas envoyé à une zone de liste déroulante avec le style [**CBS \_ simple**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d6667-121">This notification code is not sent to a combo box that has the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6667-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6667-122">Requirements</span></span>



| <span data-ttu-id="d6667-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6667-123">Requirement</span></span> | <span data-ttu-id="d6667-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6667-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6667-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6667-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d6667-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6667-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6667-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6667-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d6667-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6667-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6667-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6667-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6667-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6667-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6667-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6667-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6667-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d6667-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d6667-133">\_liste déroulante CBN</span><span class="sxs-lookup"><span data-stu-id="d6667-133">CBN\_DROPDOWN</span></span>](cbn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="d6667-134">CBN \_ selChange</span><span class="sxs-lookup"><span data-stu-id="d6667-134">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="d6667-135">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d6667-135">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d6667-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6667-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d6667-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6667-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d6667-138">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="d6667-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

