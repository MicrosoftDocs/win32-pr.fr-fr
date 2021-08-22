---
description: 'UdpIp_V1_TypeGroup1 classe : cette classe est la classe de type d’événement pour les événements UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: Classe UdpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2c4a16dc8e0d08ab70a15b1d6a887ff8863a1b81c46c4318421df2169fd5d196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069339"
---
# <a name="udpip_v1_typegroup1-class"></a>\_Classe UdpIp v1 \_ TypeGroup1

Cette classe est la classe de type d’événement pour les événements UDP/IP.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a>Membres

La classe **UdpIp \_ v1 \_ TypeGroup1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **UdpIp \_ v1 \_ TypeGroup1** possède ces propriétés.

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), extension (« IPAddr »)
</dt> </dl>

Adresse IP de destination.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5), extension ("port")
</dt> </dl>

Numéro de port de destination.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1)
</dt> </dl>

Identificateur du processus associé à la demande.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), extension (« IPAddr »)
</dt> </dl>

Adresse IP source.

</dd> <dt>

taille
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Taille du paquet.

</dd> <dt>

sport
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6), extension ("port")
</dt> </dl>

Numéro du port source.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**UdpIp \_ v1**](udpip-v1.md)
</dt> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




