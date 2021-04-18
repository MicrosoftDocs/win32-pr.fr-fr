---
description: Les \_ constantes d’indicateur de bit LINEDEVSTATE décrivent différents événements d’état de ligne.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Constantes LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540097"
---
# <a name="linedevstate_-constants"></a><span data-ttu-id="2514e-103">\_Constantes LINEDEVSTATE</span><span class="sxs-lookup"><span data-stu-id="2514e-103">LINEDEVSTATE\_ Constants</span></span>

<span data-ttu-id="2514e-104">Les constantes d’indicateur de bit **LINEDEVSTATE \_** décrivent différents événements d’état de ligne.</span><span class="sxs-lookup"><span data-stu-id="2514e-104">The **LINEDEVSTATE\_** bit-flag constants describe various line status events.</span></span>

<dl> <dt>

<span data-ttu-id="2514e-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_batterie LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="2514e-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE\_BATTERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-106">Le niveau de batterie a changé de manière significative (cellulaire).</span><span class="sxs-lookup"><span data-stu-id="2514e-106">The battery level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="2514e-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-108">Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour l’adresse ont changé.</span><span class="sxs-lookup"><span data-stu-id="2514e-108">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the address have changed.</span></span> <span data-ttu-id="2514e-109">L’application doit utiliser [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) pour lire la structure mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2514e-109">The application should use [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="2514e-110">Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à l’interface TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version TAPI précédente reçoivent des messages de **ligne \_ LINEDEVSTATE** qui spécifient LINEDEVSTATE \_ Réinit, en leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2514e-110">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="2514e-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-112">La ligne a été fermée par une autre application.</span><span class="sxs-lookup"><span data-stu-id="2514e-112">The line has been closed by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**</span><span class="sxs-lookup"><span data-stu-id="2514e-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE\_CONFIGCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-114">Indique que des modifications de configuration ont été apportées à un ou plusieurs périphériques multimédias associés à l’appareil de ligne.</span><span class="sxs-lookup"><span data-stu-id="2514e-114">Indicates that configuration changes have been made to one or more of the media devices associated with the line device.</span></span> <span data-ttu-id="2514e-115">L’application, si elle le souhaite, peut utiliser [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) pour lire les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2514e-115">The application, if it desires, can use [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) to read the updated information.</span></span> <span data-ttu-id="2514e-116">Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.</span><span class="sxs-lookup"><span data-stu-id="2514e-116">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**</span><span class="sxs-lookup"><span data-stu-id="2514e-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE\_COMPLCANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-118">Indique que l’achèvement de l’appel identifié par l’identificateur d’achèvement contenu dans le paramètre *dwParam2* de la [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) message a été annulé de manière externe et n’est plus considéré comme valide (si cette valeur devait être passée dans un appel ultérieur à [**LINEUNCOMPLETECALL**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la fonction échoue avec LINEERR \_ INVALCOMPLETIONID).</span><span class="sxs-lookup"><span data-stu-id="2514e-118">Indicates that the call completion identified by the completion identifier contained in the *dwParam2* parameter of the [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message has been externally canceled and is no longer considered valid (if that value were to be passed in a subsequent call to [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), the function would fail with LINEERR\_INVALCOMPLETIONID).</span></span> <span data-ttu-id="2514e-119">Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.</span><span class="sxs-lookup"><span data-stu-id="2514e-119">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="2514e-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-121">La ligne a été déconnectée précédemment et est maintenant connectée à TAPI.</span><span class="sxs-lookup"><span data-stu-id="2514e-121">The line was previously disconnected and is now connected to TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="2514e-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-123">Les informations spécifiques à l’appareil de la ligne ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="2514e-123">The line's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ déconnecté**</span><span class="sxs-lookup"><span data-stu-id="2514e-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-125">Cette ligne a déjà été connectée et est maintenant déconnectée de TAPI.</span><span class="sxs-lookup"><span data-stu-id="2514e-125">This line was previously connected and is now disconnected from TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**InService LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="2514e-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-127">La ligne est connectée à l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="2514e-127">The line is connected to TAPI.</span></span> <span data-ttu-id="2514e-128">Cela se produit lorsque TAPI est activé pour la première fois ou lorsque le câble de ligne est physiquement branché et en service au commutateur alors que TAPI est actif.</span><span class="sxs-lookup"><span data-stu-id="2514e-128">This happens when TAPI is first activated or when the line wire is physically plugged in and in-service at the switch while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_verrou LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="2514e-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-130">L’état verrouillé de l’appareil de ligne a changé.</span><span class="sxs-lookup"><span data-stu-id="2514e-130">The locked status of the line device has changed.</span></span> <span data-ttu-id="2514e-131">(Pour plus d’informations, consultez LINEDEVSTATUSFLAGS \_ VERROUILLÉ dans [**les \_ constantes LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md).)</span><span class="sxs-lookup"><span data-stu-id="2514e-131">(For more information, see LINEDEVSTATUSFLAGS\_LOCKED in [**LINEDEVSTATUSFLAGS\_ Constants**](linedevstatusflags--constants.md).)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**\_maintenance LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="2514e-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE\_MAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-133">La maintenance est effectuée sur la ligne au niveau du commutateur.</span><span class="sxs-lookup"><span data-stu-id="2514e-133">Maintenance is being performed on the line at the switch.</span></span> <span data-ttu-id="2514e-134">TAPI ne peut pas être utilisé pour fonctionner sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="2514e-134">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**</span><span class="sxs-lookup"><span data-stu-id="2514e-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE\_MSGWAITOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-136">L’indicateur de message en attente est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2514e-136">The message waiting indicator is turned off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**</span><span class="sxs-lookup"><span data-stu-id="2514e-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE\_MSGWAITON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-138">L’indicateur de message en attente est activé.</span><span class="sxs-lookup"><span data-stu-id="2514e-138">The message waiting indicator is turned on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="2514e-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-140">Le nombre d’appels sur le périphérique de ligne a changé.</span><span class="sxs-lookup"><span data-stu-id="2514e-140">The number of calls on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**</span><span class="sxs-lookup"><span data-stu-id="2514e-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE\_NUMCOMPLETIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-142">Le nombre de saisies semi-automatiques d’appels en attente sur le périphérique de ligne a changé.</span><span class="sxs-lookup"><span data-stu-id="2514e-142">The number of outstanding call completions on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ ouvrir**</span><span class="sxs-lookup"><span data-stu-id="2514e-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-144">La ligne a été ouverte par une autre application.</span><span class="sxs-lookup"><span data-stu-id="2514e-144">The line has been opened by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ autre**</span><span class="sxs-lookup"><span data-stu-id="2514e-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-146">Les éléments d’état de l’appareil autres que ceux listés ci-dessous ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="2514e-146">Device-status items other than those listed below have changed.</span></span> <span data-ttu-id="2514e-147">L’application doit vérifier l’état actuel de l’appareil pour déterminer les éléments qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="2514e-147">The application should check the current device status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**</span><span class="sxs-lookup"><span data-stu-id="2514e-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE\_OUTOFSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-149">La ligne est hors service au niveau du commutateur ou physiquement déconnectée.</span><span class="sxs-lookup"><span data-stu-id="2514e-149">The line is out of service at the switch or physically disconnected.</span></span> <span data-ttu-id="2514e-150">TAPI ne peut pas être utilisé pour fonctionner sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="2514e-150">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**Réinit LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="2514e-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-152">Les éléments ont été modifiés dans la configuration des appareils en ligne.</span><span class="sxs-lookup"><span data-stu-id="2514e-152">Items have changed in the configuration of line devices.</span></span> <span data-ttu-id="2514e-153">Pour être conscient de ces modifications (comme l’apparence des nouveaux appareils de ligne), l’application doit réinitialiser son utilisation de l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="2514e-153">To become aware of these changes (as for the appearance of new line devices) the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="2514e-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-155">Indique que l’appareil est en cours de suppression du système par le fournisseur de services (probablement via une action de l’utilisateur, via un panneau de configuration ou un utilitaire similaire).</span><span class="sxs-lookup"><span data-stu-id="2514e-155">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="2514e-156">Un [**message \_ LINEDEVSTATE de ligne**](line-linedevstate.md) avec cette valeur est normalement immédiatement suivi d’un message de [**\_ fermeture de ligne**](line-close.md) sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2514e-156">A [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message with this value will normally be immediately followed by a [**LINE\_CLOSE**](line-close.md) message on the device.</span></span> <span data-ttu-id="2514e-157">Les tentatives suivantes d’accès à l’appareil avant la réinitialisation de l’interface TAPI entraînent \_ le retour de LINEERR nodevice à l’application.</span><span class="sxs-lookup"><span data-stu-id="2514e-157">Subsequent attempts to access the device prior to TAPI being reinitialized will result in LINEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="2514e-158">Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.</span><span class="sxs-lookup"><span data-stu-id="2514e-158">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_sonnerie LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="2514e-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE\_RINGING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-160">Le commutateur indique à la ligne d’alerter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2514e-160">The switch tells the line to alert the user.</span></span>

<span data-ttu-id="2514e-161">**TAPI :** Les fournisseurs de services notifient les applications sur chaque cycle de sonnerie en envoyant de manière répétée des messages [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette constante.</span><span class="sxs-lookup"><span data-stu-id="2514e-161">**TAPI:** Service providers notify applications on each ring cycle by repeatedly sending [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages containing this constant.</span></span> <span data-ttu-id="2514e-162">Par exemple, dans le États-Unis, les fournisseurs de services envoient un message avec cette constante toutes les six secondes.</span><span class="sxs-lookup"><span data-stu-id="2514e-162">For example, in the United States, service providers send a message with this constant every six seconds.</span></span>

<span data-ttu-id="2514e-163">**TSPI :** Sur un appareil POTS, le fournisseur de services peut envoyer le message chaque fois que le Bureau central envoie la tension de la sonnerie.</span><span class="sxs-lookup"><span data-stu-id="2514e-163">**TSPI:** On a POTS device, the service provider can send the message whenever the central office sends ring voltage.</span></span> <span data-ttu-id="2514e-164">Sur les appareils numériques tels que RNIS, le fournisseur de services peut être amené à synthétiser la répétition du message si le commutateur ne génère qu’une seule demande de sonnerie.</span><span class="sxs-lookup"><span data-stu-id="2514e-164">On digital devices such as ISDN, the service provider may need to synthesize the repetition of the message if the switch generates only one ring request.</span></span> <span data-ttu-id="2514e-165">Chaque répétition du message doit indiquer le nombre de sonneries, afin que les fonctions Toll Save fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="2514e-165">Each repetition of the message should show the ring count increasing, so that toll save functions work properly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="2514e-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE\_ROAMMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-167">Le mode itinérant du périphérique de ligne a changé.</span><span class="sxs-lookup"><span data-stu-id="2514e-167">The roam mode of the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**\_signal LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="2514e-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE\_SIGNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-169">Le niveau de signal a changé de manière significative (cellulaire).</span><span class="sxs-lookup"><span data-stu-id="2514e-169">The signal level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminaux LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="2514e-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-171">Les paramètres du terminal ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="2514e-171">The terminal settings have changed.</span></span> <span data-ttu-id="2514e-172">Cela peut se produire, par exemple, si plusieurs périphériques de ligne partagent des terminaux entre eux (par exemple, deux lignes partageant un terminal de téléphone).</span><span class="sxs-lookup"><span data-stu-id="2514e-172">This can happen, for example, if multiple line devices share terminals among them (for example, two lines sharing a phone terminal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2514e-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**</span><span class="sxs-lookup"><span data-stu-id="2514e-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE\_TRANSLATECHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2514e-174">Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) ont changé.</span><span class="sxs-lookup"><span data-stu-id="2514e-174">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure have changed.</span></span> <span data-ttu-id="2514e-175">L’application doit utiliser [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) pour lire la structure mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2514e-175">The application should use [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) to read the updated structure.</span></span> <span data-ttu-id="2514e-176">Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à l’interface TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version TAPI précédente reçoivent des messages de **ligne \_ LINEDEVSTATE** qui spécifient LINEDEVSTATE \_ Réinit, en leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2514e-176">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2514e-177">Notes</span><span class="sxs-lookup"><span data-stu-id="2514e-177">Remarks</span></span>

<span data-ttu-id="2514e-178">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="2514e-178">No extensibility.</span></span> <span data-ttu-id="2514e-179">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="2514e-179">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="2514e-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2514e-180">Requirements</span></span>



| <span data-ttu-id="2514e-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2514e-181">Requirement</span></span> | <span data-ttu-id="2514e-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="2514e-182">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2514e-183">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2514e-183">TAPI version</span></span><br/> | <span data-ttu-id="2514e-184">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2514e-184">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2514e-185">En-tête</span><span class="sxs-lookup"><span data-stu-id="2514e-185">Header</span></span><br/>       | <dl> <span data-ttu-id="2514e-186"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2514e-186"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2514e-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2514e-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2514e-188">**fermeture de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="2514e-188">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="2514e-189">**LINEDEVSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="2514e-189">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="2514e-190">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="2514e-190">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="2514e-191">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="2514e-191">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="2514e-192">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="2514e-192">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="2514e-193">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="2514e-193">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="2514e-194">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="2514e-194">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="2514e-195">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="2514e-195">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




