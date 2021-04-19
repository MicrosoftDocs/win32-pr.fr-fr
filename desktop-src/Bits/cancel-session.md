---
title: Cancel-Session
description: Utilisez le paquet Cancel-Session pour mettre fin à la session de téléchargement avec le serveur BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session BITS
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509822"
---
# <a name="cancel-session"></a><span data-ttu-id="d8b99-104">Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="d8b99-104">Cancel-Session</span></span>

<span data-ttu-id="d8b99-105">Utilisez le paquet **Cancel-session** pour mettre fin à la session de téléchargement avec le serveur bits.</span><span class="sxs-lookup"><span data-stu-id="d8b99-105">Use the **Cancel-Session** packet to terminate the upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="d8b99-106">headers</span><span class="sxs-lookup"><span data-stu-id="d8b99-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="d8b99-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits</span><span class="sxs-lookup"><span data-stu-id="d8b99-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="d8b99-108">Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="d8b99-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="d8b99-109">Remplacez l’URL distante par l’URI absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="d8b99-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="d8b99-110">Remplacez généralement l’URL distante par le nom de fichier distant du travail.</span><span class="sxs-lookup"><span data-stu-id="d8b99-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="d8b99-111">Pour les considérations relatives à l’équilibrage de la charge réseau, consultez l’en-tête BITS-Host-ID dans le paquet [**Create-session**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b99-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="d8b99-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="d8b99-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="d8b99-113">Identifie ce paquet de demande en tant que Cancel-Session paquet.</span><span class="sxs-lookup"><span data-stu-id="d8b99-113">Identifies this request packet as a Cancel-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="d8b99-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS</span><span class="sxs-lookup"><span data-stu-id="d8b99-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="d8b99-115">GUID de chaîne qui identifie la session sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d8b99-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="d8b99-116">Remplacez {GUID} par l’identificateur de session que le serveur renvoie dans le paquet [**d’accusé de réception de la réponse de création de session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b99-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8b99-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d8b99-117">Remarks</span></span>

<span data-ttu-id="d8b99-118">Ce paquet annule un travail de chargement s’il est envoyé avant l’envoi du dernier fragment.</span><span class="sxs-lookup"><span data-stu-id="d8b99-118">This packet cancels an upload job if it is sent before the last fragment is sent.</span></span> <span data-ttu-id="d8b99-119">Cancel-Session n’a aucun effet sur un fichier dont le dernier fragment a déjà été envoyé.</span><span class="sxs-lookup"><span data-stu-id="d8b99-119">Cancel-Session has no effect on a file whose last fragment has already been sent.</span></span> <span data-ttu-id="d8b99-120">Quand le serveur BITS reçoit le dernier fragment, il écrit le fichier dans sa destination finale et, dans le cas d’une opération de chargement-réponse, publie le fichier dans l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="d8b99-120">When the BITS server receives the last fragment, it writes the file to its final destination and, in the case of an upload-reply, posts the file to the server application.</span></span> <span data-ttu-id="d8b99-121">Dans le cas de chargement-réponse, le paquet Cancel-Session annule la partie réponse d’une tâche de chargement-réponse.</span><span class="sxs-lookup"><span data-stu-id="d8b99-121">In the upload-reply case, the Cancel-Session packet cancels the reply portion of an upload-reply job.</span></span>

<span data-ttu-id="d8b99-122">Le serveur BITS libère toutes les ressources et supprime tous les fichiers temporaires lorsqu’il reçoit ce paquet.</span><span class="sxs-lookup"><span data-stu-id="d8b99-122">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="d8b99-123">Le client BITS envoie ce paquet lorsque l’utilisateur annule le travail.</span><span class="sxs-lookup"><span data-stu-id="d8b99-123">The BITS client sends this packet when the user cancels the job.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8b99-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b99-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b99-125">**ACK pour Create-session**</span><span class="sxs-lookup"><span data-stu-id="d8b99-125">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="d8b99-126">**Fermer-session**</span><span class="sxs-lookup"><span data-stu-id="d8b99-126">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




