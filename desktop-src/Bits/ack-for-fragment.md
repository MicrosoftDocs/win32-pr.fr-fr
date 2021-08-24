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
ms.openlocfilehash: ecd4b8bf5580a5724c689ced1886051006d34cd3c9ba0561d253f36428178c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702119"
---
# <a name="ack-for-fragment"></a>ACK pour fragment

Utilisez l’ACK du paquet de **fragments** pour accuser réception de la demande de [**fragment**](fragment.md) du client.

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

## <a name="headers"></a>headers

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>Reason-Code
</dt> <dd>

Remplacez Reason-Code par un code de raison HTTP. Le tableau suivant présente les codes de raison typiques d’une réponse à une demande de [**fragment**](fragment.md) . Pour obtenir la liste des codes de raison HTTP, consultez la [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Code de la raison    | Description                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | OK. La demande a abouti.<br/>                                                                             |
| 416<br/> | Plage-non-satisfaisante. Le client a envoyé un fragment dont la plage n’est pas contiguë au fragment précédent.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>raison-Description
</dt> <dd>

Remplacez Reason-Description par la description HTTP associée au code de raison. Par exemple, affectez à Reason-Description la valeur OK si code de raison est 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type
</dt> <dd>

Identifie ce paquet de réponse comme un paquet ACK.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-received-content-Range
</dt> <dd>

Décalage de base zéro à l’octet suivant que le serveur attend que le client envoie. Par exemple, si le fragment contenait la plage 128 212, vous affectez à Range la valeur 213.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS
</dt> <dd>

GUID de chaîne qui identifie la session sur le client. Remplacez {GUID} par l’identificateur de session que le client a envoyé dans le paquet de requête de [**fragment**](fragment.md) . Si vous ne reconnaissez pas l’identificateur de session, définissez l’en-tête BITS-error-code sur BG \_ E \_ session \_ \_ introuvable.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-reply-URL
</dt> <dd>

Contient l’URL des données de réponse d’une tâche de chargement-réponse. Ajoutez cet en-tête dans la réponse du fragment final une fois le téléchargement terminé et que vous recevez une réponse de l’application serveur, le cas échéant.

Utilisez l’en-tête Content-Range de la demande de fragment pour déterminer si le téléchargement est terminé. Le chargement est terminé si le décalage de fin de la valeur de la plage est égal à la valeur de longueur totale moins un.

Le serveur BITS publie le fichier de téléchargement dans l’application serveur après avoir déterminé que le téléchargement est terminé. L’application serveur traite le fichier et génère la réponse. Le serveur BITS définit la valeur de BITS-reply-URL sur l’URL du fichier de réponse de l’application serveur.

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

Si la session est destinée à une tâche de chargement-réponse, il peut y avoir un délai avant que le client n’envoie l' **accusé de** réception final pour la réponse du fragment. La durée du délai dépend de la durée nécessaire à l’application serveur (l’application sur laquelle le serveur publie le fichier de chargement) pour générer la réponse.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Créer une session**](create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> </dl>

 

 





