---
description: Cette classe représente un travail d’opération de migration créé pour le stockage ou la migration du système virtuel par le service de migration de système virtuel.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517617"
---
# <a name="msvm_migrationjob-class"></a>MSVM \_ MigrationJob, classe

Cette classe représente un travail d’opération de migration créé pour le stockage ou la migration du système virtuel par le service de migration de système virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ MigrationJob** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ MigrationJob** possède ces méthodes.



| Méthode                                                             | Description                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetError**](geterror-msvm-migrationjob.md)                     | Récupère l’objet d’erreur pour la tâche de migration, s’il en existe une.<br/>                |
| [**GetErrorEx**](geterrorex-msvm-migrationjob.md)                 | Récupère les objets d’erreur pour la tâche de migration, le cas échéant.<br/>                |
| **KillJob**                                                        | Cette méthode n'est pas prise en charge.<br/>                                                   |
| [**RequestStateChange**](requeststatechange-msvm-migrationjob.md) | Demande que l’état de la tâche de migration passe à l’état spécifié.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ MigrationJob** possède les propriétés suivantes.

<dl> <dt>

**Annulable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le travail peut être annulé. La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le travail doit être automatiquement supprimé à la fin de l’opération. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DestinationHost**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom d’hôte de la plateforme de virtualisation de destination vers laquelle le système virtuel migre. Il s’agit d’une **valeur null** pour la migration du stockage.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps pendant lequel le travail s’est exécuté, ou durée totale d’exécution si le travail est terminé. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Code d’erreur spécifique au fournisseur. La valeur doit être égale à zéro si le travail s’est terminé sans erreur. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui contient la description de l’erreur du fournisseur. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)
</dt> </dl>

Description résumée de l’erreur, le cas échéant.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intégrité actuelle de l’élément. Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants. Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de la configuration de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de fois où la tâche doit être exécutée. La valeur 1 indique que le travail n’est pas récurrent, tandis que toute valeur différente de zéro indique une limite au nombre de fois où le travail se reproduira. La valeur zéro indique qu’il n’y a pas de limite au nombre de fois où le travail peut être traité, mais qu’il se termine une fois que le **UntilTime** a été atteint ou lorsque le travail est arrêté manuellement. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**JobState** est une énumération entière qui indique l’état opérationnel d’un travail. Il peut également indiquer des transitions entre ces États, par exemple « arrêt » et « démarrage ». Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).



| Valeur                                                                                                                                                                                                                                                                 | Signification                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Nouveau**</dt> <dt>2</dt> </dl>                                                           | Le travail n’a jamais été démarré.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> À <dt>**partir**</dt> du <dt>3</dt> </dl>                                       | Le travail passe des États 2 (nouveau), 5 (suspendu) ou 11 (service) à l’État 4 (en cours d’exécution).<br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**En cours d’exécution**</dt> <dt>4</dt> </dl>                                           | La tâche est en cours d'exécution.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt>**Suspendu**</dt> <dt>5</dt> </dl>                                   | La tâche est arrêtée, mais elle peut être redémarrée de manière transparente.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Arrêt**</dt> de <dt>6</dt> </dl>                   | Le travail passe à un État 7 (terminé), 8 (terminé) ou 9 (abattu).<br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Terminé**</dt> le <dt>7</dt> </dl>                                   | Le travail s’est terminé normalement.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Terminé**</dt> <dt>8</dt> </dl>                               | La tâche a été arrêtée par une demande de modification d’État « Terminate ». Le travail et tous ses processus sous-jacents sont terminés et peuvent être redémarrés uniquement en tant que nouveau travail. L’exigence de redémarrage du travail uniquement en tant que nouveau travail est spécifique à un travail.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt>**Abattu**</dt> le <dt>9</dt> </dl>                                               | La tâche a été arrêtée par une demande de modification d’État « Kill ». Les processus sous-jacents peuvent toujours être en cours d’exécution et un nettoyage peut être nécessaire pour libérer des ressources.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Exception**</dt> <dt>10</dt> </dl>                                  | La tâche est dans un état anormal qui peut indiquer une condition d’erreur. L’état réel du travail peut être disponible par le biais d’objets spécifiques à un travail.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Service**</dt> <dt>11</dt> </dl>                                          | La tâche est dans un état spécifique au fournisseur qui prend en charge la découverte de problèmes, la résolution, ou les deux.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF réservé**</dt> <dt>12 32767</dt> </dl>            | Réservé.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Fournisseur réservé**</dt> <dt>32768 65535</dt> </dl> | Réservé.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui représente l’état de la tâche. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le type de travail faisant l’objet d’un suivi par cet objet.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

**Création d’une machine virtuelle distante** (300)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

**Vérification de la compatibilité des machines virtuelles** (301)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

**Vérification de la compatibilité des ordinateurs virtuels et du stockage** (302)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

**Vérification** de la compatibilité du stockage (303)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

**Vérification** de la migration du stockage (304)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

**Déplacement de la machine virtuelle** (305)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

**Déplacement de l’ordinateur virtuel et du stockage** (306)


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

**Déplacement du stockage** (307)


</dt> <dd></dd> </dl>

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

Indique si les heures représentées dans les propriétés **RunStartInterval** et **UntilTime** représentent des heures locales ou des heures UTC.

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Heure locale** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Heure UTC** (2)
</dt> </dl>

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")
</dt> </dl>

Type de migration représenté par cet objet de traitement. Il s’agira de l’une des valeurs définies pour la propriété **MigrationType** de la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

Nom complet de cette instance d’un travail. En outre, le nom complet peut être utilisé en tant que propriété pour une recherche ou une requête. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NewResourceSettingData**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Pour une migration dynamique, elle est toujours définie sur **null**.

Pour une migration de stockage, si la **valeur est null**, aucun disque dur virtuel (VHD) de la machine virtuelle ne sera déplacé. Sinon, elle contient un tableau d’instances incorporées de la classe [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) qui représentent les disques durs virtuels à déplacer. La propriété de **connexion** de ces instances spécifie l’emplacement de destination du disque dur virtuel.

</dd> <dt>

**NewSystemSettingData**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Pour une migration dynamique, elle est toujours définie sur **null**.

Pour une migration de stockage, si la **valeur est null**, les racines de données de l’ordinateur virtuel ne sont pas déplacées. Sinon, elle contient une instance incorporée de la [**classe MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) , où les propriétés **ExternalDataRoot**, **SnapshotDataRoot** et **SwapFileDataRoot** spécifient les nouvelles racines de données.

</dd> <dt>

**Notifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Utilisateur qui est averti en cas d’achèvement ou d’échec d’un travail. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** . Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’action de récupération lorsque la propriété **RecoveryAction** de l’instance a la valeur 1 (autre). Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Propriétaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Utilisateur qui a envoyé le travail. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MinValue** (0), **MaxValue** (100), **unités** (« percent »)
</dt> </dl>

Pourcentage d’achèvement du travail. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Importance de l’exécution d’un travail. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décrit l’action de récupération à entreprendre pour un travail qui n’a pas réussi à s’exécuter. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Ne pas continuer** (2)
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuer avec la tâche suivante** (3)
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Travail de réexécution** (4)
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Exécuter la tâche de récupération** (5)
</dt> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MinValue** (-31), **MaxValue** (31)
</dt> </dl>

Jour du mois sur lequel le travail doit être traité. Il existe différentes interprétations pour cette propriété, en fonction de la valeur de **RunDayOfWeek**.

Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est positif, **RunDay** définit le jour du mois où le travail est traité. Par exemple, si **RunDayOfWeek** est égal à 0 et que **RunDay** est égal à 12, la tâche est traitée le 12 <sup>ème</sup> jour du mois.

Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est négatif, **RunDay** définit le nombre de jours avant le dernier jour du mois où le travail est traité.  1 indique le dernier jour du mois, 2 indique un jour avant le dernier jour du mois, et ainsi de suite. Par exemple, si **RunDayOfWeek** est égal à 0 et **RunDay** la valeur 1, la tâche est traitée le dernier jour du mois.

Quand **RunDayOfWeek** n’est pas égal à 0, **RunDayOfWeek** est le jour de la semaine où le travail sera traité, par rapport à **RunDay**. Par exemple, si **RunDay** est 15 et **RunDayOfWeek** est 7 (+ samedi), le travail sera traité le premier samedi, le ou après le 15 <sup>ème</sup> jour du mois. Si **RunDay** est 20 et **RunDayOfWeek** est 7 (samedi), la tâche est traitée le premier samedi le ou avant le 20 <sup>ème</sup> jour du mois. Si **RunDay** est 1 et que **RunDayOfWeek** est 1 (dimanche), la tâche est traitée le dernier dimanche du mois.

Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Entier positif ou négatif utilisé conjointement avec **RunDay** pour indiquer le jour de la semaine ou du mois où le travail est traité. Pour plus d’informations, consultez la description de la propriété **RunDay** . Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samedi** (7)
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Vendredi** (6)
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jeudi** (5)
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercredi** (4)
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Mardi** (3)
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lundi** (2)
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Dimanche** (1)
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)
</dt> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Dimanche** (1)
</dt> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lundi** (2)
</dt> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Mardi** (3)
</dt> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercredi** (4)
</dt> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jeudi** (5)
</dt> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Vendredi** (6)
</dt> <dt>

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samedi** (7)
</dt> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Mois pendant lequel le travail doit être traité. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janvier** (0)
</dt> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Février** (1)
</dt> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>**Mars** (2)
</dt> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>**Avril** (3)
</dt> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)
</dt> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juin** (5)
</dt> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>**Juillet** (6)
</dt> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Août** (7)
</dt> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septembre** (8)
</dt> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octobre** (9)
</dt> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)
</dt> <dt>

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Décembre** (11)
</dt> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps après minuit lorsque le travail doit être traité. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure de début planifiée pour le travail, le cas échéant. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure de début de la tâche. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** . Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en minutes, pendant laquelle le travail est conservé une fois qu’il a fini de s’exécuter, soit à l’issue ou à l’échec de cette exécution. Le travail doit rester en présence pendant un certain temps, quelle que soit la valeur de la propriété **DeleteOnCompletion** . La valeur par défaut est cinq minutes. Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85))et est toujours définie sur 00000000000500.000000:000.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date ou heure de la dernière modification de l’état du travail. Si l’état de la tâche n’a pas changé et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0. Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour. Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail a été soumis. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail n’est pas valide ou doit être arrêté. Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom unique du système virtuel affecté.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

