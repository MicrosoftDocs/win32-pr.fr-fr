---
description: La \_ classe WMI de l’Association SystemUsers Win32 associe un système informatique et un compte d’utilisateur sur ce système.
ms.assetid: 0f6cba69-86f7-4795-a47d-6fb8ed0a00b8
ms.tgt_platform: multiple
title: Classe Win32_SystemUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemUsers
- Win32_SystemUsers.GroupComponent
- Win32_SystemUsers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2239983d5b9c080c60d301a557b5487f8cf7fcf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950818"
---
# <a name="win32_systemusers-class"></a>\_Classe SystemUsers Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemUsers Win32** associe un système informatique et un compte d’utilisateur sur ce système.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemUsers : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_UserAccount    REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemUsers** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemUsers** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)
</dt> </dl>

Référence à l’instance de qui représente le système informatique contenant le compte d’utilisateur.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ UserAccount**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ UserAccount")
</dt> </dl>

Référence à l’instance de qui représente le compte d’utilisateur sur le système informatique.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SystemUsers** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
