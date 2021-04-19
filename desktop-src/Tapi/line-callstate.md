---
description: Le \_ message CALLSTATE de ligne TAPI est envoyé lorsque l’état de l’appel spécifié a changé.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Message LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538767"
---
# <a name="line_callstate-message"></a><span data-ttu-id="8e421-103">\_Message CALLSTATE de ligne</span><span class="sxs-lookup"><span data-stu-id="8e421-103">LINE\_CALLSTATE message</span></span>

<span data-ttu-id="8e421-104">Le message **\_ CALLSTATE de ligne** TAPI est envoyé lorsque l’état de l’appel spécifié a changé.</span><span class="sxs-lookup"><span data-stu-id="8e421-104">The TAPI **LINE\_CALLSTATE** message is sent when the status of the specified call has changed.</span></span> <span data-ttu-id="8e421-105">En règle générale, plusieurs de ces messages sont reçus pendant la durée de vie d’un appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-105">Typically, several such messages are received during the lifetime of a call.</span></span> <span data-ttu-id="8e421-106">Les applications sont averties des nouveaux appels entrants avec ce message ; le nouvel appel est dans l’état de l' *offre* .</span><span class="sxs-lookup"><span data-stu-id="8e421-106">Applications are notified of new incoming calls with this message; the new call is in the *offering* state.</span></span> <span data-ttu-id="8e421-107">L’application peut utiliser [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) pour récupérer des informations plus détaillées sur l’état actuel de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-107">The application can use [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) to retrieve more detailed information about the current status of the call.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8e421-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e421-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e421-109">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="8e421-109">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8e421-110">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-110">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="8e421-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="8e421-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8e421-112">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-112">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="8e421-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8e421-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8e421-114">Nouvel état de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-114">The new call state.</span></span> <span data-ttu-id="8e421-115">Ce paramètre doit être une et une seule des [**\_ constantes LINECALLSTATE**](linecallstate--constants.md)suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e421-115">This parameter must be one and only one of the following [**LINECALLSTATE\_ constants**](linecallstate--constants.md).</span></span>



| <span data-ttu-id="8e421-116">dwParam1</span><span class="sxs-lookup"><span data-stu-id="8e421-116">dwParam1</span></span>                                                                                                                                                                                             | <span data-ttu-id="8e421-117">Signification</span><span class="sxs-lookup"><span data-stu-id="8e421-117">Meaning</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <span data-ttu-id="8e421-118"><dt>**LINECALLSTATE \_ occupé**</dt></span><span class="sxs-lookup"><span data-stu-id="8e421-118"><dt>**LINECALLSTATE\_BUSY**</dt></span></span> </dl>                         | <span data-ttu-id="8e421-119">*dwParam2* contient des détails sur le mode Busy.</span><span class="sxs-lookup"><span data-stu-id="8e421-119">*dwParam2* contains details about the busy mode.</span></span> <span data-ttu-id="8e421-120">Ce paramètre utilise l’une des [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e421-120">This parameter uses one of the [**LINEBUSYMODE\_ constants**](linebusymode--constants.md).</span></span><br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <span data-ttu-id="8e421-121"><dt>**LINECALLSTATE \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="8e421-121"><dt>**LINECALLSTATE\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="8e421-122">*dwParam2* contient des détails sur le mode connecté.</span><span class="sxs-lookup"><span data-stu-id="8e421-122">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="8e421-123">Ce paramètre utilise l’une des [**\_ constantes LINECONNECTEDMODE**](lineconnectedmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e421-123">This parameter uses one of the [**LINECONNECTEDMODE\_ constants**](lineconnectedmode--constants.md).</span></span><br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <span data-ttu-id="8e421-124"><dt>**LINECALLSTATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e421-124"><dt>**LINECALLSTATE\_DIALTONE**</dt></span></span> </dl>             | <span data-ttu-id="8e421-125">*dwParam2* contient des détails sur le mode de tonalité.</span><span class="sxs-lookup"><span data-stu-id="8e421-125">*dwParam2* contains details about the dial tone mode.</span></span> <span data-ttu-id="8e421-126">Ce paramètre utilise l’une des [**\_ constantes LINEDIALTONEMODE**](linedialtonemode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e421-126">This parameter uses one of the [**LINEDIALTONEMODE\_ constants**](linedialtonemode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <span data-ttu-id="8e421-127"><dt>**\_offre LINECALLSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="8e421-127"><dt>**LINECALLSTATE\_OFFERING**</dt></span></span> </dl>             | <span data-ttu-id="8e421-128">*dwParam2* contient des détails sur le mode connecté.</span><span class="sxs-lookup"><span data-stu-id="8e421-128">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="8e421-129">Ce paramètre utilise l’une des [**\_ constantes LINEOFFERINGMODE**](lineofferingmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e421-129">This parameter uses one of the [**LINEOFFERINGMODE\_ constants**](lineofferingmode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <span data-ttu-id="8e421-130"><dt>**LINECALLSTATE \_ SPECIALINFO**</dt></span><span class="sxs-lookup"><span data-stu-id="8e421-130"><dt>**LINECALLSTATE\_SPECIALINFO**</dt></span></span> </dl>    | <span data-ttu-id="8e421-131">*dwParam2* contient les détails sur le mode d’information spécial.</span><span class="sxs-lookup"><span data-stu-id="8e421-131">*dwParam2* contains the details about the special information mode.</span></span> <span data-ttu-id="8e421-132">Ce paramètre utilise l’une des [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e421-132">This parameter uses one of the [**LINESPECIALINFO\_ constants**](linespecialinfo--constants.md).</span></span><br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <span data-ttu-id="8e421-133"><dt>**LINECALLSTATE \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="8e421-133"><dt>**LINECALLSTATE\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8e421-134">*dwParam2* contient des détails sur le mode de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="8e421-134">*dwParam2* contains details about the disconnect mode.</span></span> <span data-ttu-id="8e421-135">Ce paramètre utilise l’une des [**\_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e421-135">This parameter uses one of the [**LINEDISCONNECTMODE\_ constants**](linedisconnectmode--constants.md).</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="8e421-136">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8e421-136">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8e421-137">Informations dépendantes de l’état d’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-137">Call-state-dependent information.</span></span> <span data-ttu-id="8e421-138">Consultez *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="8e421-138">See *dwParam1*.</span></span>

> [!Note]  
> <span data-ttu-id="8e421-139">Dans les cas où une réponse *différée* est appropriée, utilisez LINEDISCONNECTMODE \_ TEMPFAILURE.</span><span class="sxs-lookup"><span data-stu-id="8e421-139">In circumstances where a *delayed* response is appropriate, use LINEDISCONNECTMODE\_TEMPFAILURE.</span></span> <span data-ttu-id="8e421-140">Quand une réponse *mis en liste* est appropriée, utilisez LINEDISCONNECT \_ bloqué.</span><span class="sxs-lookup"><span data-stu-id="8e421-140">Where a *blocklisted* response is appropriate, use LINEDISCONNECT\_BLOCKED.</span></span> <span data-ttu-id="8e421-141">Pour plus d’informations, [**consultez \_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e421-141">For further information, see [**LINEDISCONNECTMODE\_ Constants**](linedisconnectmode--constants.md).</span></span>

 

<span data-ttu-id="8e421-142">Si *dwParam1* est LINECALLSTATE \_ conferenced, *DwParam2* contient le paramètre *hConfCall* de l’appel parent de la conférence dont l’objet *hCall* est membre.</span><span class="sxs-lookup"><span data-stu-id="8e421-142">If *dwParam1* is LINECALLSTATE\_CONFERENCED, *dwParam2* contains the *hConfCall* parameter of the parent call of the conference of which the subject *hCall* is a member.</span></span> <span data-ttu-id="8e421-143">Si l’appel spécifié dans *dwParam2* n’a pas été précédemment pris en compte par l’application pour être un appel de conférence parent (*hConfCall*, l’application doit le faire à la suite de ce message.</span><span class="sxs-lookup"><span data-stu-id="8e421-143">If the call specified in *dwParam2* was not previously considered by the application to be a parent conference call (*hConfCall*, the application must do so as a result of this message.</span></span> <span data-ttu-id="8e421-144">Si l’application n’a pas de handle vers l’appel parent de la Conférence (car elle a précédemment appelé [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) sur ce handle) *dwParam2* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="8e421-144">If the application does not have a handle to the parent call of the conference (because it has previously called [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) on that handle) *dwParam2* is set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8e421-145">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8e421-145">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8e421-146">Si la valeur est zéro, ce paramètre indique qu’il n’y a eu aucune modification du privilège de l’application pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-146">If zero, this parameter indicates that there has been no change in the application's privilege for the call.</span></span>

<span data-ttu-id="8e421-147">Si la valeur est différente de zéro, elle spécifie le privilège de l’application pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-147">If nonzero, it specifies the application's privilege for the call.</span></span> <span data-ttu-id="8e421-148">Cela se produit dans les situations suivantes : (1) la première fois que l’application reçoit un handle pour cet appel ; (2) lorsque l’application est la cible d’un transfert d’appel (même si l’application était déjà propriétaire de l’appel).</span><span class="sxs-lookup"><span data-stu-id="8e421-148">This occurs in the following situations: (1) The first time that the application is given a handle to this call; (2) When the application is the target of a call handoff (even if the application already was an owner of the call).</span></span> <span data-ttu-id="8e421-149">Ce paramètre utilise l’une des [**\_ constantes LINECALLPRIVILEGE**](linecallprivilege--constants.md)suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e421-149">This parameter uses one of the following [**LINECALLPRIVILEGE\_ constants**](linecallprivilege--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e421-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e421-150">Return value</span></span>

<span data-ttu-id="8e421-151">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8e421-151">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e421-152">Notes</span><span class="sxs-lookup"><span data-stu-id="8e421-152">Remarks</span></span>

<span data-ttu-id="8e421-153">Ce message est envoyé à toute application qui a un handle pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e421-153">This message is sent to any application that has a handle for the call.</span></span> <span data-ttu-id="8e421-154">Le message de **ligne \_ CALLSTATE** avertit également les applications qui surveillent les appels sur une ligne de l’existence et de l’état des appels sortants établis par d’autres applications ou manuellement par l’utilisateur (par exemple, sur un appareil téléphonique attaché).</span><span class="sxs-lookup"><span data-stu-id="8e421-154">The **LINE\_CALLSTATE** message also notifies applications that monitor calls on a line about the existence and state of outbound calls established by other applications or manually by the user (for example, on an attached phone device).</span></span> <span data-ttu-id="8e421-155">L’état d’appel de ces appels reflète l’état réel de l’appel, qui n' *offre* pas.</span><span class="sxs-lookup"><span data-stu-id="8e421-155">The call state of such calls reflects the actual state of the call, which is not *offering*.</span></span> <span data-ttu-id="8e421-156">En examinant l’état de l’appel, l’application peut déterminer si l’appel est un appel entrant qui doit être traité ou non.</span><span class="sxs-lookup"><span data-stu-id="8e421-156">By examining the call state, the application can determine whether the call is an inbound call that needs to be answered or not.</span></span>

<span data-ttu-id="8e421-157">Un **message \_ CALLSTATE de ligne** avec un état d’appel inconnu peut être envoyé à une application de surveillance suite à une réussite de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)ou [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) qui a été demandée par une autre application.</span><span class="sxs-lookup"><span data-stu-id="8e421-157">A **LINE\_CALLSTATE** message with an unknown call state can be sent to a monitoring application as the result of a successful [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference), or [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) that has been requested by another application.</span></span> <span data-ttu-id="8e421-158">En même temps que l’application à l’origine de la demande reçoit une [**\_ réponse de ligne**](line-reply.md) (succès) pour l’opération demandée, les applications de surveillance de la ligne reçoivent le message de **ligne \_ CALLSTATE** (inconnu).</span><span class="sxs-lookup"><span data-stu-id="8e421-158">At the same time that the requesting application is sent a [**LINE\_REPLY**](line-reply.md) (success) for the requested operation, any monitoring applications on the line are sent the **LINE\_CALLSTATE** (unknown) message.</span></span> <span data-ttu-id="8e421-159">Un message de **\_ CALLSTATE de ligne** indiquant l’état d’appel « réel » de l’appel récemment généré est envoyé (à l’aide des informations fournies par le fournisseur de services) aux applications de demande et de surveillance, peu de temps après.</span><span class="sxs-lookup"><span data-stu-id="8e421-159">A **LINE\_CALLSTATE** message indicating the "real" call state of the newly generated call is sent (using information provided by the service provider) to the requesting and monitoring applications shortly thereafter.</span></span>

<span data-ttu-id="8e421-160">Un message **line \_ CALLSTATE** (Unknown) est envoyé aux applications de surveillance uniquement si [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) entraîne la résolution des appels en conférence triple.</span><span class="sxs-lookup"><span data-stu-id="8e421-160">A **LINE\_CALLSTATE** (unknown) message is sent to monitoring applications only if [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causes calls to be resolved into a three-way conference.</span></span>

<span data-ttu-id="8e421-161">Pour la compatibilité descendante, les applications plus anciennes n’attendent aucune valeur particulière dans *dwParam2* d’un \_ message LINECALLSTATE conferencinged.</span><span class="sxs-lookup"><span data-stu-id="8e421-161">For backward compatibility, older applications are not expecting any particular value in *dwParam2* of a LINECALLSTATE\_CONFERENCED message.</span></span> <span data-ttu-id="8e421-162">TAPI transmet donc l’appel parent *hConfCall* dans *dwParam2* , quelle que soit la version d’API de l’application qui reçoit le message.</span><span class="sxs-lookup"><span data-stu-id="8e421-162">TAPI therefore passes the parent call *hConfCall* in *dwParam2* regardless of the API version of the application receiving the message.</span></span> <span data-ttu-id="8e421-163">Dans le cas d’un appel de conférence initié par le fournisseur de services, l’ancienne application ne sait pas que l’appel parent est devenu un appel de conférence, à moins qu’il n’examine spontanément d’autres informations (par exemple, appelez [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span><span class="sxs-lookup"><span data-stu-id="8e421-163">In the case of a conference call initiated by the service provider, the older application is not aware that the parent call has become a conference call unless it happens to spontaneously examine other information (for example, call [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span></span>

<span data-ttu-id="8e421-164">Ce message ne peut pas être désactivé.</span><span class="sxs-lookup"><span data-stu-id="8e421-164">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e421-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e421-165">Requirements</span></span>



| <span data-ttu-id="8e421-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e421-166">Requirement</span></span> | <span data-ttu-id="8e421-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e421-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8e421-168">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8e421-168">TAPI version</span></span><br/> | <span data-ttu-id="8e421-169">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8e421-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8e421-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e421-170">Header</span></span><br/>       | <dl> <span data-ttu-id="8e421-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e421-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e421-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e421-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e421-173">**réponse de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="8e421-173">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="8e421-174">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="8e421-174">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="8e421-175">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="8e421-175">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="8e421-176">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="8e421-176">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[<span data-ttu-id="8e421-177">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="8e421-177">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="8e421-178">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="8e421-178">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="8e421-179">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="8e421-179">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[<span data-ttu-id="8e421-180">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="8e421-180">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="8e421-181">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="8e421-181">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="8e421-182">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="8e421-182">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[<span data-ttu-id="8e421-183">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="8e421-183">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="8e421-184">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="8e421-184">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[<span data-ttu-id="8e421-185">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="8e421-185">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




