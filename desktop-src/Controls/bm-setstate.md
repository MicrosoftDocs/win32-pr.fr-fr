---
title: Message BM_SETSTATE (winuser. h)
description: Définit l’état de surbrillance d’un bouton. L’état de mise en surbrillance indique si le bouton est mis en surbrillance comme si l’utilisateur l’avait poussé. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ macro SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511748"
---
# <a name="bm_setstate-message"></a><span data-ttu-id="8342a-106">\_Message SETSTATE BM</span><span class="sxs-lookup"><span data-stu-id="8342a-106">BM\_SETSTATE message</span></span>

<span data-ttu-id="8342a-107">Définit l’état de surbrillance d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="8342a-107">Sets the highlight state of a button.</span></span> <span data-ttu-id="8342a-108">L’état de mise en surbrillance indique si le bouton est mis en surbrillance comme si l’utilisateur l’avait poussé.</span><span class="sxs-lookup"><span data-stu-id="8342a-108">The highlight state indicates whether the button is highlighted as if the user had pushed it.</span></span> <span data-ttu-id="8342a-109">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton macro \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .</span><span class="sxs-lookup"><span data-stu-id="8342a-109">You can send this message explicitly or use the [**Button\_SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8342a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8342a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8342a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8342a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8342a-112">Valeur **booléenne** qui spécifie si le bouton est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="8342a-112">A **BOOL** that specifies whether the button is highlighted.</span></span> <span data-ttu-id="8342a-113">La valeur **true** met en surbrillance le bouton.</span><span class="sxs-lookup"><span data-stu-id="8342a-113">A value of **TRUE** highlights the button.</span></span> <span data-ttu-id="8342a-114">La valeur **false** supprime toute mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="8342a-114">A value of **FALSE** removes any highlighting.</span></span>

</dd> <dt>

<span data-ttu-id="8342a-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8342a-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8342a-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="8342a-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8342a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8342a-117">Return value</span></span>

<span data-ttu-id="8342a-118">Ce message retourne toujours la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="8342a-118">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8342a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8342a-119">Remarks</span></span>

<span data-ttu-id="8342a-120">La mise en surbrillance affecte uniquement l’apparence d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="8342a-120">Highlighting affects only the appearance of a button.</span></span> <span data-ttu-id="8342a-121">Elle n’a aucun effet sur l’état d’activation d’une case d’option ou d’une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="8342a-121">It has no effect on the check state of a radio button or check box.</span></span>

<span data-ttu-id="8342a-122">Un bouton est automatiquement mis en surbrillance lorsque l’utilisateur positionne le curseur sur celui-ci et appuie sur le bouton gauche de la souris et le maintient enfoncé.</span><span class="sxs-lookup"><span data-stu-id="8342a-122">A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button.</span></span> <span data-ttu-id="8342a-123">La mise en surbrillance est supprimée lorsque l’utilisateur relâche le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="8342a-123">The highlighting is removed when the user releases the mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="8342a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8342a-124">Requirements</span></span>



| <span data-ttu-id="8342a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8342a-125">Requirement</span></span> | <span data-ttu-id="8342a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8342a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8342a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8342a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8342a-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8342a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8342a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8342a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8342a-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8342a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8342a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="8342a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8342a-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8342a-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8342a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8342a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="8342a-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8342a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8342a-135">**\_GETSTATE BM**</span><span class="sxs-lookup"><span data-stu-id="8342a-135">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="8342a-136">**\_SETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="8342a-136">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





