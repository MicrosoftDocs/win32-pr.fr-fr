---
title: Message EM_SETMARGINS (winuser. h)
description: Définit les largeurs des marges gauche et droite d’un contrôle d’édition. Le message redessine le contrôle pour refléter les nouvelles marges. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942301"
---
# <a name="em_setmargins-message"></a><span data-ttu-id="1788e-106">\_Message setMargins em</span><span class="sxs-lookup"><span data-stu-id="1788e-106">EM\_SETMARGINS message</span></span>

<span data-ttu-id="1788e-107">Définit les largeurs des marges gauche et droite d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="1788e-107">Sets the widths of the left and right margins for an edit control.</span></span> <span data-ttu-id="1788e-108">Le message redessine le contrôle pour refléter les nouvelles marges.</span><span class="sxs-lookup"><span data-stu-id="1788e-108">The message redraws the control to reflect the new margins.</span></span> <span data-ttu-id="1788e-109">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="1788e-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1788e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1788e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1788e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1788e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1788e-112">Marges à définir.</span><span class="sxs-lookup"><span data-stu-id="1788e-112">The margins to set.</span></span> <span data-ttu-id="1788e-113">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1788e-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1788e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1788e-114">Value</span></span>                                                                                                                                                            | <span data-ttu-id="1788e-115">Signification</span><span class="sxs-lookup"><span data-stu-id="1788e-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <span data-ttu-id="1788e-116"><dt>**\_LEFTMARGIN EC**</dt></span><span class="sxs-lookup"><span data-stu-id="1788e-116"><dt>**EC\_LEFTMARGIN**</dt></span></span> </dl>    | <span data-ttu-id="1788e-117">Définit la marge de gauche.</span><span class="sxs-lookup"><span data-stu-id="1788e-117">Sets the left margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <span data-ttu-id="1788e-118"><dt>**\_RIGHTMARGIN EC**</dt></span><span class="sxs-lookup"><span data-stu-id="1788e-118"><dt>**EC\_RIGHTMARGIN**</dt></span></span> </dl> | <span data-ttu-id="1788e-119">Définit la marge de droite.</span><span class="sxs-lookup"><span data-stu-id="1788e-119">Sets the right margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <span data-ttu-id="1788e-120"><dt>**\_USEFONTINFO EC**</dt></span><span class="sxs-lookup"><span data-stu-id="1788e-120"><dt>**EC\_USEFONTINFO**</dt></span></span> </dl> | <span data-ttu-id="1788e-121">**Contrôles RichEdit :** Définit les marges de gauche et de droite sur une largeur étroite calculée à l’aide des métriques de texte de la police actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1788e-121">**Rich edit controls:** Sets the left and right margins to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="1788e-122">Si aucune police n’a été définie pour le contrôle, les marges sont définies sur zéro.</span><span class="sxs-lookup"><span data-stu-id="1788e-122">If no font has been set for the control, the margins are set to zero.</span></span> <span data-ttu-id="1788e-123">Le paramètre *lParam* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1788e-123">The *lParam* parameter is ignored.</span></span> <br/> <span data-ttu-id="1788e-124">**Contrôles d’édition :** La valeur **EC \_ USEFONTINFO** ne peut pas être utilisée dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1788e-124">**Edit controls:** The **EC\_USEFONTINFO** value cannot be used in the *wParam* parameter.</span></span> <span data-ttu-id="1788e-125">Elle ne peut être utilisée que dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1788e-125">It can only be used in the *lParam* parameter.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1788e-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1788e-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1788e-127">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la nouvelle largeur de la marge de gauche, en pixels.</span><span class="sxs-lookup"><span data-stu-id="1788e-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new width of the left margin, in pixels.</span></span> <span data-ttu-id="1788e-128">Cette valeur est ignorée si *wParam* n’inclut pas l' **UE \_ LEFTMARGIN**.</span><span class="sxs-lookup"><span data-stu-id="1788e-128">This value is ignored if *wParam* does not include **EC\_LEFTMARGIN**.</span></span>

<span data-ttu-id="1788e-129">**Modifiez les contrôles et la modification complète 3,0 et versions ultérieures :** Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) peut spécifier la **valeur \_ USEFONTINFO EC** pour définir la marge de gauche sur une largeur étroite calculée à l’aide des mesures du texte de la police actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1788e-129">**Edit controls and Rich Edit 3.0 and later:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the left margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="1788e-130">Si aucune police n’a été définie pour le contrôle, la marge est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="1788e-130">If no font has been set for the control, the margin is set to zero.</span></span>

<span data-ttu-id="1788e-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la nouvelle largeur de la marge de droite, en pixels.</span><span class="sxs-lookup"><span data-stu-id="1788e-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new width of the right margin, in pixels.</span></span> <span data-ttu-id="1788e-132">Cette valeur est ignorée si *wParam* n’inclut pas **ce \_ RIGHTMARGIN**.</span><span class="sxs-lookup"><span data-stu-id="1788e-132">This value is ignored if *wParam* does not include **EC\_RIGHTMARGIN**.</span></span>

<span data-ttu-id="1788e-133">**Modifiez les contrôles et la modification complète 3,0 et versions ultérieures :** Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) peut spécifier la **valeur \_ USEFONTINFO EC** pour définir la marge de droite sur une largeur étroite calculée à l’aide des métriques de texte de la police actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1788e-133">**Edit controls and Rich Edit 3.0 and later:** The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the right margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="1788e-134">Si aucune police n’a été définie pour le contrôle, la marge est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="1788e-134">If no font has been set for the control, the margin is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1788e-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1788e-135">Return value</span></span>

<span data-ttu-id="1788e-136">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1788e-136">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1788e-137">Notes</span><span class="sxs-lookup"><span data-stu-id="1788e-137">Remarks</span></span>

<span data-ttu-id="1788e-138">**Contrôles d’édition :** Vous ne pouvez pas utiliser **EC \_ USEFONTINFO** dans le paramètre *wParam* , mais vous pouvez l’utiliser dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1788e-138">**Edit controls:** You cannot use **EC\_USEFONTINFO** in the *wParam* parameter, but you can use it in the *lParam* parameter.</span></span>

<span data-ttu-id="1788e-139">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1788e-139">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1788e-140">Toutes les versions RichEdit prennent en charge l’utilisation de la **\_ USEFONTINFO EC** dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1788e-140">All rich edit versions support the use of **EC\_USEFONTINFO** in the *wParam* parameter.</span></span> <span data-ttu-id="1788e-141">Toutefois, seul Microsoft Rich Edit 3,0 et versions ultérieures prennent en charge l’utilisation de **ce \_ USEFONTINFO** dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1788e-141">However, only Microsoft Rich Edit 3.0 and later support the use of **EC\_USEFONTINFO** in the *lParam* parameter.</span></span> <span data-ttu-id="1788e-142">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="1788e-142">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1788e-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1788e-143">Requirements</span></span>



| <span data-ttu-id="1788e-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1788e-144">Requirement</span></span> | <span data-ttu-id="1788e-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="1788e-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1788e-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1788e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1788e-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1788e-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1788e-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1788e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1788e-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1788e-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1788e-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="1788e-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1788e-151"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1788e-151"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1788e-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1788e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1788e-153">**\_GETMARGINS em**</span><span class="sxs-lookup"><span data-stu-id="1788e-153">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
</dt> </dl>

 

