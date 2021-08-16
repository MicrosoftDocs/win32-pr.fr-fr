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
ms.openlocfilehash: 09f31850599331027f3f8135a42dac8c8ea54519c04291d42fb06b5c7b8735fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835179"
---
# <a name="ack-for-ping"></a>ACK pour ping

Utilisez le paquet **ACK pour ping** pour accuser réception de la demande [**ping**](ping.md) du client.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>headers

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>Reason-Code
</dt> <dd>

Remplacez Reason-Code par le code de raison HTTP. Par exemple, affectez la valeur 200 à code de raison en cas de réussite. Pour obtenir la liste des codes de raison HTTP, consultez la [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>raison-Description
</dt> <dd>

Remplacez Reason-Description par la description HTTP associée au code de raison. Par exemple, affectez à Reason-Description la valeur OK si code de raison est 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type
</dt> <dd>

Identifie ce paquet de réponse comme un paquet ACK.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length
</dt> <dd>

Remplacez length par le nombre d’octets inclus dans le corps de la réponse. Obligatoire même si le corps de la réponse n’inclut pas de contenu.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erreur-code
</dt> <dd>

Remplacez error-code par un nombre hexadécimal qui représente une valeur HRESULT associée à une erreur côté serveur. Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erreur-contexte
</dt> <dd>

Remplacez erreur-Context par un nombre hexadécimal qui représente le contexte dans lequel l’erreur s’est produite. Spécifiez le nombre hexadécimal [**du \_ \_ \_ \_ fichier distant de contexte d’erreur BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si le serveur a généré l’erreur. Dans le cas contraire, spécifiez le nombre hexadécimal pour l' **\_ \_ \_ \_ application distante du contexte d’erreur BG** (0x7) si l’erreur a été générée par l’application dans laquelle le fichier de téléchargement est transmis. Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 




