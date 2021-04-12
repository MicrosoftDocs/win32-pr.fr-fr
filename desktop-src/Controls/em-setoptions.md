---
title: Message EM_SETOPTIONS (RichEdit. h)
description: Définit les options pour un contrôle RichEdit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103492"
---
# <a name="em_setoptions-message"></a><span data-ttu-id="6b0d5-104">\_Message SETOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="6b0d5-104">EM\_SETOPTIONS message</span></span>

<span data-ttu-id="6b0d5-105">Définit les options pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-105">Sets the options for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b0d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b0d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b0d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0d5-108">Spécifie l’opération, qui peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-108">Specifies the operation, which can be one of these values.</span></span>



| <span data-ttu-id="6b0d5-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b0d5-109">Value</span></span>                                                                                                                                             | <span data-ttu-id="6b0d5-110">Signification</span><span class="sxs-lookup"><span data-stu-id="6b0d5-110">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="6b0d5-111"><dt>**ensemble de ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-111"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="6b0d5-112">Définit les options à celles spécifiées par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-112">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="6b0d5-113"><dt>**ECOOP \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-113"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="6b0d5-114">Combine les options spécifiées avec les options actuelles.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-114">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="6b0d5-115"><dt>**ECOOP \_ et**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-115"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="6b0d5-116">Conserve uniquement les options actuelles qui sont également spécifiées par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-116">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="6b0d5-117"><dt>**ECOOP \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-117"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="6b0d5-118">Logiquement exclusive ou les options actuelles avec celles qui sont spécifiées par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-118">Logically exclusive OR the current options with those specified by *lParam*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b0d5-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b0d5-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0d5-120">Spécifie une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-120">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="6b0d5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b0d5-121">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="6b0d5-122">Signification</span><span class="sxs-lookup"><span data-stu-id="6b0d5-122">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <span data-ttu-id="6b0d5-123"><dt>**ECO \_ AUTOWORDSELECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-123"><dt>**ECO\_AUTOWORDSELECTION**</dt></span></span> </dl> | <span data-ttu-id="6b0d5-124">Sélection automatique du mot sur le double-clic.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-124">Automatic selection of word on double-click.</span></span><br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <span data-ttu-id="6b0d5-125"><dt>**ECO \_ AUTOVSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-125"><dt>**ECO\_AUTOVSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="6b0d5-126">Identique au style [**es \_ AUTOVSCROLL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0d5-126">Same as [**ES\_AUTOVSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <span data-ttu-id="6b0d5-127"><dt>**ECO \_ AUTOHSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-127"><dt>**ECO\_AUTOHSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="6b0d5-128">Identique au style [**es \_ AUTOHSCROLL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0d5-128">Same as [**ES\_AUTOHSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <span data-ttu-id="6b0d5-129"><dt>**ECO \_ NOHIDESEL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-129"><dt>**ECO\_NOHIDESEL**</dt></span></span> </dl>                         | <span data-ttu-id="6b0d5-130">Identique au style [**es \_ NOHIDESEL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0d5-130">Same as [**ES\_NOHIDESEL**](rich-edit-control-styles.md) style.</span></span><br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <span data-ttu-id="6b0d5-131"><dt>**ECO en \_ lecture seule**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-131"><dt>**ECO\_READONLY**</dt></span></span> </dl>                            | <span data-ttu-id="6b0d5-132">Identique au style [**es \_ ReadOnly**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0d5-132">Same as [**ES\_READONLY**](rich-edit-control-styles.md) style.</span></span><br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <span data-ttu-id="6b0d5-133"><dt>**ECO \_ WANTRETURN**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-133"><dt>**ECO\_WANTRETURN**</dt></span></span> </dl>                      | <span data-ttu-id="6b0d5-134">Identique au style [**es \_ WANTRETURN**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0d5-134">Same as [**ES\_WANTRETURN**](rich-edit-control-styles.md) style.</span></span><br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <span data-ttu-id="6b0d5-135"><dt>**ECO \_ SELECTIONBAR**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-135"><dt>**ECO\_SELECTIONBAR**</dt></span></span> </dl>                | <span data-ttu-id="6b0d5-136">Identique au style [**es \_ SELECTIONBAR**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0d5-136">Same as [**ES\_SELECTIONBAR**](rich-edit-control-styles.md) style.</span></span><br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <span data-ttu-id="6b0d5-137"><dt>**ECO \_ vertical**</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-137"><dt>**ECO\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="6b0d5-138">Identique au [**style \_ vertical es**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0d5-138">Same as [**ES\_VERTICAL**](rich-edit-control-styles.md) style.</span></span> <span data-ttu-id="6b0d5-139">Disponible uniquement dans les versions asiatiques.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-139">Available in Asian-language versions only.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b0d5-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b0d5-140">Return value</span></span>

<span data-ttu-id="6b0d5-141">Ce message retourne les options actuelles du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="6b0d5-141">This message returns the current options of the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b0d5-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b0d5-142">Requirements</span></span>



| <span data-ttu-id="6b0d5-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b0d5-143">Requirement</span></span> | <span data-ttu-id="6b0d5-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b0d5-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0d5-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b0d5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0d5-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b0d5-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b0d5-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b0d5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0d5-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b0d5-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b0d5-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b0d5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b0d5-150"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b0d5-150"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b0d5-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b0d5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0d5-152">**Styles de contrôle RichEdit**</span><span class="sxs-lookup"><span data-stu-id="6b0d5-152">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
</dt> </dl>

 

 





