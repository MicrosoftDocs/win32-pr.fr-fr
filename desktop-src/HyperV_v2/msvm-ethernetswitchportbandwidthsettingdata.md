---
description: Représente les paramètres de la bande passante du port.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Classe Msvm_EthernetSwitchPortBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521145"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a>MSVM \_ EthernetSwitchPortBandwidthSettingData, classe

Représente les paramètres de la bande passante du port.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchPortBandwidthSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchPortBandwidthSettingData** possède les propriétés suivantes.

<dl> <dt>

**BurstLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Bande passante maximale autorisée à partir du port au cours des pics.

</dd> <dt>

**BurstSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Taille de rafale maximale autorisée.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de la bande passante du port commuté Ethernet ».

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente les paramètres de bande passante du port ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de la bande passante du port commuté Ethernet ».

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Limite de bande passante autorisée pour le port.

</dd> <dt>

**Réservation**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Bande passante absolue minimale garantie pour le port.

</dd> <dt>

**Poids**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

La bande passante minimale du poids est garantie pour le port.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

