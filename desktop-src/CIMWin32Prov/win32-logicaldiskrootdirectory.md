---
description: La \_ classe WMI de l’Association LogicalDiskRootDirectory Win32 associe un disque logique et sa structure de répertoires.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Classe Win32_LogicalDiskRootDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1ec5bdbe5ab91b14c294f715aa4fc4fe26ad2a42cd63892f60288456af10505
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973389"
---
# <a name="win32_logicaldiskrootdirectory-class"></a>\_Classe LogicalDiskRootDirectory Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LogicalDiskRootDirectory Win32** associe un disque logique et sa structure de répertoires.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ LogicalDiskRootDirectory** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ LogicalDiskRootDirectory** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ disque logique Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")
</dt> </dl>

Référence à l’instance représentant les propriétés du disque logique.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ répertoire win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« PartComponent »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| répertoire win32 Win32 \_ »)
</dt> </dl>

Référence à l’instance de qui représente les propriétés de la structure de répertoires de fichiers.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ LogicalDiskRootDirectory** est dérivée [**du \_ composant CIM**](cim-component.md).

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

[**\_Composant CIM**](cim-component.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

