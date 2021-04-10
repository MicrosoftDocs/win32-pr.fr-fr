---
title: Message EM_SETWORDWRAPMODE (RichEdit. h)
description: Définit les options de retour automatique à la disposition et de césure des mots pour un contrôle RichEdit.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032973"
---
# <a name="em_setwordwrapmode-message"></a><span data-ttu-id="087d9-104">\_Message SETWORDWRAPMODE em</span><span class="sxs-lookup"><span data-stu-id="087d9-104">EM\_SETWORDWRAPMODE message</span></span>

<span data-ttu-id="087d9-105">Définit les options de retour automatique à la disposition et de césure des mots pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="087d9-105">Sets the word-wrapping and word-breaking options for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="087d9-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="087d9-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="087d9-107">Elle n’est pas prise en charge dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="087d9-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="087d9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="087d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="087d9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="087d9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="087d9-110">Spécifie une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="087d9-110">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="087d9-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="087d9-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="087d9-112">Signification</span><span class="sxs-lookup"><span data-stu-id="087d9-112">Meaning</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <span data-ttu-id="087d9-113"><dt>**WBF \_ WORDWRAP**</dt></span><span class="sxs-lookup"><span data-stu-id="087d9-113"><dt>**WBF\_WORDWRAP**</dt></span></span> </dl>    | <span data-ttu-id="087d9-114">Active les opérations de retour automatique à la ligne, telles que l’Kinsoku en japonais.</span><span class="sxs-lookup"><span data-stu-id="087d9-114">Enables Asian-specific word wrap operations, such as kinsoku in Japanese.</span></span> <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <span data-ttu-id="087d9-115"><dt>**WBF \_ WordBreak**</dt></span><span class="sxs-lookup"><span data-stu-id="087d9-115"><dt>**WBF\_WORDBREAK**</dt></span></span> </dl> | <span data-ttu-id="087d9-116">Active les opérations de césure en anglais en japonais et en chinois.</span><span class="sxs-lookup"><span data-stu-id="087d9-116">Enables English word-breaking operations in Japanese and Chinese.</span></span> <span data-ttu-id="087d9-117">Active l’opération de césure de mots hangeul.</span><span class="sxs-lookup"><span data-stu-id="087d9-117">Enables Hangeul word-breaking operation.</span></span><br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <span data-ttu-id="087d9-118"><dt>**\_dépassement WBF**</dt></span><span class="sxs-lookup"><span data-stu-id="087d9-118"><dt>**WBF\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="087d9-119">Reconnaît la ponctuation de dépassement.</span><span class="sxs-lookup"><span data-stu-id="087d9-119">Recognizes overflow punctuation.</span></span> <span data-ttu-id="087d9-120">(Non pris en charge actuellement.)</span><span class="sxs-lookup"><span data-stu-id="087d9-120">(Not currently supported.)</span></span><br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <span data-ttu-id="087d9-121"><dt>**WBF \_ niveau1**</dt></span><span class="sxs-lookup"><span data-stu-id="087d9-121"><dt>**WBF\_LEVEL1**</dt></span></span> </dl>          | <span data-ttu-id="087d9-122">Définit la table de ponctuation de niveau 1 comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="087d9-122">Sets the Level 1 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <span data-ttu-id="087d9-123"><dt>**WBF- \_ d’isolement2**</dt></span><span class="sxs-lookup"><span data-stu-id="087d9-123"><dt>**WBF\_LEVEL2**</dt></span></span> </dl>          | <span data-ttu-id="087d9-124">Définit la table de ponctuation de niveau 2 comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="087d9-124">Sets the Level 2 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <span data-ttu-id="087d9-125"><dt>**WBF \_ personnalisé**</dt></span><span class="sxs-lookup"><span data-stu-id="087d9-125"><dt>**WBF\_CUSTOM**</dt></span></span> </dl>          | <span data-ttu-id="087d9-126">Définit la table de ponctuation définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="087d9-126">Sets the application-defined punctuation table.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="087d9-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="087d9-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="087d9-128">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="087d9-128">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="087d9-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="087d9-129">Return value</span></span>

<span data-ttu-id="087d9-130">Ce message retourne les options de retour automatique à la casse et de césure en cours.</span><span class="sxs-lookup"><span data-stu-id="087d9-130">This message returns the current word-wrapping and word-breaking options.</span></span>

## <a name="remarks"></a><span data-ttu-id="087d9-131">Notes</span><span class="sxs-lookup"><span data-stu-id="087d9-131">Remarks</span></span>

<span data-ttu-id="087d9-132">Ce message ne doit pas être envoyé par la procédure de césure des mots définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="087d9-132">This message must not be sent by the application defined word breaking procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="087d9-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="087d9-133">Requirements</span></span>



| <span data-ttu-id="087d9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="087d9-134">Requirement</span></span> | <span data-ttu-id="087d9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="087d9-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="087d9-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="087d9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="087d9-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="087d9-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="087d9-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="087d9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="087d9-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="087d9-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="087d9-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="087d9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="087d9-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="087d9-141"><dt>Richedit.h</dt></span></span> </dl> |



 

 





