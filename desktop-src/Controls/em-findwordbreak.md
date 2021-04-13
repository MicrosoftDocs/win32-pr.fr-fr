---
title: Message EM_FINDWORDBREAK (RichEdit. h)
description: Recherche la prochaine césure de mot avant ou après la position de caractère spécifiée ou récupère des informations sur le caractère à cette position.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465578"
---
# <a name="em_findwordbreak-message"></a><span data-ttu-id="6be47-104">\_Message FINDWORDBREAK em</span><span class="sxs-lookup"><span data-stu-id="6be47-104">EM\_FINDWORDBREAK message</span></span>

<span data-ttu-id="6be47-105">Recherche la prochaine césure de mot avant ou après la position de caractère spécifiée ou récupère des informations sur le caractère à cette position.</span><span class="sxs-lookup"><span data-stu-id="6be47-105">Finds the next word break before or after the specified character position or retrieves information about the character at that position.</span></span>

## <a name="parameters"></a><span data-ttu-id="6be47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6be47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be47-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6be47-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6be47-108">Spécifie l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="6be47-108">Specifies the find operation.</span></span> <span data-ttu-id="6be47-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6be47-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6be47-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6be47-110">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="6be47-111">Signification</span><span class="sxs-lookup"><span data-stu-id="6be47-111">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <span data-ttu-id="6be47-112"><dt>**WB \_ classifier**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-112"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>                | <span data-ttu-id="6be47-113">Retourne la classe de caractères et les indicateurs de saut de mot du caractère à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6be47-113">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <span data-ttu-id="6be47-114"><dt>**WB \_ ISDELIMITER**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-114"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl>       | <span data-ttu-id="6be47-115">Retourne la **valeur true** si le caractère situé à la position spécifiée est un délimiteur, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6be47-115">Returns **TRUE** if the character at the specified position is a delimiter, or **FALSE** otherwise.</span></span><br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <span data-ttu-id="6be47-116"><dt>**WB \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-116"><dt>**WB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="6be47-117">Recherche le caractère le plus proche avant la position spécifiée qui commence un mot.</span><span class="sxs-lookup"><span data-stu-id="6be47-117">Finds the nearest character before the specified position that begins a word.</span></span><br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <span data-ttu-id="6be47-118"><dt>**WB \_ LEFTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-118"><dt>**WB\_LEFTBREAK**</dt></span></span> </dl>             | <span data-ttu-id="6be47-119">Recherche le mot suivant à la fin de la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6be47-119">Finds the next word end before the specified position.</span></span> <span data-ttu-id="6be47-120">Cette valeur est identique à celle de WB \_ PREVBREAK.</span><span class="sxs-lookup"><span data-stu-id="6be47-120">This value is the same as WB\_PREVBREAK.</span></span><br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <span data-ttu-id="6be47-121"><dt>**WB \_ MOVEWORDLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-121"><dt>**WB\_MOVEWORDLEFT**</dt></span></span> </dl>    | <span data-ttu-id="6be47-122">Recherche le caractère suivant qui commence un mot avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6be47-122">Finds the next character that begins a word before the specified position.</span></span> <span data-ttu-id="6be47-123">Cette valeur est utilisée pendant le traitement des touches CTRL + Flèche gauche.</span><span class="sxs-lookup"><span data-stu-id="6be47-123">This value is used during CTRL+LEFT ARROW key processing.</span></span> <span data-ttu-id="6be47-124">Cette valeur est similaire à celle de WB \_ MOVEWORDPREV.</span><span class="sxs-lookup"><span data-stu-id="6be47-124">This value is the similar to WB\_MOVEWORDPREV.</span></span> <span data-ttu-id="6be47-125">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6be47-125">See Remarks for more information.</span></span><br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <span data-ttu-id="6be47-126"><dt>**WB \_ MOVEWORDRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-126"><dt>**WB\_MOVEWORDRIGHT**</dt></span></span> </dl> | <span data-ttu-id="6be47-127">Recherche le caractère suivant qui commence un mot après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6be47-127">Finds the next character that begins a word after the specified position.</span></span> <span data-ttu-id="6be47-128">Cette valeur est utilisée pendant le traitement de la touche CTRL + droite.</span><span class="sxs-lookup"><span data-stu-id="6be47-128">This value is used during CTRL+right key processing.</span></span> <span data-ttu-id="6be47-129">Cette valeur est similaire à celle de WB \_ MOVEWORDNEXT.</span><span class="sxs-lookup"><span data-stu-id="6be47-129">This value is similar to WB\_MOVEWORDNEXT.</span></span> <span data-ttu-id="6be47-130">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6be47-130">See Remarks for more information.</span></span><br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <span data-ttu-id="6be47-131"><dt>**WB à \_ droite**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-131"><dt>**WB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="6be47-132">Recherche le caractère suivant qui commence un mot après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6be47-132">Finds the next character that begins a word after the specified position.</span></span><br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <span data-ttu-id="6be47-133"><dt>**WB \_ RIGHTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-133"><dt>**WB\_RIGHTBREAK**</dt></span></span> </dl>          | <span data-ttu-id="6be47-134">Recherche le délimiteur de fin de mot suivant après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6be47-134">Finds the next end-of-word delimiter after the specified position.</span></span> <span data-ttu-id="6be47-135">Cette valeur est identique à celle de WB \_ NEXTBREAK.</span><span class="sxs-lookup"><span data-stu-id="6be47-135">This value is the same as WB\_NEXTBREAK.</span></span><br/>                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="6be47-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6be47-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6be47-137">Position de départ d’un caractère de base zéro.</span><span class="sxs-lookup"><span data-stu-id="6be47-137">Zero-based character starting position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be47-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6be47-138">Return value</span></span>

<span data-ttu-id="6be47-139">Le message retourne une valeur basée sur le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6be47-139">The message returns a value based on the *wParam* parameter.</span></span>



| <span data-ttu-id="6be47-140">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6be47-140">Return code</span></span>                                                                                    | <span data-ttu-id="6be47-141">Description</span><span class="sxs-lookup"><span data-stu-id="6be47-141">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6be47-142"><dt>**wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-142"><dt>**wParam**</dt></span></span> </dl>          | <span data-ttu-id="6be47-143">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6be47-143">Return Value</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6be47-144"><dt>**WB \_ classifier**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-144"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>    | <span data-ttu-id="6be47-145">Retourne la classe de caractères et les indicateurs de saut de mot du caractère à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6be47-145">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                |
| <dl> <span data-ttu-id="6be47-146"><dt>**WB \_ ISDELIMITER**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-146"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl> | <span data-ttu-id="6be47-147">Retourne la **valeur true** si le caractère situé à la position spécifiée est un délimiteur. Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="6be47-147">Returns **TRUE** if the character at the specified position is a delimiter; otherwise it returns **FALSE**.</span></span><br/> |
| <dl> <span data-ttu-id="6be47-148"><dt>**Autres**</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-148"><dt>**Others**</dt></span></span> </dl>          | <span data-ttu-id="6be47-149">Retourne l’index de caractère de l’arrêt de mot.</span><span class="sxs-lookup"><span data-stu-id="6be47-149">Returns the character index of the word break.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6be47-150">Notes</span><span class="sxs-lookup"><span data-stu-id="6be47-150">Remarks</span></span>

<span data-ttu-id="6be47-151">Si *wParam* est WB \_ Left et WB \_ Right, la procédure de saut de mot recherche les césures de mots uniquement après les délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="6be47-151">If *wParam* is WB\_LEFT and WB\_RIGHT, the word-break procedure finds word breaks only after delimiters.</span></span> <span data-ttu-id="6be47-152">Cela correspond à la fonctionnalité d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="6be47-152">This matches the functionality of an edit control.</span></span> <span data-ttu-id="6be47-153">Si *wParam* est WB \_ MOVEWORDLEFT ou WB \_ MOVEWORDRIGHT, la procédure de césure de mots compare également les classes de caractères et les indicateurs de césure lexicale.</span><span class="sxs-lookup"><span data-stu-id="6be47-153">If *wParam* is WB\_MOVEWORDLEFT or WB\_MOVEWORDRIGHT, the word-break procedure also compares character classes and word-break flags.</span></span>

<span data-ttu-id="6be47-154">Pour plus d’informations sur les classes de caractères et les indicateurs de césure lexicale, consultez [mots et sauts de ligne](using-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6be47-154">For information about character classes and word-break flags, see [Word and Line Breaks](using-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6be47-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6be47-155">Requirements</span></span>



| <span data-ttu-id="6be47-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6be47-156">Requirement</span></span> | <span data-ttu-id="6be47-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="6be47-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6be47-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6be47-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6be47-159">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6be47-159">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6be47-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6be47-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6be47-161">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6be47-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6be47-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="6be47-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="6be47-163"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6be47-163"><dt>Richedit.h</dt></span></span> </dl> |



 

 





