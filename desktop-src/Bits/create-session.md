---
title: Create-Session
description: Utilisez le paquet Create-Session pour demander une session de chargement avec le serveur BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639db08c5a29b09f5c32d7b0243de66f2c4dced001a1ff2afa7e74837c8d67e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021187"
---
# <a name="create-session"></a>Create-Session

Utilisez le paquet **Create-session** pour demander une session de chargement avec le serveur bits.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>headers

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits
</dt> <dd>

Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.

Remplacez l’URL distante par l’URI absolu ou relatif. Remplacez généralement l’URL distante par le nom de fichier distant du travail. Pour plus d’informations sur l’équilibrage de charge réseau, consultez l’en-tête BITS-Host-ID.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type
</dt> <dd>

Identifie ce paquet de demande en tant que Create-Session paquet.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-protocoles pris en charge
</dt> <dd>

Liste délimitée par des espaces des protocoles pris en charge par le client. Utilisez des GUID de chaîne pour identifier les protocoles. Spécifiez la liste par ordre de préférence, du plus au moins préféré. Le tableau suivant répertorie le protocole pris en charge par le client BITS. Remplacer {GUID1}... {guidn} avec un ou plusieurs GUID de chaîne dans la liste.



| Protocole                                          | Description                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | protocole Télécharger BITS 1,5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous devez envoyer un paquet [**ping**](ping.md) pour établir une connexion http avant d’envoyer le paquet Create-Session. Le paquet Create-Session peut également établir la connexion ; Toutefois, le Create-Session paquet est moins efficace.

Le serveur sélectionne le protocole qu’il souhaite utiliser dans la liste fournie par le client dans l’en-tête BITS-Supported-Protocols. Le serveur retourne le protocole sélectionné dans l’en-tête BITS-Protocol de l’accusé de réception pour le paquet de réponse de [**création de session**](ack-for-create-session.md) .

Le client s’attend à ce que le serveur retourne un [**accusé de réception pour le paquet de réponse de création de session**](ack-for-create-session.md) . Si le serveur a pu établir une session, le client utilise le paquet de demande de [**fragment**](fragment.md) pour envoyer des plages du fichier au serveur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACK pour Create-session**](ack-for-create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 





