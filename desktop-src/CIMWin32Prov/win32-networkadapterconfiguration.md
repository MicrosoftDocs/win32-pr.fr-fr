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
# <a name="win32_networkadapterconfiguration-class"></a>\_Classe NetworkAdapterConfiguration Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkAdapterConfiguration** représente les attributs et les comportements d’une carte réseau. Cette classe comprend des propriétés et des méthodes supplémentaires qui prennent en charge la gestion du protocole TCP/IP qui sont indépendantes de la carte réseau.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **Win32 \_ NetworkAdapterConfiguration** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ NetworkAdapterConfiguration** possède ces méthodes.



| Méthode                                                                                                                       | Description                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Désactive IPsec sur cette carte réseau compatible TCP/IP.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Active le protocole DHCP (Dynamic Host Configuration Protocol) pour le service avec cette carte réseau.<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Active le système DNS (Domain Name System) pour le service sur cette carte réseau TCP/IP.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Active IPsec globalement sur toutes les cartes réseau liées à IP.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Active IPsec sur cette carte réseau TCP/IP spécifique.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Active l’adressage TCP/IP statique pour la carte réseau cible.<br/>                                                                           |
| [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Active les paramètres WINS spécifiques à TCP/IP, mais indépendamment de la carte réseau.<br/>                                                          |
| [**Dispose ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Libère l’adresse IP liée à une carte réseau DHCP spécifique.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Libère les adresses IP liées à toutes les cartes réseau compatibles DHCP.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Renouvelle l’adresse IP sur des cartes réseau compatibles DHCP spécifiques.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Renouvelle les adresses IP sur toutes les cartes réseau compatibles DHCP.<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Définit la transmission des requêtes ARP par le protocole TCP/IP.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Permet aux paquets Ethernet d’utiliser l’encodage de l’alignement 802,3.<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Définit le chemin d’accès aux fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux et protocoles).<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Active la détection de passerelle inactive.<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Obsolète. Cette méthode définit la valeur par défaut du type de service (TOS) dans l’en-tête des paquets IP sortants.<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Définit la valeur de durée de vie (TTL) par défaut dans l’en-tête des paquets IP sortants.<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Définit le domaine DNS.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Définit l’ordre de recherche du serveur sous la forme d’un tableau d’éléments.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Définit l’ordre de recherche des suffixes sous la forme d’un tableau d’éléments.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Indique l’inscription DNS dynamique des adresses IP pour cette carte liée à IP.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Spécifie la quantité de mémoire allouée par l’adresse IP pour stocker les données de paquets dans la file d’attente de paquets du routeur.<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Spécifie une liste de passerelles pour le routage des paquets destinés à un sous-réseau différent de celui auquel cette carte est connectée.<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Définit dans quelle mesure le système prend en charge la multidiffusion IP et participe au protocole de gestion de groupes Internet.<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Définit la métrique de routage associée à cette carte IP liée.<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Définit l’utilisation de la diffusion à zéro IP.<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Définit le numéro de réseau/les paires d’images IPX (Internetworking Packet Exchange) pour cette carte réseau.<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Définit le numéro de réseau virtuel IPX sur le système de l’ordinateur cible.<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Définit l’intervalle séparant les retransmissions KeepAlive jusqu’à la réception d’une réponse.<br/>                                                      |
| [**SetKeepAliveTime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Définit la fréquence à laquelle TCP tente de vérifier qu’une connexion inactive est toujours disponible en envoyant un paquet Keep Alive.<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Définit l’unité de transmission maximale (MTU) par défaut pour une interface réseau.<br/> Cette méthode n'est pas prise en charge.<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Définit le nombre d’en-têtes de paquet IP alloués pour la file d’attente de paquets du routeur.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Active la détection des routeurs trou noir.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Active la détection de l’unité de transmission maximale (MTU).<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Définit l’opération par défaut de NetBIOS sur TCP/IP.<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Définit le nombre de tentatives que TCP retransmet une demande de connexion avant d’abandonner.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Définit le nombre de retransmissions d’un segment de données individuel par TCP avant d’abandonner la connexion.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Définit le nombre maximal de connexions que TCP peut avoir ouvertes simultanément.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Spécifie si TCP utilise la spécification RFC 1122 pour les données urgentes, ou le mode utilisé par les systèmes dérivés de Berkeley Software Design (BSD).<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Définit la taille maximale de la fenêtre de réception TCP offerte par le système.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Définit les serveurs WINS (Windows Internet Service de nommage) principaux et secondaires sur cette carte réseau TCP/IP.<br/>                        |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ NetworkAdapterConfiguration** a ces propriétés.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")
</dt> </dl>

Si la **valeur est true**, TCP/IP transmet les requêtes ARP (Address Resolution Protocol) avec le routage source activé sur les réseaux Token Ring. Par défaut (FALSe), les premières requêtes ARP sans routage source sont retentées avec le routage source activé si aucune réponse n’est reçue. Le routage source permet le routage de paquets réseau sur différents types de réseaux.

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| ArpUseEtherSNAP")
</dt> </dl>

Si la **valeur est true**, les paquets Ethernet suivent l’encodage IEEE 802,3 Sub-Network Access Protocol (SNAP). Si vous affectez la valeur 1 à ce paramètre, TCP/IP transmet les paquets Ethernet à l’aide de l’encodage SNAP 802,3. Par défaut (FALSe), la pile transmet les paquets au format Ethernet DIX.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| DatabasePath")
</dt> </dl>

Chemin de fichier Windows valide pour les fichiers de base de données Internet standard (hôtes, LMHOSTS, réseaux et protocoles). Le chemin d’accès du fichier est utilisé par l’interface Windows Sockets.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnableDeadGWDetect")
</dt> </dl>

Si la **valeur est true**, la détection de passerelle inactive se produit. Lorsque cette fonctionnalité est activée, le protocole TCP (Transmission Control Protocol) demande au protocole IP (Internet Protocol) de passer à une passerelle de sauvegarde s’il retransmet un segment plusieurs fois sans recevoir de réponse.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| Parameters \| DefaultGateway")
</dt> </dl>

Tableau d’adresses IP des passerelles par défaut utilisées par le système informatique.

Exemple : « 192.168.12.1 192.168.46.1 »

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| DefaultTOS")
</dt> </dl>

Valeur de type de service (TOS) par défaut définie dans l’en-tête des paquets IP sortants. La RFC (Request for Comments) 791 définit les valeurs. Valeur par défaut : 0 (zéro), plage valide : 0-255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| DefaultTtl")
</dt> </dl>

Valeur de durée de vie (TTL) par défaut définie dans l’en-tête des paquets IP sortants. La durée de vie spécifie le nombre de routeurs qu’un paquet IP peut traverser pour atteindre sa destination avant d’être ignoré. Chaque routeur décrémente d’une unité le nombre de TTL d’un paquet au fur et à mesure qu’il passe et ignore les paquets, si la durée de vie est égale à 0 (zéro). Valeur par défaut : 32, plage valide : 1-255.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| EnableDHCP")
</dt> </dl>

Si la **valeur est true**, le serveur DHCP (Dynamic Host Configuration Protocol) attribue automatiquement une adresse IP au système informatique lors de l’établissement d’une connexion réseau.

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| LeaseTerminatesTime")
</dt> </dl>

Date et heure d’expiration d’une adresse IP louée qui a été affectée à l’ordinateur par le serveur DHCP (Dynamic Host Configuration Protocol).

Exemple : 20521201000230,000000000

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| LeaseObtainedTime")
</dt> </dl>

Date et heure auxquelles le bail a été obtenu pour l’adresse IP affectée à l’ordinateur par le serveur DHCP (Dynamic Host Configuration Protocol).

Exemple : 19521201000230,000000000

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| DhcpServer")
</dt> </dl>

Adresse IP du serveur DHCP (Dynamic Host Configuration Protocol).

Exemple : « 10.55.34.2 »

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| Domain")
</dt> </dl>

Nom de l’organisation suivi d’un point et d’une extension qui indique le type d’organisation, par exemple « microsoft.com ». Le nom peut être n’importe quelle combinaison des lettres de A à Z, les chiffres de 0 à 9 et le trait d’Union (-), ainsi que le point (.) utilisé comme séparateur.

Exemple : « microsoft.com »

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| SearchList")
</dt> </dl>

Tableau de suffixes de domaine DNS à ajouter à la fin des noms d’hôtes lors de la résolution de noms. Lorsque vous tentez de résoudre un nom de domaine complet (FQDN) à partir d’un nom d’hôte uniquement, le système ajoute d’abord le nom de domaine local. Si ce n’est pas le cas, le système utilise la liste de suffixes de domaine pour créer des noms de domaine complets supplémentaires dans l’ordre indiqué et interroger les serveurs DNS pour chacun d’entre eux.

Exemple : « samples.microsoft.com example.microsoft.com »

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnableDNS")
</dt> </dl>

Si la **valeur est true**, le système DNS (Domain Name System) est activé pour la résolution de noms sur la résolution WINS (Windows Internet service de nommage). Si le nom ne peut pas être résolu à l’aide de DNS, la demande de nom est transférée vers WINS pour la résolution.

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| hostname")
</dt> </dl>

Nom d’hôte utilisé pour identifier l’ordinateur local pour l’authentification par certains utilitaires. D’autres utilitaires basés sur TCP/IP peuvent utiliser cette valeur pour obtenir le nom de l’ordinateur local. Les noms d’hôte sont stockés sur les serveurs DNS dans une table qui mappe les noms à des adresses IP pour une utilisation par DNS. Le nom peut être n’importe quelle combinaison des lettres de A à Z, les chiffres de 0 à 9 et le trait d’Union (-), ainsi que le point (.) utilisé comme séparateur. Par défaut, cette valeur est le nom de l’ordinateur réseau Microsoft, mais l’administrateur réseau peut attribuer un autre nom d’hôte sans affecter le nom de l’ordinateur.

Exemple : « corpdns »

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| nameserver")
</dt> </dl>

Tableau d’adresses IP de serveur à utiliser pour l’interrogation des serveurs DNS.

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, les adresses IP de cette connexion sont inscrites dans DNS sous le nom de domaine de cette connexion, en plus d’être inscrites sous le nom DNS complet de l’ordinateur. Le nom de domaine de cette connexion est défini à l’aide de la méthode [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() ou affecté par DSCP. Le nom inscrit est le nom d’hôte de l’ordinateur avec le nom de domaine ajouté.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Mémoire allouée par l’adresse IP pour stocker les données de paquets dans la file d’attente de paquets du routeur. Lorsque l’espace de la mémoire tampon est rempli, le routeur commence à ignorer les paquets aléatoirement dans sa file d’attente. Les tampons de données de file d’attente de paquets ont une longueur de 256 octets, donc la valeur de ce paramètre doit être un multiple de 256. Plusieurs mémoires tampons sont chaînées pour les paquets plus volumineux. L’en-tête IP d’un paquet est stocké séparément. Ce paramètre est ignoré et aucune mémoire tampon n’est allouée si le routeur IP n’est pas activé. La taille de la mémoire tampon peut être comprise entre l’unité MTU du réseau et une valeur inférieure à 0xFFFFFFFF. Valeur par défaut : 74240 (paquets de 50 1480 octets, arrondis à un multiple de 256).

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, les adresses IP de cette connexion sont inscrites dans DNS sous le nom DNS complet de l’ordinateur. Le nom DNS complet de l’ordinateur s’affiche sous l’onglet **identification réseau** de l’application système dans le panneau de configuration.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de valeurs de métriques de coût entières (allant de 1 à 9999) à utiliser pour calculer les itinéraires les plus rapides, les plus fiables ou les moins gourmands en ressources. Cet argument a une correspondance un-à-un avec la propriété **DefaultIPGateway** .

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| IGMPLevel")
</dt> </dl>

Mesure dans laquelle le système prend en charge la multidiffusion IP et participe au protocole IGMP (Internet Group Management Protocol). Au niveau 0 (zéro), le système ne prend pas en charge la multidiffusion. Au niveau 1, le système peut uniquement envoyer des paquets de multidiffusion IP. Au niveau 2, le système peut envoyer des paquets de multidiffusion IP et participer pleinement à IGMP pour recevoir des paquets de multidiffusion.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Aucune multidiffusion** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multidiffusion IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & multidiffusion IGMP** (2)


</dt> <dd>

Multidiffusion IP et IGMP (par défaut)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Numéro d’index de la configuration de la carte réseau Windows. Le numéro d’index est utilisé lorsque plusieurs configurations sont disponibles.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur d’index qui identifie de façon unique une interface réseau locale. La valeur de cette propriété est la même que la valeur de la propriété **InterfaceIndex** dans l’instance de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) qui représente l’interface réseau dans la table d’itinéraires.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| paramètres \\ \\ tcpip \| IPAddress")
</dt> </dl>

Tableau de toutes les adresses IP associées à la carte réseau actuelle. Cette propriété peut contenir des adresses IPv6 ou IPv4. Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

Exemple d’adresse IPv6 : « 2010:836B : 4179 :: 836B : 4179 »

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Coût d’utilisation des itinéraires configurés pour la carte liée à IP et est la valeur pondérée pour ces itinéraires dans la table de routage IP. S’il existe plusieurs itinéraires vers une destination dans la table de routage IP, l’itinéraire avec la métrique la plus basse est utilisé. La valeur par défaut est 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| paramètres \\ \\ tcpip")
</dt> </dl>

Si la **valeur est true**, TCP/IP est lié et activé sur cette carte réseau.

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| IPFilterSecurityEnabled")
</dt> </dl>

Si la **valeur est true**, la sécurité du port IP est activée globalement pour toutes les cartes réseau liées à IP et les valeurs de sécurité associées aux cartes réseau individuelles sont en vigueur. Cette propriété est utilisée conjointement avec **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts** et **IPSecPermitIPProtocols**. Si la **valeur est false**, la sécurité de filtre IP est désactivée sur toutes les cartes réseau et autorise le trafic de tous les ports et protocoles à circuler non filtré.

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")
</dt> </dl>

Si la **valeur est true**, la sécurité du port IP est activée globalement pour toutes les cartes réseau liées à IP. Cette propriété est obsolète. À la place de cette propriété, vous devez utiliser **IPFilterSecurityEnabled**.

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| RawIPAllowedProtocols")
</dt> </dl>

Tableau des protocoles autorisés à s’exécuter sur l’adresse IP. La liste des protocoles est définie à l’aide de la méthode [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . La liste est vide ou contient des valeurs numériques. Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les protocoles. Une chaîne vide indique qu’aucun protocole n’est autorisé à s’exécuter lorsque **IPFilterSecurityEnabled** a la **valeur true**.

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TCPAllowedPorts")
</dt> </dl>

Tableau des ports qui seront autorisés à accéder à TCP. La liste des protocoles est définie à l’aide de la méthode [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . La liste est vide ou contient des valeurs numériques. Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les ports. Une chaîne vide indique qu’aucun port ne dispose de l’autorisation d’accès lorsque **IPFilterSecurityEnabled** a la **valeur true**.

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| UDPAllowedPorts")
</dt> </dl>

Tableau des ports qui seront autorisés à accéder au protocole UDP (User Datagram Protocol). La liste des protocoles est définie à l’aide de la méthode [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . La liste est vide ou contient des valeurs numériques. Une valeur numérique 0 (zéro) indique que l’autorisation d’accès est accordée pour tous les ports. Une chaîne vide indique qu’aucun port ne dispose de l’autorisation d’accès lorsque **IPFilterSecurityEnabled** a la **valeur true**.

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| paramètres \| Masque_Sous_réseau")
</dt> </dl>

Tableau de tous les masques de sous-réseau associés à la carte réseau actuelle.

Exemple : « 255.255.0.0 »

</dd> <dt>

**IPUseZeroBroadcast**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| UseZeroBroadcast")
</dt> </dl>

Si la **valeur est true**, les diffusions de zéro IP sont utilisées (0.0.0.0) et le système utilise des diffusions (255.255.255.255). Les systèmes informatiques utilisent généralement des diffusions à la fois, mais ceux dérivés des implémentations BSD utilisent des diffusions de zéros. Les systèmes qui n’utilisent pas ces mêmes diffusions n’interagissent pas sur le même réseau. La valeur par défaut est **false**.

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Sockets version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| \_ 'adresse IPX")
</dt> </dl>

La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| PktType")
</dt> </dl>

La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Snap Ethernet** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Automatique** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| MediaType")
</dt> </dl>

La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token Ring** (2)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (3)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**Arcnet** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXNetworkNumber**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| numéroRéseau")
</dt> </dl>

La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ NwlnkIpx \\ \\ Parameters \| VirtualNetworkNumber")
</dt> </dl>

La technologie d’échange de paquets interréseau (IPX) n’est plus prise en charge et cette propriété ne contient pas de données utiles.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Intervalle séparant les retransmissions KeepAlive jusqu’à la réception d’une réponse. Après la réception d’une réponse, le délai jusqu’à ce que la transmission Keep Alive suivante soit de nouveau contrôlé par la valeur de **keepAliveTime**. La connexion est abandonnée une fois que le nombre de retransmissions spécifié par **TcpMaxDataRetransmissions** n’a pas répondu. Valeur par défaut : 1000, plage valide : 1-0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

La propriété **keepAliveTime** indique la fréquence à laquelle le protocole TCP tente de vérifier qu’une connexion inactive est toujours intacte en envoyant un paquet Keep Alive. Un système distant accessible accuse réception de la transmission Keep Alive. Les paquets Keep Alive ne sont pas envoyés par défaut. Cette fonctionnalité peut être activée dans une connexion par une application. Valeur par défaut : 7,2 millions (deux heures).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| DeviceIoControl »)
</dt> </dl>

Adresse MAC (Media Access Control) de la carte réseau. Une adresse MAC est affectée par le fabricant pour identifier la carte réseau de manière unique.

Exemple : « 00:80 : C7:8F : 6C : 96 »

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Remplace l’unité de transmission maximale (MTU) par défaut pour une interface réseau. L’unité de transmission maximale (MTU) correspond à la taille maximale des paquets (y compris l’en-tête de transport) que le transport transmet sur le réseau sous-jacent. Le datagramme IP peut s’étendre sur plusieurs paquets. La plage de cette valeur s’étend sur la taille minimale des paquets (68) au MTU pris en charge par le réseau sous-jacent.

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| NumForwardPackets")
</dt> </dl>

Nombre d’en-têtes de paquet IP alloués pour la file d’attente de paquets du routeur. Lorsque tous les en-têtes sont en cours d’utilisation, le routeur commence à rejeter les paquets de la file d’attente au hasard. Cette valeur doit être au moins aussi grande que la valeur **ForwardBufferMemory** divisée par la taille maximale des données IP des réseaux connectés au routeur. Elle ne doit pas être supérieure à la valeur **ForwardBufferMemory** divisée par 256, car au moins 256 octets de mémoire tampon de transfert sont utilisés pour chaque paquet. Le nombre optimal de paquets de transfert pour une taille **ForwardBufferMemory** donnée dépend du type de trafic sur le réseau. Il se situe entre ces deux valeurs. Si le routeur n’est pas activé, ce paramètre est ignoré et aucun en-tête n’est alloué. Valeur par défaut : 50, plage valide : 1-0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUBHDetect")
</dt> </dl>

Si la **valeur est true**, la détection des routeurs de trou noir se produit lorsque TCP Découvre le chemin d’accès de l’unité de transmission maximale. Un routeur de trou noir ne renvoie pas de messages ICMP Destination inaccessible lorsqu’il doit fragmenter un datagramme IP avec le bit ne pas fragmenter défini. TCP dépend de la réception de ces messages pour effectuer la détection du chemin MTU. Une fois cette fonctionnalité activée, le protocole TCP essaiera d’envoyer des segments sans le bit de non fragment défini si plusieurs retransmissions d’un segment ne sont pas acquittées. Si le segment est reconnu par conséquent, la valeur MSS sera réduite et le bit ne pas fragment sera défini dans les prochains paquets sur la connexion. L’activation de la détection de trou noir augmente le nombre maximal de retransmissions effectuées pour un segment donné. La valeur par défaut de cette propriété est **false**.

</dd> <dt>

**PMTUDiscoveryEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUDiscovery")
</dt> </dl>

Si la **valeur est true**, le chemin d’accès de l’unité de transmission maximale (MTU) est découvert sur le chemin d’accès à un hôte distant. En détectant le chemin d’accès MTU et en limitant les segments TCP à cette taille, TCP peut éliminer la fragmentation sur les routeurs sur le chemin d’accès qui connecte les réseaux avec différents MTU. La fragmentation affecte le débit TCP et la congestion du réseau. Si vous affectez la **valeur false** à ce paramètre, un MTU de 576 octets est utilisé pour toutes les connexions qui ne sont pas des ordinateurs sur le sous-réseau local. La valeur par défaut est **true**.

</dd> <dt>

**NomService**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nom de service de la carte réseau. Ce nom est généralement plus petit que le nom complet du produit.

Exemple : « Elnkii »

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bitmap des paramètres possibles relatifs à NetBIOS sur TCP/IP. Les valeurs sont identifiées dans la liste suivante.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**EnableNetbiosViaDhcp** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**EnableNetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**TcpMaxConnectRetransmissions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpMaxConnectRetransmissions")
</dt> </dl>

Nombre de tentatives de retransmission d’une demande de connexion par TCP avant de mettre fin à la connexion. Le délai de retransmission initial est de 3 secondes. Le délai de retransmission double pour chaque tentative. Valeur par défaut : 3, plage valide : 0-0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ paramètres \| TcpMaxDataRetransmissions")
</dt> </dl>

Nombre de fois que le protocole TCP retransmet un segment de données individuel (segment non Connect) avant de mettre fin à la connexion. Le délai de retransmission double à chaque retransmission successive sur une connexion. Valeur par défaut : 5, plage valide : 0-0xFFFFFFFF.

</dd> <dt>

**TcpNumConnections**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpNumConnections")
</dt> </dl>

Nombre maximal de connexions ouvertes simultanément par TCP. Valeur par défaut : 0xFFFFFE, plage valide : 0-0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")
</dt> </dl>

Si la **valeur est true**, TCP utilise la spécification RFC 1122 pour les données urgentes. Si la **valeur est false** (valeur par défaut), TCP utilise le mode utilisé par les systèmes dérivés BSD (Berkeley Software Design). Les deux mécanismes interprètent le pointeur urgent différemment et ne sont pas interopérables. La valeur par défaut est **FALSE**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Taille maximale de la fenêtre de réception TCP offerte par le système. La fenêtre de réception spécifie le nombre d’octets qu’un expéditeur peut transmettre sans recevoir d’accusé de réception. En général, les fenêtres de réception plus volumineuses améliorent les performances sur les réseaux à haut débit et à bande passante élevée. Pour des performances optimales, la fenêtre de réception doit être un multiple pair de la taille maximale du segment TCP (MSS). Valeur par défaut : quatre fois la taille maximale des données TCP ou un multiple pair de la taille des données TCP arrondi au multiple le plus proche de 8192. Les réseaux Ethernet ont par défaut la valeur 8760. Plage valide : 0-65535.

> [!Note]  
> Windows Vista : cette propriété accède à l' `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrée de Registre, qui n’est pas utilisée dans l’implémentation actuelle du système d’exploitation.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| EnableLMHOSTS")
</dt> </dl>

Si la **valeur est true**, les fichiers de recherche locaux sont utilisés. Les fichiers de recherche contiennent un mappage d’adresses IP aux noms d’hôtes. S’ils existent sur le système local, ils se trouvent dans% SystemRoot% \\ system32 \\ drivers, \\ etc.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers \\ \\ etc \\ \\ Lmhosts »)
</dt> </dl>

Chemin d’accès à un fichier de recherche WINS sur le système local. Ce fichier contient un mappage d’adresses IP aux noms d’hôtes. Si le fichier spécifié dans cette propriété est trouvé, il sera copié dans le dossier% SystemRoot% \\ system32 \\ drivers, \\ etc. du système local. Valide uniquement si la propriété **WINSEnableLMHostsLookup** a la **valeur true**.

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| DeviceIoControl »)
</dt> </dl>

Adresse IP du serveur WINS principal.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ tcpip \\ \\ Parameters \| ScopeId")
</dt> </dl>

Valeur ajoutée à la fin du nom NetBIOS qui isole un groupe de systèmes informatiques communiquant les uns avec les autres. Elle est utilisée pour toutes les transactions NetBIOS sur les communications TCP/IP à partir de ce système informatique. Les ordinateurs configurés avec des identificateurs d’étendue identiques sont en mesure de communiquer avec cet ordinateur. Les clients TCP/IP avec des identificateurs d’étendue différents ignorent les paquets des ordinateurs ayant cet identificateur d’étendue. Valide uniquement lorsque la méthode [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) s’exécute correctement.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| DeviceIoControl »)
</dt> </dl>

Adresse IP du serveur WINS secondaire.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ NetworkAdapterConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

## <a name="examples"></a>Exemples

L’exemple de code VBScript de l' [extracteur d’informations WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) sur la Galerie TechNet utilise la classe **Win32 \_ NetworkAdapterConfiguration** pour récupérer des informations de configuration réseau à partir d’un certain nombre d’ordinateurs distants.

L’exemple PowerShell- [ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sur la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, notamment **Win32 \_ NetworkAdapterConfiguration**, pour afficher des informations sur un système local ou distant.

Le code PowerShell suivant récupère les paramètres de configuration de l’adaptateur Microsoft ISTAP.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



L’exemple C suivant \# récupère la description et le numéro d’index de toutes les instances de configuration de carte réseau. Notez que cet \# exemple C utilise l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , qui est généralement mis à l’échelle plus efficacement que les classes WMI d’espace de noms [System. Management](/dotnet/api/system.management) .


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



L’exemple C suivant \# récupère la description et le numéro d’index de toutes les instances de configuration de carte réseau. Notez que cet \# exemple C utilise l’espace de noms [System. Management](/dotnet/api/system.management) d’origine, qui a été remplacé par [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).


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



L’exemple suivant récupère des informations de la classe **Win32 \_ NetworkAdapterConfiguration** .


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[Tâches WMI : mise en réseau](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Tâches WMI : comptes et domaines](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[Prise en charge D’ipv6 et IPv6 dans WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
