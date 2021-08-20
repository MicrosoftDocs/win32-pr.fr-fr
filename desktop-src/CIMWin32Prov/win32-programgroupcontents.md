---
description: La \_ classe WMI de l’Association ProgramGroupContents Win32 associe un ordre de groupe de programmes et un groupe de programmes individuel ou un élément qu’elle contient.
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupContents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bd203d00ac8e0de6d25899ccd321651b0edde52b4fa2e1e64a76849bccd887bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118007809"
---
# <a name="win32_programgroupcontents-class"></a>\_Classe ProgramGroupContents Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ ProgramGroupContents Win32** associe un ordre de groupe de programmes et un groupe de programmes individuel ou un élément qu’elle contient.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ ProgramGroupContents** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ProgramGroupContents** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")
</dt> </dl>

Référence à l’instance de qui représente le groupe de programmes logique pour cette association.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ ProgramGroupOrItem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ProgramGroupOrItem")
</dt> </dl>

Référence à l’instance représentant le groupe ou l’élément du menu **Démarrer** pour cette association.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ ProgramGroupContents** est dérivée [**du \_ composant CIM**](cim-component.md).

## <a name="requirements"></a>Conditions requises



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

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
