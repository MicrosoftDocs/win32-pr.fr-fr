---
description: Représente les paramètres spécifiques à la virtualisation pour un ordinateur virtuel.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Classe Msvm_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950989"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>MSVM \_ VirtualSystemSettingData, classe

Représente les paramètres spécifiques à la virtualisation pour un ordinateur virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemSettingData** possède les propriétés suivantes.

<dl> <dt>

**AdditionalRecoveryInformation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Toutes les informations supplémentaires fournies à l’action de récupération. La signification de cette propriété est définie par l’action dans **AutomaticRecoveryAction**. Si **AutomaticRecoveryAction** a la valeur 0 (« None ») ou 1 (« Restart »), cette valeur est **null**. Si **AutomaticRecoveryAction** a la valeur 2 (« revenir à l’instantané »), il s’agit du chemin d’accès de l’objet à un instantané qui doit être appliqué en cas d’échec du processus de travail de l’ordinateur virtuel.

</dd> <dt>

**AllowFullSCSICommandSet**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**True** si les commandes SCSI du système d’exploitation invité sont transmises aux disques directs ; Sinon, **false**. Si la **valeur est true**, les commandes SCSI émises par le système d’exploitation invité sur des disques directs ne sont pas filtrées. Nous recommandons que le filtrage SCSI reste activé pour les déploiements de production.

</dd> <dt>

**AllowReducedFcRedundancy**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si la migration dynamique d’un ordinateur virtuel qui est configuré avec une carte Fibre Channel virtuelle est autorisée sur un ordinateur de destination qui peut avoir des chemins d’accès non ou réduits aux appareils Fibre Channel cibles. Cette propriété doit être désactivée après une migration dynamique.



| Valeur                                                                            | Signification                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>False</dt> </dl> | L’ordinateur virtuel ne peut pas être migré dynamiquement vers un ordinateur cible qui peut ne pas avoir de chemins d’accès à la cible de Fibre Channel.<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | La machine virtuelle peut être migrée dynamiquement vers un ordinateur cible qui peut ne pas avoir de chemins d’accès réduits aux appareils Fibre Channel cibles. Le système d’exploitation invité peut perdre la connectivité au stockage et peut se comporter de façon imprévisible.<br/> |



 

</dd> <dt>

**Architecture**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Architecture de ce système.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** ()


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** ()


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identifie l’action à entreprendre sur la machine virtuelle, lorsqu’une erreur critique se produit, comme la déconnexion du stockage.

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (0)


</dt> <dd>

Aucune action spécifique n’est effectuée pour les conditions d’erreur critique.

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Suspendre la reprise** (1)


</dt> <dd>

Entraîne la suspension de la machine virtuelle et sa reprise automatique lorsque la condition d’erreur critique est résolue.

</dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorActionTimeout**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« Interval »)
</dt> </dl>

Identifie la durée maximale d’exécution du **AutomaticCriticalErrorAction** pour résoudre l’erreur critique. Cela s’applique uniquement lorsque la valeur de la propriété **AutomaticCriticalErrorAction** n’est pas 0 (aucun). Une fois le délai d’attente expiré, la machine virtuelle est mise hors tension. La valeur est arrondie à la minute la plus proche. La valeur 0 indique que la machine virtuelle doit être mise hors tension immédiatement lorsqu’elle rencontre une condition d’erreur critique.

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour l’ordinateur virtuel lors de l’échec du logiciel exécuté par l’ordinateur virtuel. Dans ce cas, les échecs signifient qu’il s’agit d’une défaillance pouvant être détectée par la plateforme hôte, par exemple une condition d’état d’attente non interruptibles. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                               | Signification                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | Aucun<br/>               |
| <dl> <dt>3</dt> </dl>        | Redémarrer.<br/>            |
| <dl> <dt>4</dt> </dl>        | Revenir à l’instantané.<br/> |
| <dl> <dt>5.. 32768</dt> </dl> | Réservé.<br/>           |



 

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour l’ordinateur virtuel lorsque l’ordinateur hôte est arrêté. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                               | Signification                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | Désactiver.<br/>   |
| <dl> <dt>3</dt> </dl>        | Enregistrer l’État.<br/> |
| <dl> <dt>4</dt> </dl>        | Arrêter.<br/>   |
| <dl> <dt>5.. 32768</dt> </dl> | Réservé.<br/>   |



 

</dd> <dt>

**AutomaticSnapshotsEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si les instantanés automatiques doivent être activés sur cet ordinateur virtuel.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à effectuer pour l’ordinateur virtuel au démarrage de l’ordinateur hôte. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                               | Signification                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | Aucun<br/>                         |
| <dl> <dt>3</dt> </dl>        | Redémarrer si l’activité était déjà active.<br/> |
| <dl> <dt>4</dt> </dl>        | Toujours démarrer.<br/>                 |
| <dl> <dt>5.. 32768</dt> </dl> | Réservé.<br/>                     |



 

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Délai avant le démarrage automatique de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte. Un nombre inférieur indique une activation antérieure. Si une ou plusieurs configurations affichent la même valeur, la séquence dépend de l’implémentation. La valeur 0 indique que la séquence dépend de l’implémentation. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Numéro de série du tableau de base pour la machine virtuelle.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identificateur global unique du BIOS de l’ordinateur virtuel.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**True** si la touche VERR. num est activée (on) par le BIOS ; **False** si la touche VERR. num est désactivée (OFF) par le BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Numéro de série du BIOS de l’ordinateur virtuel.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

L’ordre de démarrage défini dans le BIOS de l’ordinateur virtuel. Cette propriété est un tableau de valeurs, comprise entre **BootOrder** \[ 0 \] et **BootOrder** \[ 3 \] , inclus, où chaque valeur indique un appareil à partir duquel démarrer. Chacune des 4 valeurs du tableau doit être définie et ne doit pas être la même qu’une autre valeur dans le tableau. L’ordinateur virtuel tente d’abord de démarrer à partir de l’appareil indiqué par la première valeur dans le tableau. Si cet appareil ne contient pas de secteur de démarrage, l’ordinateur virtuel tente de démarrer à partir du périphérique suivant spécifié par la propriété **BootOrder** , et ainsi de suite. Si aucun périphérique spécifié dans le **BootOrder** ne contient de secteur de démarrage, l’ordinateur virtuel ne pourra pas démarrer. La valeur par défaut d’un ordinateur virtuel est \[ 0, 1, 2, 3 \] .

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Disquette** (0)


</dt> <dd>

L’ordinateur virtuel tente de démarrer à partir de la disquette dans le lecteur de disquette.

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)


</dt> <dd>

L’ordinateur virtuel tente de démarrer à partir du premier disque CD ou DVD trouvé avec un secteur d’amorçage.

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Disque dur IDE** (2)


</dt> <dd>

L’ordinateur virtuel tente de démarrer à partir du premier lecteur de disque dur trouvé avec un secteur d’amorçage.

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Démarrage PXE** (3)


</dt> <dd>

L’ordinateur virtuel tentera un démarrage PXE à partir du réseau.

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Disque dur SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé** (5.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootSourceOrder**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Ordre de la source de démarrage de la machine virtuelle.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Numéro d’inventaire du châssis de la machine virtuelle.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Numéro de série du châssis de l’ordinateur virtuel.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations relatives à la configuration de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Fichier ConfigurationFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel. Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** . Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique de la configuration de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConsoleMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identifie le mode de console de la machine virtuelle.

> [!Note]  
> Cette propriété a été ajoutée dans Windows 10 et Windows Server 2016.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valeur par défaut** (0)


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

**COM1** (1)


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

**COM2** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création des paramètres de l’ordinateur virtuel. Si cet objet représente les paramètres actuels de l’ordinateur virtuel, cette valeur correspond à l’heure à laquelle le système a été créé. Si cet objet représente les paramètres d’instantané de la machine virtuelle, cette valeur correspond à l’heure à laquelle l’instantané a été pris. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**DebugChannelId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identificateur de canal utilisé pour déboguer l’ordinateur virtuel à l’aide du débogueur unifié.

</dd> <dt>

**DebugPort**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Port TCP/IP utilisé pour déboguer l’ordinateur virtuel à l’aide du débogage synthétique.

</dd> <dt>

**DebugPortEnabled**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si l’ordinateur virtuel utilise le débogage synthétique. Il peut s’agir de l’une des valeurs suivantes.

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>**Activé** (1)


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)


</dt> <dd>

Affecté automatiquement

</dd> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur l’une des valeurs suivantes.



| Valeur                                                                                                                  | Signification                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>« Paramètres actifs pour la machine virtuelle »</dt> </dl>   | Cette instance fait référence à un ordinateur virtuel.<br/> |
| <dl> <dt>« Paramètres d’instantané de la machine virtuelle »</dt> </dl> | Cette instance fait référence à un instantané.<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))et est toujours définie sur le nom complet de l’ordinateur. Ce nom ne doit pas dépasser 100 caractères.

</dd> <dt>

**EnhancedSessionTransportType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique le type de transport à utiliser lors de la connexion à une session étendue.

> [!Note]  
> Cette propriété a été ajoutée dans Windows 10, version 1803.

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**Canal VMBus** (0)


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Socket Hyper-V** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestControlledCacheTypes**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si l’invité peut contrôler les types de cache.

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**GuestStateDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’un répertoire où sont stockées les informations relatives à l’état d’exécution invité.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**GuestStateFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un fichier dans lequel les informations relatives à l’état d’exécution invité sont stockées. Un chemin d’accès relatif ajoute à la valeur de la propriété **GuestStateDataRoot** .

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**HighMmioGapSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

La taille du haut (au-dessus de 4 Go) Memory-Mapped écart d’e/s en Mo

> [!Note]  
> Cette propriété a été ajoutée dans Windows 10, version 1703.

 

</dd> <dt>

**IncrementalBackupEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si l’enregistreur VSS Hyper-V prend en charge les sauvegardes incrémentielles de cet ordinateur virtuel.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**IsAutomaticSnapshot**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique s’il s’agit d’un instantané créé automatiquement pour l’utilisateur.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si la configuration a une référence à un fichier d’état enregistré ; Sinon, **false**. Cela n’indique pas la présence d’un tel fichier, mais uniquement que la configuration en spécifie une.

</dd> <dt>

**LockOnDisconnect**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Verrouiller la console lors de la déconnexion de vmconnect.

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**LowMmioGapSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Configure la taille, en mégaoctets, du premier intervalle MMIO pour un ordinateur virtuel.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

Plage : 128 3584

</dd> <dt>

**NetworkBootPreferredProtocol**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Détermine si le protocole préféré pour le démarrage PXE est IPv4 ou IPv6.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> </dl>

</dd> <dt>

**Remarques**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les notes fournies par l’utilisateur sont liées à la machine virtuelle. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si cette instance ne représente pas un système basé sur un instantané d’un ordinateur virtuel, cette propriété a la **valeur null**. Sinon, la propriété contient le chemin d’accès de l’objet **MSVM \_ VirtualSystemSettingData** sur lequel cette instance est basée. Lors de la création d’une hiérarchie d’arborescence d’instantanés pour l’ordinateur virtuel, cette propriété fait référence à l’objet à partir duquel l’instance actuelle est dérivée (l’instance actuelle est le nœud enfant et l’objet référencé dans cette propriété est le nœud parent).

</dd> <dt>

**ParentPackage**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si ce système est un conteneur, le chemin d’accès au \_ ContainerPackage MSVM à partir duquel ce système est basé.

> [!Note]  
> Ajouté dans Windows 10 ; supprimé dans Windows 10, version 1703.

 

</dd> <dt>

**PauseAfterBootFailure**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le BIOS s’interrompt après chaque échec d’entrée de démarrage en attendant que l’utilisateur appuie sur une touche. **True** si le BIOS s’arrête ; Sinon, **false**.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SecureBootEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le démarrage sécurisé est activé pour la machine virtuelle. **True** si l’option est activée ; Sinon, **false**.

> [!Note]  
> Le démarrage sécurisé ne peut être activé que pour les machines virtuelles de génération 2.

 

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**SecureBootTemplateId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identificateur global unique du modèle de valeurs initiales des variables liées au démarrage sécurisé UEFI.

Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**UserSnapshotType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique le type d’instantané défini par l’utilisateur.

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (2)


</dt> <dd>

Désactivez la création d’un instantané.

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)


</dt> <dd>

Instantané de cohérence des données à utiliser dans l’environnement de production. Effectue un instantané avec l’état de l’application lorsque la possibilité de créer un instantané de cohérence des données n’est pas disponible.

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)


</dt> <dd>

Instantané de cohérence des données à utiliser dans l’environnement de production. Ne crée pas d’instantané avec l’état de l’application s’il n’est pas possible de créer un instantané de cohérence des données.

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)


</dt> <dd>

Instantané qui contient des informations sur la mémoire et l’appareil à des fins de test et de développement.

</dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version de la machine virtuelle dans un format « major. minor », par exemple « 2,0 ».

</dd> <dt>

**VirtualNumaEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**","[**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")
</dt> </dl>

**True** si des nœuds NUMA (non-Uniform Memory Access) virtuels sont projetés dans l’ordinateur virtuel ; **False** si l’ordinateur virtuel a un seul nœud. Si la **valeur est true**, le nombre de nœuds NUMA virtuels projetés dans l’ordinateur virtuel est déterminé à partir des valeurs des propriétés [**MSVM \_ ProcessorSettingData. MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) et [**MSVM MemorySettingData. \_ MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) .

</dd> <dt>

**Attribut virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData. attribut virtualsystemidentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**»)
</dt> </dl>

Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre. Cette propriété est une substitution de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Les valeurs valides pour cette propriété sont Microsoft : Hyper-V : SubType : 1 et Microsoft : Hyper-V : SubType : 2. Une machine virtuelle de génération 1 est SubType 1. Une machine virtuelle de génération 2 est sous-type 2.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft : Hyper-v : sous-type : 1** (« Microsoft : Hyper-v : SubType : 1 »)


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft : Hyper-v : sous-type : 2** (« Microsoft : Hyper-v : SubType : 2 »)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de machine virtuelle que les données de paramètre représentent. Cette propriété est héritée de la classe [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) . Il s’agit de l’une des valeurs suivantes.



| Valeur                                                                                                                                 | Signification                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>« Microsoft : Hyper-V : système : réalisé »</dt> </dl>                        | Un ordinateur virtuel réalisé.<br/>               |
| <dl> <dt>« Microsoft : Hyper-V : système : planifié »</dt> </dl>                         | Un ordinateur virtuel planifié.<br/>                |
| <dl> <dt>« Microsoft : Hyper-V : instantané : réalisé »</dt> </dl>                      | Instantané d’un ordinateur virtuel réalisé.<br/> |
| <dl> <dt>« Microsoft : Hyper-V : capture instantanée : récupération »</dt> </dl>                      | Instantané d’un ordinateur virtuel de récupération.<br/> |
| <dl> <dt>« Microsoft : Hyper-V : instantané : planifié »</dt> </dl>                       | Instantané d’un ordinateur virtuel planifié.<br/>  |
| <dl> <dt>« Microsoft : Hyper-V : instantané : manquant »</dt> </dl>                       | Instantané manquant.<br/>                       |
| <dl> <dt>« Microsoft : Hyper-V : instantané : réplica : standard »</dt> </dl>              | Instantané de point de réplication basé sur l’heure.<br/>  |
| <dl> <dt>« Microsoft : Hyper-V : instantané : réplica : ApplicationConsistent »</dt> </dl> | Instantané de point de réplication VSS.<br/>         |
| <dl> <dt>« Microsoft : Hyper-V : instantané : réplica : PlannedFailover »</dt> </dl>       | Instantané de réplication planifiée.<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ VirtualSystemSettingData** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[Classes du système virtuel](virtual-system-classes.md)
</dt> </dl>

 

