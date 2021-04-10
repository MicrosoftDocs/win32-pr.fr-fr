---
title: Fragment
description: Utilisez le paquet fragment pour envoyer un fragment du fichier de téléchargement au serveur.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- BITS de fragment
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101281"
---
# <a name="fragment"></a><span data-ttu-id="8d42f-104">Fragment</span><span class="sxs-lookup"><span data-stu-id="8d42f-104">Fragment</span></span>

<span data-ttu-id="8d42f-105">Utilisez le paquet **fragment** pour envoyer un fragment du fichier de téléchargement au serveur.</span><span class="sxs-lookup"><span data-stu-id="8d42f-105">Use the **Fragment** packet to send a fragment of the upload file to the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a><span data-ttu-id="8d42f-106">headers</span><span class="sxs-lookup"><span data-stu-id="8d42f-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="8d42f-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits</span><span class="sxs-lookup"><span data-stu-id="8d42f-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="8d42f-108">Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="8d42f-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="8d42f-109">Remplacez l’URL distante par l’URI absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="8d42f-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="8d42f-110">Remplacez généralement l’URL distante par le nom de fichier distant du travail.</span><span class="sxs-lookup"><span data-stu-id="8d42f-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="8d42f-111">Pour les considérations relatives à l’équilibrage de la charge réseau, consultez l’en-tête BITS-Host-ID dans le paquet [**Create-session**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="8d42f-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="8d42f-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="8d42f-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="8d42f-113">Identifie ce paquet de requête en tant que paquet de fragments.</span><span class="sxs-lookup"><span data-stu-id="8d42f-113">Identifies this request packet as a Fragment packet.</span></span>

</dd> <dt>

<span data-ttu-id="8d42f-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS</span><span class="sxs-lookup"><span data-stu-id="8d42f-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="8d42f-115">GUID de chaîne qui identifie la session sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="8d42f-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="8d42f-116">Remplacez {GUID} par l’identificateur de session que le serveur renvoie dans le paquet [**d’accusé de réception de la réponse de création de session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="8d42f-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> <dt>

<span data-ttu-id="8d42f-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span><span class="sxs-lookup"><span data-stu-id="8d42f-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span></span>
</dt> <dd>

<span data-ttu-id="8d42f-118">Spécifiez cet en-tête uniquement avec le fragment initial.</span><span class="sxs-lookup"><span data-stu-id="8d42f-118">Specify this header only with the initial fragment.</span></span> <span data-ttu-id="8d42f-119">Remplacez filename par le nom du fichier local du travail.</span><span class="sxs-lookup"><span data-stu-id="8d42f-119">Replace filename with the name of the local file name from the job.</span></span> <span data-ttu-id="8d42f-120">Le nom n’inclut pas le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="8d42f-120">The name does not include the path.</span></span>

</dd> <dt>

<span data-ttu-id="8d42f-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span><span class="sxs-lookup"><span data-stu-id="8d42f-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="8d42f-122">Remplacez length par le nombre d’octets envoyés dans le corps du fragment.</span><span class="sxs-lookup"><span data-stu-id="8d42f-122">Replace length with the number of bytes sent in the fragment body.</span></span>

</dd> <dt>

<span data-ttu-id="8d42f-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Plage de contenu</span><span class="sxs-lookup"><span data-stu-id="8d42f-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="8d42f-124">Indique au serveur où appliquer la plage dans le fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="8d42f-124">Tells the server where to apply the range in the destination file.</span></span> <span data-ttu-id="8d42f-125">Remplacez la plage par les décalages de début et de fin de la plage dans le fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="8d42f-125">Replace range with the start and end offsets of the range in the destination file.</span></span> <span data-ttu-id="8d42f-126">Les décalages sont de base zéro.</span><span class="sxs-lookup"><span data-stu-id="8d42f-126">The offsets are zero-based.</span></span> <span data-ttu-id="8d42f-127">Si la plage donnée chevauche une plage existante, BITS écrit uniquement la partie sans chevauchement de la plage ; Le service BITS ne remplace pas le contenu existant.</span><span class="sxs-lookup"><span data-stu-id="8d42f-127">If the given range overlaps an existing range, BITS writes only the non-overlapping portion of the range; BITS does not overwrite existing content.</span></span> <span data-ttu-id="8d42f-128">Par exemple, si le premier paquet contient la plage comprise entre 0 et 100 et que le deuxième paquet contenait la plage 50 à 150, BITS écrit uniquement les octets 101 à 150 du deuxième paquet.</span><span class="sxs-lookup"><span data-stu-id="8d42f-128">For example, if the first packet contained the range 0 through 100 and the second packet contained the range 50 through 150, BITS writes only bytes 101 through 150 from the second packet.</span></span> <span data-ttu-id="8d42f-129">Remplacez total-length par le nombre total d’octets dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="8d42f-129">Replace total-length with the total number of bytes in the file.</span></span>

</dd> <dt>

<span data-ttu-id="8d42f-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span><span class="sxs-lookup"><span data-stu-id="8d42f-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="8d42f-131">Remplacez encodage par le type d’encodage utilisé par le client sur le fragment.</span><span class="sxs-lookup"><span data-stu-id="8d42f-131">Replace encoding with the type of encoding the client uses on the fragment.</span></span> <span data-ttu-id="8d42f-132">Le client doit utiliser l’encodage identifié par le serveur dans l’en-tête Accept-Encoding de l’accusé de réception pour le paquet de réponse [**de création de session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="8d42f-132">The client must use the encoding that the server identifies in the Accept-Encoding header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="8d42f-133">Le serveur utilise le type d’encodage pour décoder le fragment.</span><span class="sxs-lookup"><span data-stu-id="8d42f-133">The server uses the encoding type to decode the fragment.</span></span> <span data-ttu-id="8d42f-134">Tous les fragments doivent spécifier le même encodage.</span><span class="sxs-lookup"><span data-stu-id="8d42f-134">All fragments must specify the same encoding.</span></span>

<span data-ttu-id="8d42f-135">N’envoyez pas cet en-tête si le type d’encodage est Identity.</span><span class="sxs-lookup"><span data-stu-id="8d42f-135">Do not send this header if the encoding type is Identity.</span></span> <span data-ttu-id="8d42f-136">Le serveur BITS prend en charge uniquement l’encodage d’identité.</span><span class="sxs-lookup"><span data-stu-id="8d42f-136">The BITS server supports only Identity encoding.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d42f-137">Notes</span><span class="sxs-lookup"><span data-stu-id="8d42f-137">Remarks</span></span>

<span data-ttu-id="8d42f-138">Le fragment est une plage d’octets envoyés dans le corps du paquet.</span><span class="sxs-lookup"><span data-stu-id="8d42f-138">The fragment is a range of bytes sent in the body of the packet.</span></span> <span data-ttu-id="8d42f-139">Le client envoie les fragments dans l’ordre séquentiel, en commençant par le décalage zéro ; le serveur n’effectue pas le suivi des plages non contiguës.</span><span class="sxs-lookup"><span data-stu-id="8d42f-139">The client sends the fragments in sequential order starting with offset zero; the server does not keep track of non-contiguous ranges.</span></span> <span data-ttu-id="8d42f-140">Si le client envoie des plages non contiguës, le serveur renvoie un code de retour HTTP 416 (satisfaisante) dans l' [**accusé de réception de**](ack-for-fragment.md) la réponse du fragment.</span><span class="sxs-lookup"><span data-stu-id="8d42f-140">If the client sends non-contiguous ranges, the server returns an HTTP 416 (range-not-satisfiable) return code in the [**Ack for Fragment**](ack-for-fragment.md) response.</span></span>

<span data-ttu-id="8d42f-141">Les en-têtes Content-*xxxx* sont des en-têtes HTTP 1,1 standard.</span><span class="sxs-lookup"><span data-stu-id="8d42f-141">The Content-*xxxx* headers are standard HTTP 1.1 headers.</span></span> <span data-ttu-id="8d42f-142">Pour plus d’informations sur les en-têtes Content-*xxxx* , consultez la spécification [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .</span><span class="sxs-lookup"><span data-stu-id="8d42f-142">For more details on the Content-*xxxx* headers, see the [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d42f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d42f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d42f-144">**ACK pour fragment**</span><span class="sxs-lookup"><span data-stu-id="8d42f-144">**Ack for Fragment**</span></span>](ack-for-fragment.md)
</dt> <dt>

[<span data-ttu-id="8d42f-145">**Fermer-session**</span><span class="sxs-lookup"><span data-stu-id="8d42f-145">**Close-Session**</span></span>](close-session.md)
</dt> <dt>

[<span data-ttu-id="8d42f-146">**Créer une session**</span><span class="sxs-lookup"><span data-stu-id="8d42f-146">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




