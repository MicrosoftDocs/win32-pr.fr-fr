---
title: Message EM_STREAMIN (RichEdit. h)
description: Remplace le contenu d’un contrôle RichEdit par un flux de données fourni par une application définie \ 8211 ; Fonction de rappel EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466347"
---
# <a name="em_streamin-message"></a><span data-ttu-id="c1697-104">\_Message de flux em</span><span class="sxs-lookup"><span data-stu-id="c1697-104">EM\_STREAMIN message</span></span>

<span data-ttu-id="c1697-105">Remplace le contenu d’un contrôle RichEdit par un flux de données fourni par une fonction de rappel [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="c1697-105">Replaces the contents of a rich edit control with a stream of data provided by an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1697-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1697-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1697-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1697-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1697-108">Spécifie le format de données et les options de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c1697-108">Specifies the data format and replacement options.</span></span> <span data-ttu-id="c1697-109">Cette valeur doit être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c1697-109">This value must be one of the following values.</span></span>



| <span data-ttu-id="c1697-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1697-110">Value</span></span>                                                                                                                                       | <span data-ttu-id="c1697-111">Signification</span><span class="sxs-lookup"><span data-stu-id="c1697-111">Meaning</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="c1697-112"><dt>**\_RTF SF**</dt></span><span class="sxs-lookup"><span data-stu-id="c1697-112"><dt>**SF\_RTF**</dt></span></span> </dl>    | <span data-ttu-id="c1697-113">RTF</span><span class="sxs-lookup"><span data-stu-id="c1697-113">RTF</span></span><br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="c1697-114"><dt>**\_texte SF**</dt></span><span class="sxs-lookup"><span data-stu-id="c1697-114"><dt>**SF\_TEXT**</dt></span></span> </dl> | <span data-ttu-id="c1697-115">Texte</span><span class="sxs-lookup"><span data-stu-id="c1697-115">Text</span></span><br/> |



 

<span data-ttu-id="c1697-116">En outre, vous pouvez spécifier les indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="c1697-116">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="c1697-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1697-117">Value</span></span>                                                                                                                                                         | <span data-ttu-id="c1697-118">Signification</span><span class="sxs-lookup"><span data-stu-id="c1697-118">Meaning</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="c1697-119"><dt>**\_PLAINRTF SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="c1697-119"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>    | <span data-ttu-id="c1697-120">S’il est spécifié, seuls les mots clés communs à tous les langages sont diffusés en continu.</span><span class="sxs-lookup"><span data-stu-id="c1697-120">If specified, only keywords common to all languages are streamed in.</span></span> <span data-ttu-id="c1697-121">Les mots clés RTF spécifiques à une langue dans le flux sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="c1697-121">Language-specific RTF keywords in the stream are ignored.</span></span> <span data-ttu-id="c1697-122">S’il n’est pas spécifié, tous les mots clés sont diffusés en continu.</span><span class="sxs-lookup"><span data-stu-id="c1697-122">If not specified, all keywords are streamed in.</span></span> <span data-ttu-id="c1697-123">Vous pouvez combiner cet indicateur avec l’indicateur de **\_ format RTF SF** .</span><span class="sxs-lookup"><span data-stu-id="c1697-123">You can combine this flag with the **SF\_RTF** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="c1697-124"><dt>**\_sélection SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="c1697-124"><dt>**SFF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="c1697-125">S’il est spécifié, le flux de données remplace le contenu de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="c1697-125">If specified, the data stream replaces the contents of the current selection.</span></span> <span data-ttu-id="c1697-126">S’il n’est pas spécifié, le flux de données remplace tout le contenu du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c1697-126">If not specified, the data stream replaces the entire contents of the control.</span></span> <span data-ttu-id="c1697-127">Vous pouvez combiner cet indicateur avec les indicateurs **\_ RTF** de **\_ texte** ou DF.</span><span class="sxs-lookup"><span data-stu-id="c1697-127">You can combine this flag with the **SF\_TEXT** or **SF\_RTF** flags.</span></span><br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="c1697-128"><dt>**\_Unicode DF**</dt></span><span class="sxs-lookup"><span data-stu-id="c1697-128"><dt>**SF\_UNICODE**</dt></span></span> </dl>          | <span data-ttu-id="c1697-129">**Microsoft Rich Edit 2,0 et versions ultérieures :** Indique un texte Unicode.</span><span class="sxs-lookup"><span data-stu-id="c1697-129">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="c1697-130">Vous pouvez combiner cet indicateur avec l’indicateur de **\_ texte DF** .</span><span class="sxs-lookup"><span data-stu-id="c1697-130">You can combine this flag with the **SF\_TEXT** flag.</span></span> <br/>                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="c1697-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1697-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1697-132">Pointeur vers une structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="c1697-132">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="c1697-133">En entrée, le membre **pfnCallback** de cette structure doit pointer vers une fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="c1697-133">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="c1697-134">En sortie, le membre **dwError** peut contenir un code d’erreur différent de zéro si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c1697-134">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1697-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1697-135">Return value</span></span>

<span data-ttu-id="c1697-136">Ce message retourne le nombre de caractères lus.</span><span class="sxs-lookup"><span data-stu-id="c1697-136">This message returns the number of characters read.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1697-137">Notes</span><span class="sxs-lookup"><span data-stu-id="c1697-137">Remarks</span></span>

<span data-ttu-id="c1697-138">Lorsque vous envoyez un message de **\_ flux em** , le contrôle RichEdit effectue des appels répétés à la fonction [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) spécifiée par le membre **pfnCallback** de la structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="c1697-138">When you send an **EM\_STREAMIN** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="c1697-139">Chaque fois que la fonction de rappel est appelée, elle remplit une mémoire tampon avec des données à lire dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c1697-139">Each time the callback function is called, it fills a buffer with data to read into the control.</span></span> <span data-ttu-id="c1697-140">Cela se poursuit jusqu’à ce que la fonction de rappel indique que l’opération de flux est terminée ou qu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="c1697-140">This continues until the callback function indicates that the stream-in operation has been completed or an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1697-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1697-141">Requirements</span></span>



| <span data-ttu-id="c1697-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1697-142">Requirement</span></span> | <span data-ttu-id="c1697-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1697-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1697-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1697-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c1697-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1697-145">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1697-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1697-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c1697-147">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1697-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1697-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1697-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1697-149"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1697-149"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1697-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1697-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1697-151">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c1697-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1697-152">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="c1697-152">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="c1697-153">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="c1697-153">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="c1697-154">**\_STREAMOUT em**</span><span class="sxs-lookup"><span data-stu-id="c1697-154">**EM\_STREAMOUT**</span></span>](em-streamout.md)
</dt> </dl>

 

 





