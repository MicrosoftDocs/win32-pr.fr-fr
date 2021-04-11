---
title: Message EM_SETRECT (winuser. h)
description: Définit le rectangle de mise en forme d’un contrôle d’édition multiligne.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032797"
---
# <a name="em_setrect-message"></a><span data-ttu-id="bdde0-104">\_Message SETRECT em</span><span class="sxs-lookup"><span data-stu-id="bdde0-104">EM\_SETRECT message</span></span>

<span data-ttu-id="bdde0-105">Définit le [rectangle de mise en forme](about-edit-controls.md) d’un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="bdde0-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="bdde0-106">Le rectangle de mise en forme est le rectangle de limitation dans lequel le contrôle dessine le texte.</span><span class="sxs-lookup"><span data-stu-id="bdde0-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="bdde0-107">Le rectangle de limitation est indépendant de la taille de la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="bdde0-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="bdde0-108">Ce message est traité uniquement par les contrôles d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="bdde0-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="bdde0-109">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="bdde0-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdde0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdde0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdde0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdde0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdde0-112">**Édition enrichie 2,0 et versions ultérieures :** Indique si *lParam* spécifie des coordonnées absolues ou relatives.</span><span class="sxs-lookup"><span data-stu-id="bdde0-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="bdde0-113">La valeur zéro indique des coordonnées absolues.</span><span class="sxs-lookup"><span data-stu-id="bdde0-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="bdde0-114">La valeur 1 indique des décalages par rapport au rectangle de mise en forme actuel.</span><span class="sxs-lookup"><span data-stu-id="bdde0-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="bdde0-115">(Les décalages peuvent être positifs ou négatifs.)</span><span class="sxs-lookup"><span data-stu-id="bdde0-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="bdde0-116">**Edit Controls et Rich edit 1,0 :** Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="bdde0-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bdde0-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdde0-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdde0-118">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie les nouvelles dimensions du rectangle.</span><span class="sxs-lookup"><span data-stu-id="bdde0-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="bdde0-119">Si ce paramètre a la **valeur null**, le rectangle de mise en forme est défini sur ses valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="bdde0-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdde0-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdde0-120">Return value</span></span>

<span data-ttu-id="bdde0-121">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bdde0-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdde0-122">Notes</span><span class="sxs-lookup"><span data-stu-id="bdde0-122">Remarks</span></span>

<span data-ttu-id="bdde0-123">L’affectation de la **valeur null** à *lParam* n’a aucun effet si un appareil tactile est installé, ou si **em \_ SETRECT** est envoyé à partir d’un thread sur lequel un raccordement est installé (voir [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="bdde0-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="bdde0-124">Dans ces cas, *lParam* doit contenir un pointeur valide vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bdde0-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="bdde0-125">Le message **em \_ SETRECT** provoque le redessin du texte du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="bdde0-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="bdde0-126">Pour modifier la taille du rectangle de mise en forme sans redessiner le texte, utilisez le message [**em \_ SETRECTNP**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="bdde0-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="bdde0-127">Lorsqu’un contrôle d’édition est créé pour la première fois, le rectangle de mise en forme est défini sur une taille par défaut.</span><span class="sxs-lookup"><span data-stu-id="bdde0-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="bdde0-128">Vous pouvez utiliser le **message \_ SETRECT em** pour agrandir ou réduire la taille du rectangle de mise en forme par rapport à la fenêtre Modifier le contrôle.</span><span class="sxs-lookup"><span data-stu-id="bdde0-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="bdde0-129">Si le contrôle d’édition n’a pas de barre de défilement horizontale et que le rectangle de mise en forme est plus grand que la fenêtre de contrôle d’édition, les lignes de texte qui dépassent la largeur de la fenêtre de contrôle d’édition (mais inférieure à la largeur du rectangle de mise en forme) sont découpées au lieu d’être encapsulées.</span><span class="sxs-lookup"><span data-stu-id="bdde0-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="bdde0-130">Si le contrôle d’édition contient une bordure, le rectangle de mise en forme est réduit de la taille de la bordure.</span><span class="sxs-lookup"><span data-stu-id="bdde0-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="bdde0-131">Si vous ajustez le rectangle retourné par un message [**em \_ GETRECT**](em-getrect.md) , vous devez supprimer la taille de la bordure avant d’utiliser le rectangle avec le message **em \_ SETRECT** .</span><span class="sxs-lookup"><span data-stu-id="bdde0-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="bdde0-132">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bdde0-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="bdde0-133">Le rectangle de mise en forme n’inclut pas la barre de sélection, qui est une zone non marquée à gauche de chaque paragraphe.</span><span class="sxs-lookup"><span data-stu-id="bdde0-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="bdde0-134">Lorsque l’utilisateur clique dans la barre de sélection, la ligne correspondante est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="bdde0-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="bdde0-135">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="bdde0-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdde0-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdde0-136">Requirements</span></span>



| <span data-ttu-id="bdde0-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdde0-137">Requirement</span></span> | <span data-ttu-id="bdde0-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdde0-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdde0-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdde0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bdde0-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdde0-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bdde0-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdde0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bdde0-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdde0-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bdde0-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdde0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdde0-144"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdde0-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdde0-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdde0-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="bdde0-146">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bdde0-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bdde0-147">**\_GETRECT em**</span><span class="sxs-lookup"><span data-stu-id="bdde0-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="bdde0-148">**\_SETRECTNP em**</span><span class="sxs-lookup"><span data-stu-id="bdde0-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="bdde0-149">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="bdde0-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="bdde0-150">[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bdde0-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

