---
title: Message EM_SETFONTSIZE (RichEdit. h)
description: Définit la taille de police du texte sélectionné dans un contrôle RichEdit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465383"
---
# <a name="em_setfontsize-message"></a><span data-ttu-id="c72ed-104">\_Message SETFONTSIZE em</span><span class="sxs-lookup"><span data-stu-id="c72ed-104">EM\_SETFONTSIZE message</span></span>

<span data-ttu-id="c72ed-105">Définit la taille de police du texte sélectionné dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="c72ed-105">Sets the font size for the selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c72ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c72ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c72ed-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c72ed-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c72ed-108">Modification de la taille en points du texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c72ed-108">Change in point size of the selected text.</span></span> <span data-ttu-id="c72ed-109">Le résultat sera arrondi en fonction des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c72ed-109">The result will be rounded according to values shown in the following table.</span></span> <span data-ttu-id="c72ed-110">Ce paramètre doit être compris entre-1637 et 1638.</span><span class="sxs-lookup"><span data-stu-id="c72ed-110">This parameter should be in the range of -1637 to 1638.</span></span> <span data-ttu-id="c72ed-111">La taille de police obtenue sera comprise dans la plage comprise entre 1 et 1638.</span><span class="sxs-lookup"><span data-stu-id="c72ed-111">The resulting font size will be within the range of 1 to 1638.</span></span>

</dd> <dt>

<span data-ttu-id="c72ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c72ed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c72ed-113">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c72ed-113">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c72ed-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c72ed-114">Return value</span></span>

<span data-ttu-id="c72ed-115">Si aucune erreur ne s’est produite, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="c72ed-115">If no error occurred, the return value is **TRUE**.</span></span>

<span data-ttu-id="c72ed-116">Si une erreur s’est produite, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="c72ed-116">If an error occurred, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c72ed-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c72ed-117">Remarks</span></span>

<span data-ttu-id="c72ed-118">Vous pouvez facilement récupérer la taille de police en envoyant le message [**em \_ GETCHARFORMAT**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="c72ed-118">You can easily get the font size by sending the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span>

<span data-ttu-id="c72ed-119">Rich Edit ajoute d’abord *wParam* à la taille de police actuelle, puis utilise la taille obtenue et le tableau suivant pour déterminer la valeur d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="c72ed-119">Rich Edit first adds *wParam* to the current font size and then uses the resulting size and the following table to determine the rounding value.</span></span>



| <span data-ttu-id="c72ed-120">Élastique</span><span class="sxs-lookup"><span data-stu-id="c72ed-120">Band</span></span>    | <span data-ttu-id="c72ed-121">Valeur d’arrondi</span><span class="sxs-lookup"><span data-stu-id="c72ed-121">Rounding value</span></span> |
|---------|----------------|
| <span data-ttu-id="c72ed-122"><= 12</span><span class="sxs-lookup"><span data-stu-id="c72ed-122"><=12</span></span> | <span data-ttu-id="c72ed-123">1</span><span class="sxs-lookup"><span data-stu-id="c72ed-123">1</span></span>              |
| <span data-ttu-id="c72ed-124">28</span><span class="sxs-lookup"><span data-stu-id="c72ed-124">28</span></span>      | <span data-ttu-id="c72ed-125">2</span><span class="sxs-lookup"><span data-stu-id="c72ed-125">2</span></span>              |
| <span data-ttu-id="c72ed-126">36</span><span class="sxs-lookup"><span data-stu-id="c72ed-126">36</span></span>      | <span data-ttu-id="c72ed-127">0</span><span class="sxs-lookup"><span data-stu-id="c72ed-127">0</span></span>              |
| <span data-ttu-id="c72ed-128">48</span><span class="sxs-lookup"><span data-stu-id="c72ed-128">48</span></span>      | <span data-ttu-id="c72ed-129">0</span><span class="sxs-lookup"><span data-stu-id="c72ed-129">0</span></span>              |
| <span data-ttu-id="c72ed-130">72</span><span class="sxs-lookup"><span data-stu-id="c72ed-130">72</span></span>      | <span data-ttu-id="c72ed-131">0</span><span class="sxs-lookup"><span data-stu-id="c72ed-131">0</span></span>              |
| <span data-ttu-id="c72ed-132">80</span><span class="sxs-lookup"><span data-stu-id="c72ed-132">80</span></span>      | <span data-ttu-id="c72ed-133">0</span><span class="sxs-lookup"><span data-stu-id="c72ed-133">0</span></span>              |
| <span data-ttu-id="c72ed-134">> 80</span><span class="sxs-lookup"><span data-stu-id="c72ed-134">> 80</span></span> | <span data-ttu-id="c72ed-135">10</span><span class="sxs-lookup"><span data-stu-id="c72ed-135">10</span></span>             |



 

<span data-ttu-id="c72ed-136">Si la taille de police obtenue n’est pas divisible par la valeur d’arrondi, la taille de police est ensuite arrondie à un nombre uniformément divisible par la valeur d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="c72ed-136">If the resulting font size is not evenly divisible by the rounding value, the font size is then rounded to a number evenly divisible by the rounding value.</span></span> <span data-ttu-id="c72ed-137">Par conséquent, si la taille de police est inférieure ou égale à 12, la valeur d’arrondi sera 1.</span><span class="sxs-lookup"><span data-stu-id="c72ed-137">So if the font size is less than or equal to 12, the rounding value will be 1.</span></span> <span data-ttu-id="c72ed-138">De même, si la taille de police est inférieure ou égale à 28, la valeur d’arrondi est 2.</span><span class="sxs-lookup"><span data-stu-id="c72ed-138">Similarly, if the font size is less than or equal to 28, the rounding value is 2.</span></span> <span data-ttu-id="c72ed-139">Pour les valeurs supérieures à 28, les tailles de police sont arrondies à la bande suivante.</span><span class="sxs-lookup"><span data-stu-id="c72ed-139">For values greater than 28, font sizes are rounded to the next band.</span></span> <span data-ttu-id="c72ed-140">Par conséquent, la taille de police passe à 36, 48, 72, 80.</span><span class="sxs-lookup"><span data-stu-id="c72ed-140">So, the font size jumps to 36, 48, 72, 80.</span></span> <span data-ttu-id="c72ed-141">Après 80, tous les arrondis sont effectués par incréments de dix points.</span><span class="sxs-lookup"><span data-stu-id="c72ed-141">After 80, all rounding is done in increments of ten points.</span></span>

<span data-ttu-id="c72ed-142">La taille de police est arrondie vers le haut ou vers le haut selon le signe de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="c72ed-142">The font size is rounded up or down depending on the sign of *wParam*.</span></span> <span data-ttu-id="c72ed-143">Si *wParam* est positif, l’arrondi est toujours en haut.</span><span class="sxs-lookup"><span data-stu-id="c72ed-143">If *wParam* is positive, the rounding is always up.</span></span> <span data-ttu-id="c72ed-144">Dans le cas contraire, l’arrondi est toujours inactif.</span><span class="sxs-lookup"><span data-stu-id="c72ed-144">Otherwise, rounding is always down.</span></span> <span data-ttu-id="c72ed-145">Ainsi, si la taille de police actuelle est 10 et que *wParam* est 3, la taille de police obtenue est 14 (10 + 3 = 13, qui n’est pas divisible par 2, donc la taille est arrondie à 14).</span><span class="sxs-lookup"><span data-stu-id="c72ed-145">So, if the current font size is 10 and *wParam* is 3, the resulting font size would be 14 (10 + 3 = 13, which is not divisible by 2, so the size rounds up to 14).</span></span> <span data-ttu-id="c72ed-146">À l’inverse, si la taille de police actuelle est 14 et que *wParam* est-3, la taille de police obtenue est 10 (14-3 = 11, qui n’est pas divisible par 2, donc la taille est arrondie à 10).</span><span class="sxs-lookup"><span data-stu-id="c72ed-146">Conversely, if the current font size is 14 and *wParam* is -3, the resulting font size would be 10 (14 - 3 = 11, which is not divisible by 2, so the size rounds down to 10).</span></span>

<span data-ttu-id="c72ed-147">La modification est appliquée à chaque partie de la sélection.</span><span class="sxs-lookup"><span data-stu-id="c72ed-147">The change is applied to each part of the selection.</span></span> <span data-ttu-id="c72ed-148">Ainsi, si une partie du texte est 10 PT et d’autres 20 points, une fois qu’un appel avec *wParam* a la valeur 1, les tailles de police deviennent 11pt et 22pt, respectivement.</span><span class="sxs-lookup"><span data-stu-id="c72ed-148">So, if some of the text is 10pt and some 20pt, after a call with *wParam* set to 1, the font sizes become 11pt and 22pt, respectively.</span></span>

<span data-ttu-id="c72ed-149">Des exemples supplémentaires sont présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c72ed-149">Additional examples are shown in the following table.</span></span>



| <span data-ttu-id="c72ed-150">Taille de la police d’origine</span><span class="sxs-lookup"><span data-stu-id="c72ed-150">Original font size</span></span> | <span data-ttu-id="c72ed-151">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c72ed-151">*wParam*</span></span> | <span data-ttu-id="c72ed-152">Taille de police obtenue</span><span class="sxs-lookup"><span data-stu-id="c72ed-152">Resulting font size</span></span> |
|--------------------|----------|---------------------|
| <span data-ttu-id="c72ed-153">7</span><span class="sxs-lookup"><span data-stu-id="c72ed-153">7</span></span>                  | <span data-ttu-id="c72ed-154">1</span><span class="sxs-lookup"><span data-stu-id="c72ed-154">1</span></span>        | <span data-ttu-id="c72ed-155">8</span><span class="sxs-lookup"><span data-stu-id="c72ed-155">8</span></span>                   |
| <span data-ttu-id="c72ed-156">7</span><span class="sxs-lookup"><span data-stu-id="c72ed-156">7</span></span>                  | <span data-ttu-id="c72ed-157">3</span><span class="sxs-lookup"><span data-stu-id="c72ed-157">3</span></span>        | <span data-ttu-id="c72ed-158">10</span><span class="sxs-lookup"><span data-stu-id="c72ed-158">10</span></span>                  |
| <span data-ttu-id="c72ed-159">10</span><span class="sxs-lookup"><span data-stu-id="c72ed-159">10</span></span>                 | <span data-ttu-id="c72ed-160">3</span><span class="sxs-lookup"><span data-stu-id="c72ed-160">3</span></span>        | <span data-ttu-id="c72ed-161">14</span><span class="sxs-lookup"><span data-stu-id="c72ed-161">14</span></span>                  |
| <span data-ttu-id="c72ed-162">14</span><span class="sxs-lookup"><span data-stu-id="c72ed-162">14</span></span>                 | <span data-ttu-id="c72ed-163">-3</span><span class="sxs-lookup"><span data-stu-id="c72ed-163">-3</span></span>       | <span data-ttu-id="c72ed-164">10</span><span class="sxs-lookup"><span data-stu-id="c72ed-164">10</span></span>                  |
| <span data-ttu-id="c72ed-165">28</span><span class="sxs-lookup"><span data-stu-id="c72ed-165">28</span></span>                 | <span data-ttu-id="c72ed-166">1</span><span class="sxs-lookup"><span data-stu-id="c72ed-166">1</span></span>        | <span data-ttu-id="c72ed-167">36</span><span class="sxs-lookup"><span data-stu-id="c72ed-167">36</span></span>                  |
| <span data-ttu-id="c72ed-168">28</span><span class="sxs-lookup"><span data-stu-id="c72ed-168">28</span></span>                 | <span data-ttu-id="c72ed-169">3</span><span class="sxs-lookup"><span data-stu-id="c72ed-169">3</span></span>        | <span data-ttu-id="c72ed-170">36</span><span class="sxs-lookup"><span data-stu-id="c72ed-170">36</span></span>                  |
| <span data-ttu-id="c72ed-171">80</span><span class="sxs-lookup"><span data-stu-id="c72ed-171">80</span></span>                 | <span data-ttu-id="c72ed-172">1</span><span class="sxs-lookup"><span data-stu-id="c72ed-172">1</span></span>        | <span data-ttu-id="c72ed-173">90</span><span class="sxs-lookup"><span data-stu-id="c72ed-173">90</span></span>                  |
| <span data-ttu-id="c72ed-174">80</span><span class="sxs-lookup"><span data-stu-id="c72ed-174">80</span></span>                 | <span data-ttu-id="c72ed-175">-1</span><span class="sxs-lookup"><span data-stu-id="c72ed-175">-1</span></span>       | <span data-ttu-id="c72ed-176">72</span><span class="sxs-lookup"><span data-stu-id="c72ed-176">72</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="c72ed-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c72ed-177">Requirements</span></span>



| <span data-ttu-id="c72ed-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c72ed-178">Requirement</span></span> | <span data-ttu-id="c72ed-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="c72ed-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c72ed-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c72ed-180">Minimum supported client</span></span><br/> | <span data-ttu-id="c72ed-181">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c72ed-181">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c72ed-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c72ed-182">Minimum supported server</span></span><br/> | <span data-ttu-id="c72ed-183">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c72ed-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c72ed-184">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c72ed-184">Redistributable</span></span><br/>          | <span data-ttu-id="c72ed-185">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="c72ed-185">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="c72ed-186">En-tête</span><span class="sxs-lookup"><span data-stu-id="c72ed-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="c72ed-187"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c72ed-187"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72ed-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c72ed-188">See also</span></span>

<dl> <dt>

<span data-ttu-id="c72ed-189">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c72ed-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c72ed-190">**\_GETCHARFORMAT em**</span><span class="sxs-lookup"><span data-stu-id="c72ed-190">**EM\_GETCHARFORMAT**</span></span>](em-getcharformat.md)
</dt> <dt>

[<span data-ttu-id="c72ed-191">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="c72ed-191">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

<span data-ttu-id="c72ed-192">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c72ed-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c72ed-193">À propos des contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="c72ed-193">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





