---
title: ACK pour fragment
description: Utilisez l’ACK du paquet de fragments pour accuser réception de la demande de fragment du client.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- ACK pour les BITS de fragment
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103941457"
---
# <a name="ack-for-fragment"></a><span data-ttu-id="78937-104">ACK pour fragment</span><span class="sxs-lookup"><span data-stu-id="78937-104">Ack for Fragment</span></span>

<span data-ttu-id="78937-105">Utilisez l’ACK du paquet de **fragments** pour accuser réception de la demande de [**fragment**](fragment.md) du client.</span><span class="sxs-lookup"><span data-stu-id="78937-105">Use the **Ack for Fragment** packet to acknowledge the client's [**Fragment**](fragment.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="78937-106">headers</span><span class="sxs-lookup"><span data-stu-id="78937-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="78937-107"><span id="reason-code"></span><span id="REASON-CODE"></span>Reason-Code</span><span class="sxs-lookup"><span data-stu-id="78937-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="78937-108">Remplacez Reason-Code par un code de raison HTTP.</span><span class="sxs-lookup"><span data-stu-id="78937-108">Replace reason-code with an HTTP reason code.</span></span> <span data-ttu-id="78937-109">Le tableau suivant présente les codes de raison typiques d’une réponse à une demande de [**fragment**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="78937-109">The following table shows the typical reason codes for a response to a [**Fragment**](fragment.md) request.</span></span> <span data-ttu-id="78937-110">Pour obtenir la liste des codes de raison HTTP, consultez la [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="78937-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="78937-111">Code de la raison</span><span class="sxs-lookup"><span data-stu-id="78937-111">Reason code</span></span>    | <span data-ttu-id="78937-112">Description</span><span class="sxs-lookup"><span data-stu-id="78937-112">Description</span></span>                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78937-113">200</span><span class="sxs-lookup"><span data-stu-id="78937-113">200</span></span><br/> | <span data-ttu-id="78937-114">OK.</span><span class="sxs-lookup"><span data-stu-id="78937-114">OK.</span></span> <span data-ttu-id="78937-115">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="78937-115">The request was successful.</span></span><br/>                                                                             |
| <span data-ttu-id="78937-116">416</span><span class="sxs-lookup"><span data-stu-id="78937-116">416</span></span><br/> | <span data-ttu-id="78937-117">Plage-non-satisfaisante.</span><span class="sxs-lookup"><span data-stu-id="78937-117">Range-Not-Satisfiable.</span></span> <span data-ttu-id="78937-118">Le client a envoyé un fragment dont la plage n’est pas contiguë au fragment précédent.</span><span class="sxs-lookup"><span data-stu-id="78937-118">The client sent a fragment whose range is not contiguous with the previous fragment.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="78937-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>raison-Description</span><span class="sxs-lookup"><span data-stu-id="78937-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="78937-120">Remplacez Reason-Description par la description HTTP associée au code de raison.</span><span class="sxs-lookup"><span data-stu-id="78937-120">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="78937-121">Par exemple, affectez à Reason-Description la valeur OK si code de raison est 200.</span><span class="sxs-lookup"><span data-stu-id="78937-121">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="78937-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="78937-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="78937-123">Identifie ce paquet de réponse comme un paquet ACK.</span><span class="sxs-lookup"><span data-stu-id="78937-123">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="78937-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-received-content-Range</span><span class="sxs-lookup"><span data-stu-id="78937-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="78937-125">Décalage de base zéro à l’octet suivant que le serveur attend que le client envoie.</span><span class="sxs-lookup"><span data-stu-id="78937-125">Zero-based offset to the next byte the server expects the client to send.</span></span> <span data-ttu-id="78937-126">Par exemple, si le fragment contenait la plage 128 212, vous affectez à Range la valeur 213.</span><span class="sxs-lookup"><span data-stu-id="78937-126">For example, if the fragment contained the range 128 212, you would set range to 213.</span></span>

</dd> <dt>

<span data-ttu-id="78937-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS</span><span class="sxs-lookup"><span data-stu-id="78937-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="78937-128">GUID de chaîne qui identifie la session sur le client.</span><span class="sxs-lookup"><span data-stu-id="78937-128">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="78937-129">Remplacez {GUID} par l’identificateur de session que le client a envoyé dans le paquet de requête de [**fragment**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="78937-129">Replace {guid} with the session identifier that the client sent in the [**Fragment**](fragment.md) request packet.</span></span> <span data-ttu-id="78937-130">Si vous ne reconnaissez pas l’identificateur de session, définissez l’en-tête BITS-error-code sur BG \_ E \_ session \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="78937-130">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="78937-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-reply-URL</span><span class="sxs-lookup"><span data-stu-id="78937-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span></span>
</dt> <dd>

<span data-ttu-id="78937-132">Contient l’URL des données de réponse d’une tâche de chargement-réponse.</span><span class="sxs-lookup"><span data-stu-id="78937-132">Contains the URL to the reply data of an upload-reply job.</span></span> <span data-ttu-id="78937-133">Ajoutez cet en-tête dans la réponse du fragment final une fois le téléchargement terminé et que vous recevez une réponse de l’application serveur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="78937-133">Include this header in the final fragment response after the upload is complete and you receive a response from the server application, if applicable.</span></span>

<span data-ttu-id="78937-134">Utilisez l’en-tête Content-Range de la demande de fragment pour déterminer si le téléchargement est terminé.</span><span class="sxs-lookup"><span data-stu-id="78937-134">Use the Content-Range header from the Fragment request to determine whether the upload is complete.</span></span> <span data-ttu-id="78937-135">Le chargement est terminé si le décalage de fin de la valeur de la plage est égal à la valeur de longueur totale moins un.</span><span class="sxs-lookup"><span data-stu-id="78937-135">The upload is complete if the end offset of the range value equals the total-length value minus one.</span></span>

<span data-ttu-id="78937-136">Le serveur BITS publie le fichier de téléchargement dans l’application serveur après avoir déterminé que le téléchargement est terminé.</span><span class="sxs-lookup"><span data-stu-id="78937-136">The BITS server posts the upload file to the server application after it determines the upload is complete.</span></span> <span data-ttu-id="78937-137">L’application serveur traite le fichier et génère la réponse.</span><span class="sxs-lookup"><span data-stu-id="78937-137">The server application processes the file and generates the reply.</span></span> <span data-ttu-id="78937-138">Le serveur BITS définit la valeur de BITS-reply-URL sur l’URL du fichier de réponse de l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="78937-138">The BITS server sets the value of BITS-Reply-URL to the URL of the reply file from the server application.</span></span>

</dd> <dt>

<span data-ttu-id="78937-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span><span class="sxs-lookup"><span data-stu-id="78937-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="78937-140">Remplacez length par le nombre d’octets inclus dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="78937-140">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="78937-141">Content-Length est requis, même si le corps de la réponse n’inclut pas de contenu.</span><span class="sxs-lookup"><span data-stu-id="78937-141">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="78937-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erreur-code</span><span class="sxs-lookup"><span data-stu-id="78937-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="78937-143">Remplacez error-code par un nombre hexadécimal qui représente une valeur HRESULT associée à une erreur côté serveur.</span><span class="sxs-lookup"><span data-stu-id="78937-143">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="78937-144">N’incluez cet en-tête que si la raison-code n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="78937-144">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="78937-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erreur-contexte</span><span class="sxs-lookup"><span data-stu-id="78937-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="78937-146">Remplacez erreur-Context par un nombre hexadécimal qui représente le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="78937-146">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="78937-147">Spécifiez le nombre hexadécimal [**du \_ \_ \_ \_ fichier distant de contexte d’erreur BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si le serveur a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="78937-147">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="78937-148">Dans le cas contraire, spécifiez le nombre hexadécimal pour l' **\_ \_ \_ \_ application distante du contexte d’erreur BG** (0x7) si l’erreur a été générée par l’application dans laquelle le fichier de téléchargement est transmis.</span><span class="sxs-lookup"><span data-stu-id="78937-148">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="78937-149">Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="78937-149">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78937-150">Notes</span><span class="sxs-lookup"><span data-stu-id="78937-150">Remarks</span></span>

<span data-ttu-id="78937-151">Si la session est destinée à une tâche de chargement-réponse, il peut y avoir un délai avant que le client n’envoie l' **accusé de** réception final pour la réponse du fragment.</span><span class="sxs-lookup"><span data-stu-id="78937-151">If the session is for an upload-reply job, there may be a delay before the client receives the final **Ack for Fragment** response.</span></span> <span data-ttu-id="78937-152">La durée du délai dépend de la durée nécessaire à l’application serveur (l’application sur laquelle le serveur publie le fichier de chargement) pour générer la réponse.</span><span class="sxs-lookup"><span data-stu-id="78937-152">The length of the delay depends on the amount of time the server application (application to which the server posts the upload file) takes to generate the reply.</span></span>

## <a name="see-also"></a><span data-ttu-id="78937-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78937-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78937-154">**Créer une session**</span><span class="sxs-lookup"><span data-stu-id="78937-154">**Create-Session**</span></span>](create-session.md)
</dt> <dt>

[<span data-ttu-id="78937-155">**Fragment**</span><span class="sxs-lookup"><span data-stu-id="78937-155">**Fragment**</span></span>](fragment.md)
</dt> </dl>

 

 





