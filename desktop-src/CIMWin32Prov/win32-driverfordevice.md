---
description: La \_ classe WMI de l’Association DriverForDevice Win32 associe une instance d’imprimante à une instance de pilote d’imprimante.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Classe Win32_DriverForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519222"
---
# <a name="win32_driverfordevice-class"></a>\_Classe DriverForDevice Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ DriverForDevice Win32** associe une instance d’imprimante à une instance de pilote d’imprimante.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ DriverForDevice** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ DriverForDevice** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ imprimante Win32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Référence à l’instance d' [**\_ imprimante Win32**](win32-printer.md) qui représente l’imprimante.

Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ PrinterDriver**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’instance [**Win32 \_ PrinterDriver**](win32-printerdriver.md) qui représente le pilote d’imprimante pour l’imprimante.

Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ DriverForDevice** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

