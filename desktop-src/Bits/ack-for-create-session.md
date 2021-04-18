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
# <a name="ack-for-create-session"></a>ACK pour Create-Session

Utilisez le paquet **ACK pour Create-session** pour accuser réception de la demande de [**création de session**](create-session.md) du client.

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

## <a name="headers"></a>headers

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>Reason-Code
</dt> <dd>

Remplacez Reason-Code par le code de raison HTTP. Le tableau suivant présente les codes de raison typiques d’une réponse à une demande de [**création de session**](create-session.md) . Pour obtenir la liste des codes de raison HTTP, consultez la [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Code de la raison    | Description                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | OK. La demande a abouti.<br/>                                          |
| 201<br/> | Créé. La session a été créée.<br/>                                        |
| 403<br/> | Interdit. L’utilisateur n’est pas autorisé à charger des fichiers sur l’URL spécifiée.<br/> |
| 404<br/> | Introuvable. L’URL spécifiée n’existe pas.<br/>                             |
| 409<br/> | Conflit. Le fichier existe sur le serveur et ne peut pas être remplacé.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>raison-Description
</dt> <dd>

Remplacez Reason-Description par la description HTTP associée au code de raison. Par exemple, affectez à Reason-Description la valeur OK si code de raison est 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type
</dt> <dd>

Identifie ce paquet de réponse comme un paquet ACK.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-protocole
</dt> <dd>

GUID de chaîne qui identifie le protocole que le serveur souhaite utiliser pour cette session. Remplacez {GUID} par l’identificateur de protocole dans la liste des protocoles que le client contient dans la demande de [**création de session**](create-session.md) ; l’en-tête BITS-Supported-Protocol contient la liste. Incluez cet en-tête uniquement si le code de raison est 200 ou 201.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS
</dt> <dd>

GUID de chaîne qui identifie cette session sur le client. Remplacez {GUID} par l’identificateur de session que le client envoie dans tous les paquets de demande suivants.

BITS utilise un GUID pour identifier la session, mais vous pouvez utiliser n’importe quelle chaîne HTTP-Legal jusqu’à 100 caractères.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-ID
</dt> <dd>

Optionnel. Incluez cet en-tête uniquement si la [propriété d’extension IIS bits](bits-iis-extension-properties.md), BITSHostId, est définie. Remplacez PublicHostName par le nom du serveur ou l’adresse IP de la propriété BITSHostId.

Le client doit remplacer la partie serveur de l’URL distante sur tous les paquets suivants. Si le client ne spécifie pas ce nom d’hôte sur les paquets suivants, il est possible que le travail redémarre sur un autre serveur de la batterie, laissant ainsi un fichier de téléchargement partiel sur le serveur précédent.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-ID-repli-Timeout
</dt> <dd>

Optionnel. Incluez cet en-tête uniquement si l’en-tête BITS-Host-ID est spécifié. Remplacez Timeout par la valeur du délai d’attente de la propriété BITSHostIdFallbackTimeout. La propriété BITSHostIdFallbackTimeout est l’une des [propriétés d’extension IIS bits](bits-iis-extension-properties.md).

Le client utilise le délai d’expiration pour déterminer la durée pendant laquelle il tente de se reconnecter au nom du serveur spécifié dans l’en-tête BITS-Host-ID avant de revenir au nom d’hôte spécifié dans le nom de fichier distant du travail. La minuterie commence lorsque BITS ne parvient pas à se connecter au serveur BITS-Host-ID. La minuterie est réinitialisée lors de la restauration d’une connexion au serveur. Si aucun délai d’attente n’est spécifié, le client ne retourne jamais au nom d’hôte spécifié dans le nom de fichier distant.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accepter-encodage
</dt> <dd>

Identifie le schéma d’encodage à utiliser sur les fragments envoyés au serveur. Le paquet fragment contient le fragment encodé dans le corps du paquet. Le serveur BITS requiert l’encodage d’identité (texte en clair). Incluez cet en-tête uniquement si le code de raison est 200 ou 201.

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

[**Créer une session**](create-session.md)
</dt> </dl>

 

 





