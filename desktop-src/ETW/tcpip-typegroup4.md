---
description: Cette classe est la classe de type d’événement pour les événements de connexion et d’acceptation TCP/IP IPv6. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: Classe TcpIp_TypeGroup4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754252"
---
# <a name="tcpip_typegroup4-class"></a>TcpIp \_ TypeGroup4, classe

Cette classe est la classe de type d’événement pour les événements de connexion et d’acceptation TCP/IP IPv6.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Membres

La classe **TcpIp \_ TypeGroup4** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **TcpIp \_ TypeGroup4** possède les propriétés suivantes.

<dl> <dt>

ID
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (15), pointeur
</dt> </dl>

Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), extension (« IPAddrV6 »)
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

**MSS**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7)
</dt> </dl>

Taille de segment maximale.

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

**rcvwin**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (11)
</dt> </dl>

Taille de la fenêtre de réception TCP.

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (12)
</dt> </dl>

Facteur d’échelle de la fenêtre de réception TCP.

</dd> <dt>

**sackopt**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (8)
</dt> </dl>

Option d’accusé de réception sélectif (SACK) dans l’en-tête TCP.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), extension (« IPAddrV6 »)
</dt> </dl>

Adresse IP source.

</dd> <dt>

SeqNum
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (14)
</dt> </dl>

Numéro de séquence.

</dd> <dt>

est
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Taille du paquet.

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (13)
</dt> </dl>

Facteur d’échelle de la fenêtre d’envoi TCP.

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

</dd> <dt>

**tsopt**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (9)
</dt> </dl>

Option d’horodatage dans l’en-tête TCP.

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (10)
</dt> </dl>

Option de mise à l’échelle de fenêtre dans l’en-tête TCP.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Msafd**](tcpip.md)
</dt> </dl>

 

 




