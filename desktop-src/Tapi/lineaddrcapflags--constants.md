---
description: Les \_ constantes d’indicateur de bit LINEADDRCAPFLAGS sont utilisées dans le membre dwAddrCapFlags de la structure de données LINEADDRESSCAPS pour décrire différentes fonctions d’adresse booléennes.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Constantes LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532820"
---
# <a name="lineaddrcapflags_-constants"></a><span data-ttu-id="41bb1-103">\_Constantes LINEADDRCAPFLAGS</span><span class="sxs-lookup"><span data-stu-id="41bb1-103">LINEADDRCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="41bb1-104">Les  \_ constantes d’indicateur de bit LINEADDRCAPFLAGS sont utilisées dans le membre **dwAddrCapFlags** de la structure de données [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) pour décrire différentes fonctions d’adresse booléennes.</span><span class="sxs-lookup"><span data-stu-id="41bb1-104">The **LINEADDRCAPFLAGS**\_ bit-flag constants are used in the **dwAddrCapFlags** member of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure to describe various Boolean address capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="41bb1-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**</span><span class="sxs-lookup"><span data-stu-id="41bb1-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS\_ACCEPTTOALERT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-106">**True** si un appel d’offre doit être accepté à l’aide de [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) pour commencer à alerter les utilisateurs aux deux extrémités de l’appel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="41bb1-106">**TRUE** if an offering call must be accepted using [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) to start alerting the users at both ends of the call; otherwise, **FALSE**.</span></span> <span data-ttu-id="41bb1-107">Cela est généralement utilisé uniquement avec RNIS.</span><span class="sxs-lookup"><span data-stu-id="41bb1-107">This is typically only used with ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**</span><span class="sxs-lookup"><span data-stu-id="41bb1-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS\_ACDGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-109">L’adresse prend en charge les [groupes ACD](about-call-center-controls.md#acd-group-object) en relation avec les opérations du centre d’appels.</span><span class="sxs-lookup"><span data-stu-id="41bb1-109">The address supports [ACD Groups](about-call-center-controls.md#acd-group-object) in connection with call center operations.</span></span> <span data-ttu-id="41bb1-110">Pour plus d’informations sur les groupes de ACD, consultez [à propos des contrôles du centre d’appels](./about-call-center-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="41bb1-110">See [About Call Center Controls](./about-call-center-controls.md) for additional information on ACD groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ reconnexion automatique**</span><span class="sxs-lookup"><span data-stu-id="41bb1-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS\_AUTORECONNECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-112">Spécifie si la suppression d’un appel de consultation se reconnecte automatiquement à l’appel sur la suspension de la consultation.</span><span class="sxs-lookup"><span data-stu-id="41bb1-112">Specifies whether dropping a consultation call automatically reconnects to the call on consultation hold.</span></span> <span data-ttu-id="41bb1-113">**True** si la reconnexion se produit automatiquement ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="41bb1-113">**TRUE** if reconnect happens automatically; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="41bb1-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS\_BLOCKIDDEFAULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-115">Spécifie si le réseau envoie ou bloque par défaut les informations relatives à l’ID de l’appelant lors d’un appel sur cette adresse.</span><span class="sxs-lookup"><span data-stu-id="41bb1-115">Specifies whether the network by default sends or blocks caller ID information when making a call on this address.</span></span> <span data-ttu-id="41bb1-116">Si la **valeur est true**, les informations d’identificateur sont bloquées par défaut ; Si la **valeur est false**, les informations d’identificateur sont transmises par défaut.</span><span class="sxs-lookup"><span data-stu-id="41bb1-116">If **TRUE**, identifier information is blocked by default; if **FALSE**, identifier information is transmitted by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="41bb1-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS\_BLOCKIDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-118">Spécifie si le paramètre par défaut pour l’envoi ou le blocage des informations d’ID de l’appelant peut être substitué par appel.</span><span class="sxs-lookup"><span data-stu-id="41bb1-118">Specifies whether the default setting for sending or blocking of caller ID information can be overridden per call.</span></span> <span data-ttu-id="41bb1-119">Si la **valeur est true**, le remplacement est possible ; Si la **valeur est false**, le remplacement n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="41bb1-119">If **TRUE**, override is possible; if **FALSE**, override is not possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="41bb1-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-121">Spécifie si les identificateurs de saisie semi-automatique retournés par [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) sont utiles et uniques.</span><span class="sxs-lookup"><span data-stu-id="41bb1-121">Specifies whether the completion identifiers returned by [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) are useful and unique.</span></span> <span data-ttu-id="41bb1-122">**True** si utile ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="41bb1-122">**TRUE** if useful; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**</span><span class="sxs-lookup"><span data-stu-id="41bb1-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS\_CONFDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-124">**True** si [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) sur un appel de conférence parent a également pour effet secondaire de supprimer (c’est-à-dire déconnecter) les autres parties impliquées dans l’appel de la Conférence ; **False** si la suppression d’un appel de conférence autorise toujours les autres parties à communiquer entre elles.</span><span class="sxs-lookup"><span data-stu-id="41bb1-124">**TRUE** if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on a conference call parent also has the side effect of dropping (that is, disconnecting) the other parties involved in the conference call; **FALSE** if dropping a conference call still allows the other parties to talk among themselves.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**</span><span class="sxs-lookup"><span data-stu-id="41bb1-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS\_CONFERENCEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-126">Spécifie si un appel bloqué peut être mis en conférence.</span><span class="sxs-lookup"><span data-stu-id="41bb1-126">Specifies whether a hard-held call can be conferenced to.</span></span> <span data-ttu-id="41bb1-127">Souvent, seuls les appels au blocage de la consultation peuvent être ajoutés à en tant qu’appel de conférence.</span><span class="sxs-lookup"><span data-stu-id="41bb1-127">Often, only calls on consultation hold can be added to as a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**</span><span class="sxs-lookup"><span data-stu-id="41bb1-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS\_CONFERENCEMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-129">Spécifie si un appel entièrement nouveau peut être établi pour une utilisation en tant qu’appel de consultation (à ajouter) lors d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="41bb1-129">Specifies whether an entirely new call can be established for use as a consultation call (to add) on conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="41bb1-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-131">Spécifie si le téléphone de la partie appelée peut être automatiquement forcé offhook lors des appels.</span><span class="sxs-lookup"><span data-stu-id="41bb1-131">Specifies whether the called party's phone can automatically be forced offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ composé**</span><span class="sxs-lookup"><span data-stu-id="41bb1-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS\_DIALED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-133">Spécifie si une adresse de destination peut être numérotée sur cette adresse pour effectuer un appel.</span><span class="sxs-lookup"><span data-stu-id="41bb1-133">Specifies whether a destination address can be dialed on this address for making a call.</span></span> <span data-ttu-id="41bb1-134">**True** si une adresse de destination doit être composée ; **False** si l’adresse de destination est fixe (comme avec un « téléphone à chaud »).</span><span class="sxs-lookup"><span data-stu-id="41bb1-134">**TRUE** if a destination address must be dialed; **FALSE** if the destination address is fixed (as with a "hot phone").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**</span><span class="sxs-lookup"><span data-stu-id="41bb1-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS\_FWDBUSYNAADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-136">Spécifie si le transfert d’appels pour Busy et pour aucune réponse peut utiliser des adresses de transfert différentes.</span><span class="sxs-lookup"><span data-stu-id="41bb1-136">Specifies whether call forwarding for busy and for no answer can use different forwarding addresses.</span></span> <span data-ttu-id="41bb1-137">Cet indicateur n’a de sens que si le transfert pour la disponibilité et l’absence de réponse peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="41bb1-137">This flag is meaningful only if forwarding for busy and for no answer can be controlled separately.</span></span> <span data-ttu-id="41bb1-138">Cet indicateur a la **valeur true** si le transfert pour Busy et pour aucune réponse peut utiliser des adresses de destination différentes ; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="41bb1-138">This flag is **TRUE** if forwarding for busy and for no answer can use different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**</span><span class="sxs-lookup"><span data-stu-id="41bb1-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS\_FWDCONSULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-140">Spécifie si le transfert d’appels implique l’établissement d’un appel de consultation.</span><span class="sxs-lookup"><span data-stu-id="41bb1-140">Specifies whether call forwarding involves the establishment of a consultation call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**</span><span class="sxs-lookup"><span data-stu-id="41bb1-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS\_FWDINTEXTADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-142">Spécifie si les appels internes et externes peuvent être transférés vers différentes adresses de transfert.</span><span class="sxs-lookup"><span data-stu-id="41bb1-142">Specifies whether internal and external calls can be forwarded to different forwarding addresses.</span></span> <span data-ttu-id="41bb1-143">Cet indicateur est significatif uniquement si le transfert d’appels internes et externes peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="41bb1-143">This flag is meaningful only if forwarding of internal and external calls can be controlled separately.</span></span> <span data-ttu-id="41bb1-144">Cet indicateur a la **valeur true** si les appels internes et externes peuvent être transférés vers des adresses de destination différentes ; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="41bb1-144">This flag is **TRUE** if internal and external calls can be forwarded to different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**</span><span class="sxs-lookup"><span data-stu-id="41bb1-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS\_FWDNUMRINGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-146">Spécifie si le nombre d’anneaux pour une réponse de non-réponse peut être spécifié lors du transfert d’appels en l’absence de réponse.</span><span class="sxs-lookup"><span data-stu-id="41bb1-146">Specifies whether the number of rings for a no-answer can be specified when forwarding calls on no answer.</span></span> <span data-ttu-id="41bb1-147">Si la **valeur est true**, la plage valide est fournie dans les membres **dwMinFwdNumRings** et **dwMaxFwdNumRings** de la structure [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="41bb1-147">If **TRUE**, the valid range is provided in the **dwMinFwdNumRings** and **dwMaxFwdNumRings** members of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**</span><span class="sxs-lookup"><span data-stu-id="41bb1-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS\_FWDSTATUSVALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-149">Spécifie si l’état de transfert dans la structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) pour cette adresse est valide ou s’il s’agit d’une « meilleure estimation », en raison de l’absence de confirmation exacte par le commutateur ou le réseau.</span><span class="sxs-lookup"><span data-stu-id="41bb1-149">Specifies whether the forwarding status in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure for this address is valid or is at most a "best estimate," given absence of accurate confirmation by the switch or network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**</span><span class="sxs-lookup"><span data-stu-id="41bb1-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS\_HOLDMAKESNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-151">Lorsqu’un appel sur cette adresse est placé en attente (à l’aide de LineHold ou d’une action externe), un nouvel appel est automatiquement créé (probablement dans la [**di**](/windows/desktop/api/Tapi/nf-tapi-linehold) LINECALLSTATE \_ ).</span><span class="sxs-lookup"><span data-stu-id="41bb1-151">When a call on this address is placed on hold (using [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) or external action), a new call is automatically created (most likely in LINECALLSTATE\_DIALTONE).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="41bb1-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS\_NOEXTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-153">L’adresse est associée à une ligne interne sur un PBX qui est limitée de telle façon qu’elle ne peut pas être utilisée pour passer des appels à une adresse en dehors du commutateur (par exemple, il s’agit d’un interphone).</span><span class="sxs-lookup"><span data-stu-id="41bb1-153">The address is associated with an internal line on a PBX that is restricted in such a way that it cannot be used to place calls to an address outside the switch (for example, it is an intercom).</span></span> <span data-ttu-id="41bb1-154">L’application peut utiliser cette indication pour aider l’utilisateur à sélectionner l’apparence d’appel correcte à utiliser pour effectuer un appel.</span><span class="sxs-lookup"><span data-stu-id="41bb1-154">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="41bb1-155">Lorsque ce bit est désactivé, il n’indique pas nécessairement que l’adresse peut être utilisée pour effectuer des appels externes, car le fournisseur de services ne peut pas être Cognizant du type de ligne.</span><span class="sxs-lookup"><span data-stu-id="41bb1-155">When this bit is off, it does not necessarily indicate that the address can be used to make external calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="41bb1-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS\_NOINTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-157">L’adresse est associée à une ligne directe (Trunk) directe et ne peut pas être utilisée pour effectuer des appels internes sur un PBX.</span><span class="sxs-lookup"><span data-stu-id="41bb1-157">The address is associated with a direct CO line (trunk), and cannot be used to make internal calls on a PBX.</span></span> <span data-ttu-id="41bb1-158">L’application peut utiliser cette indication pour aider l’utilisateur à sélectionner l’apparence d’appel correcte à utiliser pour effectuer un appel.</span><span class="sxs-lookup"><span data-stu-id="41bb1-158">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="41bb1-159">Lorsque ce bit est désactivé, il n’indique pas nécessairement que l’adresse peut être utilisée pour effectuer des appels internes, car le fournisseur de services ne peut pas être Cognizant du type de ligne.</span><span class="sxs-lookup"><span data-stu-id="41bb1-159">When this bit is off, it does not necessarily indicate that the address can be used to make internal calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**</span><span class="sxs-lookup"><span data-stu-id="41bb1-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS\_NOPSTNADDRESSTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-161">Cette adresse ne prend pas en charge la traduction d’adresses de réseau téléphonique commutée publique.</span><span class="sxs-lookup"><span data-stu-id="41bb1-161">This address does not support public switched telephone network address translation.</span></span> <span data-ttu-id="41bb1-162">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="41bb1-162">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="41bb1-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-164">Spécifie si le téléphone du tiers d’origine peut être automatiquement pris offhook lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="41bb1-164">Specifies whether the originating party's phone can automatically be taken offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**</span><span class="sxs-lookup"><span data-stu-id="41bb1-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS\_PARTIALDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-166">Spécifie si la numérotation partielle est disponible.</span><span class="sxs-lookup"><span data-stu-id="41bb1-166">Specifies whether partial dialing is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**</span><span class="sxs-lookup"><span data-stu-id="41bb1-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS\_PICKUPCALLWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-168">**True** si [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut être utilisé pour récupérer un appel détecté par l’utilisateur en tant qu’appel en attente d’appel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="41bb1-168">**TRUE** if [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can be used to pick up a call detected by the user as a call-waiting call; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**</span><span class="sxs-lookup"><span data-stu-id="41bb1-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS\_PICKUPGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-170">Spécifie si un identificateur de groupe est requis pour la collecte d’appels.</span><span class="sxs-lookup"><span data-stu-id="41bb1-170">Specifies whether a group identifier is required for call pickup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**</span><span class="sxs-lookup"><span data-stu-id="41bb1-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS\_PREDICTIVEDIALER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-172">Cette adresse a amélioré les fonctionnalités de surveillance de la progression des appels qui peuvent être appliquées aux appels sortants afin de déterminer les États d’appel tels que les *rappels*, les éléments *occupés*, les *specialinfo* et les *connexions*, ou le type de média de l’appareil qui répond à l’appel.</span><span class="sxs-lookup"><span data-stu-id="41bb1-172">This address has enhanced call progress monitoring capabilities which can be applied to outgoing calls to determine call states such as *ringback*, *busy*, *specialinfo*, and *connected*, or the media type of the device answering the call.</span></span> <span data-ttu-id="41bb1-173">Il peut également avoir la possibilité de transférer automatiquement les appels sortants vers une autre adresse lorsqu’un appel atteint un ensemble prédéfini d’États.</span><span class="sxs-lookup"><span data-stu-id="41bb1-173">It may also have the ability to automatically transfer outgoing calls to another address when a call reaches any of a predefined set of states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_file d’attente LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="41bb1-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-175">Cette adresse n’est pas associée à une station ou un appareil physique particulier, mais constitue un point de suspension où les appels attendent un traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="41bb1-175">This address is not associated with a particular station or physical device, but is a holding place where calls wait for further processing.</span></span> <span data-ttu-id="41bb1-176">Les appels placés dans la file d’attente peuvent recevoir un traitement particulier.</span><span class="sxs-lookup"><span data-stu-id="41bb1-176">The calls placed in the queue may receive a particular treatment.</span></span> <span data-ttu-id="41bb1-177">Elles peuvent également être automatiquement transférées lorsqu’une ressource particulière est disponible (par exemple, si la file d’attente est une file d’attente ACD et que des appels attendent un agent disponible).</span><span class="sxs-lookup"><span data-stu-id="41bb1-177">They may also be automatically transferred when a particular resource becomes available (for example, if the queue is an ACD queue and calls are waiting for an available agent).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**</span><span class="sxs-lookup"><span data-stu-id="41bb1-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS\_ROUTEPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-179">Cette adresse n’est pas associée à une station ou un appareil physique particulier, mais est un emplacement de stockage où les appels attendent le routage par l’application (l’application examine l’adresse appelée et peut rediriger l’appel vers une autre adresse).</span><span class="sxs-lookup"><span data-stu-id="41bb1-179">This address is not associated with a particular station or physical device, but is a holding place where calls wait for routing by the application (the application examines the called address, and can redirect the call to another address).</span></span> <span data-ttu-id="41bb1-180">L’appel peut également être transféré automatiquement en cas d’expiration du délai d’attente de routage (le commutateur suppose généralement un routage par défaut).</span><span class="sxs-lookup"><span data-stu-id="41bb1-180">The call can also be automatically transferred if a routing timeout expires (the switch usually assumes a default routing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ sécurisé**</span><span class="sxs-lookup"><span data-stu-id="41bb1-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-182">Spécifie si les appels sur cette adresse peuvent être sécurisés au moment de la configuration de l’appel.</span><span class="sxs-lookup"><span data-stu-id="41bb1-182">Specifies whether calls on this address can be made secure at call-setup time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**</span><span class="sxs-lookup"><span data-stu-id="41bb1-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS\_SETCALLINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-184">L’application peut choisir de définir le membre **CallingPartyID** dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) lors de l’appel de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) et d’autres fonctions qui acceptent une structure **LINECALLPARAMS** .</span><span class="sxs-lookup"><span data-stu-id="41bb1-184">The application can choose to set the **CallingPartyID** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) when calling [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) and other functions that accept a **LINECALLPARAMS** structure.</span></span> <span data-ttu-id="41bb1-185">Le fournisseur de services, si le contenu de l’identificateur est acceptable et qu’un chemin d’accès est disponible, transmettez l’identificateur au tiers appelé pour indiquer l’identité du tiers appelant.</span><span class="sxs-lookup"><span data-stu-id="41bb1-185">The service provider will, if the content of the identifier is acceptable and a path is available, pass the identifier along to the called party to indicate the identity of the calling party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**</span><span class="sxs-lookup"><span data-stu-id="41bb1-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS\_SETUPCONFNULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-187">Spécifie si la configuration d’un appel de conférence commence par un appel initial (**false**) ou sans appel initial (**true**).</span><span class="sxs-lookup"><span data-stu-id="41bb1-187">Specifies whether setting up a conference call starts out with an initial call (**FALSE**) or with no initial call (**TRUE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**</span><span class="sxs-lookup"><span data-stu-id="41bb1-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS\_TRANSFERHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-189">Spécifie si un appel bloqué peut être transféré.</span><span class="sxs-lookup"><span data-stu-id="41bb1-189">Specifies whether a hard-held call can be transferred.</span></span> <span data-ttu-id="41bb1-190">Souvent, seuls les appels au blocage de la consultation peuvent être transférés.</span><span class="sxs-lookup"><span data-stu-id="41bb1-190">Often, only calls on consultation hold can be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41bb1-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**</span><span class="sxs-lookup"><span data-stu-id="41bb1-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS\_TRANSFERMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41bb1-192">Spécifie si un appel entièrement nouveau peut être établi pour une utilisation en tant qu’appel de consultation lors du transfert.</span><span class="sxs-lookup"><span data-stu-id="41bb1-192">Specifies whether an entirely new call can be established for use as a consultation call on transfer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41bb1-193">Notes</span><span class="sxs-lookup"><span data-stu-id="41bb1-193">Remarks</span></span>

<span data-ttu-id="41bb1-194">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="41bb1-194">No extensibility.</span></span> <span data-ttu-id="41bb1-195">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="41bb1-195">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="41bb1-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41bb1-196">Requirements</span></span>



| <span data-ttu-id="41bb1-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41bb1-197">Requirement</span></span> | <span data-ttu-id="41bb1-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="41bb1-198">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="41bb1-199">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="41bb1-199">TAPI version</span></span><br/> | <span data-ttu-id="41bb1-200">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="41bb1-200">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="41bb1-201">En-tête</span><span class="sxs-lookup"><span data-stu-id="41bb1-201">Header</span></span><br/>       | <dl> <span data-ttu-id="41bb1-202"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="41bb1-202"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41bb1-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41bb1-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41bb1-204">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="41bb1-204">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[<span data-ttu-id="41bb1-205">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="41bb1-205">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="41bb1-206">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="41bb1-206">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="41bb1-207">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="41bb1-207">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="41bb1-208">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="41bb1-208">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="41bb1-209">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="41bb1-209">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="41bb1-210">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="41bb1-210">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[<span data-ttu-id="41bb1-211">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="41bb1-211">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="41bb1-212">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="41bb1-212">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

