---
Description: Le \_ processus Win32&\# 32 ; La classe WMI représente un processus sur un système d’exploitation.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Win32_Process, classe
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e52ae224aee9db09ffa42cf19b3550a5ff6362326b0058d87e4d2a8b2da1851e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759409"
---
# <a name="win32_process-class"></a>\_Classe de processus Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ processus Win32** représente un processus sur un système d’exploitation.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

> [!NOTE]
> pour une présentation générale des processus et des threads dans Windows, consultez la rubrique [processus et threads](/ProcThread/processes-and-threads.md).

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a>Membres

La classe de **\_ processus Win32** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ processus Win32** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachDebugger**](attachdebugger-method-in-class-win32-process.md)   | Lance le débogueur actuellement inscrit pour un processus.<br/>                                                                                                                                                                                                                      |
| [**Créer**](create-method-in-class-win32-process.md)                   | Crée un nouveau processus.<br/>                                                                                                                                                                                                                                                         |
| [**GetAvailableVirtualSize**](getavailablevirtualsize-win32-process.md) | Récupère la taille actuelle, en octets, de l’espace d’adressage virtuel libre disponible pour le processus.<br/> **Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 et Windows Vista :** cette méthode n’est pas prise en charge avant Windows 8.1 et Windows Server 2012 R2.<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | Récupère le nom d’utilisateur et le nom de domaine sous lesquels le processus s’exécute.<br/>                                                                                                                                                                                                    |
| [**GetOwnerSid**](getownersid-method-in-class-win32-process.md)         | Récupère l’identificateur de sécurité (SID) pour le propriétaire d’un processus.<br/>                                                                                                                                                                                                            |
| [**SetPriority**](setpriority-method-in-class-win32-process.md)         | Modifie la priorité d’exécution d’un processus.<br/>                                                                                                                                                                                                                                   |
| [**Terminate**](terminate-method-in-class-win32-process.md)             | Met fin à un processus et à tous ses threads.<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propriétés

La classe de **\_ processus Win32** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Description succincte d’un objet : chaîne d’une ligne.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CommandLine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« ligne de commande pour démarrer le processus »)
</dt> </dl>

Ligne de commande utilisée pour démarrer un processus spécifique, le cas échéant.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")
</dt> </dl>

Date à laquelle le processus commence à s’exécuter.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Computer System Class Name ")
</dt> </dl>

Nom de la classe de création du système d’étendue de l’ordinateur.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système de l’ordinateur ")
</dt> </dl>

Nom du système informatique d’étendue.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description d’un objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Tool Help structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("exécutable path")
</dt> </dl>

Chemin d’accès au fichier exécutable du processus.

exemple : « C : \\ Windows \\ système \\Explorer.Exe »

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« état d’exécution »)
</dt> </dl>

État de fonctionnement actuel du processus.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd>

Unknown

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd>

Autre

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Prêt** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqué** (4)


</dt> <dd>

Bloqué

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspendu bloqué** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspendu prêt** (6)


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminé** (7)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (8)


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Développement** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« handle »)
</dt> </dl>

Identificateur de processus.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("handle Count")
</dt> </dl>

Nombre total de handles ouverts détenus par le processus. **HandleCount** est la somme des handles actuellement ouverts par chaque thread dans ce processus. Un descripteur est utilisé pour examiner ou modifier les ressources système. Chaque descripteur a une entrée dans une table qui est gérée en interne. Les entrées contiennent les adresses des ressources et des données pour identifier le type de ressource.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Date d’installation d’un objet. L’objet peut être installé sans qu’une valeur ne soit écrite dans cette propriété.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")
</dt> </dl>

Temps en mode noyau, en millisecondes. Si ces informations ne sont pas disponibles, utilisez la valeur 0 (zéro).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**MaximumWorkingSetSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| winnt. H \| limites de quota \_ \| MaximumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" taille maximale de la plage de travail "), [**unités**](../wmisdk/standard-qualifiers.md) (" kilo-octets ")
</dt> </dl>

Taille maximale du jeu de travail du processus. La plage de travail d’un processus correspond à l’ensemble des pages mémoire visibles par le processus dans la mémoire RAM physique. Ces pages sont résidentes et peuvent être utilisées par une application sans déclencher une erreur de page.

Exemple : 1413120

</dd> <dt>

**MinimumWorkingSetSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| winnt. H \| limites de quota \_ \| MinimumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" taille minimale du jeu de travail "), [**unités**](../wmisdk/standard-qualifiers.md) (" kilo-octets ")
</dt> </dl>

Taille minimale du jeu de travail du processus. La plage de travail d’un processus correspond à l’ensemble des pages mémoire visibles par le processus dans la mémoire RAM physique. Ces pages résident et peuvent être utilisées par une application sans déclencher de défaillance de page.

Exemple : 20480

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Nom du fichier exécutable responsable du processus, équivalent à la propriété nom de l’image dans le gestionnaire des tâches.

Lorsqu’elle est héritée par une sous-classe, la propriété peut être substituée pour être une propriété de clé. Le nom est codé en dur dans l’application elle-même et n’est pas affecté par la modification du nom de fichier. Par exemple, même si vous renommez Calc.exe, le nom Calc.exe apparaîtra toujours dans le gestionnaire des tâches et dans tous les scripts WMI qui récupèrent le nom du processus.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom de la classe du système d’exploitation ")
</dt> </dl>

Nom de la classe de création du système d’exploitation d’étendue.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système d’exploitation ")
</dt> </dl>

Nom du système d’exploitation de portée.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**OtherOperationCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")
</dt> </dl>

Nombre d’opérations d’e/s effectuées qui ne sont pas des opérations de lecture ou d’écriture.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**OtherTransferCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantité de données transférées pendant les opérations qui ne sont pas des opérations de lecture ou d’écriture.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PageFaults**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nombre de défauts de page")
</dt> </dl>

Nombre de défauts de page générés par un processus.

Exemple : 10

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("page file usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilo-octets")
</dt> </dl>

Quantité d’espace de fichier d’échange actuellement utilisée par un processus. Cette valeur est cohérente avec la valeur **VMSize** dans TaskMgr.exe.

Exemple : 102435

</dd> <dt>

**ParentProcessId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api process \| Status \| System \_ process \_ information \| InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("parent Process ID")
</dt> </dl>

Identificateur unique du processus qui crée un processus. Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus. Il est possible que le processus identifié par **ParentProcessId** soit terminé, de sorte que **ParentProcessId** ne peut pas faire référence à un processus en cours d’exécution. Il est également possible que **ParentProcessId** fasse incorrectement référence à un processus qui réutilise un identificateur de processus. Vous pouvez utiliser la propriété **CreationDate** pour déterminer si le parent spécifié a été créé après la création du processus représenté par cette instance de **\_ processus Win32** .

</dd> <dt>

**PeakPageFileUsage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("PIC utilisation du fichier d’échange"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilo-octets")
</dt> </dl>

Quantité maximale d’espace de fichier d’échange utilisée pendant la durée de vie d’un processus.

Exemple : 102367

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("PIC utilisation de l’espace d’adressage virtuelle"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Espace d’adressage virtuel maximal qu’un processus utilise à un moment donné. L’utilisation de l’espace d’adressage virtuel n’implique pas nécessairement l’utilisation correspondante du disque ou des pages de mémoire principales. Toutefois, l’espace virtuel est fini, et en utilisant trop de temps, le processus peut ne pas être en mesure de charger des bibliothèques.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| PeakWorkingSetSize »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Peak Working Set Size »), [**Units**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Taille maximale de la plage de travail d’un processus.

Exemple : 1413120

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (« Priority »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| BasePriority »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Priority »)
</dt> </dl>

Priorité de planification d’un processus dans un système d’exploitation. Plus la valeur est élevée, plus le processus reçoit la priorité la plus élevée. Les valeurs de priorité peuvent être comprises entre 0 (zéro), qui est la priorité la plus faible à 31, qui est la priorité la plus élevée.

Exemple : 7

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private page Count")
</dt> </dl>

Nombre actuel de pages allouées qui sont uniquement accessibles au processus représenté par cette instance de **\_ processus Win32** .

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**process \_ information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process ID")
</dt> </dl>

Identificateur numérique utilisé pour distinguer un processus d’un autre. Les ProcessIDs sont valides à partir de l’heure de création du processus pour traiter l’arrêt. Lors de l’arrêt, ce même identificateur numérique peut être appliqué à un nouveau processus.

Cela signifie que vous ne pouvez pas utiliser ProcessID seul pour surveiller un processus particulier. Par exemple, une application peut avoir un ProcessID de 7, puis échouer. Lors du démarrage d’un nouveau processus, ProcessID 7 peut être affecté au nouveau processus. Un script qui vérifie uniquement un ProcessID spécifié peut donc être « trompeur » pour penser que l’application d’origine était toujours en cours d’exécution.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota d’utilisation de réserve non paginée")
</dt> </dl>

Quota d’utilisation de la réserve non paginée pour un processus.

Exemple : 15

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota d’utilisation de la réserve paginée")
</dt> </dl>

Quota d’utilisation de la réserve paginée pour un processus.

Exemple : 22

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| QuotaPeakNonPagedPoolUsage »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« quota de pic d’utilisation du pool non paginé »)
</dt> </dl>

Quota de pic d’utilisation de la réserve non paginée pour un processus.

Exemple : 31

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| QuotaPeakPagedPoolUsage »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« quota d’utilisation maximale de la réserve paginée »)
</dt> </dl>

Quota de pic d’utilisation de la réserve paginée pour un processus.

Exemple : 31

</dd> <dt>

**ReadOperationCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")
</dt> </dl>

Nombre d’opérations de lecture effectuées.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ReadTransferCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantité de données lues.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| SessionID »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« ID de session »)
</dt> </dl>

Identificateur unique généré par un système d’exploitation lors de la création d’une session. Une session s’étend sur un laps de temps à partir d’une ouverture de session jusqu’à la fermeture d’un système spécifique.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Cette propriété n’est pas implémentée et n’est pas remplie pour une instance de cette classe. La valeur est toujours **null**.

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

</dd> <dt>

**TerminationDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("date d’arrêt")
</dt> </dl>

Le processus a été arrêté ou arrêté. Pour obtenir l’heure de fin, un descripteur du processus doit être maintenu ouvert. Sinon, cette propriété retourne la **valeur null**.

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**ThreadCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nombre de threads")
</dt> </dl>

Nombre de threads actifs dans un processus. Une instruction est l’unité d’exécution de base dans un processeur, et un thread est l’objet qui exécute une instruction. Chaque processus en cours d’exécution possède au moins un thread.

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")
</dt> </dl>

Heure en mode utilisateur, en unités de nanosecondes 100. Si ces informations ne sont pas disponibles, utilisez la valeur 0 (zéro).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("utilisation de l’espace d’adressage virtuel"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Taille actuelle de l’espace d’adressage virtuel utilisé par un processus, et non de la mémoire physique ou virtuelle réellement utilisée par le processus. L’utilisation de l’espace d’adressage virtuel n’implique pas nécessairement l’utilisation correspondante du disque ou des pages de mémoire principales. L’espace virtuel est fini, et en utilisant trop, le processus peut ne pas être en mesure de charger des bibliothèques. Cette valeur est cohérente avec ce que vous voyez dans Perfmon.exe.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread functions \| GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")
</dt> </dl>

Version de Windows dans laquelle le processus est en cours d’exécution.

Exemple : 4,0

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« taille de la plage de travail »), [**unités**](../wmisdk/standard-qualifiers.md) (« octets »)
</dt> </dl>

Quantité de mémoire en octets qu’un processus doit exécuter efficacement : pour un système d’exploitation qui utilise la gestion de la mémoire basée sur les pages. Si le système ne dispose pas de suffisamment de mémoire (inférieure à la taille de la plage de travail), une surcharge se produit. Si la taille de la plage de travail n’est pas connue, utilisez la **valeur null** ou 0 (zéro). Si vous fournissez des données de jeu de travail, vous pouvez surveiller les informations pour comprendre les besoins en mémoire en constante évolution d’un processus.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).

</dd> <dt>

**WriteOperationCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write opération Count")
</dt> </dl>

Nombre d’opérations d’écriture effectuées.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WriteTransferCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantité de données écrites.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe de **\_ processus Win32** est dérivée du [**\_ processus CIM**](cim-process.md). le processus appelant qui utilise cette classe doit avoir le privilège **SE \_ restore \_ NAME** sur l’ordinateur où se trouve le registre. Pour plus d’informations, consultez [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).

### <a name="overview"></a>Vue d’ensemble

Les processus sous-tendent presque tout ce qui se produit sur un ordinateur. En fait, la cause racine de la plupart des problèmes informatiques peut être tracée sur les processus. par exemple, un trop grand nombre de processus peuvent s’exécuter sur un ordinateur (et être en conflit avec un ensemble fini de ressources), ou un processus unique peut utiliser plus que son partage de ressources. Ces facteurs compliquent le suivi des processus en cours d’exécution sur un ordinateur. La surveillance des processus, l’activité principale de la gestion des processus, vous permet de déterminer ce qu’est réellement un ordinateur, les applications que l’ordinateur exécute et la manière dont ces applications sont affectées par les modifications dans l’environnement informatique.

### <a name="monitoring-a-process"></a>Surveillance d’un processus

La surveillance régulière des processus vous permet de vous assurer qu’un ordinateur fonctionne aux pics d’activité et qu’il exécute ses tâches nommées comme prévu. Par exemple, en surveillant les processus, vous pouvez être averti immédiatement de toute application qui ne répond plus, puis prendre les mesures nécessaires pour terminer ce processus. En outre, le processus d’analyse vous permet d’identifier les problèmes avant qu’ils ne se produisent. Par exemple, en vérifiant de manière répétée la quantité de mémoire utilisée par un processus, vous pouvez identifier une fuite de mémoire. Vous pouvez ensuite arrêter le processus avant que l’application errante n’utilise toute la mémoire disponible et met l’ordinateur en arrêt.

La surveillance des processus permet également de réduire les perturbations causées par des interruptions planifiées des mises à niveau et de la maintenance. Par exemple, en vérifiant l’état d’une application de base de données qui s’exécute sur les ordinateurs clients, vous pouvez déterminer l’impact de la mise hors connexion de la base de données afin de mettre à niveau le logiciel.

Surveillance de la disponibilité du processus. Mesure le pourcentage de temps pendant lequel un processus est disponible. La disponibilité est généralement surveillée à l’aide d’une sonde simple, qui indique si le processus est toujours en cours d’exécution. En effectuant le suivi des résultats de chaque sonde, vous pouvez calculer la disponibilité du processus. Par exemple, un processus qui est interrogé 100 fois et qui répond sur 95 de ces occasions a une disponibilité de 95%. Ce type de surveillance est généralement réservé aux bases de données, aux programmes de messagerie et aux autres applications censées s’exécuter à tout moment. Il n’est pas approprié pour les programmes de traitement de texte, les feuilles de calcul ou d’autres applications qui sont régulièrement démarrés et arrêtés plusieurs fois par jour.

Vous pouvez créer une instance de la classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) pour configurer le processus.

Vous pouvez surveiller les performances des processus avec la classe de [**\_ \_ \_ processus perfproc Win32 PerfFormattedData**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) et un objet d’actualisation WMI, tel que [**SWbemRefresher**](../wmisdk/swbemrefresher.md). Pour plus d’informations, consultez [analyse des données de performances](../wmisdk/monitoring-performance-data.md).

## <a name="examples"></a>Exemples

la [liste des propriétés de l’exemple de code PowerShell des Classes WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) dans la galerie TechNet décrit la classe de **\_ processus Win32** et renvoie les résultats au format Excel.

Le [processus de fin d’exécution sur plusieurs serveurs](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) met fin à un processus s’exécutant sur un ou plusieurs ordinateurs.

Dans l' [exemple : appel d’une](../wmisdk/example--calling-a-provider-method.md) rubrique de méthode de fournisseur, le code utilise C++ pour appeler le **\_ processus Win32** afin de créer un processus.

La disponibilité est la forme la plus simple d’analyse de processus : avec cette approche, vous vous assurez simplement que le processus est en cours d’exécution. Lorsque vous surveillez la disponibilité du processus, vous récupérez généralement une liste des processus en cours d’exécution sur un ordinateur, puis vous vérifiez qu’un processus particulier est toujours actif. Si le processus est actif, il est considéré comme disponible. Si le processus n’est pas actif, il n’est pas disponible. L’exemple VBScript suivant surveille la disponibilité des processus en vérifiant la liste des processus en cours d’exécution sur un ordinateur et en émettant une notification si le processus de Database.exe est introuvable.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



L’exemple VBScript suivant surveille la création de processus à l’aide d’un consommateur d’événements temporaire.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



Le VBScript suivant surveille les informations sur les performances du processus.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



L’exemple de code VBScript suivant montre comment obtenir le propriétaire de chaque processus sur un ordinateur local. Vous pouvez utiliser ce script pour obtenir des données à partir d’un ordinateur distant, par exemple, pour déterminer quels utilisateurs ont des processus exécutant Terminal Server, remplacez le nom de l’ordinateur distant par « . » sur la première ligne. Vous devez également être administrateur sur l’ordinateur distant.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



L’exemple de code VBScript suivant montre comment obtenir la session d’ouverture de session associée à un processus en cours d’exécution. Un processus doit être en cours d’exécution Notepad.exe avant le démarrage du script. L’exemple localise les instances de [**\_ LogonSession Win32**](win32-logonsession.md) associées au **\_ processus Win32** qui représente Notepad.exe. [**Win32 \_ SessionProcess**](win32-sessionprocess.md) est spécifié en tant que classe d’association. Pour plus d’informations, consultez [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md)


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
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

[**\_Processus CIM**](cim-process.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[Tâches WMI : processus](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
