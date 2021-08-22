---
description: Cette classe est la classe de type d’événement pour les événements de message de réception ALPC. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: Classe ALPC_Receive_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98a565ea445ddd803ce217abca3993c2561d464829635bbb1a546824f27c3b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070359"
---
# <a name="alpc_receive_message-class"></a>Classe de message de \_ réception ALPC \_

Cette classe est la classe de type d’événement pour les événements de message de réception ALPC.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Membres

La classe de **\_ \_ message de réception ALPC** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ \_ message de réception ALPC** a ces propriétés.

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



 

 




