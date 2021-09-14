---
description: La \_ classe WMI de l’Association SystemOperatingSystem Win32 associe un système informatique et son système d’exploitation.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Classe Win32_SystemOperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999427"
---
# <a name="win32_systemoperatingsystem-class"></a>\_Classe SystemOperatingSystem Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemOperatingSystem Win32** associe un système informatique et son système d’exploitation.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemOperatingSystem** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemOperatingSystem** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)
</dt> </dl>

Un [**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) qui décrit les propriétés du système informatique sur lequel le système d’exploitation est installé.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ OperatingSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")
</dt> </dl>

[**Win32 \_ OperatingSystem**](win32-operatingsystem.md) qui décrit les propriétés du système d’exploitation en cours d’exécution sur ce système informatique.

</dd> <dt>

**Serveur primaire**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Système d’exploitation DMTF \| 001,4»)
</dt> </dl>

Si la **valeur est true**, le système d’exploitation installé est le système d’exploitation par défaut pour le système informatique.

Cette propriété est héritée de [**CIM \_ installed**](cim-installedos.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SystemOperatingSystem** est dérivée de [**CIM \_ installed**](cim-installedos.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CIM \_ installé**](cim-installedos.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
