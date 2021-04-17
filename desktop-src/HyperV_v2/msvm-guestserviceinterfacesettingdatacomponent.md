---
description: Classe d’association entre un composant d’interface de service invité et la ressource de service invité.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Classe Msvm_GuestServiceInterfaceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201602"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a>MSVM \_ GuestServiceInterfaceSettingDataComponent, classe

Classe d’association entre un composant d’interface de service invité et la ressource de service invité.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GuestServiceInterfaceSettingDataComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GuestServiceInterfaceSettingDataComponent** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ GuestServiceInterfaceComponentSettingData**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**substitution**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ GuestServiceInterfaceComponentSettingData MSVM**](msvm-guestserviceinterfacecomponentsettingdata.md) référençant le composant d’interface de service invité.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ SettingData CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ SettingData CIM**](cim-settingdata.md) qui fait référence à la ressource de service invité.

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

[**\_Composant CIM**](cim-component.md)
</dt> </dl>

 

