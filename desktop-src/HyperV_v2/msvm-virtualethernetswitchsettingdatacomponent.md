---
description: Association utilisée pour établir &\# 0034 ; partie de&\# 0034 ; relations entre une instance de MSVM \_ VirtualEthernetSwitchSettingData et une ou plusieurs instances de MSVM \_ EthernetSwitchFeatureSettingData.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Classe Msvm_VirtualEthernetSwitchSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52c64997ebc0bbcda5cbf8a81416827670597c647e9c3ee1d3a4cab76d9f4cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949661"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a>MSVM \_ VirtualEthernetSwitchSettingDataComponent, classe

Association utilisée pour établir des relations de « partie de » entre une instance de [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) et une ou plusieurs instances de [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualEthernetSwitchSettingDataComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualEthernetSwitchSettingDataComponent** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ VirtualEthernetSwitchSettingData**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) qui représente un port Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ EthernetSwitchFeatureSettingData**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) qui représente les paramètres appliqués au commutateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

