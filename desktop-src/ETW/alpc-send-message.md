---
description: Cette classe est la classe de type d’événement pour les événements de message d’envoi ALPC. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: Classe ALPC_Send_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8a3e53e514f80f89f1b1e97c1edde9b86add0db7a29de9443c5a1b48085a40fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070329"
---
# <a name="alpc_send_message-class"></a>Classe de message d' \_ envoi ALPC \_

Cette classe est la classe de type d’événement pour les événements de message d’envoi ALPC.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Membres

La classe de **\_ \_ message d’envoi ALPC** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ \_ message d’envoi ALPC** a ces propriétés.

<dl> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du message.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




