---
title: Close-Session
description: Utilisez le paquet Close-Session pour indiquer au serveur BITS que le téléchargement de fichiers est terminé et pour mettre fin à la session.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ae1318a99e690b13f4f0cad03624fb351c359efbcb1be9e105076ce53ceba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021197"
---
# <a name="close-session"></a>Close-Session

Utilisez le paquet **Close-session** pour indiquer au serveur bits que le téléchargement de fichiers est terminé et pour mettre fin à la session.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
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

Identifie ce paquet de demande en tant que Close-Session paquet.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS
</dt> <dd>

GUID de chaîne qui identifie la session sur le serveur. Remplacez {GUID} par l’identificateur de session que le serveur renvoie dans le paquet [**d’accusé de réception de la réponse de création de session**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

Le serveur BITS libère toutes les ressources et supprime tous les fichiers temporaires lorsqu’il reçoit ce paquet.

Pour les travaux de chargement-réponse, vous devez télécharger la réponse avant d’envoyer **Close-session**. Dans le cas contraire, la réponse est perdue.

Si vous envoyez ce paquet avant de télécharger tous les fragments, le fichier de téléchargement est supprimé. vous ne pouvez pas télécharger un fichier partiel.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACK pour Close-session**](ack-for-close-session.md)
</dt> <dt>

[**Annuler-session**](cancel-session.md)
</dt> <dt>

[**Créer une session**](create-session.md)
</dt> </dl>

 

 




