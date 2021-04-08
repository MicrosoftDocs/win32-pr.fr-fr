---
title: Message EM_UNDO (winuser. h)
description: Ce message annule la dernière opération de contrôle d’édition dans la file d’attente d’annulation du contrôle. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741580"
---
# <a name="em_undo-message"></a><span data-ttu-id="d54fb-105">\_Message d’annulation em</span><span class="sxs-lookup"><span data-stu-id="d54fb-105">EM\_UNDO message</span></span>

<span data-ttu-id="d54fb-106">Ce message annule la dernière opération de contrôle d’édition dans la file d’attente d’annulation du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d54fb-106">This message undoes the last edit control operation in the control's undo queue.</span></span> <span data-ttu-id="d54fb-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="d54fb-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d54fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d54fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d54fb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d54fb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d54fb-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d54fb-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d54fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d54fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d54fb-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d54fb-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d54fb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d54fb-113">Return value</span></span>

<span data-ttu-id="d54fb-114">Dans le cas d’un contrôle d’édition sur une seule ligne, la valeur de retour est toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="d54fb-114">For a single-line edit control, the return value is always **TRUE**.</span></span>

<span data-ttu-id="d54fb-115">Pour un contrôle d’édition multiligne, la valeur de retour est **true** si l’opération d’annulation réussit, ou **false** si l’opération d’annulation échoue.</span><span class="sxs-lookup"><span data-stu-id="d54fb-115">For a multiline edit control, the return value is **TRUE** if the undo operation is successful, or **FALSE** if the undo operation fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="d54fb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d54fb-116">Remarks</span></span>

<span data-ttu-id="d54fb-117">**Edit Controls et Rich edit 1,0 :** Une opération d’annulation peut également être annulée.</span><span class="sxs-lookup"><span data-stu-id="d54fb-117">**Edit controls and Rich Edit 1.0:** An undo operation can also be undone.</span></span> <span data-ttu-id="d54fb-118">Par exemple, vous pouvez restaurer le texte supprimé avec le premier message d' **\_ annulation d’em** , puis supprimer le texte avec un deuxième message d' **\_ annulation em** tant qu’il n’y a pas d’opération de modification intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="d54fb-118">For example, you can restore deleted text with the first **EM\_UNDO** message, and remove the text again with a second **EM\_UNDO** message as long as there is no intervening edit operation.</span></span>

<span data-ttu-id="d54fb-119">**Édition enrichie 2,0 et versions ultérieures :** La fonctionnalité d’annulation est multiniveau et l’envoi de deux messages d' **\_ annulation em** annule les deux dernières opérations dans la file d’attente d’annulation.</span><span class="sxs-lookup"><span data-stu-id="d54fb-119">**Rich Edit 2.0 and later:** The undo feature is multilevel so sending two **EM\_UNDO** messages will undo the last two operations in the undo queue.</span></span> <span data-ttu-id="d54fb-120">Pour rétablir une opération, envoyez le message de [**\_ rétablissement em**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="d54fb-120">To redo an operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

<span data-ttu-id="d54fb-121">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d54fb-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="d54fb-122">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="d54fb-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d54fb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d54fb-123">Requirements</span></span>



| <span data-ttu-id="d54fb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d54fb-124">Requirement</span></span> | <span data-ttu-id="d54fb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d54fb-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d54fb-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d54fb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d54fb-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d54fb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d54fb-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d54fb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d54fb-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d54fb-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d54fb-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d54fb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d54fb-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d54fb-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d54fb-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d54fb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54fb-133">**EM \_ CANUNDO**</span><span class="sxs-lookup"><span data-stu-id="d54fb-133">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> </dl>

 

 





