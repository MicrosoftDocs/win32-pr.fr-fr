---
title: Message EM_GETIMEPROPERTY (RichEdit. h)
description: Récupère la propriété et les fonctionnalités de l’éditeur de méthode d’entrée (IME) associé aux paramètres régionaux d’entrée actuels.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105124"
---
# <a name="em_getimeproperty-message"></a><span data-ttu-id="30873-104">\_Message GETIMEPROPERTY em</span><span class="sxs-lookup"><span data-stu-id="30873-104">EM\_GETIMEPROPERTY message</span></span>

<span data-ttu-id="30873-105">Récupère la propriété et les fonctionnalités de l’éditeur de méthode d’entrée (IME) associé aux paramètres régionaux d’entrée actuels.</span><span class="sxs-lookup"><span data-stu-id="30873-105">Retrieves the property and capabilities of the Input Method Editor (IME) associated with the current input locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="30873-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30873-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30873-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30873-108">Spécifie le type d’informations de propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="30873-108">Specifies the type of property information to retrieve.</span></span> <span data-ttu-id="30873-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="30873-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="30873-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="30873-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="30873-111">Signification</span><span class="sxs-lookup"><span data-stu-id="30873-111">Meaning</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <span data-ttu-id="30873-112"><dt>**\_propriété IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="30873-112"><dt>**IGP\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="30873-113">Informations sur les propriétés.</span><span class="sxs-lookup"><span data-stu-id="30873-113">Property information.</span></span><br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <span data-ttu-id="30873-114"><dt>**\_conversion IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="30873-114"><dt>**IGP\_CONVERSION**</dt></span></span> </dl>          | <span data-ttu-id="30873-115">Fonctionnalités de conversion.</span><span class="sxs-lookup"><span data-stu-id="30873-115">Conversion capabilities.</span></span> <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <span data-ttu-id="30873-116"><dt>**\_phrase IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="30873-116"><dt>**IGP\_SENTENCE**</dt></span></span> </dl>                | <span data-ttu-id="30873-117">Fonctionnalités du mode phrase.</span><span class="sxs-lookup"><span data-stu-id="30873-117">Sentence mode capabilities.</span></span> <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <span data-ttu-id="30873-118"><dt>**\_interface utilisateur IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="30873-118"><dt>**IGP\_UI**</dt></span></span> </dl>                                  | <span data-ttu-id="30873-119">Fonctionnalités de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30873-119">User interface capabilities.</span></span> <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <span data-ttu-id="30873-120"><dt>**IGP \_ SETCOMPSTR**</dt></span><span class="sxs-lookup"><span data-stu-id="30873-120"><dt>**IGP\_SETCOMPSTR**</dt></span></span> </dl>          | <span data-ttu-id="30873-121">Fonctionnalités de la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="30873-121">Composition string capabilities.</span></span> <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <span data-ttu-id="30873-122"><dt>**IGP, \_ Sélectionner**</dt></span><span class="sxs-lookup"><span data-stu-id="30873-122"><dt>**IGP\_SELECT**</dt></span></span> </dl>                      | <span data-ttu-id="30873-123">Fonctionnalités d’héritage de la sélection.</span><span class="sxs-lookup"><span data-stu-id="30873-123">Selection inheritance capabilities.</span></span> <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <span data-ttu-id="30873-124"><dt>**IGP \_ GETIMEVERSION**</dt></span><span class="sxs-lookup"><span data-stu-id="30873-124"><dt>**IGP\_GETIMEVERSION**</dt></span></span> </dl> | <span data-ttu-id="30873-125">Récupère le numéro de version du système pour lequel l’IME spécifié a été créé.</span><span class="sxs-lookup"><span data-stu-id="30873-125">Retrieves the system version number for which the specified IME was created.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="30873-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30873-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30873-127">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="30873-127">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30873-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30873-128">Return value</span></span>

<span data-ttu-id="30873-129">Retourne la valeur de la propriété ou de la fonctionnalité, selon la valeur du paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="30873-129">Returns the property or capability value, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="30873-130">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="30873-130">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="30873-131">Notes</span><span class="sxs-lookup"><span data-stu-id="30873-131">Remarks</span></span>

<span data-ttu-id="30873-132">Si *wParam* est \_ la propriété IGP, elle retourne une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="30873-132">If *wParam* is IGP\_PROPERTY, it returns one or more of the following values.</span></span>



| <span data-ttu-id="30873-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30873-133">Requirement</span></span> | <span data-ttu-id="30873-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="30873-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30873-135">\_prop IME \_ au \_ signe insertion</span><span class="sxs-lookup"><span data-stu-id="30873-135">IME\_PROP\_AT\_CARET</span></span>                | <span data-ttu-id="30873-136">Si cette valeur est définie, la fenêtre de conversion se trouve à l’emplacement du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="30873-136">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="30873-137">Si cette case est désactivée, la fenêtre est proche de la position du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="30873-137">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="30873-138">\_ \_ interface utilisateur spéciale prop IME \_</span><span class="sxs-lookup"><span data-stu-id="30873-138">IME\_PROP\_SPECIAL\_UI</span></span>              | <span data-ttu-id="30873-139">S’il est défini, l’éditeur IME a une interface utilisateur non standard.</span><span class="sxs-lookup"><span data-stu-id="30873-139">If set, IME has a nonstandard user interface.</span></span> <span data-ttu-id="30873-140">L’application ne doit pas être dessinée dans la fenêtre IME.</span><span class="sxs-lookup"><span data-stu-id="30873-140">The application should not draw in the IME window.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="30873-141">\_ \_ CANDLIST du prop IME \_ Démarrer \_ à partir de \_ 1</span><span class="sxs-lookup"><span data-stu-id="30873-141">IME\_PROP\_CANDLIST\_START\_FROM\_1</span></span> | <span data-ttu-id="30873-142">Si cette valeur est définie, les chaînes de la liste candidate sont numérotées à partir de 1.</span><span class="sxs-lookup"><span data-stu-id="30873-142">If set, strings in the candidate list are numbered starting at 1.</span></span> <span data-ttu-id="30873-143">Si la valeur est Clear, les chaînes commencent à zéro.</span><span class="sxs-lookup"><span data-stu-id="30873-143">If clear, strings start at zero.</span></span>                                                                                                                                                                |
| <span data-ttu-id="30873-144">\_Unicode prop \_ Unicode</span><span class="sxs-lookup"><span data-stu-id="30873-144">IME\_PROP\_UNICODE</span></span>                  | <span data-ttu-id="30873-145">Si cette valeur est définie, l’IME est affiché en tant que UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="30873-145">If set, the IME is viewed as a UnicodeIME.</span></span> <span data-ttu-id="30873-146">Le système et l’IME communiquent par l’intermédiaire de l’interface UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="30873-146">The system and the IME will communicate through the UnicodeIME interface.</span></span> <span data-ttu-id="30873-147">Si la valeur est Clear, IME utilise l’interface ANSI pour communiquer avec le système.</span><span class="sxs-lookup"><span data-stu-id="30873-147">If clear, IME will use the ANSI interface to communicate with the system.</span></span>                                                                    |
| <span data-ttu-id="30873-148">la \_ prop IME est \_ terminée \_ lors de la \_ désélection</span><span class="sxs-lookup"><span data-stu-id="30873-148">IME\_PROP\_COMPLETE\_ON\_UNSELECT</span></span>   | <span data-ttu-id="30873-149">Si cette valeur est définie, la fenêtre de conversion se trouve à l’emplacement du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="30873-149">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="30873-150">Si cette case est désactivée, la fenêtre est proche de la position du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="30873-150">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="30873-151">IME \_ prop \_ Accept \_ \_ VKEY</span><span class="sxs-lookup"><span data-stu-id="30873-151">IME\_PROP\_ACCEPT\_WIDE\_VKEY</span></span>       | <span data-ttu-id="30873-152">Si cette valeur est définie, l’IME traite le Unicode injecté qui provient de la fonction [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) à l’aide du \_ paquet VK.</span><span class="sxs-lookup"><span data-stu-id="30873-152">If set, the IME processes the injected Unicode that came from the [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) function by using VK\_PACKET.</span></span> <span data-ttu-id="30873-153">Si elle est désactivée, l’IME peut ne pas traiter le Unicode injecté et le Unicode injecté peut être envoyé directement à l’application.</span><span class="sxs-lookup"><span data-stu-id="30873-153">If clear, the IME might not process the injected Unicode, and the injected Unicode might be sent to the application directly.</span></span> |



 

<span data-ttu-id="30873-154">Si *wParam* est \_ une interface utilisateur IGP, elle retourne une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="30873-154">If *wParam* is IGP\_UI, it returns one or more of the following values.</span></span>



| <span data-ttu-id="30873-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30873-155">Requirement</span></span> | <span data-ttu-id="30873-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="30873-156">Value</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30873-157">Interface utilisateur \_ CAP \_ 2700</span><span class="sxs-lookup"><span data-stu-id="30873-157">UI\_CAP\_2700</span></span>   | <span data-ttu-id="30873-158">Prend en charge les valeurs d’échappement de texte 0 ou 2700.</span><span class="sxs-lookup"><span data-stu-id="30873-158">Supports text escapement values of 0 or 2700.</span></span> <span data-ttu-id="30873-159">Pour plus d’informations, consultez **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="30873-159">For more information, see **lfEscapement**.</span></span>             |
| <span data-ttu-id="30873-160">\_ROT90 Cap de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="30873-160">UI\_CAP\_ROT90</span></span>  | <span data-ttu-id="30873-161">Prend en charge les valeurs d’échappement de texte 0, 900, 1800 ou 2700.</span><span class="sxs-lookup"><span data-stu-id="30873-161">Supports text escapement values of 0, 900, 1800, or 2700.</span></span> <span data-ttu-id="30873-162">Pour plus d’informations, consultez **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="30873-162">For more information, see **lfEscapement**.</span></span> |
| <span data-ttu-id="30873-163">\_ROTANY Cap de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="30873-163">UI\_CAP\_ROTANY</span></span> | <span data-ttu-id="30873-164">Prend en charge toute valeur d’échappement de texte.</span><span class="sxs-lookup"><span data-stu-id="30873-164">Supports any text escapement value.</span></span> <span data-ttu-id="30873-165">Pour plus d’informations, consultez **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="30873-165">For more information, see **lfEscapement**.</span></span>                       |



 

<span data-ttu-id="30873-166">Si *wParam* est IGP \_ SETCOMPSTR, il retourne une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="30873-166">If *wParam* is IGP\_SETCOMPSTR, it returns one or more of the following values.</span></span>



| <span data-ttu-id="30873-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30873-167">Requirement</span></span> | <span data-ttu-id="30873-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="30873-168">Value</span></span> |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30873-169">SCS- \_ Cap \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="30873-169">SCS\_CAP\_COMPSTR</span></span>            | <span data-ttu-id="30873-170">Peut créer la chaîne de composition en appelant la fonction [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) avec la \_ valeur SCS SETSTR.</span><span class="sxs-lookup"><span data-stu-id="30873-170">Can create the composition string by calling the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with the SCS\_SETSTR value.</span></span>                                                      |
| <span data-ttu-id="30873-171">SCS- \_ Cap \_ MAKEREAD</span><span class="sxs-lookup"><span data-stu-id="30873-171">SCS\_CAP\_MAKEREAD</span></span>           | <span data-ttu-id="30873-172">Peut créer la chaîne de lecture à partir de la chaîne de composition correspondante lors de l’utilisation de la fonction [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) avec SCS \_ SETSTR et sans définir *lpRead*.</span><span class="sxs-lookup"><span data-stu-id="30873-172">Can create the reading string from corresponding composition string when using the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with SCS\_SETSTR and without setting *lpRead*.</span></span> |
| <span data-ttu-id="30873-173">SCS- \_ Cap \_ SETRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="30873-173">SCS\_CAP\_SETRECONVERTSTRING</span></span> | <span data-ttu-id="30873-174">Cet IME peut prendre en charge la reconversion.</span><span class="sxs-lookup"><span data-stu-id="30873-174">This IME can support reconversion.</span></span> <span data-ttu-id="30873-175">Utilisez [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) pour effectuer la reconversion.</span><span class="sxs-lookup"><span data-stu-id="30873-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) to do the reconversion.</span></span>                                                                             |



 

<span data-ttu-id="30873-176">Si *wParam* est IGP \_ , sélectionnez, il retourne une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="30873-176">If *wParam* is IGP\_SELECT, it returns one or more of the following values.</span></span>



| <span data-ttu-id="30873-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30873-177">Requirement</span></span> | <span data-ttu-id="30873-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="30873-178">Value</span></span> |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="30873-179">SÉLECTIONNER \_ un \_ CONVMODE Cap</span><span class="sxs-lookup"><span data-stu-id="30873-179">SELECT\_CAP\_CONVMODE</span></span> | <span data-ttu-id="30873-180">Hérite du mode de conversion lorsqu’un nouvel IME est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="30873-180">Inherits conversion mode when a new IME is selected.</span></span> |
| <span data-ttu-id="30873-181">SÉLECTIONNER \_ une \_ phrase d’extrémité</span><span class="sxs-lookup"><span data-stu-id="30873-181">SELECT\_CAP\_SENTENCE</span></span> | <span data-ttu-id="30873-182">Hérite du mode phrase lorsqu’un nouvel IME est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="30873-182">Inherits sentence mode when a new IME is selected.</span></span>   |



 

<span data-ttu-id="30873-183">Si *wParam* est IGP \_ GETIMEVERSION, il retourne une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="30873-183">If *wParam* is IGP\_GETIMEVERSION, it returns one or more of the following values.</span></span>



| <span data-ttu-id="30873-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30873-184">Requirement</span></span> | <span data-ttu-id="30873-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="30873-185">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="30873-186">JAMAIS \_ 0310</span><span class="sxs-lookup"><span data-stu-id="30873-186">IMEVER\_0310</span></span> | <span data-ttu-id="30873-187">L’IME a été créé pour Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="30873-187">The IME was created for Windows 3.1.</span></span>        |
| <span data-ttu-id="30873-188">JAMAIS \_ 0400</span><span class="sxs-lookup"><span data-stu-id="30873-188">IMEVER\_0400</span></span> | <span data-ttu-id="30873-189">L’IME a été créé pour Windows 95 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="30873-189">The IME was created for Windows 95 or later</span></span> |



 

<span data-ttu-id="30873-190">Ce message est semblable à [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), à ceci près qu’il utilise les paramètres régionaux d’entrée actuels.</span><span class="sxs-lookup"><span data-stu-id="30873-190">This message is similar to [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), except that it uses the current input locale.</span></span> <span data-ttu-id="30873-191">L’application doit appeler [**em \_ ISIME**](em-isime.md) avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="30873-191">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="30873-192">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30873-192">Requirements</span></span>



| <span data-ttu-id="30873-193">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30873-193">Requirement</span></span> | <span data-ttu-id="30873-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="30873-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30873-195">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30873-195">Minimum supported client</span></span><br/> | <span data-ttu-id="30873-196">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30873-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30873-197">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30873-197">Minimum supported server</span></span><br/> | <span data-ttu-id="30873-198">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30873-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30873-199">En-tête</span><span class="sxs-lookup"><span data-stu-id="30873-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="30873-200"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="30873-200"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30873-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30873-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="30873-202">**Référence**</span><span class="sxs-lookup"><span data-stu-id="30873-202">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30873-203">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="30873-203">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

<span data-ttu-id="30873-204">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="30873-204">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="30873-205">**ImmGetProperty**</span><span class="sxs-lookup"><span data-stu-id="30873-205">**ImmGetProperty**</span></span>](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

