---
description: Les \_ constantes d’indicateur de bit LINECALLINFOSTATE décrivent les différents éléments d’informations sur les appels sur lesquels une application peut être notifiée dans le message de ligne \_ CALLINFO.
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: Constantes LINECALLINFOSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532521"
---
# <a name="linecallinfostate_-constants"></a><span data-ttu-id="88ffd-103">\_Constantes LINECALLINFOSTATE</span><span class="sxs-lookup"><span data-stu-id="88ffd-103">LINECALLINFOSTATE\_ Constants</span></span>

<span data-ttu-id="88ffd-104">Les constantes d’indicateur de bit **LINECALLINFOSTATE \_** décrivent les différents éléments d’informations sur les appels sur lesquels une application peut être notifiée dans le message de [**ligne \_ CALLINFO**](line-callinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="88ffd-104">The **LINECALLINFOSTATE\_** bit-flag constants describe various call information items about which an application can be notified in the [**LINE\_CALLINFO**](line-callinfo.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="88ffd-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE \_ APPSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="88ffd-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE\_APPSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-106">Champ propre à l’application de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-106">The application-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE \_ BEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="88ffd-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE\_BEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-108">Champ du mode porteur de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-108">The bearer mode field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE \_ CALLDATA**</span><span class="sxs-lookup"><span data-stu-id="88ffd-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE\_CALLDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-110">Le membre **CallData** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="88ffd-110">The **CallData** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE \_ CALLEDID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE\_CALLEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-112">Un des champs liés à calledID de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-112">One of the calledID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE \_ CALLERID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE\_CALLERID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-114">Un des champs liés à callerID de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-114">One of the callerID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE \_ CALLID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-116">Champ ID d’appel de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-116">The call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE \_ CHARGINGINFO**</span><span class="sxs-lookup"><span data-stu-id="88ffd-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE\_CHARGINGINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-118">Informations de facturation de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-118">The charging information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE \_ COMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-120">Champ d’identificateur de saisie semi-automatique de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-120">The completion identifier field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE \_ CONNECTEDID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE\_CONNECTEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-122">Un des champs liés à connectedID de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-122">One of the connectedID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="88ffd-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-124">Champ spécifique à l’appareil de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-124">The device-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE \_ DIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="88ffd-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE\_DIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-126">Paramètres de numérotation de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-126">The dial parameters of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**\_affichage LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="88ffd-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**LINECALLINFOSTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-128">Champ d’affichage de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-128">The display field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE \_ HIGHLEVELCOMP**</span><span class="sxs-lookup"><span data-stu-id="88ffd-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE\_HIGHLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-130">Champ de compatibilité de haut niveau de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-130">The high level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE \_ LOWLEVELCOMP**</span><span class="sxs-lookup"><span data-stu-id="88ffd-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE\_LOWLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-132">Champ de compatibilité de bas niveau de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-132">The low level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE \_ MEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="88ffd-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE\_MEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-134">Champ type de média de l’enregistrement Call-information.</span><span class="sxs-lookup"><span data-stu-id="88ffd-134">The media type field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE \_ MONITORMODES**</span><span class="sxs-lookup"><span data-stu-id="88ffd-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE\_MONITORMODES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-136">Un ou plusieurs champs de surveillance de chiffre, de tonalité ou de média dans l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-136">One or more of the digit, tone, or media monitoring fields in the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE \_ NUMMONITORS**</span><span class="sxs-lookup"><span data-stu-id="88ffd-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE\_NUMMONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-138">Le champ nombre de moniteurs dans l’enregistrement d’informations d’appel a changé.</span><span class="sxs-lookup"><span data-stu-id="88ffd-138">The number of monitors field in the call-information record has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE \_ NUMOWNERDECR**</span><span class="sxs-lookup"><span data-stu-id="88ffd-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE\_NUMOWNERDECR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-140">Le nombre de champs de propriétaire dans l’enregistrement d’informations d’appel a été réduit.</span><span class="sxs-lookup"><span data-stu-id="88ffd-140">The number of owner field in the call-information record was decreased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE \_ NUMOWNERINCR**</span><span class="sxs-lookup"><span data-stu-id="88ffd-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE\_NUMOWNERINCR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-142">Le nombre de champs de propriétaire dans l’enregistrement d’informations d’appel a été augmenté.</span><span class="sxs-lookup"><span data-stu-id="88ffd-142">The number of owner field in the call-information record was increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE \_ origine**</span><span class="sxs-lookup"><span data-stu-id="88ffd-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE\_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-144">Champ Origin de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-144">The origin field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE \_ autre**</span><span class="sxs-lookup"><span data-stu-id="88ffd-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-146">Les éléments d’informations d’appel autres que ceux listés ci-dessous ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="88ffd-146">Call information items other than those listed below have changed.</span></span> <span data-ttu-id="88ffd-147">L’application doit vérifier les informations d’appel actuelles pour déterminer les éléments qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="88ffd-147">The application should check the current call information to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**\_QoS LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="88ffd-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE\_QOS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-149">Un ou plusieurs des membres **QoS** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="88ffd-149">One or more of the **QOS** members in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**taux de LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="88ffd-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**LINECALLINFOSTATE\_RATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-151">Le champ rate de l’enregistrement Call-information.</span><span class="sxs-lookup"><span data-stu-id="88ffd-151">The rate field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**\_raison LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="88ffd-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**LINECALLINFOSTATE\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-153">Champ raison de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-153">The reason field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE \_ REDIRECTINGID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE\_REDIRECTINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-155">Identificateur d’adresse de l’emplacement qui a redirigé un appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-155">The address identifier of the location that redirected a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE \_ REDIRECTIONID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE\_REDIRECTIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-157">Identificateur d’adresse de l’emplacement vers lequel un appel a été redirigé.</span><span class="sxs-lookup"><span data-stu-id="88ffd-157">The address identifier of the location to which a call has been redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE \_ RELATEDCALLID**</span><span class="sxs-lookup"><span data-stu-id="88ffd-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE\_RELATEDCALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-159">Champ ID d’appel associé de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-159">The related call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**\_Terminal LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="88ffd-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**LINECALLINFOSTATE\_TERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-161">Informations relatives au mode terminal de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-161">The terminal mode information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**\_traitement LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="88ffd-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**LINECALLINFOSTATE\_TREATMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-163">Le membre **CallTreatment** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="88ffd-163">The **CallTreatment** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span> <span data-ttu-id="88ffd-164">Cela peut se produire en réponse à une fonction [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) , à un changement d’état d’appel, à un appel « Vector » ou à un autre script contrôlant l’appel, ou à la fin de la lecture d’un message enregistré (en général, en indiquant une modification de « silence » ou de « musique »).</span><span class="sxs-lookup"><span data-stu-id="88ffd-164">This can occur in response to a [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) function, a call state change, a call "vector" or other script controlling the call, or upon completion of playback of a recorded message (ordinarily, indicating a change to "silence" or "music").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE \_ Trunk**</span><span class="sxs-lookup"><span data-stu-id="88ffd-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-166">Champ Trunk de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-166">The trunk field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88ffd-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE \_ USERUSERINFO**</span><span class="sxs-lookup"><span data-stu-id="88ffd-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE\_USERUSERINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88ffd-168">Informations utilisateur utilisateur de l’enregistrement d’informations d’appel.</span><span class="sxs-lookup"><span data-stu-id="88ffd-168">The user-user information of the call-information record.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88ffd-169">Notes</span><span class="sxs-lookup"><span data-stu-id="88ffd-169">Remarks</span></span>

<span data-ttu-id="88ffd-170">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="88ffd-170">No extensibility.</span></span> <span data-ttu-id="88ffd-171">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="88ffd-171">All 32 bits are reserved.</span></span>

<span data-ttu-id="88ffd-172">Lorsque des modifications se produisent dans cette structure de données, un message [**\_ CALLINFO de ligne**](line-callinfo.md) est envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="88ffd-172">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="88ffd-173">Les paramètres de ce message sont un descripteur de l’appel et une indication de l’élément d’information qui a changé.</span><span class="sxs-lookup"><span data-stu-id="88ffd-173">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="88ffd-174">La structure de données [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) indique également les éléments d’informations d’appel qui sont valides pour chaque appel sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="88ffd-174">The [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure also indicates which of these call information elements are valid for every call on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ffd-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88ffd-175">Requirements</span></span>



| <span data-ttu-id="88ffd-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88ffd-176">Requirement</span></span> | <span data-ttu-id="88ffd-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="88ffd-177">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="88ffd-178">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="88ffd-178">TAPI version</span></span><br/> | <span data-ttu-id="88ffd-179">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="88ffd-179">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="88ffd-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="88ffd-180">Header</span></span><br/>       | <dl> <span data-ttu-id="88ffd-181"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="88ffd-181"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ffd-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88ffd-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ffd-183">**CALLINFO de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="88ffd-183">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="88ffd-184">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="88ffd-184">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="88ffd-185">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="88ffd-185">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="88ffd-186">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="88ffd-186">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




