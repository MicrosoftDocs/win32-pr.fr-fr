---
title: Message WM_UNDO (winuser. h)
description: Une application envoie un \_ message WM Undo à un contrôle d’édition pour annuler la dernière opération. Lorsque ce message est envoyé à un contrôle d’édition, le texte supprimé précédemment est restauré ou le texte ajouté précédemment est supprimé.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465847"
---
# <a name="wm_undo-message"></a><span data-ttu-id="d0d04-105">\_Message d’annulation WM</span><span class="sxs-lookup"><span data-stu-id="d0d04-105">WM\_UNDO message</span></span>

<span data-ttu-id="d0d04-106">Une application envoie un message **WM \_ Undo** à un contrôle d’édition pour annuler la dernière opération.</span><span class="sxs-lookup"><span data-stu-id="d0d04-106">An application sends a **WM\_UNDO** message to an edit control to undo the last operation.</span></span> <span data-ttu-id="d0d04-107">Lorsque ce message est envoyé à un contrôle d’édition, le texte supprimé précédemment est restauré ou le texte ajouté précédemment est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d0d04-107">When this message is sent to an edit control, the previously deleted text is restored or the previously added text is deleted.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0d04-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0d04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0d04-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0d04-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0d04-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d0d04-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d0d04-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0d04-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0d04-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d0d04-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0d04-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0d04-113">Return value</span></span>

<span data-ttu-id="d0d04-114">Si le message est correctement exécuté, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="d0d04-114">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="d0d04-115">Si le message échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="d0d04-115">If the message fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0d04-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d0d04-116">Remarks</span></span>

<span data-ttu-id="d0d04-117">**Modification riche :** Il est recommandé d’utiliser l' [**\_ annulation em**](em-undo.md) à la place de l' **\_ annulation de WM**.</span><span class="sxs-lookup"><span data-stu-id="d0d04-117">**Rich Edit:** It is recommended that [**EM\_UNDO**](em-undo.md) be used instead of **WM\_UNDO**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0d04-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0d04-118">Requirements</span></span>



| <span data-ttu-id="d0d04-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0d04-119">Requirement</span></span> | <span data-ttu-id="d0d04-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0d04-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d04-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0d04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d0d04-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0d04-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d0d04-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0d04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d0d04-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0d04-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0d04-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0d04-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0d04-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0d04-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0d04-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0d04-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0d04-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d0d04-128">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d0d04-129">**WM- \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="d0d04-129">**WM\_CLEAR**</span></span>](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[<span data-ttu-id="d0d04-130">**\_copie WM**</span><span class="sxs-lookup"><span data-stu-id="d0d04-130">**WM\_COPY**</span></span>](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[<span data-ttu-id="d0d04-131">**découpe WM \_**</span><span class="sxs-lookup"><span data-stu-id="d0d04-131">**WM\_CUT**</span></span>](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[<span data-ttu-id="d0d04-132">**\_coller WM**</span><span class="sxs-lookup"><span data-stu-id="d0d04-132">**WM\_PASTE**</span></span>](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

