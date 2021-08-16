---
title: Cancel-Session
description: Utilisez le paquet Cancel-Session pour mettre fin à la session de téléchargement avec le serveur BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session BITS
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d570a49d1a5ba632fbbb453b6397338af70d29b0dc837db12193d2889c867eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835108"
---
# <a name="cancel-session"></a>Cancel-Session

Utilisez le paquet **Cancel-session** pour mettre fin à la session de téléchargement avec le serveur bits.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>headers

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits
</dt> <dd>

Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.

Remplacez l’URL distante par l’URI absolu ou relatif. Remplacez généralement l’URL distante par le nom de fichier distant du travail. Pour les considérations relatives à l’équilibrage de la charge réseau, consultez l’en-tête BITS-Host-ID dans le paquet [**Create-session**](create-session.md) .

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type
</dt> <dd>

Identifie ce paquet de demande en tant que Cancel-Session paquet.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS
</dt> <dd>

GUID de chaîne qui identifie la session sur le serveur. Remplacez {GUID} par l’identificateur de session que le serveur renvoie dans le paquet [**d’accusé de réception de la réponse de création de session**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce paquet annule un travail de chargement s’il est envoyé avant l’envoi du dernier fragment. Cancel-Session n’a aucun effet sur un fichier dont le dernier fragment a déjà été envoyé. Quand le serveur BITS reçoit le dernier fragment, il écrit le fichier dans sa destination finale et, dans le cas d’une opération de chargement-réponse, publie le fichier dans l’application serveur. Dans le cas de chargement-réponse, le paquet Cancel-Session annule la partie réponse d’une tâche de chargement-réponse.

Le serveur BITS libère toutes les ressources et supprime tous les fichiers temporaires lorsqu’il reçoit ce paquet.

Le client BITS envoie ce paquet lorsque l’utilisateur annule le travail.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACK pour Create-session**](ack-for-create-session.md)
</dt> <dt>

[**Fermer-session**](close-session.md)
</dt> </dl>

 

 




