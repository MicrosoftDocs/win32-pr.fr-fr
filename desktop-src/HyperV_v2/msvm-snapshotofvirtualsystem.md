---
description: Associe un système virtuel à un instantané qui a été capturé à partir du système virtuel.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Classe Msvm_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc1971c1123ab30fb88da9278b1d4f142e35785a393a75e1bf8a3ec69771f98a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950298"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a>MSVM \_ SnapshotOfVirtualSystem, classe

Associe un système virtuel à un instantané qui a été capturé à partir du système virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SnapshotOfVirtualSystem** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SnapshotOfVirtualSystem** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente le système virtuel. Cette propriété est dérivée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente l’instantané. Cette propriété est dérivée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

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

[**\_SNAPSHOTOFVIRTUALSYSTEM CIM**](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[**CreateSnapshot**](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

