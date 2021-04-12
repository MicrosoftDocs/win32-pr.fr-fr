---
title: Create-Session
description: Utilisez le paquet Create-Session pour demander une session de chargement avec le serveur BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462515"
---
# <a name="create-session"></a><span data-ttu-id="a692e-104">Create-Session</span><span class="sxs-lookup"><span data-stu-id="a692e-104">Create-Session</span></span>

<span data-ttu-id="a692e-105">Utilisez le paquet **Create-session** pour demander une session de chargement avec le serveur bits.</span><span class="sxs-lookup"><span data-stu-id="a692e-105">Use the **Create-Session** packet to request an upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a><span data-ttu-id="a692e-106">headers</span><span class="sxs-lookup"><span data-stu-id="a692e-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="a692e-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits</span><span class="sxs-lookup"><span data-stu-id="a692e-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="a692e-108">Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="a692e-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="a692e-109">Remplacez l’URL distante par l’URI absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="a692e-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="a692e-110">Remplacez généralement l’URL distante par le nom de fichier distant du travail.</span><span class="sxs-lookup"><span data-stu-id="a692e-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="a692e-111">Pour plus d’informations sur l’équilibrage de charge réseau, consultez l’en-tête BITS-Host-ID.</span><span class="sxs-lookup"><span data-stu-id="a692e-111">For network load balancing considerations, see the BITS-Host-Id header.</span></span>

</dd> <dt>

<span data-ttu-id="a692e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="a692e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="a692e-113">Identifie ce paquet de demande en tant que Create-Session paquet.</span><span class="sxs-lookup"><span data-stu-id="a692e-113">Identifies this request packet as a Create-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="a692e-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="a692e-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span></span>
</dt> <dd>

<span data-ttu-id="a692e-115">Liste délimitée par des espaces des protocoles pris en charge par le client.</span><span class="sxs-lookup"><span data-stu-id="a692e-115">Space-delimited list of the protocols that the client supports.</span></span> <span data-ttu-id="a692e-116">Utilisez des GUID de chaîne pour identifier les protocoles.</span><span class="sxs-lookup"><span data-stu-id="a692e-116">Use string GUIDs to identify the protocols.</span></span> <span data-ttu-id="a692e-117">Spécifiez la liste par ordre de préférence, du plus au moins préféré.</span><span class="sxs-lookup"><span data-stu-id="a692e-117">Specify the list in order of preference from most to least preferred.</span></span> <span data-ttu-id="a692e-118">Le tableau suivant répertorie le protocole pris en charge par le client BITS.</span><span class="sxs-lookup"><span data-stu-id="a692e-118">The following table lists the protocol that the BITS client supports.</span></span> <span data-ttu-id="a692e-119">Remplacer {GUID1}... {guidn} avec un ou plusieurs GUID de chaîne dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a692e-119">Replace {guid1} ... {guidN} with one or more string GUIDs from the list.</span></span>



| <span data-ttu-id="a692e-120">Protocol</span><span class="sxs-lookup"><span data-stu-id="a692e-120">Protocol</span></span>                                          | <span data-ttu-id="a692e-121">Description</span><span class="sxs-lookup"><span data-stu-id="a692e-121">Description</span></span>                         |
|---------------------------------------------------|-------------------------------------|
| <span data-ttu-id="a692e-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span><span class="sxs-lookup"><span data-stu-id="a692e-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span></span><br/> | <span data-ttu-id="a692e-123">Protocole de téléchargement BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="a692e-123">BITS 1.5 Upload Protocol</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a692e-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a692e-124">Remarks</span></span>

<span data-ttu-id="a692e-125">Vous devez envoyer un paquet [**ping**](ping.md) pour établir une connexion http avant d’envoyer le paquet Create-Session.</span><span class="sxs-lookup"><span data-stu-id="a692e-125">You should send a [**Ping**](ping.md) packet to establish an HTTP connection before sending the Create-Session packet.</span></span> <span data-ttu-id="a692e-126">Le paquet Create-Session peut également établir la connexion ; Toutefois, le Create-Session paquet est moins efficace.</span><span class="sxs-lookup"><span data-stu-id="a692e-126">The Create-Session packet can also establish the connection; however, the Create-Session packet is less efficient.</span></span>

<span data-ttu-id="a692e-127">Le serveur sélectionne le protocole qu’il souhaite utiliser dans la liste fournie par le client dans l’en-tête BITS-Supported-Protocols.</span><span class="sxs-lookup"><span data-stu-id="a692e-127">The server selects the protocol it wants to use from the list the client provides in the BITS-Supported-Protocols header.</span></span> <span data-ttu-id="a692e-128">Le serveur retourne le protocole sélectionné dans l’en-tête BITS-Protocol de l’accusé de réception pour le paquet de réponse de [**création de session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="a692e-128">The server returns the selected protocol in the BITS-Protocol header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

<span data-ttu-id="a692e-129">Le client s’attend à ce que le serveur retourne un [**accusé de réception pour le paquet de réponse de création de session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="a692e-129">The client expects the server to return an [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="a692e-130">Si le serveur a pu établir une session, le client utilise le paquet de demande de [**fragment**](fragment.md) pour envoyer des plages du fichier au serveur.</span><span class="sxs-lookup"><span data-stu-id="a692e-130">If the server was able to establish a session, the client uses the [**Fragment**](fragment.md) request packet to send ranges of the file to the server.</span></span>

## <a name="see-also"></a><span data-ttu-id="a692e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a692e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a692e-132">**ACK pour Create-session**</span><span class="sxs-lookup"><span data-stu-id="a692e-132">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="a692e-133">**Fragment**</span><span class="sxs-lookup"><span data-stu-id="a692e-133">**Fragment**</span></span>](fragment.md)
</dt> <dt>

[<span data-ttu-id="a692e-134">**Ping**</span><span class="sxs-lookup"><span data-stu-id="a692e-134">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 





