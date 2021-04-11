---
description: Gère la réplication d’un ordinateur virtuel.
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203415"
---
# <a name="msvm_replicationservice-class"></a><span data-ttu-id="3dec0-103">MSVM \_ ReplicationService, classe</span><span class="sxs-lookup"><span data-stu-id="3dec0-103">Msvm\_ReplicationService class</span></span>

<span data-ttu-id="3dec0-104">Gère la réplication d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-104">Manages the replication for a virtual machine.</span></span>

<span data-ttu-id="3dec0-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3dec0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dec0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dec0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="3dec0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3dec0-107">Members</span></span>

<span data-ttu-id="3dec0-108">La classe **MSVM \_ ReplicationService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3dec0-108">The **Msvm\_ReplicationService** class has these types of members:</span></span>

-   [<span data-ttu-id="3dec0-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3dec0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3dec0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3dec0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3dec0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3dec0-111">Methods</span></span>

<span data-ttu-id="3dec0-112">La classe **MSVM \_ ReplicationService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3dec0-112">The **Msvm\_ReplicationService** class has these methods.</span></span>



| <span data-ttu-id="3dec0-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="3dec0-113">Method</span></span>                                                                                                 | <span data-ttu-id="3dec0-114">Description</span><span class="sxs-lookup"><span data-stu-id="3dec0-114">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dec0-115">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="3dec0-115">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="3dec0-116">Ajoute une entrée d’autorisation à un serveur.</span><span class="sxs-lookup"><span data-stu-id="3dec0-116">Adds an authorization entry to a server.</span></span><br/>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3dec0-117">**ChangeReplicationModeToPrimary**</span><span class="sxs-lookup"><span data-stu-id="3dec0-117">**ChangeReplicationModeToPrimary**</span></span>](changereplicationmodetoprimary-msvm-replicationservice.md)       | <span data-ttu-id="3dec0-118">Modifie la relation de réplication étendue en relation principale pour un ordinateur virtuel de réplication.</span><span class="sxs-lookup"><span data-stu-id="3dec0-118">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="3dec0-119">L’ordinateur virtuel de réplication doit être dans un état de basculement validé.</span><span class="sxs-lookup"><span data-stu-id="3dec0-119">The replica virtual machine must be in a failover committed state.</span></span><br/> <span data-ttu-id="3dec0-120">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3dec0-120">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="3dec0-121">**CommitFailover**</span><span class="sxs-lookup"><span data-stu-id="3dec0-121">**CommitFailover**</span></span>](commitfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="3dec0-122">Valide l’instantané de récupération utilisé par la méthode [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) pour un basculement.</span><span class="sxs-lookup"><span data-stu-id="3dec0-122">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="3dec0-123">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="3dec0-123">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="3dec0-124">Crée une relation de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-124">Creates a new replication relationship for a virtual machine.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="3dec0-125">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="3dec0-125">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)                   | <span data-ttu-id="3dec0-126">Récupère les statistiques de réplication d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-126">Retrieves replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="3dec0-127">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="3dec0-127">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)               | <span data-ttu-id="3dec0-128">Récupère les statistiques de réplication associées à la relation de réplication spécifiée de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-128">Retrieves the replication statistics that are associated with specified replication relationship of the virtual machine.</span></span><br/> <span data-ttu-id="3dec0-129">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3dec0-129">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                    |
| [<span data-ttu-id="3dec0-130">**GetSystemCertificates**</span><span class="sxs-lookup"><span data-stu-id="3dec0-130">**GetSystemCertificates**</span></span>](getsystemcertificates-msvm-replicationservice.md)                         | <span data-ttu-id="3dec0-131">Récupère les certificats système sur un système hôte.</span><span class="sxs-lookup"><span data-stu-id="3dec0-131">Retrieves the system certificates on a host system.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="3dec0-132">**ImportInitialReplica**</span><span class="sxs-lookup"><span data-stu-id="3dec0-132">**ImportInitialReplica**</span></span>](importinitialreplica-msvm-replicationservice.md)                           | <span data-ttu-id="3dec0-133">Importe la réplication initiale d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-133">Imports the initial replication for a virtual machine.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="3dec0-134">**InitiateFailback**</span><span class="sxs-lookup"><span data-stu-id="3dec0-134">**InitiateFailback**</span></span>](initiatefailback-msvm-replicationservice.md)                                   | <span data-ttu-id="3dec0-135">Lance la restauration automatique pour un ordinateur virtuel de récupération.</span><span class="sxs-lookup"><span data-stu-id="3dec0-135">Initiates the failback for a recovery virtual machine.</span></span> <span data-ttu-id="3dec0-136">Autrement dit, définit le basculement de la machine virtuelle sur une image de cohérence d’application ou d’incident.</span><span class="sxs-lookup"><span data-stu-id="3dec0-136">That is, sets the failover for the virtual machine to an app or crash consistent image.</span></span><br/> <span data-ttu-id="3dec0-137">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3dec0-137">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                              |
| [<span data-ttu-id="3dec0-138">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="3dec0-138">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)                                   | <span data-ttu-id="3dec0-139">Lance un basculement d’une machine virtuelle vers une image de point de réplication standard ou d’application.</span><span class="sxs-lookup"><span data-stu-id="3dec0-139">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="3dec0-140">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="3dec0-140">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="3dec0-141">Modifie une entrée d’autorisation sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="3dec0-141">Modifies an authorization entry on a server.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="3dec0-142">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="3dec0-142">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)                 | <span data-ttu-id="3dec0-143">Modifie les paramètres de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-143">Modifies the replication settings for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="3dec0-144">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="3dec0-144">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)                         | <span data-ttu-id="3dec0-145">Modifie les paramètres pour le service de réplication Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="3dec0-145">Modifies the settings for the Hyper-V Replica service.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="3dec0-146">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="3dec0-146">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="3dec0-147">Supprime l’entrée d’autorisation d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="3dec0-147">Removes the authorization entry from a server.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="3dec0-148">**RemoveReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="3dec0-148">**RemoveReplicationRelationship**</span></span>](removereplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="3dec0-149">Supprime une relation de réplication d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-149">Removes a virtual machine replication relationship.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="3dec0-150">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="3dec0-150">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)     | <span data-ttu-id="3dec0-151">Supprime la relation de réplication d’ordinateur virtuel spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3dec0-151">Removes the specified virtual machine replication relationship.</span></span> <span data-ttu-id="3dec0-152">Pour un ordinateur virtuel de réplication, la réplication principale ne peut pas être supprimée si la réplication étendue est activée.</span><span class="sxs-lookup"><span data-stu-id="3dec0-152">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span><br/> <span data-ttu-id="3dec0-153">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3dec0-153">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>     |
| [<span data-ttu-id="3dec0-154">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3dec0-154">**RequestStateChange**</span></span>](msvm-replicationservice-requeststatechange.md)                               | <span data-ttu-id="3dec0-155">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="3dec0-155">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3dec0-156">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="3dec0-156">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)               | <span data-ttu-id="3dec0-157">Réinitialise les statistiques de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-157">Resets the replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="3dec0-158">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="3dec0-158">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)           | <span data-ttu-id="3dec0-159">Réinitialise les statistiques de réplication associées à la relation de réplication spécifiée d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-159">Resets replication statistics that are associated with the specified replication relationship of a virtual machine.</span></span><br/> <span data-ttu-id="3dec0-160">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3dec0-160">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                         |
| [<span data-ttu-id="3dec0-161">**Resynchronise**</span><span class="sxs-lookup"><span data-stu-id="3dec0-161">**Resynchronize**</span></span>](resynchronize-msvm-replicationservice.md)                                         | <span data-ttu-id="3dec0-162">Effectue une opération de resynchronisation sur l’ordinateur virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="3dec0-162">Performs a resynchronization operation on the specified virtual machine.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="3dec0-163">**ReverseReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="3dec0-163">**ReverseReplicationRelationship**</span></span>](reversereplicationrelationship-msvm-replicationservice.md)       | <span data-ttu-id="3dec0-164">Réplication d’une machine virtuelle basculée sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="3dec0-164">Replicates a failed-over virtual machine back to the primary server.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="3dec0-165">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="3dec0-165">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="3dec0-166">Restaure le basculement en cours pour un ordinateur virtuel en ignorant le disque de basculement actuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-166">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="3dec0-167">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="3dec0-167">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="3dec0-168">Définit l’entrée d’autorisation de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-168">Sets the replication authorization entry for a virtual machine.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="3dec0-169">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="3dec0-169">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md) | <span data-ttu-id="3dec0-170">Configure les paramètres IP de la carte réseau à appliquer à un ordinateur virtuel après un basculement.</span><span class="sxs-lookup"><span data-stu-id="3dec0-170">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="3dec0-171">**StartReplication**</span><span class="sxs-lookup"><span data-stu-id="3dec0-171">**StartReplication**</span></span>](startreplication-msvm-replicationservice.md)                                   | <span data-ttu-id="3dec0-172">Démarre la réplication d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-172">Starts the replication of a virtual machine.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="3dec0-173">**StartService**</span><span class="sxs-lookup"><span data-stu-id="3dec0-173">**StartService**</span></span>](msvm-replicationservice-startservice.md)                                           | <span data-ttu-id="3dec0-174">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="3dec0-174">Starts the service.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="3dec0-175">**StopService**</span><span class="sxs-lookup"><span data-stu-id="3dec0-175">**StopService**</span></span>](msvm-replicationservice-stopservice.md)                                             | <span data-ttu-id="3dec0-176">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="3dec0-176">Stops the service.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="3dec0-177">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="3dec0-177">**TestReplicaSystem**</span></span>](testreplicasystem-msvm-replicationservice.md)                                 | <span data-ttu-id="3dec0-178">Crée un réplica d’une machine virtuelle avec la capture instantanée spécifiée à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="3dec0-178">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="3dec0-179">**TestReplicationConnection**</span><span class="sxs-lookup"><span data-stu-id="3dec0-179">**TestReplicationConnection**</span></span>](testreplicationconnection-msvm-replicationservice.md)                 | <span data-ttu-id="3dec0-180">Vérifie si la réplication peut être activée à partir du système hôte actuel vers le système de récupération spécifié.</span><span class="sxs-lookup"><span data-stu-id="3dec0-180">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span><br/>                                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="3dec0-181">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3dec0-181">Properties</span></span>

<span data-ttu-id="3dec0-182">La classe **MSVM \_ ReplicationService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3dec0-182">The **Msvm\_ReplicationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3dec0-183">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3dec0-183">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-184">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-186">Indique les valeurs possibles pour le paramètre *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="3dec0-186">Indicates the possible values for the *RequestedState* parameter.</span></span> <span data-ttu-id="3dec0-187">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-188">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3dec0-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-191">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3dec0-191">A short description of the object.</span></span> <span data-ttu-id="3dec0-192">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de réplication Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="3dec0-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Replica Service".</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3dec0-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-194">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-196">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="3dec0-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3dec0-197">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="3dec0-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3dec0-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3dec0-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3dec0-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3dec0-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="3dec0-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="3dec0-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="3dec0-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="3dec0-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3dec0-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3dec0-206">)</span><span class="sxs-lookup"><span data-stu-id="3dec0-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3dec0-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3dec0-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-210">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="3dec0-210">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-211">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="3dec0-211">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3dec0-212">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ReplicationService ».</span><span class="sxs-lookup"><span data-stu-id="3dec0-212">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ReplicationService".</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-213">**Description**</span><span class="sxs-lookup"><span data-stu-id="3dec0-213">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-216">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="3dec0-216">A description of the object.</span></span> <span data-ttu-id="3dec0-217">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de réplication ».</span><span class="sxs-lookup"><span data-stu-id="3dec0-217">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service".</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-218">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3dec0-218">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-219">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-221">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3dec0-221">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3dec0-222">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="3dec0-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3dec0-223">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3dec0-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="3dec0-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="3dec0-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="3dec0-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="3dec0-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="3dec0-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="3dec0-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="3dec0-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3dec0-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3dec0-232">)</span><span class="sxs-lookup"><span data-stu-id="3dec0-232">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3dec0-233">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3dec0-233">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-236">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3dec0-236">A display name for the object.</span></span> <span data-ttu-id="3dec0-237">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3dec0-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-239">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-241">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="3dec0-241">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="3dec0-242">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="3dec0-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="3dec0-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dec0-243">Value</span></span>                                                                        | <span data-ttu-id="3dec0-244">Signification</span><span class="sxs-lookup"><span data-stu-id="3dec0-244">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="3dec0-245"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-245"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3dec0-246">activé</span><span class="sxs-lookup"><span data-stu-id="3dec0-246">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3dec0-247">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3dec0-247">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-248">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-250">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="3dec0-250">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3dec0-251">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="3dec0-251">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="3dec0-252">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="3dec0-252">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="3dec0-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dec0-253">Value</span></span>                                                                        | <span data-ttu-id="3dec0-254">Signification</span><span class="sxs-lookup"><span data-stu-id="3dec0-254">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="3dec0-255"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-255"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3dec0-256">activé</span><span class="sxs-lookup"><span data-stu-id="3dec0-256">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3dec0-257">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3dec0-257">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-258">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-260">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3dec0-260">The current health of the element.</span></span> <span data-ttu-id="3dec0-261">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="3dec0-261">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="3dec0-262">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-262">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3dec0-263">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="3dec0-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="3dec0-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dec0-264">Value</span></span>                                                                        | <span data-ttu-id="3dec0-265">Signification</span><span class="sxs-lookup"><span data-stu-id="3dec0-265">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="3dec0-266"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-266"><dt>5</dt></span></span> </dl> | <span data-ttu-id="3dec0-267">L’état d’intégrité est normal.</span><span class="sxs-lookup"><span data-stu-id="3dec0-267">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3dec0-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3dec0-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-269">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3dec0-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-271">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3dec0-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="3dec0-272">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3dec0-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-276">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="3dec0-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-277">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3dec0-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3dec0-278">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-279">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3dec0-279">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-282">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="3dec0-282">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-283">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="3dec0-283">The label by which the object is known.</span></span> <span data-ttu-id="3dec0-284">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « replicasvc ».</span><span class="sxs-lookup"><span data-stu-id="3dec0-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "replicasvc".</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-285">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3dec0-285">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-286">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-288">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3dec0-288">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3dec0-289">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="3dec0-289">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3dec0-290">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-290">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3dec0-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3dec0-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3dec0-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="3dec0-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="3dec0-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="3dec0-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="3dec0-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="3dec0-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="3dec0-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="3dec0-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="3dec0-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="3dec0-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="3dec0-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="3dec0-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="3dec0-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="3dec0-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="3dec0-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="3dec0-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="3dec0-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3dec0-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3dec0-310">)</span><span class="sxs-lookup"><span data-stu-id="3dec0-310">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3dec0-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3dec0-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-312">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-314">Tableau qui contient les États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3dec0-314">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="3dec0-315">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="3dec0-316">La valeur à l’index zéro sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3dec0-316">The value at index zero will be one of the following values.</span></span>



| <span data-ttu-id="3dec0-317">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dec0-317">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="3dec0-318">Signification</span><span class="sxs-lookup"><span data-stu-id="3dec0-318">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="3dec0-319"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-319"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                  | <span data-ttu-id="3dec0-320">Le service de réplication fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="3dec0-320">The replication service is operating normally.</span></span><br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <span data-ttu-id="3dec0-321"><dt>**Erreur**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-321"><dt>**Error**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="3dec0-322">Un ou plusieurs écouteurs réseau de réplication ne sont pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3dec0-322">One or more replication network listeners are not running.</span></span> <span data-ttu-id="3dec0-323">Vérifiez que les paramètres du service de réplication sont valides.</span><span class="sxs-lookup"><span data-stu-id="3dec0-323">Verify that the replication service settings are valid.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3dec0-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3dec0-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-327">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="3dec0-327">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="3dec0-328">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="3dec0-328">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3dec0-329">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-330">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="3dec0-330">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-333">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="3dec0-333">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-334">Toutes les informations relatives à la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="3dec0-334">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="3dec0-335">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-335">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-336">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="3dec0-336">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-339">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="3dec0-339">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-340">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="3dec0-340">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="3dec0-341">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="3dec0-341">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="3dec0-342">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-342">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3dec0-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-344">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-346">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="3dec0-346">Provides high level status information.</span></span> <span data-ttu-id="3dec0-347">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="3dec0-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3dec0-348">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="3dec0-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3dec0-349">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3dec0-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3dec0-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="3dec0-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="3dec0-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="3dec0-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="3dec0-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3dec0-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3dec0-356">)</span><span class="sxs-lookup"><span data-stu-id="3dec0-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3dec0-357">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3dec0-357">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-358">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-360">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="3dec0-360">The last requested or desired state for the element.</span></span> <span data-ttu-id="3dec0-361">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-361">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="3dec0-362">Cette propriété est fournie pour comparer les derniers États demandés et actuels d’un élément.</span><span class="sxs-lookup"><span data-stu-id="3dec0-362">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="3dec0-363">Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la propriété **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="3dec0-363">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="3dec0-364">Si cela se produit, la valeur 12 (« non applicable ») est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3dec0-364">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="3dec0-365">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="3dec0-365">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="3dec0-366">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dec0-366">Value</span></span>                                                                         | <span data-ttu-id="3dec0-367">Signification</span><span class="sxs-lookup"><span data-stu-id="3dec0-367">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="3dec0-368"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-368"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3dec0-369">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="3dec0-369">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3dec0-370">**Cours**</span><span class="sxs-lookup"><span data-stu-id="3dec0-370">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-371">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3dec0-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-373">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3dec0-373">Indicates whether the service is currently running.</span></span> <span data-ttu-id="3dec0-374">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-374">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-375">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="3dec0-375">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-378">Qualificateurs : **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="3dec0-378">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-379">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="3dec0-379">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="3dec0-380">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-380">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-381">**État**</span><span class="sxs-lookup"><span data-stu-id="3dec0-381">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-384">Indique l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3dec0-384">Indicates the status of the element.</span></span> <span data-ttu-id="3dec0-385">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="3dec0-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-386">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3dec0-386">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-387">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="3dec0-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-389">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3dec0-389">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3dec0-390">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3dec0-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3dec0-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-392">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-394">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="3dec0-394">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-395">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="3dec0-395">The scoping system's creation class name.</span></span> <span data-ttu-id="3dec0-396">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="3dec0-396">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-397">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3dec0-397">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-398">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3dec0-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-400">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="3dec0-400">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-401">Nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3dec0-401">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="3dec0-402">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="3dec0-402">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3dec0-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-404">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3dec0-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-406">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3dec0-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3dec0-407">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3dec0-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3dec0-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3dec0-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dec0-409">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3dec0-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3dec0-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dec0-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dec0-411">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="3dec0-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3dec0-412">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3dec0-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3dec0-413">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3dec0-413">Requirements</span></span>



| <span data-ttu-id="3dec0-414">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dec0-414">Requirement</span></span> | <span data-ttu-id="3dec0-415">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dec0-415">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dec0-416">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dec0-416">Minimum supported client</span></span><br/> | <span data-ttu-id="3dec0-417">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dec0-417">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3dec0-418">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dec0-418">Minimum supported server</span></span><br/> | <span data-ttu-id="3dec0-419">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dec0-419">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3dec0-420">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3dec0-420">Namespace</span></span><br/>                | <span data-ttu-id="3dec0-421">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3dec0-421">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3dec0-422">MOF</span><span class="sxs-lookup"><span data-stu-id="3dec0-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dec0-423"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-423"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dec0-424">DLL</span><span class="sxs-lookup"><span data-stu-id="3dec0-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dec0-425"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3dec0-425"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

