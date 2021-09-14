---
description: la \_ classe WMI d’association LogicalProgramGroupDirectory Win32 associe les groupes de programmes logiques (regroupements dans le menu Démarrer) et les répertoires de fichiers dans lesquels elles sont stockées.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239400"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>\_Classe LogicalProgramGroupDirectory Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LogicalProgramGroupDirectory Win32** associe les groupes de programmes logiques (regroupements dans le menu **Démarrer** ) et les répertoires de fichiers dans lesquels elles sont stockées.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ LogicalProgramGroupDirectory** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ LogicalProgramGroupDirectory** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroup")
</dt> </dl>

Référence à l’instance de qui représente le groupe de programmes logique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ répertoire win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| répertoire win32 Win32 \_ »)
</dt> </dl>

Référence à l’instance représentant le répertoire de fichiers pour le groupe de programmes logique.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ LogicalProgramGroupDirectory** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

le processus appelant qui utilise cette classe doit avoir le privilège **SE \_ restore \_ NAME** sur l’ordinateur où se trouve le registre. Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège. Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

