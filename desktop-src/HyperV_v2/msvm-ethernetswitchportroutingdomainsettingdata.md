---
description: Représente les données de paramètre du domaine de routage.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Classe Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869270"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a>MSVM \_ EthernetSwitchPortRoutingDomainSettingData, classe

Représente les données de paramètre du domaine de routage.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchPortRoutingDomainSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchPortRoutingDomainSettingData** possède les propriétés suivantes.

<dl> <dt>

**IsolationIdList**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (3), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

ID VirtualSubnetId ou VLAN pour les domaines de routage.

</dd> <dt>

**IsolationIdNameList**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (4), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Tableau de noms conviviaux VirtualSubnetId ou VLAN.

</dd> <dt>

**RoutingDomainGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

GUID du domaine de routage.

</dd> <dt>

**RoutingDomainName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Nom convivial du domaine de routage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

