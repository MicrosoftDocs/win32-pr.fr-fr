---
title: CBN_EDITCHANGE le code de notification (winuser. h)
description: Envoyé après que l’utilisateur a effectué une action qui a peut-être modifié le texte dans la partie de contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- Contrôles Windows de code de notification CBN_EDITCHANGE
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512208"
---
# <a name="cbn_editchange-notification-code"></a><span data-ttu-id="d9183-104">\_Code de notification CBN EDITCHANGE</span><span class="sxs-lookup"><span data-stu-id="d9183-104">CBN\_EDITCHANGE notification code</span></span>

<span data-ttu-id="d9183-105">Envoyé après que l’utilisateur a effectué une action qui a peut-être modifié le texte dans la partie de contrôle d’édition d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d9183-105">Sent after the user has taken an action that may have altered the text in the edit control portion of a combo box.</span></span> <span data-ttu-id="d9183-106">Contrairement au code de notification [CBN \_ EDITUPDATE](cbn-editupdate.md) , ce code de notification est envoyé une fois que le système a mis à jour l’écran.</span><span class="sxs-lookup"><span data-stu-id="d9183-106">Unlike the [CBN\_EDITUPDATE](cbn-editupdate.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="d9183-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d9183-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d9183-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9183-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9183-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9183-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9183-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d9183-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d9183-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="d9183-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d9183-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9183-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9183-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d9183-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9183-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d9183-114">Remarks</span></span>

<span data-ttu-id="d9183-115">Si la zone de liste déroulante a le style [**\_ DropDownList SCC**](combo-box-styles.md) , ce code de notification n’est pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="d9183-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9183-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9183-116">Requirements</span></span>



| <span data-ttu-id="d9183-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9183-117">Requirement</span></span> | <span data-ttu-id="d9183-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9183-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9183-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9183-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9183-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9183-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9183-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9183-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9183-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9183-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9183-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9183-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9183-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9183-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9183-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9183-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9183-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d9183-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9183-127">CBN \_ EDITUPDATE</span><span class="sxs-lookup"><span data-stu-id="d9183-127">CBN\_EDITUPDATE</span></span>](cbn-editupdate.md)
</dt> <dt>

<span data-ttu-id="d9183-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d9183-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d9183-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d9183-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d9183-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d9183-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d9183-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="d9183-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

