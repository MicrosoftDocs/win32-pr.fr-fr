---
description: Limite les ressources internes utilisées par les opérations initiées par les clients WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: Classe __ArbitratorConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203546"
---
# <a name="__arbitratorconfiguration-class"></a><span data-ttu-id="d1e65-103">\_\_ArbitratorConfiguration, classe</span><span class="sxs-lookup"><span data-stu-id="d1e65-103">\_\_ArbitratorConfiguration class</span></span>

<span data-ttu-id="d1e65-104">La classe **\_ \_ ArbitratorConfiguration** est une classe de configuration qui limite les ressources internes utilisées par les opérations initiées par les clients WMI.</span><span class="sxs-lookup"><span data-stu-id="d1e65-104">The **\_\_ArbitratorConfiguration** class is a configuration class that limits the internal resources that are used by operations initiated by WMI clients.</span></span> <span data-ttu-id="d1e65-105">Il s’agit d’une classe singleton qui réside dans l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="d1e65-105">This is a singleton class that resides in the \\root namespace.</span></span> <span data-ttu-id="d1e65-106">La classe est générée en interne et il n’y a aucun fichier MOF pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="d1e65-106">The class is internally generated so there is no MOF file for it.</span></span>

<span data-ttu-id="d1e65-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d1e65-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1e65-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d1e65-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e65-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1e65-109">Syntax</span></span>

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a><span data-ttu-id="d1e65-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d1e65-110">Members</span></span>

<span data-ttu-id="d1e65-111">La classe **\_ \_ ArbitratorConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1e65-111">The **\_\_ArbitratorConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="d1e65-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1e65-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1e65-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1e65-113">Properties</span></span>

<span data-ttu-id="d1e65-114">La classe **\_ \_ ArbitratorConfiguration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1e65-114">The **\_\_ArbitratorConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1e65-115">**OutstandingTasksPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-115">**OutstandingTasksPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-116">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-118">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-118">Unused.</span></span> <span data-ttu-id="d1e65-119">Nombre de tâches initiées par l’utilisateur en attente à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-119">Number of outstanding user initiated tasks at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-120">**OutstandingTasksTotal**</span><span class="sxs-lookup"><span data-stu-id="d1e65-120">**OutstandingTasksTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-121">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-123">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-123">Unused.</span></span> <span data-ttu-id="d1e65-124">Nombre total de tâches en suspens à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d1e65-124">Total number of outstanding tasks at any time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-125">**PermanentSubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-125">**PermanentSubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-128">Nombre d’abonnements permanents autorisés pour un utilisateur particulier à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-128">Number of permanent subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-129">**PermanentSubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="d1e65-129">**PermanentSubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-132">Nombre total d’abonnements permanents autorisés pour tous les utilisateurs à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-132">Total number of permanent subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-133">**PollingInstructionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-133">**PollingInstructionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-136">Nombre de requêtes d’événement d’interrogation autorisées pour un utilisateur particulier à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-136">Number of polling event queries allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-137">**PollingInstructionsTotal**</span><span class="sxs-lookup"><span data-stu-id="d1e65-137">**PollingInstructionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-140">Nombre total d’instructions d’interrogation autorisées pour tous les utilisateurs à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-140">Total number of polling instructions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-141">**PollingMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-141">**PollingMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-144">Quantité de requêtes d’événements d’interrogation de mémoire, émises par un utilisateur particulier, pouvant être consommées à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-144">Amount of memory polling event queries, issued by a particular user, can consume at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-145">**PollingMemoryTotal**</span><span class="sxs-lookup"><span data-stu-id="d1e65-145">**PollingMemoryTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-148">La quantité totale de mémoire utilisée par l’interrogation des requêtes d’événements pour tous les utilisateurs, peut être consommateur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d1e65-148">Total amount of memory that polling event queries, for all users combined, can consumer at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-149">**QuotaRetryCount**</span><span class="sxs-lookup"><span data-stu-id="d1e65-149">**QuotaRetryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-152">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-152">Unused.</span></span> <span data-ttu-id="d1e65-153">Nombre de violations de quota autorisées avant l’annulation d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="d1e65-153">Number of quota violations permitted before a task is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-154">**QuotaRetryWaitInterval**</span><span class="sxs-lookup"><span data-stu-id="d1e65-154">**QuotaRetryWaitInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-157">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-157">Unused.</span></span> <span data-ttu-id="d1e65-158">Délai introduit dans l’exécution de la tâche à chaque violation de quota.</span><span class="sxs-lookup"><span data-stu-id="d1e65-158">Delay introduced into the task execution on each quota violation.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-159">**TaskThreadsPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-159">**TaskThreadsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-162">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-162">Unused.</span></span> <span data-ttu-id="d1e65-163">Nombre maximal de threads de tâches associés à un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="d1e65-163">Maximum number of task threads associated with a particular user t any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-164">**TaskThreadsTotal**</span><span class="sxs-lookup"><span data-stu-id="d1e65-164">**TaskThreadsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-167">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-167">Unused.</span></span> <span data-ttu-id="d1e65-168">Nombre maximal de threads de tâche.</span><span class="sxs-lookup"><span data-stu-id="d1e65-168">Maximum number of task threads.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-169">**TemporarySubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-169">**TemporarySubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-172">Nombre d’abonnements temporaires autorisés pour un utilisateur particulier à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-172">Number of temporary subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-173">**TemporarySubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="d1e65-173">**TemporarySubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-174">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-176">Nombre total d’abonnements temporaires autorisés pour tous les utilisateurs à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-176">Total number of temporary subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-177">**TotalCacheDisk**</span><span class="sxs-lookup"><span data-stu-id="d1e65-177">**TotalCacheDisk**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-178">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-180">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-180">Unused.</span></span> <span data-ttu-id="d1e65-181">Cache disque total associé à tous les utilisateurs à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-181">Total disk cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-182">**TotalCacheDiskPerTask**</span><span class="sxs-lookup"><span data-stu-id="d1e65-182">**TotalCacheDiskPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-183">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-185">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-185">Unused.</span></span> <span data-ttu-id="d1e65-186">Cache disque total associé à une tâche particulière à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-186">Total disk cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-187">**TotalCacheDiskPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-187">**TotalCacheDiskPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-188">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-190">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-190">Unused.</span></span> <span data-ttu-id="d1e65-191">Cache disque total associé à un utilisateur particulier à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-191">Total disk cache associated with a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-192">**TotalCacheMemory**</span><span class="sxs-lookup"><span data-stu-id="d1e65-192">**TotalCacheMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-193">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-195">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-195">Unused.</span></span> <span data-ttu-id="d1e65-196">Cache mémoire total associé à tous les utilisateurs à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-196">Total memory cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-197">**TotalCacheMemoryPerTask**</span><span class="sxs-lookup"><span data-stu-id="d1e65-197">**TotalCacheMemoryPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-198">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-200">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-200">Unused.</span></span> <span data-ttu-id="d1e65-201">Cache mémoire total associé à une tâche particulière à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d1e65-201">Total memory cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-202">**TotalCacheMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="d1e65-202">**TotalCacheMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-203">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-205">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-205">Unused.</span></span> <span data-ttu-id="d1e65-206">Mémoire cache totale associée à un utilisateur particulier, à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d1e65-206">Total memory cache associated with a particular user at anyone time.</span></span>

</dd> <dt>

<span data-ttu-id="d1e65-207">**TotalUsers**</span><span class="sxs-lookup"><span data-stu-id="d1e65-207">**TotalUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e65-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e65-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e65-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e65-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e65-210">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d1e65-210">Unused.</span></span> <span data-ttu-id="d1e65-211">Nombre maximal d’utilisateurs connectés.</span><span class="sxs-lookup"><span data-stu-id="d1e65-211">Maximum number of connected users.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1e65-212">Notes</span><span class="sxs-lookup"><span data-stu-id="d1e65-212">Remarks</span></span>

<span data-ttu-id="d1e65-213">**\_ \_ ArbitratorConfiguration** est héritée de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="d1e65-213">**\_\_ArbitratorConfiguration** is inherited from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e65-214">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1e65-214">Requirements</span></span>



| <span data-ttu-id="d1e65-215">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1e65-215">Requirement</span></span> | <span data-ttu-id="d1e65-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1e65-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d1e65-217">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e65-217">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e65-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1e65-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d1e65-219">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e65-219">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e65-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1e65-220">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d1e65-221">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d1e65-221">Namespace</span></span><br/>                | <span data-ttu-id="d1e65-222">Root</span><span class="sxs-lookup"><span data-stu-id="d1e65-222">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d1e65-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1e65-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e65-224">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="d1e65-224">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="d1e65-225">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="d1e65-225">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

