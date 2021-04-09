---
title: Message EM_SCROLL (winuser. h)
description: Fait défiler le texte verticalement dans un contrôle d’édition multiligne. Ce message revient à envoyer un message WM \_ VSCROLL au contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106267"
---
# <a name="em_scroll-message"></a><span data-ttu-id="b7b7b-106">\_Message de défilement em</span><span class="sxs-lookup"><span data-stu-id="b7b7b-106">EM\_SCROLL message</span></span>

<span data-ttu-id="b7b7b-107">Fait défiler le texte verticalement dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-107">Scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="b7b7b-108">Ce message revient à envoyer un message [**WM \_ VSCROLL**](wm-vscroll.md) au contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-108">This message is equivalent to sending a [**WM\_VSCROLL**](wm-vscroll.md) message to the edit control.</span></span> <span data-ttu-id="b7b7b-109">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7b7b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7b7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b7b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7b7b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7b7b-112">Action que la barre de défilement doit prendre.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-112">The action the scroll bar is to take.</span></span> <span data-ttu-id="b7b7b-113">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b7b7b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7b7b-114">Value</span></span>                                                                                                                                                   | <span data-ttu-id="b7b7b-115">Signification</span><span class="sxs-lookup"><span data-stu-id="b7b7b-115">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="b7b7b-116"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="b7b7b-116"><dt>**SB\_LINEDOWN**</dt></span></span> </dl> | <span data-ttu-id="b7b7b-117">Fait défiler d’une ligne vers le bas.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-117">Scrolls down one line.</span></span><br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="b7b7b-118"><dt>**\_gamme SB**</dt></span><span class="sxs-lookup"><span data-stu-id="b7b7b-118"><dt>**SB\_LINEUP**</dt></span></span> </dl>       | <span data-ttu-id="b7b7b-119">Fait défiler d’une ligne vers le haut.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-119">Scrolls up one line.</span></span><br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="b7b7b-120"><dt>**SB \_ PG.**</dt></span><span class="sxs-lookup"><span data-stu-id="b7b7b-120"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl> | <span data-ttu-id="b7b7b-121">Fait défiler d’une page vers le bas.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-121">Scrolls down one page.</span></span><br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="b7b7b-122"><dt>**SB \_ PG PRÉC**</dt></span><span class="sxs-lookup"><span data-stu-id="b7b7b-122"><dt>**SB\_PAGEUP**</dt></span></span> </dl>       | <span data-ttu-id="b7b7b-123">Fait défiler d’une page vers le haut.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-123">Scrolls up one page.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="b7b7b-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7b7b-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7b7b-125">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-125">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7b7b-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7b7b-126">Return value</span></span>

<span data-ttu-id="b7b7b-127">Si le message est réussi, le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de la valeur de retour est **true** et le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est le nombre de lignes que la commande défile.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-127">If the message is successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the return value is **TRUE**, and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the number of lines that the command scrolls.</span></span> <span data-ttu-id="b7b7b-128">Le nombre retourné peut ne pas être le même que le nombre réel de lignes défilantes si le défilement se déplace au début ou à la fin du texte.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-128">The number returned may not be the same as the actual number of lines scrolled if the scrolling moves to the beginning or the end of the text.</span></span> <span data-ttu-id="b7b7b-129">Si le paramètre *wParam* spécifie une valeur non valide, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-129">If the *wParam* parameter specifies an invalid value, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b7b-130">Notes</span><span class="sxs-lookup"><span data-stu-id="b7b7b-130">Remarks</span></span>

<span data-ttu-id="b7b7b-131">Pour faire défiler jusqu’à la position d’un caractère ou d’une ligne spécifique, utilisez le message [**em \_ LINESCROLL**](em-linescroll.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b7b-131">To scroll to a specific line or character position, use the [**EM\_LINESCROLL**](em-linescroll.md) message.</span></span> <span data-ttu-id="b7b7b-132">Pour faire défiler le signe insertion dans la vue, utilisez le message [**em \_ SCROLLCARET**](em-scrollcaret.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b7b-132">To scroll the caret into view, use the [**EM\_SCROLLCARET**](em-scrollcaret.md) message.</span></span>

<span data-ttu-id="b7b7b-133">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-133">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b7b7b-134">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="b7b7b-134">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b7b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7b7b-135">Requirements</span></span>



| <span data-ttu-id="b7b7b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7b7b-136">Requirement</span></span> | <span data-ttu-id="b7b7b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7b7b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b7b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7b7b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b7b-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7b7b-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b7b7b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7b7b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b7b-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7b7b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7b7b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7b7b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b7b-143"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7b7b-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7b7b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7b7b-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7b7b-145">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b7b7b-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b7b7b-146">**\_LINESCROLL em**</span><span class="sxs-lookup"><span data-stu-id="b7b7b-146">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="b7b7b-147">**\_SCROLLCARET em**</span><span class="sxs-lookup"><span data-stu-id="b7b7b-147">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="b7b7b-148">**\_VSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="b7b7b-148">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

