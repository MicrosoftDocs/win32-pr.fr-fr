---
description: Envoyé à une application lorsque l’IME modifie l’état de la composition à la suite d’une séquence de touches. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Message WM_IME_COMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953172"
---
# <a name="wm_ime_composition-message"></a><span data-ttu-id="9be99-104">Message de composition du WM \_ IME \_</span><span class="sxs-lookup"><span data-stu-id="9be99-104">WM\_IME\_COMPOSITION message</span></span>

<span data-ttu-id="9be99-105">Envoyé à une application lorsque l’IME modifie l’état de la composition à la suite d’une séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="9be99-105">Sent to an application when the IME changes composition status as a result of a keystroke.</span></span> <span data-ttu-id="9be99-106">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9be99-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a><span data-ttu-id="9be99-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9be99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be99-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="9be99-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9be99-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9be99-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="9be99-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9be99-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9be99-111">Caractère DBCS représentant la dernière modification apportée à la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="9be99-111">DBCS character representing the latest change to the composition string.</span></span>

</dd> <dt>

<span data-ttu-id="9be99-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9be99-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9be99-113">Valeur spécifiant le mode de modification de la chaîne ou du caractère de composition.</span><span class="sxs-lookup"><span data-stu-id="9be99-113">Value specifying how the composition string or character changed.</span></span> <span data-ttu-id="9be99-114">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9be99-114">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="9be99-115">Pour plus d’informations sur ces valeurs, consultez [valeurs de chaîne de composition IME](ime-composition-string-values.md).</span><span class="sxs-lookup"><span data-stu-id="9be99-115">For more information about these values, see [IME Composition String Values](ime-composition-string-values.md).</span></span>

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

<span data-ttu-id="9be99-116">**comfromateurs \_ gc**</span><span class="sxs-lookup"><span data-stu-id="9be99-116">**GCS\_COMPATTR**</span></span>
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

<span data-ttu-id="9be99-117">**catalogues globaux \_ COMPCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="9be99-117">**GCS\_COMPCLAUSE**</span></span>
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

<span data-ttu-id="9be99-118">**catalogues globaux \_ COMPREADSTR**</span><span class="sxs-lookup"><span data-stu-id="9be99-118">**GCS\_COMPREADSTR**</span></span>
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

<span data-ttu-id="9be99-119">**catalogues globaux \_ COMPREADATTR**</span><span class="sxs-lookup"><span data-stu-id="9be99-119">**GCS\_COMPREADATTR**</span></span>
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

<span data-ttu-id="9be99-120">**catalogues globaux \_ COMPREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="9be99-120">**GCS\_COMPREADCLAUSE**</span></span>
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

<span data-ttu-id="9be99-121">**catalogues globaux \_ COMPSTR**</span><span class="sxs-lookup"><span data-stu-id="9be99-121">**GCS\_COMPSTR**</span></span>
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

<span data-ttu-id="9be99-122">**catalogues globaux \_ CURSORPOS**</span><span class="sxs-lookup"><span data-stu-id="9be99-122">**GCS\_CURSORPOS**</span></span>
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

<span data-ttu-id="9be99-123">**catalogues globaux \_ DELTASTART**</span><span class="sxs-lookup"><span data-stu-id="9be99-123">**GCS\_DELTASTART**</span></span>
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

<span data-ttu-id="9be99-124">**catalogues globaux \_ RESULTCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="9be99-124">**GCS\_RESULTCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

<span data-ttu-id="9be99-125">**catalogues globaux \_ RESULTREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="9be99-125">**GCS\_RESULTREADCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

<span data-ttu-id="9be99-126">**catalogues globaux \_ RESULTREADSTR**</span><span class="sxs-lookup"><span data-stu-id="9be99-126">**GCS\_RESULTREADSTR**</span></span>
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

<span data-ttu-id="9be99-127">**GC \_ RESULTSTR**</span><span class="sxs-lookup"><span data-stu-id="9be99-127">**GCS\_RESULTSTR**</span></span>
</dt> </dl>

<span data-ttu-id="9be99-128">Le paramètre *lParam* peut également avoir une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9be99-128">The *lParam* parameter can also have one or more of the following values.</span></span>



| <span data-ttu-id="9be99-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9be99-129">Value</span></span>                                                                                                                                                            | <span data-ttu-id="9be99-130">Signification</span><span class="sxs-lookup"><span data-stu-id="9be99-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <span data-ttu-id="9be99-131"><dt>**\_INSERTCHAR CS**</dt></span><span class="sxs-lookup"><span data-stu-id="9be99-131"><dt>**CS\_INSERTCHAR**</dt></span></span> </dl>    | <span data-ttu-id="9be99-132">Insérez le caractère de composition *wParam* au niveau du point d’insertion actuel.</span><span class="sxs-lookup"><span data-stu-id="9be99-132">Insert the *wParam* composition character at the current insertion point.</span></span> <span data-ttu-id="9be99-133">Une application doit afficher le caractère de composition s’il traite ce message.</span><span class="sxs-lookup"><span data-stu-id="9be99-133">An application should display the composition character if it processes this message.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <span data-ttu-id="9be99-134"><dt>**\_NOMOVECARET CS**</dt></span><span class="sxs-lookup"><span data-stu-id="9be99-134"><dt>**CS\_NOMOVECARET**</dt></span></span> </dl> | <span data-ttu-id="9be99-135">Ne pas déplacer l’emplacement du signe insertion à la suite du traitement du message.</span><span class="sxs-lookup"><span data-stu-id="9be99-135">Do not move the caret position as a result of processing the message.</span></span> <span data-ttu-id="9be99-136">Par exemple, si un IME spécifie une combinaison de CS \_ INSERTCHAR et CS \_ NOMOVECARET, l’application doit insérer le caractère spécifié à la position actuelle du point d’insertion, mais ne doit pas déplacer le signe insertion à la position suivante.</span><span class="sxs-lookup"><span data-stu-id="9be99-136">For example, if an IME specifies a combination of CS\_INSERTCHAR and CS\_NOMOVECARET, the application should insert the specified character at the current caret position but should not move the caret to the next position.</span></span> <span data-ttu-id="9be99-137">Un message de \_ composition de l’IME WM ultérieur \_ avec GC \_ RESULTSTR remplace ce caractère.</span><span class="sxs-lookup"><span data-stu-id="9be99-137">A subsequent WM\_IME\_COMPOSITION message with GCS\_RESULTSTR will replace this character.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be99-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9be99-138">Return value</span></span>

<span data-ttu-id="9be99-139">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9be99-139">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9be99-140">Notes</span><span class="sxs-lookup"><span data-stu-id="9be99-140">Remarks</span></span>

<span data-ttu-id="9be99-141">Une application doit traiter ce message si elle affiche lui-même des caractères de composition.</span><span class="sxs-lookup"><span data-stu-id="9be99-141">An application should process this message if it displays composition characters itself.</span></span> <span data-ttu-id="9be99-142">Dans le cas contraire, il doit envoyer le message à la fenêtre IME.</span><span class="sxs-lookup"><span data-stu-id="9be99-142">Otherwise, it should send the message to the IME window.</span></span>

<span data-ttu-id="9be99-143">Si l’application a créé une fenêtre IME, elle doit transmettre ce message à cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9be99-143">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="9be99-144">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  traite ce message en le passant à la fenêtre IME par défaut.</span><span class="sxs-lookup"><span data-stu-id="9be99-144">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span> <span data-ttu-id="9be99-145">La fenêtre IME traite ce message en mettant à jour son apparence en fonction de l’indicateur de modification spécifié.</span><span class="sxs-lookup"><span data-stu-id="9be99-145">The IME window processes this message by updating its appearance based on the change flag specified.</span></span> <span data-ttu-id="9be99-146">Une application peut appeler [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) pour récupérer l’état de la nouvelle composition.</span><span class="sxs-lookup"><span data-stu-id="9be99-146">An application can call [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) to retrieve the new composition status.</span></span>

<span data-ttu-id="9be99-147">Si aucune des valeurs de catalogues globaux \_ n’est définie, le message indique que la composition actuelle a été annulée et que les applications qui dessinent la chaîne de composition doivent supprimer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="9be99-147">If none of the GCS\_ values are set, the message indicates that the current composition has been canceled and applications that draw the composition string should delete the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="9be99-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9be99-148">Requirements</span></span>



| <span data-ttu-id="9be99-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9be99-149">Requirement</span></span> | <span data-ttu-id="9be99-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="9be99-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9be99-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9be99-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9be99-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9be99-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="9be99-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9be99-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9be99-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9be99-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="9be99-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="9be99-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be99-156"><dt>Winuser. h (inclure Windows. h); </dt> <dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9be99-156"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be99-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9be99-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be99-158">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9be99-158">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9be99-159">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9be99-159">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="9be99-160">**ImmGetCompositionString**</span><span class="sxs-lookup"><span data-stu-id="9be99-160">**ImmGetCompositionString**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
