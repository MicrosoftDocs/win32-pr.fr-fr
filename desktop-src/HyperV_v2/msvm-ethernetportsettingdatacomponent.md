---
description: Association utilisée pour établir &\# 0034 ; partie de&\# 0034 ; relations entre une instance d’un EthernetPortAllocationSettingData MSVM \_ et une ou plusieurs instances d’un EthernetSwitchFeatureSettingData MSVM \_ .
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Classe Msvm_EthernetPortSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 989d734d4c59d710c737c218b22591517347a8f5e434ff99e195887cbb4b6774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524839"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a>MSVM \_ EthernetPortSettingDataComponent, classe

Association utilisée pour établir des relations de « partie de » entre une instance d' [**un \_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) et une ou plusieurs instances d' [**un \_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetPortSettingDataComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetPortSettingDataComponent** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agrégat**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) qui représente le port Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) qui représente les paramètres de fonctionnalités appliqués au port.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

