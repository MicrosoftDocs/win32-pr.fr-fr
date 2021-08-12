---
description: Le \_ QuickFixEngineering Win32&\# 8194 ; La classe WMI représente une petite mise à jour à l’échelle du système, communément appelée mise à jour du correctif QFE (rapide), appliquée au système d’exploitation actuel.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Classe Win32_QuickFixEngineering
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15110b5801555947eed434b8148aec3cc753f6eec359f32b96cd67a5b2649f31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675011"
---
# <a name="win32_quickfixengineering-class"></a>\_Classe QuickFixEngineering Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ QuickFixEngineering** WMI représente une petite mise à jour à l’échelle du système, communément appelée mise à jour du correctif QFE (rapide), appliquée au système d’exploitation actuel. Cette classe retourne uniquement les mises à jour fournies par la fonction de maintenance basée sur les composants (CBS). Ces mises à jour ne sont pas répertoriées dans le registre. les mises à jour fournies par Microsoft Windows Installer (MSI) ou le site de mise à jour Windows ( [https://update.microsoft.com](https://update.microsoft.com/) ) ne sont pas retournées par **Win32 \_ QuickFixEngineering**.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ QuickFixEngineering** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ QuickFixEngineering** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**propagée**](../wmisdk/standard-qualifiers.md) («[**CIMOM \_ CIM**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" WMI ")
</dt> </dl>

Nom local du système informatique. La valeur de cette propriété provient de la [**classe \_ ComputerSystem CIM**](cim-computersystem.md) .

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**FixComments**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Commentaires supplémentaires liés à la mise à jour.

</dd> <dt>

**HotFixID.**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Identificateur unique associé à une mise à jour particulière.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Indique le moment où l’objet a été installé. L’absence de valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstalledBy**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Personne qui a installé la mise à jour. Si cette valeur est inconnue, la propriété est vide.

</dd> <dt>

**InstalledOn**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Date à laquelle la mise à jour a été installée. Si cette valeur est inconnue, la propriété est vide.

> [!Note]  
> Cette propriété peut utiliser des formats différents, en fonction du moment où le QuickFix a été installé. La plupart des systèmes utilisent un format de date standard, tel que « 23-10-2013 ». Toutefois, certains systèmes peuvent retourner une valeur hexadécimale 64 bits au format [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Win32.

 

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ServicePackInEffect**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Service Pack en vigueur lorsque la mise à jour a été appliquée. Si aucun Service Pack n’a été appliqué, la propriété prend la valeur SP0. S’il n’est pas possible de déterminer ce que Service Pack était en vigueur, cette propriété a la **valeur null**.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Chaîne qui indique l’état actuel de l’objet. L’état opérationnel et non opérationnel peut être défini. L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ». « Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).

L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ». Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ QuickFixEngineering** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).

Étant donné que les mises à jour sont stockées à deux emplacements, une énumération de cette classe peut entraîner des doublons.

Un correctif est un correctif de système d’exploitation temporaire produit par le groupe d’ingénierie de correction rapide chez Microsoft. à l’instar des service packs, les correctifs représentent les modifications apportées à une version de Windows après la publication du système d’exploitation.

Contrairement aux service packs, les correctifs ne sont pas destinés à une installation permanente sur tous les ordinateurs. Au lieu de cela, ils sont développés pour résoudre des problèmes très spécifiques, souvent pour des configurations d’ordinateur spécifiques.

En outre, les correctifs représentent des installations indépendantes qui ne dépendent pas d’autres correctifs publiés. Par exemple, un hypothétique correctif 4 n’inclut pas les correctifs de bogues et les fonctionnalités incluses dans les correctifs à chaud 1, 2 et 3. Dans la plupart des cas, il n’y aurait pas non plus besoin d’installer les correctifs 1, 2 et 3 avant d’installer le correctif 4 à chaud. Cela permet à l’énumération des correctifs individuels d’effectuer une tâche administrative importante : pour connaître la configuration exacte d’un ordinateur, vous devez savoir non seulement quels service packs ont été installés, mais également quels correctifs ont été installés.

La **classe \_ QuickFixEngineering Win32** vous permet d’énumérer tous les correctifs logiciels qui ont été installés sur un ordinateur

## <a name="examples"></a>Exemples

L’exemple d' [extraction de programmes installés](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) dans PowerShell retourne la liste complète des programmes installés.

L’exemple VBScript suivant énumère les correctifs logiciels installés sur un ordinateur


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[Tâches WMI : systèmes d’exploitation](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
