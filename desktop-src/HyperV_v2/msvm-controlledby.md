---
description: Associe un appareil de stockage au contrôleur de stockage qui possède l’appareil.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Classe Msvm_ControlledBy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b08cf97c54363009e839ea78fe139c6c8a1bdd81cac07182d019d3d00857dee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130599"
---
# <a name="msvm_controlledby-class"></a>MSVM \_ ControlledBy, classe

Associe un appareil de stockage au contrôleur de stockage qui possède l’appareil. Cette association est utilisée avec les contrôleurs de disque et IDE.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ControlledBy** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ControlledBy** possède les propriétés suivantes.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Accessibilité de l’appareil via le contrôleur antécédent. Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)et est toujours définie sur 2 (lecture/écriture).

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Priorité donnée aux accès de l’appareil par le biais de ce contrôleur. Le chemin d’accès avec la priorité la plus élevée aura la valeur la plus faible. Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)et est toujours définie sur 0.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le contrôleur commande ou accède activement à l’appareil. Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)et est toujours définie sur 1 (active).

</dd> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence au contrôleur. Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’appareil contrôlé. Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse de l’appareil associé dans le contexte du contrôleur antécédent. Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)et est toujours définie sur 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)et est toujours définie sur 0.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mais elle n’est pas utilisée.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mais elle n’est pas utilisée.

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mais elle n’est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ControlledBy** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[**\_CONTROLLEDBY CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Stockage Catégories](storage-classes.md)
</dt> </dl>

 

