---
description: Association générique utilisée pour établir une partie des relations entre une instance de \_ VIRTUALSYSTEMSETTINGDATA CIM et une ou plusieurs instances de \_ ResourceAllocationSettingData CIM.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Classe Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 485ac065f91a83479081a3cddd89cbae5b6eaa95bc3a30733371075226f58cdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083149"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a>MSVM \_ VirtualSystemSettingDataComponent, classe

Association générique utilisée pour établir des relations de « partie de » entre une instance [**de \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) et une ou plusieurs instances [**de \_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemSettingDataComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemSettingDataComponent** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **override**, **min** (1), **Max** (1)
</dt> </dl>

Élément parent dans l’Association. Cette propriété est héritée de la [**\_ VirtualSystemSettingDataComponent CIM**](/previous-versions//cc150674(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Élément enfant dans l’Association. Cette propriété est héritée de la [**\_ VirtualSystemSettingDataComponent CIM**](/previous-versions//cc150674(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ VirtualSystemSettingDataComponent** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](/previous-versions//cc150674(v=vs.85))
</dt> <dt>

[Classes du système virtuel](virtual-system-classes.md)
</dt> </dl>

 

