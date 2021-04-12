---
title: Message EM_SETSEL (winuser. h)
description: Sélectionne une plage de caractères dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464895"
---
# <a name="em_setsel-message"></a><span data-ttu-id="8b97a-105">\_Message SETSEL em</span><span class="sxs-lookup"><span data-stu-id="8b97a-105">EM\_SETSEL message</span></span>

<span data-ttu-id="8b97a-106">Sélectionne une plage de caractères dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="8b97a-106">Selects a range of characters in an edit control.</span></span> <span data-ttu-id="8b97a-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="8b97a-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b97a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b97a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b97a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b97a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b97a-110">Position du caractère de début de la sélection.</span><span class="sxs-lookup"><span data-stu-id="8b97a-110">The starting character position of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="8b97a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b97a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b97a-112">Position du caractère de fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="8b97a-112">The ending character position of the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b97a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b97a-113">Return value</span></span>

<span data-ttu-id="8b97a-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8b97a-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b97a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8b97a-115">Remarks</span></span>

<span data-ttu-id="8b97a-116">La valeur de début peut être supérieure à la valeur de fin.</span><span class="sxs-lookup"><span data-stu-id="8b97a-116">The start value can be greater than the end value.</span></span> <span data-ttu-id="8b97a-117">La plus petite des deux valeurs spécifie la position de caractère du premier caractère dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="8b97a-117">The lower of the two values specifies the character position of the first character in the selection.</span></span> <span data-ttu-id="8b97a-118">La valeur la plus élevée spécifie la position du premier caractère au-delà de la sélection.</span><span class="sxs-lookup"><span data-stu-id="8b97a-118">The higher value specifies the position of the first character beyond the selection.</span></span>

<span data-ttu-id="8b97a-119">La valeur de début est le point d’ancrage de la sélection, et la valeur de fin est l’extrémité active.</span><span class="sxs-lookup"><span data-stu-id="8b97a-119">The start value is the anchor point of the selection, and the end value is the active end.</span></span> <span data-ttu-id="8b97a-120">Si l’utilisateur utilise la touche Maj pour ajuster la taille de la sélection, l’extrémité active peut se déplacer, mais le point d’ancrage reste le même.</span><span class="sxs-lookup"><span data-stu-id="8b97a-120">If the user uses the SHIFT key to adjust the size of the selection, the active end can move but the anchor point remains the same.</span></span>

<span data-ttu-id="8b97a-121">Si le début est égal à 0 et que la fin est égale à-1, tout le texte du contrôle d’édition est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8b97a-121">If the start is 0 and the end is -1, all the text in the edit control is selected.</span></span> <span data-ttu-id="8b97a-122">Si le début est-1, toute sélection actuelle est désélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8b97a-122">If the start is -1, any current selection is deselected.</span></span>

<span data-ttu-id="8b97a-123">**Contrôles d’édition :** Le contrôle affiche un signe insertion clignotant à la position de fin, quelles que soient les valeurs relatives de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="8b97a-123">**Edit controls:** The control displays a flashing caret at the end position regardless of the relative values of start and end.</span></span>

<span data-ttu-id="8b97a-124">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8b97a-124">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8b97a-125">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="8b97a-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="8b97a-126">Si le contrôle d’édition a le style [**es \_ NOHIDESEL**](edit-control-styles.md) , le texte sélectionné est mis en surbrillance, que le contrôle ait le focus ou non.</span><span class="sxs-lookup"><span data-stu-id="8b97a-126">If the edit control has the [**ES\_NOHIDESEL**](edit-control-styles.md) style, the selected text is highlighted regardless of whether the control has focus.</span></span> <span data-ttu-id="8b97a-127">Sans le style **es \_ NOHIDESEL** , le texte sélectionné est mis en surbrillance uniquement lorsque le contrôle d’édition a le focus.</span><span class="sxs-lookup"><span data-stu-id="8b97a-127">Without the **ES\_NOHIDESEL** style, the selected text is highlighted only when the edit control has the focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b97a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b97a-128">Requirements</span></span>



| <span data-ttu-id="8b97a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b97a-129">Requirement</span></span> | <span data-ttu-id="8b97a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b97a-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b97a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b97a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b97a-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b97a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b97a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b97a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b97a-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b97a-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b97a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b97a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b97a-136"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b97a-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b97a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b97a-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b97a-138">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8b97a-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b97a-139">**\_GETSEL em**</span><span class="sxs-lookup"><span data-stu-id="8b97a-139">**EM\_GETSEL**</span></span>](em-getsel.md)
</dt> <dt>

[<span data-ttu-id="8b97a-140">**\_REPLACESEL em**</span><span class="sxs-lookup"><span data-stu-id="8b97a-140">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
</dt> <dt>

[<span data-ttu-id="8b97a-141">**\_SCROLLCARET em**</span><span class="sxs-lookup"><span data-stu-id="8b97a-141">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="8b97a-142">**\_EXSETSEL em**</span><span class="sxs-lookup"><span data-stu-id="8b97a-142">**EM\_EXSETSEL**</span></span>](em-exsetsel.md)
</dt> </dl>

 

 





