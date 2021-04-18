---
description: Fournit des statistiques de réplication pour un ordinateur virtuel.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Classe Msvm_ReplicationStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519997"
---
# <a name="msvm_replicationstatistics-class"></a><span data-ttu-id="42c58-103">MSVM \_ ReplicationStatistics, classe</span><span class="sxs-lookup"><span data-stu-id="42c58-103">Msvm\_ReplicationStatistics class</span></span>

<span data-ttu-id="42c58-104">Fournit des statistiques de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="42c58-104">Provides replication statistics for a virtual machine.</span></span> <span data-ttu-id="42c58-105">Ces statistiques couvrent la durée spécifiée par les propriétés **MonitoringStartTime** et **MonitoringInterval** de la [**classe \_ ReplicationServiceSettingData MSVM**](msvm-replicationservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="42c58-105">These statistics cover the duration specified by the **MonitoringStartTime** and **MonitoringInterval** properties of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class.</span></span>

<span data-ttu-id="42c58-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="42c58-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c58-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42c58-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a><span data-ttu-id="42c58-108">Membres</span><span class="sxs-lookup"><span data-stu-id="42c58-108">Members</span></span>

<span data-ttu-id="42c58-109">La classe **MSVM \_ ReplicationStatistics** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="42c58-109">The **Msvm\_ReplicationStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="42c58-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="42c58-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42c58-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="42c58-111">Properties</span></span>

<span data-ttu-id="42c58-112">La classe **MSVM \_ ReplicationStatistics** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="42c58-112">The **Msvm\_ReplicationStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42c58-113">**ApplicationConsistentSnapshotFailureCount**</span><span class="sxs-lookup"><span data-stu-id="42c58-113">**ApplicationConsistentSnapshotFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-116">Nombre total d’échecs d’instantanés VSS.</span><span class="sxs-lookup"><span data-stu-id="42c58-116">The total number of VSS snapshot failures.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="42c58-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="42c58-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-120">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="42c58-120">A short description of the object.</span></span> <span data-ttu-id="42c58-121">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="42c58-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="42c58-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="42c58-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-125">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="42c58-125">A description of the object.</span></span> <span data-ttu-id="42c58-126">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="42c58-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="42c58-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="42c58-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-130">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="42c58-130">A display name for the object.</span></span> <span data-ttu-id="42c58-131">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="42c58-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-132">**EndStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="42c58-132">**EndStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-133">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42c58-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-135">Heure, en UTC, à laquelle le service de réplication Hyper-V a arrêté la collecte des données des statistiques de réplication.</span><span class="sxs-lookup"><span data-stu-id="42c58-135">The time, in UTC, when the Hyper-V Replica service stopped gathering replication statistics data.</span></span> <span data-ttu-id="42c58-136">À ce stade, un nouveau cycle des statistiques de réplication démarre.</span><span class="sxs-lookup"><span data-stu-id="42c58-136">At this time, a new replication statistics cycle starts.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="42c58-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="42c58-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42c58-140">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="42c58-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="42c58-141">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="42c58-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="42c58-142">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="42c58-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-143">**LastTestFailoverTime**</span><span class="sxs-lookup"><span data-stu-id="42c58-143">**LastTestFailoverTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-144">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42c58-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-146">Indique la dernière fois qu’un système de réplication de test a été créé pour un ordinateur virtuel de réplication activé sur le serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="42c58-146">Indicates the last time a test replica system was created for a replication enabled virtual machine on the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-147">**MaxReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="42c58-147">**MaxReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-150">Durée maximale d’exécution d’un cycle de réplication unique, en secondes.</span><span class="sxs-lookup"><span data-stu-id="42c58-150">The maximum amount of time taken to complete a single replication cycle, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-151">**MaxReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="42c58-151">**MaxReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-152">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42c58-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-154">Nombre maximal de données de réplication transférées au système hôte de récupération, en octets.</span><span class="sxs-lookup"><span data-stu-id="42c58-154">Maximum replication data transferred to the recovery host system, in bytes.</span></span> <span data-ttu-id="42c58-155">Il s’agit de la taille maximale des données de réplication envoyées sur un cycle unique pour cet intervalle.</span><span class="sxs-lookup"><span data-stu-id="42c58-155">This represents the maximum size of replication data sent over a single cycle for this interval.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-156">**NetworkFailureCount**</span><span class="sxs-lookup"><span data-stu-id="42c58-156">**NetworkFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-159">Nombre total d’erreurs réseau rencontrées pour le canal de réplication avec le système hôte de récupération.</span><span class="sxs-lookup"><span data-stu-id="42c58-159">The total number of network errors encountered for the replication channel with recovery host system.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-160">**PendingReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="42c58-160">**PendingReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-161">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42c58-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-163">Taille des données pour une réplication en attente, en octets.</span><span class="sxs-lookup"><span data-stu-id="42c58-163">The size of the data for a pending replication, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-164">**ReplicationFailureCount**</span><span class="sxs-lookup"><span data-stu-id="42c58-164">**ReplicationFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-167">Nombre total d’échecs de réplication.</span><span class="sxs-lookup"><span data-stu-id="42c58-167">The total number of replication failures.</span></span> <span data-ttu-id="42c58-168">Cela comprend les erreurs de l’opération de réplication.</span><span class="sxs-lookup"><span data-stu-id="42c58-168">This includes errors for replication operation.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-169">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="42c58-169">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-172">Intégrité de la réplication pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="42c58-172">The replication health for the virtual machine.</span></span> <span data-ttu-id="42c58-173">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="42c58-173">This will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="42c58-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (0)</span><span class="sxs-lookup"><span data-stu-id="42c58-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not applicable** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42c58-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="42c58-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok** (1)</span></span>
</dt> <dt>

<span data-ttu-id="42c58-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (2)</span><span class="sxs-lookup"><span data-stu-id="42c58-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (2)</span></span>
</dt> <dt>

<span data-ttu-id="42c58-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="42c58-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critical** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42c58-178">**ReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="42c58-178">**ReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-179">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-181">Latence totale de réplication lors du transfert des données vers le système hôte de récupération, en secondes.</span><span class="sxs-lookup"><span data-stu-id="42c58-181">Total replication latency while transferring the data to the recovery host system, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-182">**ReplicationMissCount**</span><span class="sxs-lookup"><span data-stu-id="42c58-182">**ReplicationMissCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-183">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-185">Nombre de cycles de réplication manqués.</span><span class="sxs-lookup"><span data-stu-id="42c58-185">The number of missed replication cycles.</span></span> <span data-ttu-id="42c58-186">Cela peut être dû à de lourdes charges de travail, problèmes réseau ou erreurs de réplication.</span><span class="sxs-lookup"><span data-stu-id="42c58-186">This can be because of heavy workload, network issues, or replication errors.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-187">**ReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="42c58-187">**ReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-188">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42c58-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-190">Quantité totale de données de réplication transférées au système hôte de récupération, en octets.</span><span class="sxs-lookup"><span data-stu-id="42c58-190">The total amount of replication data transferred to the recovery host system, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-191">**ReplicationSuccessCount**</span><span class="sxs-lookup"><span data-stu-id="42c58-191">**ReplicationSuccessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-192">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42c58-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-194">Nombre total de réplications réussies pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="42c58-194">The total number of successful replications for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="42c58-195">**StartStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="42c58-195">**StartStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42c58-196">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42c58-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42c58-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42c58-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42c58-198">Heure, en UTC, à laquelle le service de réplication Hyper-V a démarré la collecte des données des statistiques de réplication.</span><span class="sxs-lookup"><span data-stu-id="42c58-198">The time, in UTC, when the Hyper-V Replica service started gathering replication statistics data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42c58-199">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42c58-199">Requirements</span></span>



| <span data-ttu-id="42c58-200">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42c58-200">Requirement</span></span> | <span data-ttu-id="42c58-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="42c58-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42c58-202">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c58-202">Minimum supported client</span></span><br/> | <span data-ttu-id="42c58-203">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42c58-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42c58-204">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c58-204">Minimum supported server</span></span><br/> | <span data-ttu-id="42c58-205">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42c58-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42c58-206">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="42c58-206">Namespace</span></span><br/>                | <span data-ttu-id="42c58-207">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="42c58-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42c58-208">MOF</span><span class="sxs-lookup"><span data-stu-id="42c58-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42c58-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42c58-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42c58-210">DLL</span><span class="sxs-lookup"><span data-stu-id="42c58-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42c58-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42c58-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

