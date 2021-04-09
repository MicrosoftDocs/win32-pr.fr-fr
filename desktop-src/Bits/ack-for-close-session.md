---
title: ACK pour Close-Session
description: Utilisez le paquet ACK pour Close-Session pour accuser réception de la demande de Close-Session du client. Le serveur envoie l’accusé de réception après avoir libéré toutes les ressources associées à la session de téléchargement.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- ACK pour Close-Session BITS
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7142bfd8d1d5d65d1f669a328c75a2c8cdfb036
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104102533"
---
# <a name="ack-for-close-session"></a><span data-ttu-id="ec961-105">ACK pour Close-Session</span><span class="sxs-lookup"><span data-stu-id="ec961-105">Ack for Close-Session</span></span>

<span data-ttu-id="ec961-106">Utilisez le paquet **ACK pour le paquet Close-session** pour accuser réception de la demande de [**fermeture de session**](close-session.md) du client.</span><span class="sxs-lookup"><span data-stu-id="ec961-106">Use the **Ack for Close-Session** packet to acknowledge the client's [**Close-Session**](close-session.md) request.</span></span> <span data-ttu-id="ec961-107">Le serveur envoie l’accusé de réception après avoir libéré toutes les ressources associées à la session de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ec961-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="ec961-108">headers</span><span class="sxs-lookup"><span data-stu-id="ec961-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="ec961-109"><span id="reason-code"></span><span id="REASON-CODE"></span>Reason-Code</span><span class="sxs-lookup"><span data-stu-id="ec961-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="ec961-110">Remplacez Reason-Code par le code de raison HTTP.</span><span class="sxs-lookup"><span data-stu-id="ec961-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="ec961-111">Par exemple, affectez la valeur 200 à code de raison en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ec961-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="ec961-112">Pour obtenir la liste des codes de raison HTTP, consultez la [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="ec961-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="ec961-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>raison-Description</span><span class="sxs-lookup"><span data-stu-id="ec961-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="ec961-114">Remplacez Reason-Description par la description HTTP associée au code de raison.</span><span class="sxs-lookup"><span data-stu-id="ec961-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="ec961-115">Par exemple, affectez à Reason-Description la valeur OK si code de raison est 200.</span><span class="sxs-lookup"><span data-stu-id="ec961-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="ec961-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="ec961-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="ec961-117">Identifie ce paquet de réponse comme un paquet ACK.</span><span class="sxs-lookup"><span data-stu-id="ec961-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="ec961-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS</span><span class="sxs-lookup"><span data-stu-id="ec961-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="ec961-119">GUID de chaîne qui identifie la session sur le client.</span><span class="sxs-lookup"><span data-stu-id="ec961-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="ec961-120">Remplacez {GUID} par l’identificateur de session que le client a envoyé dans le paquet de demande de [**fermeture de session**](close-session.md) .</span><span class="sxs-lookup"><span data-stu-id="ec961-120">Replace {guid} with the session identifier that the client sent in the [**Close-Session**](close-session.md) request packet.</span></span> <span data-ttu-id="ec961-121">Si vous ne reconnaissez pas l’identificateur de session, définissez l’en-tête BITS-error-code sur BG \_ E \_ session \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="ec961-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="ec961-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span><span class="sxs-lookup"><span data-stu-id="ec961-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="ec961-123">Remplacez length par le nombre d’octets inclus dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="ec961-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="ec961-124">Content-Length est requis, même si le corps de la réponse n’inclut pas de contenu.</span><span class="sxs-lookup"><span data-stu-id="ec961-124">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="ec961-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erreur-code</span><span class="sxs-lookup"><span data-stu-id="ec961-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="ec961-126">Remplacez error-code par un nombre hexadécimal qui représente une valeur HRESULT associée à une erreur côté serveur.</span><span class="sxs-lookup"><span data-stu-id="ec961-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="ec961-127">N’incluez cet en-tête que si la raison-code n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="ec961-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="ec961-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erreur-contexte</span><span class="sxs-lookup"><span data-stu-id="ec961-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="ec961-129">Remplacez erreur-Context par un nombre hexadécimal qui représente le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ec961-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="ec961-130">Spécifiez le nombre hexadécimal [**du \_ \_ \_ \_ fichier distant de contexte d’erreur BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si le serveur a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ec961-130">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="ec961-131">Dans le cas contraire, spécifiez le nombre hexadécimal pour l' **\_ \_ \_ \_ application distante du contexte d’erreur BG** (0x7) si l’erreur a été générée par l’application dans laquelle le fichier de téléchargement est transmis.</span><span class="sxs-lookup"><span data-stu-id="ec961-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="ec961-132">Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="ec961-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec961-133">Notes</span><span class="sxs-lookup"><span data-stu-id="ec961-133">Remarks</span></span>

<span data-ttu-id="ec961-134">Le client BITS renvoie le paquet de [**session de fermeture**](close-session.md) si le code de raison est compris entre 500 et 599, sauf si l’en-tête de code d’erreur bits est présent avec la valeur BG \_ E \_ session \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="ec961-134">The BITS client resends the [**Close-Session**](close-session.md) packet if the reason-code is in the range 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="ec961-135">Le client n’effectue pas de nouvelle tentative pour les codes de raison 100 à 499.</span><span class="sxs-lookup"><span data-stu-id="ec961-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec961-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec961-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec961-137">**ACK pour Cancel-session**</span><span class="sxs-lookup"><span data-stu-id="ec961-137">**Ack for Cancel-Session**</span></span>](ack-for-cancel-session.md)
</dt> <dt>

[<span data-ttu-id="ec961-138">**Fermer-session**</span><span class="sxs-lookup"><span data-stu-id="ec961-138">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




