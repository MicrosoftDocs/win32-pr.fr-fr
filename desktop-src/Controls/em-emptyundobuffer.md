---
title: Message EM_EMPTYUNDOBUFFER (winuser. h)
description: Réinitialise l’indicateur d’annulation d’un contrôle d’édition. L’indicateur Undo est défini chaque fois qu’une opération dans le contrôle d’édition peut être annulée. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465899"
---
# <a name="em_emptyundobuffer-message"></a><span data-ttu-id="2d59e-106">\_Message EMPTYUNDOBUFFER em</span><span class="sxs-lookup"><span data-stu-id="2d59e-106">EM\_EMPTYUNDOBUFFER message</span></span>

<span data-ttu-id="2d59e-107">Réinitialise l’indicateur d’annulation d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2d59e-107">Resets the undo flag of an edit control.</span></span> <span data-ttu-id="2d59e-108">L’indicateur Undo est défini chaque fois qu’une opération dans le contrôle d’édition peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="2d59e-108">The undo flag is set whenever an operation within the edit control can be undone.</span></span> <span data-ttu-id="2d59e-109">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="2d59e-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d59e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d59e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d59e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d59e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d59e-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2d59e-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2d59e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d59e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d59e-114">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2d59e-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d59e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d59e-115">Return value</span></span>

<span data-ttu-id="2d59e-116">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2d59e-116">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d59e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2d59e-117">Remarks</span></span>

<span data-ttu-id="2d59e-118">L’indicateur d’annulation est automatiquement réinitialisé chaque fois que le contrôle d’édition reçoit un message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) ou [**em \_ SETHANDLE**](em-sethandle.md) .</span><span class="sxs-lookup"><span data-stu-id="2d59e-118">The undo flag is automatically reset whenever the edit control receives a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) or [**EM\_SETHANDLE**](em-sethandle.md) message.</span></span>

<span data-ttu-id="2d59e-119">**Edit Controls et Rich edit 1,0 :** Le contrôle peut uniquement annuler ou rétablir l’opération la plus récente.</span><span class="sxs-lookup"><span data-stu-id="2d59e-119">**Edit controls and Rich Edit 1.0:** The control can only undo or redo the most recent operation.</span></span>

<span data-ttu-id="2d59e-120">**Édition enrichie 2,0 et versions ultérieures :** Le message **em \_ EMPTYUNDOBUFFER** vide toutes les mémoires tampons d’annulation et de rétablissement.</span><span class="sxs-lookup"><span data-stu-id="2d59e-120">**Rich Edit 2.0 and later:** The **EM\_EMPTYUNDOBUFFER** message empties all undo and redo buffers.</span></span> <span data-ttu-id="2d59e-121">Les contrôles RichEdit permettent à l’utilisateur d’annuler ou de rétablir plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="2d59e-121">Rich edit controls enable the user to undo or redo multiple operations.</span></span>

<span data-ttu-id="2d59e-122">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2d59e-122">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2d59e-123">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="2d59e-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d59e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d59e-124">Requirements</span></span>



| <span data-ttu-id="2d59e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d59e-125">Requirement</span></span> | <span data-ttu-id="2d59e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d59e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d59e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d59e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2d59e-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d59e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2d59e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d59e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2d59e-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d59e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2d59e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d59e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d59e-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d59e-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d59e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d59e-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d59e-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2d59e-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2d59e-135">**EM \_ CANUNDO**</span><span class="sxs-lookup"><span data-stu-id="2d59e-135">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="2d59e-136">**\_SETHANDLE em**</span><span class="sxs-lookup"><span data-stu-id="2d59e-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

[<span data-ttu-id="2d59e-137">**\_Effacer em**</span><span class="sxs-lookup"><span data-stu-id="2d59e-137">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

<span data-ttu-id="2d59e-138">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="2d59e-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2d59e-139">**WM, \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="2d59e-139">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

