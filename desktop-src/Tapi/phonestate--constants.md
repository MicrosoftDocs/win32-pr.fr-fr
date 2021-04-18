---
description: Les \_ constantes d’indicateur de bit PHONESTATE décrivent les différents éléments d’état d’un appareil téléphonique.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Constantes PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526017"
---
# <a name="phonestate_-constants"></a><span data-ttu-id="e470b-103">\_Constantes PHONESTATE</span><span class="sxs-lookup"><span data-stu-id="e470b-103">PHONESTATE\_ Constants</span></span>

<span data-ttu-id="e470b-104">Les constantes d’indicateur de bit **PHONESTATE \_** décrivent les différents éléments d’état d’un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="e470b-104">The **PHONESTATE\_** bit-flag constants describe various status items for a phone device.</span></span>

<dl> <dt>

<span data-ttu-id="e470b-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="e470b-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-106">Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) ont changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) structure have changed.</span></span> <span data-ttu-id="e470b-107">L’application doit utiliser [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) pour lire la structure mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e470b-107">The application should use [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="e470b-108">Si un fournisseur de services envoie un message d' [**\_ État de téléphone**](phone-state.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API précédente recevront des messages d’état de téléphone qui \_ spécifient la réinitialisation PHONESTATE, en \_ leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="e470b-108">If a service provider sends a [**PHONE\_STATE**](phone-state.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive PHONE\_STATE messages specifying PHONESTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="e470b-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-110">La connexion entre l’appareil téléphonique et l’interface TAPI vient d’être établie.</span><span class="sxs-lookup"><span data-stu-id="e470b-110">The connection between the phone device and TAPI was just made.</span></span> <span data-ttu-id="e470b-111">Cela se produit lorsque l’interface TAPI est appelée pour la première fois ou lorsque le câble qui connecte le téléphone au PC est branché avec l’interface TAPI active.</span><span class="sxs-lookup"><span data-stu-id="e470b-111">This happens when TAPI is first invoked or when the wire connecting the phone to the PC is plugged in with TAPI active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="e470b-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-113">Les informations spécifiques à l’appareil du téléphone ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="e470b-113">The phone's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE \_ déconnecté**</span><span class="sxs-lookup"><span data-stu-id="e470b-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-115">La connexion entre l’appareil téléphonique et l’interface TAPI vient d’être rompue.</span><span class="sxs-lookup"><span data-stu-id="e470b-115">The connection between the phone device and TAPI was just broken.</span></span> <span data-ttu-id="e470b-116">Cela se produit lorsque le câble connectant le téléphone à l’ordinateur est débranché alors que TAPI est actif.</span><span class="sxs-lookup"><span data-stu-id="e470b-116">This happens when the wire connecting the phone set to the PC is unplugged while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**\_affichage PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="e470b-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-118">L’affichage du téléphone a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-118">The display of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE \_ HANDSETGAIN**</span><span class="sxs-lookup"><span data-stu-id="e470b-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE\_HANDSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-120">Le paramètre d’augmentation du microphone du combiné a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-120">The handset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE \_ HANDSETHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="e470b-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE\_HANDSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-122">L’état de l’hookswitch de téléphone a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-122">The handset hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE \_ HANDSETVOLUME**</span><span class="sxs-lookup"><span data-stu-id="e470b-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE\_HANDSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-124">Le paramètre du volume de haut-parleur du téléphone a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-124">The handset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE \_ HEADSETHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="e470b-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE\_HEADSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-126">L’état de hookswitch du casque a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-126">The headset's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE \_ HEADSETGAIN**</span><span class="sxs-lookup"><span data-stu-id="e470b-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE\_HEADSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-128">Le paramètre d’augmentation du microphone du casque a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-128">The headset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE \_ HEADSETVOLUME**</span><span class="sxs-lookup"><span data-stu-id="e470b-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE\_HEADSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-130">Le paramètre du volume de haut-parleur du casque a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-130">The headset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_lampe PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="e470b-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE\_LAMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-132">Une lampe du téléphone a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-132">A lamp of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_analyses PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="e470b-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE\_MONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-134">Nombre d’analyses pour l’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="e470b-134">The number of monitors for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ autre**</span><span class="sxs-lookup"><span data-stu-id="e470b-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-136">Les éléments de l’état du téléphone autres que ceux listés ci-dessous ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="e470b-136">Phone-status items other than those listed below have changed.</span></span> <span data-ttu-id="e470b-137">L’application doit vérifier l’état actuel du téléphone pour déterminer les éléments qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="e470b-137">The application should check the current phone status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**\_propriétaire PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="e470b-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-139">Nombre de propriétaires de l’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="e470b-139">The number of owners for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**Réinit PHONESTATE \_**</span><span class="sxs-lookup"><span data-stu-id="e470b-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-141">Les éléments ont été modifiés dans la configuration des appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="e470b-141">Items have changed in the configuration of phone devices.</span></span> <span data-ttu-id="e470b-142">Pour être conscient de ces modifications (comme l’apparence des nouveaux appareils téléphoniques), l’application doit réinitialiser son utilisation de l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="e470b-142">To become aware of these changes (as for the appearance of new phone devices), the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="e470b-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-144">Indique que l’appareil est en cours de suppression du système par le fournisseur de services (probablement via une action de l’utilisateur, via un panneau de configuration ou un utilitaire similaire).</span><span class="sxs-lookup"><span data-stu-id="e470b-144">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="e470b-145">Un message d' [**\_ État de téléphone**](phone-state.md) avec cette valeur est normalement immédiatement suivi d’un message de [**\_ fermeture de téléphone**](phone-close.md) sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e470b-145">A [**PHONE\_STATE**](phone-state.md) message with this value will normally be immediately followed by a [**PHONE\_CLOSE**](phone-close.md) message on the device.</span></span> <span data-ttu-id="e470b-146">Les tentatives suivantes d’accès à l’appareil avant la réinitialisation de l’interface TAPI entraînent \_ le retour de PHONEERR nodevice à l’application.</span><span class="sxs-lookup"><span data-stu-id="e470b-146">Subsequent attempts to access the device prior to TAPI being reinitialized will result in PHONEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="e470b-147">Si un fournisseur de services envoie un \_ message d’état de téléphone contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.</span><span class="sxs-lookup"><span data-stu-id="e470b-147">If a service provider sends a PHONE\_STATE message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE \_ Resume**</span><span class="sxs-lookup"><span data-stu-id="e470b-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-149">L’utilisation de l’appareil téléphonique par l’application reprend après avoir été interrompue pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="e470b-149">The application's use of the phone device is resumed after having been suspended for some time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE \_ RINGMODE**</span><span class="sxs-lookup"><span data-stu-id="e470b-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE\_RINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-151">Le mode Ring du téléphone a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-151">The ring mode of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE \_ RINGVOLUME**</span><span class="sxs-lookup"><span data-stu-id="e470b-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE\_RINGVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-153">Le volume de la sonnerie du téléphone a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-153">The ring volume of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE \_ SPEAKERHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="e470b-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE\_SPEAKERHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-155">L’état de hookswitch du haut-parleur a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-155">The speakerphone's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE \_ SPEAKERGAIN**</span><span class="sxs-lookup"><span data-stu-id="e470b-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE\_SPEAKERGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-157">L’état du paramètre de gain du microphone du haut-parleur a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-157">The speakerphone's microphone gain setting state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE \_ SPEAKERVOLUME**</span><span class="sxs-lookup"><span data-stu-id="e470b-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE\_SPEAKERVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-159">Le paramètre du volume de haut-parleur de haut-parleur a changé.</span><span class="sxs-lookup"><span data-stu-id="e470b-159">The speakerphone's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e470b-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE \_ suspendre**</span><span class="sxs-lookup"><span data-stu-id="e470b-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e470b-161">L’utilisation du téléphone par l’application est temporairement suspendue.</span><span class="sxs-lookup"><span data-stu-id="e470b-161">The application's use of the phone is temporarily suspended.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e470b-162">Notes</span><span class="sxs-lookup"><span data-stu-id="e470b-162">Remarks</span></span>

<span data-ttu-id="e470b-163">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="e470b-163">No extensibility.</span></span> <span data-ttu-id="e470b-164">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="e470b-164">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e470b-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e470b-165">Requirements</span></span>



| <span data-ttu-id="e470b-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e470b-166">Requirement</span></span> | <span data-ttu-id="e470b-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="e470b-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e470b-168">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="e470b-168">TAPI version</span></span><br/> | <span data-ttu-id="e470b-169">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e470b-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e470b-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="e470b-170">Header</span></span><br/>       | <dl> <span data-ttu-id="e470b-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e470b-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e470b-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e470b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e470b-173">**\_Fermer le téléphone**</span><span class="sxs-lookup"><span data-stu-id="e470b-173">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="e470b-174">**État du téléphone \_**</span><span class="sxs-lookup"><span data-stu-id="e470b-174">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="e470b-175">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="e470b-175">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="e470b-176">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="e470b-176">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




