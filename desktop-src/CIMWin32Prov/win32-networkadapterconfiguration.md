---
description: Représente les attributs et les comportements d’une carte réseau. Cette classe comprend des propriétés et des méthodes supplémentaires qui prennent en charge la gestion du protocole TCP/IP qui sont indépendantes de la carte réseau.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153572"
---
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="2daa3-104">\_Classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="2daa3-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2daa3-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkAdapterConfiguration** représente les attributs et les comportements d’une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="2daa3-106">Cette classe comprend des propriétés et des méthodes supplémentaires qui prennent en charge la gestion du protocole TCP/IP qui sont indépendantes de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="2daa3-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2daa3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2daa3-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2daa3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2daa3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2daa3-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a><span data-ttu-id="2daa3-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2daa3-110">Members</span></span>

<span data-ttu-id="2daa3-111">La classe **Win32 \_ NetworkAdapterConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2daa3-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="2daa3-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2daa3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2daa3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2daa3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2daa3-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2daa3-114">Methods</span></span>

<span data-ttu-id="2daa3-115">La classe **Win32 \_ NetworkAdapterConfiguration** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2daa3-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="2daa3-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="2daa3-116">Method</span></span>                                                                                                                       | <span data-ttu-id="2daa3-117">Description</span><span class="sxs-lookup"><span data-stu-id="2daa3-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2daa3-118">**DisableIPSec**</span><span class="sxs-lookup"><span data-stu-id="2daa3-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="2daa3-119">Désactive IPsec sur cette carte réseau compatible TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="2daa3-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="2daa3-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="2daa3-121">Active le protocole DHCP (Dynamic Host Configuration Protocol) pour le service avec cette carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="2daa3-122">**EnableDNS**</span><span class="sxs-lookup"><span data-stu-id="2daa3-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="2daa3-123">Active le système DNS (Domain Name System) pour le service sur cette carte réseau TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="2daa3-124">**EnableIPFilterSec**</span><span class="sxs-lookup"><span data-stu-id="2daa3-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="2daa3-125">Active IPsec globalement sur toutes les cartes réseau liées à IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="2daa3-126">**EnableIPSec**</span><span class="sxs-lookup"><span data-stu-id="2daa3-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="2daa3-127">Active IPsec sur cette carte réseau TCP/IP spécifique.</span><span class="sxs-lookup"><span data-stu-id="2daa3-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="2daa3-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="2daa3-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="2daa3-129">Active l’adressage TCP/IP statique pour la carte réseau cible.</span><span class="sxs-lookup"><span data-stu-id="2daa3-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="2daa3-130">**EnableWINS**</span><span class="sxs-lookup"><span data-stu-id="2daa3-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="2daa3-131">Active les paramètres WINS spécifiques à TCP/IP, mais indépendamment de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="2daa3-132">**Dispose ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="2daa3-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="2daa3-133">Libère l’adresse IP liée à une carte réseau DHCP spécifique.</span><span class="sxs-lookup"><span data-stu-id="2daa3-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="2daa3-134">**ReleaseDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="2daa3-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="2daa3-135">Libère les adresses IP liées à toutes les cartes réseau compatibles DHCP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="2daa3-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="2daa3-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="2daa3-137">Renouvelle l’adresse IP sur des cartes réseau compatibles DHCP spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2daa3-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="2daa3-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="2daa3-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="2daa3-139">Renouvelle les adresses IP sur toutes les cartes réseau compatibles DHCP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="2daa3-140">**SetArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="2daa3-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="2daa3-141">Définit la transmission des requêtes ARP par le protocole TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="2daa3-142">**SetArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="2daa3-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="2daa3-143">Permet aux paquets Ethernet d’utiliser l’encodage de l’alignement 802,3.</span><span class="sxs-lookup"><span data-stu-id="2daa3-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="2daa3-144">**SetDatabasePath**</span><span class="sxs-lookup"><span data-stu-id="2daa3-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="2daa3-145">Définit le chemin d’accès aux fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux et protocoles).</span><span class="sxs-lookup"><span data-stu-id="2daa3-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="2daa3-146">**SetDeadGWDetect**</span><span class="sxs-lookup"><span data-stu-id="2daa3-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="2daa3-147">Active la détection de passerelle inactive.</span><span class="sxs-lookup"><span data-stu-id="2daa3-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="2daa3-148">**SetDefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="2daa3-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="2daa3-149">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="2daa3-149">Obsolete.</span></span> <span data-ttu-id="2daa3-150">Cette méthode définit la valeur par défaut du type de service (TOS) dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="2daa3-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="2daa3-151">**SetDefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="2daa3-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="2daa3-152">Définit la valeur de durée de vie (TTL) par défaut dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="2daa3-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="2daa3-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="2daa3-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="2daa3-154">Définit le domaine DNS.</span><span class="sxs-lookup"><span data-stu-id="2daa3-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="2daa3-155">**SetDNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="2daa3-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="2daa3-156">Définit l’ordre de recherche du serveur sous la forme d’un tableau d’éléments.</span><span class="sxs-lookup"><span data-stu-id="2daa3-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="2daa3-157">**SetDNSSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="2daa3-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="2daa3-158">Définit l’ordre de recherche des suffixes sous la forme d’un tableau d’éléments.</span><span class="sxs-lookup"><span data-stu-id="2daa3-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="2daa3-159">**SetDynamicDNSRegistration**</span><span class="sxs-lookup"><span data-stu-id="2daa3-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="2daa3-160">Indique l’inscription DNS dynamique des adresses IP pour cette carte liée à IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="2daa3-161">**SetForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="2daa3-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="2daa3-162">Spécifie la quantité de mémoire allouée par l’adresse IP pour stocker les données de paquets dans la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="2daa3-163">**SetGateways**</span><span class="sxs-lookup"><span data-stu-id="2daa3-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="2daa3-164">Spécifie une liste de passerelles pour le routage des paquets destinés à un sous-réseau différent de celui auquel cette carte est connectée.</span><span class="sxs-lookup"><span data-stu-id="2daa3-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="2daa3-165">**SetIGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="2daa3-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="2daa3-166">Définit dans quelle mesure le système prend en charge la multidiffusion IP et participe au protocole de gestion de groupes Internet.</span><span class="sxs-lookup"><span data-stu-id="2daa3-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="2daa3-167">**SetIPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="2daa3-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="2daa3-168">Définit la métrique de routage associée à cette carte IP liée.</span><span class="sxs-lookup"><span data-stu-id="2daa3-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="2daa3-169">**SetIPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="2daa3-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="2daa3-170">Définit l’utilisation de la diffusion à zéro IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="2daa3-171">**SetIPXFrameTypeNetworkPairs**</span><span class="sxs-lookup"><span data-stu-id="2daa3-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="2daa3-172">Définit le numéro de réseau/les paires d’images IPX (Internetworking Packet Exchange) pour cette carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="2daa3-173">**SetIPXVirtualNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="2daa3-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="2daa3-174">Définit le numéro de réseau virtuel IPX sur le système de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="2daa3-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="2daa3-175">**SetKeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="2daa3-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="2daa3-176">Définit l’intervalle séparant les retransmissions KeepAlive jusqu’à la réception d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="2daa3-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="2daa3-177">**SetKeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="2daa3-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="2daa3-178">Définit la fréquence à laquelle TCP tente de vérifier qu’une connexion inactive est toujours disponible en envoyant un paquet Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="2daa3-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="2daa3-179">**SetMTU**</span><span class="sxs-lookup"><span data-stu-id="2daa3-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="2daa3-180">Définit l’unité de transmission maximale (MTU) par défaut pour une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="2daa3-181">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2daa3-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="2daa3-182">**SetNumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="2daa3-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="2daa3-183">Définit le nombre d’en-têtes de paquet IP alloués pour la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="2daa3-184">**SetPMTUBHDetect**</span><span class="sxs-lookup"><span data-stu-id="2daa3-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="2daa3-185">Active la détection des routeurs trou noir.</span><span class="sxs-lookup"><span data-stu-id="2daa3-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="2daa3-186">**SetPMTUDiscovery**</span><span class="sxs-lookup"><span data-stu-id="2daa3-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="2daa3-187">Active la détection de l’unité de transmission maximale (MTU).</span><span class="sxs-lookup"><span data-stu-id="2daa3-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2daa3-188">**SetTcpipNetbios**</span><span class="sxs-lookup"><span data-stu-id="2daa3-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="2daa3-189">Définit l’opération par défaut de NetBIOS sur TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2daa3-190">**SetTcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="2daa3-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="2daa3-191">Définit le nombre de tentatives que TCP retransmet une demande de connexion avant d’abandonner.</span><span class="sxs-lookup"><span data-stu-id="2daa3-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="2daa3-192">**SetTcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="2daa3-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="2daa3-193">Définit le nombre de retransmissions d’un segment de données individuel par TCP avant d’abandonner la connexion.</span><span class="sxs-lookup"><span data-stu-id="2daa3-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="2daa3-194">**SetTcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="2daa3-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="2daa3-195">Définit le nombre maximal de connexions que TCP peut avoir ouvertes simultanément.</span><span class="sxs-lookup"><span data-stu-id="2daa3-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="2daa3-196">**SetTcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa3-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="2daa3-197">Spécifie si TCP utilise la spécification RFC 1122 pour les données urgentes, ou le mode utilisé par les systèmes dérivés de Berkeley Software Design (BSD).</span><span class="sxs-lookup"><span data-stu-id="2daa3-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="2daa3-198">**SetTcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="2daa3-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="2daa3-199">Définit la taille maximale de la fenêtre de réception TCP offerte par le système.</span><span class="sxs-lookup"><span data-stu-id="2daa3-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="2daa3-200">**SetWINSServer**</span><span class="sxs-lookup"><span data-stu-id="2daa3-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="2daa3-201">Définit les serveurs WINS (Windows Internet Service de nommage) principaux et secondaires sur cette carte réseau TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="2daa3-202">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2daa3-202">Properties</span></span>

<span data-ttu-id="2daa3-203">La classe **Win32 \_ NetworkAdapterConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2daa3-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2daa3-204">**ArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="2daa3-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-205">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-207">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")</span><span class="sxs-lookup"><span data-stu-id="2daa3-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-208">Si la **valeur est true**, TCP/IP transmet les requêtes ARP (Address Resolution Protocol) avec le routage source activé sur les réseaux Token Ring.</span><span class="sxs-lookup"><span data-stu-id="2daa3-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="2daa3-209">Par défaut (FALSe), les premières requêtes ARP sans routage source sont retentées avec le routage source activé si aucune réponse n’est reçue.</span><span class="sxs-lookup"><span data-stu-id="2daa3-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="2daa3-210">Le routage source permet le routage de paquets réseau sur différents types de réseaux.</span><span class="sxs-lookup"><span data-stu-id="2daa3-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-211">**ArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="2daa3-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-212">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-214">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| ArpUseEtherSNAP")</span><span class="sxs-lookup"><span data-stu-id="2daa3-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-215">Si la **valeur est true**, les paquets Ethernet suivent l’encodage IEEE 802,3 Sub-Network Access Protocol (SNAP).</span><span class="sxs-lookup"><span data-stu-id="2daa3-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="2daa3-216">Si vous affectez la valeur 1 à ce paramètre, TCP/IP transmet les paquets Ethernet à l’aide de l’encodage SNAP 802,3.</span><span class="sxs-lookup"><span data-stu-id="2daa3-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="2daa3-217">Par défaut (FALSe), la pile transmet les paquets au format Ethernet DIX.</span><span class="sxs-lookup"><span data-stu-id="2daa3-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2daa3-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-221">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="2daa3-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-222">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="2daa3-222">Short textual description of the current object.</span></span>

<span data-ttu-id="2daa3-223">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="2daa3-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-224">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="2daa3-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-227">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| DatabasePath")</span><span class="sxs-lookup"><span data-stu-id="2daa3-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-228">Chemin de fichier Windows valide pour les fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux et protocoles).</span><span class="sxs-lookup"><span data-stu-id="2daa3-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="2daa3-229">Le chemin d’accès du fichier est utilisé par l’interface Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2daa3-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-230">**DeadGWDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-233">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnableDeadGWDetect")</span><span class="sxs-lookup"><span data-stu-id="2daa3-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-234">Si la **valeur est true**, la détection de passerelle inactive se produit.</span><span class="sxs-lookup"><span data-stu-id="2daa3-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="2daa3-235">Lorsque cette fonctionnalité est activée, le protocole TCP (Transmission Control Protocol) demande au protocole IP (Internet Protocol) de passer à une passerelle de sauvegarde s’il retransmet un segment plusieurs fois sans recevoir de réponse.</span><span class="sxs-lookup"><span data-stu-id="2daa3-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="2daa3-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-237">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-239">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| Parameters \| DefaultGateway")</span><span class="sxs-lookup"><span data-stu-id="2daa3-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-240">Tableau d’adresses IP des passerelles par défaut utilisées par le système informatique.</span><span class="sxs-lookup"><span data-stu-id="2daa3-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="2daa3-241">Exemple : « 192.168.12.1 192.168.46.1 »</span><span class="sxs-lookup"><span data-stu-id="2daa3-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-242">**DefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="2daa3-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-243">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2daa3-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-245">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| DefaultTOS")</span><span class="sxs-lookup"><span data-stu-id="2daa3-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-246">Valeur de type de service (TOS) par défaut définie dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="2daa3-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="2daa3-247">La RFC (Request for Comments) 791 définit les valeurs.</span><span class="sxs-lookup"><span data-stu-id="2daa3-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="2daa3-248">Valeur par défaut : 0 (zéro), plage valide : 0-255.</span><span class="sxs-lookup"><span data-stu-id="2daa3-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="2daa3-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-250">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2daa3-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-252">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| DefaultTtl")</span><span class="sxs-lookup"><span data-stu-id="2daa3-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-253">Valeur de durée de vie (TTL) par défaut définie dans l’en-tête des paquets IP sortants.</span><span class="sxs-lookup"><span data-stu-id="2daa3-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="2daa3-254">La durée de vie spécifie le nombre de routeurs qu’un paquet IP peut traverser pour atteindre sa destination avant d’être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2daa3-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="2daa3-255">Chaque routeur décrémente d’une unité le nombre de TTL d’un paquet au fur et à mesure qu’il passe et ignore les paquets, si la durée de vie est égale à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2daa3-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="2daa3-256">Valeur par défaut : 32, plage valide : 1-255.</span><span class="sxs-lookup"><span data-stu-id="2daa3-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-257">**Description**</span><span class="sxs-lookup"><span data-stu-id="2daa3-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-260">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="2daa3-260">Textual description of the current object.</span></span>

<span data-ttu-id="2daa3-261">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="2daa3-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-263">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-265">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| EnableDHCP")</span><span class="sxs-lookup"><span data-stu-id="2daa3-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-266">Si la **valeur est true**, le serveur DHCP (Dynamic Host Configuration Protocol) attribue automatiquement une adresse IP au système informatique lors de l’établissement d’une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-267">**DHCPLeaseExpires**</span><span class="sxs-lookup"><span data-stu-id="2daa3-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-268">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2daa3-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-270">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| LeaseTerminatesTime")</span><span class="sxs-lookup"><span data-stu-id="2daa3-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-271">Date et heure d’expiration d’une adresse IP louée qui a été affectée à l’ordinateur par le serveur DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="2daa3-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="2daa3-272">Exemple : 20521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="2daa3-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-273">**DHCPLeaseObtained**</span><span class="sxs-lookup"><span data-stu-id="2daa3-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-274">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2daa3-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-276">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| LeaseObtainedTime")</span><span class="sxs-lookup"><span data-stu-id="2daa3-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-277">Date et heure auxquelles le bail a été obtenu pour l’adresse IP affectée à l’ordinateur par le serveur DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="2daa3-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="2daa3-278">Exemple : 19521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="2daa3-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-279">**DHCPServer**</span><span class="sxs-lookup"><span data-stu-id="2daa3-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-282">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| DhcpServer")</span><span class="sxs-lookup"><span data-stu-id="2daa3-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-283">Adresse IP du serveur DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="2daa3-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="2daa3-284">Exemple : « 10.55.34.2 »</span><span class="sxs-lookup"><span data-stu-id="2daa3-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="2daa3-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-288">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| Domain")</span><span class="sxs-lookup"><span data-stu-id="2daa3-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-289">Nom de l’organisation suivi d’un point et d’une extension qui indique le type d’organisation, par exemple « microsoft.com ».</span><span class="sxs-lookup"><span data-stu-id="2daa3-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="2daa3-290">Le nom peut être n’importe quelle combinaison des lettres de A à Z, les chiffres de 0 à 9 et le trait d’Union (-), ainsi que le point (.) utilisé comme séparateur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="2daa3-291">Exemple : « microsoft.com »</span><span class="sxs-lookup"><span data-stu-id="2daa3-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-292">**DNSDomainSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="2daa3-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-293">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-295">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| SearchList")</span><span class="sxs-lookup"><span data-stu-id="2daa3-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-296">Tableau de suffixes de domaine DNS à ajouter à la fin des noms d’hôtes lors de la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="2daa3-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="2daa3-297">Lorsque vous tentez de résoudre un nom de domaine complet (FQDN) à partir d’un nom d’hôte uniquement, le système ajoute d’abord le nom de domaine local.</span><span class="sxs-lookup"><span data-stu-id="2daa3-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="2daa3-298">Si ce n’est pas le cas, le système utilise la liste de suffixes de domaine pour créer des noms de domaine complets supplémentaires dans l’ordre indiqué et interroger les serveurs DNS pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="2daa3-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="2daa3-299">Exemple : « samples.microsoft.com example.microsoft.com »</span><span class="sxs-lookup"><span data-stu-id="2daa3-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-300">**DNSEnabledForWINSResolution**</span><span class="sxs-lookup"><span data-stu-id="2daa3-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-301">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-303">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnableDNS")</span><span class="sxs-lookup"><span data-stu-id="2daa3-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-304">Si la **valeur est true**, le système DNS (Domain Name System) est activé pour la résolution de noms sur la résolution WINS (Windows Internet service de nommage).</span><span class="sxs-lookup"><span data-stu-id="2daa3-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="2daa3-305">Si le nom ne peut pas être résolu à l’aide de DNS, la demande de nom est transférée vers WINS pour la résolution.</span><span class="sxs-lookup"><span data-stu-id="2daa3-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-306">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="2daa3-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-309">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| hostname")</span><span class="sxs-lookup"><span data-stu-id="2daa3-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-310">Nom d’hôte utilisé pour identifier l’ordinateur local pour l’authentification par certains utilitaires.</span><span class="sxs-lookup"><span data-stu-id="2daa3-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="2daa3-311">D’autres utilitaires basés sur TCP/IP peuvent utiliser cette valeur pour obtenir le nom de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2daa3-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="2daa3-312">Les noms d’hôte sont stockés sur les serveurs DNS dans une table qui mappe les noms à des adresses IP pour une utilisation par DNS.</span><span class="sxs-lookup"><span data-stu-id="2daa3-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="2daa3-313">Le nom peut être n’importe quelle combinaison des lettres de A à Z, les chiffres de 0 à 9 et le trait d’Union (-), ainsi que le point (.) utilisé comme séparateur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="2daa3-314">Par défaut, cette valeur est le nom de l’ordinateur réseau Microsoft, mais l’administrateur réseau peut attribuer un autre nom d’hôte sans affecter le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="2daa3-315">Exemple : « corpdns »</span><span class="sxs-lookup"><span data-stu-id="2daa3-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-316">**DNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="2daa3-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-317">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-319">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| nameserver")</span><span class="sxs-lookup"><span data-stu-id="2daa3-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-320">Tableau d’adresses IP de serveur à utiliser pour l’interrogation des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="2daa3-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-321">**DomainDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-322">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-324">Si la **valeur est true**, les adresses IP de cette connexion sont inscrites dans DNS sous le nom de domaine de cette connexion, en plus d’être inscrites sous le nom DNS complet de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="2daa3-325">Le nom de domaine de cette connexion est défini à l’aide de la méthode [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() ou affecté par DSCP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="2daa3-326">Le nom inscrit est le nom d’hôte de l’ordinateur avec le nom de domaine ajouté.</span><span class="sxs-lookup"><span data-stu-id="2daa3-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-327">**ForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="2daa3-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-328">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-330">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2daa3-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-331">Mémoire allouée par l’adresse IP pour stocker les données de paquets dans la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="2daa3-332">Lorsque l’espace de la mémoire tampon est rempli, le routeur commence à ignorer les paquets aléatoirement dans sa file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2daa3-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="2daa3-333">Les tampons de données de file d’attente de paquets ont une longueur de 256 octets, donc la valeur de ce paramètre doit être un multiple de 256.</span><span class="sxs-lookup"><span data-stu-id="2daa3-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="2daa3-334">Plusieurs mémoires tampons sont chaînées pour les paquets plus volumineux.</span><span class="sxs-lookup"><span data-stu-id="2daa3-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="2daa3-335">L’en-tête IP d’un paquet est stocké séparément.</span><span class="sxs-lookup"><span data-stu-id="2daa3-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="2daa3-336">Ce paramètre est ignoré et aucune mémoire tampon n’est allouée si le routeur IP n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="2daa3-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="2daa3-337">La taille de la mémoire tampon peut être comprise entre l’unité MTU du réseau et une valeur inférieure à 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2daa3-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="2daa3-338">Valeur par défaut : 74240 (paquets de 50 1480 octets, arrondis à un multiple de 256).</span><span class="sxs-lookup"><span data-stu-id="2daa3-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-339">**FullDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-340">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-342">Si la **valeur est true**, les adresses IP de cette connexion sont inscrites dans DNS sous le nom DNS complet de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="2daa3-343">Le nom DNS complet de l’ordinateur s’affiche sous l’onglet **identification réseau** de l’application système dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="2daa3-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-344">**GatewayCostMetric**</span><span class="sxs-lookup"><span data-stu-id="2daa3-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-345">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2daa3-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-347">Tableau de valeurs de métriques de coût entières (allant de 1 à 9999) à utiliser pour calculer les itinéraires les plus rapides, les plus fiables ou les moins gourmands en ressources.</span><span class="sxs-lookup"><span data-stu-id="2daa3-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="2daa3-348">Cet argument a une correspondance un-à-un avec la propriété **DefaultIPGateway** .</span><span class="sxs-lookup"><span data-stu-id="2daa3-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-349">**IGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="2daa3-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-350">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2daa3-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-352">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| IGMPLevel")</span><span class="sxs-lookup"><span data-stu-id="2daa3-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-353">Mesure dans laquelle le système prend en charge la multidiffusion IP et participe au protocole IGMP (Internet Group Management Protocol).</span><span class="sxs-lookup"><span data-stu-id="2daa3-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="2daa3-354">Au niveau 0 (zéro), le système ne prend pas en charge la multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="2daa3-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="2daa3-355">Au niveau 1, le système peut uniquement envoyer des paquets de multidiffusion IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="2daa3-356">Au niveau 2, le système peut envoyer des paquets de multidiffusion IP et participer pleinement à IGMP pour recevoir des paquets de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="2daa3-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="2daa3-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Aucune multidiffusion** (0)</span><span class="sxs-lookup"><span data-stu-id="2daa3-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="2daa3-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multidiffusion IP** (1)</span><span class="sxs-lookup"><span data-stu-id="2daa3-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="2daa3-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & multidiffusion IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="2daa3-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2daa3-360">Multidiffusion IP et IGMP (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2daa3-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2daa3-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="2daa3-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-362">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-364">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="2daa3-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-365">Numéro d’index de la configuration de la carte réseau Windows.</span><span class="sxs-lookup"><span data-stu-id="2daa3-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="2daa3-366">Le numéro d’index est utilisé lorsque plusieurs configurations sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-367">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="2daa3-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-368">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-370">Valeur d’index qui identifie de façon unique une interface réseau locale.</span><span class="sxs-lookup"><span data-stu-id="2daa3-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="2daa3-371">La valeur de cette propriété est la même que la valeur de la propriété **InterfaceIndex** dans l’instance de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) qui représente l’interface réseau dans la table d’itinéraires.</span><span class="sxs-lookup"><span data-stu-id="2daa3-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-372">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="2daa3-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-373">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-375">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| paramètres \\ \\ tcpip \| IPAddress")</span><span class="sxs-lookup"><span data-stu-id="2daa3-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-376">Tableau de toutes les adresses IP associées à la carte réseau actuelle.</span><span class="sxs-lookup"><span data-stu-id="2daa3-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="2daa3-377">Cette propriété peut contenir des adresses IPv6 ou IPv4.</span><span class="sxs-lookup"><span data-stu-id="2daa3-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="2daa3-378">Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2daa3-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="2daa3-379">Exemple d’adresse IPv6 : « 2010:836B : 4179 :: 836B : 4179 »</span><span class="sxs-lookup"><span data-stu-id="2daa3-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-380">**IPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="2daa3-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-381">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-383">Coût d’utilisation des itinéraires configurés pour la carte liée à IP et est la valeur pondérée pour ces itinéraires dans la table de routage IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="2daa3-384">S’il existe plusieurs itinéraires vers une destination dans la table de routage IP, l’itinéraire avec la métrique la plus basse est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2daa3-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="2daa3-385">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="2daa3-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-387">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-389">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| paramètres \\ \\ tcpip")</span><span class="sxs-lookup"><span data-stu-id="2daa3-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-390">Si la **valeur est true**, TCP/IP est lié et activé sur cette carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-391">**IPFilterSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-392">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-394">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="2daa3-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-395">Si la **valeur est true**, la sécurité du port IP est activée globalement pour toutes les cartes réseau liées à IP et les valeurs de sécurité associées aux cartes réseau individuelles sont en vigueur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="2daa3-396">Cette propriété est utilisée conjointement avec **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts** et **IPSecPermitIPProtocols**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="2daa3-397">Si la **valeur est false**, la sécurité de filtre IP est désactivée sur toutes les cartes réseau et autorise le trafic de tous les ports et protocoles à circuler non filtré.</span><span class="sxs-lookup"><span data-stu-id="2daa3-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-398">**IPPortSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-399">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-401">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="2daa3-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-402">Si la **valeur est true**, la sécurité du port IP est activée globalement pour toutes les cartes réseau liées à IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="2daa3-403">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="2daa3-403">This property is obsolete.</span></span> <span data-ttu-id="2daa3-404">À la place de cette propriété, vous devez utiliser **IPFilterSecurityEnabled**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-405">**IPSecPermitIPProtocols**</span><span class="sxs-lookup"><span data-stu-id="2daa3-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-406">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-408">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| RawIPAllowedProtocols")</span><span class="sxs-lookup"><span data-stu-id="2daa3-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-409">Tableau des protocoles autorisés à s’exécuter sur l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="2daa3-410">La liste des protocoles est définie à l’aide de la méthode [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2daa3-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="2daa3-411">La liste est vide ou contient des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="2daa3-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="2daa3-412">Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="2daa3-413">Une chaîne vide indique qu’aucun protocole n’est autorisé à s’exécuter lorsque **IPFilterSecurityEnabled** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-414">**IPSecPermitTCPPorts**</span><span class="sxs-lookup"><span data-stu-id="2daa3-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-415">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-417">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TCPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="2daa3-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-418">Tableau des ports qui seront autorisés à accéder à TCP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="2daa3-419">La liste des protocoles est définie à l’aide de la méthode [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2daa3-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="2daa3-420">La liste est vide ou contient des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="2daa3-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="2daa3-421">Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les ports.</span><span class="sxs-lookup"><span data-stu-id="2daa3-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="2daa3-422">Une chaîne vide indique qu’aucun port ne dispose de l’autorisation d’accès lorsque **IPFilterSecurityEnabled** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-423">**IPSecPermitUDPPorts**</span><span class="sxs-lookup"><span data-stu-id="2daa3-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-424">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-426">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| UDPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="2daa3-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-427">Tableau des ports qui seront autorisés à accéder au protocole UDP (User Datagram Protocol).</span><span class="sxs-lookup"><span data-stu-id="2daa3-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="2daa3-428">La liste des protocoles est définie à l’aide de la méthode [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2daa3-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="2daa3-429">La liste est vide ou contient des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="2daa3-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="2daa3-430">Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les ports.</span><span class="sxs-lookup"><span data-stu-id="2daa3-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="2daa3-431">Une chaîne vide indique qu’aucun port ne dispose de l’autorisation d’accès lorsque **IPFilterSecurityEnabled** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="2daa3-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-433">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-435">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| paramètres \| Masque_Sous_réseau")</span><span class="sxs-lookup"><span data-stu-id="2daa3-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-436">Tableau de tous les masques de sous-réseau associés à la carte réseau actuelle.</span><span class="sxs-lookup"><span data-stu-id="2daa3-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="2daa3-437">Exemple : « 255.255.0.0 »</span><span class="sxs-lookup"><span data-stu-id="2daa3-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-438">**IPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="2daa3-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-439">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-441">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| UseZeroBroadcast")</span><span class="sxs-lookup"><span data-stu-id="2daa3-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-442">Si la **valeur est true**, les diffusions de zéro IP sont utilisées (0.0.0.0) et le système utilise des diffusions (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="2daa3-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="2daa3-443">Les systèmes informatiques utilisent généralement des diffusions à la fois, mais ceux dérivés des implémentations BSD utilisent des diffusions de zéros.</span><span class="sxs-lookup"><span data-stu-id="2daa3-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="2daa3-444">Les systèmes qui n’utilisent pas ces mêmes diffusions n’interagissent pas sur le même réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="2daa3-445">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-446">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="2daa3-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-447">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-449">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Sockets version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| \_ 'adresse IPX")</span><span class="sxs-lookup"><span data-stu-id="2daa3-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-450">La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-451">**IPXEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-452">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-454">Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="2daa3-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-455">La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-456">**IPXFrameType**</span><span class="sxs-lookup"><span data-stu-id="2daa3-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-457">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-459">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| PktType")</span><span class="sxs-lookup"><span data-stu-id="2daa3-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-460">La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="2daa3-461">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="2daa3-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="2daa3-462">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="2daa3-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="2daa3-463">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="2daa3-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="2daa3-464">**Snap Ethernet** (3)</span><span class="sxs-lookup"><span data-stu-id="2daa3-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="2daa3-465">**Automatique** (255)</span><span class="sxs-lookup"><span data-stu-id="2daa3-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2daa3-466">**IPXMediaType**</span><span class="sxs-lookup"><span data-stu-id="2daa3-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-467">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-469">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| MediaType")</span><span class="sxs-lookup"><span data-stu-id="2daa3-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-470">La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="2daa3-471">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="2daa3-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="2daa3-472">**Token Ring** (2)</span><span class="sxs-lookup"><span data-stu-id="2daa3-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="2daa3-473">**FDDI** (3)</span><span class="sxs-lookup"><span data-stu-id="2daa3-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="2daa3-474">**Arcnet** (8)</span><span class="sxs-lookup"><span data-stu-id="2daa3-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2daa3-475">**IPXNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="2daa3-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-476">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2daa3-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-478">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| numéroRéseau")</span><span class="sxs-lookup"><span data-stu-id="2daa3-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-479">La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-480">**IPXVirtualNetNumber**</span><span class="sxs-lookup"><span data-stu-id="2daa3-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-483">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| VirtualNetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="2daa3-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-484">La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.</span><span class="sxs-lookup"><span data-stu-id="2daa3-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="2daa3-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-486">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-488">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="2daa3-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-489">Intervalle séparant les retransmissions KeepAlive jusqu’à la réception d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="2daa3-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="2daa3-490">Après la réception d’une réponse, le délai jusqu’à ce que la transmission Keep Alive suivante soit de nouveau contrôlé par la valeur de **keepAliveTime**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="2daa3-491">La connexion est abandonnée une fois que le nombre de retransmissions spécifié par **TcpMaxDataRetransmissions** n’a pas répondu.</span><span class="sxs-lookup"><span data-stu-id="2daa3-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="2daa3-492">Valeur par défaut : 1000, plage valide : 1-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2daa3-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="2daa3-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-494">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-496">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="2daa3-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-497">La propriété **keepAliveTime** indique la fréquence à laquelle le protocole TCP tente de vérifier qu’une connexion inactive est toujours intacte en envoyant un paquet Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="2daa3-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="2daa3-498">Un système distant accessible accuse réception de la transmission Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="2daa3-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="2daa3-499">Les paquets Keep Alive ne sont pas envoyés par défaut.</span><span class="sxs-lookup"><span data-stu-id="2daa3-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="2daa3-500">Cette fonctionnalité peut être activée dans une connexion par une application.</span><span class="sxs-lookup"><span data-stu-id="2daa3-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="2daa3-501">Valeur par défaut : 7,2 millions (deux heures).</span><span class="sxs-lookup"><span data-stu-id="2daa3-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="2daa3-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-503">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-504">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-505">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| DeviceIoControl »)</span><span class="sxs-lookup"><span data-stu-id="2daa3-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-506">Adresse MAC (Media Access Control) de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="2daa3-507">Une adresse MAC est affectée par le fabricant pour identifier la carte réseau de manière unique.</span><span class="sxs-lookup"><span data-stu-id="2daa3-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="2daa3-508">Exemple : « 00:80 : C7:8F : 6C : 96 »</span><span class="sxs-lookup"><span data-stu-id="2daa3-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-509">**MTU**</span><span class="sxs-lookup"><span data-stu-id="2daa3-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-510">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-511">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-512">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2daa3-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-513">Remplace l’unité de transmission maximale (MTU) par défaut pour une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="2daa3-514">L’unité de transmission maximale (MTU) correspond à la taille maximale des paquets (y compris l’en-tête de transport) que le transport transmet sur le réseau sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2daa3-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="2daa3-515">Le datagramme IP peut s’étendre sur plusieurs paquets.</span><span class="sxs-lookup"><span data-stu-id="2daa3-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="2daa3-516">La plage de cette valeur s’étend sur la taille minimale des paquets (68) au MTU pris en charge par le réseau sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2daa3-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-517">**NumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="2daa3-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-518">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-520">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| NumForwardPackets")</span><span class="sxs-lookup"><span data-stu-id="2daa3-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-521">Nombre d’en-têtes de paquet IP alloués pour la file d’attente de paquets du routeur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="2daa3-522">Lorsque tous les en-têtes sont en cours d’utilisation, le routeur commence à rejeter les paquets de la file d’attente au hasard.</span><span class="sxs-lookup"><span data-stu-id="2daa3-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="2daa3-523">Cette valeur doit être au moins aussi grande que la valeur **ForwardBufferMemory** divisée par la taille maximale des données IP des réseaux connectés au routeur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="2daa3-524">Elle ne doit pas être supérieure à la valeur **ForwardBufferMemory** divisée par 256, car au moins 256 octets de mémoire tampon de transfert sont utilisés pour chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="2daa3-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="2daa3-525">Le nombre optimal de paquets de transfert pour une taille **ForwardBufferMemory** donnée dépend du type de trafic sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="2daa3-526">Il se situe entre ces deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="2daa3-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="2daa3-527">Si le routeur n’est pas activé, ce paramètre est ignoré et aucun en-tête n’est alloué.</span><span class="sxs-lookup"><span data-stu-id="2daa3-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="2daa3-528">Valeur par défaut : 50, plage valide : 1-0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="2daa3-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-529">**PMTUBHDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-530">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-531">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-532">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUBHDetect")</span><span class="sxs-lookup"><span data-stu-id="2daa3-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-533">Si la **valeur est true**, la détection des routeurs de trou noir se produit lorsque TCP Découvre le chemin d’accès de l’unité de transmission maximale.</span><span class="sxs-lookup"><span data-stu-id="2daa3-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="2daa3-534">Un routeur de trou noir ne renvoie pas de messages ICMP Destination inaccessible lorsqu’il doit fragmenter un datagramme IP avec le bit ne pas fragmenter défini.</span><span class="sxs-lookup"><span data-stu-id="2daa3-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="2daa3-535">TCP dépend de la réception de ces messages pour effectuer la détection du chemin MTU.</span><span class="sxs-lookup"><span data-stu-id="2daa3-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="2daa3-536">Une fois cette fonctionnalité activée, le protocole TCP essaiera d’envoyer des segments sans le bit de non fragment défini si plusieurs retransmissions d’un segment ne sont pas acquittées.</span><span class="sxs-lookup"><span data-stu-id="2daa3-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="2daa3-537">Si le segment est reconnu par conséquent, la valeur MSS sera réduite et le bit ne pas fragment sera défini dans les prochains paquets sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="2daa3-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="2daa3-538">L’activation de la détection de trou noir augmente le nombre maximal de retransmissions effectuées pour un segment donné.</span><span class="sxs-lookup"><span data-stu-id="2daa3-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="2daa3-539">La valeur par défaut de cette propriété est **false**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-540">**PMTUDiscoveryEnabled**</span><span class="sxs-lookup"><span data-stu-id="2daa3-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-541">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-542">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-543">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUDiscovery")</span><span class="sxs-lookup"><span data-stu-id="2daa3-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-544">Si la **valeur est true**, le chemin d’accès de l’unité de transmission maximale (MTU) est découvert sur le chemin d’accès à un hôte distant.</span><span class="sxs-lookup"><span data-stu-id="2daa3-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="2daa3-545">En détectant le chemin d’accès MTU et en limitant les segments TCP à cette taille, TCP peut éliminer la fragmentation sur les routeurs sur le chemin d’accès qui connecte les réseaux avec différents MTU.</span><span class="sxs-lookup"><span data-stu-id="2daa3-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="2daa3-546">La fragmentation affecte le débit TCP et la congestion du réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="2daa3-547">Si vous affectez la **valeur false** à ce paramètre, un MTU de 576 octets est utilisé pour toutes les connexions qui ne sont pas des ordinateurs sur le sous-réseau local.</span><span class="sxs-lookup"><span data-stu-id="2daa3-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="2daa3-548">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-549">**NomService**</span><span class="sxs-lookup"><span data-stu-id="2daa3-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-550">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-551">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-552">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="2daa3-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-553">Nom de service de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-553">Service name of the network adapter.</span></span> <span data-ttu-id="2daa3-554">Ce nom est généralement plus petit que le nom complet du produit.</span><span class="sxs-lookup"><span data-stu-id="2daa3-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="2daa3-555">Exemple : « Elnkii »</span><span class="sxs-lookup"><span data-stu-id="2daa3-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="2daa3-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-557">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-558">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-559">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="2daa3-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-560">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="2daa3-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="2daa3-561">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="2daa3-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-562">**TcpipNetbiosOptions**</span><span class="sxs-lookup"><span data-stu-id="2daa3-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-563">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-564">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-565">Bitmap des paramètres possibles relatifs à NetBIOS sur TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="2daa3-566">Les valeurs sont identifiées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="2daa3-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="2daa3-567">**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="2daa3-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="2daa3-568">**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="2daa3-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="2daa3-569">**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="2daa3-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2daa3-570">**TcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="2daa3-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-571">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-572">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-573">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpMaxConnectRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="2daa3-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-574">Nombre de tentatives de retransmission d’une demande de connexion par TCP avant de mettre fin à la connexion.</span><span class="sxs-lookup"><span data-stu-id="2daa3-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="2daa3-575">Le délai de retransmission initial est de 3 secondes.</span><span class="sxs-lookup"><span data-stu-id="2daa3-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="2daa3-576">Le délai de retransmission double pour chaque tentative.</span><span class="sxs-lookup"><span data-stu-id="2daa3-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="2daa3-577">Valeur par défaut : 3, plage valide : 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2daa3-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="2daa3-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-579">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-580">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-581">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| TcpMaxDataRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="2daa3-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-582">Nombre de fois que le protocole TCP retransmet un segment de données individuel (segment non Connect) avant de mettre fin à la connexion.</span><span class="sxs-lookup"><span data-stu-id="2daa3-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="2daa3-583">Le délai de retransmission double à chaque retransmission successive sur une connexion.</span><span class="sxs-lookup"><span data-stu-id="2daa3-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="2daa3-584">Valeur par défaut : 5, plage valide : 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2daa3-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-585">**TcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="2daa3-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-586">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2daa3-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-587">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-588">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpNumConnections")</span><span class="sxs-lookup"><span data-stu-id="2daa3-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-589">Nombre maximal de connexions ouvertes simultanément par TCP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="2daa3-590">Valeur par défaut : 0xFFFFFE, plage valide : 0-0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="2daa3-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-591">**TcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa3-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-592">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-593">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-594">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")</span><span class="sxs-lookup"><span data-stu-id="2daa3-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-595">Si la **valeur est true**, TCP utilise la spécification RFC 1122 pour les données urgentes.</span><span class="sxs-lookup"><span data-stu-id="2daa3-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="2daa3-596">Si la **valeur est false** (valeur par défaut), TCP utilise le mode utilisé par les systèmes dérivés BSD (Berkeley Software Design).</span><span class="sxs-lookup"><span data-stu-id="2daa3-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="2daa3-597">Les deux mécanismes interprètent le pointeur urgent différemment et ne sont pas interopérables.</span><span class="sxs-lookup"><span data-stu-id="2daa3-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="2daa3-598">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="2daa3-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-600">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2daa3-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-601">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-602">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2daa3-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-603">Taille maximale de la fenêtre de réception TCP offerte par le système.</span><span class="sxs-lookup"><span data-stu-id="2daa3-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="2daa3-604">La fenêtre de réception spécifie le nombre d’octets qu’un expéditeur peut transmettre sans recevoir d’accusé de réception.</span><span class="sxs-lookup"><span data-stu-id="2daa3-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="2daa3-605">En général, les fenêtres de réception plus volumineuses améliorent les performances sur les réseaux à haut débit et à bande passante élevée.</span><span class="sxs-lookup"><span data-stu-id="2daa3-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="2daa3-606">Pour des performances optimales, la fenêtre de réception doit être un multiple pair de la taille maximale du segment TCP (MSS).</span><span class="sxs-lookup"><span data-stu-id="2daa3-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="2daa3-607">Valeur par défaut : quatre fois la taille maximale des données TCP ou un multiple pair de la taille des données TCP arrondi au multiple le plus proche de 8192.</span><span class="sxs-lookup"><span data-stu-id="2daa3-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="2daa3-608">Les réseaux Ethernet ont par défaut la valeur 8760.</span><span class="sxs-lookup"><span data-stu-id="2daa3-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="2daa3-609">Plage valide : 0-65535.</span><span class="sxs-lookup"><span data-stu-id="2daa3-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="2daa3-610">Windows Vista : cette propriété accède à l' `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrée de Registre, qui n’est pas utilisée dans l’implémentation actuelle du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2daa3-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="2daa3-611">**WINSEnableLMHostsLookup**</span><span class="sxs-lookup"><span data-stu-id="2daa3-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-612">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2daa3-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-613">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-614">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnableLMHOSTS")</span><span class="sxs-lookup"><span data-stu-id="2daa3-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-615">Si la **valeur est true**, les fichiers de recherche locaux sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="2daa3-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="2daa3-616">Les fichiers de recherche contiennent un mappage d’adresses IP aux noms d’hôtes.</span><span class="sxs-lookup"><span data-stu-id="2daa3-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="2daa3-617">S’ils existent sur le système local, ils se trouvent dans% SystemRoot% \\ system32 \\ drivers, \\ etc.</span><span class="sxs-lookup"><span data-stu-id="2daa3-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-618">**WINSHostLookupFile**</span><span class="sxs-lookup"><span data-stu-id="2daa3-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-619">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-620">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-621">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers \\ \\ etc \\ \\ Lmhosts »)</span><span class="sxs-lookup"><span data-stu-id="2daa3-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-622">Chemin d’accès à un fichier de recherche WINS sur le système local.</span><span class="sxs-lookup"><span data-stu-id="2daa3-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="2daa3-623">Ce fichier contient un mappage d’adresses IP aux noms d’hôtes.</span><span class="sxs-lookup"><span data-stu-id="2daa3-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="2daa3-624">Si le fichier spécifié dans cette propriété est trouvé, il sera copié dans le dossier% SystemRoot% \\ system32 \\ drivers, \\ etc. du système local.</span><span class="sxs-lookup"><span data-stu-id="2daa3-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="2daa3-625">Valide uniquement si la propriété **WINSEnableLMHostsLookup** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="2daa3-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-626">**WINSPrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="2daa3-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-627">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-628">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-629">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| DeviceIoControl »)</span><span class="sxs-lookup"><span data-stu-id="2daa3-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-630">Adresse IP du serveur WINS principal.</span><span class="sxs-lookup"><span data-stu-id="2daa3-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-631">**WINSScopeID**</span><span class="sxs-lookup"><span data-stu-id="2daa3-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-632">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-633">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-634">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| ScopeId")</span><span class="sxs-lookup"><span data-stu-id="2daa3-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-635">Valeur ajoutée à la fin du nom NetBIOS qui isole un groupe de systèmes informatiques communiquant les uns avec les autres.</span><span class="sxs-lookup"><span data-stu-id="2daa3-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="2daa3-636">Elle est utilisée pour toutes les transactions NetBIOS sur les communications TCP/IP à partir de ce système informatique.</span><span class="sxs-lookup"><span data-stu-id="2daa3-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="2daa3-637">Les ordinateurs configurés avec des identificateurs d’étendue identiques sont en mesure de communiquer avec cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2daa3-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="2daa3-638">Les clients TCP/IP avec des identificateurs d’étendue différents ignorent les paquets des ordinateurs ayant cet identificateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2daa3-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="2daa3-639">Valide uniquement lorsque la méthode [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="2daa3-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="2daa3-640">**WINSSecondaryServer**</span><span class="sxs-lookup"><span data-stu-id="2daa3-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2daa3-641">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2daa3-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-642">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2daa3-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2daa3-643">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| DeviceIoControl »)</span><span class="sxs-lookup"><span data-stu-id="2daa3-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="2daa3-644">Adresse IP du serveur WINS secondaire.</span><span class="sxs-lookup"><span data-stu-id="2daa3-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2daa3-645">Remarques</span><span class="sxs-lookup"><span data-stu-id="2daa3-645">Remarks</span></span>

<span data-ttu-id="2daa3-646">La classe **Win32 \_ NetworkAdapterConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="2daa3-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2daa3-647">Exemples</span><span class="sxs-lookup"><span data-stu-id="2daa3-647">Examples</span></span>

<span data-ttu-id="2daa3-648">L’exemple de code VBScript de l' [extracteur d’informations WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) sur la Galerie TechNet utilise la classe **Win32 \_ NetworkAdapterConfiguration** pour récupérer des informations de configuration réseau à partir d’un certain nombre d’ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="2daa3-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="2daa3-649">L’exemple PowerShell- [ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sur la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, notamment **Win32 \_ NetworkAdapterConfiguration**, pour afficher des informations sur un système local ou distant.</span><span class="sxs-lookup"><span data-stu-id="2daa3-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="2daa3-650">Le code PowerShell suivant récupère les paramètres de configuration de l’adaptateur Microsoft ISTAP.</span><span class="sxs-lookup"><span data-stu-id="2daa3-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="2daa3-651">L’exemple C suivant \# récupère la description et le numéro d’index de toutes les instances de configuration de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="2daa3-652">Notez que cet \# exemple C utilise l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , qui est généralement mis à l’échelle plus efficacement que les classes WMI d’espace de noms [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="2daa3-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



<span data-ttu-id="2daa3-653">L’exemple C suivant \# récupère la description et le numéro d’index de toutes les instances de configuration de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2daa3-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="2daa3-654">Notez que cet \# exemple C utilise l’espace de noms [System. Management](/dotnet/api/system.management) d’origine, qui a été remplacé par [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2daa3-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



<span data-ttu-id="2daa3-655">L’exemple suivant récupère des informations de la classe **Win32 \_ NetworkAdapterConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="2daa3-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a><span data-ttu-id="2daa3-656">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2daa3-656">Requirements</span></span>



| <span data-ttu-id="2daa3-657">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2daa3-657">Requirement</span></span> | <span data-ttu-id="2daa3-658">Valeur</span><span class="sxs-lookup"><span data-stu-id="2daa3-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2daa3-659">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2daa3-659">Minimum supported client</span></span><br/> | <span data-ttu-id="2daa3-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2daa3-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2daa3-661">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2daa3-661">Minimum supported server</span></span><br/> | <span data-ttu-id="2daa3-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2daa3-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2daa3-663">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2daa3-663">Namespace</span></span><br/>                | <span data-ttu-id="2daa3-664">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2daa3-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2daa3-665">MOF</span><span class="sxs-lookup"><span data-stu-id="2daa3-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2daa3-666"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2daa3-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2daa3-667">DLL</span><span class="sxs-lookup"><span data-stu-id="2daa3-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2daa3-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2daa3-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2daa3-669">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2daa3-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2daa3-670">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="2daa3-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="2daa3-671">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="2daa3-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2daa3-672">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="2daa3-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="2daa3-673">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="2daa3-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="2daa3-674">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="2daa3-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
