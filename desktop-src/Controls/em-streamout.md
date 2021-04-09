---
title: Message EM_STREAMOUT (RichEdit. h)
description: Fait en sorte qu’un contrôle RichEdit passe son contenu à une fonction de rappel EditStreamCallback définie par l’application \ 8211 ;. La fonction de rappel peut ensuite écrire le flux de données dans un fichier ou tout autre emplacement qu’il choisit.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942169"
---
# <a name="em_streamout-message"></a><span data-ttu-id="a89ba-105">\_Message STREAMOUT em</span><span class="sxs-lookup"><span data-stu-id="a89ba-105">EM\_STREAMOUT message</span></span>

<span data-ttu-id="a89ba-106">Fait en sorte qu’un contrôle RichEdit passe son contenu à une fonction de rappel [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="a89ba-106">Causes a rich edit control to pass its contents to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span> <span data-ttu-id="a89ba-107">La fonction de rappel peut ensuite écrire le flux de données dans un fichier ou tout autre emplacement qu’il choisit.</span><span class="sxs-lookup"><span data-stu-id="a89ba-107">The callback function can then write the stream of data to a file or any other location that it chooses.</span></span>

## <a name="parameters"></a><span data-ttu-id="a89ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a89ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a89ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a89ba-110">Spécifie le format de données et les options de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a89ba-110">Specifies the data format and replacement options.</span></span>

<span data-ttu-id="a89ba-111">Cette valeur doit être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a89ba-111">This value must be one of the following values.</span></span>



| <span data-ttu-id="a89ba-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a89ba-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="a89ba-113">Signification</span><span class="sxs-lookup"><span data-stu-id="a89ba-113">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="a89ba-114"><dt>**\_RTF SF**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-114"><dt>**SF\_RTF**</dt></span></span> </dl>                   | <span data-ttu-id="a89ba-115">RTF.</span><span class="sxs-lookup"><span data-stu-id="a89ba-115">RTF.</span></span><br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <span data-ttu-id="a89ba-116"><dt>**\_RTFNOOBJS DF**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-116"><dt>**SF\_RTFNOOBJS**</dt></span></span> </dl> | <span data-ttu-id="a89ba-117">RTF avec espaces à la place des objets COM.</span><span class="sxs-lookup"><span data-stu-id="a89ba-117">RTF with spaces in place of COM objects.</span></span><br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="a89ba-118"><dt>**\_texte SF**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-118"><dt>**SF\_TEXT**</dt></span></span> </dl>                | <span data-ttu-id="a89ba-119">Texte avec des espaces à la place des objets COM.</span><span class="sxs-lookup"><span data-stu-id="a89ba-119">Text with spaces in place of COM objects.</span></span><br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <span data-ttu-id="a89ba-120"><dt>**SF \_ texte**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-120"><dt>**SF\_TEXTIZED**</dt></span></span> </dl>    | <span data-ttu-id="a89ba-121">Texte avec une représentation textuelle des objets COM.</span><span class="sxs-lookup"><span data-stu-id="a89ba-121">Text with a text representation of COM objects.</span></span><br/> |



 

<span data-ttu-id="a89ba-122">L’option **DF \_ RTFNOOBJS** est utile si une application stocke des objets com lui-même, car la représentation RTF des objets com n’est pas très compacte.</span><span class="sxs-lookup"><span data-stu-id="a89ba-122">The **SF\_RTFNOOBJS** option is useful if an application stores COM objects itself, as RTF representation of COM objects is not very compact.</span></span> <span data-ttu-id="a89ba-123">Le mot de contrôle \\ objattph, suivi d’un espace, indique la position de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a89ba-123">The control word, \\objattph, followed by a space denotes the object position.</span></span>

<span data-ttu-id="a89ba-124">En outre, vous pouvez spécifier les indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="a89ba-124">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="a89ba-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a89ba-125">Value</span></span>                                                                                                                                                            | <span data-ttu-id="a89ba-126">Signification</span><span class="sxs-lookup"><span data-stu-id="a89ba-126">Meaning</span></span>                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="a89ba-127"><dt>**\_PLAINRTF SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-127"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>       | <span data-ttu-id="a89ba-128">S’il est spécifié, le contrôle RichEdit diffuse uniquement les mots clés communs à tous les langages, en ignorant les mots clés spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="a89ba-128">If specified, the rich edit control streams out only the keywords common to all languages, ignoring language-specific keywords.</span></span> <span data-ttu-id="a89ba-129">S’il n’est pas spécifié, le contrôle RichEdit diffuse tous les mots clés.</span><span class="sxs-lookup"><span data-stu-id="a89ba-129">If not specified, the rich edit control streams out all keywords.</span></span> <span data-ttu-id="a89ba-130">Vous pouvez combiner cet indicateur avec l’indicateur **DF \_ RTF** ou **DF \_ RTFNOOBJS** .</span><span class="sxs-lookup"><span data-stu-id="a89ba-130">You can combine this flag with the **SF\_RTF** or **SF\_RTFNOOBJS** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="a89ba-131"><dt>**\_sélection SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-131"><dt>**SFF\_SELECTION**</dt></span></span> </dl>    | <span data-ttu-id="a89ba-132">S’il est spécifié, le contrôle RichEdit diffuse uniquement le contenu de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="a89ba-132">If specified, the rich edit control streams out only the contents of the current selection.</span></span> <span data-ttu-id="a89ba-133">S’il n’est pas spécifié, le contrôle diffuse en continu le contenu entier.</span><span class="sxs-lookup"><span data-stu-id="a89ba-133">If not specified, the control streams out the entire contents.</span></span> <span data-ttu-id="a89ba-134">Vous pouvez combiner cet indicateur avec l’une des valeurs de format de données.</span><span class="sxs-lookup"><span data-stu-id="a89ba-134">You can combine this flag with any of data format values.</span></span><br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="a89ba-135"><dt>**\_Unicode DF**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-135"><dt>**SF\_UNICODE**</dt></span></span> </dl>             | <span data-ttu-id="a89ba-136">**Microsoft Rich Edit 2,0 et versions ultérieures :** Indique un texte Unicode.</span><span class="sxs-lookup"><span data-stu-id="a89ba-136">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="a89ba-137">Vous pouvez combiner cet indicateur avec l’indicateur de **\_ texte DF** .</span><span class="sxs-lookup"><span data-stu-id="a89ba-137">You can combine this flag with the **SF\_TEXT** flag.</span></span><br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <span data-ttu-id="a89ba-138"><dt>**DF \_ USECODEPAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-138"><dt>**SF\_USECODEPAGE**</dt></span></span> </dl> | <span data-ttu-id="a89ba-139">**Édition enrichie 3,0 et versions ultérieures :** Génère le format RTF UTF-8 ainsi que du texte à l’aide d’autres pages de codes.</span><span class="sxs-lookup"><span data-stu-id="a89ba-139">**Rich Edit 3.0 and later:** Generates UTF-8 RTF as well as text using other code pages.</span></span> <span data-ttu-id="a89ba-140">La page de codes est définie dans le mot de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a89ba-140">The code page is set in the high word of *wParam*.</span></span> <span data-ttu-id="a89ba-141">Par exemple, pour le format RTF UTF-8, affectez à *wParam* la valeur (CP \_ UTF8 << 16) \| SF \_ USECODEPAGE \| DF \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="a89ba-141">For example, for UTF-8 RTF, set *wParam* to (CP\_UTF8 << 16) \| SF\_USECODEPAGE \| SF\_RTF.</span></span><br/>                               |



 

</dd> <dt>

<span data-ttu-id="a89ba-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a89ba-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a89ba-143">Pointeur vers une structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="a89ba-143">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="a89ba-144">En entrée, le membre **pfnCallback** de cette structure doit pointer vers une fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="a89ba-144">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="a89ba-145">En sortie, le membre **dwError** peut contenir un code d’erreur différent de zéro si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a89ba-145">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89ba-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a89ba-146">Return value</span></span>

<span data-ttu-id="a89ba-147">Ce message retourne le nombre de caractères écrits dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="a89ba-147">This message returns the number of characters written to the data stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="a89ba-148">Notes</span><span class="sxs-lookup"><span data-stu-id="a89ba-148">Remarks</span></span>

<span data-ttu-id="a89ba-149">Lorsque vous envoyez un **message \_ em STREAMOUT** , le contrôle RichEdit effectue des appels répétés à la fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) spécifiée par le membre **pfnCallback** de la structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="a89ba-149">When you send an **EM\_STREAMOUT** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="a89ba-150">À chaque fois qu’il appelle la fonction de rappel, le contrôle passe une mémoire tampon contenant une partie du contenu du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a89ba-150">Each time it calls the callback function, the control passes a buffer containing a portion of the contents of the control.</span></span> <span data-ttu-id="a89ba-151">Ce processus se poursuit jusqu’à ce que le contrôle ait passé tout son contenu à la fonction de rappel, ou jusqu’à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="a89ba-151">This process continues until the control has passed all its contents to the callback function, or until an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89ba-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a89ba-152">Requirements</span></span>



| <span data-ttu-id="a89ba-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a89ba-153">Requirement</span></span> | <span data-ttu-id="a89ba-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="a89ba-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a89ba-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a89ba-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a89ba-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a89ba-156">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a89ba-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a89ba-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a89ba-158">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a89ba-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a89ba-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="a89ba-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="a89ba-160"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a89ba-160"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a89ba-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a89ba-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="a89ba-162">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a89ba-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a89ba-163">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="a89ba-163">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="a89ba-164">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="a89ba-164">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="a89ba-165">**\_flux em**</span><span class="sxs-lookup"><span data-stu-id="a89ba-165">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





