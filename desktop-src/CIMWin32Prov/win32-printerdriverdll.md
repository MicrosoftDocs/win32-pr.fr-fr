---
description: La \_ classe WMI de l’Association PrinterDriverDll Win32 lie une imprimante locale et son fichier de pilote.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriverDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483696"
---
# <a name="win32_printerdriverdll-class"></a>\_Classe PrinterDriverDll Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PrinterDriverDll Win32** lie une imprimante locale et son fichier de pilote.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PrinterDriverDll** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PrinterDriverDll** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ fichier** de données CIM
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Référence à l’instance de fichier de fichier [**CIM \_**](cim-datafile.md) représentant le fichier de pilote pour cette imprimante Windows.

Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ imprimante Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Référence à l’instance de l' [**\_ imprimante Win32**](win32-printer.md) .

Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ PrinterDriverDll** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
