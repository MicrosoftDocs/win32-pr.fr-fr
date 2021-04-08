---
title: Message EM_SETIMEOPTIONS (RichEdit. h)
description: Définit les options de l’éditeur de méthode d’entrée (IME).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843810"
---
# <a name="em_setimeoptions-message"></a><span data-ttu-id="2fc25-104">\_Message SETIMEOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="2fc25-104">EM\_SETIMEOPTIONS message</span></span>

<span data-ttu-id="2fc25-105">Définit les options de l’éditeur de méthode d’entrée (IME).</span><span class="sxs-lookup"><span data-stu-id="2fc25-105">Sets the Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="2fc25-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="2fc25-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="2fc25-107">Elle n’est pas prise en charge dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2fc25-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="2fc25-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fc25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fc25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc25-110">Spécifie l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2fc25-110">Specifies one of the following values.</span></span>



| <span data-ttu-id="2fc25-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fc25-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="2fc25-112">Signification</span><span class="sxs-lookup"><span data-stu-id="2fc25-112">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="2fc25-113"><dt>**ensemble de ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-113"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="2fc25-114">Définit les options à celles spécifiées par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2fc25-114">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="2fc25-115"><dt>**ECOOP \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-115"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="2fc25-116">Combine les options spécifiées avec les options actuelles.</span><span class="sxs-lookup"><span data-stu-id="2fc25-116">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="2fc25-117"><dt>**ECOOP \_ et**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-117"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="2fc25-118">Conserve uniquement les options actuelles qui sont également spécifiées par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2fc25-118">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="2fc25-119"><dt>**ECOOP \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-119"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="2fc25-120">Logiquement exclusive ou les options actuelles avec celles qui sont spécifiées par *lParam.*</span><span class="sxs-lookup"><span data-stu-id="2fc25-120">Logically exclusive OR the current options with those specified by *lParam.*</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2fc25-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fc25-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc25-122">Spécifie une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2fc25-122">Specifies one of more of the following values.</span></span>



| <span data-ttu-id="2fc25-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fc25-123">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="2fc25-124">Signification</span><span class="sxs-lookup"><span data-stu-id="2fc25-124">Meaning</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <span data-ttu-id="2fc25-125"><dt>**\_CLOSESTATUSWINDOW IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-125"><dt>**IMF\_CLOSESTATUSWINDOW**</dt></span></span> </dl> | <span data-ttu-id="2fc25-126">Ferme la fenêtre d’État IME lorsque le contrôle reçoit le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2fc25-126">Closes the IME status window when the control receives the input focus.</span></span><br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <span data-ttu-id="2fc25-127"><dt>**\_FORCEACTIVE IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-127"><dt>**IMF\_FORCEACTIVE**</dt></span></span> </dl>                   | <span data-ttu-id="2fc25-128">Active l’IME lorsque le contrôle reçoit le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2fc25-128">Activates the IME when the control receives the input focus.</span></span><br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <span data-ttu-id="2fc25-129"><dt>**\_FORCEDISABLE IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-129"><dt>**IMF\_FORCEDISABLE**</dt></span></span> </dl>                | <span data-ttu-id="2fc25-130">Désactive l’IME lorsque le contrôle reçoit le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2fc25-130">Disables the IME when the control receives the input focus.</span></span><br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <span data-ttu-id="2fc25-131"><dt>**\_FORCEENABLE IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-131"><dt>**IMF\_FORCEENABLE**</dt></span></span> </dl>                   | <span data-ttu-id="2fc25-132">Active l’IME lorsque le contrôle reçoit le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2fc25-132">Enables the IME when the control receives the input focus.</span></span><br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <span data-ttu-id="2fc25-133"><dt>**\_FORCEINACTIVE IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-133"><dt>**IMF\_FORCEINACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="2fc25-134">Désactive l’IME lorsque le contrôle reçoit le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2fc25-134">Inactivates the IME when the control receives the input focus.</span></span><br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <span data-ttu-id="2fc25-135"><dt>**\_FORCENONE IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-135"><dt>**IMF\_FORCENONE**</dt></span></span> </dl>                         | <span data-ttu-id="2fc25-136">Désactive la gestion de l’IME.</span><span class="sxs-lookup"><span data-stu-id="2fc25-136">Disables IME handling.</span></span><br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <span data-ttu-id="2fc25-137"><dt>**\_FORCEREMEMBER IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-137"><dt>**IMF\_FORCEREMEMBER**</dt></span></span> </dl>             | <span data-ttu-id="2fc25-138">Restaure l’État IME précédent lorsque le contrôle reçoit le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2fc25-138">Restores the previous IME status when the control receives the input focus.</span></span><br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <span data-ttu-id="2fc25-139"><dt>**\_MULTIPLEEDIT IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-139"><dt>**IMF\_MULTIPLEEDIT**</dt></span></span> </dl>                | <span data-ttu-id="2fc25-140">Spécifie que la chaîne de composition ne sera pas annulée ou déterminée par les modifications de focus.</span><span class="sxs-lookup"><span data-stu-id="2fc25-140">Specifies that the composition string will not be canceled or determined by focus changes.</span></span> <span data-ttu-id="2fc25-141">Cela permet à une application d’avoir des chaînes de composition distinctes sur chaque contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="2fc25-141">This allows an application to have separate composition strings on each rich edit control.</span></span><br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <span data-ttu-id="2fc25-142"><dt>**VERTICAL de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-142"><dt>**IMF\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="2fc25-143">Remarque utilisée dans Rich Edit 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2fc25-143">Note used in Rich Edit 2.0 and later.</span></span> <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc25-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fc25-144">Return value</span></span>

<span data-ttu-id="2fc25-145">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2fc25-145">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2fc25-146">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="2fc25-146">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fc25-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fc25-147">Requirements</span></span>



| <span data-ttu-id="2fc25-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fc25-148">Requirement</span></span> | <span data-ttu-id="2fc25-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fc25-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc25-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fc25-150">Minimum supported client</span></span><br/> | <span data-ttu-id="2fc25-151">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fc25-151">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fc25-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fc25-152">Minimum supported server</span></span><br/> | <span data-ttu-id="2fc25-153">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fc25-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fc25-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fc25-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fc25-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc25-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fc25-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fc25-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc25-157">**\_GETIMEOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="2fc25-157">**EM\_GETIMEOPTIONS**</span></span>](em-getimeoptions.md)
</dt> </dl>

 

 





