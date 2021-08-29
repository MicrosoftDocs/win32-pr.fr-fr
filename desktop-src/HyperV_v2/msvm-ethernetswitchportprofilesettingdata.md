---
description: Représente les paramètres de profil de port.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Classe Msvm_EthernetSwitchPortProfileSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d90106690346b98e466d35028eb09d67386b89e9a04e05642fe130ecac290164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789929"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a>MSVM \_ EthernetSwitchPortProfileSettingData, classe

Représente les paramètres de profil de port.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchPortProfileSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchPortProfileSettingData** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. cette propriété est héritée de la [**\_ propriété managedelement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « profil de Port de commutateur Ethernet Paramètres ».

</dd> <dt>

**CdnLabelId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

identificateur d’étiquette CDN.

</dd> <dt>

**CdnLabelString**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

chaîne d’étiquette CDN.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « représente les paramètres du profil de port ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. cette propriété est héritée de la [**\_ propriété managedelement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « profil de Port de commutateur Ethernet Paramètres ».

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

**ID NetCfgInstanceId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Identificateur d’appareil unique de la sous-interface.

</dd> <dt>

**PciBusNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numéro de bus PCI.

</dd> <dt>

**PciDeviceNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numéro du périphérique PCI.

</dd> <dt>

**PciFunctionNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numéro de fonction PCI.

</dd> <dt>

**PciSegmentNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Numéro de segment PCI.

</dd> <dt>

**ProfileData**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Données supplémentaires pour le profil de port.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Identificateur du profil de port.

</dd> <dt>

**ProfileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Nom du profil de port.

</dd> <dt>

**VendorId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Identificateur du fournisseur définissant le profil.

</dd> <dt>

**VendorName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Nom du fournisseur définissant le profil.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

