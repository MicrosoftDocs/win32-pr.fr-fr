---
description: Représente une collection de systèmes virtuels.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Classe Msvm_VirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393423"
---
# <a name="msvm_virtualsystemcollection-class"></a><span data-ttu-id="284be-103">MSVM \_ VirtualSystemCollection, classe</span><span class="sxs-lookup"><span data-stu-id="284be-103">Msvm\_VirtualSystemCollection class</span></span>

<span data-ttu-id="284be-104">Représente une collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="284be-104">Represents a collection of virtual systems.</span></span>

<span data-ttu-id="284be-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="284be-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="284be-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="284be-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a><span data-ttu-id="284be-107">Membres</span><span class="sxs-lookup"><span data-stu-id="284be-107">Members</span></span>

<span data-ttu-id="284be-108">La classe **MSVM \_ VirtualSystemCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="284be-108">The **Msvm\_VirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="284be-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="284be-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="284be-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="284be-110">Properties</span></span>

<span data-ttu-id="284be-111">La classe **MSVM \_ VirtualSystemCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="284be-111">The **Msvm\_VirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="284be-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="284be-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="284be-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284be-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284be-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« porte »), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="284be-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="284be-116">Identification unique de l’objet de collection.</span><span class="sxs-lookup"><span data-stu-id="284be-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="284be-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="284be-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="284be-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284be-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284be-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="284be-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="284be-121">Nom défini par l’utilisateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="284be-121">An user-defined name for the collection.</span></span> <span data-ttu-id="284be-122">Notez qu’il n’est pas garanti qu’il soit unique.</span><span class="sxs-lookup"><span data-stu-id="284be-122">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="284be-123">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="284be-123">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-124">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284be-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284be-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284be-126">Type de basculement effectué pour la collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="284be-126">Type of failover that was performed for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="284be-127">Ajouté dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="284be-127">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="284be-128">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="284be-128">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="284be-129">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="284be-129">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="284be-130">**Planifié** (2)</span><span class="sxs-lookup"><span data-stu-id="284be-130">**Planned** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="284be-131">**LastApplyConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="284be-131">**LastApplyConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284be-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284be-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284be-134">Niveau de cohérence du dernier Delta appliqué.</span><span class="sxs-lookup"><span data-stu-id="284be-134">Consistency level of the last applied delta.</span></span>

> [!Note]  
> <span data-ttu-id="284be-135">Ajouté dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="284be-135">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="284be-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="284be-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="284be-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Cohérence des applications** (1)</span><span class="sxs-lookup"><span data-stu-id="284be-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="284be-138">Le dernier Delta appliqué indique un point dans le temps où le système virtuel était dans un état de cohérence des applications.</span><span class="sxs-lookup"><span data-stu-id="284be-138">The last applied delta indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="284be-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Cohérence des incidents** (2)</span><span class="sxs-lookup"><span data-stu-id="284be-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="284be-140">Le dernier Delta appliqué indique un point dans le temps où le système virtuel était en état de cohérence en cas d’incident.</span><span class="sxs-lookup"><span data-stu-id="284be-140">The last applied delta indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span data-ttu-id="284be-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Cohérence des pannes de groupe** (3)</span><span class="sxs-lookup"><span data-stu-id="284be-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Group Crash Consistent** (3)</span></span>


</dt> <dd>

<span data-ttu-id="284be-142">Le dernier Delta appliqué indique un point dans le temps où le groupe était dans un état de cohérence en cas d’incident.</span><span class="sxs-lookup"><span data-stu-id="284be-142">The last applied delta indicates a point in time when the group was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="284be-143">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="284be-143">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-144">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="284be-144">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="284be-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284be-146">Heure à laquelle la dernière réplication est appliquée lors de la récupération de la collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="284be-146">The time at which the last replication is applied on recovery for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="284be-147">Ajouté dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="284be-147">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="284be-148">**LastApplyVirtualMachineIds**</span><span class="sxs-lookup"><span data-stu-id="284be-148">**LastApplyVirtualMachineIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-149">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="284be-149">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="284be-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284be-151">Tableau d’ID d’ordinateur virtuel qui ont été correctement appliqués lors du dernier cycle d’application.</span><span class="sxs-lookup"><span data-stu-id="284be-151">Array of Virtual Machine Ids which were successfully applied in last apply cycle.</span></span>

> [!Note]  
> <span data-ttu-id="284be-152">Ajouté dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="284be-152">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="284be-153">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="284be-153">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284be-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284be-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284be-156">Type de réplication pour la collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="284be-156">Replication type for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="284be-157">Ajouté dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="284be-157">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="284be-158">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="284be-158">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="284be-159">**Principal** (1)</span><span class="sxs-lookup"><span data-stu-id="284be-159">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="284be-160">**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="284be-160">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="284be-161">**Réplica de test** (3)</span><span class="sxs-lookup"><span data-stu-id="284be-161">**Test Replica** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="284be-162">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="284be-162">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284be-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284be-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284be-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="284be-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284be-165">État de réplication pour la collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="284be-165">Replication state for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="284be-166">Ajouté dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="284be-166">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="284be-167">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="284be-167">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="284be-168">**Prêt pour la réplication** (1)</span><span class="sxs-lookup"><span data-stu-id="284be-168">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="284be-169">**En attente de l’exécution de la réplication initiale** (2)</span><span class="sxs-lookup"><span data-stu-id="284be-169">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="284be-170">**Réplication** (3)</span><span class="sxs-lookup"><span data-stu-id="284be-170">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

<span data-ttu-id="284be-171">**Basculement initié** (4)</span><span class="sxs-lookup"><span data-stu-id="284be-171">**Failover initiated** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="284be-172">**Récupéré** (5)</span><span class="sxs-lookup"><span data-stu-id="284be-172">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="284be-173">**Validé** (6)</span><span class="sxs-lookup"><span data-stu-id="284be-173">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="284be-174">**Suspendu** (7)</span><span class="sxs-lookup"><span data-stu-id="284be-174">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="284be-175">**Critique** (8)</span><span class="sxs-lookup"><span data-stu-id="284be-175">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="284be-176">**En attente de démarrage de la resynchronisation** (9)</span><span class="sxs-lookup"><span data-stu-id="284be-176">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="284be-177">**Resynchronisation** (10)</span><span class="sxs-lookup"><span data-stu-id="284be-177">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

<span data-ttu-id="284be-178">**Basculement planifié InitiatedRepurpose initiatedTest basculement initiatedPartially activé** (11)</span><span class="sxs-lookup"><span data-stu-id="284be-178">**Planned failover initiatedRepurpose initiatedTest failover initiatedPartially enabled** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

<span data-ttu-id="284be-179">**Partiellement désactivé** (12)</span><span class="sxs-lookup"><span data-stu-id="284be-179">**Partially disabled** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

<span data-ttu-id="284be-180">**Partiellement récupéré** (13)</span><span class="sxs-lookup"><span data-stu-id="284be-180">**Partially recovered** (13)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="284be-181">(14)</span><span class="sxs-lookup"><span data-stu-id="284be-181">(14)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="284be-182">(15)</span><span class="sxs-lookup"><span data-stu-id="284be-182">(15)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="284be-183">(16)</span><span class="sxs-lookup"><span data-stu-id="284be-183">(16)</span></span>


<span data-ttu-id="284be-184"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="284be-184"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="284be-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="284be-185">Requirements</span></span>



| <span data-ttu-id="284be-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="284be-186">Requirement</span></span> | <span data-ttu-id="284be-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="284be-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="284be-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="284be-188">Minimum supported client</span></span><br/> | <span data-ttu-id="284be-189">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="284be-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="284be-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="284be-190">Minimum supported server</span></span><br/> | <span data-ttu-id="284be-191">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="284be-191">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="284be-192">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="284be-192">Namespace</span></span><br/>                | <span data-ttu-id="284be-193">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="284be-193">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="284be-194">MOF</span><span class="sxs-lookup"><span data-stu-id="284be-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="284be-195"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="284be-195"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="284be-196">DLL</span><span class="sxs-lookup"><span data-stu-id="284be-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="284be-197"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="284be-197"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="284be-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="284be-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284be-199">**\_COLLECTIONOFMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="284be-199">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

