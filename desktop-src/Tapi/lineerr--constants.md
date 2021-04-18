---
description: La liste suivante répertorie les codes d’erreur que TAPI peut retourner lors de l’appel d’opérations sur des lignes, des adresses ou des appels.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Constantes LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540092"
---
# <a name="lineerr_-constants"></a><span data-ttu-id="ccbf1-103">\_Constantes LINEERR</span><span class="sxs-lookup"><span data-stu-id="ccbf1-103">LINEERR\_ Constants</span></span>

<span data-ttu-id="ccbf1-104">La liste suivante répertorie les codes d’erreur que TAPI peut retourner lors de l’appel d’opérations sur des lignes, des adresses ou des appels.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-104">The following is a list of error codes that TAPI can return when invoking operations on lines, addresses, or calls.</span></span> <span data-ttu-id="ccbf1-105">Pour plus d’informations sur la façon de déterminer les codes d’erreur qu’une fonction particulière peut retourner, consultez les descriptions des fonctions individuelles.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-105">For more information about how to determine which of these error codes a particular function can return, see the individual function descriptions.</span></span>

<dl> <dt>

<span data-ttu-id="ccbf1-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-107">L’adresse spécifiée est bloquée et ne peut pas être numérotée sur l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-107">The specified address is blocked from being dialed on the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-109">Le blocage des appels est activé pour l’adresse de l’appel cible.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-109">The target call address has call blocking enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ allouée**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-111">La ligne ne peut pas être ouverte en raison d’une condition persistante, telle que celle d’un port série qui est ouvert en mode exclusif par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-111">The line cannot be opened due to a persistent condition, such as that of a serial port being exclusively opened by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-113">L’identificateur d’appareil ou l’identificateur de périphérique de ligne spécifié, par exemple dans un paramètre *dwDeviceID* , n’est pas valide ou est hors limites.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-113">The specified device identifier or line device identifier, such as in a *dwDeviceID* parameter, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR\_BEARERMODEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-115">Le membre du mode porteur dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) n’est pas valide, le mode porteur spécifié dans **LINECALLPARAMS** n’est pas disponible, ou le mode porteur de l’appel ne peut pas être remplacé par le mode de support spécifié.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-115">The bearer mode member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) is invalid, the bearer mode specified in **LINECALLPARAMS** is not available, or the call bearer mode cannot be changed to the specified bearer mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR\_BILLINGREJECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-117">Le mode de facturation de l’appel a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-117">The billing mode of the call was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR\_CALLUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-119">Toutes les apparences des appels sur l’adresse spécifiée sont en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-119">All call appearances on the specified address are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR\_COMPLETIONOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-121">Le nombre maximal d’appels terminés en attente a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-121">The maximum number of outstanding call completions has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR\_CONFERENCEFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-123">Le nombre maximal de tiers pour une conférence a été atteint ou le nombre demandé de tiers ne peut pas être respecté.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-123">The maximum number of parties for a conference has been reached, or the requested number of parties cannot be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-125">Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-125">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-127">Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-127">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-129">Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-129">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-131">Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-131">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR\_DIALVOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-133">Utilisation du modificateur de numérotation ( :) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-133">Use of the dial modifier (:) is not supported.</span></span> <span data-ttu-id="ccbf1-134">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-134">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ déconnecté**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-136">L’appel a été déconnecté.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-136">The call has been disconnected.</span></span> <span data-ttu-id="ccbf1-137">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,2 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-137">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-139">L’application a demandé une version ou une plage de versions TAPI qui est incompatible avec, ou ne peut pas être prise en charge par, l’implémentation de l’API de téléphonie et le fournisseur de services correspondant.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-139">The application requested a TAPI version or version range that is either incompatible with, or cannot be supported by, the Telephony API implementation and the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-141">L’application a demandé une plage de versions d’extension qui n’est pas valide ou qui ne peut pas être prise en charge par le fournisseur de services correspondant.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-141">The application requested an extension version range that is either invalid or cannot be supported by the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-143">L’interface TAPI ne peut pas lire ou comprendre correctement le fichier Telephon.ini en raison d’incohérences internes ou de problèmes de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-143">The Telephon.ini file cannot be read or understood properly by TAPI because of internal inconsistencies or formatting problems.</span></span> <span data-ttu-id="ccbf1-144">Par exemple, la \[ \] section emplacements, \[ cartes \] ou \[ pays \] du fichier Telephon.ini peut être endommagée ou incohérente.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-144">For example, the \[Locations\], \[Cards\], or \[Countries\] section of the Telephon.ini file may be corrupted or inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ Inuse**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-146">Le périphérique de ligne est en cours d’utilisation et ne peut pas être configuré, autoriser l’ajout d’un tiers, autoriser la réponse à un appel, autoriser le placement d’un appel ou autoriser le transfert d’un appel.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-146">The line device is in use and cannot currently be configured, allow a party to be added, allow a call to be answered, allow a call to be placed, or allow a call to be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR\_INVALADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-148">L’adresse spécifiée n’est pas valide ou n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-148">A specified address is either invalid or not allowed.</span></span> <span data-ttu-id="ccbf1-149">Si ce n’est pas le cas, l’adresse contient des caractères ou des chiffres non valides, ou l’adresse de destination contient des caractères de contrôle de numérotation (W, @, $ ou ?) qui ne sont pas pris en charge par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-149">If invalid, the address contains invalid characters or digits, or the destination address contains dialing control characters (W, @, $, or ?) that are not supported by the service provider.</span></span> <span data-ttu-id="ccbf1-150">Si cette valeur n’est pas autorisée, l’adresse spécifiée n’est pas affectée à la ligne spécifiée ou n’est pas valide pour la redirection d’adresse.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-150">If not allowed, the specified address is either not assigned to the specified line or is not valid for address redirection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR\_INVALADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-152">L’identificateur d’adresse spécifié n’est pas valide ou est hors limites.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-152">The specified address identifier is either invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR\_INVALADDRESSMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-154">Le mode d’adresse spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-154">The specified address mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR\_INVALADDRESSSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-156">L’état de l’adresse spécifiée contient un ou plusieurs bits qui ne sont pas des [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="ccbf1-156">The specified address state contains one or more bits that are not [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR\_INVALADDRESSTYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-158">L’application a référencé un type d’adresse qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-158">The application referenced an address type that is not valid.</span></span> <span data-ttu-id="ccbf1-159">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 3,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-159">This value is exposed only to applications that negotiate a TAPI version of 3.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-161">L’activité de l’agent spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-161">The specified agent activity is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-163">L’application qui appelle cette opération est la cible du transfert indirect.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-163">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="ccbf1-164">Autrement dit, TAPI a déterminé que l’application appelante est également l’application de priorité la plus élevée pour le type de média donné.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-164">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span> <span data-ttu-id="ccbf1-165">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-165">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-167">Les informations de groupe d’agents spécifiées ne sont pas valides ou contiennent des erreurs.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-167">The specified agent group information is not valid or contains errors.</span></span> <span data-ttu-id="ccbf1-168">L’action demandée n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-168">The requested action has not been performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-170">L’application a référencé un groupe d’agents non valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-170">The application referenced an agent group that is not valid.</span></span> <span data-ttu-id="ccbf1-171">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-171">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-173">L’identificateur d’agent spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-173">The specified agent identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-175">Un identificateur d’agent non valide a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-175">An invalid agent identifier was used.</span></span> <span data-ttu-id="ccbf1-176">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-176">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR\_INVALAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-178">L’état de session de l’agent n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-178">The agent session state is invalid.</span></span> <span data-ttu-id="ccbf1-179">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,2 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-179">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-181">L’état spécifié de l’agent n’est pas valide ou contient des erreurs.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-181">The specified agent state is not valid or contains errors.</span></span> <span data-ttu-id="ccbf1-182">Aucune modification n’a été apportée à l’état de l’agent de l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-182">No changes have been made to the agent state of the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-184">L’application a référencé un état d’agent non valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-184">The application referenced an agent state that is not valid.</span></span> <span data-ttu-id="ccbf1-185">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-185">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-187">Le descripteur d’application (tel que spécifié par un paramètre *hLineApp* ) ou le descripteur d’inscription de l’application n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-187">The application handle (such as specified by a *hLineApp* parameter) or the application registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-189">Le nom d’application spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-189">The specified application name is invalid.</span></span> <span data-ttu-id="ccbf1-190">Si un nom d’application est spécifié par l’application, il est supposé que la chaîne ne contient pas de caractères non affichables et qu’elle se termine par zéro.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-190">If an application name is specified by the application, it is assumed that the string does not contain any non-displayable characters, and is zero-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR\_INVALBEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-192">Le mode de support spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-192">The specified bearer mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR\_INVALCALLCOMPLMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-194">La saisie semi-automatique spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-194">The specified completion is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR\_INVALCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-196">Le descripteur d’appel spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-196">The specified call handle is not valid.</span></span> <span data-ttu-id="ccbf1-197">Par exemple, le handle n’est pas **null** , mais n’appartient pas à la ligne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-197">For example, the handle is not **NULL** but does not belong to the given line.</span></span> <span data-ttu-id="ccbf1-198">Dans certains cas, le descripteur d’appareil d’appel spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-198">In some cases, the specified call device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR\_INVALCALLPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-200">Les paramètres d’appel spécifiés ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-200">The specified call parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR\_INVALCALLPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-202">Le paramètre de privilège d’appel spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-202">The specified call privilege parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR\_INVALCALLSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-204">Le paramètre Select spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-204">The specified select parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR\_INVALCALLSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-206">L’état actuel d’un appel n’est pas dans un état valide pour l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-206">The current state of a call is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR\_INVALCALLSTATELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-208">La liste d’États d’appels spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-208">The specified call state list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR\_INVALCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-210">L’identificateur de carte permanente spécifié dans *dwCard* est introuvable dans une entrée de la \[ section des cartes du \] Registre.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-210">The permanent card identifier specified in *dwCard* could not be found in any entry in the \[Cards\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR\_INVALCOMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-212">L’identificateur de saisie semi-automatique n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-212">The completion identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR\_INVALCONFCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-214">Le descripteur d’appel spécifié pour l’appel de conférence n’est pas valide ou n’est pas un handle pour un appel de conférence.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-214">The specified call handle for the conference call is invalid or is not a handle for a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR\_INVALCONSULTCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-216">Le handle de l’appel de consultation spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-216">The specified consultation call handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR\_INVALCOUNTRYCODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-218">Le code du pays ou de la région spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-218">The specified country or region code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-220">Le périphérique de ligne n’a aucun appareil associé pour la classe d’appareil donnée, ou la ligne spécifiée ne prend pas en charge la classe d’appareil indiquée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-220">The line device has no associated device for the given device class, or the specified line does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR\_INVALDEVICEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-222">Le handle de périphérique de ligne n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-222">The line device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR\_INVALDIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-224">Les paramètres de numérotation ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-224">The dialing parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR\_INVALDIGITLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-226">La liste de chiffres spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-226">The specified digit list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR\_INVALDIGITMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-228">Le mode de chiffrement spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-228">The specified digit mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR\_INVALDIGITS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-230">Les chiffres de fin spécifiés ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-230">The specified termination digits are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-232">Le numéro de version de l’extension du fournisseur de services n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-232">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-234">Le paramètre *dwFeature* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-234">The *dwFeature* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-236">L’application a appelé une fonctionnalité qui n’est pas disponible sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-236">The application invoked a feature that is not available on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR\_INVALGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-238">L’identificateur de groupe spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-238">The specified group identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR\_INVALLINEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-240">L’appel, l’appareil, le périphérique de ligne ou le handle de ligne spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-240">The specified call, device, line device, or line handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR\_INVALLINESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-242">La configuration de l’appareil ne peut pas être modifiée dans l’état actuel de la ligne.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-242">The device configuration may not be changed in the current line state.</span></span> <span data-ttu-id="ccbf1-243">La ligne peut être utilisée par une autre application ou un paramètre *dwLineStates* contient un ou plusieurs bits qui ne sont pas des [ \_ constantes LINEDEVSTATE](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="ccbf1-243">The line may be in use by another application or a *dwLineStates* parameter contains one or more bits that are not [LINEDEVSTATE\_ constants](linedevstate--constants.md).</span></span> <span data-ttu-id="ccbf1-244">La valeur **LINEERR \_ INVALLINESTATE** peut également indiquer que l’appareil est déconnecté ou hors service.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-244">The **LINEERR\_INVALLINESTATE** value can also indicate that the device is disconnected or out of service.</span></span> <span data-ttu-id="ccbf1-245">Ces États sont indiqués en définissant les bits correspondant aux valeurs d' *\_ InService* *LINEDEVSTATUSFLAGS \_ Connected* et LINEDEVSTATUSFLAGS sur 0 dans le membre **dwDevStatusFlags** de la structure [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) retournée par la fonction [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="ccbf1-245">These states are indicated by setting the bits corresponding to the *LINEDEVSTATUSFLAGS\_CONNECTED* and *LINEDEVSTATUSFLAGS\_INSERVICE* values to 0 in the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure returned by the [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR\_INVALLOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-247">L’identificateur d’emplacement permanent spécifié dans *dwLocation* est introuvable dans une entrée de la \[ section locations du \] Registre.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-247">The permanent location identifier specified in *dwLocation* could not be found in any entry in the \[Locations\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR\_INVALMEDIALIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-249">La liste de médias spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-249">The specified media list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR\_INVALMEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-251">La liste des types de média (modes) à analyser contient des informations non valides, le paramètre de type de média spécifié n’est pas valide ou le fournisseur de services ne prend pas en charge le type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-251">The list of media types (modes) to be monitored contains invalid information, the specified media type parameter is invalid, or the service provider does not support the specified media type.</span></span> <span data-ttu-id="ccbf1-252">Les types de médias pris en charge sur la ligne sont répertoriés dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="ccbf1-252">The media types supported on the line are listed in the **dwMediaModes** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR\_INVALMESSAGEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-254">Le nombre donné dans *dwMessageID* est en dehors de la plage spécifiée par le membre **dwNumCompletionMessages** dans la structure [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="ccbf1-254">The number given in *dwMessageID* is outside the range specified by the **dwNumCompletionMessages** member in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-256">Un paramètre ou une structure vers laquelle pointe un paramètre contient des informations non valides, un code de pays ou de région n’est pas valide, un handle de fenêtre n’est pas valide ou le paramètre de liste de transfert spécifié contient des informations non valides.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-256">A parameter or structure that a parameter points to contains invalid information, a country or region code is invalid, a window handle is invalid, or the specified forward list parameter contains invalid information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR\_INVALPARKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-258">L’identificateur de parc n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-258">The park identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR\_INVALPARKMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-260">Le mode de parc spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-260">The specified park mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-262">Le mot de passe spécifié n’est pas correct et l’action demandée n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-262">The specified password is not correct and the requested action has not been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-264">L’application a utilisé un mot de passe non valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-264">The application used an invalid password.</span></span> <span data-ttu-id="ccbf1-265">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-265">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-267">Un ou plusieurs des paramètres de pointeur spécifiés (tels que *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* et *lpToneList*) ne sont pas valides, ou un pointeur obligatoire vers un paramètre de sortie a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-267">One or more of the specified pointer parameters (such as *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps*, and *lpToneList*) are invalid, or a required pointer to an output parameter is **NULL**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR\_INVALPRIVSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-269">Un indicateur ou une combinaison d’indicateurs non valide a été défini pour le paramètre *dwPrivileges* .</span><span class="sxs-lookup"><span data-stu-id="ccbf1-269">An invalid flag or combination of flags was set for the *dwPrivileges* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR\_INVALRATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-271">Le taux spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-271">The specified rate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR\_INVALREQUESTMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-273">L’indicateur [**LINEREQUESTMODE**](linerequestmode--constants.md) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-273">The [**LINEREQUESTMODE**](linerequestmode--constants.md) indicator is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR\_INVALTERMINALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-275">L’identificateur de terminal spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-275">The specified terminal identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR\_INVALTERMINALMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-277">Le paramètre du mode terminal spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-277">The specified terminal modes parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR\_INVALTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-279">Les délais d’attente ne sont pas pris en charge ou une valeur se trouve en dehors de la plage valide spécifiée dans [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="ccbf1-279">Timeouts are not supported or a value falls outside the valid range specified in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR\_INVALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-281">Le ton personnalisé spécifié ne représente pas un ton valide ou est constitué d’un trop grand nombre de fréquences ou la structure tonale spécifiée ne décrit pas un ton valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-281">The specified custom tone does not represent a valid tone or is made up of too many frequencies or the specified tone structure does not describe a valid tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR\_INVALTONELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-283">La liste de tonalités spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-283">The specified tone list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR\_INVALTONEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-285">Le paramètre de mode de tonalité spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-285">The specified tone mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR\_INVALTRANSFERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-287">Le paramètre de mode de transfert spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-287">The specified transfer mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR\_LINEMAPPERFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-289">LINEMAPPER était la valeur passée dans le paramètre *dwDeviceID* , mais aucune ligne ne correspond aux critères spécifiés dans le paramètre *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="ccbf1-289">LINEMAPPER was the value passed in the *dwDeviceID* parameter, but no lines were found that match the requirements specified in the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOconference**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR\_NOCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-291">L’appel spécifié n’est pas un handle d’appel de conférence ou un appel de participant.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-291">The specified call is not a conference call handle or a participant call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NOdevice**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-293">L’identificateur de périphérique spécifié, qui était précédemment valide, n’est plus accepté, car l’appareil associé a été supprimé du système depuis le dernier initialisation de l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-293">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized.</span></span> <span data-ttu-id="ccbf1-294">Sinon, le périphérique de ligne n’a aucun appareil associé pour la classe d’appareil donnée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-294">Alternately, the line device has no associated device for the given device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOdriver**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-296">Soit Tapiaddr.dll est introuvable, soit le fournisseur de service téléphonique pour l’appareil spécifié a détecté que l’un de ses composants est manquant ou endommagé d’une façon qui n’a pas été détectée lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-296">Either Tapiaddr.dll could not be located or the telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="ccbf1-297">L’utilisateur doit être invité à utiliser le panneau de configuration de la téléphonie pour corriger le problème.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-297">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-299">Mémoire insuffisante pour effectuer l’opération ou impossible de verrouiller la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-299">Insufficient memory to perform the operation, or unable to lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-301">Un fournisseur de services de téléphonie qui ne prend pas en charge plusieurs instances est listé plusieurs fois dans la \[ section fournisseurs du \] Registre.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-301">A telephony service provider that does not support multiple instances is listed more than once in the \[Providers\] section in the registry.</span></span> <span data-ttu-id="ccbf1-302">L’application doit demander à l’utilisateur d’utiliser le panneau de configuration de la téléphonie pour supprimer le pilote dupliqué.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-302">The application should advise the user to use the Telephony Control Panel to remove the duplicated driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-304">Plusieurs instances de ce fournisseur de services ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-304">Multiple instances of this service provider are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOrequest**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR\_NOREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-306">Il n’y a actuellement aucune demande en attente du mode indiqué, ou l’application n’est plus la priorité la plus élevée pour le mode de demande spécifié.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-306">There currently is no request pending of the indicated mode, or the application is no longer the highest-priority application for the specified request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-308">L’application n’a pas de privilège de propriétaire pour l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-308">The application does not have owner privilege to the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ NOTREGISTERED**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR\_NOTREGISTERED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-310">L’application n’est pas inscrite en tant que destinataire de la demande pour le mode de requête indiqué.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-310">The application is not registered as a request recipient for the indicated request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-312">L’opération a échoué pour une raison non spécifiée ou inconnue.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-312">The operation failed for an unspecified or unknown reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-314">L’opération n’est pas disponible, par exemple pour l’appareil donné ou la ligne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-314">The operation is not available, such as for the given device or specified line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR\_RATEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-316">Actuellement, le fournisseur de services n’a pas suffisamment de bande passante disponible pour la vitesse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-316">The service provider currently does not have enough bandwidth available for the specified rate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**Réinit LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-318">Si la réinitialisation TAPI a été demandée, par exemple suite à l’ajout ou à la suppression d’un fournisseur de services de téléphonie, les demandes [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)ou [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) sont rejetées avec cette erreur jusqu’à ce que la dernière application arrête son utilisation de l’API (à l’aide de [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), et que les applications soient de nouveau autorisées à appeler **lineInitialize** ou **lineInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-318">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), or [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **lineInitialize** or **lineInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**Réinit LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-320">L’application a tenté d’initialiser TAPI deux fois.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-320">The application attempted to initialize TAPI twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-322">Plus de demandes sont en attente que l’appareil ne peut en gérer.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-322">More requests are pending than the device can handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-324">Ressources insuffisantes pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-324">Insufficient resources to complete the operation.</span></span> <span data-ttu-id="ccbf1-325">Par exemple, une ligne ne peut pas être ouverte en raison d’un surengagement de ressources dynamique.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-325">For example, a line cannot be opened due to a dynamic resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-327">Le membre **dwTotalSize** d’une structure ne spécifie pas suffisamment de mémoire pour contenir la partie fixe de la structure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-327">The **dwTotalSize** member of a structure does not specify enough memory to contain the fixed portion of the specified structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR\_TARGETNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-329">Une cible pour le transfert d’appel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-329">A target for the call handoff was not found.</span></span> <span data-ttu-id="ccbf1-330">Cela peut se produire si l’application nommée n’a pas ouvert la même ligne avec le \_ bit de propriétaire LINECALLPRIVILEGE dans le paramètre *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="ccbf1-330">This can occur if the named application did not open the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span> <span data-ttu-id="ccbf1-331">Ou, dans le cas de la remise en mode Media, aucune application n’a ouvert la même ligne avec le \_ bit de propriétaire LINECALLPRIVILEGE dans le paramètre *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) et avec le type de média spécifié dans le paramètre *dwMediaMode* ayant été spécifié dans le paramètre *dwMediaModes* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="ccbf1-331">Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) and with the media type specified in the *dwMediaMode* parameter having been specified in the *dwMediaModes* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR\_TARGETSELF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-333">L’application qui appelle cette opération est la cible du transfert indirect.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-333">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="ccbf1-334">Autrement dit, TAPI a déterminé que l’application appelante est également l’application de priorité la plus élevée pour le type de média donné.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-334">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR \_ non initialisé**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-336">L’opération a été appelée avant toute application appelée [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="ccbf1-336">The operation was invoked before any application called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR\_USERCANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-338">L’utilisateur a annulé l’appel.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-338">The user cancelled the call.</span></span> <span data-ttu-id="ccbf1-339">Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,2 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-339">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ccbf1-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR\_USERUSERINFOTOOBIG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ccbf1-341">La chaîne contenant les informations utilisateur-utilisateur dépasse le nombre maximal d’octets spécifié dans le membre **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** ou **dwUUISendUserUserInfoSize** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), ou la chaîne contenant les informations utilisateur-utilisateur est trop longue.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-341">The string containing user-user information exceeds the maximum number of bytes specified in the **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize**, or **dwUUISendUserUserInfoSize** member of [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), or the string containing user-user information is too long.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccbf1-342">Notes</span><span class="sxs-lookup"><span data-stu-id="ccbf1-342">Remarks</span></span>

<span data-ttu-id="ccbf1-343">Les valeurs 0xC0000000 à 0xFFFFFFFF sont disponibles pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-343">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions.</span></span> <span data-ttu-id="ccbf1-344">Les valeurs 0x80000000 à 0xBFFFFFFF sont réservées, tandis que 0x00000000 à 0x7FFFFFFF sont utilisées en tant qu’identificateurs de demande.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-344">The values 0x80000000 through 0xBFFFFFFF are reserved, while 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="ccbf1-345">Si une application obtient une erreur indiquant qu’elle n’est pas spécifiquement gérée (par exemple, une erreur définie par une extension spécifique à l’appareil), elle doit traiter l’erreur comme un \_ OPERATIONFAILED LINEERR (pour une raison non spécifiée).</span><span class="sxs-lookup"><span data-stu-id="ccbf1-345">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a LINEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

<span data-ttu-id="ccbf1-346">Lors de l’appel des \_ constantes LINEERR qui sont nouvelles avec TAPI 3,0, le fichier Tapierr.MC doit être mis à jour avec de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="ccbf1-346">When invoking the LINEERR\_constants which are new with TAPI 3.0, the Tapierr.mc file must be updated with new messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbf1-347">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccbf1-347">Requirements</span></span>



| <span data-ttu-id="ccbf1-348">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccbf1-348">Requirement</span></span> | <span data-ttu-id="ccbf1-349">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbf1-349">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ccbf1-350">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="ccbf1-350">TAPI version</span></span><br/> | <span data-ttu-id="ccbf1-351">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ccbf1-351">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ccbf1-352">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccbf1-352">Header</span></span><br/>       | <dl> <span data-ttu-id="ccbf1-353"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccbf1-353"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccbf1-354">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccbf1-354">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccbf1-355">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-355">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="ccbf1-356">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-356">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="ccbf1-357">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-357">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="ccbf1-358">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-358">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="ccbf1-359">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-359">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="ccbf1-360">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-360">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[<span data-ttu-id="ccbf1-361">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-361">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="ccbf1-362">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="ccbf1-362">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




