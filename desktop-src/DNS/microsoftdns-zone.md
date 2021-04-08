---
title: Classe MicrosoftDNS_Zone
description: La \_ classe de zone MicrosoftDNS décrit une zone DNS. Chaque instance de la \_ classe de zone MicrosoftDNS doit être affectée à un seul serveur DNS. Les zones peuvent être associées à plusieurs instances de \_ classes MicrosoftDNS Domain ou MicrosoftDNS \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone de la classe DNS
- MicrosoftDNS_Zone de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033358"
---
# <a name="microsoftdns_zone-class"></a><span data-ttu-id="74858-107">\_Classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="74858-107">MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="74858-108">Cet article contient des références au terme esclave, un terme que Microsoft n’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="74858-108">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="74858-109">Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.</span><span class="sxs-lookup"><span data-stu-id="74858-109">When the term is removed from the software, we’ll remove it from this article.</span></span>

> [!NOTE]
> <span data-ttu-id="74858-110">Cet article contient des références au terme serveur maître, un terme que Microsoft n’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="74858-110">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="74858-111">Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.</span><span class="sxs-lookup"><span data-stu-id="74858-111">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="74858-112">La classe de **\_ zone MicrosoftDNS** décrit une zone DNS.</span><span class="sxs-lookup"><span data-stu-id="74858-112">The **MicrosoftDNS\_Zone** class describes a DNS Zone.</span></span> <span data-ttu-id="74858-113">Chaque instance de la classe de **\_ zone MicrosoftDNS** doit être affectée à un seul serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="74858-113">Every instance of the **MicrosoftDNS\_Zone** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="74858-114">Les zones peuvent être associées à plusieurs instances de classes [**MicrosoftDNS \_ Domain**](microsoftdns-domain.md) ou [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="74858-114">Zones may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="74858-115">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="74858-115">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="74858-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74858-116">Syntax</span></span>

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a><span data-ttu-id="74858-117">Membres</span><span class="sxs-lookup"><span data-stu-id="74858-117">Members</span></span>

<span data-ttu-id="74858-118">La classe de **\_ zone MicrosoftDNS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="74858-118">The **MicrosoftDNS\_Zone** class has these types of members:</span></span>

-   [<span data-ttu-id="74858-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="74858-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="74858-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="74858-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="74858-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="74858-121">Methods</span></span>

<span data-ttu-id="74858-122">La classe de **\_ zone MicrosoftDNS** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="74858-122">The **MicrosoftDNS\_Zone** class has these methods.</span></span>



| <span data-ttu-id="74858-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="74858-123">Method</span></span>                   | <span data-ttu-id="74858-124">Description</span><span class="sxs-lookup"><span data-stu-id="74858-124">Description</span></span>                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74858-125">**AgeAllRecords**</span><span class="sxs-lookup"><span data-stu-id="74858-125">**AgeAllRecords**</span></span>        | <span data-ttu-id="74858-126">Active l’antériorité pour certains ou tous les enregistrements non NS et non SOA.</span><span class="sxs-lookup"><span data-stu-id="74858-126">Enables aging for some or all non-NS and non-SOA records.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="74858-127">**ChangeZoneType**</span><span class="sxs-lookup"><span data-stu-id="74858-127">**ChangeZoneType**</span></span>       | <span data-ttu-id="74858-128">Modifie les types de zone.</span><span class="sxs-lookup"><span data-stu-id="74858-128">Changes zone types.</span></span> <br/> <span data-ttu-id="74858-129">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-129">Qualifiers: Implemented</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="74858-130">**CreateZone**</span><span class="sxs-lookup"><span data-stu-id="74858-130">**CreateZone**</span></span>           | <span data-ttu-id="74858-131">Crée une nouvelle zone.</span><span class="sxs-lookup"><span data-stu-id="74858-131">Creates a new zone.</span></span> <br/> <span data-ttu-id="74858-132">Qualificateurs : aucun.</span><span class="sxs-lookup"><span data-stu-id="74858-132">Qualifiers: None.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="74858-133">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="74858-133">**ForceRefresh**</span></span>         | <span data-ttu-id="74858-134">Force une mise à jour de la base de données secondaire à partir du serveur DNS maître.</span><span class="sxs-lookup"><span data-stu-id="74858-134">Forces an update of the secondary from the Master DNS Server.</span></span> <br/> <span data-ttu-id="74858-135">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-135">Qualifiers: Implemented</span></span><br/>                                                                                               |
| <span data-ttu-id="74858-136">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="74858-136">**GetDistinguishedName**</span></span> | <span data-ttu-id="74858-137">Obtient le nom unique du service d’annuaire pour la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-137">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="74858-138">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-138">Qualifiers: Implemented</span></span><br/>                                                                                                                 |
| <span data-ttu-id="74858-139">**PauseZone**</span><span class="sxs-lookup"><span data-stu-id="74858-139">**PauseZone**</span></span>            | <span data-ttu-id="74858-140">Suspend la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-140">Pauses the Zone.</span></span> <br/> <span data-ttu-id="74858-141">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-141">Qualifiers: Implemented</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="74858-142">**ReloadZone**</span><span class="sxs-lookup"><span data-stu-id="74858-142">**ReloadZone**</span></span>           | <span data-ttu-id="74858-143">Recharge la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-143">Reloads the Zone.</span></span> <br/> <span data-ttu-id="74858-144">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-144">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="74858-145">**ResetSecondaries**</span><span class="sxs-lookup"><span data-stu-id="74858-145">**ResetSecondaries**</span></span>     | <span data-ttu-id="74858-146">Réinitialise le tableau d’adresses IP secondaire.</span><span class="sxs-lookup"><span data-stu-id="74858-146">Resets the secondary ip address array.</span></span> <br/> <span data-ttu-id="74858-147">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-147">Qualifiers: Implemented</span></span><br/>                                                                                                                      |
| <span data-ttu-id="74858-148">**ResumeZone**</span><span class="sxs-lookup"><span data-stu-id="74858-148">**ResumeZone**</span></span>           | <span data-ttu-id="74858-149">Reprend la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-149">Resumes the Zone.</span></span> <br/> <span data-ttu-id="74858-150">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-150">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="74858-151">**UpdateFromDS**</span><span class="sxs-lookup"><span data-stu-id="74858-151">**UpdateFromDS**</span></span>         | <span data-ttu-id="74858-152">Force une mise à jour de la zone à partir du service d’annuaire (DS).</span><span class="sxs-lookup"><span data-stu-id="74858-152">Forces an update of the Zone from the Directory Service (DS).</span></span> <span data-ttu-id="74858-153">Pour que cette méthode soit valide, le ZoneType doit être égal à 0. la zone doit effectivement être stockée dans le DS.</span><span class="sxs-lookup"><span data-stu-id="74858-153">For this method to be valid, the ZoneType must be 0 the Zone must indeed be stored in the DS.</span></span> <br/> <span data-ttu-id="74858-154">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="74858-154">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="74858-155">**WriteBackZone**</span><span class="sxs-lookup"><span data-stu-id="74858-155">**WriteBackZone**</span></span>        | <span data-ttu-id="74858-156">Enregistre les données de zone dans son fichier de zone.</span><span class="sxs-lookup"><span data-stu-id="74858-156">Saves Zone data to its zone file.</span></span> <br/> <span data-ttu-id="74858-157">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="74858-157">Qualifiers: Implemented, static</span></span><br/>                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="74858-158">Propriétés</span><span class="sxs-lookup"><span data-stu-id="74858-158">Properties</span></span>

<span data-ttu-id="74858-159">La classe de **\_ zone MicrosoftDNS** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="74858-159">The **MicrosoftDNS\_Zone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74858-160">**Cumulé**</span><span class="sxs-lookup"><span data-stu-id="74858-160">**Aging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-161">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-163">Spécifie le comportement de vieillissement et de nettoyage de la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-163">Specifies the aging and scavenging behavior of the zone.</span></span> <span data-ttu-id="74858-164">La valeur zéro indique que le nettoyage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="74858-164">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="74858-165">Lorsque le nettoyage est désactivé, les horodateurs des enregistrements de la zone ne sont pas actualisés et les enregistrements ne sont pas soumis au nettoyage.</span><span class="sxs-lookup"><span data-stu-id="74858-165">When scavenging is disabled, the timestamps of records in the zone are not refreshed, and the records are not subjected to scavenging.</span></span> <span data-ttu-id="74858-166">Lorsque la valeur est définie sur un, les enregistrements sont soumis au nettoyage et leurs horodateurs sont actualisés lorsque le serveur reçoit la requête de mise à jour dynamique pour les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="74858-166">When set to one, records are subjected to scavenging and their timestamps are refreshed when the server receives the dynamic update request for the records.</span></span> <span data-ttu-id="74858-167">Pour les zones intégrées à Active Directory, cette valeur est définie sur la propriété *DefaultAgingState* du serveur DNS sur lequel la zone est créée.</span><span class="sxs-lookup"><span data-stu-id="74858-167">For Active Directory-integrated zones, this value is set to the *DefaultAgingState* property of the DNS Server where the zone is created.</span></span> <span data-ttu-id="74858-168">Pour les zones principales standard, la valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="74858-168">For standard primary zones, the default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="74858-169">**Possède**</span><span class="sxs-lookup"><span data-stu-id="74858-169">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-172">Indique si la zone accepte les demandes de mise à jour dynamique.</span><span class="sxs-lookup"><span data-stu-id="74858-172">Indicates whether the Zone accepts dynamic update requests.</span></span>

</dd> <dt>

<span data-ttu-id="74858-173">**Créé automatiquement**</span><span class="sxs-lookup"><span data-stu-id="74858-173">**AutoCreated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-174">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-176">Indique si la zone est créée de façon autocrée.</span><span class="sxs-lookup"><span data-stu-id="74858-176">Indicates whether the Zone is autocreated.</span></span>

</dd> <dt>

<span data-ttu-id="74858-177">**AvailForScavengeTime**</span><span class="sxs-lookup"><span data-stu-id="74858-177">**AvailForScavengeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-178">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-180">Spécifie l’heure à laquelle le serveur peut tenter de nettoyer la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-180">Specifies the time when the server may attempt scavenging the zone.</span></span> <span data-ttu-id="74858-181">Même si la zone est configurée pour activer le nettoyage, le serveur DNS ne tentera pas de nettoyer cette zone avant ce moment.</span><span class="sxs-lookup"><span data-stu-id="74858-181">Even if the zone is configured to enable scavenging the DNS server will not attempt scavenging this zone until after this moment.</span></span> <span data-ttu-id="74858-182">Cette valeur est définie sur l’heure actuelle plus l’intervalle d’actualisation de la zone chaque fois que la zone est chargée.</span><span class="sxs-lookup"><span data-stu-id="74858-182">This value is set to the current time plus the Refresh Interval of the zone whenever the zone is loaded.</span></span> <span data-ttu-id="74858-183">Ce paramètre est stocké localement et n’est pas répliqué vers d’autres copies de la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-183">This parameter is stored locally, and is not replicated to other copies of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="74858-184">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="74858-184">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="74858-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74858-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-187">Indique le nom du fichier de zone.</span><span class="sxs-lookup"><span data-stu-id="74858-187">Indicates the name of the zone file.</span></span>

</dd> <dt>

<span data-ttu-id="74858-188">**DisableWINSRecordReplication**</span><span class="sxs-lookup"><span data-stu-id="74858-188">**DisableWINSRecordReplication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-189">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-191">Indique si l’enregistrement WINS est répliqué.</span><span class="sxs-lookup"><span data-stu-id="74858-191">Indicates whether the WINS record is replicated.</span></span> <span data-ttu-id="74858-192">Si la valeur est TRUE, la réplication des enregistrements WINS est désactivée.</span><span class="sxs-lookup"><span data-stu-id="74858-192">If set to TRUE, WINS record replication is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="74858-193">**DsIntegrated**</span><span class="sxs-lookup"><span data-stu-id="74858-193">**DsIntegrated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-194">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-196">Spécifie si la zone est intégrée au service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="74858-196">Specifies whether the zone is DS integrated.</span></span>

</dd> <dt>

<span data-ttu-id="74858-197">**ForwarderSlave**</span><span class="sxs-lookup"><span data-stu-id="74858-197">**ForwarderSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-198">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-200">Indique si le DNS utilise la récursivité lors de la résolution des noms pour la zone de transfert spécifiée.</span><span class="sxs-lookup"><span data-stu-id="74858-200">Indicates whether the DNS uses recursion when resolving the names for the specified forward zone.</span></span> <span data-ttu-id="74858-201">Applicable uniquement aux zones de transfert conditionnel.</span><span class="sxs-lookup"><span data-stu-id="74858-201">Applicable to Conditional Forwarding zones only.</span></span>

</dd> <dt>

<span data-ttu-id="74858-202">**ForwarderTimeout**</span><span class="sxs-lookup"><span data-stu-id="74858-202">**ForwarderTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-203">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-205">Indique la durée, en secondes, pendant laquelle un serveur DNS qui transfère une requête pour le nom sous la zone de transfert attend la résolution du redirecteur avant de tenter de résoudre la requête elle-même.</span><span class="sxs-lookup"><span data-stu-id="74858-205">Indicates the time, in seconds, a DNS server forwarding a query for the name under the forward zone waits for resolution from the forwarder before attempting to resolve the query itself.</span></span> <span data-ttu-id="74858-206">Ce paramètre s’applique uniquement aux zones de transfert.</span><span class="sxs-lookup"><span data-stu-id="74858-206">This parameter is applicable to the Forward zones only.</span></span>

</dd> <dt>

<span data-ttu-id="74858-207">**LastSuccessfulSoaCheck**</span><span class="sxs-lookup"><span data-stu-id="74858-207">**LastSuccessfulSoaCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-210">Nombre de secondes depuis le 1er janvier 1970 GMT, depuis la dernière vérification du numéro de série SOA de la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-210">Number of seconds since the beginning of January 1, 1970 GMT, since the SOA serial number for the zone was last checked.</span></span>

</dd> <dt>

<span data-ttu-id="74858-211">**LastSuccessfulXfr**</span><span class="sxs-lookup"><span data-stu-id="74858-211">**LastSuccessfulXfr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-212">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-214">Nombre de secondes depuis le 1er janvier 1970 GMT, depuis que la zone a été transférée pour la dernière fois à partir d’un serveur maître.</span><span class="sxs-lookup"><span data-stu-id="74858-214">Number of seconds since the beginning of January 1, 1970 GMT, since the zone was last transferred from a master server.</span></span>

</dd> <dt>

<span data-ttu-id="74858-215">**LocalMasterServers**</span><span class="sxs-lookup"><span data-stu-id="74858-215">**LocalMasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-216">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74858-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74858-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-218">Adresses IP locales des serveurs DNS maîtres pour cette zone.</span><span class="sxs-lookup"><span data-stu-id="74858-218">Local IP addresses of the master DNS servers for this zone.</span></span> <span data-ttu-id="74858-219">Si cette valeur est définie, ces maîtres définissent le MasterServers trouvé dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74858-219">If set, these masters over-ride the MasterServers found in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="74858-220">**MasterServers**</span><span class="sxs-lookup"><span data-stu-id="74858-220">**MasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-221">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74858-221">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74858-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-223">Adresses IP des serveurs DNS maîtres pour cette zone.</span><span class="sxs-lookup"><span data-stu-id="74858-223">IP addresses of the master DNS servers for this zone.</span></span>

</dd> <dt>

<span data-ttu-id="74858-224">**NoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="74858-224">**NoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-225">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-227">Spécifie l’intervalle de temps entre la dernière mise à jour de l’horodateur d’un enregistrement et le premier moment où l’horodatage peut être actualisé.</span><span class="sxs-lookup"><span data-stu-id="74858-227">Specifies the time interval between the last update of a record's timestamp and the earliest moment when the timestamp can be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="74858-228">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="74858-228">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-229">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-231">Indique si la zone principale notifie les bases de données secondaires de toute modification apportée à sa base de données RR.</span><span class="sxs-lookup"><span data-stu-id="74858-231">Indicates whether the master Zone notifies secondaries of any changes in its RRs database.</span></span> <span data-ttu-id="74858-232">Définissez la valeur 1 pour notifier les secondaires.</span><span class="sxs-lookup"><span data-stu-id="74858-232">Set to 1 to notify secondaries.</span></span>

</dd> <dt>

<span data-ttu-id="74858-233">**NotifyServers**</span><span class="sxs-lookup"><span data-stu-id="74858-233">**NotifyServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-234">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74858-234">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74858-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-236">Tableau de chaînes énumérant les adresses IP des serveurs DNS qui doivent être avertis des modifications apportées à cette zone.</span><span class="sxs-lookup"><span data-stu-id="74858-236">Array of strings enumerating IP addresses of DNS servers to be notified of changes in this zone.</span></span>

</dd> <dt>

<span data-ttu-id="74858-237">**En pause**</span><span class="sxs-lookup"><span data-stu-id="74858-237">**Paused**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-238">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-238">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-240">Indique si la zone est suspendue.</span><span class="sxs-lookup"><span data-stu-id="74858-240">Indicates whether the Zone is paused.</span></span>

</dd> <dt>

<span data-ttu-id="74858-241">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="74858-241">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-242">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-244">Spécifie l’intervalle d’actualisation, pendant lequel les enregistrements avec un horodatage différent de zéro sont censés être actualisés pour rester dans la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-244">Specifies the refresh interval, during which the records with nonzero timestamp are expected to be refreshed to remain in the zone.</span></span> <span data-ttu-id="74858-245">Les enregistrements qui n’ont pas été actualisés par l’expiration de l’intervalle d’actualisation peuvent être supprimés par le nettoyage suivant effectué par un serveur.</span><span class="sxs-lookup"><span data-stu-id="74858-245">Records that have not been refreshed by expiration of the Refresh interval could be removed by the next scavenging performed by a server.</span></span> <span data-ttu-id="74858-246">Cette valeur ne doit jamais être inférieure à la période d’actualisation la plus longue des enregistrements inscrits dans la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-246">This value should never be less than the longest refresh period of the records registered in the zone.</span></span> <span data-ttu-id="74858-247">Les valeurs trop petites peuvent entraîner la suppression d’enregistrements DNS valides.</span><span class="sxs-lookup"><span data-stu-id="74858-247">Values that are too small may lead to removal of valid DNS records.</span></span> <span data-ttu-id="74858-248">les valeurs trop volumineuses prolongent la durée de vie des enregistrements obsolètes.</span><span class="sxs-lookup"><span data-stu-id="74858-248">values that are too large prolong the lifetime of stale records.</span></span> <span data-ttu-id="74858-249">Cette valeur est définie sur la propriété *DefaultRefreshInterval,* du serveur DNS sur lequel la zone est créée.</span><span class="sxs-lookup"><span data-stu-id="74858-249">This value is set to the *DefaultRefreshInterval* property of the DNS server where the zone is created.</span></span>

</dd> <dt>

<span data-ttu-id="74858-250">**TVA**</span><span class="sxs-lookup"><span data-stu-id="74858-250">**Reverse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-251">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-253">Indique si la zone est inversée (TRUE) ou Forward (FALSe).</span><span class="sxs-lookup"><span data-stu-id="74858-253">Indicates whether the Zone is reverse (TRUE) or forward (FALSE).</span></span>

</dd> <dt>

<span data-ttu-id="74858-254">**ScavengeServers**</span><span class="sxs-lookup"><span data-stu-id="74858-254">**ScavengeServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-255">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74858-255">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74858-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-257">Tableau de chaînes qui énumère la liste des adresses IP des serveurs DNS autorisés à effectuer le nettoyage des enregistrements obsolètes de cette zone.</span><span class="sxs-lookup"><span data-stu-id="74858-257">Array of strings that enumerates the list of IP addresses of DNS servers that are allowed to perform scavenging of stale records of this zone.</span></span> <span data-ttu-id="74858-258">Si la liste n’est pas spécifiée, tout serveur DNS principal faisant autorité pour la zone est autorisé à nettoyer la zone lorsque d’autres conditions préalables sont remplies.</span><span class="sxs-lookup"><span data-stu-id="74858-258">If the list is not specified, any primary DNS server authoritative for the zone is allowed to scavenge the zone when other prerequisites are met.</span></span>

</dd> <dt>

<span data-ttu-id="74858-259">**SecondaryServers**</span><span class="sxs-lookup"><span data-stu-id="74858-259">**SecondaryServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-260">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="74858-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74858-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-262">Tableau de chaînes énumérant les adresses IP des serveurs DNS autorisés à recevoir cette zone via la réplication de zone.</span><span class="sxs-lookup"><span data-stu-id="74858-262">Array of strings enumerating IP addresses of DNS servers allowed to receive this zone through zone replication.</span></span>

</dd> <dt>

<span data-ttu-id="74858-263">**SecureSecondaries**</span><span class="sxs-lookup"><span data-stu-id="74858-263">**SecureSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-264">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-266">Indique si le transfert de zone est autorisé uniquement aux serveurs secondaires désignés.</span><span class="sxs-lookup"><span data-stu-id="74858-266">Indicates whether zone transfer is allowed to designated secondaries only.</span></span> <span data-ttu-id="74858-267">Les serveurs secondaires désignés sont des serveurs DNS dont les adresses IP sont répertoriées dans SecondariesIPAddressesArray.</span><span class="sxs-lookup"><span data-stu-id="74858-267">Designated secondaries are DNS Servers whose IP addresses are listed in SecondariesIPAddressesArray.</span></span>

</dd> <dt>

<span data-ttu-id="74858-268">**Arrêter**</span><span class="sxs-lookup"><span data-stu-id="74858-268">**Shutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-269">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-271">Indique si la copie de la zone a expiré.</span><span class="sxs-lookup"><span data-stu-id="74858-271">Indicates whether the copy of the Zone is expired.</span></span> <span data-ttu-id="74858-272">Si la valeur est TRUE, la zone est expirée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="74858-272">If TRUE, the Zone is expired, or shut down.</span></span>

</dd> <dt>

<span data-ttu-id="74858-273">**UseNBStat**</span><span class="sxs-lookup"><span data-stu-id="74858-273">**UseNBStat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-274">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-276">Cette valeur booléenne indique si la zone utilise la recherche inversée NBStat.</span><span class="sxs-lookup"><span data-stu-id="74858-276">This Boolean indicates whether the Zone uses NBStat reverse lookup.</span></span>

</dd> <dt>

<span data-ttu-id="74858-277">**UseWins**</span><span class="sxs-lookup"><span data-stu-id="74858-277">**UseWins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-278">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74858-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74858-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-280">Indique si la zone utilise les recherches WINS.</span><span class="sxs-lookup"><span data-stu-id="74858-280">Indicates whether the Zone uses WINS look up.</span></span>

</dd> <dt>

<span data-ttu-id="74858-281">**ZoneType**</span><span class="sxs-lookup"><span data-stu-id="74858-281">**ZoneType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74858-282">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74858-282">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74858-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="74858-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74858-284">Indique le type de la zone.</span><span class="sxs-lookup"><span data-stu-id="74858-284">Indicates the type of the Zone.</span></span> <span data-ttu-id="74858-285">Les valeurs autorisées sont :</span><span class="sxs-lookup"><span data-stu-id="74858-285">Valid values are:</span></span>

-   <span data-ttu-id="74858-286">Intégration DS</span><span class="sxs-lookup"><span data-stu-id="74858-286">DS integrated</span></span>
-   <span data-ttu-id="74858-287">Principal</span><span class="sxs-lookup"><span data-stu-id="74858-287">Primary</span></span>
-   <span data-ttu-id="74858-288">Secondary</span><span class="sxs-lookup"><span data-stu-id="74858-288">Secondary</span></span>

<span data-ttu-id="74858-289">\* \* Windows Server 2003 : \* \*</span><span class="sxs-lookup"><span data-stu-id="74858-289">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="74858-290">Valeurs supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="74858-290">Additional values:</span></span>

-   <span data-ttu-id="74858-291">Cache</span><span class="sxs-lookup"><span data-stu-id="74858-291">Cache</span></span>
-   <span data-ttu-id="74858-292">Talon</span><span class="sxs-lookup"><span data-stu-id="74858-292">Stub</span></span>
-   <span data-ttu-id="74858-293">Redirecteur</span><span class="sxs-lookup"><span data-stu-id="74858-293">Forwarder</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74858-294">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74858-294">Requirements</span></span>



| <span data-ttu-id="74858-295">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74858-295">Requirement</span></span> | <span data-ttu-id="74858-296">Valeur</span><span class="sxs-lookup"><span data-stu-id="74858-296">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74858-297">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74858-297">Minimum supported client</span></span><br/> | <span data-ttu-id="74858-298">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="74858-298">None supported</span></span><br/>                                                              |
| <span data-ttu-id="74858-299">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74858-299">Minimum supported server</span></span><br/> | <span data-ttu-id="74858-300">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74858-300">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="74858-301">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="74858-301">Namespace</span></span><br/>                | <span data-ttu-id="74858-302">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="74858-302">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="74858-303">MOF</span><span class="sxs-lookup"><span data-stu-id="74858-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74858-304"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74858-304"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74858-305">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74858-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74858-306">**\_Domaine MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-306">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="74858-307">**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-307">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="74858-308">**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-308">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="74858-309">**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-309">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="74858-310">**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-310">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="74858-311">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-311">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="74858-312">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-312">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="74858-313">**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-313">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="74858-314">**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-314">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="74858-315">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-315">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="74858-316">**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-316">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="74858-317">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="74858-317">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





