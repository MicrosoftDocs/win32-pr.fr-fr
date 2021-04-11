---
title: Message EM_SETCHARFORMAT (RichEdit. h)
description: Définit la mise en forme des caractères dans un contrôle RichEdit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105586"
---
# <a name="em_setcharformat-message"></a><span data-ttu-id="1d55a-104">\_Message SETCHARFORMAT em</span><span class="sxs-lookup"><span data-stu-id="1d55a-104">EM\_SETCHARFORMAT message</span></span>

<span data-ttu-id="1d55a-105">Définit la mise en forme des caractères dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="1d55a-105">Sets character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d55a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d55a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d55a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d55a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d55a-108">Mise en forme des caractères qui s’applique au contrôle.</span><span class="sxs-lookup"><span data-stu-id="1d55a-108">Character formatting that applies to the control.</span></span> <span data-ttu-id="1d55a-109">Si ce paramètre est égal à zéro, le format de caractère par défaut est défini.</span><span class="sxs-lookup"><span data-stu-id="1d55a-109">If this parameter is zero, the default character format is set.</span></span> <span data-ttu-id="1d55a-110">Dans le cas contraire, il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d55a-110">Otherwise, it can be one of the following values.</span></span>



| <span data-ttu-id="1d55a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d55a-111">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="1d55a-112">Signification</span><span class="sxs-lookup"><span data-stu-id="1d55a-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <span data-ttu-id="1d55a-113"><dt>**CSAH \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-113"><dt>**SCF\_ALL**</dt></span></span> </dl>                                     | <span data-ttu-id="1d55a-114">Applique la mise en forme à tout le texte du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1d55a-114">Applies the formatting to all text in the control.</span></span> <span data-ttu-id="1d55a-115">Non valide avec **la \_ sélection SCF** ou le **\_ mot SCF**.</span><span class="sxs-lookup"><span data-stu-id="1d55a-115">Not valid with **SCF\_SELECTION** or **SCF\_WORD**.</span></span><br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <span data-ttu-id="1d55a-116"><dt>**CSAH \_ ASSOCIATEFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-116"><dt>**SCF\_ASSOCIATEFONT**</dt></span></span> </dl>       | <span data-ttu-id="1d55a-117">**RichEdit 4,1 :** Associe une police à un script donné, modifiant ainsi la police par défaut pour ce script.</span><span class="sxs-lookup"><span data-stu-id="1d55a-117">**RichEdit 4.1:** Associates a font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="1d55a-118">Pour spécifier la police, utilisez les membres suivants de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** et **LCID**.</span><span class="sxs-lookup"><span data-stu-id="1d55a-118">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <span data-ttu-id="1d55a-119"><dt>**CSAH \_ ASSOCIATEFONT2**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-119"><dt>**SCF\_ASSOCIATEFONT2**</dt></span></span> </dl>    | <span data-ttu-id="1d55a-120">**RichEdit 4,1 :** Associe une police de substitution (plan-2) à un script donné, modifiant ainsi la police par défaut pour ce script.</span><span class="sxs-lookup"><span data-stu-id="1d55a-120">**RichEdit 4.1:** Associates a surrogate (plane-2) font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="1d55a-121">Pour spécifier la police, utilisez les membres suivants de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** et **LCID**.</span><span class="sxs-lookup"><span data-stu-id="1d55a-121">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <span data-ttu-id="1d55a-122"><dt>**CSAH \_ CHARREPFROMLCID**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-122"><dt>**SCF\_CHARREPFROMLCID**</dt></span></span> </dl> | <span data-ttu-id="1d55a-123">Obtient le répertoire de caractères à partir du LCID.</span><span class="sxs-lookup"><span data-stu-id="1d55a-123">Gets the character repertoire from the LCID.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="1d55a-124"><dt>**CSAH \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-124"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>                         | <span data-ttu-id="1d55a-125">**RichEdit 4,1 :** Définit la police par défaut pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="1d55a-125">**RichEdit 4.1:** Sets the default font for the control.</span></span> <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <span data-ttu-id="1d55a-126"><dt>**\_DONTSETDEFAULT SPF**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-126"><dt>**SPF\_DONTSETDEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="1d55a-127">Empêche de définir le format de paragraphe par défaut lorsque le contrôle RichEdit est vide.</span><span class="sxs-lookup"><span data-stu-id="1d55a-127">Prevents setting the default paragraph format when the rich edit control is empty.</span></span><br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <span data-ttu-id="1d55a-128"><dt>**CSAH \_ NOKBUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-128"><dt>**SCF\_NOKBUPDATE**</dt></span></span> </dl>                | <span data-ttu-id="1d55a-129">**RichEdit 4,1 :** Empêche le changement de clavier de correspondre à la police.</span><span class="sxs-lookup"><span data-stu-id="1d55a-129">**RichEdit 4.1:** Prevents keyboard switching to match the font.</span></span> <span data-ttu-id="1d55a-130">Par exemple, si une police arabe est définie, normalement la fonctionnalité de clavier automatique pour les langues bidi remplace le clavier par un clavier arabe.</span><span class="sxs-lookup"><span data-stu-id="1d55a-130">For example, if an Arabic font is set, normally the automatic keyboard feature for Bidi languages changes the keyboard to an Arabic keyboard.</span></span><br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="1d55a-131"><dt>**\_sélection SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-131"><dt>**SCF\_SELECTION**</dt></span></span> </dl>                   | <span data-ttu-id="1d55a-132">Applique la mise en forme à la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="1d55a-132">Applies the formatting to the current selection.</span></span> <span data-ttu-id="1d55a-133">Si la sélection est vide, la mise en forme des caractères est appliquée au point d’insertion et le nouveau format de caractère est en vigueur uniquement jusqu’à ce que le point d’insertion soit modifié.</span><span class="sxs-lookup"><span data-stu-id="1d55a-133">If the selection is empty, the character formatting is applied to the insertion point, and the new character format is in effect only until the insertion point changes.</span></span><br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <span data-ttu-id="1d55a-134"><dt>**de SPF \_ SETDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-134"><dt>**SPF\_SETDEFAULT**</dt></span></span> </dl>                | <span data-ttu-id="1d55a-135">Définit les attributs de mise en forme par défaut des paragraphes.</span><span class="sxs-lookup"><span data-stu-id="1d55a-135">Sets the default paragraph formatting attributes.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <span data-ttu-id="1d55a-136"><dt>**CSAH \_ SMARTFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-136"><dt>**SCF\_SMARTFONT**</dt></span></span> </dl>                   | <span data-ttu-id="1d55a-137">Appliquez la police uniquement si elle peut gérer le script.</span><span class="sxs-lookup"><span data-stu-id="1d55a-137">Apply the font only if it can handle script.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <span data-ttu-id="1d55a-138"><dt>**CSAH \_ USEUIRULES**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-138"><dt>**SCF\_USEUIRULES**</dt></span></span> </dl>                | <span data-ttu-id="1d55a-139">**RichEdit 4,1 :** Utilisé avec **la \_ sélection SCF**.</span><span class="sxs-lookup"><span data-stu-id="1d55a-139">**RichEdit 4.1:** Used with **SCF\_SELECTION**.</span></span> <span data-ttu-id="1d55a-140">Indique que le format provient d’une barre d’outils ou d’un autre outil d’interface utilisateur. les règles de mise en forme de l’interface utilisateur doivent donc être utilisées à la place de la mise en forme littérale</span><span class="sxs-lookup"><span data-stu-id="1d55a-140">Indicates that format came from a toolbar or other UI tool, so UI formatting rules should be used instead of literal formatting.</span></span><br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <span data-ttu-id="1d55a-141"><dt>**\_mot SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-141"><dt>**SCF\_WORD**</dt></span></span> </dl>                                  | <span data-ttu-id="1d55a-142">Applique la mise en forme au ou aux mots sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="1d55a-142">Applies the formatting to the selected word or words.</span></span> <span data-ttu-id="1d55a-143">Si la sélection est vide, mais que le point d’insertion se trouve à l’intérieur d’un mot, la mise en forme est appliquée au mot.</span><span class="sxs-lookup"><span data-stu-id="1d55a-143">If the selection is empty but the insertion point is inside a word, the formatting is applied to the word.</span></span> <span data-ttu-id="1d55a-144">La valeur du **\_ mot SCF** doit être utilisée conjointement avec la valeur de **\_ sélection SCF** .</span><span class="sxs-lookup"><span data-stu-id="1d55a-144">The **SCF\_WORD** value must be used in conjunction with the **SCF\_SELECTION** value.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="1d55a-145">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d55a-145">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d55a-146">Pointeur vers une structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) spécifiant la mise en forme des caractères à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1d55a-146">Pointer to a [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure specifying the character formatting to use.</span></span> <span data-ttu-id="1d55a-147">Seuls les attributs de mise en forme spécifiés par le membre **dwMask** sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="1d55a-147">Only the formatting attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="1d55a-148">Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , qui est une extension de la structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="1d55a-148">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="1d55a-149">Avant d’envoyer le message **\_ SETCHARFORMAT em** , définissez le membre **cbSize** de la structure sur `sizeof(CHARFORMAT)` ou `sizeof(CHARFORMAT2)` Indiquez la version de la structure utilisée.</span><span class="sxs-lookup"><span data-stu-id="1d55a-149">Before sending the **EM\_SETCHARFORMAT** message, set the structure's **cbSize** member to `sizeof(CHARFORMAT)` or `sizeof(CHARFORMAT2)` indicate which version of the structure is being used.</span></span>

<span data-ttu-id="1d55a-150">Les membres **szFaceName** et **bCharSet** peuvent être remplacés lorsqu’ils ne sont pas valides pour les caractères, par exemple : Arial sur les caractères Kanji.</span><span class="sxs-lookup"><span data-stu-id="1d55a-150">The **szFaceName** and **bCharSet** members may be overruled when invalid for characters, for example: Arial on kanji characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d55a-151">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d55a-151">Return value</span></span>

<span data-ttu-id="1d55a-152">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="1d55a-152">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1d55a-153">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="1d55a-153">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d55a-154">Notes</span><span class="sxs-lookup"><span data-stu-id="1d55a-154">Remarks</span></span>

<span data-ttu-id="1d55a-155">Si ce message est envoyé plusieurs fois avec les mêmes paramètres, l’effet sur le texte est basculé.</span><span class="sxs-lookup"><span data-stu-id="1d55a-155">If this message is sent more than once with the same parameters, the effect on the text is toggled.</span></span> <span data-ttu-id="1d55a-156">Autrement dit, l’envoi du message une fois produit l’effet, l’envoi du message à deux reprises annule l’effet, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="1d55a-156">That is, sending the message once produces the effect, sending the message twice cancels the effect, and so forth.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d55a-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d55a-157">Requirements</span></span>



| <span data-ttu-id="1d55a-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d55a-158">Requirement</span></span> | <span data-ttu-id="1d55a-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d55a-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d55a-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d55a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1d55a-161">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d55a-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d55a-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d55a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1d55a-163">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d55a-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d55a-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d55a-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d55a-165"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d55a-165"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d55a-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d55a-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d55a-167">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1d55a-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d55a-168">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="1d55a-168">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="1d55a-169">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="1d55a-169">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





