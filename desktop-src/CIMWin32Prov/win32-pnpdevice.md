---
description: La \_ classe WMI de l’Association PnPDevice Win32 associe un appareil (connu pour Configuration Manager en tant que PNPEntity) et la fonction qu’il exécute.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Classe Win32_PnPDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516589"
---
# <a name="win32_pnpdevice-class"></a>\_Classe PnPDevice Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PnPDevice Win32** associe un appareil (connu pour Configuration Manager en tant que PNPEntity) et la fonction qu’il exécute. Sa fonction est représentée par une sous-classe de l’appareil logique qui décrit son utilisation. Par exemple, un [**\_ clavier Win32**](win32-keyboard.md) ou une instance [**Win32 \_ DiskDrive**](win32-diskdrive.md) . Les deux objets référencés représentent le même périphérique système sous-jacent ; les modifications apportées à l’allocation des ressources côté PNPEntity affecteront l’appareil associé.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PnPDevice** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PnPDevice** a ces propriétés.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Type de données **: \_ LogicalDevice CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Référence à l’instance du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente les propriétés de l’appareil logique associées à l’appareil plug-and-Play.

</dd> <dt>

**SYSTEME**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ PnPEntity**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")
</dt> </dl>

Référence à l’instance [**Win32 \_ PnPEntity**](win32-pnpentity.md) qui représente l’appareil plug-and-Play associé à l’appareil logique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
