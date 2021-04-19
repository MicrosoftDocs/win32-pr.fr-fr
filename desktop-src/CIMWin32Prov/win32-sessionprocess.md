---
description: La \_ classe WMI d’association SessionProcess Win32 représente une association entre une ouverture de session et les processus associés à cette session.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Classe Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516562"
---
# <a name="win32_sessionprocess-class"></a>\_Classe SessionProcess Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) d’association **\_ SessionProcess Win32** représente une association entre une ouverture de session et les processus associés à cette session.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionProcess** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionProcess** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ LogonSession**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**clé**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) qui représente la session associée au processus.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ processus Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (« Dependent »), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ Processus Win32**](win32-processor.md) qui représente le processus associé à la session.

</dd> </dl>

## <a name="remarks"></a>Notes

**Win32 \_ SessionProcess** retourne l’ensemble de la session de l’administrateur lorsqu’il est connecté avec élévation de privilèges ou lorsqu’il est exécuté à distance. Il s’agit d’une extension du comportement de la classe.

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

[**\_SessionResource Win32**](win32-sessionresource.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
