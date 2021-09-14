---
description: La \_ classe WMI de l’Association SystemBIOS Win32 associe un système informatique (y compris des données telles que les propriétés de démarrage, les fuseaux horaires, les configurations de démarrage ou les mots de passe d’administration) et un BIOS système (services, langues et propriétés de gestion du système).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Classe Win32_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999455"
---
# <a name="win32_systembios-class"></a>\_Classe SystemBIOS Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemBIOS Win32** associe un système informatique (y compris des données telles que les propriétés de démarrage, les fuseaux horaires, les configurations de démarrage ou les mots de passe d’administration) et un BIOS système (services, langues et propriétés de gestion du système).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemBIOS** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemBIOS** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)
</dt> </dl>

Le [**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) qui contient le BIOS de l’Association.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ BIOS Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« PartComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| BIOS Win32 WMI \_ »)
</dt> </dl>

Un [**\_ BIOS Win32**](win32-bios.md) contenu dans le système informatique de cette association.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SystemBIOS** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
