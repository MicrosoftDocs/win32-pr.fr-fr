---
title: ACK pour Create-Session
description: Utilisez le paquet ACK pour Create-Session pour accuser réception de la demande de Create-Session du client.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- ACK pour Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "106536283"
---
# <a name="ack-for-create-session"></a><span data-ttu-id="37013-104">ACK pour Create-Session</span><span class="sxs-lookup"><span data-stu-id="37013-104">Ack for Create-Session</span></span>

<span data-ttu-id="37013-105">Utilisez le paquet **ACK pour Create-session** pour accuser réception de la demande de [**création de session**](create-session.md) du client.</span><span class="sxs-lookup"><span data-stu-id="37013-105">Use the **Ack for Create-Session** packet to acknowledge the client's [**Create-Session**](create-session.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="37013-106">headers</span><span class="sxs-lookup"><span data-stu-id="37013-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="37013-107"><span id="reason-code"></span><span id="REASON-CODE"></span>Reason-Code</span><span class="sxs-lookup"><span data-stu-id="37013-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="37013-108">Remplacez Reason-Code par le code de raison HTTP.</span><span class="sxs-lookup"><span data-stu-id="37013-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="37013-109">Le tableau suivant présente les codes de raison typiques d’une réponse à une demande de [**création de session**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="37013-109">The following table shows the typical reason codes for a response to a [**Create-Session**](create-session.md) request.</span></span> <span data-ttu-id="37013-110">Pour obtenir la liste des codes de raison HTTP, consultez la [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="37013-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="37013-111">Code de la raison</span><span class="sxs-lookup"><span data-stu-id="37013-111">Reason code</span></span>    | <span data-ttu-id="37013-112">Description</span><span class="sxs-lookup"><span data-stu-id="37013-112">Description</span></span>                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37013-113">200</span><span class="sxs-lookup"><span data-stu-id="37013-113">200</span></span><br/> | <span data-ttu-id="37013-114">OK.</span><span class="sxs-lookup"><span data-stu-id="37013-114">OK.</span></span> <span data-ttu-id="37013-115">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="37013-115">The request was successful.</span></span><br/>                                          |
| <span data-ttu-id="37013-116">201</span><span class="sxs-lookup"><span data-stu-id="37013-116">201</span></span><br/> | <span data-ttu-id="37013-117">Créé.</span><span class="sxs-lookup"><span data-stu-id="37013-117">Created.</span></span> <span data-ttu-id="37013-118">La session a été créée.</span><span class="sxs-lookup"><span data-stu-id="37013-118">The session was created.</span></span><br/>                                        |
| <span data-ttu-id="37013-119">403</span><span class="sxs-lookup"><span data-stu-id="37013-119">403</span></span><br/> | <span data-ttu-id="37013-120">Interdit.</span><span class="sxs-lookup"><span data-stu-id="37013-120">Forbidden.</span></span> <span data-ttu-id="37013-121">L’utilisateur n’est pas autorisé à charger des fichiers sur l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="37013-121">The user is not allowed to upload files to the specified URL.</span></span><br/> |
| <span data-ttu-id="37013-122">404</span><span class="sxs-lookup"><span data-stu-id="37013-122">404</span></span><br/> | <span data-ttu-id="37013-123">Introuvable.</span><span class="sxs-lookup"><span data-stu-id="37013-123">Not Found.</span></span> <span data-ttu-id="37013-124">L’URL spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="37013-124">The specified URL does not exist.</span></span><br/>                             |
| <span data-ttu-id="37013-125">409</span><span class="sxs-lookup"><span data-stu-id="37013-125">409</span></span><br/> | <span data-ttu-id="37013-126">Conflit.</span><span class="sxs-lookup"><span data-stu-id="37013-126">Conflict.</span></span> <span data-ttu-id="37013-127">Le fichier existe sur le serveur et ne peut pas être remplacé.</span><span class="sxs-lookup"><span data-stu-id="37013-127">The file exists on the server and cannot be overwritten.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="37013-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>raison-Description</span><span class="sxs-lookup"><span data-stu-id="37013-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="37013-129">Remplacez Reason-Description par la description HTTP associée au code de raison.</span><span class="sxs-lookup"><span data-stu-id="37013-129">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="37013-130">Par exemple, affectez à Reason-Description la valeur OK si code de raison est 200.</span><span class="sxs-lookup"><span data-stu-id="37013-130">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="37013-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="37013-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="37013-132">Identifie ce paquet de réponse comme un paquet ACK.</span><span class="sxs-lookup"><span data-stu-id="37013-132">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="37013-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-protocole</span><span class="sxs-lookup"><span data-stu-id="37013-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protocol</span></span>
</dt> <dd>

<span data-ttu-id="37013-134">GUID de chaîne qui identifie le protocole que le serveur souhaite utiliser pour cette session.</span><span class="sxs-lookup"><span data-stu-id="37013-134">String GUID that identifies the protocol that the server wants to use for this session.</span></span> <span data-ttu-id="37013-135">Remplacez {GUID} par l’identificateur de protocole dans la liste des protocoles que le client contient dans la demande de [**création de session**](create-session.md) ; l’en-tête BITS-Supported-Protocol contient la liste.</span><span class="sxs-lookup"><span data-stu-id="37013-135">Replace {guid} with the protocol identifier from the list of protocols the client includes in the [**Create-Session**](create-session.md) request; the BITS-Supported-Protocol header contains the list.</span></span> <span data-ttu-id="37013-136">Incluez cet en-tête uniquement si le code de raison est 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="37013-136">Include this header only if the reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="37013-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS</span><span class="sxs-lookup"><span data-stu-id="37013-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="37013-138">GUID de chaîne qui identifie cette session sur le client.</span><span class="sxs-lookup"><span data-stu-id="37013-138">String GUID that identifies this session to the client.</span></span> <span data-ttu-id="37013-139">Remplacez {GUID} par l’identificateur de session que le client envoie dans tous les paquets de demande suivants.</span><span class="sxs-lookup"><span data-stu-id="37013-139">Replace {guid} with the session identifier that the client sends in all subsequent request packets.</span></span>

<span data-ttu-id="37013-140">BITS utilise un GUID pour identifier la session, mais vous pouvez utiliser n’importe quelle chaîne HTTP-Legal jusqu’à 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="37013-140">BITS uses a GUID to identify the session, but you can use any HTTP-legal string up to 100 characters.</span></span>

</dd> <dt>

<span data-ttu-id="37013-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-ID</span><span class="sxs-lookup"><span data-stu-id="37013-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id</span></span>
</dt> <dd>

<span data-ttu-id="37013-142">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="37013-142">Optional.</span></span> <span data-ttu-id="37013-143">Incluez cet en-tête uniquement si la [propriété d’extension IIS bits](bits-iis-extension-properties.md), BITSHostId, est définie.</span><span class="sxs-lookup"><span data-stu-id="37013-143">Include this header only if the [BITS IIS extension property](bits-iis-extension-properties.md), BITSHostId, is set.</span></span> <span data-ttu-id="37013-144">Remplacez PublicHostName par le nom du serveur ou l’adresse IP de la propriété BITSHostId.</span><span class="sxs-lookup"><span data-stu-id="37013-144">Replace PublicHostName with the server name or IP address from the BITSHostId property.</span></span>

<span data-ttu-id="37013-145">Le client doit remplacer la partie serveur de l’URL distante sur tous les paquets suivants.</span><span class="sxs-lookup"><span data-stu-id="37013-145">The client must replace the server portion of the remote-URL on all subsequent packets.</span></span> <span data-ttu-id="37013-146">Si le client ne spécifie pas ce nom d’hôte sur les paquets suivants, il est possible que le travail redémarre sur un autre serveur de la batterie, laissant ainsi un fichier de téléchargement partiel sur le serveur précédent.</span><span class="sxs-lookup"><span data-stu-id="37013-146">If the client does not specify this host name on subsequent packets, it is possible that the job will begin again on another server in the farm, leaving a partial upload file on the previous server.</span></span>

</dd> <dt>

<span data-ttu-id="37013-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-ID-repli-Timeout</span><span class="sxs-lookup"><span data-stu-id="37013-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout</span></span>
</dt> <dd>

<span data-ttu-id="37013-148">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="37013-148">Optional.</span></span> <span data-ttu-id="37013-149">Incluez cet en-tête uniquement si l’en-tête BITS-Host-ID est spécifié.</span><span class="sxs-lookup"><span data-stu-id="37013-149">Include this header only if the BITS-Host-Id header is specified.</span></span> <span data-ttu-id="37013-150">Remplacez Timeout par la valeur du délai d’attente de la propriété BITSHostIdFallbackTimeout.</span><span class="sxs-lookup"><span data-stu-id="37013-150">Replace Timeout with the time-out value from the BITSHostIdFallbackTimeout property.</span></span> <span data-ttu-id="37013-151">La propriété BITSHostIdFallbackTimeout est l’une des [propriétés d’extension IIS bits](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="37013-151">The BITSHostIdFallbackTimeout property is one of the [BITS IIS extension properties](bits-iis-extension-properties.md).</span></span>

<span data-ttu-id="37013-152">Le client utilise le délai d’expiration pour déterminer la durée pendant laquelle il tente de se reconnecter au nom du serveur spécifié dans l’en-tête BITS-Host-ID avant de revenir au nom d’hôte spécifié dans le nom de fichier distant du travail.</span><span class="sxs-lookup"><span data-stu-id="37013-152">The client uses the time-out period to determine how long it tries to reconnect to the server name specified in the BITS-Host-Id header before reverting to the host name specified in the remote file name of the job.</span></span> <span data-ttu-id="37013-153">La minuterie commence lorsque BITS ne parvient pas à se connecter au serveur BITS-Host-ID.</span><span class="sxs-lookup"><span data-stu-id="37013-153">The timer begins when BITS is unable to connect to the BITS-Host-Id server.</span></span> <span data-ttu-id="37013-154">La minuterie est réinitialisée lors de la restauration d’une connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="37013-154">The timer is reset when a connection to the server is restored.</span></span> <span data-ttu-id="37013-155">Si aucun délai d’attente n’est spécifié, le client ne retourne jamais au nom d’hôte spécifié dans le nom de fichier distant.</span><span class="sxs-lookup"><span data-stu-id="37013-155">If a time-out period is not specified, the client never reverts to the host name specified in the remote file name.</span></span>

</dd> <dt>

<span data-ttu-id="37013-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accepter-encodage</span><span class="sxs-lookup"><span data-stu-id="37013-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="37013-157">Identifie le schéma d’encodage à utiliser sur les fragments envoyés au serveur.</span><span class="sxs-lookup"><span data-stu-id="37013-157">Identifies the encoding scheme to use on the fragments sent to the server.</span></span> <span data-ttu-id="37013-158">Le paquet fragment contient le fragment encodé dans le corps du paquet.</span><span class="sxs-lookup"><span data-stu-id="37013-158">The Fragment packet contains the encoded fragment in the body of the packet.</span></span> <span data-ttu-id="37013-159">Le serveur BITS requiert l’encodage d’identité (texte en clair).</span><span class="sxs-lookup"><span data-stu-id="37013-159">The BITS server requires Identity encoding (plaintext).</span></span> <span data-ttu-id="37013-160">Incluez cet en-tête uniquement si le code de raison est 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="37013-160">Include this header only if the Reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="37013-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span><span class="sxs-lookup"><span data-stu-id="37013-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="37013-162">Remplacez length par le nombre d’octets inclus dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="37013-162">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="37013-163">Obligatoire même si le corps de la réponse n’inclut pas de contenu.</span><span class="sxs-lookup"><span data-stu-id="37013-163">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="37013-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erreur-code</span><span class="sxs-lookup"><span data-stu-id="37013-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="37013-165">Remplacez error-code par un nombre hexadécimal qui représente une valeur HRESULT associée à une erreur côté serveur.</span><span class="sxs-lookup"><span data-stu-id="37013-165">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="37013-166">Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="37013-166">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="37013-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erreur-contexte</span><span class="sxs-lookup"><span data-stu-id="37013-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="37013-168">Remplacez erreur-Context par un nombre hexadécimal qui représente le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="37013-168">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="37013-169">Spécifiez le nombre hexadécimal [**du \_ \_ \_ \_ fichier distant de contexte d’erreur BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si le serveur a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="37013-169">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="37013-170">Dans le cas contraire, spécifiez le nombre hexadécimal pour l' **\_ \_ \_ \_ application distante du contexte d’erreur BG** (0x7) si l’erreur a été générée par l’application dans laquelle le fichier de téléchargement est transmis.</span><span class="sxs-lookup"><span data-stu-id="37013-170">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="37013-171">Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="37013-171">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="37013-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37013-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37013-173">**Créer une session**</span><span class="sxs-lookup"><span data-stu-id="37013-173">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 





