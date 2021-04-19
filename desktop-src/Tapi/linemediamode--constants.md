---
description: Les \_ constantes LINEMEDIAMODE décrivent les types de média (ou modes) d’une session ou d’un appel de communication.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Constantes LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539999"
---
# <a name="linemediamode_-constants"></a><span data-ttu-id="dfca0-103">\_Constantes LINEMEDIAMODE</span><span class="sxs-lookup"><span data-stu-id="dfca0-103">LINEMEDIAMODE\_ Constants</span></span>

<span data-ttu-id="dfca0-104">Les constantes **LINEMEDIAMODE \_** décrivent les types de média (ou modes) d’une session ou d’un appel de communication.</span><span class="sxs-lookup"><span data-stu-id="dfca0-104">The **LINEMEDIAMODE\_** constants describe media types (or modes)of a communications session or call.</span></span>

<dl> <dt>

<span data-ttu-id="dfca0-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**</span><span class="sxs-lookup"><span data-stu-id="dfca0-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE\_AUTOMATEDVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-106">L’énergie vocale a été détectée lors de l’appel et la voix est gérée localement par une application automatisée telle qu’une application de machine de réponse.</span><span class="sxs-lookup"><span data-stu-id="dfca0-106">Voice energy was detected on the call, and the voice is locally handled by an automated application such as with an answering machine application.</span></span> <span data-ttu-id="dfca0-107">Lorsqu’un fournisseur de services ne peut pas faire la distinction entre l’interactivité et la voix automatisée sur un appel entrant, il signale l’appel comme interactif vocal.</span><span class="sxs-lookup"><span data-stu-id="dfca0-107">When a service provider cannot distinguish between interactive and automated voice on an incoming call, it will report the call as interactive voice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**</span><span class="sxs-lookup"><span data-stu-id="dfca0-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE\_DATAMODEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-109">Une session de modem de données sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-109">A data modem session on the call.</span></span> <span data-ttu-id="dfca0-110">Les protocoles de modem actuels requièrent la station appelée pour initier le protocole de transfert.</span><span class="sxs-lookup"><span data-stu-id="dfca0-110">Current modem protocols require the called station to initiate the handshake.</span></span> <span data-ttu-id="dfca0-111">Pour un appel de modem de données entrant, l’application ne peut généralement pas effectuer de détection positive.</span><span class="sxs-lookup"><span data-stu-id="dfca0-111">For an incoming data modem call, the application can typically make no positive detection.</span></span> <span data-ttu-id="dfca0-112">La manière dont le fournisseur de services effectue cette détermination est son choix.</span><span class="sxs-lookup"><span data-stu-id="dfca0-112">How the service provider makes this determination is its choice.</span></span> <span data-ttu-id="dfca0-113">Par exemple, une période de silence juste après avoir répondu à un appel entrant peut être utilisée comme heuristique pour décider qu’il peut s’agir d’un appel de modem de données.</span><span class="sxs-lookup"><span data-stu-id="dfca0-113">For example, a period of silence just after answering an incoming call can be used as a heuristic to decide that this might be a data modem call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**</span><span class="sxs-lookup"><span data-stu-id="dfca0-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE\_ADSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-115">Session ADSI (ANALOG DISPLAY services interface) sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-115">An ADSI (Analog Display Services Interface) session on the call.</span></span> <span data-ttu-id="dfca0-116">ADSI améliore les appels vocaux avec des informations alphanumériques téléchargées sur le téléphone et l’utilisation de boutons logiciels sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="dfca0-116">ADSI enhances voice calls with alphanumeric information downloaded to the phone and the use of soft buttons on the phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**</span><span class="sxs-lookup"><span data-stu-id="dfca0-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE\_DIGITALDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-118">Flux de données numériques d’un format non spécifié.</span><span class="sxs-lookup"><span data-stu-id="dfca0-118">A digital data stream of unspecified format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**</span><span class="sxs-lookup"><span data-stu-id="dfca0-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE\_G3FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-120">Une télécopie de groupe 3 est envoyée ou reçue via l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-120">A group 3 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**</span><span class="sxs-lookup"><span data-stu-id="dfca0-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE\_G4FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-122">Une télécopie de groupe 4 est en cours d’envoi ou de réception sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-122">A group 4 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**</span><span class="sxs-lookup"><span data-stu-id="dfca0-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE\_INTERACTIVEVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-124">L’énergie vocale a été détectée lors de l’appel, et l’appel est traité comme un appel vocal interactif avec des humains aux deux extrémités.</span><span class="sxs-lookup"><span data-stu-id="dfca0-124">Voice energy was detected on the call, and the call is handled as an interactive voice call with humans on both ends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ mixte**</span><span class="sxs-lookup"><span data-stu-id="dfca0-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE\_MIXED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-126">Session mixte sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-126">A mixed session on the call.</span></span> <span data-ttu-id="dfca0-127">Mixed est l’un des services télématiques RNIS.</span><span class="sxs-lookup"><span data-stu-id="dfca0-127">Mixed is one of the ISDN telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**</span><span class="sxs-lookup"><span data-stu-id="dfca0-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE\_TDD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-129">Une session TDD (appareils de téléphonie pour les sourds) sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-129">A TDD (Telephony Devices for the Deaf) session on the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**</span><span class="sxs-lookup"><span data-stu-id="dfca0-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE\_TELETEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-131">Session TELETEX sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-131">A teletex session on the call.</span></span> <span data-ttu-id="dfca0-132">Teletex est l’un des services télématiques.</span><span class="sxs-lookup"><span data-stu-id="dfca0-132">Teletex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**\_télex LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="dfca0-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE\_TELEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-134">Session de télex sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-134">A telex session on the call.</span></span> <span data-ttu-id="dfca0-135">Le télex est l’un des services télématiques.</span><span class="sxs-lookup"><span data-stu-id="dfca0-135">Telex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**\_vidéo LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="dfca0-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE\_VIDEO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-137">Le type de média de l’appel est vidéo.</span><span class="sxs-lookup"><span data-stu-id="dfca0-137">The media type of the call is video.</span></span> <span data-ttu-id="dfca0-138">(TAPI versions 2,1 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="dfca0-138">(TAPI versions 2.1 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**</span><span class="sxs-lookup"><span data-stu-id="dfca0-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE\_VIDEOTEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-140">Une session Videotex sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-140">A videotex session on the call.</span></span> <span data-ttu-id="dfca0-141">Videotex est l’un des services télématiques.</span><span class="sxs-lookup"><span data-stu-id="dfca0-141">Videotex is one the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**</span><span class="sxs-lookup"><span data-stu-id="dfca0-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE\_VOICEVIEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-143">Le type de média de l’appel est VoiceView.</span><span class="sxs-lookup"><span data-stu-id="dfca0-143">The media type of the call is VoiceView.</span></span> <span data-ttu-id="dfca0-144">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="dfca0-144">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfca0-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="dfca0-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dfca0-146">Un flux de média existe mais son mode n’est pas actuellement connu et peut devenir connu ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="dfca0-146">A media stream exists but its mode is not currently known and may become known later.</span></span> <span data-ttu-id="dfca0-147">Cela correspond à un appel avec un type de média non classifié.</span><span class="sxs-lookup"><span data-stu-id="dfca0-147">This would correspond to a call with an unclassified media type.</span></span> <span data-ttu-id="dfca0-148">Dans les environnements de téléphonie analogique classiques, le type de média d’un appel entrant peut être inconnu jusqu’à ce que l’appel ait répondu et que le flux de média ait été filtré pour effectuer une détermination.</span><span class="sxs-lookup"><span data-stu-id="dfca0-148">In typical analog telephony environments, an incoming call's media type may be unknown until after the call has been answered and the media stream has been filtered to make a determination.</span></span>

<span data-ttu-id="dfca0-149">Si l’indicateur de mode multimédia inconnu est défini, d’autres indicateurs multimédias peuvent également être définis.</span><span class="sxs-lookup"><span data-stu-id="dfca0-149">If the unknown media-mode flag is set, other media flags can also be set.</span></span> <span data-ttu-id="dfca0-150">Cela permet d’indiquer que le média est inconnu, mais qu’il est susceptible d’être l’un des autres types de médias sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="dfca0-150">This is used to signify that the media is unknown but that it is likely to be one of the other selected media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfca0-151">Notes</span><span class="sxs-lookup"><span data-stu-id="dfca0-151">Remarks</span></span>

<span data-ttu-id="dfca0-152">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="dfca0-152">All 32 bits are reserved.</span></span>

<span data-ttu-id="dfca0-153">Notez que le mode porteur et le type de média sont des notions différentes.</span><span class="sxs-lookup"><span data-stu-id="dfca0-153">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="dfca0-154">Le mode de support d’un appel est une indication de la qualité de la connexion téléphonique, comme fourni principalement par le réseau.</span><span class="sxs-lookup"><span data-stu-id="dfca0-154">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="dfca0-155">Le type de média d’un appel est une indication du type de flux d’informations échangé sur cet appel.</span><span class="sxs-lookup"><span data-stu-id="dfca0-155">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="dfca0-156">Le modem de télécopie ou de données de groupe 3 est un type de support qui utilise un appel avec un mode de support vocal 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="dfca0-156">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

<span data-ttu-id="dfca0-157">Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser cette \_ valeur LINEMEDIAMODE si elle n’est pas prise en charge sur la version négociée.</span><span class="sxs-lookup"><span data-stu-id="dfca0-157">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEMEDIAMODE\_ value if not supported on the negotiated version.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfca0-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfca0-158">Requirements</span></span>



| <span data-ttu-id="dfca0-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfca0-159">Requirement</span></span> | <span data-ttu-id="dfca0-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfca0-160">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dfca0-161">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="dfca0-161">TAPI version</span></span><br/> | <span data-ttu-id="dfca0-162">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="dfca0-162">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dfca0-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfca0-163">Header</span></span><br/>       | <dl> <span data-ttu-id="dfca0-164"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfca0-164"><dt>Tapi.h</dt></span></span> </dl> |



 

 




