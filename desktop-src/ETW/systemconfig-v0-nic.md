---
description: Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: Classe SystemConfig_V0_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973647"
---
# <a name="systemconfig_v0_nic-class"></a>\_Classe de \_ carte réseau SystemConfig v0

Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a>Membres

La classe de **\_ \_ carte réseau SystemConfig v0** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ \_ carte réseau SystemConfig v0** possède ces propriétés.

<dl> <dt>

**Données**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (16)
</dt> </dl>

Champ de données.

</dd> <dt>

**DhcpServer**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (8)
</dt> </dl>

Adresse IP du serveur DHCP (Dynamic Host Configuration Protocol). La valeur 255.255.255.255 indique que le serveur DHCP n’a pas pu être atteint ou qu’il est en train d’être atteint. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (12)
</dt> </dl>

Premières adresses IP de serveur à utiliser pour l’interrogation des serveurs DNS. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (13)
</dt> </dl>

Deuxième adresse IP du serveur à utiliser pour l’interrogation des serveurs DNS. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (14)
</dt> </dl>

Adresses IP de troisième serveur à utiliser pour l’interrogation des serveurs DNS. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (15)
</dt> </dl>

Quatrième adresses IP de serveur à utiliser pour l’interrogation des serveurs DNS. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**Passerelle**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (9)
</dt> </dl>

Adresse IP de la passerelle par défaut utilisée par le système de l’ordinateur. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2)
</dt> </dl>

Index de l’adaptateur. L’index de l’adaptateur peut changer lorsqu’un adaptateur est désactivé, puis activé, ou dans d’autres circonstances, et ne doit pas être considéré comme persistant.

</dd> <dt>

**IpAddress**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6)
</dt> </dl>

Adresses IP associées à la carte d’interface réseau. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**NICName**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1), **Max** (256)
</dt> </dl>

Nom de la carte d’interface réseau.

</dd> <dt>

**PhysicalAddr**
</dt> <dd> <dl> <dt>

Type de données : **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4), **Max** (8)
</dt> </dl>

Adresse matérielle de la carte.

</dd> <dt>

**PhysicalAddrLen**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3)
</dt> </dl>

Longueur de l’adresse matérielle de la carte.

</dd> <dt>

**PrimaryWinsServer**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (10)
</dt> </dl>

Adresse IP du serveur WINS principal. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**SecondaryWinsServer**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (11)
</dt> </dl>

Adresse IP du serveur WINS secondaire. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> <dt>

**Taille**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5)
</dt> </dl>

Taille, en octets, de la propriété de données.

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7)
</dt> </dl>

Masque de sous-réseau associé à la carte d’interface réseau. Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




