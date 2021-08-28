---
description: Représente l’association entre les extensions Ethernet et leurs fonctionnalités.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Classe Msvm_EthernetSwitchExtensionCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22ff1cd8d720dcb42ae71b1155b7cd69dbc8d098f0cd8ad799f1d47c448c8c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148345"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a>MSVM \_ EthernetSwitchExtensionCapabilities, classe

Représente l’association entre les extensions Ethernet et leurs fonctionnalités.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchExtensionCapabilities** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchExtensionCapabilities** possède les propriétés suivantes.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Capabilities")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) qui représente l’objet de fonctionnalités associé au commutateur. Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> <dt>

**Caractéristiques**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations descriptives sur les fonctionnalités de. Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).



| Valeur                                                                                                                                                                                                                       | Signification                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Par défaut**</dt> <dt>2</dt> </dl> | Les fonctionnalités associées représentent les fonctionnalités par défaut de l’élément géré.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Actuel**</dt> <dt>3</dt> </dl> | Les fonctionnalités associées représentent les fonctionnalités actuelles de l’élément managé.<br/> |



 

</dd> <dt>

**Propriété ManagedElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("propriété ManagedElement")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) qui représente l’extension installée. Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

