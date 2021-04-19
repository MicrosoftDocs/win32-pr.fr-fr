---
description: Les termes suivants sont utiles pour comprendre la technologie TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 23331332-38bc-41b9-84c4-281722ddf563
title: C (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6fade540235ef6c68b42a0aba364038d674e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534174"
---
# <a name="c-telephony-api"></a><span data-ttu-id="a2340-103">C (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="a2340-103">C (Telephony API)</span></span>

<span data-ttu-id="a2340-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [e](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a2340-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a2340-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**classification des appels**</span><span class="sxs-lookup"><span data-stu-id="a2340-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**call classification**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-106">Processus TAPI qui signale les modifications apportées au type de flux multimédia (voix, télécopie, modem de données, etc.) pour les applications participantes.</span><span class="sxs-lookup"><span data-stu-id="a2340-106">TAPI process that reports changes in the type of media stream (voice, fax, data modem, and so on) to participating applications.</span></span>

</dd> <dt>

<span data-ttu-id="a2340-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**surveiller la progression de l’appel**</span><span class="sxs-lookup"><span data-stu-id="a2340-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**call progress monitoring**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-108">Processus d’écoute de tonalités audibles telles qu’une tonalité, des tonalités d’information spéciales, des signaux occupés et des tonalités de rappel pour déterminer l’état d’un appel (sa progression via le réseau).</span><span class="sxs-lookup"><span data-stu-id="a2340-108">The process of listening for audible tones such as a dial tone, special information tones, busy signals, and ringback tones to determine the state of a call (its progress through the network).</span></span>

</dd> <dt>

<span data-ttu-id="a2340-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**redirection d’appel**</span><span class="sxs-lookup"><span data-stu-id="a2340-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**call redirection**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-110">Fonction qui permet à une application de dévier un appel d’offre vers une autre adresse sans avoir d’abord répondu à l’appel.</span><span class="sxs-lookup"><span data-stu-id="a2340-110">A function that allows an application to deflect an offering call to another address without first answering the call.</span></span> <span data-ttu-id="a2340-111">La redirection d’appel diffère du transfert d’appel dans le sens où le transfert d’appel est effectué par le commutateur sans l’implication de l’application ; la redirection peut être effectuée appel par appel par l’application, par exemple, en fonction des informations d’ID de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="a2340-111">Call redirection differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information.</span></span> <span data-ttu-id="a2340-112">Il diffère du transfert d’appel dans le fait que le transfert d’un appel requiert la réponse initiale à l’appel.</span><span class="sxs-lookup"><span data-stu-id="a2340-112">It differs from call transfer in that transferring a call requires that the call first be answered.</span></span> <span data-ttu-id="a2340-113">Consultez Call *-ID*, *Caller-ID*, [*redirection ID*](r-tapgloss.md), [*ID de redirection*](r-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="a2340-113">See *called-ID*, *caller-ID*, [*redirecting ID*](r-tapgloss.md), [*redirection ID*](r-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2340-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**ID d’appel**</span><span class="sxs-lookup"><span data-stu-id="a2340-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**called-ID**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-115">Identifie l’adresse de destination d’origine d’un appel.</span><span class="sxs-lookup"><span data-stu-id="a2340-115">Identifies the original destination address of a call.</span></span> <span data-ttu-id="a2340-116">Consultez *appel redirection*.</span><span class="sxs-lookup"><span data-stu-id="a2340-116">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="a2340-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**ID appelant**</span><span class="sxs-lookup"><span data-stu-id="a2340-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**caller-ID**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-118">Identifie l’adresse d’origine d’un appel.</span><span class="sxs-lookup"><span data-stu-id="a2340-118">Identifies the originating address of a call.</span></span> <span data-ttu-id="a2340-119">Consultez *appel redirection*.</span><span class="sxs-lookup"><span data-stu-id="a2340-119">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="a2340-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**Bureau central**</span><span class="sxs-lookup"><span data-stu-id="a2340-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**central office**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-121">Service local de l’entreprise téléphonique qui fournit un service téléphonique dans un domaine spécifique.</span><span class="sxs-lookup"><span data-stu-id="a2340-121">Telephone company's local facility that provides telephone service in a specific area.</span></span> <span data-ttu-id="a2340-122">En règle générale, les lignes des abonnés sont jointes à l’équipement de commutation qui connecte les autres abonnés, localement et sur une longue distance.</span><span class="sxs-lookup"><span data-stu-id="a2340-122">Typically, subscribers' lines are joined to switching equipment that connects other subscribers to each other, locally and over long distance.</span></span> <span data-ttu-id="a2340-123">Également appelé *co*.</span><span class="sxs-lookup"><span data-stu-id="a2340-123">Also called *CO*.</span></span>

</dd> <dt>

<span data-ttu-id="a2340-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span><span class="sxs-lookup"><span data-stu-id="a2340-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-125">Service de téléphone professionnel proposé par une société de téléphone locale à partir d’un bureau central local.</span><span class="sxs-lookup"><span data-stu-id="a2340-125">A business telephone service offered by a local telephone company from a local, central office.</span></span>

</dd> <dt>

<span data-ttu-id="a2340-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**connexion centrée sur l’ordinateur**</span><span class="sxs-lookup"><span data-stu-id="a2340-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**computer-centric connection**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-127">Une connexion qui utilise une carte de complément d’ordinateur ou une zone externe connectée au réseau téléphonique et à l’ensemble téléphonique.</span><span class="sxs-lookup"><span data-stu-id="a2340-127">A connection that uses a computer add-in card or external box that is connected to both the telephone network and the phone set.</span></span> <span data-ttu-id="a2340-128">Comparer la [*connexion axée sur le téléphone*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="a2340-128">Compare [*phone-centric connection*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2340-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**ID connecté**</span><span class="sxs-lookup"><span data-stu-id="a2340-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**connected-ID**</span></span>
</dt> <dd>

<span data-ttu-id="a2340-130">Identificateur du tiers auquel l’appel a été réellement connecté.</span><span class="sxs-lookup"><span data-stu-id="a2340-130">Identifier for the party to which the call was actually connected.</span></span> <span data-ttu-id="a2340-131">Cela peut être différent du tiers appelé si l’appel a été détourné.</span><span class="sxs-lookup"><span data-stu-id="a2340-131">This may be different from the called party if the call was diverted.</span></span>

</dd> </dl>

 

 



