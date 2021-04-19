---
description: Les \_ constantes d’indicateur de bit LINECALLSTATE décrivent les États d’appel dans lesquels un appel peut se trouver.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Constantes LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541148"
---
# <a name="linecallstate_-constants"></a><span data-ttu-id="8187e-103">\_Constantes LINECALLSTATE</span><span class="sxs-lookup"><span data-stu-id="8187e-103">LINECALLSTATE\_ Constants</span></span>

<span data-ttu-id="8187e-104">Les constantes d’indicateur de bit **LINECALLSTATE \_** décrivent les États d’appel dans lesquels un appel peut se trouver.</span><span class="sxs-lookup"><span data-stu-id="8187e-104">The **LINECALLSTATE\_** bit-flag constants describe the call states a call can be in.</span></span>

<dl> <dt>

<span data-ttu-id="8187e-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ accepté**</span><span class="sxs-lookup"><span data-stu-id="8187e-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-106">L’appel était dans l’état d’offre et a été accepté.</span><span class="sxs-lookup"><span data-stu-id="8187e-106">The call was in the offering state and has been accepted.</span></span> <span data-ttu-id="8187e-107">Cela indique à d’autres applications (de surveillance) que l’application propriétaire actuelle a déclaré responsable de la réponse à l’appel.</span><span class="sxs-lookup"><span data-stu-id="8187e-107">This indicates to other (monitoring) applications that the current owner application has claimed responsibility for answering the call.</span></span> <span data-ttu-id="8187e-108">Dans RNIS, l’état accepté est entré lorsque l’équipement de la partie appelée envoie un message au commutateur, indiquant qu’il est disposé à présenter l’appel à la personne appelée.</span><span class="sxs-lookup"><span data-stu-id="8187e-108">In ISDN, the accepted state is entered when the called-party equipment sends a message to the switch indicating that it is willing to present the call to the called person.</span></span> <span data-ttu-id="8187e-109">Cela a pour effet secondaire d’alerter (sonnerie) les utilisateurs aux deux extrémités de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8187e-109">This has the side effect of alerting (ringing) the users at both ends of the call.</span></span> <span data-ttu-id="8187e-110">Un appel entrant peut toujours recevoir une réponse immédiatement sans avoir d’abord accepté séparément.</span><span class="sxs-lookup"><span data-stu-id="8187e-110">An incoming call can always be immediately answered without first being separately accepted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="8187e-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-112">L’appel reçoit un ton occupé.</span><span class="sxs-lookup"><span data-stu-id="8187e-112">The call is receiving a busy tone.</span></span> <span data-ttu-id="8187e-113">Une tonalité occupée indique que l’appel ne peut pas être effectué sur un circuit (Trunk) ou si la station distante est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8187e-113">A busy tone indicates that the call cannot be completed either a circuit (trunk) or the remote party's station are in use.</span></span> <span data-ttu-id="8187e-114">Consultez [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8187e-114">See [**LINEBUSYMODE\_ Constants**](linebusymode--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ Conférence**</span><span class="sxs-lookup"><span data-stu-id="8187e-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE\_CONFERENCED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-116">L’appel est membre d’un appel de conférence et est logiquement dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="8187e-116">The call is a member of a conference call and is logically in the connected state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="8187e-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-118">L’appel a été établi et la connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="8187e-118">The call has been established and the connection is made.</span></span> <span data-ttu-id="8187e-119">Les informations peuvent être transmises à l’appel entre l’adresse d’origine et l’adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="8187e-119">Information is able to flow over the call between the originating address and the destination address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_numérotation LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="8187e-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE\_DIALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-121">L’expéditeur compose des chiffres sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="8187e-121">The originator is dialing digits on the call.</span></span> <span data-ttu-id="8187e-122">Les chiffres composés sont collectés par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="8187e-122">The dialed digits are collected by the switch.</span></span> <span data-ttu-id="8187e-123">Notez que ni [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ni [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) ne placent la ligne dans l’état de numérotation.</span><span class="sxs-lookup"><span data-stu-id="8187e-123">Note that neither [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nor [**TSPI\_lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) will place the line into the dialing state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="8187e-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-125">L’appel reçoit une tonalité du commutateur, ce qui signifie que le commutateur est prêt à recevoir un numéro composé.</span><span class="sxs-lookup"><span data-stu-id="8187e-125">The call is receiving a dial tone from the switch, which means that the switch is ready to receive a dialed number.</span></span> <span data-ttu-id="8187e-126">Consultez [**LINEDIALTONEMODE \_ constantes**](linedialtonemode--constants.md) pour les identificateurs de tonalités spéciales, telles qu’une tonalité d’interruption de la messagerie vocale normale.</span><span class="sxs-lookup"><span data-stu-id="8187e-126">See [**LINEDIALTONEMODE\_ Constants**](linedialtonemode--constants.md) for identifiers of special dial tones, such as a stutter tone of normal voice mail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ déconnecté**</span><span class="sxs-lookup"><span data-stu-id="8187e-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-128">Le tiers distant s’est déconnecté de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8187e-128">The remote party has disconnected from the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="8187e-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-130">L’appel existe mais n’a pas été connecté.</span><span class="sxs-lookup"><span data-stu-id="8187e-130">The call exists but has not been connected.</span></span> <span data-ttu-id="8187e-131">Aucune activité n’existe sur l’appel, ce qui signifie qu’aucun appel n’est actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="8187e-131">No activity exists on the call, which means that no call is currently active.</span></span> <span data-ttu-id="8187e-132">Un appel ne peut jamais passer de l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="8187e-132">A call can never transition out of the idle state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**\_offre LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="8187e-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE\_OFFERING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-134">L’appel est offert à la station, signalant l’arrivée d’un nouvel appel.</span><span class="sxs-lookup"><span data-stu-id="8187e-134">The call is being offered to the station, signaling the arrival of a new call.</span></span> <span data-ttu-id="8187e-135">L’état de l’offre n’est pas le même que celui d’un téléphone ou d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8187e-135">The offering state is not the same as causing a phone or computer to ring.</span></span> <span data-ttu-id="8187e-136">Dans certains environnements, un appel dans l’état de l’offre ne sonne pas l’utilisateur tant que le commutateur ne demande pas à la ligne de sonner.</span><span class="sxs-lookup"><span data-stu-id="8187e-136">In some environments, a call in the offering state does not ring the user until the switch instructs the line to ring.</span></span> <span data-ttu-id="8187e-137">Un exemple d’utilisation peut être l’endroit où un appel entrant s’affiche sur plusieurs ensembles de stations, mais uniquement les sonneries d’adresse principales.</span><span class="sxs-lookup"><span data-stu-id="8187e-137">An example use might be where an incoming call appears on several station sets but only the primary address rings.</span></span> <span data-ttu-id="8187e-138">L’instruction à Ring n’affecte pas les États d’appel.</span><span class="sxs-lookup"><span data-stu-id="8187e-138">The instruction to ring does not affect any call states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ ONHOLD**</span><span class="sxs-lookup"><span data-stu-id="8187e-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE\_ONHOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-140">L’appel est en attente par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="8187e-140">The call is on hold by the switch.</span></span> <span data-ttu-id="8187e-141">Cela libère la ligne physique, ce qui permet à un autre appel d’utiliser la ligne.</span><span class="sxs-lookup"><span data-stu-id="8187e-141">This frees the physical line, which allows another call to use the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**</span><span class="sxs-lookup"><span data-stu-id="8187e-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE\_ONHOLDPENDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-143">L’appel est actuellement en attente pendant son ajout à une conférence.</span><span class="sxs-lookup"><span data-stu-id="8187e-143">The call is currently on hold while it is being added to a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="8187e-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE\_ONHOLDPENDTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-145">L’appel est actuellement en attente de transfert vers un autre nombre.</span><span class="sxs-lookup"><span data-stu-id="8187e-145">The call is currently on hold awaiting transfer to another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="8187e-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE\_PROCEEDING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-147">La numérotation est terminée et l’appel se poursuit via le commutateur ou le réseau téléphonique.</span><span class="sxs-lookup"><span data-stu-id="8187e-147">Dialing has completed and the call is proceeding through the switch or telephone network.</span></span> <span data-ttu-id="8187e-148">Cela se produit une fois que la numérotation est terminée et que l’appel atteint le tiers composé, comme indiqué par le rappel, le occupé ou la réponse.</span><span class="sxs-lookup"><span data-stu-id="8187e-148">This occurs after dialing is complete and before the call reaches the dialed party, as indicated by ringback, busy, or answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**\_rappel LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="8187e-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-150">La station à appeler a été atteinte et le commutateur de la destination génère une tonalité de retour à l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8187e-150">The station to be called has been reached, and the destination's switch is generating a ring tone back to the originator.</span></span> <span data-ttu-id="8187e-151">Un *rappel* signifie que l’adresse de destination est avertie de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8187e-151">A *ringback* means that the destination address is being alerted to the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**</span><span class="sxs-lookup"><span data-stu-id="8187e-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE\_SPECIALINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-153">L’appel reçoit un signal d’information spécial, qui précède une annonce préenregistrée indiquant la raison pour laquelle un appel ne peut pas être effectué.</span><span class="sxs-lookup"><span data-stu-id="8187e-153">The call is receiving a special information signal, which precedes a prerecorded announcement indicating why a call cannot be completed.</span></span> <span data-ttu-id="8187e-154">Consultez [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8187e-154">See [**LINESPECIALINFO\_ Constants**](linespecialinfo--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8187e-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="8187e-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8187e-156">L’appel existe, mais son état est actuellement inconnu.</span><span class="sxs-lookup"><span data-stu-id="8187e-156">The call exists, but its state is currently unknown.</span></span> <span data-ttu-id="8187e-157">Cela peut être dû à une mauvaise détection de la progression de l’appel par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="8187e-157">This may be the result of poor call progress detection by the service provider.</span></span> <span data-ttu-id="8187e-158">Un message d’état d’appel avec l’état d’appel défini sur inconnu peut également être généré pour informer la DLL TAPI à propos d’un nouvel appel à la fois lorsque l’état d’appel réel de l’appel n’est pas exactement connu.</span><span class="sxs-lookup"><span data-stu-id="8187e-158">A call state message with the call state set to unknown may also be generated to inform the TAPI DLL about a new call at a time when the actual call state of the call is not exactly known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8187e-159">Notes</span><span class="sxs-lookup"><span data-stu-id="8187e-159">Remarks</span></span>

<span data-ttu-id="8187e-160">Les 8 bits de poids fort peuvent définir un sous-état spécifique à l’appareil de l’un des États prédéfinis, à condition que l’un des \_ bits LINECALLSTATE définis ci-dessus soit également défini.</span><span class="sxs-lookup"><span data-stu-id="8187e-160">The high-order 8 bits can define a device-specific substate of any of the predefined states, provided that one of the LINECALLSTATE\_ bits defined above is also set.</span></span> <span data-ttu-id="8187e-161">Les 24 bits de poids faible sont réservés aux États prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="8187e-161">The low-order 24 bits are reserved for predefined states.</span></span>

<span data-ttu-id="8187e-162">Les **\_ constantes LINECALLSTATE** sont utilisées comme paramètres par le message de [**ligne \_ CALLSTATE**](line-callstate.md) envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="8187e-162">The **LINECALLSTATE\_constants** are used as parameters by the [**LINE\_CALLSTATE**](line-callstate.md) message sent to the application.</span></span> <span data-ttu-id="8187e-163">Le message transporte le nouvel état d’appel vers lequel l’appel a été transféré.</span><span class="sxs-lookup"><span data-stu-id="8187e-163">The message carries the new call state that the call transitioned to.</span></span> <span data-ttu-id="8187e-164">Ces constantes sont également utilisées comme membres dans la structure [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) retournée par la fonction [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .</span><span class="sxs-lookup"><span data-stu-id="8187e-164">These constants are also used as members in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure returned by the [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8187e-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8187e-165">Requirements</span></span>



| <span data-ttu-id="8187e-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8187e-166">Requirement</span></span> | <span data-ttu-id="8187e-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="8187e-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8187e-168">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8187e-168">TAPI version</span></span><br/> | <span data-ttu-id="8187e-169">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8187e-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8187e-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="8187e-170">Header</span></span><br/>       | <dl> <span data-ttu-id="8187e-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8187e-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8187e-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8187e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8187e-173">**CALLSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="8187e-173">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="8187e-174">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="8187e-174">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="8187e-175">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="8187e-175">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="8187e-176">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="8187e-176">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

