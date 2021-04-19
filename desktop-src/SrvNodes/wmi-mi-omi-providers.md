---
description: WMI (Windows Management Infrastructure), MI (Management Instrumentation) et OMI (Open Management Infrastructure) utilisent tous des fichiers MOF (Management Object Format) pour décrire les informations mises à disposition par leurs fournisseurs respectifs.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Fournisseurs WMI/MI/OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505a0853d9df7d9cf6f2371f6342b77f61f536b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522476"
---
# <a name="wmimiomi-providers"></a><span data-ttu-id="25c78-103">Fournisseurs WMI/MI/OMI</span><span class="sxs-lookup"><span data-stu-id="25c78-103">WMI/MI/OMI Providers</span></span>

<span data-ttu-id="25c78-104">WMI (Windows Management Infrastructure), MI (Management Instrumentation) et OMI (Open Management Infrastructure) utilisent tous des fichiers MOF (Management Object Format) pour décrire les informations mises à disposition par leurs fournisseurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="25c78-104">Windows Management Infrastructure (WMI), Management Instrumentation (MI) and Open Management Infrastructure (OMI) all use Management Object Format (MOF) files to describe the information made available through their respective providers.</span></span>

<dl> <dt>

<span data-ttu-id="25c78-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-106">Le fournisseur Active Directory, également connu sous le nom de fournisseur des services d’annuaire, mappe les objets Active Directory à WMI.</span><span class="sxs-lookup"><span data-stu-id="25c78-106">The Active Directory provider, also known as the Directory Services (DS) provider, maps Active Directory objects to WMI.</span></span> <span data-ttu-id="25c78-107">En accédant à l’espace de noms LDAP (Lightweight Directory Access Protocol) dans WMI, vous pouvez référencer un objet ou en faire un alias dans le Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25c78-107">By accessing the Lightweight Directory Access Protocol (LDAP) namespace in WMI, you can reference or make an object an alias in the Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Inventaire des applications](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Application Inventory](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-109">Les classes WMI pour l’inventaire des applications permettent la découverte des applications Win32 installées et des applications du Windows Store sur un système Windows.</span><span class="sxs-lookup"><span data-stu-id="25c78-109">The WMI classes for Application Inventory enable discovery of the installed Win32 applications and Windows store applications on a Windows system.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Proxy d’application](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Application Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-111">Le fournisseur WMI de proxy d’application permet aux développeurs d’accéder au service de proxy d’application Web pour que les administrateurs puissent publier des applications pour un accès externe.</span><span class="sxs-lookup"><span data-stu-id="25c78-111">Application Proxy WMI Provider enables developers to access the Web Application Proxy service so administrators can publish applications for external access.</span></span> <span data-ttu-id="25c78-112">Le proxy d’application Web est un proxy inverse pour services de fédération Active Directory (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="25c78-112">Web Application Proxy is a reverse proxy for Active Directory Federation Services (AD FS).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Chiffrement de lecteur BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker Drive Encryption (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-114">Fournit la configuration et la gestion d’une zone de stockage sur un lecteur de disque dur, représenté par une instance de [**\_ EncryptableVolume Win32**](/windows/desktop/SecProv/win32-encryptablevolume), qui peut être protégée à l’aide du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="25c78-114">Provides configuration and management for an area of storage on a hard disk drive, represented by an instance of [**Win32\_EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), that can be protected by using encryption.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-115"><span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-115"><span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-116">Le serveur compact Service de transfert intelligent en arrière-plan (BITS) avec la gestion à distance BITS permet aux administrateurs authentifiés ou aux applications de contrôleur de créer, modifier et gérer des tâches de transfert BITS à distance sans utiliser le service Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="25c78-116">The Background Intelligent Transfer Service (BITS) Compact Server with BITS Remote Management allows authenticated administrators or controller applications to create, modify and manage BITS transfer jobs remotely without using the Internet Information Services (IIS) service.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span><span class="sxs-lookup"><span data-stu-id="25c78-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-118">Fournit l’accès aux objets d’administration de BizTalk représentés par les classes WMI.</span><span class="sxs-lookup"><span data-stu-id="25c78-118">Supplies access to the BizTalk administration objects represented by WMI classes.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Données de configuration de démarrage (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Boot Configuration Data](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-120">Le fournisseur Données de configuration de démarrage (BCD) (BCD) fournit un magasin utilisé pour décrire les applications de démarrage et les paramètres d’application de démarrage.</span><span class="sxs-lookup"><span data-stu-id="25c78-120">The Boot Configuration Data (BCD) provider provides a store that is used to describe boot applications and boot application settings.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Collecteur d’événements de démarrage](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Boot Event Collector](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-122">Le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server.</span><span class="sxs-lookup"><span data-stu-id="25c78-122">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, événements de gestion de l’alimentation](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span><span class="sxs-lookup"><span data-stu-id="25c78-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Power Management Events](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-124">Les fournisseurs CIMWin32 prennent en charge les classes implémentées dans CimWin32.dll et se composent des classes CIM principales, de l’implémentation Win32 de ces classes et des événements de gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="25c78-124">The CIMWin32 providers support the classes implemented in CimWin32.dll, and consist of the core CIM classes, the Win32 implementation of those classes, and power management events.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-126">Le fournisseur CIMWin32a étend les classes disponibles dans le [cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span><span class="sxs-lookup"><span data-stu-id="25c78-126">The CIMWin32a provider extends the classes available in the [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span><span class="sxs-lookup"><span data-stu-id="25c78-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-128">Le fournisseur DcbQosCim prend en charge les classes qui décrivent les données de paramètre QOS réseau, les données de paramètre de contrôle et les données de paramètres de classe de trafic.</span><span class="sxs-lookup"><span data-stu-id="25c78-128">The DcbQosCim provider supports classes that describe Network QOS setting data, control setting data, and traffic class setting data.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Système de fichiers DFS (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Distributed File System (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-130">Le fournisseur DFS fournit des fonctions DFS scriptables via WMI.</span><span class="sxs-lookup"><span data-stu-id="25c78-130">The DFS provider supplies scriptable DFS functions through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Réplication de système de fichiers DFS (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span><span class="sxs-lookup"><span data-stu-id="25c78-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-132">Crée des outils pour configurer et surveiller le service [système de fichiers DFS (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) .</span><span class="sxs-lookup"><span data-stu-id="25c78-132">Creates tools for configuring and monitoring the [Distributed File System (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) service.</span></span> <span data-ttu-id="25c78-133">Pour plus d’informations, consultez [classes WMI DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="25c78-133">For more information, see [DFSR WMI Classes](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-135">Le fournisseur [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) prend en charge les classes qui implémentent l’accès à l’espace de noms DFS.</span><span class="sxs-lookup"><span data-stu-id="25c78-135">The [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) provider supports classes that implement DFS namespace access.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-137">Le fournisseur [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) prend en charge les classes qui interagissent avec un serveur DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="25c78-137">The [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) provider supports classes that interact with a dynamic host configuration protocol (DHCP) server.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Quota de disque](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Disk Quota](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-139">Le fournisseur de quotas de disque Windows permet aux administrateurs de contrôler la quantité de données que chaque utilisateur stocke sur un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="25c78-139">The Windows Disk Quota provider allows administrators to control the amount of data that each user stores on an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-141">Le fournisseur DTC permet de gérer le DTC.</span><span class="sxs-lookup"><span data-stu-id="25c78-141">The DTC provider enables management of the DTC.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-142"><span id="DNS"></span><span id="dns"></span>[DN](/windows/desktop/DNS/dns-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-142"><span id="DNS"></span><span id="dns"></span>[DNS](/windows/desktop/DNS/dns-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-143">Permet aux administrateurs et aux programmeurs de configurer des enregistrements de ressources DNS (Domain Name System) et des serveurs DNS à l’aide de WMI.</span><span class="sxs-lookup"><span data-stu-id="25c78-143">Enables administrators and programmers to configure Domain Name System (DNS) resource records (RRs) and DNS Servers using WMI.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Classes du fournisseur Dnsclientcim](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim Provider Classes](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-145">Le fournisseur Dnsclientcim prend en charge les classes qui interagissent avec un client DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="25c78-145">The Dnsclientcim provider supports classes that interact with a Domain Name System (DNS) client.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-147">Le fournisseur [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) prend en charge les classes WMI qui interagissent avec un client DNS.</span><span class="sxs-lookup"><span data-stu-id="25c78-147">The [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) provider supports WMI classes that interact with a DNS client.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-149">Le fournisseur [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) prend en charge les classes WMI qui interagissent avec un serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="25c78-149">The [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) provider supports WMI classes that interact with a DNS server.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-151">Le fournisseur du [Journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider) fournit l’accès aux données du service journal des événements et la notification des événements.</span><span class="sxs-lookup"><span data-stu-id="25c78-151">The [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supplies access to data from the event log service, and notification of events.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Gestion du suivi des événements](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Event Tracing Management](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-153">Le fournisseur de gestion du suivi d’événements fournit l’accès aux configurations de session de journalisation automatique Suivi d’v nements pour Windows (ETW) et aux événements de trace.</span><span class="sxs-lookup"><span data-stu-id="25c78-153">The Event Tracing Management provider provides access to Event Tracing for Windows (ETW) autologger session configurations and trace events.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Mise à jour du Cluster-Aware de basculement](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Updating](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-155">Le fournisseur de mise à jour de Cluster-Aware de basculement prend en charge la coordination avec et la gestion de la mise à jour adaptée aux clusters.</span><span class="sxs-lookup"><span data-stu-id="25c78-155">The Failover Cluster-Aware Updating (CAU) provider supports coordination with and management of CAU.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Clustering de basculement Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failover Clustering Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-157">Le fournisseur Hyper-V de clustering de basculement fournit la gestion et la création de rapports d’Hyper-V dans un environnement de clustering.</span><span class="sxs-lookup"><span data-stu-id="25c78-157">The Failover Clustering Hyper-V provider provides management and reporting of Hyper-V in a clustering environment.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[QoS de stockage du clustering de basculement](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Failover Clustering Storage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-159">Le fournisseur de qualité de service (QoS) de stockage du clustering de basculement fournit la gestion et la création de rapports des stratégies QoS de stockage de cluster.</span><span class="sxs-lookup"><span data-stu-id="25c78-159">The Failover Clustering Storage Quality of Service (QoS) provider provides management and reporting of the clustering storage QoS policies.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Fournisseur de cluster de basculement v1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failover Cluster V1 Provider](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-161">Le fournisseur de cluster de basculement v1 assure la gestion d’un cluster de basculement.</span><span class="sxs-lookup"><span data-stu-id="25c78-161">The Failover Cluster V1 provider provides management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Extensions v1 du cluster de basculement](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failover Cluster V1 Extensions](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-163">Le fournisseur d’extensions de cluster de basculement fournit une gestion supplémentaire d’un cluster de basculement.</span><span class="sxs-lookup"><span data-stu-id="25c78-163">The Failover Cluster Extensions provider provides additional management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Moniteur d’intégrité de la passerelle](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gateway Health Monitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-165">Le fournisseur du moniteur d’intégrité de la passerelle gère les événements et les informations de surveillance de l’intégrité de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="25c78-165">The Gateway Health Monitor provider manages gateway health monitoring events and information.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[API stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span><span class="sxs-lookup"><span data-stu-id="25c78-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Group Policy API](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-167">Le fournisseur stratégie de groupe permet l’administration basée sur des stratégies à l’aide des services d’annuaire Microsoft Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="25c78-167">The Group Policy provider enables policy-based administration using Microsoft Active Directory (AD) directory services.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Service Guardian hôte](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host Guardian Service](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-169">Le fournisseur de service Guardian hôte assure la gestion du service Guardian hôte pour les machines virtuelles protégées.</span><span class="sxs-lookup"><span data-stu-id="25c78-169">The Host Guardian Service provider provides management of the Host Guardian Service for shielded VMs.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-171">Le fournisseur Hyper-V vous permet de gérer et de récupérer des informations sur les machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="25c78-171">The Hyper-V provider allows you to manage and retrieve information about virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-173">Le fournisseur Hyper-V (v2) étend le fournisseur [Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) .</span><span class="sxs-lookup"><span data-stu-id="25c78-173">The Hyper-V (V2) provider extends the [Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) provider.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="25c78-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span></span>
</dt> <dd>

<span data-ttu-id="25c78-175">Expose des interfaces de programmation qui peuvent être utilisées pour interroger et configurer la métabase IIS.</span><span class="sxs-lookup"><span data-stu-id="25c78-175">Exposes programming interfaces that can be used to query and configure the IIS metabase.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Serveur de gestion des adresses IP (IPAM)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Internet Protocol Address Management (IPAM) Server](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-177">Le fournisseur de serveur IPAM permet aux développeurs de gérer IPAM via WMI.</span><span class="sxs-lookup"><span data-stu-id="25c78-177">The IPAM Server Provider enables developers to manage IPAM through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Fournisseur d’itinéraires IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-179">Le fournisseur d’itinéraires IP préinstallé fournit des informations de routage réseau IPV4, y compris (mais sans s’y limiter) les informations disponibles via la commande **route print** .</span><span class="sxs-lookup"><span data-stu-id="25c78-179">The preinstalled IP Route provider supplies IPV4 network routing information, including (but not limited to) the information available through the **route print** command.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Interface de gestion de plateforme intelligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-181">Fournit des données IPMI à partir des opérations du contrôleur BMC (Baseboard Management Controller).</span><span class="sxs-lookup"><span data-stu-id="25c78-181">Supplies IPMI data from Baseboard Management Controller (BMC) operations.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Serveur cible iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI Target Server](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-183">Le fournisseur de serveur cible iSCSI prend en charge une interface WMI pour la gestion du serveur cible Microsoft iSCSI, telle que la création de disques virtuels, et la présentation du client au client.</span><span class="sxs-lookup"><span data-stu-id="25c78-183">The iSCSI Target Server provider supports a WMI interface for managing the Microsoft iSCSI Target Server, such as creating virtual disks, and for presenting them to the client.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Objet de traitement](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Job Object](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-185">Le fournisseur d’objets de tâche prend en charge l’accès aux données relatives aux objets de travail de noyau nommés.</span><span class="sxs-lookup"><span data-stu-id="25c78-185">The Job Object provider supports access to data about named kernel job objects.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Suivi du noyau](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel Trace](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-187">Le fournisseur d’événements de trace du noyau préinstallé vous permet de voir les événements de trace du noyau lors de la création du processus, de l’arrêt du processus, de la création du thread, de l’arrêt du thread et du chargement du module.</span><span class="sxs-lookup"><span data-stu-id="25c78-187">The preinstalled Kernel Trace event provider allows you to see kernel trace events on Process creation, Process termination, Thread creation, Thread termination and module load.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span><span class="sxs-lookup"><span data-stu-id="25c78-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span></span>
</dt> <dd>

<span data-ttu-id="25c78-189">Fournit des classes qui créent, inscrivent, configurent et gèrent des applications SIP (Session Initiation Protocol) personnalisées avec [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span><span class="sxs-lookup"><span data-stu-id="25c78-189">Provides classes that create, register, configure, manage custom Session Initiation Protocol (SIP) applications with the [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registre des outils de gestion](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Management Tools Registry](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-191">Le fournisseur de registre des outils de gestion fournit un accès à distance au registre.</span><span class="sxs-lookup"><span data-stu-id="25c78-191">The Management Tools Registry provider provides remote access to the registry.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Gestionnaire des tâches des outils de gestion](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Management Tools Task Manager](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-193">Le fournisseur du gestionnaire des tâches des outils d’administration fournit l’accès et la gestion des données du gestionnaire des tâches.</span><span class="sxs-lookup"><span data-stu-id="25c78-193">The Management Tools Task Manager provider provides access and management of the Task Manager data.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Application MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM Application](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-195">Le fournisseur d’applications de gestion des appareils mobiles (MDM) gère les applications sur les appareils qui sont abonnés au service MDM.</span><span class="sxs-lookup"><span data-stu-id="25c78-195">The Mobile Device Management (MDM) application provider manages applications on devices that are subscribed to the MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Pont MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-197">Le fournisseur de pont MDM active la gestion MDM d’un pont réseau.</span><span class="sxs-lookup"><span data-stu-id="25c78-197">The MDM Bridge provider enables MDM management of a network bridge.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Paramètres MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM Settings](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-199">Le fournisseur de paramètres MDM permet de gérer les paramètres sur les appareils inscrits auprès d’un service MDM.</span><span class="sxs-lookup"><span data-stu-id="25c78-199">The MDM Settings Provider enables management of settings on devices enrolled with a MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[\_PCSVDEVICE msft](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-201">Le [fournisseur \_ PCSVDevice msft](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) expose une classe qui définit une classe d’affichage pour un système informatique physique.</span><span class="sxs-lookup"><span data-stu-id="25c78-201">The [MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) provider exposes a class that defines a view class for a physical computer system.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-203">La section du fournisseur [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) fournit des informations de référence pour les classes de fournisseur MsNetImPlatform implémentées dans NdisIMPlatCim.dll.</span><span class="sxs-lookup"><span data-stu-id="25c78-203">The [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) provider section provides reference information for MsNetImPlatform provider classes implemented in NdisIMPlatCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-205">Le fournisseur [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) prend en charge les classes qui accèdent aux cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="25c78-205">The [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) provider supports classes that access network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-207">Cette section fournit des informations de référence pour les classes de fournisseur [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) .</span><span class="sxs-lookup"><span data-stu-id="25c78-207">This section provides reference information for [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) Provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span><span class="sxs-lookup"><span data-stu-id="25c78-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-209">Fournit des informations de référence pour les classes de fournisseur [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) .</span><span class="sxs-lookup"><span data-stu-id="25c78-209">Provides reference information for [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span><span class="sxs-lookup"><span data-stu-id="25c78-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-211">Le fournisseur [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) prend en charge les classes qui interagissent avec l’infrastructure du cache de branche.</span><span class="sxs-lookup"><span data-stu-id="25c78-211">The [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) provider supports classes that interact with the Branch Cache infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-213">Le fournisseur [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) fournit des données pour la qualité de service (QoS) du réseau et les données de paramètre de QoS.</span><span class="sxs-lookup"><span data-stu-id="25c78-213">The [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) provider supplies data for network quality of service (QoS) and QoS setting data.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-215">Cette section fournit des informations de référence pour les classes de fournisseur NetSwitchTeam déclarées dans NetSwitchTeam. mof et implémentées dans NetSwitchTeamCim.dll.</span><span class="sxs-lookup"><span data-stu-id="25c78-215">This section provides reference information for NetSwitchTeam provider classes declared in NetSwitchTeam.mof and implemented in NetSwitchTeamCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[TCP TCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-217">Le fournisseur Nettcpip prend en charge les classes qui interagissent avec les connexions TCPIP.</span><span class="sxs-lookup"><span data-stu-id="25c78-217">The NetTCPIP provider supports classes that interact with TCPIP connections.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-219">Cette section fournit des informations de référence pour les classes de fournisseur NetTtCim définies dans NetTtCim. mof et implémentées dans NetTtCim.dll.</span><span class="sxs-lookup"><span data-stu-id="25c78-219">This section provides reference information for NetTtCim provider classes defined in NetTtCim.mof and implemented in NetTtCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-221">Le fournisseur NetWNV prend en charge les classes qui interagissent avec les technologies de virtualisation réseau.</span><span class="sxs-lookup"><span data-stu-id="25c78-221">The NetWNV provider supports classes that interact with net virtualization technologies.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Protection d’accès réseau](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Network Access Protection](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-223">Le fournisseur de protection d’accès réseau expose une plateforme pour l’accès protégé aux réseaux privés.</span><span class="sxs-lookup"><span data-stu-id="25c78-223">The Network Access Protection provider exposes a platform for protected access to private networks.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Équilibrage de la charge réseau](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Network Load Balancing](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-225">Le fournisseur d’équilibrage de la charge réseau (NLB) permet la gestion d’un cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="25c78-225">The Network Load Balancing (NLB) Provider enables management of a NLB cluster.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Serveur NetworkController](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-227">Le fournisseur permet la gestion d’un serveur de contrôleur de réseau.</span><span class="sxs-lookup"><span data-stu-id="25c78-227">The provider enables management of a network controller server.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-229">Le fournisseur pour NFS vous permet de créer des outils et des scripts pour configurer et surveiller le système de fichiers réseau Windows.</span><span class="sxs-lookup"><span data-stu-id="25c78-229">The provider for NFS allows you to create tools and scripts for configuring and monitoring the Windows Network File System.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-231">Le fournisseur ping fournit l’accès aux informations d’État fournies par la commande ping standard.</span><span class="sxs-lookup"><span data-stu-id="25c78-231">The Ping provider supplies access to the status information provided by the standard ping command.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Renvoi](/previous-versions/windows/desktop/policmanprov/policy-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Policy](/previous-versions/windows/desktop/policmanprov/policy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-233">Fournit des extensions à la stratégie de groupe et permet d’affiner l’application de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="25c78-233">Provides extensions to group policy, and permits refinements in the application of policy.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Compteur d’alimentation](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span><span class="sxs-lookup"><span data-stu-id="25c78-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Power Meter](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-235">Le fournisseur de contrôle d’alimentation prend en charge l’interface de contrôle d’alimentation et de budgétisation (PMB).</span><span class="sxs-lookup"><span data-stu-id="25c78-235">The Power Meter provider supports the Power Metering and Budgeting (PMB) interface.</span></span> <span data-ttu-id="25c78-236">Ces classes sont l’interface principale pour la requête d’informations de l’interface de contrôle d’alimentation (PMI) à partir des compteurs d’alimentation sous-jacents sur le système.</span><span class="sxs-lookup"><span data-stu-id="25c78-236">These classes are the primary interface for the query of Power Meter Interface (PMI) information from underlying power meters on the system.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Stratégie d’alimentation](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span><span class="sxs-lookup"><span data-stu-id="25c78-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Power Policy](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-238">Le fournisseur de stratégie d’alimentation fournit des classes qui permettent de gérer à distance toute l’infrastructure de la stratégie d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="25c78-238">The Power Policy provider provides classes the ability to remotely manage all the power policy infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span><span class="sxs-lookup"><span data-stu-id="25c78-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-240">Le fournisseur [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) fournit des classes pour gérer l’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="25c78-240">The [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) provider provides classes to manage Remote Access.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span><span class="sxs-lookup"><span data-stu-id="25c78-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-242">Le fournisseur [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) fournit des classes pour gérer le serveur d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="25c78-242">The [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) provider provides classes to manage the Remote Access Server.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-244">Le fournisseur [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) expose les mesures de fiabilité du journal des événements système et Windows.</span><span class="sxs-lookup"><span data-stu-id="25c78-244">The [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) provider exposes system and Windows Event Log reliability metrics.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Services Bureau à distance](/windows/desktop/TermServ/terminal-services-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remote Desktop Services](/windows/desktop/TermServ/terminal-services-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-246">Permet une administration de serveur cohérente dans un environnement Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="25c78-246">Enables consistent server administration in a Remote Desktop Services environment.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span><span class="sxs-lookup"><span data-stu-id="25c78-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-248">Définit des classes qui vous permettent d’écrire des scripts et du code pour modifier les paramètres du serveur de rapports et du Gestionnaire de rapports.</span><span class="sxs-lookup"><span data-stu-id="25c78-248">Defines classes that allow you to write scripts and code to modify the settings of the report server and the Report Manager.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Jeu de stratégie résultant (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span><span class="sxs-lookup"><span data-stu-id="25c78-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Resultant Set of Policy (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-250">Fournit des méthodes pour planifier et déboguer des paramètres de stratégie dans une situation de simulation.</span><span class="sxs-lookup"><span data-stu-id="25c78-250">Supplies methods to plan and debug policy settings in a what-if situation.</span></span> <span data-ttu-id="25c78-251">Ces méthodes permettent aux administrateurs de déterminer facilement la combinaison des paramètres de stratégie qui s’appliquent à un utilisateur ou à un ordinateur, ou s’appliquent à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="25c78-251">These methods allow administrators to determine easily the combination of policy settings that apply to, or will apply to, a user or computer.</span></span> <span data-ttu-id="25c78-252">C’est ce que l’on appelle le jeu de stratégie résultant (RSoP).</span><span class="sxs-lookup"><span data-stu-id="25c78-252">This is known as the Resultant Set of Policy (RSoP).</span></span> <span data-ttu-id="25c78-253">Pour plus d’informations, consultez [à propos du fournisseur de méthodes WMI RSoP](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) et des [classes WMI RSoP](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="25c78-253">For more information, see [About the RSoP WMI Method Provider](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) and [RSoP WMI Classes](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Caution](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Security](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-255">Récupère ou modifie les paramètres de sécurité qui contrôlent la propriété, l’audit et les droits d’accès aux fichiers, répertoires et partages.</span><span class="sxs-lookup"><span data-stu-id="25c78-255">Retrieves or changes security settings that control ownership, auditing, and access rights to files, directories, and shares.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span><span class="sxs-lookup"><span data-stu-id="25c78-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-257">[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) expose les fonctionnalités de déploiement.</span><span class="sxs-lookup"><span data-stu-id="25c78-257">The [ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) exposes deployment functionality.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Session](/previous-versions/windows/desktop/wmipsess/session-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Session](/previous-versions/windows/desktop/wmipsess/session-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-259">Gère les sessions et les connexions réseau.</span><span class="sxs-lookup"><span data-stu-id="25c78-259">Manages network sessions and connections.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Cliché instantané](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Shadow Copy](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-261">Fournit des fonctions de gestion pour les clichés instantanés de la fonctionnalité dossiers partagés.</span><span class="sxs-lookup"><span data-stu-id="25c78-261">Supplies management functions for the Shadow Copies of the Shared Folders feature.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Approvisionnement de machines virtuelles protégées](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Shielded VM Provisioning](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-263">Le fournisseur d’approvisionnement de machine virtuelle protégé permet à un contrôleur de structure de démarrer l’approvisionnement sécurisé d’une machine virtuelle protégée sur un ordinateur hôte Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="25c78-263">The Shielded VM Provisioning provider enables a fabric controller to start the secure provisioning of a shielded VM on a Hyper-V host.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Service de provisionnement de machines virtuelles protégées](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Shielded VM Provisioning Service](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-265">Le fournisseur permet la configuration d’un ordinateur virtuel protégé.</span><span class="sxs-lookup"><span data-stu-id="25c78-265">The provider enables provisioning of a shielded virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Gestion SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB Management](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-267">L’API de gestion SMB fournit des classes et des méthodes pour gérer les partages et l’accès au partage.</span><span class="sxs-lookup"><span data-stu-id="25c78-267">The SMB Management API provides classes and methods to manage shares and share access.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-268"><span id="SNMP"></span><span id="snmp"></span>[SMTP](/windows/desktop/WmiSdk/snmp-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-268"><span id="SNMP"></span><span id="snmp"></span>[SNMP](/windows/desktop/WmiSdk/snmp-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-269">Mappe les objets SNMP (simple Network Management Protocol) définis dans les objets de schéma MIB (Management Information base) aux classes.</span><span class="sxs-lookup"><span data-stu-id="25c78-269">Maps Simple Network Management Protocol (SNMP) objects that are defined in Management Information Base (MIB) schema objects to classes.</span></span> <span data-ttu-id="25c78-270">Pour plus d’informations, consultez [configuration de l’environnement SNMP WMI](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span><span class="sxs-lookup"><span data-stu-id="25c78-270">For more information, see [Setting up the WMI SNMP Environment](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Journalisation de l’inventaire logiciel](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Software Inventory Logging](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-272">Le fournisseur de journalisation de l’inventaire logiciel recueille les données de licence relatives aux logiciels installés sur un serveur Windows et fournit un accès à distance aux données afin qu’elles puissent être agrégées facilement par un centre de données.</span><span class="sxs-lookup"><span data-stu-id="25c78-272">The Software Inventory Logging provider collects licensing data about software installed on a Windows Server, and provides remote access to the data so it can be aggregated easily by a datacenter.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Licences logicielles pour Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span><span class="sxs-lookup"><span data-stu-id="25c78-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Software Licensing for Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-274">[Classes de licences logicielles](/previous-versions/windows/desktop/sppwmi/software-license-provider-) utilisées pour Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25c78-274">[Software Licensing Classes](/previous-versions/windows/desktop/sppwmi/software-license-provider-) used for Windows Vista.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Licence logicielle](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span><span class="sxs-lookup"><span data-stu-id="25c78-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Software License](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-276">Le fournisseur de licences logicielles récupère les données de licence logicielle.</span><span class="sxs-lookup"><span data-stu-id="25c78-276">The Software Licensing provider retrieves software licensing data.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Volume de stockage](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Storage Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-278">Le fournisseur de volume de stockage fournit des fonctions de gestion de volume.</span><span class="sxs-lookup"><span data-stu-id="25c78-278">The Storage Volume provider supplies volume management functions.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Réplica de stockage](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Storage Replica](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-280">Le fournisseur permet la gestion d’un réplica de stockage.</span><span class="sxs-lookup"><span data-stu-id="25c78-280">The provider enables management of a storage replica.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-282">Le fournisseur de Registre système permet aux applications de gestion de récupérer et de modifier des données dans le registre système, et de recevoir des notifications lorsque des modifications se produisent.</span><span class="sxs-lookup"><span data-stu-id="25c78-282">The System Registry provider enables management applications to retrieve and modify data in the system registry, and receive notifications when changes occur.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Restauration du système](/windows/desktop/sr/system-restore-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[System Restore](/windows/desktop/sr/system-restore-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-284">Fournit des classes qui configurent et utilisent la fonctionnalité de restauration du système.</span><span class="sxs-lookup"><span data-stu-id="25c78-284">Supplies classes that configure and use System Restore functionality.</span></span> <span data-ttu-id="25c78-285">Pour plus d’informations, consultez Configuration de la [restauration du système](/windows/desktop/sr/configuring-system-restore) et des [classes WMI de restauration du système](/windows/desktop/sr/system-restore-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="25c78-285">For more information, see [Configuring System Restore](/windows/desktop/sr/configuring-system-restore) and the [System Restore WMI Classes](/windows/desktop/sr/system-restore-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Module de plateforme sécurisée (TPM)](/windows/desktop/SecProv/trusted-platform-module-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-287">Fournit l’accès aux données relatives à un appareil de sécurité, représenté par une instance de [**\_ TPM Win32**](/windows/desktop/SecProv/win32-tpm), qui est la racine de l’approbation pour un système informatique de plateforme sécurisée Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="25c78-287">Provides access to data about a security device, represented by an instance of [**Win32\_TPM**](/windows/desktop/SecProv/win32-tpm), that is the root of trust for a Microsoft Windows trusted platform computer system.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-289">Le fournisseur [TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) est un fournisseur d’instances qui crée des classes avec des informations sur les relations d’approbation entre les domaines.</span><span class="sxs-lookup"><span data-stu-id="25c78-289">The [Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) provider is an instance provider that creates classes with information about the trust relationships between domains.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Journalisation des accès utilisateur](/previous-versions/windows/desktop/ual/user-access-logging)</span><span class="sxs-lookup"><span data-stu-id="25c78-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[User Access Logging](/previous-versions/windows/desktop/ual/user-access-logging)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-291">La journalisation des accès utilisateur est un Framework commun pour les rôles Windows Server afin de signaler leurs mesures de consommation respectives.</span><span class="sxs-lookup"><span data-stu-id="25c78-291">User Access Logging (UAL) is a common framework for Windows Server roles to report their respective consumption metrics.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-293">Le fournisseur [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) expose des classes qui fournissent des informations sur un profil utilisateur sur un système Windows, ainsi que l’état d’intégrité d’un dossier utilisateur Redirigé.</span><span class="sxs-lookup"><span data-stu-id="25c78-293">The [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) provider exposes classes that provide information about a user profile on a Windows system, as well as the health status of a redirected user folder.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Gestion de l’état utilisateur](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[User State Management](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-295">Le fournisseur de gestion de l’état utilisateur expose une API de gestion et de création de rapports pour les scénarios d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="25c78-295">The User State Management provider exposes a management and reporting API for enterprise scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[Affichage](/windows/desktop/WmiSdk/view-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[View](/windows/desktop/WmiSdk/view-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-297">Crée des instances et des méthodes basées sur des instances d’autres classes.</span><span class="sxs-lookup"><span data-stu-id="25c78-297">Creates new instances and methods based on instances of other classes.</span></span> <span data-ttu-id="25c78-298">Deux versions du fournisseur d’affichages sont disponibles sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="25c78-298">Two versions of the View provider are available on 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span><span class="sxs-lookup"><span data-stu-id="25c78-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-300">Le fournisseur [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) expose une plateforme pour l’automatisation de la connectivité à un client de réseau privé virtuel.</span><span class="sxs-lookup"><span data-stu-id="25c78-300">The [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) provider exposes a platform for automating connectivity to a virtual private network client.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-302">Permet d’accéder aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="25c78-302">Provides access to the classes, instances, methods, and events of hardware drivers that conform to the Windows Driver Model (WDM).</span></span>

</dd> <dt>

<span data-ttu-id="25c78-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-304">Le fournisseur [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) expose les fonctionnalités de sécurité et de filtrage du réseau.</span><span class="sxs-lookup"><span data-stu-id="25c78-304">The [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) provider exposes network security and filtering features.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-306">Le fournisseur [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) expose des informations de signature numérique sur les pilotes.</span><span class="sxs-lookup"><span data-stu-id="25c78-306">The [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) provider exposes digital signature information about drivers.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-308">Le fournisseur [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) expose les horodateurs actuels, locaux et UTC sur un système informatique.</span><span class="sxs-lookup"><span data-stu-id="25c78-308">The [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) provider exposes the current, local, and UTC-based timestamps on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Composants WDAC (Windows Data Access Components)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-310">Fournit la gestion de WDAC.</span><span class="sxs-lookup"><span data-stu-id="25c78-310">Provides management of WDAC.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-312">Le fournisseur Windows Defender expose les fonctionnalités de sécurité de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="25c78-312">The Windows Defender provider exposes Windows Defender security features.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-314">Le fournisseur Windows Installer, également connu sous le nom de fournisseur MSI, permet aux applications d’accéder aux informations collectées à partir d’applications conformes Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="25c78-314">The Windows Installer provider, also known as the MSI provider allows applications to access information collected from Windows Installer compliant applications.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Activation de produit Windows](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Product Activation](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-316">Le fournisseur d’activation de produit Windows (WPA) est une technologie anti-piratage visant à réduire la copie occasionnelle des logiciels.</span><span class="sxs-lookup"><span data-stu-id="25c78-316">The Windows Product Activation (WPA) provider is an anti-piracy technology aimed at reducing the casual copying of software.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Gestionnaire de serveur Windows](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Server Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-318">Le fournisseur permet l’accès et la gestion de la configuration contrôlée par l’application Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="25c78-318">The provider enables access to and management of the configuration controlled by the Server Manager application.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Gestion du stockage Windows Server (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server Storage Management (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-320">Le fournisseur MsftStrgMan fournit la gestion des systèmes de stockage sur les produits Windows Server.</span><span class="sxs-lookup"><span data-stu-id="25c78-320">The MsftStrgMan provider provides management for storage systems on Windows Server products.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Gestion du stockage Windows (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows Storage Management (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-322">Le fournisseur StrgMgmt peut être utilisé pour gérer un large éventail de configurations de stockage, de tablettes à des groupes de stockage externes sur les serveurs.</span><span class="sxs-lookup"><span data-stu-id="25c78-322">The StrgMgmt provider can be used to manage a wide range of storage configurations, from tablets to external storage arrays on servers.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Outil d’évaluation système Windows](/windows/desktop/WinSAT/winsat-mof-classes)</span><span class="sxs-lookup"><span data-stu-id="25c78-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows System Assessment Tool](/windows/desktop/WinSAT/winsat-mof-classes)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-324">L’outil d’évaluation système Windows (WinSAT) expose un certain nombre de classes qui évaluent les caractéristiques de performances et les fonctionnalités d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="25c78-324">The Windows System Assessment Tool (WinSAT) exposes a number of classes that assesses the performance characteristics and capabilities of a computer.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[Noyau WMI](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span><span class="sxs-lookup"><span data-stu-id="25c78-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-326">Le fournisseur principal WMI définit des classes qui composent les fonctionnalités de base de WMI.</span><span class="sxs-lookup"><span data-stu-id="25c78-326">The WMI Core provider defines classes that compose the core functionality of WMI.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[\_ProviderSubSystem msft](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span><span class="sxs-lookup"><span data-stu-id="25c78-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-328">Le [fournisseur \_ ProviderSubSystem msft](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) prend en charge les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="25c78-328">The [Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) provider supports providers.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[\_Performances Win32](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="25c78-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32\_Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-330">La classe abstraite de performances [**\_ Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) est la classe de base pour les classes de compteur de performance [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) et [**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span><span class="sxs-lookup"><span data-stu-id="25c78-330">The [**Win32\_Perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) abstract class is the base class for the performance counter classes [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) and [**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span></span> <span data-ttu-id="25c78-331">Il définit les propriétés timestamp et Frequency nécessaires utilisées dans les algorithmes de la classe de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="25c78-331">It defines the required timestamp and frequency properties used in the CounterType algorithms for the performance counter classes.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**\_PerfFormattedData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="25c78-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-333">Classe de base abstraite pour les classes de données calculées préinstallées.</span><span class="sxs-lookup"><span data-stu-id="25c78-333">An abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**\_PerfRawData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="25c78-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-335">La classe de compteur de performance [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) est la classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes.</span><span class="sxs-lookup"><span data-stu-id="25c78-335">The performance counter class [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) is the abstract base class for all concrete raw performance counter classes.</span></span> <span data-ttu-id="25c78-336">Pour apparaître dans le moniteur système, les classes de compteur de performance doivent être ajoutées à l' \\ espace de noms root cimv2 et dérivées de **Win32 \_ PerfRawData**.</span><span class="sxs-lookup"><span data-stu-id="25c78-336">To appear in System Monitor, performance counter classes must be added to the "Root\\CIMv2" namespace and derived from **Win32\_PerfRawData**.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-338">Crée les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="25c78-338">Creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="25c78-339">Les données sont fournies dynamiquement à ces classes de performance par le fournisseur WMIPerfInst.</span><span class="sxs-lookup"><span data-stu-id="25c78-339">Data is dynamically supplied to these performance classes by the WMIPerfInst provider.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span><span class="sxs-lookup"><span data-stu-id="25c78-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-341">Fournit des données de compteur de performances brutes et mises en forme de manière dynamique à partir des définitions de [classe de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) .</span><span class="sxs-lookup"><span data-stu-id="25c78-341">Supplies raw and formatted performance counter data dynamically from [Performance Counter Class](/windows/desktop/CIMWin32Prov/performance-counter-classes) definitions.</span></span>

</dd> <dt>

<span data-ttu-id="25c78-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Dossiers de travail](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span><span class="sxs-lookup"><span data-stu-id="25c78-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Work Folders](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span></span>
</dt> <dd>

<span data-ttu-id="25c78-343">Dossiers de travail permet de synchroniser des fichiers avec plusieurs ordinateurs et appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="25c78-343">Work Folders is used to synchronize files with multiple PCs and mobile devices.</span></span>

</dd> </dl>

 

 
