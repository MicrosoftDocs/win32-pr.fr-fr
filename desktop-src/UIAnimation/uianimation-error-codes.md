---
title: Codes d’erreur d’animation Windows (winerror. h)
description: Si une erreur se produit, l’animation Windows retourne un code en tant que valeur HRESULT. Cette section fournit la liste des codes d’erreur spécifiques à l’animation Windows. Pour obtenir la liste des codes d’erreur COM généraux, consultez Codes d’erreur COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511358"
---
# <a name="windows-animation-error-codes"></a><span data-ttu-id="b36d5-105">Codes d’erreur de l’animation Windows</span><span class="sxs-lookup"><span data-stu-id="b36d5-105">Windows Animation Error Codes</span></span>

<span data-ttu-id="b36d5-106">Si une erreur se produit, l’animation Windows retourne un code en tant que valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b36d5-106">If an error occurs, Windows Animation returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="b36d5-107">Cette section fournit la liste des codes d’erreur spécifiques à l’animation Windows.</span><span class="sxs-lookup"><span data-stu-id="b36d5-107">This section provides a list of error codes specific to Windows Animation.</span></span> <span data-ttu-id="b36d5-108">Pour obtenir la liste des codes d’erreur COM généraux, consultez [codes d’erreur com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b36d5-108">For a list of general COM error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b36d5-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**échec de la création de l’interface utilisateur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b36d5-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI\_E\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-110">0x802A0001</span><span class="sxs-lookup"><span data-stu-id="b36d5-110">0x802A0001</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-111">Impossible de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="b36d5-111">The object could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**arrêt de l’interface utilisateur \_ E \_ \_ appelé**</span><span class="sxs-lookup"><span data-stu-id="b36d5-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI\_E\_SHUTDOWN\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-113">0x802A0002</span><span class="sxs-lookup"><span data-stu-id="b36d5-113">0x802A0002</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-114">La méthode [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) a été appelée sur le gestionnaire d’animations, provoquant l’arrêt du gestionnaire d’animations, ainsi que toutes les variables d’animation et les storyboards qu’il a créées pour être libérés.</span><span class="sxs-lookup"><span data-stu-id="b36d5-114">The [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method has been called on the animation manager, causing the animation manager to shut down and all the animation variables and storyboards it created to be released.</span></span>

> [!Note]  
> <span data-ttu-id="b36d5-115">Aucune méthode ne peut être appelée sur un objet d’animation après l' [**arrêt**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span><span class="sxs-lookup"><span data-stu-id="b36d5-115">No methods can be called on any animation object after [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**\_ \_ réentrance non conforme de l’interface utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="b36d5-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI\_E\_ILLEGAL\_REENTRANCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-117">0x802A0003</span><span class="sxs-lookup"><span data-stu-id="b36d5-117">0x802A0003</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-118">Cette méthode ne peut pas être appelée pendant ce type de rappel.</span><span class="sxs-lookup"><span data-stu-id="b36d5-118">This method cannot be called during this type of callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**\_objet UI \_ E \_ sealed**</span><span class="sxs-lookup"><span data-stu-id="b36d5-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI\_E\_OBJECT\_SEALED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-120">0x802A0004</span><span class="sxs-lookup"><span data-stu-id="b36d5-120">0x802A0004</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-121">Cet objet ayant été scellé, cette modification n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="b36d5-121">This object has been sealed, so this change is no longer allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_valeur UI \_ E \_ non \_ définie**</span><span class="sxs-lookup"><span data-stu-id="b36d5-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**UI\_E\_VALUE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-123">0x802A0005</span><span class="sxs-lookup"><span data-stu-id="b36d5-123">0x802A0005</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-124">La valeur demandée n’a jamais été définie et ne peut donc pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="b36d5-124">The requested value has never been set, and therefore cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**\_valeur UI \_ E \_ non \_ déterminée**</span><span class="sxs-lookup"><span data-stu-id="b36d5-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI\_E\_VALUE\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-126">0x802A0006</span><span class="sxs-lookup"><span data-stu-id="b36d5-126">0x802A0006</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-127">La valeur demandée ne peut pas être déterminée.</span><span class="sxs-lookup"><span data-stu-id="b36d5-127">The requested value cannot be determined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**sortie de l’interface utilisateur \_ \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="b36d5-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI\_E\_INVALID\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-129">0x802A0007</span><span class="sxs-lookup"><span data-stu-id="b36d5-129">0x802A0007</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-130">Un rappel a retourné un paramètre de sortie non valide.</span><span class="sxs-lookup"><span data-stu-id="b36d5-130">A callback returned an invalid output parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**interface utilisateur \_ E \_ booléenne \_ attendue**</span><span class="sxs-lookup"><span data-stu-id="b36d5-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI\_E\_BOOLEAN\_EXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-132">0x802A0008</span><span class="sxs-lookup"><span data-stu-id="b36d5-132">0x802A0008</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-133">Un rappel a retourné un code de réussite autre que S \_ OK ou s \_ false.</span><span class="sxs-lookup"><span data-stu-id="b36d5-133">A callback returned a success code other than S\_OK or S\_FALSE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**interface utilisateur \_ E \_ autre \_ propriétaire**</span><span class="sxs-lookup"><span data-stu-id="b36d5-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI\_E\_DIFFERENT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-135">0x802A0009</span><span class="sxs-lookup"><span data-stu-id="b36d5-135">0x802A0009</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-136">Un paramètre qui doit être détenu par cet objet est détenu par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="b36d5-136">A parameter that should be owned by this object is owned by a different object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ correspondance ambiguë de l’interface utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="b36d5-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI\_E\_AMBIGUOUS\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-138">0x802A000A</span><span class="sxs-lookup"><span data-stu-id="b36d5-138">0x802A000A</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-139">Plus d’un élément correspond aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="b36d5-139">More than one item matched the search criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**dépassement de capacité de l’interface utilisateur \_ E \_ FP \_**</span><span class="sxs-lookup"><span data-stu-id="b36d5-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI\_E\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-141">0x802A000B</span><span class="sxs-lookup"><span data-stu-id="b36d5-141">0x802A000B</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-142">Un dépassement de capacité à virgule flottante s’est produit.</span><span class="sxs-lookup"><span data-stu-id="b36d5-142">A floating-point overflow occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**THREAD d’interface utilisateur \_ \_ incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="b36d5-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI\_E\_WRONG\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-144">0x802A000C</span><span class="sxs-lookup"><span data-stu-id="b36d5-144">0x802A000C</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-145">Cette méthode peut uniquement être appelée à partir du thread qui a créé l’objet.</span><span class="sxs-lookup"><span data-stu-id="b36d5-145">This method can only be called from the thread that created the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**Storyboard de l’interface utilisateur \_ \_ \_ actif**</span><span class="sxs-lookup"><span data-stu-id="b36d5-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI\_E\_STORYBOARD\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-147">0x802A0101</span><span class="sxs-lookup"><span data-stu-id="b36d5-147">0x802A0101</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-148">La table de montage séquentiel est actuellement dans la planification.</span><span class="sxs-lookup"><span data-stu-id="b36d5-148">The storyboard is currently in the schedule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**IU \_ E \_ Storyboard \_ non \_ lu**</span><span class="sxs-lookup"><span data-stu-id="b36d5-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI\_E\_STORYBOARD\_NOT\_PLAYING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-150">0x802A0102</span><span class="sxs-lookup"><span data-stu-id="b36d5-150">0x802A0102</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-151">Le Storyboard n’est pas en train de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="b36d5-151">The storyboard is not playing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**IMAGE clé de démarrage de l’interface utilisateur \_ \_ après la \_ \_ \_ fin**</span><span class="sxs-lookup"><span data-stu-id="b36d5-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI\_E\_START\_KEYFRAME\_AFTER\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-153">0x802A0103</span><span class="sxs-lookup"><span data-stu-id="b36d5-153">0x802A0103</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-154">L’image clé de début peut se produire après l’image clé de fin.</span><span class="sxs-lookup"><span data-stu-id="b36d5-154">The start keyframe might occur after the end keyframe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**\_ \_ image clé de fin UI E \_ \_ non \_ déterminée**</span><span class="sxs-lookup"><span data-stu-id="b36d5-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI\_E\_END\_KEYFRAME\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-156">0x802A0104</span><span class="sxs-lookup"><span data-stu-id="b36d5-156">0x802A0104</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-157">Il se peut qu’il ne soit pas possible de déterminer l’heure de fin de l’image clé lorsque l’image clé de démarrage est atteinte.</span><span class="sxs-lookup"><span data-stu-id="b36d5-157">It might not be possible to determine the end keyframe time when the start keyframe is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**\_ \_ chevauchement des boucles UI E \_**</span><span class="sxs-lookup"><span data-stu-id="b36d5-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI\_E\_LOOPS\_OVERLAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-159">0x802A0105</span><span class="sxs-lookup"><span data-stu-id="b36d5-159">0x802A0105</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-160">Deux parties répétées d’une table de montage séquentiel peuvent se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="b36d5-160">Two repeated portions of a storyboard might overlap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**TRANSITION d’interface utilisateur \_ E \_ \_ déjà \_ utilisée**</span><span class="sxs-lookup"><span data-stu-id="b36d5-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI\_E\_TRANSITION\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-162">0x802A0106</span><span class="sxs-lookup"><span data-stu-id="b36d5-162">0x802A0106</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-163">La transition a déjà été ajoutée à un autre Storyboard ou a été ajoutée à une table de montage séquentiel qui a terminé la diffusion et a été libérée.</span><span class="sxs-lookup"><span data-stu-id="b36d5-163">The transition has already been added to a different storyboard or has been added to a storyboard that has finished playing and been released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**\_transition UI \_ E \_ non \_ dans le \_ Storyboard**</span><span class="sxs-lookup"><span data-stu-id="b36d5-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI\_E\_TRANSITION\_NOT\_IN\_STORYBOARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-165">0x802A0107</span><span class="sxs-lookup"><span data-stu-id="b36d5-165">0x802A0107</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-166">La transition n’a pas été ajoutée à une table de montage séquentiel.</span><span class="sxs-lookup"><span data-stu-id="b36d5-166">The transition has not been added to any storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**\_transition UI \_ E \_ eclipsed**</span><span class="sxs-lookup"><span data-stu-id="b36d5-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI\_E\_TRANSITION\_ECLIPSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-168">0x802A0108</span><span class="sxs-lookup"><span data-stu-id="b36d5-168">0x802A0108</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-169">La transition peut Eclipse le début d’une autre transition dans le Storyboard.</span><span class="sxs-lookup"><span data-stu-id="b36d5-169">The transition might eclipse the beginning of another transition in the storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**heure de l’interface utilisateur \_ E \_ avant la \_ \_ dernière \_ mise à jour**</span><span class="sxs-lookup"><span data-stu-id="b36d5-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI\_E\_TIME\_BEFORE\_LAST\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-171">0x802A0109</span><span class="sxs-lookup"><span data-stu-id="b36d5-171">0x802A0109</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-172">L’heure spécifiée est antérieure à l’heure passée à la dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b36d5-172">The specified time is earlier than the time passed to the last update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b36d5-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_ \_ client du minuteur de l’interface utilisateur \_ \_ déjà \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="b36d5-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI\_E\_TIMER\_CLIENT\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36d5-174">0x802A010A</span><span class="sxs-lookup"><span data-stu-id="b36d5-174">0x802A010A</span></span>
</dt> <dt>



<span data-ttu-id="b36d5-175">Ce client est déjà connecté à un minuteur.</span><span class="sxs-lookup"><span data-stu-id="b36d5-175">This client is already connected to a timer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b36d5-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b36d5-176">Requirements</span></span>



| <span data-ttu-id="b36d5-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b36d5-177">Requirement</span></span> | <span data-ttu-id="b36d5-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="b36d5-178">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b36d5-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b36d5-179">Minimum supported client</span></span><br/> | <span data-ttu-id="b36d5-180">Windows 7, Windows Vista et la mise à jour de la plateforme pour les applications de bureau Windows Vista \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b36d5-180">Windows 7, Windows Vista and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b36d5-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b36d5-181">Minimum supported server</span></span><br/> | <span data-ttu-id="b36d5-182">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b36d5-182">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b36d5-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="b36d5-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="b36d5-184"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="b36d5-184"><dt>Winerror.h</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="b36d5-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b36d5-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b36d5-186">Informations de référence sur les animations Windows</span><span class="sxs-lookup"><span data-stu-id="b36d5-186">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

