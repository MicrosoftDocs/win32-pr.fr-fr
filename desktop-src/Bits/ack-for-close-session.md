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
ms.openlocfilehash: 289f2cfc2ca9f1e879e0aa592af28d86ae433f6e06d007aa71e00581baba2af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835412"
---
# <a name="ack-for-close-session"></a>ACK pour Close-Session

Utilisez le paquet **ACK pour le paquet Close-session** pour accuser réception de la demande de [**fermeture de session**](close-session.md) du client. Le serveur envoie l’accusé de réception après avoir libéré toutes les ressources associées à la session de téléchargement.

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

GUID de chaîne qui identifie la session sur le client. Remplacez {GUID} par l’identificateur de session que le client a envoyé dans le paquet de demande de [**fermeture de session**](close-session.md) . Si vous ne reconnaissez pas l’identificateur de session, définissez l’en-tête BITS-error-code sur BG \_ E \_ session \_ \_ introuvable.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length
</dt> <dd>

Remplacez length par le nombre d’octets inclus dans le corps de la réponse. Content-Length est requis, même si le corps de la réponse n’inclut pas de contenu.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erreur-code
</dt> <dd>

Remplacez error-code par un nombre hexadécimal qui représente une valeur HRESULT associée à une erreur côté serveur. N’incluez cet en-tête que si la raison-code n’est pas 200 ou 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erreur-contexte
</dt> <dd>

Remplacez erreur-Context par un nombre hexadécimal qui représente le contexte dans lequel l’erreur s’est produite. Spécifiez le nombre hexadécimal [**du \_ \_ \_ \_ fichier distant de contexte d’erreur BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) si le serveur a généré l’erreur. Dans le cas contraire, spécifiez le nombre hexadécimal pour l' **\_ \_ \_ \_ application distante du contexte d’erreur BG** (0x7) si l’erreur a été générée par l’application dans laquelle le fichier de téléchargement est transmis. Incluez cet en-tête uniquement si le code de raison n’est pas 200 ou 201.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le client BITS renvoie le paquet de [**session de fermeture**](close-session.md) si le code de raison est compris entre 500 et 599, sauf si l’en-tête de code d’erreur bits est présent avec la valeur BG \_ E \_ session \_ \_ introuvable. Le client n’effectue pas de nouvelle tentative pour les codes de raison 100 à 499.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACK pour Cancel-session**](ack-for-cancel-session.md)
</dt> <dt>

[**Fermer-session**](close-session.md)
</dt> </dl>

 

 




