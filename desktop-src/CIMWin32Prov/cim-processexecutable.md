---
description: La \_ classe CIM ProcessExecutable représente un lien entre un processus et un fichier de données, et indique que le fichier participe à l’exécution du processus.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: Classe CIM_ProcessExecutable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e55d5116c4f3f9d14840b5a5e0b75205156dbbaee3aa21c2d14dbb25c53d4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080413"
---
# <a name="cim_processexecutable-class"></a>\_Classe CIM ProcessExecutable

La classe **CIM \_ ProcessExecutable** représente un lien entre un processus et un fichier de données, et indique que le fichier participe à l’exécution du processus.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ProcessExecutable** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ProcessExecutable** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ fichier** de données CIM
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Un fichier de données CIM qui décrit le fichier de données qui participe à l’exécution du processus. [**\_**](cim-datafile.md)

</dd> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Adresse de base du module dans l’espace d’adressage du processus associé.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ processus CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (dépendant), [**clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**\_ Processus CIM**](cim-process.md) qui décrit le processus.

</dd> <dt>

**GlobalProcessCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Nombre actuel de processus sur lesquels le fichier est chargé en mémoire.

</dd> <dt>

**ModuleInstance**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »)
</dt> </dl>

Handle d’instance Win32. Cette propriété est obsolète et il n’y a aucune valeur de remplacement.

</dd> <dt>

**ProcessCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Nombre de références du fichier dans le processus associé.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ ProcessExecutable** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

WMI implémente la classe **CIM \_ ProcessExecutable** . La **classe \_ ProcessExecutable CIM** est une classe dynamique.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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
</dt> </dl>

 

