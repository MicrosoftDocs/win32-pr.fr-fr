---
title: Message EM_SETTEXTMODE (RichEdit. h)
description: Définit le mode texte ou le niveau d’annulation d’un contrôle RichEdit. Le message échoue si le contrôle contient du texte.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942295"
---
# <a name="em_settextmode-message"></a><span data-ttu-id="ad12d-105">\_Message SETTEXTMODE em</span><span class="sxs-lookup"><span data-stu-id="ad12d-105">EM\_SETTEXTMODE message</span></span>

<span data-ttu-id="ad12d-106">Définit le mode texte ou le niveau d’annulation d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="ad12d-106">Sets the text mode or undo level of a rich edit control.</span></span> <span data-ttu-id="ad12d-107">Le message échoue si le contrôle contient du texte.</span><span class="sxs-lookup"><span data-stu-id="ad12d-107">The message fails if the control contains any text.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad12d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad12d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad12d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad12d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad12d-110">Une ou plusieurs valeurs du type d’énumération [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="ad12d-110">One or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="ad12d-111">Les valeurs spécifient les nouveaux paramètres pour le mode texte du contrôle et les paramètres de niveau d’annulation.</span><span class="sxs-lookup"><span data-stu-id="ad12d-111">The values specify the new settings for the control's text mode and undo level parameters.</span></span>

<span data-ttu-id="ad12d-112">Spécifiez l’une des valeurs suivantes pour définir le paramètre de mode texte.</span><span class="sxs-lookup"><span data-stu-id="ad12d-112">Specify one of the following values to set the text mode parameter.</span></span> <span data-ttu-id="ad12d-113">Si vous ne spécifiez pas de valeur de mode texte, le mode texte conserve son paramètre actuel.</span><span class="sxs-lookup"><span data-stu-id="ad12d-113">If you do not specify a text mode value, the text mode remains at its current setting.</span></span> 

| <span data-ttu-id="ad12d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad12d-114">Value</span></span>                                          | <span data-ttu-id="ad12d-115">Signification</span><span class="sxs-lookup"><span data-stu-id="ad12d-115">Meaning</span></span>                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad12d-116">**\_texte en clair**</span><span class="sxs-lookup"><span data-stu-id="ad12d-116">**TM\_PLAINTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="ad12d-117">Indique le mode texte brut, dans lequel le contrôle est similaire à un contrôle d’édition standard.</span><span class="sxs-lookup"><span data-stu-id="ad12d-117">Indicates plain text mode, in which the control is similar to a standard edit control.</span></span> <span data-ttu-id="ad12d-118">Pour plus d’informations sur le mode texte brut, consultez la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="ad12d-118">For more information about plain text mode, see the following Remarks section.</span></span> |
| [<span data-ttu-id="ad12d-119">**\_RTF TM**</span><span class="sxs-lookup"><span data-stu-id="ad12d-119">**TM\_RICHTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="ad12d-120">Indique le mode texte enrichi, dans lequel le contrôle possède une fonctionnalité de modification enrichie standard.</span><span class="sxs-lookup"><span data-stu-id="ad12d-120">Indicates rich text mode, in which the control has standard rich edit functionality.</span></span> <span data-ttu-id="ad12d-121">Le mode de texte enrichi est le paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad12d-121">Rich text mode is the default setting.</span></span>                                           |



 

<span data-ttu-id="ad12d-122">Spécifiez l’une des valeurs suivantes pour définir le paramètre de niveau d’annulation.</span><span class="sxs-lookup"><span data-stu-id="ad12d-122">Specify one of the following values to set the undo level parameter.</span></span> <span data-ttu-id="ad12d-123">Si vous ne spécifiez pas de valeur de niveau d’annulation, le niveau d’annulation reste le paramètre actuel.</span><span class="sxs-lookup"><span data-stu-id="ad12d-123">If you do not specify an undo level value, the undo level remains at its current setting.</span></span> 

| <span data-ttu-id="ad12d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad12d-124">Value</span></span>                                                      | <span data-ttu-id="ad12d-125">Signification</span><span class="sxs-lookup"><span data-stu-id="ad12d-125">Meaning</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad12d-126">**\_SINGLELEVELUNDO TM**</span><span class="sxs-lookup"><span data-stu-id="ad12d-126">**TM\_SINGLELEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="ad12d-127">Le contrôle permet à l’utilisateur d’annuler uniquement la dernière action qui peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="ad12d-127">The control allows the user to undo only the last action that can be undone.</span></span>                                                                                                       |
| [<span data-ttu-id="ad12d-128">**\_MULTILEVELUNDO TM**</span><span class="sxs-lookup"><span data-stu-id="ad12d-128">**TM\_MULTILEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="ad12d-129">Le contrôle prend en charge plusieurs opérations d’annulation.</span><span class="sxs-lookup"><span data-stu-id="ad12d-129">The control supports multiple undo operations.</span></span> <span data-ttu-id="ad12d-130">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad12d-130">This is the default setting.</span></span> <span data-ttu-id="ad12d-131">Utilisez le message [**em \_ SETUNDOLIMIT**](em-setundolimit.md) pour définir le nombre maximal d’actions d’annulation.</span><span class="sxs-lookup"><span data-stu-id="ad12d-131">Use the [**EM\_SETUNDOLIMIT**](em-setundolimit.md) message to set the maximum number of undo actions.</span></span> |



 

<span data-ttu-id="ad12d-132">Spécifiez l’une des valeurs suivantes pour définir le paramètre de page de codes.</span><span class="sxs-lookup"><span data-stu-id="ad12d-132">Specify one of the following values to set the code page parameter.</span></span> <span data-ttu-id="ad12d-133">Si vous ne spécifiez pas de valeur de page de codes, la page de codes conserve son paramètre actuel.</span><span class="sxs-lookup"><span data-stu-id="ad12d-133">If you do not specify an code page value, the code page remains at its current setting.</span></span> 

| <span data-ttu-id="ad12d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad12d-134">Value</span></span>                                                    | <span data-ttu-id="ad12d-135">Signification</span><span class="sxs-lookup"><span data-stu-id="ad12d-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad12d-136">**\_SINGLECODEPAGE TM**</span><span class="sxs-lookup"><span data-stu-id="ad12d-136">**TM\_SINGLECODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="ad12d-137">Le contrôle autorise uniquement le clavier anglais et un clavier correspondant au jeu de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad12d-137">The control only allows the English keyboard and a keyboard corresponding to the default character set.</span></span> <span data-ttu-id="ad12d-138">Par exemple, vous pouvez avoir des lettres grecque et anglais.</span><span class="sxs-lookup"><span data-stu-id="ad12d-138">For example, you could have Greek and English.</span></span> <span data-ttu-id="ad12d-139">Notez que cela empêche le texte Unicode d’entrer dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ad12d-139">Note that this prevents Unicode text from entering the control.</span></span> <span data-ttu-id="ad12d-140">Par exemple, utilisez cette valeur si un contrôle RichEdit doit être limité au texte ANSI.</span><span class="sxs-lookup"><span data-stu-id="ad12d-140">For example, use this value if a Rich Edit control must be restricted to ANSI text.</span></span> |
| [<span data-ttu-id="ad12d-141">**\_MULTICODEPAGE TM**</span><span class="sxs-lookup"><span data-stu-id="ad12d-141">**TM\_MULTICODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="ad12d-142">Le contrôle permet l’insertion de plusieurs pages de codes et de texte Unicode dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ad12d-142">The control allows multiple code pages and Unicode text into the control.</span></span> <span data-ttu-id="ad12d-143">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad12d-143">This is the default setting.</span></span>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="ad12d-144">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad12d-144">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad12d-145">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ad12d-145">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad12d-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad12d-146">Return value</span></span>

<span data-ttu-id="ad12d-147">Si le message est correctement exécuté, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="ad12d-147">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="ad12d-148">Si le message échoue, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ad12d-148">If the message fails, the return value is a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad12d-149">Notes</span><span class="sxs-lookup"><span data-stu-id="ad12d-149">Remarks</span></span>

<span data-ttu-id="ad12d-150">En mode de texte enrichi, un contrôle RichEdit offre des fonctionnalités de modification enrichies standard.</span><span class="sxs-lookup"><span data-stu-id="ad12d-150">In rich text mode, a rich edit control has standard rich edit functionality.</span></span> <span data-ttu-id="ad12d-151">Toutefois, en mode texte brut, le contrôle est similaire à un contrôle d’édition standard :</span><span class="sxs-lookup"><span data-stu-id="ad12d-151">However, in plain text mode, the control is similar to a standard edit control:</span></span>

-   <span data-ttu-id="ad12d-152">Le texte d’un contrôle de texte brut ne peut avoir qu’un seul format (par exemple, gras, Arial 10 PT).</span><span class="sxs-lookup"><span data-stu-id="ad12d-152">The text in a plain text control can have only one format (such as Bold, 10pt Arial).</span></span>
-   <span data-ttu-id="ad12d-153">L’utilisateur ne peut pas coller des formats de texte enrichi, tels que RTF (Rich Text Format) ou des objets incorporés dans un contrôle de texte brut.</span><span class="sxs-lookup"><span data-stu-id="ad12d-153">The user cannot paste rich text formats, such as Rich Text Format (RTF) or embedded objects into a plain text control.</span></span>
-   <span data-ttu-id="ad12d-154">Les contrôles en mode de texte enrichi ont toujours un marqueur de fin de document par défaut ou un retour chariot, pour mettre en forme des paragraphes.</span><span class="sxs-lookup"><span data-stu-id="ad12d-154">Rich text mode controls always have a default end-of-document marker or carriage return, to format paragraphs.</span></span> <span data-ttu-id="ad12d-155">En revanche, les contrôles de texte brut n’ont pas besoin du marqueur de fin de document par défaut. il est donc omis.</span><span class="sxs-lookup"><span data-stu-id="ad12d-155">Plain text controls, on the other hand, do not need the default, end-of-document marker, so it is omitted.</span></span>

<span data-ttu-id="ad12d-156">Le contrôle ne doit pas contenir de texte lorsqu’il reçoit le message **em \_ SETTEXTMODE** .</span><span class="sxs-lookup"><span data-stu-id="ad12d-156">The control must contain no text when it receives the **EM\_SETTEXTMODE** message.</span></span> <span data-ttu-id="ad12d-157">Pour garantir qu’il n’y a pas de texte, envoyez un message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) avec une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="ad12d-157">To ensure there is no text, send a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message with an empty string ("").</span></span>

## <a name="requirements"></a><span data-ttu-id="ad12d-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad12d-158">Requirements</span></span>



| <span data-ttu-id="ad12d-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad12d-159">Requirement</span></span> | <span data-ttu-id="ad12d-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad12d-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad12d-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad12d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="ad12d-162">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad12d-162">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad12d-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad12d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="ad12d-164">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad12d-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad12d-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad12d-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad12d-166"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad12d-166"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad12d-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad12d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad12d-168">**\_GETTEXTMODE em**</span><span class="sxs-lookup"><span data-stu-id="ad12d-168">**EM\_GETTEXTMODE**</span></span>](em-gettextmode.md)
</dt> <dt>

[<span data-ttu-id="ad12d-169">**\_SETUNDOLIMIT em**</span><span class="sxs-lookup"><span data-stu-id="ad12d-169">**EM\_SETUNDOLIMIT**</span></span>](em-setundolimit.md)
</dt> <dt>

[<span data-ttu-id="ad12d-170">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="ad12d-170">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[<span data-ttu-id="ad12d-171">**WM, \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="ad12d-171">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

