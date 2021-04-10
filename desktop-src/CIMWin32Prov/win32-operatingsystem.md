---
description: Représente un système d’exploitation Windows installé sur un ordinateur.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201108"
---
# <a name="win32_operatingsystem-class"></a>\_Classe Win32 OperatingSystem

La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ OperatingSystem** représente un système d’exploitation Windows installé sur un ordinateur.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ OperatingSystem** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ OperatingSystem** possède ces méthodes.



| Méthode                                                                                     | Description                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reboot**](reboot-method-in-class-win32-operatingsystem.md)                             | Arrête puis redémarre le système informatique.<br/>                                                                                                                                                                                                           |
| [**SetDateTime**](setdatetime-method-in-class-win32-operatingsystem.md)                   | Autorise la définition de la date et de l’heure de l’ordinateur.<br/>                                                                                                                                                                                                                |
| [**Correct**](shutdown-method-in-class-win32-operatingsystem.md)                         | Décharge les programmes et les dll jusqu’au point où il est possible de mettre hors tension l’ordinateur en toute sécurité.<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | Fournit l’ensemble complet d’options d’arrêt prises en charge par les systèmes d’exploitation Windows.<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | Fournit le même ensemble d’options d’arrêt prises en charge par la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) dans **Win32 \_ OperatingSystem**, mais vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ OperatingSystem** possède ces propriétés.

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| lecteur \_ Map \_ info \| btInt13Unit »)
</dt> </dl>

Nom du lecteur de disque à partir duquel le système d’exploitation Windows démarre.

Exemple : « \\ \\ Harddisk0 d’appareil \\ »

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")
</dt> </dl>

Numéro de build d’un système d’exploitation. Il peut être utilisé pour obtenir des informations de version plus précises que les numéros de version de produit.

Exemple : « 1381 »

</dd> <dt>

**BuildType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType")
</dt> </dl>

Type de build utilisé pour un système d’exploitation.

Exemples : « version commerciale », « version contrôlée »»

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description de l’objet : chaîne d’une ligne. La chaîne comprend la version du système d’exploitation. Par exemple, « Microsoft Windows 7 entreprise ». Cette propriété peut être localisée.

**Windows Vista et Windows 7 :** Cette propriété peut contenir des caractères de fin. Par exemple, la chaîne « Microsoft Windows 7 entreprise » (espace de fin inclus) peut être nécessaire pour récupérer des informations à l’aide de cette propriété.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Codes**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| fonctions de prise en charge linguistique nationale \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ IDEFAULTANSICODEPAGE")
</dt> </dl>

Valeur de page de codes utilisée par un système d’exploitation. Une page de codes contient une table de caractères qu’un système d’exploitation utilise pour traduire des chaînes pour différentes langues. Le American National Standards Institute (ANSI) répertorie les valeurs qui représentent des pages de codes définies. Si un système d’exploitation n’utilise pas de page de codes ANSI, ce membre a la valeur 0 (zéro). La **chaîne du** Codeet peut utiliser six caractères au maximum pour définir la valeur de la page de codes.

Exemple : « 1255 »

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ ICOUNTRY")
</dt> </dl>

Code du pays ou de la région utilisé par un système d’exploitation. Les valeurs sont basées sur des préfixes de numérotation téléphonique internationaux, également appelées codes pays/région IBM. Cette propriété peut utiliser six caractères au maximum pour définir la valeur du code de pays/région.

Exemple : « 1 » (États-Unis)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété permet d’identifier toutes les instances de cette classe et de ses sous-classes de manière unique.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nom de la classe de création du système d’étendue de l’ordinateur.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")
</dt> </dl>

Chaîne terminée par le caractère **null** qui indique la dernière Service Pack installée sur un ordinateur. Si aucun Service Pack n’est installé, la chaîne est **null**.

Exemple : « Service Pack 3 »

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nom du système informatique d’étendue.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Type de données : **sint16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« minutes »)
</dt> </dl>

Nombre, en minutes, un système d’exploitation est décalé par rapport à l’heure GMT (Greenwich Mean Time). Le nombre est positif, négatif ou égal à zéro.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**DataExecutionPrevention \_ 32BitApplications**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Lorsque la fonctionnalité matérielle de prévention de l’exécution des données est disponible, cette propriété indique que la fonctionnalité est configurée pour fonctionner pour les applications 32 bits si la **valeur est true**. Sur les ordinateurs 64 bits, la fonctionnalité de prévention de l’exécution des données est configurée dans le magasin [données de configuration de démarrage (BCD) (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) et les propriétés dans **Win32 \_ OperatingSystem** sont définies en conséquence.

</dd> <dt>

**DataExecutionPrevention \_ disponibles**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

La prévention de l’exécution des données est une fonctionnalité matérielle permettant d’empêcher les attaques par dépassement de mémoire tampon en arrêtant l’exécution du code sur les pages de mémoire de type de données. Si la **valeur est true**, cette fonctionnalité est disponible. Sur les ordinateurs 64 bits, la fonctionnalité de prévention de l’exécution des données est configurée dans le magasin BCD et les propriétés dans **Win32 \_ OperatingSystem** sont définies en conséquence.

</dd> <dt>

**\_Pilotes DataExecutionPrevention**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Lorsque la fonctionnalité matérielle de prévention de l’exécution des données est disponible, cette propriété indique que la fonctionnalité est configurée pour fonctionner pour les pilotes si la **valeur est true**. Sur les ordinateurs 64 bits, la fonctionnalité de prévention de l’exécution des données est configurée dans le magasin BCD et les propriétés dans **Win32 \_ OperatingSystem** sont définies en conséquence.

</dd> <dt>

**DataExecutionPrevention \_ SupportPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Indique quel paramètre de prévention de l’exécution des données (DEP) est appliqué. Le paramètre DEP spécifie dans quelle mesure DEP s’applique aux applications 32 bits sur le système. DEP est toujours appliqué au noyau Windows.

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Toujours désactivé** (0)


</dt> <dd>

DEP est désactivé pour toutes les applications 32 bits sur l’ordinateur sans exceptions. Ce paramètre n’est pas disponible pour l’interface utilisateur.

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)


</dt> <dd>

DEP est activé pour toutes les applications 32 bits sur l’ordinateur. Ce paramètre n’est pas disponible pour l’interface utilisateur.

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Accepter** (2)


</dt> <dd>

DEP est activé pour un nombre limité de fichiers binaires, le noyau et tous les services Windows. Toutefois, elle est désactivée par défaut pour toutes les applications 32 bits. Un utilisateur ou un administrateur doit choisir explicitement le **Always on** ou le paramètre d' **annulation** avant que DEP puisse être appliqué aux applications 32 bits.

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Refuser** (3)


</dt> <dd>

DEP est activé par défaut pour toutes les applications 32 bits. Un utilisateur ou un administrateur peut supprimer explicitement la prise en charge d’une application 32 bits en ajoutant l’application à une liste d’exceptions.

</dd> </dl>

</dd> <dt>

**Déboguer**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ debug")
</dt> </dl>

Le système d’exploitation est une version (débogage) vérifiée. Si la **valeur est true**, la version de débogage est installée. Les builds vérifiées permettent de vérifier les erreurs, la vérification des arguments et le code de débogage du système. Du code supplémentaire dans un fichier binaire vérifié génère un message d’erreur du débogueur du noyau et s’arrête dans le débogueur. Cela permet de déterminer immédiatement la cause et l’emplacement de l’erreur. Les performances peuvent être affectées dans une build vérifiée en raison du code supplémentaire qui est exécuté.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Description du système d’exploitation Windows. Certaines interfaces utilisateur, par exemple, celles qui autorisent la modification de cette description, limitent sa longueur à 48 caractères.

</dd> <dt>

**Graphique**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le système d’exploitation est distribué sur plusieurs nœuds système de l’ordinateur. Dans ce cas, ces nœuds doivent être regroupés en tant que cluster.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Niveau de chiffrement pour les transactions sécurisées : 40 bits, 128 bits ou *n*-bit.

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

**40 bits** (0)


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

**128** bits (1)


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

**n** bits (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ForegroundApplicationBoost**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

Une augmentation de la priorité est accordée à l’application de premier plan. L’amélioration de l’application est implémentée en donnant à une application plus de tranches de temps d’exécution (longueurs de Quantum).

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (0)


</dt> <dd>

Le système augmente la longueur de quantum de 6.

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)


</dt> <dd>

Le système augmente la longueur de quantum de 12.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)


</dt> <dd>

Le système augmente la longueur de quantum de 18.

</dd> </dl>

</dd> <dt>

**FreePhysicalMemory**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Nombre, en kilo-octets, de la mémoire physique actuellement inutilisée et disponible.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**FreeSpaceInPagingFiles**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Paramètres de mémoire système DMTF \| 001,4»), [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Nombre, en kilo-octets, qui peut être mappé dans les fichiers de pagination du système d’exploitation sans entraîner le remplacement de toutes les autres pages.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**FreeVirtualMemory**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Nombre, en kilo-octets, de la mémoire virtuelle actuellement inutilisée et disponible.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

L’objet date a été installé. Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LargeSystemCache**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Cette propriété est obsolète et n’est pas prise en charge.

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimiser pour les applications** (0)


</dt> <dd>

Optimiser la mémoire pour les applications.

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimiser pour les performances du système** (1)


</dt> <dd>

Optimiser la mémoire pour les performances du système.

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure du dernier redémarrage du système d’exploitation.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**LocalDateTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrSystemDate "," MIF. \|Informations générales sur DMTF \| 001,6»)
</dt> </dl>

Version du système d’exploitation de la date et de l’heure locales.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Paramètres régionaux**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ ILANGUAGE")
</dt> </dl>

Identificateur de langue utilisé par le système d’exploitation. Un identificateur de langue est une abréviation numérique internationale standard pour un pays ou une région. Chaque langue possède un identificateur de langue unique (LANGID), une valeur de 16 bits qui se compose d’un identificateur de langue primaire et d’un identificateur de langue secondaire.

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Nom du fabricant du système d’exploitation. Pour les systèmes Windows, cette valeur est « Microsoft Corporation ».

</dd> <dt>

**MaxNumberOfProcesses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemMaxProcesses ")
</dt> </dl>

Nombre maximal de contextes de processus que le système d’exploitation peut prendre en charge. La valeur par défaut définie par le fournisseur est 4294967295 (0xFFFFFFFF). S’il n’y a pas de valeur maximale fixe, la valeur doit être 0 (zéro). Sur les systèmes qui ont un maximum fixe, cet objet peut aider à diagnostiquer les défaillances qui se produisent lorsque la valeur maximale est atteinte. si elle est inconnue, entrez 4294967295 (0xFFFFFFFF).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**MaxProcessMemorySize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Nombre maximal, en kilo-octets, de la mémoire qui peut être allouée à un processus. Pour les systèmes d’exploitation sans mémoire virtuelle, cette valeur est généralement égale à la quantité totale de mémoire physique moins la mémoire utilisée par le BIOS et le système d’exploitation. Pour certains systèmes d’exploitation, cette valeur peut être l’infini, auquel cas 0 (zéro) doit être entré. Dans d’autres cas, cette valeur peut être une constante, par exemple 2G ou 4G.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**MUILanguages**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Langues du pack d’interface utilisateur multilingue (MUI Pack) installées sur l’ordinateur. Par exemple, « en-US ». Les langues du Pack MUI sont des fichiers de ressources qui peuvent être installés sur la version anglaise du système d’exploitation. Quand un pack MUI est installé, vous pouvez modifier la langue de l’interface utilisateur en 33 langues prises en charge.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Instance du système d’exploitation au sein d’un système informatique.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfLicensedUsers**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de licences utilisateur pour le système d’exploitation. Si la valeur est Unlimited, entrez 0 (zéro). S’il est inconnu, entrez-1.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfProcesses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemProcesses ")
</dt> </dl>

Nombre de contextes de processus actuellement chargés ou en cours d’exécution sur le système d’exploitation.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Numdatabases**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemNumUsers ")
</dt> </dl>

Nombre de sessions utilisateur pour lesquelles le système d’exploitation stocke actuellement des informations d’État.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**OperatingSystemSKU**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Numéro SKU (Stock Keeping Unit) du système d’exploitation. Ces valeurs sont les mêmes que les constantes **Product \_ \** _ définies dans Winnt. h, qui sont utilisées avec la fonction [_ *GetProductInfo* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .

La liste suivante répertorie les valeurs SKU possibles.

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Produit \_ NON défini** (0)


</dt> <dd>

Indéfini

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Produit \_ ÉDITION INTÉGRALe** (1)


</dt> <dd>

Édition intégrale, par exemple, Windows Vista Édition intégrale.

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Produit \_ Édition \_ familial** (2)


</dt> <dd>

Édition familial basique

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Produit \_ Édition familiale \_ Premium** (3)


</dt> <dd>

Édition familiale Premium

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Produit \_ ENTREPRISE** (4)


</dt> <dd>

Édition Entreprise

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Produit \_ ENTREPRISE** (6)


</dt> <dd>

Professionnel

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Produit \_ \_Serveur standard** (7)


</dt> <dd>

Windows Server Standard Edition (installation de l’expérience utilisateur)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Produit \_ \_Serveur de centre de centres** (8)


</dt> <dd>

Windows Server Datacenter Edition (installation de l’expérience utilisateur)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Produit \_ \_Serveur SMALLBUSINESS** (9)


</dt> <dd>

Édition Small Business Server

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Produit \_ \_Serveur d’entreprise** (10)


</dt> <dd>

Édition Enterprise Server

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Produit \_ STARTER** (11)


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Produit \_ DATACENTER \_ Server \_ Core** (12)


</dt> <dd>

Édition Core de Datacenter Server

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Produit \_ STANDARD \_ Server \_ Core** (13)


</dt> <dd>

Édition Standard Server Core

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Produit \_ ENTERPRISE \_ Server \_ Core** (14)


</dt> <dd>

Enterprise Server Core Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Produit \_ \_Serveur Web** (17)


</dt> <dd>

Édition Web Server

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Produit \_ \_Serveur d’hébergement** (19)


</dt> <dd>

Édition de serveur principal

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Produit \_ STORAGE \_ Express \_ Server** (20)


</dt> <dd>

Storage Express Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Produit \_ \_ \_ Serveur de stockage standard** (21)


</dt> <dd>

Windows Storage Server Standard Edition (installation de l’expérience utilisateur)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Produit \_ STORAGE \_ Workgroup \_ Server** (22)


</dt> <dd>

Windows Storage Server Workgroup Edition (installation de l’expérience utilisateur)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Produit \_ STORAGE \_ Enterprise \_ Server** (23)


</dt> <dd>

Stockage Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Produit \_ SERVEUR \_ pour \_ SMALLBUSINESS** (24)


</dt> <dd>

Server pour Small Business Edition

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Produit \_ SMALLBUSINESS \_ Server \_ Premium** (25)


</dt> <dd>

Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Produit \_ ENTREPRISE \_ N** (27)


</dt> <dd>

Windows édition entreprise

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Produit \_ ULTIMATE \_ N** (28)


</dt> <dd>

Édition Windows édition intégrale

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Produit \_ WEB \_ Server \_ Core** (29)


</dt> <dd>

Windows Server Web Edition (installation minimale)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Produit \_ \_Serveur standard \_ V** (36)


</dt> <dd>

Windows Server Standard Edition sans Hyper-V

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Produit \_ DATACENTER \_ Server \_ V** (37)


</dt> <dd>

Windows Server Datacenter Edition sans Hyper-V (installation complète)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Produit \_ Serveur d’entreprise \_ \_ V** (38)


</dt> <dd>

Windows Server Enterprise Edition sans Hyper-V (installation complète)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Produit \_ DATACENTER \_ Server \_ Core \_ V** (39)


</dt> <dd>

Windows Server Datacenter Edition sans Hyper-V (installation Server Core)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Produit \_ STANDARD \_ Server \_ Core \_ V** (40)


</dt> <dd>

Windows Server Standard Edition sans Hyper-V (installation Server Core)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Produit \_ ENTERPRISE \_ Server \_ Core \_ V** (41)


</dt> <dd>

Windows Server entreprise Edition sans Hyper-V (installation Server Core)

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Produit \_ HYPERV** (42)


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Produit \_ STORAGE \_ Express \_ Server \_ Core** (43)


</dt> <dd>

Storage Server Express Edition (installation minimale)

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Produit \_ \_Core Storage standard \_ Server \_ Core** (44)


</dt> <dd>

Storage Server Standard Edition (installation minimale)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Produit \_ STORAGE \_ Workgroup \_ Server \_ Core** (45)


</dt> <dd>

Storage Server Workgroup Edition (installation minimale)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Produit \_ STOCKAGE \_ Enterprise \_ Server \_ Core** (46)


</dt> <dd>

Storage Server Workgroup Edition (installation minimale)

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Produit \_ PROFESSIONNEL** (48)


</dt> <dd>

Windows professionnel

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Produit \_ \_ \_ Serveur de solutions SB** (50)


</dt> <dd>

Windows Server Essentials (installation de l’expérience utilisateur)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Produit \_ SMALLBUSINESS \_ Server \_ Premium \_ Core** (63)


</dt> <dd>

Small Business Server Premium (installation minimale)

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Produit \_ Serveur de CLUSTER \_ \_ V** (64)


</dt> <dd>

Windows Compute Cluster Server sans Hyper-V

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Produit \_ \_ARM Core** (97)


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**Produit \_ CORE** (101)


</dt> <dd>

Page d’hébergement Windows

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Produit \_ \_WMC professionnel** (103)


</dt> <dd>

Windows professionnel avec Media Center

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Produit \_ MOBILE \_ Core** (104)


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Produit \_ IOTUAP** (123)


</dt> <dd>

Noyau Windows IoT (Internet des objets)

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Produit \_ Serveur de centre de \_ \_ serveurs de NANO** (143)


</dt> <dd>

Windows Server Datacenter Edition (installation nano Server)

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Produit \_ \_Nano \_ Server STANDARD** (144)


</dt> <dd>

Windows Server Standard Edition (installation nano Server)

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Produit \_ DATACENTER \_ WS \_ Server \_ Core** (147)


</dt> <dd>

Windows Server Datacenter Edition (installation minimale)

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Produit \_ STANDARD \_ WS \_ Server \_ Core** (148)


</dt> <dd>

Windows Server Standard Edition (installation minimale)

</dd> </dl>

</dd> <dt>

**Organisation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")
</dt> </dl>

Nom de la société pour l’utilisateur inscrit du système d’exploitation.

Exemple : « Microsoft Corporation »

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Architecture du système d’exploitation, par opposition au processeur. Cette propriété peut être localisée.

Exemple : 32-bit

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| par défaut \\ \\ du panneau de configuration \\ \\ \| paramètres régionaux")
</dt> </dl>

Version linguistique du système d’exploitation installé. La liste suivante répertorie les valeurs possibles. Exemple : 0x0807 (allemand, Suisse).

<dt>

1 (0x1)
</dt> <dd>

Arabe

</dd> <dt>

4 (0x4)
</dt> <dd>

Chinois (simplifié) – Chine

</dd> <dt>

9 (0x9)
</dt> <dd>

Anglais

</dd> <dt>

1025 (0x401)
</dt> <dd>

Arabe – Arabie saoudite

</dd> <dt>

1026 (0x402)
</dt> <dd>

Bulgare

</dd> <dt>

1027 (0x403)
</dt> <dd>

Catalan

</dd> <dt>

1028 (0x404)
</dt> <dd>

Chinois (traditionnel) – Taïwan

</dd> <dt>

1029 (0x405)
</dt> <dd>

Tchèque

</dd> <dt>

1030 (0x406)
</dt> <dd>

Danois

</dd> <dt>

1031 (0x407)
</dt> <dd>

Allemand – Allemagne

</dd> <dt>

1032 (0x408)
</dt> <dd>

Grec

</dd> <dt>

1033 (0x40C)
</dt> <dd>

Anglais – États-Unis

</dd> <dt>

1034 (0x40A)
</dt> <dd>

Espagnol – tri traditionnel

</dd> <dt>

1035 (0x40B)
</dt> <dd>

Finnois

</dd> <dt>

1036 (0x40C)
</dt> <dd>

Français – France

</dd> <dt>

1037 (0x40D)
</dt> <dd>

Hébreu

</dd> <dt>

1038 (0x40E)
</dt> <dd>

Hongrois

</dd> <dt>

1039 (0x40F)
</dt> <dd>

Islandais

</dd> <dt>

1040 (0x410)
</dt> <dd>

Italien – Italie

</dd> <dt>

1041 (0x411)
</dt> <dd>

Japonais

</dd> <dt>

1042 (0x412)
</dt> <dd>

Coréen

</dd> <dt>

1043 (0x413)
</dt> <dd>

Néerlandais – Pays-Bas

</dd> <dt>

1044 (0x414)
</dt> <dd>

Norvégien – bokmal

</dd> <dt>

1045 (0x415)
</dt> <dd>

Polonais

</dd> <dt>

1046 (0x416)
</dt> <dd>

Portugais – Brésil

</dd> <dt>

1047 (0x417)
</dt> <dd>

Rhaeto-Romanic

</dd> <dt>

1048 (0x418)
</dt> <dd>

Roumain

</dd> <dt>

1049 (0x419)
</dt> <dd>

Russe

</dd> <dt>

1050 (0x41A)
</dt> <dd>

Croate

</dd> <dt>

1051 (0x41B)
</dt> <dd>

Slovaque

</dd> <dt>

1052 (0x41C)
</dt> <dd>

Albanais

</dd> <dt>

1053 (0x41D)
</dt> <dd>

Suédois

</dd> <dt>

1054 (0x41E)
</dt> <dd>

Thaï

</dd> <dt>

1055 (0x41F)
</dt> <dd>

Turc

</dd> <dt>

1056 (0x420)
</dt> <dd>

Ourdou

</dd> <dt>

1057 (0x421)
</dt> <dd>

Indonésien

</dd> <dt>

1058 (0x422)
</dt> <dd>

Ukrainien

</dd> <dt>

1059 (0x423)
</dt> <dd>

Biélorusse

</dd> <dt>

1060 (0x424)
</dt> <dd>

Slovène

</dd> <dt>

1061 (0x425)
</dt> <dd>

Estonien

</dd> <dt>

1062 (0x426)
</dt> <dd>

Letton

</dd> <dt>

1063 (0x427)
</dt> <dd>

Lituanien

</dd> <dt>

1065 (0x429)
</dt> <dd>

Persan

</dd> <dt>

1066 (0x42A)
</dt> <dd>

Vietnamien

</dd> <dt>

1069 (0x42D)
</dt> <dd>

Basque (Basque)

</dd> <dt>

1070 (0x42E)
</dt> <dd>

Serbe

</dd> <dt>

1071 (0x42F)
</dt> <dd>

Macédonien (Macédoine du Nord)

</dd> <dt>

1072 (0x430)
</dt> <dd>

Sutu

</dd> <dt>

1073 (0x431)
</dt> <dd>

Tsonga

</dd> <dt>

1074 (0x432)
</dt> <dd>

Tswana

</dd> <dt>

1076 (0x434)
</dt> <dd>

Xhosa

</dd> <dt>

1077 (0x435)
</dt> <dd>

Zoulou

</dd> <dt>

1078 (0x436)
</dt> <dd>

Afrikaans

</dd> <dt>

1080 (0x438)
</dt> <dd>

Féroïen

</dd> <dt>

1081 (0x439)
</dt> <dd>

Hindi

</dd> <dt>

1082 (0x43A)
</dt> <dd>

Maltais

</dd> <dt>

1084 (0x43C)
</dt> <dd>

Gaélique écossais (Royaume-Uni)

</dd> <dt>

1085 (0x43D)
</dt> <dd>

Yiddish

</dd> <dt>

1086 (0x43E)
</dt> <dd>

Malais – Malaisie

</dd> <dt>

2049 (0x801)
</dt> <dd>

Arabe – Irak

</dd> <dt>

2052 (0x804)
</dt> <dd>

Chinois (simplifié) – RPC

</dd> <dt>

2055 (0x807)
</dt> <dd>

Allemand – Suisse

</dd> <dt>

2057 (0x809)
</dt> <dd>

Anglais – Royaume-Uni

</dd> <dt>

2058 (0x80A)
</dt> <dd>

Espagnol – Mexique

</dd> <dt>

2060 (0x80C)
</dt> <dd>

Français – Belgique

</dd> <dt>

2064 (0x810)
</dt> <dd>

Italien – Suisse

</dd> <dt>

2067 (0x813)
</dt> <dd>

Néerlandais – Belgique

</dd> <dt>

2068 (0x814)
</dt> <dd>

Norvégien – nynorsk

</dd> <dt>

2070 (0x816)
</dt> <dd>

Portugais – Portugal

</dd> <dt>

2072 (0x818)
</dt> <dd>

Roumain – Moldavie

</dd> <dt>

2073 (0x819)
</dt> <dd>

Russe – Moldavie

</dd> <dt>

2074 (0x81A)
</dt> <dd>

Serbe – latin

</dd> <dt>

2077 (0x81D)
</dt> <dd>

Suédois – Finlande

</dd> <dt>

3073 (0xC01)
</dt> <dd>

Arabe – Égypte

</dd> <dt>

3076 (0xC04)
</dt> <dd>

Chinois (traditionnel) – Hong Kong (R.A.S.)

</dd> <dt>

3079 (0xC07)
</dt> <dd>

Allemand – Autriche

</dd> <dt>

3081 (0xC09)
</dt> <dd>

Anglais – Australie

</dd> <dt>

3082 (0xC0A)
</dt> <dd>

Espagnol – international

</dd> <dt>

3084 (0xC0C)
</dt> <dd>

Français – Canada

</dd> <dt>

3098 (0xC1A)
</dt> <dd>

Serbe – cyrillique

</dd> <dt>

4097 (0x1001)
</dt> <dd>

Arabe – Libye

</dd> <dt>

4100 (0x1004)
</dt> <dd>

Chinois (simplifié) – Singapour

</dd> <dt>

4103 (0x1007)
</dt> <dd>

Allemand – Luxembourg

</dd> <dt>

4105 (0x1009)
</dt> <dd>

Anglais – Canada

</dd> <dt>

4106 (0x100A)
</dt> <dd>

Espagnol – Guatemala

</dd> <dt>

4108 (0x100C)
</dt> <dd>

Français-Suisse

</dd> <dt>

5121 (0x1401)
</dt> <dd>

Arabe – Algérie

</dd> <dt>

5127 (0x1407)
</dt> <dd>

Allemand – Liechtenstein

</dd> <dt>

5129 (0x1409)
</dt> <dd>

Anglais-Nouvelle-Zélande

</dd> <dt>

5130 (0x140A)
</dt> <dd>

Espagnol – Costa Rica

</dd> <dt>

5132 (0x140C)
</dt> <dd>

Français – Luxembourg

</dd> <dt>

6145 (0x1801)
</dt> <dd>

Arabe – Maroc

</dd> <dt>

6153 (0x1809)
</dt> <dd>

Anglais – Irlande

</dd> <dt>

6154 (0x180A)
</dt> <dd>

Espagnol – Panama

</dd> <dt>

7169 (0x1C01)
</dt> <dd>

Arabe – Tunisie

</dd> <dt>

7177 (0x1C09)
</dt> <dd>

Anglais – Afrique du Sud

</dd> <dt>

7178 (0x1C0A)
</dt> <dd>

Espagnol – République dominicaine

</dd> <dt>

8193 (0x2001)
</dt> <dd>

Arabe – Oman

</dd> <dt>

8201 (0x2009)
</dt> <dd>

Anglais – Jamaïque

</dd> <dt>

8202 (0x200A)
</dt> <dd>

Espagnol – Venezuela

</dd> <dt>

9217 (0x2401)
</dt> <dd>

Arabe – Yémen

</dd> <dt>

9226 (0x240A)
</dt> <dd>

Espagnol – Colombie

</dd> <dt>

10241 (0x2801)
</dt> <dd>

Arabe – Syrie

</dd> <dt>

10249 (0x2809)
</dt> <dd>

Anglais – Belize

</dd> <dt>

10250 (0x280A)
</dt> <dd>

Espagnol – Pérou

</dd> <dt>

11265 (0x2C01)
</dt> <dd>

Arabe – Jordanie

</dd> <dt>

11273 (0x2C09)
</dt> <dd>

Anglais – Trinidad

</dd> <dt>

11274 (0x2C0A)
</dt> <dd>

Espagnol – Argentine

</dd> <dt>

12289 (0x3001)
</dt> <dd>

Arabe – Liban

</dd> <dt>

12298 (0x300A)
</dt> <dd>

Espagnol – Équateur

</dd> <dt>

13313 (0x3401)
</dt> <dd>

Arabe – Koweït

</dd> <dt>

13322 (0x340A)
</dt> <dd>

Espagnol – Chili

</dd> <dt>

14337 (0x3801)
</dt> <dd>

Arabe – E.A.U.

</dd> <dt>

14346 (0x380A)
</dt> <dd>

Espagnol – Uruguay

</dd> <dt>

15361 (0x3C01)
</dt> <dd>

Arabe – Bahreïn

</dd> <dt>

15370 (0x3C0A)
</dt> <dd>

Espagnol – Paraguay

</dd> <dt>

16385 (0x4001)
</dt> <dd>

Arabe – Qatar

</dd> <dt>

16394 (0x400A)
</dt> <dd>

Espagnol – Bolivie

</dd> <dt>

17418 (0x440A)
</dt> <dd>

Espagnol – El Salvador

</dd> <dt>

18442 (0x480A)
</dt> <dd>

Espagnol – Honduras

</dd> <dt>

19466 (0x4C0A)
</dt> <dd>

Espagnol – Nicaragua

</dd> <dt>

20490 (0x500A)
</dt> <dd>

Espagnol – Porto Rico

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ ProductOptions \| ProductSuite »), [**bitvalues**](../wmisdk/standard-qualifiers.md) (« Small Business », « Enterprise », « BackOffice », « communication Server », « Terminal Server », « Small Business (Restricted) », « Embedded NT », « Data Center »)
</dt> </dl>

Des compléments de produits système installés et sous licence au système d’exploitation. Par exemple, la valeur de 146 (0x92) pour **OSProductSuite** indique Enterprise, Terminal Services et Data Center (bits 1, quatre et sept Set). La liste suivante répertorie les valeurs possibles.

<dt>

1 (0x1)
</dt> <dd>

Microsoft Small Business Server a été installé, mais il a peut-être été mis à niveau vers une autre version de Windows.

</dd> <dt>

2 (0X2)
</dt> <dd>

Windows Server 2008 Enterprise est installé.

</dd> <dt>

4 (0x4)
</dt> <dd>

Les composants Windows BackOffice sont installés.

</dd> <dt>

8 (0x8)
</dt> <dd>

Communication Server est installé.

</dd> <dt>

16 (0x10)
</dt> <dd>

Les services Terminal Server sont installés.

</dd> <dt>

32 (0x20)
</dt> <dd>

Microsoft Small Business Server est installé avec la licence client restrictive.

</dd> <dt>

64 (0x40)
</dt> <dd>

Windows Embedded est installé.

</dd> <dt>

128 (0x80)
</dt> <dd>

Une édition Datacenter est installée.

</dd> <dt>

256 (0x100)
</dt> <dd>

Les services Terminal Server sont installés, mais une seule session interactive est prise en charge.

</dd> <dt>

512 (0x200)
</dt> <dd>

Windows Édition personnelle est installé.

</dd> <dt>

1024 (0x400)
</dt> <dd>

L’édition Web Server est installée.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

L’édition Storage Server est installée.

</dd> <dt>

16384 (0x4000)
</dt> <dd>

Compute Cluster Edition est installé.

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")
</dt> </dl>

Type de système d'exploitation. La liste suivante identifie les valeurs possibles.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MacOS** (2)


</dt> <dd>

MACROS

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span id="AIX"></span><span id="aix"></span>**Aix** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span id="MVS"></span><span id="mvs"></span>**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span id="OS400"></span><span id="os400"></span>**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**Win95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**Win98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WinCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span id="OSF"></span><span id="osf"></span>**OSF** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span id="IRIX"></span><span id="irix"></span>**IRIX** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)


</dt> <dd>

Solaris

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**Linux** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (61)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (62)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Description supplémentaire pour la version actuelle du système d’exploitation.

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**PAEEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, les extensions d’adresse physique (PAE) sont activées par le système d’exploitation qui s’exécute sur les processeurs Intel. PAE permet aux applications d’adresser plus de 4 Go de mémoire physique. Lorsque PAE est activé, le système d’exploitation utilise la traduction d’adresses linéaires à trois niveaux plutôt que deux niveaux. Le fait de fournir plus de mémoire physique à une application réduit la nécessité d’échanger la mémoire dans le fichier d’échange et d’augmenter les performances. Pour activer, PAE, utilisez le commutateur « /PAE » dans le fichier Boot.ini. Pour plus d’informations sur la fonctionnalité d’extension d’adresse physique, consultez <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .

</dd> <dt>

**PlusProductID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion plus \| ! ProductId»)
</dt> </dl>

Non pris en charge.

</dd> <dt>

**PlusVersionNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion plus \| ! VersionNumber»)
</dt> </dl>

Non pris en charge.

</dd> <dt>

**PortableOperatingSystem**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le système d’exploitation est démarré à partir d’un périphérique USB externe. Si la valeur est true, le système d’exploitation a détecté qu’il démarre sur un dispositif de stockage connecté localement et pris en charge.

**Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 8 et Windows Server 2012.

</dd> <dt>

**Primaire**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Spécifie s’il s’agit du système d’exploitation principal.

</dd> <dt>

**ProductType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations système supplémentaires.

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**Poste de travail** (1)


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**Contrôleur de domaine** (2)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Serveur** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumLength**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

Non pris en charge

* * Windows Server 2008 et Windows Vista : * *

La propriété **QuantumLength** définit le nombre de battements d’horloge par Quantum. Un Quantum est une unité de durée d’exécution que le planificateur est autorisé à fournir à une application avant de basculer vers d’autres applications. Lorsqu’un thread exécute un Quantum, le noyau le prépasse et le déplace à la fin d’une file d’attente pour les applications avec des priorités identiques. La longueur réelle du quantum d’un thread varie selon les plateformes Windows. Pour Windows NT/Windows 2000 uniquement.

Les valeurs possibles sont.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

**Un battement** (1)


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

**Deux graduations** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non pris en charge

* * Windows Server 2008 et Windows Vista : * *

La propriété **QuantumType** spécifie des quantums de longueur fixe ou variable. Windows utilise par défaut des quantums de longueur variable, où l’application de premier plan a un Quantum plus long que les applications en arrière-plan. Windows Server passe par défaut à des quantums de longueur fixe. Un Quantum est une unité de durée d’exécution que le planificateur est autorisé à fournir à une application avant de passer à une autre application. Lorsqu’un thread exécute un Quantum, le noyau le prépasse et le déplace à la fin d’une file d’attente pour les applications avec des priorités identiques. La longueur réelle du quantum d’un thread varie selon les plateformes Windows.

Les valeurs possibles sont.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Fixe** (1)


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**Variable** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Inscrit**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")
</dt> </dl>

Nom de l’utilisateur inscrit du système d’exploitation.

Exemple : « Ben Smith »

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")
</dt> </dl>

Numéro d’identification de série du produit de système d’exploitation.

Exemple : « 10497-OEM-0031416-71674 »

</dd> <dt>

**ServicePackMajorVersion**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")
</dt> </dl>

Numéro de version principale du Service Pack installé sur le système informatique. Si aucun Service Pack n’a été installé, la valeur est 0 (zéro).

</dd> <dt>

**ServicePackMinorVersion**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")
</dt> </dl>

Numéro de version mineure du Service Pack installé sur le système informatique. Si aucun Service Pack n’a été installé, la valeur est 0 (zéro).

</dd> <dt>

**SizeStoredInPagingFiles**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Paramètres de mémoire système DMTF \| 001,3»), [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Nombre total de kilo-octets pouvant être stockés dans les fichiers de pagination du système d’exploitation : 0 (zéro) indique qu’il n’y a aucun fichier de pagination. N’oubliez pas que ce nombre ne représente pas la taille physique réelle du fichier d’échange sur le disque.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent peut fonctionner correctement, mais prédit une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». L’état du service s’applique aux tâches administratives, telles que la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

**SuiteMask**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), deux- [**TValue**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition», « Windows Server, BackOffice Edition », « Windows Server, Communications Edition », « Microsoft Terminal Services », « Windows Server, Small Business Edition Restricted », « Windows Embedded », « Windows Server, Datacenter Edition », « Single User », « Windows Édition personnelle », « Windows Server, Web Edition »)
</dt> </dl>

Indicateurs de bits qui identifient les suites de produits disponibles sur le système.

Par exemple, pour spécifier Personal et BackOffice, définissez **SuiteMask** sur `4 | 512` ou `516` .

<dt>

1
</dt> <dd>

Small Business

</dd> <dt>

2
</dt> <dd>

Enterprise

</dd> <dt>

4
</dt> <dd>

BackOffice

</dd> <dt>

8
</dt> <dd>

Communications

</dd> <dt>

16
</dt> <dd>

Terminal Services

</dd> <dt>

32
</dt> <dd>

Restreint aux petites entreprises

</dd> <dt>

64
</dt> <dd>

Édition intégrée

</dd> <dt>

128
</dt> <dd>

Édition Datacenter

</dd> <dt>

256
</dt> <dd>

Utilisateur unique

</dd> <dt>

512
</dt> <dd>

Édition personnelle

</dd> <dt>

1 024
</dt> <dd>

Édition Web Server

</dd> </dl>

</dd> <dt>

**SystemDevice**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Registry Functions \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| paths \| appareil cible »)
</dt> </dl>

Partition de disque physique sur laquelle le système d’exploitation est installé.

</dd> <dt>

**SystemDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions d’informations système [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))
</dt> </dl>

Répertoire système du système d’exploitation.

Exemple : « C : \\ Windows \\ system32 »

</dd> <dt>

**%SystemDrive%**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Lettre du lecteur de disque sur lequel réside le système d’exploitation. Exemple : "C :"

</dd> <dt>

**TotalSwapSpaceSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Espace d’échange total en kilo-octets. Cette valeur peut être **null** (non spécifié) si l’espace d’échange n’est pas distingué des fichiers d’échange. Toutefois, certains systèmes d’exploitation distinguent ces concepts. Par exemple, dans UNIX, les processus entiers peuvent être échangés lorsque la liste de pages libre tombe et reste sous un montant spécifié.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**TotalVirtualMemorySize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Nombre, en kilo-octets, de la mémoire virtuelle. Par exemple, cela peut être calculé en ajoutant la quantité de mémoire RAM totale à la quantité d’espace de pagination, c’est-à-dire en ajoutant la quantité de mémoire dans ou agrégée par le système informatique à la propriété, **SizeStoredInPagingFiles**.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**TotalVisibleMemorySize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Quantité totale, en kilo-octets, de la mémoire physique disponible pour le système d’exploitation. Cette valeur n’indique pas nécessairement la véritable quantité de mémoire physique, mais ce qui est signalé au système d’exploitation comme disponible.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")
</dt> </dl>

Numéro de version du système d’exploitation.

Exemple : « 4,0 »

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| System Information Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)»)
</dt> </dl>

Répertoire Windows du système d’exploitation.

Exemple : « C : \\ Windows »

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ OperatingSystem** est dérivée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

Tout système d’exploitation qui peut être installé sur un ordinateur qui peut exécuter un système d’exploitation Windows est un descendant ou un membre de cette classe. **Win32 \_ OperatingSystem** est une classe singleton. Pour obtenir l’instance unique, utilisez « @ » pour la clé.

Contrairement à la plupart des autres classes WMI générées par MgmtClassGen, la méthode **OperatingSystem. CreateInstance**() renverra un objet **OperatingSystem** vide. Par conséquent, si vous utilisez C \# avec MgmtClassGen, vous pouvez utiliser le code suivant :


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>Exemples

Vous trouverez un exemple VBScript qui obtient les données du système d’exploitation et du processeur à partir de [**Win32 \_ ComputerSystem**](win32-computersystem.md), du [**\_ processeur Win32**](win32-processor.md)et de **Win32 \_ OperatingSystem** dans les exemples de sujets relatifs au [**\_ processeur Win32**](win32-processor.md) .

L’exemple de [génération de rapports d’environnement Exchange à l’aide](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) de PowerShell PowerShell sur la Galerie TechNet utilise une classe **Win32 \_ OperatingSystem** dans le cadre d’une application plus volumineuse pour générer des rapports d’environnement Exchange.

L’exemple [obtenir le temps d’activité du serveur à l’aide de WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) dans la Galerie TechNet utilise la propriété **LastBootupTime** pour déterminer la durée pendant laquelle le serveur a été actif. L’exemple utilise également l’option timeout pour s’assurer que l’appel WMI ne se bloque pas.

L’exemple de code VBScript de l' [extracteur d’informations WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) sur la Galerie TechNet utilise la classe **Win32 \_ OperatingSystem** pour récupérer des informations de système d’exploitation à partir d’un certain nombre d’ordinateurs distants.

Le script suivant obtient les instances de **Win32 \_ OperatingSystem** dans l’espace de noms « root \\ cimv2 » par défaut, puis affiche des informations sur le système d’exploitation.


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



L’exemple de code PowerShell suivant affiche toutes les informations d’exploitation relatives au système d’exploitation actuel.


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
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

[**\_OPERATINGSYSTEM CIM**](cim-operatingsystem.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[Tâches WMI : systèmes d’exploitation](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[Tâches WMI : matériel de l’ordinateur](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[Tâches WMI : gestion des postes de travail](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
