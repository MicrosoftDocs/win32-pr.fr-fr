---
title: ACK pour Cancel-Session
description: Utilisez le paquet ACK pour Cancel-Session pour accuser réception de la demande de Cancel-Session du client. Le serveur envoie l’accusé de réception après avoir libéré toutes les ressources associées à la session de téléchargement.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- ACK pour Cancel-Session BITS
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85ff937b720a69ee2722cef2f02b25273ea58d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032064"
---
# <a name="ack-for-cancel-session"></a>ACK pour Cancel-Session

Utilisez le paquet **ACK pour annuler la session** pour accuser réception de la demande d' [**annulation de session**](cancel-session.md) du client. Le serveur envoie l’accusé de réception après avoir libéré toutes les ressources associées à la session de téléchargement.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
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

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS
</dt> <dd>

GUID de chaîne qui identifie la session sur le client. Remplacez {GUID} par l’identificateur de session que le client a envoyé dans le paquet de demande d' [**annulation de session**](cancel-session.md) . Si vous ne reconnaissez pas l’identificateur de session, définissez l’en-tête BITS-error-code sur BG \_ E \_ session \_ \_ introuvable.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length
</dt> <dd>

Remplacez length par le nombre d’octets inclus dans le corps de la réponse. Obligatoire même si le corps de la réponse n’inclut pas de contenu.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erreur-code
</dt> <dd>

Remplacez error-code par un nombre hexadécimal qui représente une valeur HRESULT associée à une erreur côté serveur. N’incluez cet en-tête que si la raison-code n’est pas 200 ou 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erreur-contexte
</dt> <dd>

Remplacez erreur-Context par un nombre hexadécimal qui représente le contexte dans lequel l’erreur s’est produite. Spécifiez le nombre hexadécimal pour [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si le serveur a généré l’erreur. Dans le cas contraire, spécifiez le nombre hexadécimal pour l' **\_ \_ \_ \_ application distante du contexte d’erreur BG** (0x7) si l’erreur a été générée par l’application dans laquelle le fichier de téléchargement est transmis. Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.

</dd> </dl>

## <a name="remarks"></a>Notes

Le client BITS renvoie le paquet d' [**annulation de session**](cancel-session.md) si le code de raison est compris entre 500 et 599, sauf si l’en-tête de code d’erreur bits est présent avec la valeur BG \_ E \_ session \_ \_ introuvable. Le client n’effectue pas de nouvelle tentative pour les codes de raison 100 à 499.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACK pour Close-session**](ack-for-close-session.md)
</dt> <dt>

[**Annuler-session**](cancel-session.md)
</dt> </dl>

 

 




