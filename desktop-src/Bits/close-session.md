---
title: Close-Session
description: Utilisez le paquet Close-Session pour indiquer au serveur BITS que le téléchargement de fichiers est terminé et pour mettre fin à la session.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841013"
---
# <a name="close-session"></a><span data-ttu-id="d9648-104">Close-Session</span><span class="sxs-lookup"><span data-stu-id="d9648-104">Close-Session</span></span>

<span data-ttu-id="d9648-105">Utilisez le paquet **Close-session** pour indiquer au serveur bits que le téléchargement de fichiers est terminé et pour mettre fin à la session.</span><span class="sxs-lookup"><span data-stu-id="d9648-105">Use the **Close-Session** packet to tell the BITS server that file upload is complete and to end the session.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="d9648-106">headers</span><span class="sxs-lookup"><span data-stu-id="d9648-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="d9648-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits</span><span class="sxs-lookup"><span data-stu-id="d9648-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="d9648-108">Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="d9648-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="d9648-109">Remplacez l’URL distante par l’URI absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="d9648-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="d9648-110">Remplacez généralement l’URL distante par le nom de fichier distant du travail.</span><span class="sxs-lookup"><span data-stu-id="d9648-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="d9648-111">Pour les considérations relatives à l’équilibrage de la charge réseau, consultez l’en-tête BITS-Host-ID dans le paquet [**Create-session**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d9648-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="d9648-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="d9648-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="d9648-113">Identifie ce paquet de demande en tant que Close-Session paquet.</span><span class="sxs-lookup"><span data-stu-id="d9648-113">Identifies this request packet as a Close-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="d9648-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS</span><span class="sxs-lookup"><span data-stu-id="d9648-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="d9648-115">GUID de chaîne qui identifie la session sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d9648-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="d9648-116">Remplacez {GUID} par l’identificateur de session que le serveur renvoie dans le paquet [**d’accusé de réception de la réponse de création de session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d9648-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9648-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d9648-117">Remarks</span></span>

<span data-ttu-id="d9648-118">Le serveur BITS libère toutes les ressources et supprime tous les fichiers temporaires lorsqu’il reçoit ce paquet.</span><span class="sxs-lookup"><span data-stu-id="d9648-118">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="d9648-119">Pour les travaux de chargement-réponse, vous devez télécharger la réponse avant d’envoyer **Close-session**.</span><span class="sxs-lookup"><span data-stu-id="d9648-119">For upload-reply jobs, you must download the reply before sending **Close-Session**.</span></span> <span data-ttu-id="d9648-120">Dans le cas contraire, la réponse est perdue.</span><span class="sxs-lookup"><span data-stu-id="d9648-120">Otherwise, the reply is lost.</span></span>

<span data-ttu-id="d9648-121">Si vous envoyez ce paquet avant de télécharger tous les fragments, le fichier de téléchargement est supprimé. vous ne pouvez pas télécharger un fichier partiel.</span><span class="sxs-lookup"><span data-stu-id="d9648-121">If you send this packet before uploading all fragments, the upload file is deleted; you cannot upload a partial file.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9648-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9648-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9648-123">**ACK pour Close-session**</span><span class="sxs-lookup"><span data-stu-id="d9648-123">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="d9648-124">**Annuler-session**</span><span class="sxs-lookup"><span data-stu-id="d9648-124">**Cancel-Session**</span></span>](cancel-session.md)
</dt> <dt>

[<span data-ttu-id="d9648-125">**Créer une session**</span><span class="sxs-lookup"><span data-stu-id="d9648-125">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




