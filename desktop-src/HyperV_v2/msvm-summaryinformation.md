---
description: Utilisé dans les méthodes GetSummaryInformation et GetDefinitionFileSummaryInformation de la \_ classe MSVM VirtualSystemManagementService pour récupérer rapidement les informations communes relatives à un ordinateur virtuel ou à un instantané.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Classe Msvm_SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515882"
---
# <a name="msvm_summaryinformation-class"></a>MSVM \_ SummaryInformation, classe

Utilisé dans les méthodes [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) et [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pour récupérer rapidement les informations communes relatives à un ordinateur virtuel ou à un instantané.

La syntaxe suivante est simplifiée format MOF (MOF).

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SummaryInformation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SummaryInformation** possède les propriétés suivantes.

<dl> <dt>

**AllocatedGPU**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de l’unité de traitement graphique (GPU) physique allouée à cette machine virtuelle. Cette propriété s’applique uniquement aux machines virtuelles qui utilisent RemoteFX.

</dd> <dt>

**ApplicationHealth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État d’intégrité actuel de l’application pour l’ordinateur virtuel. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (2)


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**Critique** pour l’Application (32782)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (32896)


</dt> <dd></dd> </dl>

</dd> <dt>

**AsynchronousTasks**
</dt> <dd> <dl> <dt>

Type de données : tableau **\_ ConcreteJob CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau d’instances [**MSVM \_ ConcreteJob**](msvm-concretejob.md) qui représentent les opérations asynchrones relatives à l’ordinateur virtuel en cours d’exécution. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**AvailableMemoryBuffer**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Pourcentage de mémoire tampon disponible pour la machine virtuelle. Lorsque la mémoire dynamique est activée pour un ordinateur virtuel, cette propriété représente le rapport entre la mémoire tampon disponible et la mémoire tampon idéale pour l’ordinateur virtuel. La taille de mémoire tampon idéale est configurée à l’aide de la propriété **TargetMemoryBuffer** de la classe [**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md) .

Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent des ordinateurs virtuels pour lesquels la mémoire dynamique n’est pas activée.

Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure de création de l’ordinateur virtuel ou de l’instantané.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’ordinateur virtuel ou de l’instantané.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État actuel de l’ordinateur virtuel ou de l’instantané. Pour connaître les valeurs possibles, consultez la propriété **EnabledState** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les connexions en mode étendu sont autorisées par l’hôte et, si elles sont autorisées, si elles sont disponibles pour l’ordinateur virtuel.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Autorisé et disponible** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Non autorisé** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Autorisé mais non disponible** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestOperatingSystem**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du système d’exploitation invité, s’il est disponible. Si ces informations ne sont pas disponibles, la valeur de cette propriété est **null**. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État d’intégrité actuel de la machine virtuelle. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**Pulsation**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État actuel de la pulsation pour la machine virtuelle. Pour plus d’informations, consultez la documentation relative à la propriété [**StatusDescriptions**](msvm-heartbeatcomponent.md) de la classe **\_ HeartbeatComponent MSVM** . Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

<dl> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (6)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (12)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Perte de communication** (13)
</dt> </dl>

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur hébergeant cet ordinateur virtuel.

> [!Note]  
> Ajouté dans Windows 10.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ propriété ManagedElement. InstanceId"), [**clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID est une propriété facultative qui peut être utilisée pour identifier de manière opaque et unique une instance de cette classe dans l’étendue de l’espace de noms d’instanciation. Plusieurs sous-classes de cette classe peuvent substituer cette propriété pour la rendre obligatoire ou une clé. Ces sous-classes peuvent également modifier les algorithmes préférés pour garantir l’unicité définie ci-dessous.

Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant :

<OrgID>:<LocalID>

Où <OrgID> et <LocalID> sont séparés par un signe deux-points ( :), et où <OrgID> doivent inclure un nom protégé par des droits d’auteur, une marque ou un nom unique qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier par une autorité globale reconnue. (Cette spécification est semblable à la <Schema Name> \_ <Class Name> suivante : structure des noms de classes de schéma.) En outre, pour garantir l’unicité, <OrgID> ne doit pas contenir de deux-points ( :). Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre <OrgID> et <LocalID> .

<LocalID> est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels). Si la valeur n’est pas null et que l’algorithme « préféré » ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance.

Si vous ne définissez pas la valeur null pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le <OrgID> défini sur CIM.

> [!Note]  
> Ajouté dans Windows 10.

 

</dd> <dt>

**IntegrationServicesVersionState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les services d’intégration installés sur l’ordinateur virtuel sont à jour.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**Uptodate** (1)


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

**Incompatibilité** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**MemoryAvailable**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Pourcentage de la mémoire actuelle disponible pour l’ordinateur virtuel. Lorsque la mémoire dynamique est activée pour un ordinateur virtuel, cette propriété représente le rapport entre la mémoire disponible de l’ordinateur virtuel et la mémoire physique totale affectée à l’ordinateur virtuel. Lorsqu’un ordinateur virtuel n’a pas de mémoire disponible, cette propriété est négative et contient le ratio de mémoire nécessaire pour l’ordinateur virtuel à la mémoire physique totale affectée à l’ordinateur virtuel.

Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent des ordinateurs virtuels pour lesquels la mémoire dynamique n’est pas activée.

Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**MemorySpansPhysicalNumaNodes**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la mémoire de l’un ou plusieurs des nœuds NUMA (non-Uniform Memory Access) virtuels de l’ordinateur virtuel s’étend sur plusieurs nœuds NUMA physiques du système informatique d’hébergement. Contient la **valeur true** si la mémoire s’étend sur plusieurs nœuds NUMA physiques ou **false** dans le cas contraire.

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Utilisation actuelle de la mémoire, en mégaoctets, de l’ordinateur virtuel. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom unique de l’ordinateur virtuel ou de l’instantané.

</dd> <dt>

**Remarques**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Remarques associées à la machine virtuelle ou à la capture instantanée.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de processeurs virtuels alloués à l’ordinateur virtuel ou à la capture instantanée.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

États opérationnels actuels de la machine virtuelle. Pour connaître les valeurs possibles, consultez la propriété **OperationalStatus** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1. Cette propriété est définie sur **null** quand **EnabledState** a une valeur autre que 1.

</dd> <dt>

**ProcessorLoad**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Utilisation actuelle du processeur de l’ordinateur virtuel, en pourcentage. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**ProcessorLoadHistory**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau des précédents exemples 100 de l’utilisation du processeur, en pourcentage, pour l’ordinateur virtuel. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationHealthEx**")
</dt> </dl>

Intégrité de la réplication pour la machine virtuelle. Pour connaître les valeurs possibles, consultez la propriété **ReplicationHealth** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt **ReplicationHealthEx**.

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicable** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avertissement** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationHealthEx**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau des valeurs d’intégrité de la réplication pour les différentes relations de réplication de l’ordinateur virtuel. Pour connaître les valeurs possibles, consultez la propriété **ReplicationHealth** de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicable** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avertissement** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de réplication pour la machine virtuelle. Pour connaître les valeurs possibles, consultez la propriété **ReplicationMode** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Principal** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Réplica** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Réplica de test** (3)


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**Réplica étendu** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Pour la machine virtuelle de réplication principale ou étendue, il s’agit de l’ID du fournisseur de réplication principal. Pour un ordinateur virtuel de réplication et si la réplication étendue est activée, il s’agit de l’ID de fournisseur pour la relation étendue.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationStateEx**")
</dt> </dl>

État de réplication de la machine virtuelle. Pour connaître les valeurs possibles, consultez la propriété **ReplicationState** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .

> [!Note]  
> Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt **ReplicationStateEx**.

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Prêt pour la réplication** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**En attente de l’exécution de la réplication initiale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Réplication** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Réplication synchronisée terminée** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Récupéré** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Validé** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Suspendu** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**En attente de démarrage de la resynchronisation** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Resynchronisation** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Resynchronisation suspendue** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Basculement en cours** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationStateEx**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau des valeurs d’état de réplication pour les différentes relations de réplication de l’ordinateur virtuel. Pour connaître les valeurs possibles, consultez la propriété **ReplicationState** de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Prêt pour la réplication** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**En attente de l’exécution de la réplication initiale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Réplication** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Réplication synchronisée terminée** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Récupéré** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Validé** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**En attente de démarrage de la resynchronisation** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronisation** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronisation suspendue** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Basculement en cours** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Restauration automatique en cours** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Restauration automatique terminée** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Mise à jour du disque en cours** (15)


</dt> <dd>

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Mise à jour critique du disque** (16)


</dt> <dd>

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (17)


</dt> <dd>

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Réplication réaffectée en cours** (18)


</dt> <dd>

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Préparation pour la réplication de la synchronisation** (19)


</dt> <dd>

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Préparé pour la réplication inverse de groupe** (20)


</dt> <dd>

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill en cours** (21)


</dt> <dd>

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**Protégé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la protection est configurée pour la machine virtuelle.

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

**Instantanés**
</dt> <dd> <dl> <dt>

Type de données : tableau **\_ VirtualSystemSettingData CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau d’instances [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représentent les instantanés de la machine virtuelle. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes. Cela correspond à la propriété **StatusDescriptions** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .

</dd> <dt>

**SwapFilesInUse**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la pagination de second niveau est active. Contient la **valeur true** si la pagination de second niveau est active ou **false** dans le cas contraire.

</dd> <dt>

**TestReplicaSystem**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une [**instance \_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel de réplication de test pour l’ordinateur virtuel. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**ThumbnailImage**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImageWidth**","**MSVM \_ SummaryInformation**.**ThumbnailImageHeight**")
</dt> </dl>

Tableau qui contient une petite image de taille miniature du Bureau de l’ordinateur virtuel ou de l’instantané au format RGB565.

</dd> <dt>

**ThumbnailImageHeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Hauteur, en pixels, de l’image dans la propriété ThumbnailImage.

> [!Note]  
> Ajouté dans Windows 10.

 

</dd> <dt>

**ThumbnailImageWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Largeur en pixels de l’image dans la propriété ThumbnailImage.

> [!Note]  
> Ajouté dans Windows 10.

 

</dd> <dt>

**Activité**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée écoulée depuis le dernier démarrage de la machine virtuelle. Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version du système virtuel dans un format « major. minor », par exemple « 2,0 ».

> [!Note]  
> Ajouté dans Windows 10.

 

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Chaînes qui spécifient les noms conviviaux des commutateurs virtuels auxquels la machine virtuelle est connectée.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Sous-type du système virtuel.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft : Hyper-V : sous-type : 1** ()


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft : Hyper-V : sous-type : 2** ()


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ SummaryInformation** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
</dt> <dt>

[Classes du système virtuel](virtual-system-classes.md)
</dt> </dl>

 

