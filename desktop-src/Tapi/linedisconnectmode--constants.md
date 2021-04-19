---
description: Les \_ constantes d’indicateur de bit LINEDISCONNECTMODE décrivent les différentes raisons d’une demande de déconnexion distante. Un mode de déconnexion est disponible en tant qu’État d’appel à l’application une fois que l’état d’appel passe à déconnecté.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Constantes LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540026"
---
# <a name="linedisconnectmode_-constants"></a><span data-ttu-id="76911-104">\_Constantes LINEDISCONNECTMODE</span><span class="sxs-lookup"><span data-stu-id="76911-104">LINEDISCONNECTMODE\_ Constants</span></span>

<span data-ttu-id="76911-105">Les constantes d’indicateur de bit **LINEDISCONNECTMODE \_** décrivent les différentes raisons d’une demande de déconnexion distante.</span><span class="sxs-lookup"><span data-stu-id="76911-105">The **LINEDISCONNECTMODE\_** bit-flag constants describe different reasons for a remote disconnect request.</span></span> <span data-ttu-id="76911-106">Un mode de déconnexion est disponible en tant qu’État d’appel à l’application une fois que l’état d’appel passe à déconnecté.</span><span class="sxs-lookup"><span data-stu-id="76911-106">A disconnect mode is available as call status to the application after the call state transitions to disconnected.</span></span>

<dl> <dt>

<span data-ttu-id="76911-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**</span><span class="sxs-lookup"><span data-stu-id="76911-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE\_BADADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-108">L’adresse de destination n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="76911-108">The destination address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="76911-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-110">L’appel n’a pas pu être connecté, car les appels à partir de l’adresse d’origine ne sont pas acceptés à l’adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="76911-110">The call could not be connected because calls from the origination address are not being accepted at the destination address.</span></span> <span data-ttu-id="76911-111">Cela diffère de LINEDISCONNECTMODE \_ Reject dans ce blocage qui est implémenté dans le réseau (un rejet passif), tandis qu’un rejet est implémenté dans l’équipement de destination (un rejet actif).</span><span class="sxs-lookup"><span data-stu-id="76911-111">This differs from LINEDISCONNECTMODE\_REJECT in that blocking is implemented in the network (a passive reject) while a rejection is implemented in the destination equipment (an active reject).</span></span> <span data-ttu-id="76911-112">Le blocage peut être dû à une exclusion spécifique de l’adresse d’origine, ou parce que la destination accepte uniquement les appels d’un ensemble d’adresses d’origine sélectionné (groupe d’utilisateurs fermés).</span><span class="sxs-lookup"><span data-stu-id="76911-112">The blocking can be due to a specific exclusion of the origination address, or because the destination accepts calls from only a selected set of origination address (closed user group).</span></span> <span data-ttu-id="76911-113">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-113">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="76911-114">LINEDISCONNECTMODE \_ bloqué est approprié en tant que réponse mis en liste.</span><span class="sxs-lookup"><span data-stu-id="76911-114">LINEDISCONNECTMODE\_BLOCKED is appropriate as a blocklisted response.</span></span> <span data-ttu-id="76911-115">Par exemple, un modem a reçu une réponse plus de six secondes sans détecter les rappels, échec de la connexion d’un nombre défini de fois, détermine que le numéro de téléphone n’est pas valide pour appeler et émet une réponse « mis en liste ».</span><span class="sxs-lookup"><span data-stu-id="76911-115">For example, a modem has received an answer, gone more than six seconds without detecting Ringback, failed to connect a defined number of times, determines that the phone number is not valid to call, and issues a 'blocklisted' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="76911-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-117">La station de l’utilisateur distant est occupée.</span><span class="sxs-lookup"><span data-stu-id="76911-117">The remote user's station is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ annulé**</span><span class="sxs-lookup"><span data-stu-id="76911-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-119">L’appel a été annulé.</span><span class="sxs-lookup"><span data-stu-id="76911-119">The call was cancelled.</span></span> <span data-ttu-id="76911-120">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-120">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**\_congestion LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="76911-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE\_CONGESTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-122">Le réseau est encombré.</span><span class="sxs-lookup"><span data-stu-id="76911-122">The network is congested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**</span><span class="sxs-lookup"><span data-stu-id="76911-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE\_DONOTDISTURB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-124">L’appel n’a pas pu être connecté, car la destination a appelé la fonctionnalité ne pas déranger.</span><span class="sxs-lookup"><span data-stu-id="76911-124">The call could not be connected because the destination has invoked the Do Not Disturb feature.</span></span> <span data-ttu-id="76911-125">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-125">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ transféré**</span><span class="sxs-lookup"><span data-stu-id="76911-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-127">L’appel a été transféré par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="76911-127">The call was forwarded by the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatible**</span><span class="sxs-lookup"><span data-stu-id="76911-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-129">L’équipement de la station de l’utilisateur distant n’est pas compatible avec le type d’appel demandé.</span><span class="sxs-lookup"><span data-stu-id="76911-129">The remote user's station equipment is incompatible with the type of call requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOanswer**</span><span class="sxs-lookup"><span data-stu-id="76911-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE\_NOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-131">La station de l’utilisateur distant ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="76911-131">The remote user's station does not answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**</span><span class="sxs-lookup"><span data-stu-id="76911-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE\_NODIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-133">Une tonalité n’a pas été détectée dans un délai d’attente défini par le fournisseur de services, à un moment donné pendant la numérotation (par exemple, « W » dans la chaîne de numérotation).</span><span class="sxs-lookup"><span data-stu-id="76911-133">A dial tone was not detected within a service-provider defined timeout, at a point during dialing when one was expected (such as at a "W" in the dialable string).</span></span> <span data-ttu-id="76911-134">Cela peut également se produire sans délai d’attente défini par le fournisseur de services ou sans valeur spécifiée dans le membre **dwWaitForDialTone** de la structure [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) .</span><span class="sxs-lookup"><span data-stu-id="76911-134">This can also occur without a service-provider-defined timeout period or without a value specified in the **dwWaitForDialTone** member of the [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) structure.</span></span> <span data-ttu-id="76911-135">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-135">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="76911-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-137">Il s’agit d’une demande de déconnexion normale de la partie distante.</span><span class="sxs-lookup"><span data-stu-id="76911-137">This is a normal disconnect request by the remote party.</span></span> <span data-ttu-id="76911-138">L’appel a été arrêté normalement.</span><span class="sxs-lookup"><span data-stu-id="76911-138">The call was terminated normally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**</span><span class="sxs-lookup"><span data-stu-id="76911-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE\_NUMBERCHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-140">L’appel n’a pas pu être connecté car le numéro de destination a été modifié, mais la redirection automatique vers le nouveau numéro n’est pas fournie.</span><span class="sxs-lookup"><span data-stu-id="76911-140">The call could not be connected because the destination number has been changed, but automatic redirection to the new number is not provided.</span></span> <span data-ttu-id="76911-141">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-141">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**</span><span class="sxs-lookup"><span data-stu-id="76911-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE\_OUTOFORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-143">L’appel n’a pas pu être connecté ou a été déconnecté car l’appareil de destination est dans le désordre (défaillance matérielle).</span><span class="sxs-lookup"><span data-stu-id="76911-143">The call could not be connected or was disconnected because the destination device is out of order (hardware failure).</span></span> <span data-ttu-id="76911-144">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-144">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**\_collecte LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="76911-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-146">L’appel a été récupéré à partir d’un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="76911-146">The call was picked up from elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="76911-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE\_QOSUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-148">L’appel n’a pas pu être connecté ou a été déconnecté, car la qualité minimale du service n’a pas pu être obtenue ou maintenue.</span><span class="sxs-lookup"><span data-stu-id="76911-148">The call could not be connected or was disconnected because the minimum quality of service could not be obtained or sustained.</span></span> <span data-ttu-id="76911-149">Cela diffère de LINEDISCONNECTMODE \_ incompatible dans le fait que le manque de ressources peut être une condition temporaire au niveau de la destination.</span><span class="sxs-lookup"><span data-stu-id="76911-149">This differs from LINEDISCONNECTMODE\_INCOMPATIBLE in that the lack of resources may be a temporary condition at the destination.</span></span> <span data-ttu-id="76911-150">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-150">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rejeter**</span><span class="sxs-lookup"><span data-stu-id="76911-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE\_REJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-152">L’utilisateur distant a rejeté l’appel.</span><span class="sxs-lookup"><span data-stu-id="76911-152">The remote user has rejected the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**</span><span class="sxs-lookup"><span data-stu-id="76911-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE\_TEMPFAILURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-154">L’appel n’a pas pu être connecté ou a été déconnecté en raison d’une défaillance temporaire du réseau. l’appel peut être retenté ultérieurement et devrait finir.</span><span class="sxs-lookup"><span data-stu-id="76911-154">The call could not be connected or was disconnected because of a temporary failure in the network; the call can be reattempted later and is expected to eventually complete.</span></span> <span data-ttu-id="76911-155">(TAPI versions 2,0 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="76911-155">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="76911-156">LINEDISCONNECTMODE \_ TEMPFAILURE est approprié en tant que réponse différée.</span><span class="sxs-lookup"><span data-stu-id="76911-156">LINEDISCONNECTMODE\_TEMPFAILURE is appropriate as a delayed response.</span></span> <span data-ttu-id="76911-157">Par exemple, un modem obtenant un signal occupé ou un équivalent trop fréquent dans une période donnée conclut que le nombre ne doit pas être rappelé tant qu’une heure définie n’est pas écoulée et qu’il émet une réponse « retardée ».</span><span class="sxs-lookup"><span data-stu-id="76911-157">For example, a modem getting a busy signal or equivalent too many times in a particular time period concludes that the number should not be called again until a defined time has elapsed and issues a 'delayed' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="76911-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-159">La raison de la déconnexion n’est pas disponible et ne sera pas connue ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="76911-159">The reason for the disconnect is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="76911-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-161">La raison de la demande de déconnexion est inconnue, mais peut devenir connue ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="76911-161">The reason for the disconnect request is unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76911-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ INaccessible**</span><span class="sxs-lookup"><span data-stu-id="76911-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76911-163">L’utilisateur distant n’a pas pu être atteint.</span><span class="sxs-lookup"><span data-stu-id="76911-163">The remote user could not be reached.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76911-164">Notes</span><span class="sxs-lookup"><span data-stu-id="76911-164">Remarks</span></span>

<span data-ttu-id="76911-165">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="76911-165">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="76911-166">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="76911-166">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="76911-167">Une demande de déconnexion distante pour un appel donné entraîne la transition de l’état de l’appel à l’État Disconnected et un message de [**ligne \_ CALLSTATE**](line-callstate.md) est envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="76911-167">A remote disconnect request for a given call results in the call state transitioning to the disconnected state and a [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="76911-168">Les informations de LINEDISCONNECTMODE \_ fournissent des détails sur la demande de déconnexion distante.</span><span class="sxs-lookup"><span data-stu-id="76911-168">The LINEDISCONNECTMODE\_ information provides details about the remote disconnect request.</span></span> <span data-ttu-id="76911-169">Elle est disponible dans la structure [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) de l’appel lorsque l’appel est à l’État Disconnected.</span><span class="sxs-lookup"><span data-stu-id="76911-169">It is available in the call's [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure when the call is in the disconnected state.</span></span> <span data-ttu-id="76911-170">Lorsqu’un appel est dans cet État, l’application est toujours autorisée à interroger les informations et l’état de l’appel.</span><span class="sxs-lookup"><span data-stu-id="76911-170">While a call is in this state, the application is still allowed to query the call's information and status.</span></span> <span data-ttu-id="76911-171">Par exemple, les informations utilisateur utilisateur reçues dans le cadre de la déconnexion distante sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="76911-171">For example, user-user information that is received as part of the remote disconnect is available then.</span></span> <span data-ttu-id="76911-172">L’application peut effacer un appel déconnecté en supprimant l’appel.</span><span class="sxs-lookup"><span data-stu-id="76911-172">The application can clear a disconnected call by dropping the call.</span></span>

<span data-ttu-id="76911-173">Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser cette \_ valeur LINEDISCONNECTMODE si elle n’est pas prise en charge sur la version négociée (LINEDISCONNECTMODE \_ normal ou \_ Unknown peut être utilisé à la place).</span><span class="sxs-lookup"><span data-stu-id="76911-173">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEDISCONNECTMODE\_ value if it is not supported on the negotiated version (LINEDISCONNECTMODE\_NORMAL or \_UNKNOWN could be used instead).</span></span>

## <a name="requirements"></a><span data-ttu-id="76911-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76911-174">Requirements</span></span>



| <span data-ttu-id="76911-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76911-175">Requirement</span></span> | <span data-ttu-id="76911-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="76911-176">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="76911-177">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="76911-177">TAPI version</span></span><br/> | <span data-ttu-id="76911-178">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="76911-178">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="76911-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="76911-179">Header</span></span><br/>       | <dl> <span data-ttu-id="76911-180"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="76911-180"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76911-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76911-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76911-182">**CALLSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="76911-182">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="76911-183">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="76911-183">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="76911-184">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="76911-184">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




