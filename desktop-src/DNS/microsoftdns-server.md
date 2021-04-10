---
title: Classe MicrosoftDNS_Server
description: La \_ classe de serveur MicrosoftDNS décrit un serveur DNS. Chaque instance de cette classe peut être associée à une instance du \_ cache MicrosoftDNS, une instance de MicrosoftDNS \_ RootHints et plusieurs instances de la \_ zone MicrosoftDNS.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- MicrosoftDNS_Server de la classe DNS
- MicrosoftDNS_Server de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941737"
---
# <a name="microsoftdns_server-class"></a><span data-ttu-id="4f0f3-106">\_Classe de serveur MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="4f0f3-106">MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="4f0f3-107">La classe de **\_ serveur MicrosoftDNS** décrit un serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-107">The **MicrosoftDNS\_Server** class describes a DNS Server.</span></span> <span data-ttu-id="4f0f3-108">Chaque instance de cette classe peut être associée à une instance du [**\_ cache MicrosoftDNS**](microsoftdns-cache.md), une instance de [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)et plusieurs instances de la [**\_ zone MicrosoftDNS**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-108">Every instance of this class may be associated with one instance of [**MicrosoftDNS\_Cache**](microsoftdns-cache.md), one instance of [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md), and multiple instances of [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

<span data-ttu-id="4f0f3-109">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0f3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f0f3-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a><span data-ttu-id="4f0f3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4f0f3-111">Members</span></span>

<span data-ttu-id="4f0f3-112">La classe de **\_ serveur MicrosoftDNS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f0f3-112">The **MicrosoftDNS\_Server** class has these types of members:</span></span>

-   [<span data-ttu-id="4f0f3-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f0f3-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="4f0f3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f0f3-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4f0f3-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f0f3-115">Methods</span></span>

<span data-ttu-id="4f0f3-116">La classe de **\_ serveur MicrosoftDNS** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-116">The **MicrosoftDNS\_Server** class has these methods.</span></span>



| <span data-ttu-id="4f0f3-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="4f0f3-117">Method</span></span>                   | <span data-ttu-id="4f0f3-118">Description</span><span class="sxs-lookup"><span data-stu-id="4f0f3-118">Description</span></span>                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="4f0f3-119">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-119">**GetDistinguishedName**</span></span> | <span data-ttu-id="4f0f3-120">Récupère le nom unique DNS de la zone.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-120">Retrieves DNS distinguished name for the zone.</span></span><br/>                        |
| <span data-ttu-id="4f0f3-121">**StartScavenging**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-121">**StartScavenging**</span></span>      | <span data-ttu-id="4f0f3-122">Démarre le nettoyage des enregistrements obsolètes dans les zones soumises au nettoyage.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-122">Starts scavenging stale records in the zones subjected to scavenging.</span></span><br/> |
| <span data-ttu-id="4f0f3-123">**StartService**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-123">**StartService**</span></span>         | <span data-ttu-id="4f0f3-124">Démarre le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-124">Starts the DNS Server.</span></span><br/>                                                |
| <span data-ttu-id="4f0f3-125">**StopService**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-125">**StopService**</span></span>          | <span data-ttu-id="4f0f3-126">Arrête le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-126">Stops the DNS Server.</span></span><br/>                                                 |



 

### <a name="properties"></a><span data-ttu-id="4f0f3-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f0f3-127">Properties</span></span>

<span data-ttu-id="4f0f3-128">La classe de **\_ serveur MicrosoftDNS** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-128">The **MicrosoftDNS\_Server** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f0f3-129">**AddressAnswerLimit**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-129">**AddressAnswerLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-132">Nombre maximal d’enregistrements d’hôte renvoyés en réponse à une demande d’adresse.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-132">Maximum number of host records returned in response to an address request.</span></span> <span data-ttu-id="4f0f3-133">Les valeurs comprises entre 5 et 28 sont valides.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-133">Values between 5 and 28 are valid.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-134">**Possède**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-134">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-137">Spécifie si le serveur DNS accepte les demandes de mise à jour dynamiques.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-137">Specifies whether the DNS Server accepts dynamic update requests.</span></span> <span data-ttu-id="4f0f3-138">Les valeurs valides sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-138">Valid values are as shown in the following table.</span></span>



| <span data-ttu-id="4f0f3-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-139">Value</span></span>                                                                                                | <span data-ttu-id="4f0f3-140">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-140">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4f0f3-141"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-141"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-142">Aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-142">No Restrictions.</span></span><br/>                                                                           |
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-143"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-143"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-144">N’autorise pas les mises à jour dynamiques des enregistrements SOA.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-144">Does not allow dynamic updates of SOA records.</span></span><br/>                                             |
| <span id="2"></span><dl> <span data-ttu-id="4f0f3-145"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-145"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-146">N’autorise pas les mises à jour dynamiques des enregistrements NS à la racine de la zone.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-146">Does not allow dynamic updates of NS records at the zone root.</span></span><br/>                             |
| <span id="4"></span><dl> <span data-ttu-id="4f0f3-147"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-147"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-148">N’autorise pas les mises à jour dynamiques des enregistrements NS qui ne se trouvent pas à la racine de la zone (enregistrements NS de délégation).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-148">Does not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span><br/> |



 

<span data-ttu-id="4f0f3-149">Additionnez ces valeurs pour déterminer la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-149">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-150">**AutoCacheUpdate**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-150">**AutoCacheUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-151">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-153">Indique si le serveur DNS tente de mettre à jour ses entrées de cache en utilisant les données des serveurs racines.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-153">Indicates whether the DNS Server attempts to update its cache entries using data from root servers.</span></span> <span data-ttu-id="4f0f3-154">Lorsqu’un serveur DNS démarre, il a besoin d’une liste de NS « indicateurs » du serveur racine et d’enregistrements A pour les serveurs historiquement appelés « fichier cache ».</span><span class="sxs-lookup"><span data-stu-id="4f0f3-154">When a DNS Server boots, it needs a list of root server 'hints' NS and A records for the servers historically called the cache file.</span></span> <span data-ttu-id="4f0f3-155">Les serveurs DNS Microsoft ont une fonctionnalité qui leur permet de tenter d’écrire un nouveau fichier cache en fonction des réponses des serveurs racine.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-155">Microsoft DNS Servers have a feature that enables them to attempt to write back a new cache file based on the responses from root servers.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-156">**AutoConfigFileZones**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-156">**AutoConfigFileZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-159">Indique quelles zones principales standard faisant autorité pour le nom du serveur DNS doivent être mises à jour lorsque le serveur de noms change.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-159">Indicates which standard primary zones that are authoritative for the name of the DNS Server must be updated when the name server changes.</span></span> <span data-ttu-id="4f0f3-160">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f0f3-160">Valid values are as follows:</span></span>



| <span data-ttu-id="4f0f3-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-161">Value</span></span>                                                                                                | <span data-ttu-id="4f0f3-162">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-162">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4f0f3-163"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-163"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-164">Aucun</span><span class="sxs-lookup"><span data-stu-id="4f0f3-164">None.</span></span><br/>                                           |
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-165"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-165"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-166">Uniquement les serveurs qui autorisent les mises à jour dynamiques.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-166">Only servers that allow dynamic updates.</span></span><br/>        |
| <span id="2"></span><dl> <span data-ttu-id="4f0f3-167"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-167"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-168">Seuls les serveurs qui n’autorisent pas les mises à jour dynamiques.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-168">Only servers that do not allow dynamic updates.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="4f0f3-169"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-169"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-170">Tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-170">All servers.</span></span><br/>                                    |



 

<span data-ttu-id="4f0f3-171">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-171">The default value is 1.</span></span>

<span data-ttu-id="4f0f3-172">\* \* Windows Server 2003 : \* \*</span><span class="sxs-lookup"><span data-stu-id="4f0f3-172">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="4f0f3-173">Le nombre 3 représente tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-173">The number 3 represents All servers.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-174">**BindSecondaries**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-174">**BindSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-175">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-176">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-176">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-177">Détermine le format de message AXFR lors de l’envoi à des serveurs secondaires de serveur DNS non-Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-177">Determines the AXFR message format when sending to non-Microsoft DNS Server secondaries.</span></span> <span data-ttu-id="4f0f3-178">Lorsque la valeur est TRUE, le serveur DNS envoie les transferts vers des serveurs secondaires DNS non-Microsoft au format non compressé.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-178">When set to TRUE, the DNS Server sends transfers to non-Microsoft DNS Server secondaries in the uncompressed format.</span></span> <span data-ttu-id="4f0f3-179">Si la valeur est FALSe, tous les transferts sont envoyés dans le format rapide.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-179">When FALSE, all transfers are sent in the fast format.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-180">**BootMethod**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-180">**BootMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-181">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-183">Méthode d’initialisation pour le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-183">Initialization method for the DNS Server.</span></span> <span data-ttu-id="4f0f3-184">Le tableau ci-dessous répertorie les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-184">Valid values are shown in the following table.</span></span>



| <span data-ttu-id="4f0f3-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-185">Value</span></span>                                                                                                | <span data-ttu-id="4f0f3-186">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-186">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4f0f3-187"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-187"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-188">Non initialisé.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-188">Uninitialized.</span></span><br/>                    |
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-189"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-189"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-190">Démarrez à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-190">Boot from file.</span></span><br/>                   |
| <span id="2"></span><dl> <span data-ttu-id="4f0f3-191"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-191"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-192">Démarrage à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-192">Boot from registry.</span></span><br/>               |
| <span id="3"></span><dl> <span data-ttu-id="4f0f3-193"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-193"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-194">Démarrez à partir du répertoire et du Registre.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-194">Boot from directory and registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4f0f3-195">**DefaultAgingState**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-195">**DefaultAgingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-197">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-198">Valeur **ScavengingInterval** par défaut définie pour toutes les zones intégrées à Active Directory créées sur ce serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-198">Default **ScavengingInterval** value set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="4f0f3-199">La valeur par défaut est zéro, ce qui indique que le nettoyage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-199">The default value is zero, indicating scavenging is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-200">**DefaultNoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-200">**DefaultNoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-202">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-203">Intervalle de non-actualisation, en heures, défini pour toutes les zones intégrées à l’Active Directory créées sur ce serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-203">No-refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="4f0f3-204">La valeur par défaut est 168 heures (sept jours).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-204">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-205">**DefaultRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-205">**DefaultRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-206">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-207">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-207">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-208">Intervalle d’actualisation, en heures, défini pour toutes les zones intégrées à l’Active Directory créées sur ce serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-208">Refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="4f0f3-209">La valeur par défaut est 168 heures (sept jours).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-209">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-210">**DisableAutoReverseZones**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-210">**DisableAutoReverseZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-211">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-212">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-213">Indique si le serveur DNS crée automatiquement des zones de recherche inversée standard.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-213">Indicates whether the DNS Server automatically creates standard reverse look up zones.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-214">**DisjointNets**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-214">**DisjointNets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-215">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-216">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-217">Indique si la liaison de port par défaut pour un socket utilisé pour envoyer des requêtes à des serveurs DNS distants peut être remplacée.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-217">Indicates whether the default port binding for a socket used to send queries to remote DNS Servers can be overridden.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-218">**DsAvailable**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-218">**DsAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-221">Indique s’il existe un DS disponible sur le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-221">Indicates whether there is an available DS on the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-222">**DsPollingInterval**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-222">**DsPollingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-223">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-224">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-224">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-225">Intervalle, en secondes, pour interroger les zones DS intégrées.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-225">Interval, in seconds, to poll the DS-integrated zones.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-226">**DsTombstoneInterval**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-226">**DsTombstoneInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-227">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-228">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-229">Durée de vie des enregistrements désactivés dans les zones intégrées du service d’annuaire, en secondes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-229">Lifetime of tombstoned records in Directory Service integrated zones, expressed in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-230">**EDnsCacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-230">**EDnsCacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-231">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-231">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-233">Durée de vie, en secondes, des informations mises en cache qui décrivent la version d’EDNS prise en charge par d’autres serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-233">Lifetime, in seconds, of the cached information describing the EDNS version supported by other DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-234">**EnableDirectoryPartitions**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-234">**EnableDirectoryPartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-235">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-236">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-237">Spécifie si la prise en charge des partitions d’annuaire d’applications est activée sur le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-237">Specifies whether support for application directory partitions is enabled on the DNS Server.</span></span>

<span data-ttu-id="4f0f3-238">\* \* Windows Server 2003 : \* \*</span><span class="sxs-lookup"><span data-stu-id="4f0f3-238">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="4f0f3-239">Cette méthode est nommée EnableDirectoryPartitionSupport.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-239">This method is named EnableDirectoryPartitionSupport.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-240">**EnableDnsSec**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-240">**EnableDnsSec**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-241">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-242">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-243">Spécifie si le serveur DNS comprend des enregistrements de ressource spécifiques à DNSSEC, KEY, SIG et NXT dans une réponse, conformément au tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="4f0f3-243">Specifies whether the DNS Server includes DNSSEC-specific RRs, KEY, SIG, and NXT in a response, per the following table:</span></span>



| <span data-ttu-id="4f0f3-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-244">Value</span></span>                                                                                                | <span data-ttu-id="4f0f3-245">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-245">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4f0f3-246"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-246"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-247">Aucun enregistrement DNSSEC n’est inclus dans la réponse, sauf si la requête a demandé un jeu d’enregistrements de ressources du type d’enregistrement DNSSEC.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-247">No DNSSEC records are included in the response unless the query requested a resource record set of the DNSSEC record type.</span></span><br/>          |
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-248"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-248"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-249">Les enregistrements DNSSEC sont inclus dans la réponse conformément à la norme RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-249">DNSSEC records are included in the response according to RFC 2535.</span></span><br/>                                                                  |
| <span id="2"></span><dl> <span data-ttu-id="4f0f3-250"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-250"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-251">Les enregistrements DNSSEC sont inclus dans une réponse uniquement si la requête du client d’origine contenait l’enregistrement de ressource OPT conformément à la norme RFC 2671</span><span class="sxs-lookup"><span data-stu-id="4f0f3-251">DNSSEC records are included in a response only if the original client query contained the OPT resource record according to RFC 2671</span></span><br/> |



 

<span data-ttu-id="4f0f3-252">Si une requête demande un jeu d’enregistrements de ressources du type DNSSEC, le serveur DNS répond toujours avec ces enregistrements, s’ils sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-252">If a query requests a resource record set of the DNSSEC type, the DNS Server always responds with such records, if available.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-253">**EnableEDnsProbes**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-253">**EnableEDnsProbes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-254">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-254">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-255">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-255">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-256">Spécifie le comportement du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-256">Specifies the behavior of the DNS Server.</span></span> <span data-ttu-id="4f0f3-257">Si la valeur est TRUE, le serveur DNS répond toujours avec les enregistrements de ressource OPT conformément à la RFC 2671, sauf si le serveur distant a indiqué qu’il ne prend pas en charge EDNS dans un échange antérieur.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-257">When TRUE, the DNS Server always responds with OPT resource records according to RFC 2671, unless the remote server has indicated it does not support EDNS in a prior exchange.</span></span> <span data-ttu-id="4f0f3-258">Si la valeur est FALSe, le serveur DNS répond aux requêtes avec OPTs uniquement si les OPTs sont envoyées dans la requête d’origine.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-258">If FALSE, the DNS Server responds to queries with OPTs only if OPTs are sent in the original query.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-259">**EventLogLevel**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-259">**EventLogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-260">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-260">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-261">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-261">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-262">Indique les événements que le serveur DNS enregistre dans le journal système observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-262">Indicates which events the DNS Server records in the Event Viewer system log.</span></span> <span data-ttu-id="4f0f3-263">Les valeurs suivantes sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-263">The following values are used.</span></span>



| <span data-ttu-id="4f0f3-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-264">Value</span></span>                                                                                                | <span data-ttu-id="4f0f3-265">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-265">Meaning</span></span>                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4f0f3-266"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-266"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-267">Aucun</span><span class="sxs-lookup"><span data-stu-id="4f0f3-267">None.</span></span><br/>                         |
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-268"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-268"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-269">Consigner uniquement les erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-269">Log only errors.</span></span><br/>              |
| <span id="2"></span><dl> <span data-ttu-id="4f0f3-270"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-270"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-271">Consigne uniquement les avertissements et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-271">Log only warnings and errors.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="4f0f3-272"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-272"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-273">Consigner tous les événements.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-273">Log all events.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="4f0f3-274">**ForwardDelegations**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-274">**ForwardDelegations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-275">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-276">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-276">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-277">Spécifie si les requêtes vers les sous-zones déléguées sont transférées.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-277">Specifies whether queries to delegated sub-zones are forwarded.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-278">**Redirecteurs**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-278">**Forwarders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-279">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-279">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-280">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-280">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-281">Énumère la liste des adresses IP des redirecteurs sur lesquels le serveur DNS transfère des requêtes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-281">Enumerates the list of IP addresses of Forwarders to which the DNS Server forwards queries.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-282">**ForwardingTimeout**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-282">**ForwardingTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-284">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-284">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-285">Durée, en secondes, pendant laquelle un serveur DNS qui transfère une requête attend la résolution du [*redirecteur*](f-gly.md) avant de tenter de résoudre lui-même la requête.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-285">Time, in seconds, a DNS Server forwarding a query will wait for resolution from the [*forwarder*](f-gly.md) before attempting to resolve the query itself.</span></span>

<span data-ttu-id="4f0f3-286">Cette valeur n’a pas de sens si le serveur de transfert n’est pas configuré pour utiliser la récursivité.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-286">This value is meaningless if the forwarding server is not set to use recursion.</span></span> <span data-ttu-id="4f0f3-287">Pour déterminer cela, vérifiez la propriété booléenne IsSlave.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-287">To determine this, check the IsSlave Boolean property.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-288">**IsSlave**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-288">**IsSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-289">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-290">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-291">**True** si le serveur DNS n’utilise pas la récursivité lorsque la résolution de nom par le biais des redirecteurs échoue.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-291">**TRUE** if the DNS server does not use recursion when name-resolution through forwarders fails.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-292">**ListenAddresses**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-292">**ListenAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-293">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-294">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-294">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-295">Énumère la liste des adresses IP sur lesquelles le serveur DNS peut recevoir des requêtes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-295">Enumerates the list of IP addresses on which the DNS Server can receive queries.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-296">**LocalNetPriority**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-296">**LocalNetPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-297">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-298">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-298">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-299">Indique si le serveur DNS donne la priorité à l’adresse réseau locale lors du retour d’enregistrements A.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-299">Indicates whether the DNS Server gives priority to the local net address when returning A records.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-300">**LogFileMaxSize**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-300">**LogFileMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-301">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-302">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-302">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-303">Taille, en octets, du journal de débogage du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-303">Size of the DNS Server debug log, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-304">**LogFilePath**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-304">**LogFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-306">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-306">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-307">Nom de fichier et chemin d’accès du journal de débogage du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-307">File name and path for the DNS Server debug log.</span></span> <span data-ttu-id="4f0f3-308">La valeur par défaut est% System32% DNS DNS. \\ \\ log.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-308">Default is %system32%\\dns\\dns.log.</span></span> <span data-ttu-id="4f0f3-309">Les chemins d’accès relatifs sont relatifs à% systemroot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-309">Relative paths are relative to %Systemroot%\\System32.</span></span> <span data-ttu-id="4f0f3-310">Les chemins d’accès absolus peuvent être utilisés, mais les chemins d’accès UNC ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-310">Absolute paths may be used, but UNC paths are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-311">**LogIPFilterList**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-311">**LogIPFilterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-312">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-312">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-313">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-313">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-314">Liste des adresses IP utilisées pour filtrer les événements DNS écrits dans le journal de débogage.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-314">List of IP addresses used to filter DNS events written to the debug log.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-315">**LogLevel**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-315">**LogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-316">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-317">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-317">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-318">Indique les stratégies qui sont activées dans le journal système observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-318">Indicates which policies are activated in the Event Viewer system log.</span></span>

<span data-ttu-id="4f0f3-319">Doit être défini sur des valeurs spécifiques en fonction de l’algorithme suivant : chaque stratégie (à activer dans le journal système observateur d’événements) reçoit une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-319">Should be set to specific values based on the following algorithm: Every policy (to be activated in the Event Viewer system log) is assigned a specific value.</span></span>



| <span data-ttu-id="4f0f3-320">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-320">Value</span></span>                                                                                                                  | <span data-ttu-id="4f0f3-321">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-321">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-322"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-322"><dt>**1**</dt></span></span> </dl>                   | <span data-ttu-id="4f0f3-323">Demande.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-323">Query.</span></span><br/>                                   |
| <span id="16"></span><dl> <span data-ttu-id="4f0f3-324"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-324"><dt>**16**</dt></span></span> </dl>                 | <span data-ttu-id="4f0f3-325">Indiquer.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-325">Notify.</span></span><br/>                                  |
| <span id="32"></span><dl> <span data-ttu-id="4f0f3-326"><dt>**32**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-326"><dt>**32**</dt></span></span> </dl>                 | <span data-ttu-id="4f0f3-327">Mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-327">Update.</span></span><br/>                                  |
| <span id="254"></span><dl> <span data-ttu-id="4f0f3-328"><dt>**254**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-328"><dt>**254**</dt></span></span> </dl>               | <span data-ttu-id="4f0f3-329">Transactions qui ne sont pas des requêtes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-329">Nonquery transactions.</span></span><br/>                   |
| <span id="256"></span><dl> <span data-ttu-id="4f0f3-330"><dt>**256**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-330"><dt>**256**</dt></span></span> </dl>               | <span data-ttu-id="4f0f3-331">Questions.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-331">Questions.</span></span><br/>                               |
| <span id="512"></span><dl> <span data-ttu-id="4f0f3-332"><dt>**512**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-332"><dt>**512**</dt></span></span> </dl>               | <span data-ttu-id="4f0f3-333">Forum.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-333">Answers.</span></span><br/>                                 |
| <span id="4096"></span><dl> <span data-ttu-id="4f0f3-334"><dt>**4096**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-334"><dt>**4096**</dt></span></span> </dl>             | <span data-ttu-id="4f0f3-335">Envoi.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-335">Send.</span></span><br/>                                    |
| <span id="8192"></span><dl> <span data-ttu-id="4f0f3-336"><dt>**8192**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-336"><dt>**8192**</dt></span></span> </dl>             | <span data-ttu-id="4f0f3-337">Réception.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-337">Receive.</span></span><br/>                                 |
| <span id="16384"></span><dl> <span data-ttu-id="4f0f3-338"><dt>**16384**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-338"><dt>**16384**</dt></span></span> </dl>           | <span data-ttu-id="4f0f3-339">Passerelle.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-339">UDP.</span></span><br/>                                     |
| <span id="32768"></span><dl> <span data-ttu-id="4f0f3-340"><dt>**32768**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-340"><dt>**32768**</dt></span></span> </dl>           | <span data-ttu-id="4f0f3-341">TCP.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-341">TCP.</span></span><br/>                                     |
| <span id="65535"></span><dl> <span data-ttu-id="4f0f3-342"><dt>**65535**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-342"><dt>**65535**</dt></span></span> </dl>           | <span data-ttu-id="4f0f3-343">Tous les paquets.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-343">All packets.</span></span><br/>                             |
| <span id="65536"></span><dl> <span data-ttu-id="4f0f3-344"><dt>**65536**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-344"><dt>**65536**</dt></span></span> </dl>           | <span data-ttu-id="4f0f3-345">Transaction d’écriture du service d’annuaire NT.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-345">NT Directory Service write transaction.</span></span><br/>  |
| <span id="131072"></span><dl> <span data-ttu-id="4f0f3-346"><dt>**131 072**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-346"><dt>**131072**</dt></span></span> </dl>         | <span data-ttu-id="4f0f3-347">Transaction de mise à jour du service d’annuaire NT.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-347">NT Directory Service update transaction.</span></span><br/> |
| <span id="16777216"></span><dl> <span data-ttu-id="4f0f3-348"><dt>**16777216**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-348"><dt>**16777216**</dt></span></span> </dl>     | <span data-ttu-id="4f0f3-349">Paquets complets.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-349">Full packets.</span></span><br/>                            |
| <span id="2147483648"></span><dl> <span data-ttu-id="4f0f3-350"><dt>**2147483648**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-350"><dt>**2147483648**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-351">Écrire.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-351">Write through.</span></span><br/>                           |



 

<span data-ttu-id="4f0f3-352">La somme des valeurs correspondant à toutes les stratégies à activer est indiquée dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-352">The sum of the values corresponding to all the policies to be activated is indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-353">**LooseWildcarding**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-353">**LooseWildcarding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-354">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-355">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-355">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-356">Indique si le serveur DNS effectue un caractère générique libre.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-356">Indicates whether the DNS Server performs loose wildcarding.</span></span> <span data-ttu-id="4f0f3-357">Si la valeur est non définie ou égale à zéro, le serveur suit le comportement de caractères génériques spécifié dans la RFC DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-357">If undefined or zero, the server follows the wildcarding behavior specified in the DNS RFC.</span></span> <span data-ttu-id="4f0f3-358">Dans ce cas, un administrateur est invité à inclure les enregistrements MX pour tous les hôtes qui ne peuvent pas recevoir de messages.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-358">In this case, an administrator is advised to include MX records for all hosts incapable of receiving mail.</span></span> <span data-ttu-id="4f0f3-359">Si la valeur est différente de zéro, le serveur recherche le nœud générique le plus proche. dans ce cas, un administrateur doit placer les enregistrements MX à la racine de la zone et dans un nœud générique (« \* ») directement sous la racine de la zone.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-359">If nonzero, the server seeks the closest wildcard node; in this case, an administrator should put MX records at the zone root and in a wildcard node ('\*') directly below the zone root.</span></span> <span data-ttu-id="4f0f3-360">En outre, les administrateurs doivent placer les enregistrements MX à référence automatique sur les hôtes qui reçoivent leur propre courrier.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-360">Also, administrators should put self-referencing MX records on hosts that receive their own mail.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-361">**MaxCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-361">**MaxCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-362">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-363">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-363">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-364">Durée maximale, en secondes, pendant laquelle l’enregistrement d’une requête de nom récursif peut rester dans le cache du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-364">Maximum time, in seconds, the record of a recursive name query may remain in the DNS Server cache.</span></span> <span data-ttu-id="4f0f3-365">Le serveur DNS supprime les enregistrements du cache lorsque la valeur de cette entrée expire, même si la valeur du champ TTL de l’enregistrement est supérieure.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-365">The DNS Server deletes records from the cache when the value of this entry expires, even if the value of the TTL field in the record is greater.</span></span>

<span data-ttu-id="4f0f3-366">La valeur par défaut de cette propriété est 86 400 secondes (1 jour).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-366">The default value of this property is 86,400 seconds (1 day).</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-367">**MaxNegativeCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-367">**MaxNegativeCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-368">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-369">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-369">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-370">Durée maximale, en secondes, qu’une erreur de nom d’une requête récursive peut rester dans le cache du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-370">Maximum time, in seconds, a name error result from a recursive query may remain in the DNS Server cache.</span></span> <span data-ttu-id="4f0f3-371">DNS supprime les enregistrements du cache lorsque ce minuteur expire, même si le champ TTL est supérieur.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-371">DNS deletes records from the cache when this timer expires, even if the TTL field is greater.</span></span> <span data-ttu-id="4f0f3-372">La valeur par défaut est 86 400 (un jour).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-372">Default value is 86,400 (one day).</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-373">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f0f3-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-376">Nom de domaine complet (FQDN) ou adresse IP du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-376">Fully qualified domain name (FQDN) or IP address of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-377">**NameCheckFlag**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-377">**NameCheckFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-378">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-379">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-379">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-380">Indique l’ensemble de caractères éligibles à utiliser dans les noms DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-380">Indicates the set of eligible characters to be used in DNS names.</span></span> <span data-ttu-id="4f0f3-381">Les valeurs suivantes sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-381">The following values are used.</span></span>



| <span data-ttu-id="4f0f3-382">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-382">Value</span></span>                                                                                                | <span data-ttu-id="4f0f3-383">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-383">Meaning</span></span>                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4f0f3-384"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-384"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-385">RFC strict (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f0f3-385">Strict RFC (ANSI)</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-386"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-386"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-387">Non RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f0f3-387">Non RFC (ANSI)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="4f0f3-388"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-388"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-389">Multioctet (UTF8)</span><span class="sxs-lookup"><span data-stu-id="4f0f3-389">Multibyte (UTF8)</span></span><br/>  |



 

<span data-ttu-id="4f0f3-390">\* \* Windows Server 2003 : \* \*</span><span class="sxs-lookup"><span data-stu-id="4f0f3-390">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="4f0f3-391">La valeur « 2 » indique « any ».</span><span class="sxs-lookup"><span data-stu-id="4f0f3-391">A value of "2" indicates "Any."</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-392">**NoRecursion**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-392">**NoRecursion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-393">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-393">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-394">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-394">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-395">Indique si le serveur DNS effectue des recherches récursives.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-395">Indicates whether the DNS Server performs recursive look ups.</span></span> <span data-ttu-id="4f0f3-396">TRUE indique que les recherches récursives ne sont pas effectuées.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-396">TRUE indicates recursive look ups are not performed.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-397">**RecursionRetry**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-397">**RecursionRetry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-398">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-399">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-399">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-400">Secondes écoulées avant une nouvelle tentative de recherche récursive.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-400">Elapsed seconds before retrying a recursive look up.</span></span> <span data-ttu-id="4f0f3-401">Si la propriété est non définie ou zéro, les nouvelles tentatives sont effectuées au bout de trois secondes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-401">If the property is undefined or zero, retries are made after three seconds.</span></span> <span data-ttu-id="4f0f3-402">Les utilisateurs sont déconseillés de modifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-402">Users are discouraged from altering this property.</span></span> <span data-ttu-id="4f0f3-403">Dans certaines situations, la propriété doit être modifiée. C’est le cas, par exemple, lorsque le serveur DNS contacte des serveurs distants via une liaison lente et que le serveur DNS tente une nouvelle tentative avant de recevoir la réponse du DNS distant.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-403">There are certain situations when the property should be changed; one example is when the DNS Server contacts remote servers over a slow link, and the DNS Server is retrying before receiving response from the remote DNS.</span></span> <span data-ttu-id="4f0f3-404">Dans ce cas, l’augmentation du délai d’attente doit être un peu plus long que le temps de réponse observé du DNS distant est raisonnable.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-404">In this case, raising the time out to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-405">**RecursionTimeout**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-405">**RecursionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-406">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-406">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-407">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-407">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-408">Secondes écoulées avant que le serveur DNS n’abandonne la requête récursive.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-408">Elapsed seconds before the DNS Server gives up recursive query.</span></span> <span data-ttu-id="4f0f3-409">Si la propriété n’est pas définie ou est égale à zéro, le serveur DNS abandonne au bout de 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-409">If the property is undefined or zero, the DNS Server gives up after 15 seconds.</span></span> <span data-ttu-id="4f0f3-410">En général, le délai d’expiration de 15 secondes est suffisant pour permettre à toute réponse en suspens de revenir au serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-410">In general, the 15-second time out is sufficient to allow any outstanding response to get back to the DNS Server.</span></span>

<span data-ttu-id="4f0f3-411">Les utilisateurs sont déconseillés de modifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-411">Users are discouraged from altering this property.</span></span> <span data-ttu-id="4f0f3-412">La propriété doit être modifiée lorsque le serveur DNS contacte des serveurs distants via une liaison lente, et que le serveur DNS est en mesure de rejeter les requêtes (avec défaillance du serveur \_ ) avant la réception des réponses.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-412">One scenario where the property should be changed is when the DNS Server contacts remote servers over a slow link, and the DNS Server is observed rejecting queries (with SERVER\_FAILURE) before responses are received.</span></span>

<span data-ttu-id="4f0f3-413">Les programmes de résolution des clients renouvellent également les requêtes. une investigation minutieuse est donc nécessaire pour déterminer si les réponses distantes sont réellement associées à la requête qui a expiré. Dans ce cas, l’augmentation de la valeur du délai d’attente doit être légèrement plus longue que le temps de réponse observé du DNS distant est raisonnable.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-413">Client resolvers also retry queries, so careful investigation is required to determine whether remote responses are actually associated with the query that timed out. In this case, raising the time out value to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-414">**RoundRobin**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-414">**RoundRobin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-415">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-416">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-416">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-417">Indique si le serveur DNS arrondit Robins plusieurs enregistrements A.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-417">Indicates whether the DNS Server round robins multiple A records.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-418">**RpcProtocol**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-418">**RpcProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-419">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-419">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-420">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-420">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-421">Protocole RPC ou protocoles sur lesquels l’appel RPC d’administration s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-421">RPC protocol or protocols over which administrative RPC runs.</span></span> <span data-ttu-id="4f0f3-422">L’algorithme suivant est utilisé pour assigner une valeur spécifique :</span><span class="sxs-lookup"><span data-stu-id="4f0f3-422">The following algorithm is used to assign a specific value:</span></span>



| <span data-ttu-id="4f0f3-423">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-423">Value</span></span>                                                                                                | <span data-ttu-id="4f0f3-424">Signification</span><span class="sxs-lookup"><span data-stu-id="4f0f3-424">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4f0f3-425"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-425"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-426">Aucun</span><span class="sxs-lookup"><span data-stu-id="4f0f3-426">None</span></span><br/>        |
| <span id="1"></span><dl> <span data-ttu-id="4f0f3-427"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-427"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-428">TCP</span><span class="sxs-lookup"><span data-stu-id="4f0f3-428">TCP</span></span><br/>         |
| <span id="2"></span><dl> <span data-ttu-id="4f0f3-429"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-429"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-430">Canaux nommés</span><span class="sxs-lookup"><span data-stu-id="4f0f3-430">Named Pipes</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="4f0f3-431"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-431"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4f0f3-432">LPC</span><span class="sxs-lookup"><span data-stu-id="4f0f3-432">LPC</span></span><br/>         |



 

<span data-ttu-id="4f0f3-433">La somme des valeurs indique les protocoles utilisés.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-433">The sum of the values indicates the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-434">**ScavengingInterval**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-434">**ScavengingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-435">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-435">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-436">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-436">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-437">Intervalle, en heures, entre deux opérations de nettoyage consécutives effectuées par le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-437">Interval, in hours, between two consecutive scavenging operations performed by the DNS Server.</span></span> <span data-ttu-id="4f0f3-438">La valeur zéro indique que le nettoyage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-438">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="4f0f3-439">La valeur par défaut est 168 heures (sept jours).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-439">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-440">**SecureResponses**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-440">**SecureResponses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-441">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-441">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-442">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-442">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-443">Indique si le serveur DNS enregistre exclusivement les enregistrements de noms dans la même sous-arborescence que le serveur qui les a fournis.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-443">Indicates whether the DNS Server exclusively saves records of names in the same subtree as the server that provided them.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-444">**SendPort**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-444">**SendPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-445">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-446">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-446">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-447">Port sur lequel le serveur DNS envoie des requêtes UDP à d’autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-447">Port on which the DNS Server sends UDP queries to other servers.</span></span> <span data-ttu-id="4f0f3-448">Par défaut, le serveur DNS envoie des requêtes sur un socket lié au port DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-448">By default, the DNS Server sends queries on a socket bound to the DNS port.</span></span>

<span data-ttu-id="4f0f3-449">Dans certains cas, il ne s’agit pas de la meilleure configuration.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-449">Under certain situations, this is not the best configuration.</span></span> <span data-ttu-id="4f0f3-450">Un cas évident est lorsqu’un administrateur bloque le port DNS avec un pare-feu pour empêcher l’accès externe au serveur DNS, mais souhaite toujours que le serveur soit en mesure de contacter les serveurs DNS Internet pour fournir la résolution de noms pour les clients internes.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-450">One obvious case is when an administrator blocks the DNS port with a firewall to prevent outside access to the DNS Server, but still wants the server to be able to contact Internet DNS Servers to provide name resolution for internal clients.</span></span> <span data-ttu-id="4f0f3-451">Autre cas de figure : le serveur DNS prend en charge les réseaux disjoints (la propriété **DisjointNets** définie sur true identifie ce scénario).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-451">Another case is when the DNS Server is supporting disjoint nets (the property **DisjointNets** set to TRUE identifies this scenario).</span></span> <span data-ttu-id="4f0f3-452">Dans ce cas, la définition de la propriété **SendOnNonDnsPort** sur une valeur différente de zéro indique au serveur DNS de se lier à un port arbitraire pour l’envoi aux serveurs DNS distants.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-452">In these cases, setting the **SendOnNonDnsPort** property to a nonzero value directs the DNS Server to bind to an arbitrary port for sending to remote DNS Servers.</span></span>

<span data-ttu-id="4f0f3-453">Si la valeur **SendOnNonDnsPort** est supérieure à 1024, le serveur DNS effectue une liaison explicite avec la valeur de port donnée.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-453">If the **SendOnNonDnsPort** value is greater than 1024, the DNS Server binds explicitly to the port value given.</span></span> <span data-ttu-id="4f0f3-454">Cette option de configuration est utile lorsqu’un administrateur doit corriger le port de requête DNS à des fins de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-454">This configuration option is useful when an administrator needs to fix the DNS query port for firewall purposes.</span></span>

<span data-ttu-id="4f0f3-455">\* \* Windows Server 2003 : \* \*</span><span class="sxs-lookup"><span data-stu-id="4f0f3-455">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="4f0f3-456">Si vous affectez à la propriété port d’envoi une valeur différente de zéro, le serveur DNS se lie à un port arbitraire pour l’envoi aux serveurs DNS distants.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-456">Setting the SendPort property to a non-zero value causes the DNS server to bind to an arbitrary port for sending to remote DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-457">**ServerAddresses**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-457">**ServerAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-458">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-458">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-459">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f0f3-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-460">Énumère la liste des adresses IP du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-460">Enumerates the list of IP addresses for the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-461">**StrictFileParsing**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-461">**StrictFileParsing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-462">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-462">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-463">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-463">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-464">Indique si le serveur DNS analyse les [*fichiers de zone*](z-gly.md) de manière stricte.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-464">Indicates whether the DNS Server parses [*zone files*](z-gly.md) strictly.</span></span> <span data-ttu-id="4f0f3-465">Si la valeur n’est pas définie ou égale à zéro, le serveur consigne et ignore les données incorrectes dans le fichier de zone et poursuit le chargement.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-465">If undefined or zero, the server will log and ignore bad data in the zone file and continue to load.</span></span> <span data-ttu-id="4f0f3-466">Si la valeur est différente de zéro, le serveur consigne et échoue sur les erreurs de fichier de zone.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-466">If nonzero, the server will log and fail on zone file errors.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-467">**UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-467">**UpdateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-468">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f0f3-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-470">Restreint le type d’enregistrements qui peuvent être mis à jour dynamiquement sur le serveur, utilisé en plus des paramètres **AllowUpdate** sur les objets serveur et zone.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-470">Restricts the type of records that can be dynamically updated on the server, used in addition to the **AllowUpdate** settings on Server and Zone objects.</span></span>

<span data-ttu-id="4f0f3-471">\* \* Windows Server 2003 : \* \*</span><span class="sxs-lookup"><span data-stu-id="4f0f3-471">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="4f0f3-472">0 : aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-472">0: No restrictions.</span></span>

<span data-ttu-id="4f0f3-473">1 : ne pas autoriser les mises à jour dynamiques des enregistrements SOA.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-473">1: Do not allow dynamic updates of SOA records.</span></span>

<span data-ttu-id="4f0f3-474">2 : n’autorisez pas les mises à jour dynamiques des enregistrements NS à la racine de la zone.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-474">2: Do not allow dynamic updates of NS records at the zone root.</span></span>

<span data-ttu-id="4f0f3-475">4 : n’autorisez pas les mises à jour dynamiques des enregistrements NS qui ne sont pas à la racine de la zone (enregistrements NS de délégation).</span><span class="sxs-lookup"><span data-stu-id="4f0f3-475">4: Do not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span>

<span data-ttu-id="4f0f3-476">Additionnez ces valeurs pour déterminer la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-476">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-477">**Version**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-477">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-478">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-479">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f0f3-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-480">Version du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-480">Version of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-481">**WriteAuthorityNS**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-481">**WriteAuthorityNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-482">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-483">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-483">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-484">Spécifie si le serveur DNS écrit des enregistrements NS et SOA dans la section autorité en cas de réponse correcte.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-484">Specifies whether the DNS Server writes NS and SOA records to the authority section on successful response.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f3-485">**XfrConnectTimeout**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-485">**XfrConnectTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f3-486">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f3-487">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f0f3-487">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4f0f3-488">Durée, en secondes, pendant laquelle le serveur DNS attend la réussite d’une connexion TCP à un serveur distant lors d’une tentative de transfert de zone.</span><span class="sxs-lookup"><span data-stu-id="4f0f3-488">Time, in seconds, the DNS Server waits for a successful TCP connection to a remote server when attempting a zone transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f0f3-489">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f0f3-489">Requirements</span></span>



| <span data-ttu-id="4f0f3-490">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f0f3-490">Requirement</span></span> | <span data-ttu-id="4f0f3-491">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0f3-491">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0f3-492">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0f3-492">Minimum supported client</span></span><br/> | <span data-ttu-id="4f0f3-493">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0f3-493">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f0f3-494">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0f3-494">Minimum supported server</span></span><br/> | <span data-ttu-id="4f0f3-495">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f0f3-495">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4f0f3-496">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f0f3-496">Namespace</span></span><br/>                | <span data-ttu-id="4f0f3-497">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="4f0f3-497">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4f0f3-498">MOF</span><span class="sxs-lookup"><span data-stu-id="4f0f3-498">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f0f3-499"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f0f3-499"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0f3-500">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f0f3-500">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0f3-501">**Méthode StartService de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-501">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="4f0f3-502">**Méthode StopService de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-502">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="4f0f3-503">**Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-503">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="4f0f3-504">**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f0f3-504">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





