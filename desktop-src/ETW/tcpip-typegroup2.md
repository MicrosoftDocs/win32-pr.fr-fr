---
description: Cette classe est la classe de type d’événement pour les événements de connexion TCP/IP IPv4 et d’acceptation. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: Classe TcpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 316daec5b6bb186756f8597a63ee35d18125181b6575ae24c8ba8fae63f53d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814499"
---
# <a name="tcpip_typegroup2-class"></a>TcpIp \_ TypeGroup2, classe

Cette classe est la classe de type d’événement pour les événements de connexion TCP/IP IPv4 et d’acceptation.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
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

La classe **TcpIp \_ TypeGroup2** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **TcpIp \_ TypeGroup2** possède les propriétés suivantes.

<dl> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (15)**, **pointeur**
</dt> </dl>

Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.

</dd> <dt>

**daddr**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (3)**, **extension (« IPAddrV4 »)**
</dt> </dl>

Adresse IP de destination.

</dd> <dt>

**dport**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (5)**, **extension ("port")**
</dt> </dl>

Numéro de port de destination.

</dd> <dt>

**MSS**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (7)**
</dt> </dl>

Taille de segment maximale.

</dd> <dt>

**ELECTRIQUE**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (1)**
</dt> </dl>

Identificateur du processus associé à la demande.

</dd> <dt>

**rcvwin**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (11)**
</dt> </dl>

Taille de la fenêtre de réception TCP.

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (12)**
</dt> </dl>

Facteur d’échelle de la fenêtre de réception TCP.

</dd> <dt>

**sackopt**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (8)**
</dt> </dl>

Option d’accusé de réception sélectif (SACK) dans l’en-tête TCP.

</dd> <dt>

**saddr**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (4)**, **extension (« IPAddrV4 »)**
</dt> </dl>

Adresse IP source.

</dd> <dt>

**SeqNum**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (14)**
</dt> </dl>

Numéro de séquence.

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (2)**
</dt> </dl>

Taille du paquet.

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (13)**
</dt> </dl>

Facteur d’échelle de la fenêtre d’envoi TCP.

</dd> <dt>

**sport**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (6)**, **extension ("port")**
</dt> </dl>

Numéro du port source.

</dd> <dt>

**tsopt**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (9)**
</dt> </dl>

Option d’horodatage dans l’en-tête TCP.

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId (10)**
</dt> </dl>

Option de mise à l’échelle de fenêtre dans l’en-tête TCP.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Msafd**](tcpip.md)
</dt> </dl>

 

 




