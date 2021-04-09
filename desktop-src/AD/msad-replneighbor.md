---
title: Classe MSAD_ReplNeighbor
description: Représente la structure du voisin du service de \_ \_ réplication de contenu, qui contient les informations d’état de la réplication entrante pour un contexte d’appellation (NC) et une paire de serveurs sources spécifiques.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor de la classe Active Directory
- MSAD_ReplNeighbor de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942172"
---
# <a name="msad_replneighbor-class"></a><span data-ttu-id="aabbb-105">MSAD \_ ReplNeighbor, classe</span><span class="sxs-lookup"><span data-stu-id="aabbb-105">MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="aabbb-106">Représente la structure du [**\_ \_ voisin du service**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) de réplication de contenu, qui contient les informations d’état de la réplication entrante pour un contexte d’appellation (NC) et une paire de serveurs sources spécifiques, tels que retournés par la fonction [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="aabbb-106">Represents the [**DS\_REPL\_NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) structure, which contains the inbound replication state information for a particular naming context (NC) and source server pair, as returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabbb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aabbb-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a><span data-ttu-id="aabbb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="aabbb-108">Members</span></span>

<span data-ttu-id="aabbb-109">La classe **MSAD \_ ReplNeighbor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aabbb-109">The **MSAD\_ReplNeighbor** class has these types of members:</span></span>

-   [<span data-ttu-id="aabbb-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aabbb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aabbb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aabbb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aabbb-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aabbb-112">Methods</span></span>

<span data-ttu-id="aabbb-113">La classe **MSAD \_ ReplNeighbor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="aabbb-113">The **MSAD\_ReplNeighbor** class has these methods.</span></span>



| <span data-ttu-id="aabbb-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="aabbb-114">Method</span></span>                                                           | <span data-ttu-id="aabbb-115">Description</span><span class="sxs-lookup"><span data-stu-id="aabbb-115">Description</span></span>                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="aabbb-116">**SyncNamingContext**</span><span class="sxs-lookup"><span data-stu-id="aabbb-116">**SyncNamingContext**</span></span>](syncnamingcontext-msad-replneighbor.md) | <span data-ttu-id="aabbb-117">Synchronise un contexte d’appellation de destination avec l’une de ses sources.</span><span class="sxs-lookup"><span data-stu-id="aabbb-117">Synchronizes a destination naming context with one of its sources.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="aabbb-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aabbb-118">Properties</span></span>

<span data-ttu-id="aabbb-119">La classe **MSAD \_ ReplNeighbor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="aabbb-119">The **MSAD\_ReplNeighbor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aabbb-120">**AsyncIntersiteTransportDN**</span><span class="sxs-lookup"><span data-stu-id="aabbb-120">**AsyncIntersiteTransportDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-123">Obtient le chemin d’accès X. 500 de l’objet [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) qui correspond au transport sur lequel la réplication est effectuée.</span><span class="sxs-lookup"><span data-stu-id="aabbb-123">Gets the X.500 path of the [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) object that corresponds to the transport over which replication is performed.</span></span> <span data-ttu-id="aabbb-124">Affectez la valeur **null** pour la réplication RPC/IP.</span><span class="sxs-lookup"><span data-stu-id="aabbb-124">Set to **NULL** for RPC/IP replication.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-125">**AsyncIntersiteTransportObjGuid**</span><span class="sxs-lookup"><span data-stu-id="aabbb-125">**AsyncIntersiteTransportObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-126">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-128">Obtient le GUID de l’objet de transport intersite qui correspond à la propriété **AsyncIntersiteTransportDN** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-128">Gets the GUID of the intersite transport object that corresponds to the **AsyncIntersiteTransportDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-129">**CompressChanges**</span><span class="sxs-lookup"><span data-stu-id="aabbb-129">**CompressChanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-132">Obtient la valeur qui indique si l’indicateur de **\_ modifications de \_ \_ compresser les \_ changements de réplication DS** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-132">Gets the value that indicates whether the **DS\_REPL\_NBR\_COMPRESS\_CHANGES** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-133">**DisableScheduledSync**</span><span class="sxs-lookup"><span data-stu-id="aabbb-133">**DisableScheduledSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-136">Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ synchronisation planifiée du service de réplication de l’annuaire de réplication** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-136">Gets the value that indicates whether the **DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-137">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="aabbb-137">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-138">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-140">Obtient le nom canonique du domaine du contexte de nommage répliqué.</span><span class="sxs-lookup"><span data-stu-id="aabbb-140">Gets the canonical name of the domain of the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-141">**DoScheduledSyncs**</span><span class="sxs-lookup"><span data-stu-id="aabbb-141">**DoScheduledSyncs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-144">Obtient la valeur qui indique si l’indicateur de **synchronisations de réplication de service d’annuaire \_ \_ \_ do do \_ scheduled \_** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-144">Gets the value that indicates whether the **DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-145">**FullSyncInProgress**</span><span class="sxs-lookup"><span data-stu-id="aabbb-145">**FullSyncInProgress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-148">Obtient la valeur qui indique si l’indicateur **DS \_ REPL \_ NBR \_ Full \_ Sync \_ en \_ cours** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-148">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-149">**FullSyncNextPacket**</span><span class="sxs-lookup"><span data-stu-id="aabbb-149">**FullSyncNextPacket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-150">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-152">Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ paquet Next Sync de \_ paquets de réplication complète** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-152">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-153">**IgnoreChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="aabbb-153">**IgnoreChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-154">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-156">Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ notification des modifications de l’annuaire de réplication des modifications** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-156">Gets the value that indicates whether the **DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-157">**IsDeletedSourceDsa**</span><span class="sxs-lookup"><span data-stu-id="aabbb-157">**IsDeletedSourceDsa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-158">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-160">Obtient la valeur qui indique si cette connexion représente un contrôleur de périphérique source qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="aabbb-160">Gets the value that indicates whether this connection represents a source DC that has been deleted.</span></span> <span data-ttu-id="aabbb-161">**True** si cette connexion représente un contrôleur de périphérique source qui a été supprimé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="aabbb-161">**TRUE** if this connection represents a source DC that has been deleted; otherwise, **FALSE**.</span></span> <span data-ttu-id="aabbb-162">Par défaut, le service d’annuaire continue à répliquer ces connexions pendant un certain temps, après la suppression du contrôleur de domaine source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-162">By design, the DS will continue to replicate these connections for some time for some time after the source DC is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-163">**LastSyncResult**</span><span class="sxs-lookup"><span data-stu-id="aabbb-163">**LastSyncResult**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-164">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aabbb-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-166">Obtient le code d’erreur **HRESULT** de la dernière tentative de réplication.</span><span class="sxs-lookup"><span data-stu-id="aabbb-166">Gets the **HRESULT** error code for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-167">**ModifiedNumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="aabbb-167">**ModifiedNumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aabbb-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-170">Obtient le nombre de tentatives de réplication consécutives ayant échoué, à l’exclusion des connexions qui sont supposées échouer.</span><span class="sxs-lookup"><span data-stu-id="aabbb-170">Gets the number of consecutive failed replication attempts, not including the connections that are expected to fail.</span></span> <span data-ttu-id="aabbb-171">Par exemple, si la propriété **IsDeletedSourceDsa** a la valeur **true**, elle est censée échouer.</span><span class="sxs-lookup"><span data-stu-id="aabbb-171">For example, if the **IsDeletedSourceDsa** property is set to **TRUE**, it is expected to fail.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-172">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="aabbb-172">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-173">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-175">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aabbb-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-176">Obtient le chemin d’accès X. 500 pour le contexte de nommage qui est répliqué par cette connexion.</span><span class="sxs-lookup"><span data-stu-id="aabbb-176">Gets the X.500 path for the NC that is replicated by this connection.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-177">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="aabbb-177">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-178">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-180">Obtient le GUID du contexte de nommage répliqué.</span><span class="sxs-lookup"><span data-stu-id="aabbb-180">Gets the GUID for the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-181">**NeverSynced**</span><span class="sxs-lookup"><span data-stu-id="aabbb-181">**NeverSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-182">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-184">Obtient la valeur qui indique si l’indicateur de **réplication du service d’annuaire \_ n’est \_ \_ jamais \_ synchronisé** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-184">Gets the value that indicates whether the **DS\_REPL\_NBR\_NEVER\_SYNCED** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-185">**NoChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="aabbb-185">**NoChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-186">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-188">Obtient la valeur qui indique si l’indicateur de **notification de modification du \_ numéro de réplication DS n’a \_ \_ pas \_ \_** été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-188">Gets the value that indicates whether the **DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-189">**NumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="aabbb-189">**NumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-190">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aabbb-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-192">Obtient le nombre de tentatives de réplication consécutives ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="aabbb-192">Gets the number of consecutive failed replication attempts.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-193">**ReplicaFlags**</span><span class="sxs-lookup"><span data-stu-id="aabbb-193">**ReplicaFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-194">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aabbb-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-196">Obtient le jeu d’indicateurs qui spécifient des attributs et des options pour les données de réplication.</span><span class="sxs-lookup"><span data-stu-id="aabbb-196">Gets the set of flags that specify attributes and options for the replication data.</span></span> <span data-ttu-id="aabbb-197">Cette propriété peut être zéro ou une combinaison d’un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="aabbb-197">This property can be zero or a combination of one or more of the following flags.</span></span>

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span data-ttu-id="aabbb-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**Service d’annuaire \_ REPL \_ NBR \_ inscriptible** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="aabbb-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS\_REPL\_NBR\_WRITEABLE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-199">La copie locale du contexte de nommage est accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="aabbb-199">The local copy of the naming context is writable.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span data-ttu-id="aabbb-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**Service d’annuaire \_ REPL \_ NBR \_ Sync \_ au \_ démarrage** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="aabbb-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-201">La réplication de ce contexte d’appellation à partir de cette source est tentée lors du démarrage du serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="aabbb-201">Replication of this naming context from this source is attempted when the destination server is booted.</span></span> <span data-ttu-id="aabbb-202">En règle générale, cet indicateur s’applique uniquement aux voisins intra-sites.</span><span class="sxs-lookup"><span data-stu-id="aabbb-202">This flag usually only applies to intra-site neighbors.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span data-ttu-id="aabbb-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**Service d’annuaire \_ REPL \_ \_ do do \_ scheduled \_ syncs** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="aabbb-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-204">Exécuter la réplication selon une planification.</span><span class="sxs-lookup"><span data-stu-id="aabbb-204">Perform replication on a schedule.</span></span> <span data-ttu-id="aabbb-205">Cet indicateur est généralement défini, à moins que la planification de ce contexte de nommage ou source ne soit « jamais », autrement dit, la planification vide.</span><span class="sxs-lookup"><span data-stu-id="aabbb-205">This flag is usually set unless the schedule for this naming context or source is "never", that is, the empty schedule.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span data-ttu-id="aabbb-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**Service d’annuaire \_ REPL \_ NBR \_ use \_ Async \_ intersite \_ transport** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="aabbb-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-207">Exécuter la réplication indirectement par le biais du service de messagerie inter-sites.</span><span class="sxs-lookup"><span data-stu-id="aabbb-207">Perform replication indirectly through the Inter-Site Messaging Service.</span></span> <span data-ttu-id="aabbb-208">Cet indicateur est défini uniquement lors de la réplication sur SMTP.</span><span class="sxs-lookup"><span data-stu-id="aabbb-208">This flag is set only when replicating over SMTP.</span></span> <span data-ttu-id="aabbb-209">Cet indicateur n'est pas défini lors de la réplication sur RPC/IP inter-site.</span><span class="sxs-lookup"><span data-stu-id="aabbb-209">This flag is not set when replicating over inter-site RPC/IP.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span data-ttu-id="aabbb-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**Service d’annuaire \_ \_ \_ \_ \_ Synchronisation bidirectionnelle REPL** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="aabbb-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS\_REPL\_NBR\_TWO\_WAY\_SYNC** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-211">Si cette valeur est définie, cela indique que lorsque la réplication entrante est terminée, le serveur de destination doit indiquer au serveur source de se synchroniser dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="aabbb-211">If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction.</span></span> <span data-ttu-id="aabbb-212">Cette fonctionnalité est utilisée dans les scénarios d'accès à distance dans lesquels un seul des deux serveurs peut initier une connexion d'accès à distance.</span><span class="sxs-lookup"><span data-stu-id="aabbb-212">This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection.</span></span> <span data-ttu-id="aabbb-213">Par exemple, cette option peut être utilisée dans un siège social et une filiale, où la filiale se connecte au siège social sur Internet au moyen d’une connexion d’accès à distance à l’ISP.</span><span class="sxs-lookup"><span data-stu-id="aabbb-213">For example, this option could be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span data-ttu-id="aabbb-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**Service d’annuaire \_ L' \_ \_ objet REPL retourne les \_ \_ parents** de l’objet (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="aabbb-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS\_REPL\_NBR\_RETURN\_OBJECT\_PARENTS** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-215">Ce voisin est dans un état où il retourne les objets parents avant les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="aabbb-215">This neighbor is in a state where it returns parent objects before children objects.</span></span> <span data-ttu-id="aabbb-216">Il bascule dans cet état après avoir reçu un objet enfant avant son parent.</span><span class="sxs-lookup"><span data-stu-id="aabbb-216">It goes into this state after it receives a child object before its parent.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span data-ttu-id="aabbb-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**Service d’annuaire \_ Réplication \_ \_ complète \_ de la synchronisation \_ en \_ cours** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-218">Le serveur de destination exécute une synchronisation complète à partir du serveur source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-218">The destination server is performing a full synchronization from the source server.</span></span> <span data-ttu-id="aabbb-219">Les synchronisations complètes n’utilisent pas les vecteurs qui créent des mises à jour (tels que les [**\_ \_ curseurs REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) pour le filtrage des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="aabbb-219">Full synchronizations do not use vectors that create updates (such as [**DS\_REPL\_CURSORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) for filtering updates.</span></span> <span data-ttu-id="aabbb-220">Les synchronisations complètes ne sont pas utilisées dans le cadre du protocole de réplication par défaut.</span><span class="sxs-lookup"><span data-stu-id="aabbb-220">Full synchronizations are not used as a part of the default replication protocol.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span data-ttu-id="aabbb-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**Service d’annuaire \_ Paquet de réplication \_ \_ complète à \_ synchronisation \_ \_ complète** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-222">Le dernier paquet de la source indiquait une modification d’un objet que le serveur de destination n’a pas encore créé.</span><span class="sxs-lookup"><span data-stu-id="aabbb-222">The last packet from the source indicated a modification of an object that the destination server has not yet created.</span></span> <span data-ttu-id="aabbb-223">Le paquet suivant à demander demande au serveur source de placer tous les attributs de l’objet modifié dans le paquet.</span><span class="sxs-lookup"><span data-stu-id="aabbb-223">The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span data-ttu-id="aabbb-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**Service d’annuaire \_ REPL \_ \_ n’est jamais \_ synchronisé** (2097152 (0x200000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS\_REPL\_NBR\_NEVER\_SYNCED** (2097152 (0x200000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-225">Aucune synchronisation n'a jamais été effectuée avec succès à partir de cette source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-225">A synchronization has never been successfully completed from this source.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span data-ttu-id="aabbb-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**Service d’annuaire \_ Taux de réplication \_ \_ anticipé** (16777216 (0x1000000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS\_REPL\_NBR\_PREEMPTED** (16777216 (0x1000000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-227">Le moteur de réplication a temporairement cessé de traiter ce voisin afin de traiter un autre voisin de priorité plus élevée, que ce soit pour cette partition ou pour une autre partition.</span><span class="sxs-lookup"><span data-stu-id="aabbb-227">The replication engine has temporarily stopped processing this neighbor in order to service another higher-priority neighbor, either for this partition or for another partition.</span></span> <span data-ttu-id="aabbb-228">Le moteur de réplication reprendra le traitement de ce voisin une fois le travail de priorité plus élevée terminé.</span><span class="sxs-lookup"><span data-stu-id="aabbb-228">The replication engine will resume processing this neighbor after the higher-priority work is completed.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span data-ttu-id="aabbb-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**Service d’annuaire \_ Réplication \_ \_ Ignorer \_ les \_ notifications de modifications** (67108864 (0x4000000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** (67108864 (0x4000000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-230">Ce voisin est défini pour désactiver les synchronisations basées sur les notifications.</span><span class="sxs-lookup"><span data-stu-id="aabbb-230">This neighbor is set to disable notification-based synchronizations.</span></span> <span data-ttu-id="aabbb-231">Dans un site, les contrôleurs de domaine se synchronisent les uns avec les autres en fonction des notifications lorsque des modifications se produisent.</span><span class="sxs-lookup"><span data-stu-id="aabbb-231">Within a site, domain controllers synchronize with each other based on notifications when changes occur.</span></span> <span data-ttu-id="aabbb-232">Ce paramètre empêche ce voisin d’effectuer des synchronisations qui sont déclenchées par des notifications.</span><span class="sxs-lookup"><span data-stu-id="aabbb-232">This setting prevents this neighbor from performing synchronizations that are triggered by notifications.</span></span> <span data-ttu-id="aabbb-233">Le voisin effectue toujours des synchronisations en fonction de sa planification, ou en réponse à des synchronisations demandées manuellement.</span><span class="sxs-lookup"><span data-stu-id="aabbb-233">The neighbor will still do synchronizations based on its schedule, or in response to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span data-ttu-id="aabbb-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**Service d’annuaire \_ REPL \_ NBR \_ Disable \_ scheduled \_ Sync** (134217728 (0x8000000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** (134217728 (0x8000000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-235">Ce voisin est configuré de façon à ne pas effectuer de synchronisations selon sa planification.</span><span class="sxs-lookup"><span data-stu-id="aabbb-235">This neighbor is set to not perform synchronizations based on its schedule.</span></span> <span data-ttu-id="aabbb-236">La seule façon dont ce voisin effectuera des synchronisations est en réponse aux notifications de modification ou aux synchronisations demandées manuellement.</span><span class="sxs-lookup"><span data-stu-id="aabbb-236">The only way this neighbor will perform synchronizations is in response to change notifications or to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span data-ttu-id="aabbb-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**Service d’annuaire \_ Réplication des \_ \_ \_ changements de compression** (268435456 (0x10000000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS\_REPL\_NBR\_COMPRESS\_CHANGES** (268435456 (0x10000000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-238">Les modifications reçues de cette source doivent être compressées.</span><span class="sxs-lookup"><span data-stu-id="aabbb-238">Changes received from this source are to be compressed.</span></span> <span data-ttu-id="aabbb-239">La compression se produit généralement uniquement si le serveur source se trouve dans un autre site.</span><span class="sxs-lookup"><span data-stu-id="aabbb-239">Compression usually occurs only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span data-ttu-id="aabbb-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**Service d’annuaire \_ REPL \_ \_ n ° \_ de \_ notifications de modification** (536870912 (0x20000000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** (536870912 (0x20000000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-241">Aucune notification de modification ne doit être reçue à partir de cette source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-241">No change notifications should be received from this source.</span></span> <span data-ttu-id="aabbb-242">Généralement défini uniquement si le serveur source se trouve dans un autre site.</span><span class="sxs-lookup"><span data-stu-id="aabbb-242">Usually set only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span data-ttu-id="aabbb-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**Service d’annuaire \_ \_Jeu d' \_ \_ attributs \_ partiels REPL NBR** (1073741824 (0x40000000))</span><span class="sxs-lookup"><span data-stu-id="aabbb-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS\_REPL\_NBR\_PARTIAL\_ATTRIBUTE\_SET** (1073741824 (0x40000000))</span></span>


</dt> <dd>

<span data-ttu-id="aabbb-244">Ce voisin est dans un état où il recrée le contenu de ce réplica à cause d'une modification dans le jeu d'attributs partiel.</span><span class="sxs-lookup"><span data-stu-id="aabbb-244">This neighbor is in a state where it is rebuilding the contents of this replica because of a change in the partial attribute set.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aabbb-245">**SourceDsaAddress**</span><span class="sxs-lookup"><span data-stu-id="aabbb-245">**SourceDsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-246">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-248">Obtient l’adresse DNS du contrôleur de domaine source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-248">Gets the DNS address of the source DC.</span></span>

> [!Note]  
> <span data-ttu-id="aabbb-249">Cette chaîne contient un GUID modifié, et non le nom DNS canonique couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="aabbb-249">This string contains a modified GUID, not the commonly used canonical DNS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="aabbb-250">**SourceDsaCN**</span><span class="sxs-lookup"><span data-stu-id="aabbb-250">**SourceDsaCN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-251">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-253">Obtient le composant de chemin d’accès de l’objet pour le DSA qui représente le contrôleur de périphérique source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-253">Gets the object path component for the DSA that represents the source DC.</span></span> <span data-ttu-id="aabbb-254">Cette chaîne est souvent similaire au nom de l’ordinateur, mais elle n’est pas toujours identique.</span><span class="sxs-lookup"><span data-stu-id="aabbb-254">This string is often similar to the computer name but is not always identical.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-255">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="aabbb-255">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-256">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-258">Obtient le chemin d’accès X. 500 pour le DSA qui représente le contrôleur de périphérique source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-258">Gets the X.500 path for the DSA that represents the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-259">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="aabbb-259">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-260">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-262">Obtient l’ID d’appel qui a été utilisé par le serveur source à partir de la dernière réplication.</span><span class="sxs-lookup"><span data-stu-id="aabbb-262">Gets the invocation ID that was used by the source server as of the last replication.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-263">**SourceDsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="aabbb-263">**SourceDsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-264">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-266">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aabbb-266">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-267">Obtient le GUID de l’agent de service d’annuaire (DSA) qui représente le contrôleur de domaine source (DC).</span><span class="sxs-lookup"><span data-stu-id="aabbb-267">Gets the GUID for the directory service agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-268">**SourceDsaSite**</span><span class="sxs-lookup"><span data-stu-id="aabbb-268">**SourceDsaSite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aabbb-269">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-271">Obtient le site qui contient le contrôleur de site source.</span><span class="sxs-lookup"><span data-stu-id="aabbb-271">Gets the site that contains the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-272">**SyncOnStartup**</span><span class="sxs-lookup"><span data-stu-id="aabbb-272">**SyncOnStartup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-273">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-275">Obtient la valeur qui indique si l’indicateur **DS \_ REPL \_ NBR \_ Sync \_ au \_ démarrage** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-275">Gets the value that indicates whether the **DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-276">**TimeOfLastSyncAttempt**</span><span class="sxs-lookup"><span data-stu-id="aabbb-276">**TimeOfLastSyncAttempt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-277">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aabbb-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-279">Obtient l’horodateur de la dernière tentative de réplication.</span><span class="sxs-lookup"><span data-stu-id="aabbb-279">Gets the timestamp for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-280">**TimeOfLastSyncSuccess**</span><span class="sxs-lookup"><span data-stu-id="aabbb-280">**TimeOfLastSyncSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-281">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aabbb-281">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-283">Obtient l’horodateur de la dernière tentative de réplication réussie.</span><span class="sxs-lookup"><span data-stu-id="aabbb-283">Gets the timestamp for the last successful replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-284">**TwoWaySync**</span><span class="sxs-lookup"><span data-stu-id="aabbb-284">**TwoWaySync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-285">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-287">Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ synchronisation de réplication du compte de réplication bi** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-287">Gets the value that indicates whether the **DS\_REPL\_NBR\_TWO\_WAY\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-288">**UseAsyncIntersiteTransport**</span><span class="sxs-lookup"><span data-stu-id="aabbb-288">**UseAsyncIntersiteTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-289">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-291">Obtient la valeur qui indique si l’indicateur de **\_ \_ \_ \_ \_ \_ transport intersite asynchrone du service d’annuaire de réplication d’annuaire** a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-291">Gets the value that indicates whether the **DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-292">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="aabbb-292">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-293">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aabbb-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-295">Obtient la valeur de la propriété **USNLastObjChangeSynced** à la fin du dernier cycle de réplication effectué avec succès.</span><span class="sxs-lookup"><span data-stu-id="aabbb-295">Gets the **USNLastObjChangeSynced** property value at the end of the last successful completed replication cycle.</span></span> <span data-ttu-id="aabbb-296">Zéro si aucun cycle de réplication n’a été effectué avec succès.</span><span class="sxs-lookup"><span data-stu-id="aabbb-296">Zero if there were no successfully completed replication cycles.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-297">**USNLastObjChangeSynced**</span><span class="sxs-lookup"><span data-stu-id="aabbb-297">**USNLastObjChangeSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-298">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aabbb-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-300">Obtient la valeur d’attribut non [**modifiée**](/windows/desktop/ADSchema/a-usnchanged) de la dernière mise à jour d’objet qui a été reçue.</span><span class="sxs-lookup"><span data-stu-id="aabbb-300">Gets the [**unchanged**](/windows/desktop/ADSchema/a-usnchanged) attribute value of the last object update that was received.</span></span>

</dd> <dt>

<span data-ttu-id="aabbb-301">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="aabbb-301">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabbb-302">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aabbb-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aabbb-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aabbb-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabbb-304">Obtient la valeur qui indique si l’indicateur d' **\_ \_ \_ écriture de réplication** de compte d’annuaire a été défini dans la propriété **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="aabbb-304">Gets the value that indicates whether the **DS\_REPL\_NBR\_WRITEABLE** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aabbb-305">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aabbb-305">Requirements</span></span>



| <span data-ttu-id="aabbb-306">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aabbb-306">Requirement</span></span> | <span data-ttu-id="aabbb-307">Valeur</span><span class="sxs-lookup"><span data-stu-id="aabbb-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aabbb-308">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aabbb-308">Minimum supported client</span></span><br/> | <span data-ttu-id="aabbb-309">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="aabbb-309">None supported</span></span><br/>                                                               |
| <span data-ttu-id="aabbb-310">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aabbb-310">Minimum supported server</span></span><br/> | <span data-ttu-id="aabbb-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aabbb-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aabbb-312">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aabbb-312">Namespace</span></span><br/>                | <span data-ttu-id="aabbb-313">\\MicrosoftActiveDirectory racine</span><span class="sxs-lookup"><span data-stu-id="aabbb-313">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="aabbb-314">MOF</span><span class="sxs-lookup"><span data-stu-id="aabbb-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aabbb-315"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aabbb-315"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="aabbb-316">DLL</span><span class="sxs-lookup"><span data-stu-id="aabbb-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aabbb-317"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aabbb-317"><dt>Replprov.dll</dt></span></span> </dl> |



 

