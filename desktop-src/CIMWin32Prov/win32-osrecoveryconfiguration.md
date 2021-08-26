---
description: Le \_ OSRecoveryConfiguration Win32&\# 8194 ; La classe WMI représente les types d’informations qui seront collectées à partir de la mémoire en cas d’échec du système d’exploitation. Cela comprend les échecs de démarrage et les pannes du système.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Classe Win32_OSRecoveryConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a780e0997ef3a56bc644adda2842b905aaf9744d28a2075fbc4726134c16aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972289"
---
# <a name="win32_osrecoveryconfiguration-class"></a>\_Classe OSRecoveryConfiguration Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OSRecoveryConfiguration** WMI représente les types d’informations qui seront collectées à partir de la mémoire en cas d’échec du système d’exploitation. Cela comprend les échecs de démarrage et les pannes du système.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ OSRecoveryConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ OSRecoveryConfiguration** a ces propriétés.

<dl> <dt>

**Redémarrage**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| reboot")
</dt> </dl>

Le système redémarre automatiquement au cours d’une opération de récupération.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**DebugFilePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| dumpfile")
</dt> </dl>

Chemin d’accès complet au fichier de débogage. Un fichier de débogage est créé avec l’état de la mémoire de l’ordinateur après une défaillance de l’ordinateur.

exemple : « C : \\ Windows \\ Memory. dmp »

</dd> <dt>

**DebugInfoType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Type d’informations de débogage écrites dans le fichier journal.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

**Image mémoire complète** (1)


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

**Image mémoire du noyau** (2)


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

**Image mémoire réduite** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**ExpandedDebugFilePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Version développée de la propriété **DebugFilePath** .

exemple : « C : \\ Windows \\ Memory. dmp »

</dd> <dt>

**ExpandedMiniDumpDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Version développée de la propriété **MiniDumpDirectory** .

exemple : « C : \\ Windows \\ minidump »

</dd> <dt>

**KernelDumpOnly**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| KernelDumpOnly")
</dt> </dl>

Seules les informations de débogage du noyau sont écrites dans le fichier journal de débogage. Si la **valeur est true**, seul l’état du noyau est écrit dans un fichier en cas de défaillance du système. Si la **valeur est false**, le système tente d’enregistrer l’état de la mémoire et tous les appareils qui peuvent fournir des informations sur le système en cas d’échec.

</dd> <dt>

**MiniDumpDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| MiniDumpDir")
</dt> </dl>

Répertoire où les petits fichiers de vidage de mémoire seront enregistrés et accumulés.

Exemple : « % systemRoot% \\ minidump »

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Nom identifiant cette instance de la **classe \_ OSRecoveryConfiguration Win32** .

</dd> <dt>

**OverwriteExistingDebugFile**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| overwrite")
</dt> </dl>

Le nouveau fichier de débogage remplace un fichier existant.

</dd> <dt>

**SendAdminAlert**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| SendAlert")
</dt> </dl>

Le message d’alerte sera envoyé à l’administrateur système en cas de défaillance du système d’exploitation.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**WriteDebugInfo**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| CrashDumpEnabled")
</dt> </dl>

Les informations de débogage doivent être écrites dans un fichier journal.

</dd> <dt>

**WriteToSystemLog**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent")
</dt> </dl>

Les événements seront écrits dans un journal système.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ OSRecoveryConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

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

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
