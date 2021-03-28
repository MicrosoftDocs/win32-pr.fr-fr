---
description: Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: Classe SystemConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951209"
---
# <a name="systemconfig_nic-class"></a>\_Classe de carte réseau SystemConfig

Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a>Membres

La classe de **\_ carte réseau SystemConfig** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ carte réseau SystemConfig** a ces propriétés.

<dl> <dt>

DnsServerAddresses
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Adresses IP à utiliser pour l’interrogation des serveurs DNS. La liste des adresses est délimitée par des virgules.

</dd> <dt>

AdressesIP
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Adresses IP associées à la carte d’interface réseau. La liste des adresses est délimitée par des virgules.

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Index de l’adaptateur pour la carte réseau IPv4. L’index de l’adaptateur peut changer lorsqu’un adaptateur est désactivé, puis activé, ou dans d’autres circonstances, et ne doit pas être considéré comme persistant.

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Index de l’adaptateur pour la carte réseau IPv6. L’index de l’adaptateur peut changer lorsqu’un adaptateur est désactivé, puis activé, ou dans d’autres circonstances, et ne doit pas être considéré comme persistant.

</dd> <dt>

NICDescription
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Description de l’adaptateur.

</dd> <dt>

PhysicalAddr
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), format ("x")
</dt> </dl>

Adresse matérielle de la carte.

</dd> <dt>

PhysicalAddrLen
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Longueur de l’adresse matérielle de la carte.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




