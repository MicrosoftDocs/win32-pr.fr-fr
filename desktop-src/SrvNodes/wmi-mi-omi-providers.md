---
description: Windows Management infrastructure (WMI), Management Instrumentation (MI) et Open Management infrastructure (OMI) utilisent tous des fichiers MOF (Management Object Format) pour décrire les informations mises à disposition par leurs fournisseurs respectifs.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Fournisseurs WMI/MI/OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682629f72da94cd2210fb781284a7cb4cf7f85868ff405f22727e619d128ae65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992415"
---
# <a name="wmimiomi-providers"></a>Fournisseurs WMI/MI/OMI

Windows Management infrastructure (WMI), Management Instrumentation (MI) et Open Management infrastructure (OMI) utilisent tous des fichiers MOF (Management Object Format) pour décrire les informations mises à disposition par leurs fournisseurs respectifs.

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

Le fournisseur Active Directory, également connu sous le nom de fournisseur des services d’annuaire, mappe les objets Active Directory à WMI. En accédant à l’espace de noms LDAP (Lightweight Directory Access Protocol) dans WMI, vous pouvez référencer un objet ou en faire un alias dans le Active Directory.

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Inventaire des applications](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

les classes WMI pour l’inventaire des applications permettent la découverte des applications Win32 installées et des applications de Windows store sur un système Windows.

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Proxy d’application](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

Le fournisseur WMI de proxy d’application permet aux développeurs d’accéder au service de proxy d’application Web pour que les administrateurs puissent publier des applications pour un accès externe. Le proxy d’application Web est un proxy inverse pour services de fédération Active Directory (AD FS) (AD FS).

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Chiffrement de lecteur BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

Fournit la configuration et la gestion d’une zone de stockage sur un lecteur de disque dur, représenté par une instance de [**\_ EncryptableVolume Win32**](/windows/desktop/SecProv/win32-encryptablevolume), qui peut être protégée à l’aide du chiffrement.

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

le serveur Compact Service de transfert intelligent en arrière-plan (bits) avec la gestion à distance bits permet aux administrateurs authentifiés ou aux applications de contrôleur de créer, modifier et gérer des tâches de transfert bits à distance sans utiliser le Service Internet Information Services (IIS).

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

Fournit l’accès aux objets d’administration de BizTalk représentés par les classes WMI.

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Données de configuration de démarrage (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

Le fournisseur Données de configuration de démarrage (BCD) (BCD) fournit un magasin utilisé pour décrire les applications de démarrage et les paramètres d’application de démarrage.

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Collecteur d’événements de démarrage](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server.

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, événements de gestion de l’alimentation](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

Les fournisseurs CIMWin32 prennent en charge les classes implémentées dans CimWin32.dll et se composent des classes CIM principales, de l’implémentation Win32 de ces classes et des événements de gestion de l’alimentation.

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

Le fournisseur CIMWin32a étend les classes disponibles dans le [cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

Le fournisseur DcbQosCim prend en charge les classes qui décrivent les données de paramètre QOS réseau, les données de paramètre de contrôle et les données de paramètres de classe de trafic.

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Système de fichiers DFS (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

Le fournisseur DFS fournit des fonctions DFS scriptables via WMI.

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Réplication de système de fichiers DFS (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

Crée des outils pour configurer et surveiller le service [système de fichiers DFS (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) . Pour plus d’informations, consultez [classes WMI DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

Le fournisseur [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) prend en charge les classes qui implémentent l’accès à l’espace de noms DFS.

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

Le fournisseur [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) prend en charge les classes qui interagissent avec un serveur DHCP (Dynamic Host Configuration Protocol).

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Quota de disque](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

le fournisseur de quotas de disque Windows permet aux administrateurs de contrôler la quantité de données que chaque utilisateur stocke sur un système de fichiers NTFS.

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

Le fournisseur DTC permet de gérer le DTC.

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[DN](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

Permet aux administrateurs et aux programmeurs de configurer des enregistrements de ressources DNS (Domain Name System) et des serveurs DNS à l’aide de WMI.

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Classes du fournisseur Dnsclientcim](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

Le fournisseur Dnsclientcim prend en charge les classes qui interagissent avec un client DNS (Domain Name System).

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

Le fournisseur [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) prend en charge les classes WMI qui interagissent avec un client DNS.

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

Le fournisseur [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) prend en charge les classes WMI qui interagissent avec un serveur DNS.

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

Le fournisseur du [Journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider) fournit l’accès aux données du service journal des événements et la notification des événements.

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Gestion du suivi des événements](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

le fournisseur de gestion du suivi d’événements fournit l’accès aux configurations de session de journalisation automatique Suivi d’v nements pour Windows (ETW) et aux événements de trace.

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Mise à jour du Cluster-Aware de basculement](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

Le fournisseur de mise à jour de Cluster-Aware de basculement prend en charge la coordination avec et la gestion de la mise à jour adaptée aux clusters.

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Clustering de basculement Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

Le fournisseur Hyper-V de clustering de basculement fournit la gestion et la création de rapports d’Hyper-V dans un environnement de clustering.

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[clustering de basculement Stockage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

le clustering de basculement Stockage fournisseur de qualité de Service (qos) fournit la gestion et la création de rapports des stratégies qos de stockage du clustering.

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Fournisseur de cluster de basculement v1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

Le fournisseur de cluster de basculement v1 assure la gestion d’un cluster de basculement.

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Extensions v1 du cluster de basculement](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

Le fournisseur d’extensions de cluster de basculement fournit une gestion supplémentaire d’un cluster de basculement.

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Health Monitor de la passerelle](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

le fournisseur de Health Monitor de passerelle gère les événements et les informations de surveillance de l’intégrité de la passerelle.

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[API stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

Le fournisseur stratégie de groupe permet l’administration basée sur des stratégies à l’aide des services d’annuaire Microsoft Active Directory (AD).

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Service Guardian hôte](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

Le fournisseur de service Guardian hôte assure la gestion du service Guardian hôte pour les machines virtuelles protégées.

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

Le fournisseur Hyper-V vous permet de gérer et de récupérer des informations sur les machines virtuelles.

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

Le fournisseur Hyper-V (v2) étend le fournisseur [Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) .

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

Expose des interfaces de programmation qui peuvent être utilisées pour interroger et configurer la métabase IIS.

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[serveur de gestion des adresses ip (IPAM)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

le fournisseur IPAM Server permet aux développeurs de gérer des IPAM par le biais de WMI.

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Fournisseur d’itinéraires IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

Le fournisseur d’itinéraires IP préinstallé fournit des informations de routage réseau IPV4, y compris (mais sans s’y limiter) les informations disponibles via la commande **route print** .

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Interface de gestion de plateforme intelligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

Fournit des données IPMI à partir des opérations du contrôleur BMC (Baseboard Management Controller).

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Serveur cible iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

le fournisseur Serveur cible iSCSI prend en charge une interface WMI pour la gestion des Serveur cible iSCSI Microsoft, telles que la création de disques virtuels et la présentation du client au client.

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Objet de traitement](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

Le fournisseur d’objets de tâche prend en charge l’accès aux données relatives aux objets de travail de noyau nommés.

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Suivi du noyau](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

Le fournisseur d’événements de trace du noyau préinstallé vous permet de voir les événements de trace du noyau lors de la création du processus, de l’arrêt du processus, de la création du thread, de l’arrêt du thread et du chargement du module.

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

Fournit des classes qui créent, inscrivent, configurent et gèrent des applications SIP (Session Initiation Protocol) personnalisées avec [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registre des outils de gestion](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

Le fournisseur de registre des outils de gestion fournit un accès à distance au registre.

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Gestionnaire des tâches des outils de gestion](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

Le fournisseur du gestionnaire des tâches des outils d’administration fournit l’accès et la gestion des données du gestionnaire des tâches.

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Application MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

Le fournisseur d’applications de gestion des appareils mobiles (MDM) gère les applications sur les appareils qui sont abonnés au service MDM.

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Pont MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

Le fournisseur de pont MDM active la gestion MDM d’un pont réseau.

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Paramètres MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

le fournisseur de Paramètres mdm permet de gérer les paramètres sur les appareils inscrits auprès d’un service mdm.

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[\_PCSVDEVICE msft](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

Le [fournisseur \_ PCSVDevice msft](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) expose une classe qui définit une classe d’affichage pour un système informatique physique.

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

La section du fournisseur [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) fournit des informations de référence pour les classes de fournisseur MsNetImPlatform implémentées dans NdisIMPlatCim.dll.

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

Le fournisseur [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) prend en charge les classes qui accèdent aux cartes réseau.

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

Cette section fournit des informations de référence pour les classes de fournisseur [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) .

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

Fournit des informations de référence pour les classes de fournisseur [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) .

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

Le fournisseur [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) prend en charge les classes qui interagissent avec l’infrastructure du cache de branche.

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

Le fournisseur [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) fournit des données pour la qualité de service (QoS) du réseau et les données de paramètre de QoS.

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

Cette section fournit des informations de référence pour les classes de fournisseur NetSwitchTeam déclarées dans NetSwitchTeam. mof et implémentées dans NetSwitchTeamCim.dll.

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[TCP TCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

Le fournisseur Nettcpip prend en charge les classes qui interagissent avec les connexions TCPIP.

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

Cette section fournit des informations de référence pour les classes de fournisseur NetTtCim définies dans NetTtCim. mof et implémentées dans NetTtCim.dll.

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

Le fournisseur NetWNV prend en charge les classes qui interagissent avec les technologies de virtualisation réseau.

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Protection d’accès réseau](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

Le fournisseur de protection d’accès réseau expose une plateforme pour l’accès protégé aux réseaux privés.

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Équilibrage de la charge réseau](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

Le fournisseur d’équilibrage de la charge réseau (NLB) permet la gestion d’un cluster NLB.

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Serveur NetworkController](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

Le fournisseur permet la gestion d’un serveur de contrôleur de réseau.

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

le fournisseur pour NFS vous permet de créer des outils et des scripts pour configurer et surveiller le Windows système de fichiers réseau.

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

Le fournisseur ping fournit l’accès aux informations d’État fournies par la commande ping standard.

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Renvoi](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

Fournit des extensions à la stratégie de groupe et permet d’affiner l’application de la stratégie.

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Compteur d’alimentation](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

Le fournisseur de contrôle d’alimentation prend en charge l’interface de contrôle d’alimentation et de budgétisation (PMB). Ces classes sont l’interface principale pour la requête d’informations de l’interface de contrôle d’alimentation (PMI) à partir des compteurs d’alimentation sous-jacents sur le système.

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Stratégie d’alimentation](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

Le fournisseur de stratégie d’alimentation fournit des classes qui permettent de gérer à distance toute l’infrastructure de la stratégie d’alimentation.

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

Le fournisseur [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) fournit des classes pour gérer l’accès à distance.

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

Le fournisseur [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) fournit des classes pour gérer le serveur d’accès à distance.

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

le fournisseur [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) expose les mesures de fiabilité du journal des événements système et Windows.

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Services Bureau à distance](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

Permet une administration de serveur cohérente dans un environnement Services Bureau à distance.

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

Définit des classes qui vous permettent d’écrire des scripts et du code pour modifier les paramètres du serveur de rapports et du Gestionnaire de rapports.

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Jeu de stratégie résultant (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

Fournit des méthodes pour planifier et déboguer des paramètres de stratégie dans une situation de simulation. Ces méthodes permettent aux administrateurs de déterminer facilement la combinaison des paramètres de stratégie qui s’appliquent à un utilisateur ou à un ordinateur, ou s’appliquent à celui-ci. C’est ce que l’on appelle le jeu de stratégie résultant (RSoP). Pour plus d’informations, consultez [à propos du fournisseur de méthodes WMI RSoP](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) et des [classes WMI RSoP](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Caution](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

Récupère ou modifie les paramètres de sécurité qui contrôlent la propriété, l’audit et les droits d’accès aux fichiers, répertoires et partages.

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) expose les fonctionnalités de déploiement.

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Session](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

Gère les sessions et les connexions réseau.

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Cliché instantané](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

Fournit des fonctions de gestion pour les clichés instantanés de la fonctionnalité dossiers partagés.

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Approvisionnement de machines virtuelles protégées](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

Le fournisseur d’approvisionnement de machine virtuelle protégé permet à un contrôleur de structure de démarrer l’approvisionnement sécurisé d’une machine virtuelle protégée sur un ordinateur hôte Hyper-V.

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Service de provisionnement de machines virtuelles protégées](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

Le fournisseur permet la configuration d’un ordinateur virtuel protégé.

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Gestion SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

L’API de gestion SMB fournit des classes et des méthodes pour gérer les partages et l’accès au partage.

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[SMTP](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

Cartes Objets SNMP (simple Network Management Protocol) définis dans les objets de schéma MIB (Management Information base) aux classes. Pour plus d’informations, consultez [configuration de l’environnement SNMP WMI](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Journalisation de l’inventaire logiciel](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

le fournisseur de journalisation de l’inventaire logiciel recueille les données de licence relatives aux logiciels installés sur un serveur Windows et fournit un accès à distance aux données afin de pouvoir les agréger facilement à l’aide d’un centre de données.

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[licences logicielles pour Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

[Classes de licences logicielles](/previous-versions/windows/desktop/sppwmi/software-license-provider-) utilisées pour Windows Vista.

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Licence logicielle](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

Le fournisseur de licences logicielles récupère les données de licence logicielle.

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Stockage Agrégat](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

le fournisseur de volume Stockage fournit des fonctions de gestion de volume.

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Stockage Double](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

Le fournisseur permet la gestion d’un réplica de stockage.

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

Le fournisseur de Registre système permet aux applications de gestion de récupérer et de modifier des données dans le registre système, et de recevoir des notifications lorsque des modifications se produisent.

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Restauration du système](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

Fournit des classes qui configurent et utilisent la fonctionnalité de restauration du système. Pour plus d’informations, consultez Configuration de la [restauration du système](/windows/desktop/sr/configuring-system-restore) et des [classes WMI de restauration du système](/windows/desktop/sr/system-restore-wmi-classes).

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Module de plateforme sécurisée (TPM)](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

fournit l’accès aux données relatives à un appareil de sécurité, représenté par une instance de [**\_ TPM Win32**](/windows/desktop/SecProv/win32-tpm), qui est la racine de l’approbation pour un système informatique de plateforme sécurisée Microsoft Windows.

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

Le fournisseur [TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) est un fournisseur d’instances qui crée des classes avec des informations sur les relations d’approbation entre les domaines.

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Journalisation des accès utilisateur](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

la journalisation des accès utilisateur est un framework commun pour les rôles de serveur Windows pour signaler leurs mesures de consommation respectives.

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

le fournisseur [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) expose des classes qui fournissent des informations sur un profil utilisateur sur un système Windows, ainsi que l’état d’intégrité d’un dossier utilisateur redirigé.

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Gestion de l’état utilisateur](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

Le fournisseur de gestion de l’état utilisateur expose une API de gestion et de création de rapports pour les scénarios d’entreprise.

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[Affichage](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

Crée des instances et des méthodes basées sur des instances d’autres classes. Deux versions du fournisseur d’affichages sont disponibles sur les plateformes 64 bits.

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

Le fournisseur [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) expose une plateforme pour l’automatisation de la connectivité à un client de réseau privé virtuel.

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

permet d’accéder aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au Windows Driver Model (WDM).

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

Le fournisseur [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) expose les fonctionnalités de sécurité et de filtrage du réseau.

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

Le fournisseur [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) expose des informations de signature numérique sur les pilotes.

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

Le fournisseur [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) expose les horodateurs actuels, locaux et UTC sur un système informatique.

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Composants d’accès aux données (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

Fournit la gestion de WDAC.

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

le fournisseur Windows Defender expose Windows Defender fonctionnalités de sécurité.

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows D'](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

le fournisseur Windows Installer, également connu sous le nom de fournisseur MSI, permet aux applications d’accéder aux informations collectées à partir d’applications conformes Windows Installer.

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Activation du produit](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

le fournisseur WPA (Windows Product Activation) est une technologie anti-piratage visant à réduire la copie occasionnelle des logiciels.

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Gestionnaire de serveur](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

Le fournisseur permet l’accès et la gestion de la configuration contrôlée par l’application Gestionnaire de serveur.

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows gestion des Stockage de serveur (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

le fournisseur MsftStrgMan fournit la gestion des systèmes de stockage sur les produits Windows Server.

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[gestion de la Stockage Windows (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

Le fournisseur StrgMgmt peut être utilisé pour gérer un large éventail de configurations de stockage, de tablettes à des groupes de stockage externes sur les serveurs.

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows Outil d’évaluation du système](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

l’outil Windows System Assessment Tool (winsat) expose un certain nombre de classes qui évaluent les caractéristiques de performances et les fonctionnalités d’un ordinateur.

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[Noyau WMI](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

Le fournisseur principal WMI définit des classes qui composent les fonctionnalités de base de WMI.

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[\_ProviderSubSystem msft](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

Le [fournisseur \_ ProviderSubSystem msft](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) prend en charge les fournisseurs.

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[\_Performances Win32](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

La classe abstraite de performances [**\_ Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) est la classe de base pour les classes de compteur de performance [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) et [**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov). Il définit les propriétés timestamp et Frequency nécessaires utilisées dans les algorithmes de la classe de compteur de performance.

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**\_PerfFormattedData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

Classe de base abstraite pour les classes de données calculées préinstallées.

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**\_PerfRawData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

La classe de compteur de performance [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) est la classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes. Pour apparaître dans le moniteur système, les classes de compteur de performance doivent être ajoutées à l' \\ espace de noms root cimv2 et dérivées de **Win32 \_ PerfRawData**.

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

Crée les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI. Les données sont fournies dynamiquement à ces classes de performance par le fournisseur WMIPerfInst.

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

Fournit des données de compteur de performances brutes et mises en forme de manière dynamique à partir des définitions de [classe de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) .

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Dossiers de travail](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

Dossiers de travail permet de synchroniser des fichiers avec plusieurs ordinateurs et appareils mobiles.

</dd> </dl>

 

 
