---
title: Message EM_SETCTFMODEBIAS (RichEdit. h)
description: Définit le décalage du mode Text Services Framework (TSF) pour un contrôle RichEdit.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509173"
---
# <a name="em_setctfmodebias-message"></a><span data-ttu-id="acf30-104">\_Message SETCTFMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="acf30-104">EM\_SETCTFMODEBIAS message</span></span>

<span data-ttu-id="acf30-105">Définit le décalage du mode Text Services Framework (TSF) pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="acf30-105">Sets the Text Services Framework (TSF) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="acf30-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acf30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf30-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acf30-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acf30-108">Valeur de décalage du mode.</span><span class="sxs-lookup"><span data-stu-id="acf30-108">Mode bias value.</span></span> <span data-ttu-id="acf30-109">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="acf30-109">This can be one of the following values.</span></span>



| <span data-ttu-id="acf30-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="acf30-110">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="acf30-111">Signification</span><span class="sxs-lookup"><span data-stu-id="acf30-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <span data-ttu-id="acf30-112"><dt>**CTFMODEBIAS \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-112"><dt>**CTFMODEBIAS\_DEFAULT**</dt></span></span> </dl>                                           | <span data-ttu-id="acf30-113">Il n’y a pas de décalage de mode.</span><span class="sxs-lookup"><span data-stu-id="acf30-113">There is no mode bias.</span></span><br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <span data-ttu-id="acf30-114"><dt>**\_nom de fichier CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-114"><dt>**CTFMODEBIAS\_FILENAME**</dt></span></span> </dl>                                        | <span data-ttu-id="acf30-115">Le décalage est vers un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="acf30-115">The bias is to a filename.</span></span><br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <span data-ttu-id="acf30-116"><dt>**nom de CTFMODEBIAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-116"><dt>**CTFMODEBIAS\_NAME**</dt></span></span> </dl>                                                    | <span data-ttu-id="acf30-117">Le biais correspond à un nom.</span><span class="sxs-lookup"><span data-stu-id="acf30-117">The bias is to a name.</span></span><br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <span data-ttu-id="acf30-118"><dt>**\_lecture CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-118"><dt>**CTFMODEBIAS\_READING**</dt></span></span> </dl>                                           | <span data-ttu-id="acf30-119">Le décalage concerne la lecture.</span><span class="sxs-lookup"><span data-stu-id="acf30-119">The bias is to the reading.</span></span><br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <span data-ttu-id="acf30-120"><dt>**CTFMODEBIAS \_ DateTime**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-120"><dt>**CTFMODEBIAS\_DATETIME**</dt></span></span> </dl>                                        | <span data-ttu-id="acf30-121">L’écart concerne une date ou une heure.</span><span class="sxs-lookup"><span data-stu-id="acf30-121">The bias is to a date or time.</span></span><br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <span data-ttu-id="acf30-122"><dt>**\_conversation CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-122"><dt>**CTFMODEBIAS\_CONVERSATION**</dt></span></span> </dl>                            | <span data-ttu-id="acf30-123">Le décalage concerne une conversation.</span><span class="sxs-lookup"><span data-stu-id="acf30-123">The bias is to a conversation.</span></span><br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <span data-ttu-id="acf30-124"><dt>**CTFMODEBIAS \_ numérique**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-124"><dt>**CTFMODEBIAS\_NUMERIC**</dt></span></span> </dl>                                           | <span data-ttu-id="acf30-125">Le biais est un nombre.</span><span class="sxs-lookup"><span data-stu-id="acf30-125">The bias is to a number.</span></span><br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <span data-ttu-id="acf30-126"><dt>**CTFMODEBIAS \_ hiragana**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-126"><dt>**CTFMODEBIAS\_HIRAGANA**</dt></span></span> </dl>                                        | <span data-ttu-id="acf30-127">Le décalage est vers des chaînes Hiragana.</span><span class="sxs-lookup"><span data-stu-id="acf30-127">The bias is to hiragana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <span data-ttu-id="acf30-128"><dt>**CTFMODEBIAS \_ Katakana**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-128"><dt>**CTFMODEBIAS\_KATAKANA**</dt></span></span> </dl>                                        | <span data-ttu-id="acf30-129">Le décalage est le biais des chaînes Katakana.</span><span class="sxs-lookup"><span data-stu-id="acf30-129">The bias is to katakana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <span data-ttu-id="acf30-130"><dt>**\_HANGUL CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-130"><dt>**CTFMODEBIAS\_HANGUL**</dt></span></span> </dl>                                              | <span data-ttu-id="acf30-131">Le décalage concerne les caractères Hangul.</span><span class="sxs-lookup"><span data-stu-id="acf30-131">The bias is to Hangul characters.</span></span><br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <span data-ttu-id="acf30-132"><dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-132"><dt>**CTFMODEBIAS\_HALFWIDTHKATAKANA**</dt></span></span> </dl>             | <span data-ttu-id="acf30-133">Le décalage est vers les chaînes katakana à demi-chasse.</span><span class="sxs-lookup"><span data-stu-id="acf30-133">The bias is to half-width katakana strings.</span></span><br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <span data-ttu-id="acf30-134"><dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-134"><dt>**CTFMODEBIAS\_FULLWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="acf30-135">L’écart est de caractères alphanumériques à pleine chasse.</span><span class="sxs-lookup"><span data-stu-id="acf30-135">The bias is to full-width alphanumeric characters.</span></span><br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <span data-ttu-id="acf30-136"><dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-136"><dt>**CTFMODEBIAS\_HALFWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="acf30-137">Le décalage se fait en caractères alphanumériques à demi-chasse.</span><span class="sxs-lookup"><span data-stu-id="acf30-137">The bias is to half-width alphanumeric characters.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="acf30-138">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acf30-138">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acf30-139">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="acf30-139">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf30-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acf30-140">Return value</span></span>

<span data-ttu-id="acf30-141">En cas de réussite, la valeur de retour est la nouvelle valeur de biais du mode TSF.</span><span class="sxs-lookup"><span data-stu-id="acf30-141">If successful, the return value is the new TSF mode bias value.</span></span> <span data-ttu-id="acf30-142">En cas d’échec, la valeur de retour est l’ancienne valeur de biais du mode TSF.</span><span class="sxs-lookup"><span data-stu-id="acf30-142">If unsuccessful, the return value is the old TSF mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf30-143">Notes</span><span class="sxs-lookup"><span data-stu-id="acf30-143">Remarks</span></span>

<span data-ttu-id="acf30-144">Quand une application RichEdit (Microsoft Rich Edit) utilise TSF, elle peut sélectionner le biais du mode TSF.</span><span class="sxs-lookup"><span data-stu-id="acf30-144">When a Microsoft Rich Edit application uses TSF, it can select the TSF mode bias.</span></span> <span data-ttu-id="acf30-145">Ce message définit les critères selon lesquels un autre choix apparaît en haut de la liste pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="acf30-145">This message sets the criteria by which an alternative choice appears at the top of the list for selection.</span></span>

<span data-ttu-id="acf30-146">Pour définir le décalage de mode pour l’éditeur de méthode d’entrée (IME), utilisez [**em \_ SETIMEMODEBIAS**](em-setimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="acf30-146">To set the mode bias for the Input Method Editor (IME), use [**EM\_SETIMEMODEBIAS**](em-setimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acf30-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acf30-147">Requirements</span></span>



| <span data-ttu-id="acf30-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acf30-148">Requirement</span></span> | <span data-ttu-id="acf30-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="acf30-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acf30-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acf30-150">Minimum supported client</span></span><br/> | <span data-ttu-id="acf30-151">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acf30-151">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acf30-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acf30-152">Minimum supported server</span></span><br/> | <span data-ttu-id="acf30-153">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acf30-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acf30-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="acf30-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="acf30-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="acf30-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf30-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acf30-156">See also</span></span>

<dl> <dt>

<span data-ttu-id="acf30-157">**Référence**</span><span class="sxs-lookup"><span data-stu-id="acf30-157">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="acf30-158">**\_GETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="acf30-158">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="acf30-159">**\_SETIMEMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="acf30-159">**EM\_SETIMEMODEBIAS**</span></span>](em-setimemodebias.md)
</dt> </dl>

 

 





