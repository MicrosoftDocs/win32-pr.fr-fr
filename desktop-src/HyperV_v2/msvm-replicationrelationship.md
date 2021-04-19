---
description: Représente l’état de la réplication pour une relation de réplication.
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Classe Msvm_ReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationRelationship
- Msvm_ReplicationRelationship.InstanceID
- Msvm_ReplicationRelationship.ReplicationState
- Msvm_ReplicationRelationship.ReplicationHealth
- Msvm_ReplicationRelationship.FailedOverReplicationType
- Msvm_ReplicationRelationship.LastReplicationType
- Msvm_ReplicationRelationship.LastApplicationConsistentReplicationTime
- Msvm_ReplicationRelationship.LastReplicationTime
- Msvm_ReplicationRelationship.LastApplyTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04665f96f4ec77501ee0b161d816c84943ca2c98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517880"
---
# <a name="msvm_replicationrelationship-class"></a><span data-ttu-id="be18f-103">MSVM \_ ReplicationRelationship, classe</span><span class="sxs-lookup"><span data-stu-id="be18f-103">Msvm\_ReplicationRelationship class</span></span>

<span data-ttu-id="be18f-104">Représente l’état de la réplication pour une relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-104">Represents replication status for a replication relationship.</span></span> <span data-ttu-id="be18f-105">Étant donné que vous pouvez avoir plusieurs réplications pour chaque ordinateur virtuel de réplication, vous pouvez utiliser cette classe pour identifier chaque relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-105">Because you can have multiple replications for each replica virtual machine, you can use this class to identify each replication relationship.</span></span>

<span data-ttu-id="be18f-106">La syntaxe suivante est simplifiée à partir du code MOF et comprend les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="be18f-106">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be18f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be18f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationRelationship : CIM_ManagedSystemElement
{
  string   InstanceID;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  datetime LastApplicationConsistentReplicationTime;
  datetime LastReplicationTime;
  datetime LastApplyTime;
};
```

## <a name="members"></a><span data-ttu-id="be18f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="be18f-108">Members</span></span>

<span data-ttu-id="be18f-109">La classe **MSVM \_ ReplicationRelationship** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be18f-109">The **Msvm\_ReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="be18f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be18f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be18f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be18f-111">Properties</span></span>

<span data-ttu-id="be18f-112">La classe **MSVM \_ ReplicationRelationship** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="be18f-112">The **Msvm\_ReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be18f-113">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="be18f-113">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be18f-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be18f-116">Type de basculement effectué pour la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-116">The type of failover that was performed for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="be18f-117">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="be18f-117">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="be18f-118">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="be18f-118">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="be18f-119">**Cohérence des applications** (2)</span><span class="sxs-lookup"><span data-stu-id="be18f-119">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="be18f-120">**Planifiée** (3)</span><span class="sxs-lookup"><span data-stu-id="be18f-120">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be18f-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="be18f-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be18f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be18f-124">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="be18f-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="be18f-125">Identifie la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-125">Identifies replication relationship.</span></span> <span data-ttu-id="be18f-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be18f-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="be18f-127">Cette propriété a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="be18f-127">This property has this format:</span></span>

<span data-ttu-id="be18f-128">**Microsoft : <vmid> \\ HVR \\<0/1>**</span><span class="sxs-lookup"><span data-stu-id="be18f-128">**Microsoft:<vmid>\\HVR\\<0/1>**</span></span>

<span data-ttu-id="be18f-129">0 indique principal et 1 indique [la réplication étendue](#extended-replication).</span><span class="sxs-lookup"><span data-stu-id="be18f-129">0 indicates primary and 1 indicates [extended replication](#extended-replication).</span></span>

</dd> <dt>

<span data-ttu-id="be18f-130">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="be18f-130">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-131">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be18f-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be18f-133">Date et heure de réception de la dernière réplication cohérente d’application lors de la récupération de la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-133">The date and time at which the last application consistent replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="be18f-134">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="be18f-134">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-135">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be18f-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be18f-137">Date et heure auxquelles la dernière réplication est appliquée lors de la récupération de la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-137">The date and time at which the last replication is applied on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="be18f-138">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="be18f-138">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-139">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be18f-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be18f-141">Date et heure de réception de la dernière réplication lors de la récupération de la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-141">The date and time at which the last replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="be18f-142">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="be18f-142">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be18f-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be18f-145">Type de la dernière réplication qui a été reçue pour la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-145">The type of the last replication that was received for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="be18f-146">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="be18f-146">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="be18f-147">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="be18f-147">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="be18f-148">**Cohérence des applications** (2)</span><span class="sxs-lookup"><span data-stu-id="be18f-148">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="be18f-149">**Planifiée** (3)</span><span class="sxs-lookup"><span data-stu-id="be18f-149">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be18f-150">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="be18f-150">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be18f-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be18f-153">Intégrité de la réplication pour la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-153">Replication health for the replication relationship.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="be18f-154">**Non applicable** (0)</span><span class="sxs-lookup"><span data-stu-id="be18f-154">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="be18f-155">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="be18f-155">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="be18f-156">**Avertissement** (2)</span><span class="sxs-lookup"><span data-stu-id="be18f-156">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="be18f-157">**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="be18f-157">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be18f-158">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="be18f-158">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be18f-159">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be18f-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be18f-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be18f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be18f-161">État de réplication pour la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="be18f-161">Replication state for the replication relationship.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="be18f-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="be18f-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="be18f-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Prêt pour la réplication** (1)</span><span class="sxs-lookup"><span data-stu-id="be18f-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="be18f-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**En attente de l’exécution de la réplication initiale** (2)</span><span class="sxs-lookup"><span data-stu-id="be18f-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="be18f-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Réplication** (3)</span><span class="sxs-lookup"><span data-stu-id="be18f-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="be18f-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Réplication synchronisée terminée** (4)</span><span class="sxs-lookup"><span data-stu-id="be18f-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="be18f-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Récupéré** (5)</span><span class="sxs-lookup"><span data-stu-id="be18f-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="be18f-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Validé** (6)</span><span class="sxs-lookup"><span data-stu-id="be18f-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="be18f-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (7)</span><span class="sxs-lookup"><span data-stu-id="be18f-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="be18f-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (8)</span><span class="sxs-lookup"><span data-stu-id="be18f-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="be18f-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**En attente de démarrage de la resynchronisation** (9)</span><span class="sxs-lookup"><span data-stu-id="be18f-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="be18f-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronisation** (10)</span><span class="sxs-lookup"><span data-stu-id="be18f-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="be18f-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronisation suspendue** (11)</span><span class="sxs-lookup"><span data-stu-id="be18f-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="be18f-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Basculement en cours** (12)</span><span class="sxs-lookup"><span data-stu-id="be18f-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="be18f-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Restauration automatique en cours** (13)</span><span class="sxs-lookup"><span data-stu-id="be18f-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="be18f-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Restauration automatique terminée** (14)</span><span class="sxs-lookup"><span data-stu-id="be18f-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="be18f-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Mise à jour du disque en cours** (15)</span><span class="sxs-lookup"><span data-stu-id="be18f-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="be18f-178">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="be18f-178">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="be18f-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Mise à jour critique du disque** (16)</span><span class="sxs-lookup"><span data-stu-id="be18f-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="be18f-180">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="be18f-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="be18f-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (17)</span><span class="sxs-lookup"><span data-stu-id="be18f-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="be18f-182">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="be18f-182">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="be18f-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Réplication réaffectée en cours** (18)</span><span class="sxs-lookup"><span data-stu-id="be18f-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="be18f-184">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="be18f-184">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="be18f-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Préparation pour la réplication de la synchronisation** (19)</span><span class="sxs-lookup"><span data-stu-id="be18f-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="be18f-186">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="be18f-186">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="be18f-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Préparé pour la réplication inverse de groupe** (20)</span><span class="sxs-lookup"><span data-stu-id="be18f-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="be18f-188">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="be18f-188">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="be18f-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill en cours** (21)</span><span class="sxs-lookup"><span data-stu-id="be18f-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="be18f-190">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="be18f-190">This property was added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be18f-191">Notes</span><span class="sxs-lookup"><span data-stu-id="be18f-191">Remarks</span></span>

### <a name="extended-replication"></a><span data-ttu-id="be18f-192">Réplication étendue</span><span class="sxs-lookup"><span data-stu-id="be18f-192">Extended replication</span></span>

<span data-ttu-id="be18f-193">La fonctionnalité de réplication Hyper-V dans Windows 8 permet aux machines virtuelles qui s’exécutent sur un serveur Hyper-V du site principal d’être répliquées efficacement sur un autre serveur Hyper-V sur le site secondaire.</span><span class="sxs-lookup"><span data-stu-id="be18f-193">The Hyper-V replication feature in Windows 8 allows virtual machines that run on a Hyper-V server at the primary site to be efficiently replicated to another Hyper-V server at the secondary site.</span></span>

<span data-ttu-id="be18f-194">La fonctionnalité de réplication Hyper-V dans Windows 8.1 permet à un utilisateur d’étendre la relation de réplication du site secondaire vers un troisième site.</span><span class="sxs-lookup"><span data-stu-id="be18f-194">The Hyper-V replication feature in Windows 8.1 enables a user to extend the replication relationship from the secondary site onwards to a third site.</span></span> <span data-ttu-id="be18f-195">Le troisième site peut être un hôte Hyper-V préconfiguré en tant que serveur de récupération ou fournisseur de réplication externe.</span><span class="sxs-lookup"><span data-stu-id="be18f-195">The third site can be a Hyper-V host pre-provisioned as a recovery server or external replication provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="be18f-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be18f-196">Requirements</span></span>



| <span data-ttu-id="be18f-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be18f-197">Requirement</span></span> | <span data-ttu-id="be18f-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="be18f-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be18f-199">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be18f-199">Minimum supported client</span></span><br/> | <span data-ttu-id="be18f-200">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be18f-200">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="be18f-201">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be18f-201">Minimum supported server</span></span><br/> | <span data-ttu-id="be18f-202">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be18f-202">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be18f-203">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be18f-203">Namespace</span></span><br/>                | <span data-ttu-id="be18f-204">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="be18f-204">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="be18f-205">MOF</span><span class="sxs-lookup"><span data-stu-id="be18f-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be18f-206"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be18f-206"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be18f-207">DLL</span><span class="sxs-lookup"><span data-stu-id="be18f-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be18f-208"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be18f-208"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be18f-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be18f-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be18f-210">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="be18f-210">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="be18f-211">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="be18f-211">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

