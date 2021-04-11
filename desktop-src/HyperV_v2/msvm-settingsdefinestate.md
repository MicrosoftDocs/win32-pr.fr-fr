---
description: Associe un ordinateur virtuel et ses appareils à des instances de CIM \_ SettingData qui représentent les paramètres actuels qui s’appliquent à ces objets.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Classe Msvm_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203602"
---
# <a name="msvm_settingsdefinestate-class"></a>MSVM \_ SettingsDefineState, classe

Associe un ordinateur virtuel et ses appareils à des instances de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) qui représentent les paramètres actuels qui s’appliquent à ces objets. Plus spécifiquement, il associe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) à des instances de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)et associe ** \_ \* MSVM* _ DERIVES de [_ *CIM \_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) avec les dérivés **MSVM \_ \** _ de [_ *CIM \_ ResourceAllocationSettingData* *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SettingsDefineState** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SettingsDefineState** possède les propriétés suivantes.

<dl> <dt>

**Propriété ManagedElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’ordinateur virtuel.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence aux paramètres actuellement actifs pour l’ordinateur virtuel.

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ SettingsDefineState** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGSDEFINESTATE CIM**](cim-settingsdefinestate.md)
</dt> <dt>

[**\_SETTINGSDEFINESTATE CIM**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Classes de gestion du système virtuel](virtual-system-management-classes.md)
</dt> </dl>

 

