---
description: Représente la configuration d’une carte réseau dans le système d’exploitation invité.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Classe Msvm_GuestNetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0c208a14a8db57303b3ccc857ca15a5d7f88369b7093b9931c0c9cb80012230d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147974"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a>MSVM \_ GuestNetworkAdapterConfiguration, classe

Représente la configuration d’une carte réseau dans le système d’exploitation invité.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GuestNetworkAdapterConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GuestNetworkAdapterConfiguration** possède les propriétés suivantes.

<dl> <dt>

**DefaultGateways**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de chaînes qui contient les passerelles IP par défaut configurées sur la carte réseau au sein du système d’exploitation invité. Le nombre maximal de passerelles IP par défaut qui peuvent être configurées sur une seule carte réseau est de cinq.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le protocole DHCP est activé sur la carte réseau au sein du système d’exploitation invité.

</dd> <dt>

**DNSServers**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de chaînes contenant les serveurs DNS configurés sur la carte réseau au sein du système d’exploitation invité.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificateur unique de cet objet.

</dd> <dt>

**IPAddresses**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de chaînes contenant les adresses IP configurées sur la carte réseau au sein du système d’exploitation invité.

</dd> <dt>

**IPAddressOrigins**
</dt> <dd> <dl> <dt>

Type de données : tableau **UINT16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Source des adresses IP configurées sur la carte réseau au sein du système d’exploitation invité.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

**Statique** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie les protocoles IP auxquels s’appliquent les paramètres spécifiés par cette instance.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

**IPv4/v6** (4098)


</dt> <dd></dd> </dl>

</dd> <dt>

**Sous-réseaux**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de chaînes qui contient les sous-réseaux configurés sur la carte réseau au sein du système d’exploitation invité. Chaque élément de ce tableau s’applique à l’élément correspondant dans le tableau **adressesIP** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

