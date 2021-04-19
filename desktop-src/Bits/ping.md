---
title: Ping
description: Utilisez le paquet ping pour établir une connexion et négocier la sécurité avec le serveur.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- BITS ping
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "106510449"
---
# <a name="ping"></a>Ping

Utilisez le paquet **ping** pour établir une connexion et négocier la sécurité avec le serveur.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>headers

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits
</dt> <dd>

Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.

Remplacez l’URL distante par l’URI absolu ou relatif. Remplacez généralement l’URL distante par le nom de fichier distant du travail.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type
</dt> <dd>

Identifie ce paquet de requête en tant que paquet ping.

</dd> </dl>

## <a name="remarks"></a>Notes

Le paquet **ping** est facultatif. Au lieu d’envoyer un paquet **ping** , vous pouvez utiliser le paquet [**Create-session**](create-session.md) pour établir une connexion et négocier la sécurité. Toutefois, il est plus efficace d’utiliser le paquet **ping** à cet effet.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACK pour ping**](ack-for-ping.md)
</dt> <dt>

[**Créer une session**](create-session.md)
</dt> </dl>

 

 




