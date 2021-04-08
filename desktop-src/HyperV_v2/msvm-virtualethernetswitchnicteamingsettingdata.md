---
description: Représente les paramètres d’association de cartes réseau du commutateur.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Classe Msvm_VirtualEthernetSwitchNicTeamingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760851"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a>MSVM \_ VirtualEthernetSwitchNicTeamingSettingData, classe

Représente les paramètres d’association de cartes réseau du commutateur.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** possède les propriétés suivantes.

<dl> <dt>

**LoadBalancingAlgorithm**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Algorithme d’équilibrage de charge.

</dd> <dt>

**TeamingMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Mode d’association.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




