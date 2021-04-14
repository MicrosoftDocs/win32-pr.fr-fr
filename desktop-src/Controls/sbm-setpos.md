---
title: Message SBM_SETPOS (winuser. h)
description: Le \_ message SBM SetPos est envoyé pour définir la position de la case de défilement (Thumb) et, le cas échéant, redessine la barre de défilement pour refléter la nouvelle position de la case de défilement.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- SBM_SETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466934"
---
# <a name="sbm_setpos-message"></a><span data-ttu-id="ebbc2-104">\_Message SBM SetPos</span><span class="sxs-lookup"><span data-stu-id="ebbc2-104">SBM\_SETPOS message</span></span>

<span data-ttu-id="ebbc2-105">Le message **SBM \_ SetPos** est envoyé pour définir la position de la case de défilement (Thumb) et, le cas échéant, redessine la barre de défilement pour refléter la nouvelle position de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-105">The **SBM\_SETPOS** message is sent to set the position of the scroll box (thumb) and, if requested, redraw the scroll bar to reflect the new position of the scroll box.</span></span>

<span data-ttu-id="ebbc2-106">Les applications ne doivent pas envoyer ce message directement.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-106">Applications should not send this message directly.</span></span> <span data-ttu-id="ebbc2-107">Au lieu de cela, ils doivent utiliser la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="ebbc2-107">Instead, they should use the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span> <span data-ttu-id="ebbc2-108">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ebbc2-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="ebbc2-109">Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollPos** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollPos** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebbc2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebbc2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebbc2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebbc2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebbc2-112">Spécifie la nouvelle position de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-112">Specifies the new position of the scroll box.</span></span> <span data-ttu-id="ebbc2-113">Elle doit être comprise dans la plage de défilement.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-113">It must be within the scrolling range.</span></span> <span data-ttu-id="ebbc2-114">Si ce paramètre est en dehors de la plage de défilement, la valeur est arrondie à la valeur la plus proche valide.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-114">If this parameter is outside of the scrolling range, the value is rounded up or down to the nearest valid value.</span></span>

</dd> <dt>

<span data-ttu-id="ebbc2-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebbc2-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebbc2-116">Spécifie si la barre de défilement doit être redessinée pour refléter la nouvelle position de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-116">Specifies whether the scroll bar should be redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="ebbc2-117">Si ce paramètre a la **valeur true**, la barre de défilement est redessinée.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-117">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="ebbc2-118">Si la **valeur est false**, la barre de défilement n’est pas redessinée.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-118">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebbc2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebbc2-119">Return value</span></span>

<span data-ttu-id="ebbc2-120">**ComCtl32.dll version 5,0**: si la position de la case de défilement a changé, la valeur de retour est la position précédente de la case de défilement ; dans le cas contraire, il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-120">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="ebbc2-121">**ComCtl32.dll version 6,0**: position actuelle de la case de défilement, qu’elle ait été modifiée ou non.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-121">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebbc2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ebbc2-122">Remarks</span></span>

<span data-ttu-id="ebbc2-123">Si le contrôle de barre de défilement est redessiné par un appel ultérieur à une autre fonction, l’affectation de la **valeur false** au paramètre *lParam* est utile.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-123">If the scroll bar control is redrawn by a subsequent call to another function, setting the *lParam* parameter to **FALSE** is useful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebbc2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebbc2-124">Requirements</span></span>



| <span data-ttu-id="ebbc2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebbc2-125">Requirement</span></span> | <span data-ttu-id="ebbc2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebbc2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbc2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebbc2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ebbc2-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebbc2-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ebbc2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebbc2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ebbc2-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebbc2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebbc2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebbc2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebbc2-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebbc2-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebbc2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebbc2-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebbc2-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ebbc2-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ebbc2-135">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="ebbc2-135">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="ebbc2-136">**\_GETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="ebbc2-136">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="ebbc2-137">**\_DÉtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="ebbc2-137">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="ebbc2-138">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="ebbc2-138">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

