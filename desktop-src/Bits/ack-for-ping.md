---
title: ACK pour ping
description: Utilisez le paquet ACK pour ping pour accuser réception de la demande Ping du client.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- ACK pour BITS ping
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103941456"
---
# <a name="ack-for-ping"></a><span data-ttu-id="644a2-104">ACK pour ping</span><span class="sxs-lookup"><span data-stu-id="644a2-104">Ack for Ping</span></span>

<span data-ttu-id="644a2-105">Utilisez le paquet **ACK pour ping** pour accuser réception de la demande [**ping**](ping.md) du client.</span><span class="sxs-lookup"><span data-stu-id="644a2-105">Use the **Ack for Ping** packet to acknowledge the client's [**Ping**](ping.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="644a2-106">headers</span><span class="sxs-lookup"><span data-stu-id="644a2-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="644a2-107"><span id="reason-code"></span><span id="REASON-CODE"></span>Reason-Code</span><span class="sxs-lookup"><span data-stu-id="644a2-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="644a2-108">Remplacez Reason-Code par le code de raison HTTP.</span><span class="sxs-lookup"><span data-stu-id="644a2-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="644a2-109">Par exemple, affectez la valeur 200 à code de raison en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="644a2-109">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="644a2-110">Pour obtenir la liste des codes de raison HTTP, consultez la [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="644a2-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="644a2-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>raison-Description</span><span class="sxs-lookup"><span data-stu-id="644a2-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="644a2-112">Remplacez Reason-Description par la description HTTP associée au code de raison.</span><span class="sxs-lookup"><span data-stu-id="644a2-112">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="644a2-113">Par exemple, affectez à Reason-Description la valeur OK si code de raison est 200.</span><span class="sxs-lookup"><span data-stu-id="644a2-113">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="644a2-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="644a2-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="644a2-115">Identifie ce paquet de réponse comme un paquet ACK.</span><span class="sxs-lookup"><span data-stu-id="644a2-115">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="644a2-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span><span class="sxs-lookup"><span data-stu-id="644a2-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="644a2-117">Remplacez length par le nombre d’octets inclus dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="644a2-117">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="644a2-118">Obligatoire même si le corps de la réponse n’inclut pas de contenu.</span><span class="sxs-lookup"><span data-stu-id="644a2-118">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="644a2-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erreur-code</span><span class="sxs-lookup"><span data-stu-id="644a2-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="644a2-120">Remplacez error-code par un nombre hexadécimal qui représente une valeur HRESULT associée à une erreur côté serveur.</span><span class="sxs-lookup"><span data-stu-id="644a2-120">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="644a2-121">Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="644a2-121">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="644a2-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erreur-contexte</span><span class="sxs-lookup"><span data-stu-id="644a2-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="644a2-123">Remplacez erreur-Context par un nombre hexadécimal qui représente le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="644a2-123">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="644a2-124">Spécifiez le nombre hexadécimal [**du \_ \_ \_ \_ fichier distant de contexte d’erreur BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si le serveur a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="644a2-124">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="644a2-125">Dans le cas contraire, spécifiez le nombre hexadécimal pour l' **\_ \_ \_ \_ application distante du contexte d’erreur BG** (0x7) si l’erreur a été générée par l’application dans laquelle le fichier de téléchargement est transmis.</span><span class="sxs-lookup"><span data-stu-id="644a2-125">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="644a2-126">Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="644a2-126">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="644a2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="644a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644a2-128">**Ping**</span><span class="sxs-lookup"><span data-stu-id="644a2-128">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 




