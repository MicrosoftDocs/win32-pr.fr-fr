---
description: Les \_ constantes d’indicateur de bit LINECALLREASON décrivent la raison d’un appel.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Constantes LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523889"
---
# <a name="linecallreason_-constants"></a><span data-ttu-id="00776-103">\_Constantes LINECALLREASON</span><span class="sxs-lookup"><span data-stu-id="00776-103">LINECALLREASON\_ Constants</span></span>

<span data-ttu-id="00776-104">Les constantes d’indicateur de bit **LINECALLREASON \_** décrivent la raison d’un appel.</span><span class="sxs-lookup"><span data-stu-id="00776-104">The **LINECALLREASON\_** bit-flag constants describe the reason for a call.</span></span>

<dl> <dt>

<span data-ttu-id="00776-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**</span><span class="sxs-lookup"><span data-stu-id="00776-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON\_CALLCOMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-106">L’appel était le résultat d’une demande d’achèvement d’appel.</span><span class="sxs-lookup"><span data-stu-id="00776-106">The call was the result of a call completion request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**</span><span class="sxs-lookup"><span data-stu-id="00776-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON\_CAMPEDON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-108">L’appel a été campé sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="00776-108">The call was camped on the address.</span></span> <span data-ttu-id="00776-109">En règle générale, il apparaît initialement dans l’État onHold et peut être remplacé par [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span><span class="sxs-lookup"><span data-stu-id="00776-109">Usually, it appears initially in the onhold state, and can be switched to using [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span></span> <span data-ttu-id="00776-110">Si un appel actif devient inactif, l’appel d’activation peut passer à l’état de l’offre et à la sonnerie de démarrage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00776-110">If an active call becomes idle, the camped-on call may change to the offering state and the device start ringing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ direct**</span><span class="sxs-lookup"><span data-stu-id="00776-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-112">Il s’agit d’un appel direct entrant ou sortant.</span><span class="sxs-lookup"><span data-stu-id="00776-112">This is a direct incoming or outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**</span><span class="sxs-lookup"><span data-stu-id="00776-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON\_FWDBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-114">Cet appel a été transféré à partir d’une autre extension qui était occupée au moment de l’appel.</span><span class="sxs-lookup"><span data-stu-id="00776-114">This call was forwarded from another extension that was busy at the time of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**</span><span class="sxs-lookup"><span data-stu-id="00776-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON\_FWDNOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-116">L’appel a été transféré à partir d’une autre extension qui n’a pas répondu à l’appel après un certain nombre d’anneaux.</span><span class="sxs-lookup"><span data-stu-id="00776-116">The call was forwarded from another extension that didn't answer the call after some number of rings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**</span><span class="sxs-lookup"><span data-stu-id="00776-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON\_FWDUNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-118">L’appel a été transféré sans condition à partir d’un autre nombre.</span><span class="sxs-lookup"><span data-stu-id="00776-118">The call was forwarded unconditionally from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ intrus**</span><span class="sxs-lookup"><span data-stu-id="00776-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-120">L’appel a été effectué sur la ligne, soit par une action d’achèvement d’appel appelée par une autre station, soit par une action de l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="00776-120">The call intruded onto the line, either by a call completion action invoked by another station or by operator action.</span></span> <span data-ttu-id="00776-121">Selon l’implémentation du commutateur, l’appel peut apparaître dans l’état connecté ou être associé à un appel actif existant sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="00776-121">Depending on switch implementation, the call may appear either in the connected state, or conferenced with an existing active call on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ parqué**</span><span class="sxs-lookup"><span data-stu-id="00776-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON\_PARKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-123">L’appel a été parqué sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="00776-123">The call was parked on the address.</span></span> <span data-ttu-id="00776-124">En règle générale, il apparaît initialement dans l’État onHold.</span><span class="sxs-lookup"><span data-stu-id="00776-124">Usually, it appears initially in the onhold state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**\_collecte LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="00776-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-126">L’appel a été récupéré à partir d’une autre extension.</span><span class="sxs-lookup"><span data-stu-id="00776-126">The call was picked up from another extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**redirection LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="00776-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-128">L’appel a été redirigé vers cette station.</span><span class="sxs-lookup"><span data-stu-id="00776-128">The call was redirected to this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**\_rappel LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="00776-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON\_REMINDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-130">L’appel est un rappel (ou « rappel ») que l’utilisateur a un appel parqué ou bloqué pendant (potentiellement) un long moment.</span><span class="sxs-lookup"><span data-stu-id="00776-130">The call is a reminder (or "recall") that the user has a call parked or on hold for (potentially) a long time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="00776-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON\_ROUTEREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-132">L’appel apparaît sur l’adresse, car le commutateur a besoin d’instructions de routage de l’application.</span><span class="sxs-lookup"><span data-stu-id="00776-132">The call appears on the address because the switch needs routing instructions from the application.</span></span> <span data-ttu-id="00776-133">L’application doit examiner le membre **CalledID** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)et utiliser la fonction [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) pour fournir une nouvelle adresse de numérotation pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="00776-133">The application should examine the **CalledID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo), and use the [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) function to provide a new dialable address for the call.</span></span> <span data-ttu-id="00776-134">Si l’appel doit être bloqué à la place, l’application peut appeler [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="00776-134">If the call is to be blocked instead, the application may call [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span></span> <span data-ttu-id="00776-135">Si l’application ne parvient pas à effectuer d’action dans un délai défini par le commutateur, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="00776-135">If the application fails to take action within a switch-defined timeout period, a default action will be taken.</span></span> <span data-ttu-id="00776-136">Un fournisseur de services peut utiliser cette constante uniquement si la version négociée sur la ligne est 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="00776-136">A service provider can use this constant only if the negotiated version on the line is 2.0 or higher.</span></span> <span data-ttu-id="00776-137">Dans le cas contraire, le fournisseur de services doit substituer LINECALLREASON \_ .</span><span class="sxs-lookup"><span data-stu-id="00776-137">Otherwise the service provider should substitute LINECALLREASON\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_transfert LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="00776-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-139">L’appel a été transféré à partir d’un autre nombre.</span><span class="sxs-lookup"><span data-stu-id="00776-139">The call has been transferred from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="00776-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-141">La raison de l’appel n’est pas disponible et ne sera pas connue ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="00776-141">The reason for the call is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="00776-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-143">La raison de l’appel est actuellement inconnue, mais peut devenir connue ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="00776-143">The reason for the call is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00776-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**déspark LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="00776-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00776-145">L’appel a été récupéré en tant qu’appel parqué.</span><span class="sxs-lookup"><span data-stu-id="00776-145">The call was retrieved as a parked call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00776-146">Notes</span><span class="sxs-lookup"><span data-stu-id="00776-146">Remarks</span></span>

<span data-ttu-id="00776-147">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="00776-147">No extensibility.</span></span> <span data-ttu-id="00776-148">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="00776-148">All 32 bits are reserved.</span></span>

<span data-ttu-id="00776-149">Les \_ constantes LINECALLREASON sont utilisées dans le membre **dwReason** de la structure de données [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="00776-149">The LINECALLREASON\_ constants are used in the **dwReason** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="00776-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00776-150">Requirements</span></span>



| <span data-ttu-id="00776-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00776-151">Requirement</span></span> | <span data-ttu-id="00776-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="00776-152">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="00776-153">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="00776-153">TAPI version</span></span><br/> | <span data-ttu-id="00776-154">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="00776-154">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="00776-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="00776-155">Header</span></span><br/>       | <dl> <span data-ttu-id="00776-156"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="00776-156"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00776-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00776-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00776-158">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="00776-158">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="00776-159">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="00776-159">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="00776-160">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="00776-160">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[<span data-ttu-id="00776-161">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="00776-161">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




