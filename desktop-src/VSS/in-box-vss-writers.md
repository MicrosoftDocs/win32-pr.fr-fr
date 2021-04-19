---
description: Le système d’exploitation Windows comprend un ensemble d’enregistreurs VSS chargés d’énumérer les données nécessaires aux différentes fonctionnalités Windows. Celles-ci sont appelées &\# 0034 ; in-box&\# 0034 ; Writers.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: Enregistreurs VSS intégrés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533629"
---
# <a name="in-box-vss-writers"></a><span data-ttu-id="e64ea-104">Enregistreurs VSS intégrés</span><span class="sxs-lookup"><span data-stu-id="e64ea-104">In-Box VSS Writers</span></span>

<span data-ttu-id="e64ea-105">Le système d’exploitation Windows comprend un ensemble d’enregistreurs VSS chargés d’énumérer les données nécessaires aux différentes fonctionnalités Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-105">The Windows operating system includes a set of VSS writers that are responsible for enumerating the data that is required by various Windows features.</span></span> <span data-ttu-id="e64ea-106">On parle alors d’enregistreurs « intégrés ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-106">These are referred to as "in-box" writers.</span></span>

> [!Note]  
> <span data-ttu-id="e64ea-107">Le writer intégré MSDE n’est pas disponible dans Windows Vista, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e64ea-107">The MSDE in-box writer is not available in Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="e64ea-108">Au lieu de cela, le writer SQL doit être utilisé pour sauvegarder les bases de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e64ea-108">Instead, the SQL Writer should be used to back up SQL Server databases.</span></span> <span data-ttu-id="e64ea-109">Seuls les SQL Server 2005 SP2 et versions ultérieures sont pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e64ea-109">Only SQL Server 2005 SP2 and later are supported on Windows Vista, Windows Server 2008, and later.</span></span>

 

-   [<span data-ttu-id="e64ea-110">Enregistreur VSS Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-110">Active Directory Domain Services (NTDS) VSS Writer</span></span>](#active-directory-domain-services-ntds-vss-writer)
-   [<span data-ttu-id="e64ea-111">Rédacteur de services de fédération Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-111">Active Directory Federation Services Writer</span></span>](#active-directory-federation-services-writer)
-   [<span data-ttu-id="e64ea-112">Enregistreur VSS services AD LDS (Active Directory Lightweight Directory Services) (LDS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [<span data-ttu-id="e64ea-113">Enregistreur services AD RMS (Active Directory Rights Management Services) (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-113">Active Directory Rights Management Services (AD RMS) Writer</span></span>](#active-directory-rights-management-services-ad-rms-writer)
-   [<span data-ttu-id="e64ea-114">Rédacteur de récupération automatique du système (ASR)</span><span class="sxs-lookup"><span data-stu-id="e64ea-114">Automated System Recovery (ASR) Writer</span></span>](#automated-system-recovery-asr-writer)
-   [<span data-ttu-id="e64ea-115">Enregistreur Service de transfert intelligent en arrière-plan (BITS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-115">Background Intelligent Transfer Service (BITS) Writer</span></span>](#background-intelligent-transfer-service-bits-writer)
-   [<span data-ttu-id="e64ea-116">Auteur de l’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="e64ea-116">Certificate Authority Writer</span></span>](#certificate-authority-writer)
-   [<span data-ttu-id="e64ea-117">Rédacteur de service de cluster</span><span class="sxs-lookup"><span data-stu-id="e64ea-117">Cluster Service Writer</span></span>](#cluster-service-writer)
-   [<span data-ttu-id="e64ea-118">Enregistreur VSS Volume partagé de cluster (CSV)</span><span class="sxs-lookup"><span data-stu-id="e64ea-118">Cluster Shared Volume (CSV) VSS Writer</span></span>](#cluster-shared-volume-csv-vss-writer)
-   [<span data-ttu-id="e64ea-119">Enregistreur de base de données d’inscription de classe COM+</span><span class="sxs-lookup"><span data-stu-id="e64ea-119">COM+ Class Registration Database Writer</span></span>](#com-class-registration-database-writer)
-   [<span data-ttu-id="e64ea-120">Enregistreur de déduplication des données</span><span class="sxs-lookup"><span data-stu-id="e64ea-120">Data Deduplication Writer</span></span>](#data-deduplication-writer)
-   [<span data-ttu-id="e64ea-121">Réplication du système de fichiers distribués (DFSR)</span><span class="sxs-lookup"><span data-stu-id="e64ea-121">Distributed File System Replication (DFSR)</span></span>](#distributed-file-system-replication-dfsr)
-   [<span data-ttu-id="e64ea-122">Enregistreur DHCP (Dynamic Host Configuration Protocol)</span><span class="sxs-lookup"><span data-stu-id="e64ea-122">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>](#dynamic-host-configuration-protocol-dhcp-writer)
-   [<span data-ttu-id="e64ea-123">Service de réplication de fichiers (FRS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-123">File Replication Service (FRS)</span></span>](#file-replication-service-frs)
-   [<span data-ttu-id="e64ea-124">Enregistreur de Gestionnaire des ressources du serveur de fichiers (FSRM)</span><span class="sxs-lookup"><span data-stu-id="e64ea-124">File Server Resource Manager (FSRM) Writer</span></span>](#file-server-resource-manager-fsrm-writer)
-   [<span data-ttu-id="e64ea-125">Enregistreur Hyper-V</span><span class="sxs-lookup"><span data-stu-id="e64ea-125">Hyper-V Writer</span></span>](#hyper-v-writer)
-   [<span data-ttu-id="e64ea-126">Rédacteur de configuration IIS</span><span class="sxs-lookup"><span data-stu-id="e64ea-126">IIS Configuration Writer</span></span>](#iis-configuration-writer)
-   [<span data-ttu-id="e64ea-127">Enregistreur de la métabase IIS</span><span class="sxs-lookup"><span data-stu-id="e64ea-127">IIS Metabase Writer</span></span>](#iis-metabase-writer)
-   [<span data-ttu-id="e64ea-128">Enregistreur Microsoft Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="e64ea-128">Microsoft Message Queuing (MSMQ) Writer</span></span>](#microsoft-message-queuing-msmq-writer)
-   [<span data-ttu-id="e64ea-129">Rédacteur MSSearch service</span><span class="sxs-lookup"><span data-stu-id="e64ea-129">MSSearch Service Writer</span></span>](#mssearch-service-writer)
-   [<span data-ttu-id="e64ea-130">Enregistreur VSS NPS</span><span class="sxs-lookup"><span data-stu-id="e64ea-130">NPS VSS Writer</span></span>](#nps-vss-writer)
-   [<span data-ttu-id="e64ea-131">Enregistreur des compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="e64ea-131">Performance Counters Writer</span></span>](#performance-counters-writer)
-   [<span data-ttu-id="e64ea-132">Enregistreur du Registre</span><span class="sxs-lookup"><span data-stu-id="e64ea-132">Registry Writer</span></span>](#registry-writer)
-   [<span data-ttu-id="e64ea-133">Enregistreur VSS de la passerelle Services Bureau à distance (services Terminal Server)</span><span class="sxs-lookup"><span data-stu-id="e64ea-133">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [<span data-ttu-id="e64ea-134">Enregistreur VSS du gestionnaire de licences des Services Bureau à distance (services Terminal Server)</span><span class="sxs-lookup"><span data-stu-id="e64ea-134">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [<span data-ttu-id="e64ea-135">Enregistreur d’optimisation des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="e64ea-135">Shadow Copy Optimization Writer</span></span>](#shadow-copy-optimization-writer)
-   [<span data-ttu-id="e64ea-136">Rédacteur de service de partage de synchronisation</span><span class="sxs-lookup"><span data-stu-id="e64ea-136">Sync Share Service Writer</span></span>](#sync-share-service-writer)
-   [<span data-ttu-id="e64ea-137">Enregistreur du système</span><span class="sxs-lookup"><span data-stu-id="e64ea-137">System Writer</span></span>](#system-writer)
-   [<span data-ttu-id="e64ea-138">Rédacteur de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e64ea-138">Task Scheduler Writer</span></span>](#task-scheduler-writer)
-   [<span data-ttu-id="e64ea-139">Enregistreur du magasin de métadonnées VSS</span><span class="sxs-lookup"><span data-stu-id="e64ea-139">VSS Metadata Store Writer</span></span>](#vss-metadata-store-writer)
-   [<span data-ttu-id="e64ea-140">Enregistreur des services de déploiement Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-140">Windows Deployment Services (WDS) Writer</span></span>](#windows-deployment-services-wds-writer)
-   [<span data-ttu-id="e64ea-141">Enregistreur de base de données interne Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="e64ea-141">Windows Internal Database (WID) Writer</span></span>](#windows-internal-database-wid-writer)
-   [<span data-ttu-id="e64ea-142">Enregistreur WINS (Windows Internet Name Service)</span><span class="sxs-lookup"><span data-stu-id="e64ea-142">Windows Internet Name Service (WINS) Writer</span></span>](#windows-internet-name-service-wins-writer)
-   [<span data-ttu-id="e64ea-143">Rédacteur WMI</span><span class="sxs-lookup"><span data-stu-id="e64ea-143">WMI Writer</span></span>](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a><span data-ttu-id="e64ea-144">Enregistreur VSS Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-144">Active Directory Domain Services (NTDS) VSS Writer</span></span>

<span data-ttu-id="e64ea-145">Ce writer signale le fichier de base de données NTDS (NTDS. dit) et les fichiers journaux associés.</span><span class="sxs-lookup"><span data-stu-id="e64ea-145">This writer reports the NTDS database file (ntds.dit) and the associated log files.</span></span> <span data-ttu-id="e64ea-146">Ces fichiers sont nécessaires pour restaurer correctement l’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e64ea-146">These files are required to restore the Active Directory correctly.</span></span>

<span data-ttu-id="e64ea-147">Il n’existe qu’un seul fichier Ntds. dit par contrôleur de domaine et il est signalé dans les métadonnées de l’enregistreur comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="e64ea-147">There is only one ntds.dit file per domain controller, and it is reported in the writer metadata as in the following example:</span></span>

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

<span data-ttu-id="e64ea-148">Voici un exemple qui montre comment répertorier les composants dans les métadonnées du writer :</span><span class="sxs-lookup"><span data-stu-id="e64ea-148">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="e64ea-149">Au moment de la sauvegarde, l’enregistreur définit l’heure d’expiration de la sauvegarde dans les métadonnées de sauvegarde du writer.</span><span class="sxs-lookup"><span data-stu-id="e64ea-149">At backup time, the writer sets the backup expiration time in the writer's backup metadata.</span></span> <span data-ttu-id="e64ea-150">Les demandeurs doivent récupérer ces métadonnées à l’aide de [**IVssComponent :: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) pour déterminer si la base de données a expiré.</span><span class="sxs-lookup"><span data-stu-id="e64ea-150">Requesters should retrieve this metadata by using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) to determine whether the database has expired.</span></span> <span data-ttu-id="e64ea-151">Les bases de données expirées ne peuvent pas être restaurées.</span><span class="sxs-lookup"><span data-stu-id="e64ea-151">Expired databases cannot be restored.</span></span>

<span data-ttu-id="e64ea-152">Si l’ordinateur qui contient la base de données NTDS est un contrôleur de domaine, l’application de sauvegarde doit toujours effectuer une sauvegarde de l’état du système sur tous les volumes contenant des informations d’État du système critiques.</span><span class="sxs-lookup"><span data-stu-id="e64ea-152">If the computer that contains the NTDS database is a domain controller, the backup application should always perform a system state backup across all volumes containing critical system state information.</span></span> <span data-ttu-id="e64ea-153">Au moment de la restauration, l’application doit d’abord redémarrer l’ordinateur en mode de restauration des services d’annuaire, puis effectuer une restauration de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-153">At restore time, the application should first restart the computer in Directory Services Restore Mode and then perform a system state restore.</span></span>

<span data-ttu-id="e64ea-154">La chaîne du nom de l’enregistreur pour ce writer est « NTDS ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-154">The writer name string for this writer is "NTDS".</span></span>

<span data-ttu-id="e64ea-155">L’ID d’enregistreur pour ce writer est B2014C9E-8711-4C5C-A5A9-3CF384484757.</span><span class="sxs-lookup"><span data-stu-id="e64ea-155">The writer ID for this writer is B2014C9E-8711-4C5C-A5A9-3CF384484757.</span></span>

## <a name="active-directory-federation-services-writer"></a><span data-ttu-id="e64ea-156">Rédacteur de services de fédération Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-156">Active Directory Federation Services Writer</span></span>

<span data-ttu-id="e64ea-157">Ce writer signale les fichiers de données services de fédération Active Directory (AD FS) (ADFS).</span><span class="sxs-lookup"><span data-stu-id="e64ea-157">This writer reports the Active Directory Federation Services (ADFS) data files.</span></span>

<span data-ttu-id="e64ea-158">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-159">La chaîne du nom de l’enregistreur pour ce writer est « l’enregistreur VSS ADFS ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-159">The writer name string for this writer is "ADFS VSS Writer".</span></span>

<span data-ttu-id="e64ea-160">L’ID d’enregistreur pour ce writer est 772C45F8-AE01-4F94-940C-94961864ACAD.</span><span class="sxs-lookup"><span data-stu-id="e64ea-160">The writer ID for this writer is 772C45F8-AE01-4F94-940C-94961864ACAD.</span></span>

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a><span data-ttu-id="e64ea-161">Enregistreur VSS services AD LDS (Active Directory Lightweight Directory Services) (LDS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>

<span data-ttu-id="e64ea-162">Ce writer signale le fichier de base de données ADAM (fichier Adamntds. dit) et les fichiers journaux associés pour chaque instance dans% Program Files% \\ Microsoft Adam \\ instance *n* \\ Data, où *N* est le numéro d’instance ADAM.</span><span class="sxs-lookup"><span data-stu-id="e64ea-162">This writer reports the ADAM database file (adamntds.dit) and the associated log files for each instance in %program files%\\Microsoft ADAM\\instance *N*\\data, where *N* is the ADAM instance number.</span></span> <span data-ttu-id="e64ea-163">Ces fichiers journaux de base de données sont requis pour restaurer les instances ADAM.</span><span class="sxs-lookup"><span data-stu-id="e64ea-163">These database log files are required to restore ADAM instances.</span></span>

<span data-ttu-id="e64ea-164">**Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-164">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-165">Voici un exemple qui montre comment répertorier les composants dans les métadonnées du writer :</span><span class="sxs-lookup"><span data-stu-id="e64ea-165">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="e64ea-166">Au moment de la sauvegarde, l’enregistreur définit l’heure d’expiration de la sauvegarde dans les métadonnées de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="e64ea-166">At backup time, the writer sets the backup expiration time in the backup metadata.</span></span> <span data-ttu-id="e64ea-167">Les applications de sauvegarde doivent récupérer ces métadonnées à l’aide de la méthode [**IVssComponent :: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) pour déterminer si la base de données a expiré.</span><span class="sxs-lookup"><span data-stu-id="e64ea-167">Backup applications should retrieve this metadata by using the [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) method to determine whether the database has expired.</span></span> <span data-ttu-id="e64ea-168">Les bases de données expirées ne peuvent pas être restaurées.</span><span class="sxs-lookup"><span data-stu-id="e64ea-168">Expired databases cannot be restored.</span></span>

<span data-ttu-id="e64ea-169">La chaîne du nom de l’enregistreur pour ce writer est « ADAM (instance *N*) writer », où *N* est le numéro de l’instance ADAM, par exemple « Adam (instance1) writer », « Adam (Instance2) writer », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e64ea-169">The writer name string for this writer is "ADAM (instance *N*) Writer", where *N* is the ADAM instance number, for example, "ADAM (instance1) Writer", "ADAM (instance2) Writer", and so on.</span></span>

<span data-ttu-id="e64ea-170">L’ID d’enregistreur pour ce writer est DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span><span class="sxs-lookup"><span data-stu-id="e64ea-170">The writer ID for this writer is DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span></span> <span data-ttu-id="e64ea-171">Cet ID d’enregistreur est le même pour toutes les instances.</span><span class="sxs-lookup"><span data-stu-id="e64ea-171">This writer ID is the same for all instances.</span></span>

## <a name="active-directory-rights-management-services-ad-rms-writer"></a><span data-ttu-id="e64ea-172">Enregistreur services AD RMS (Active Directory Rights Management Services) (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-172">Active Directory Rights Management Services (AD RMS) Writer</span></span>

<span data-ttu-id="e64ea-173">Ce writer signale les fichiers de données du service de Active Directory Rights Management (AD RMS).</span><span class="sxs-lookup"><span data-stu-id="e64ea-173">This writer reports the Active Directory Rights Management Service (AD RMS) data files.</span></span>

<span data-ttu-id="e64ea-174">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-175">La chaîne du nom de l’enregistreur pour ce writer est « AD RMS Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-175">The writer name string for this writer is "AD RMS Writer".</span></span>

<span data-ttu-id="e64ea-176">L’ID d’enregistreur pour ce writer est 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span><span class="sxs-lookup"><span data-stu-id="e64ea-176">The writer ID for this writer is 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span></span>

## <a name="automated-system-recovery-asr-writer"></a><span data-ttu-id="e64ea-177">Rédacteur de récupération automatique du système (ASR)</span><span class="sxs-lookup"><span data-stu-id="e64ea-177">Automated System Recovery (ASR) Writer</span></span>

<span data-ttu-id="e64ea-178">L’Enregistreur ASR stocke la configuration des disques sur le système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-178">The ASR writer stores the configuration of disks on the system.</span></span> <span data-ttu-id="e64ea-179">Ce writer signale la base de données de configuration de démarrage (BCD) et est également chargé de démonter la ruche de Registre qui représente le BCD lors de la création de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="e64ea-179">This writer reports the Boot Configuration Database (BCD) and is also responsible for dismounting the registry hive that represents the BCD during shadow copy creation.</span></span> <span data-ttu-id="e64ea-180">L’Enregistreur ASR doit être inclus dans toutes les sauvegardes requises pour la récupération complète.</span><span class="sxs-lookup"><span data-stu-id="e64ea-180">The ASR writer must be included in any backups required for bare-metal recovery.</span></span> <span data-ttu-id="e64ea-181">Pour plus d’informations sur ASR, consultez [utilisation de la récupération automatique du système VSS pour la récupération d’urgence](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="e64ea-181">For more information about ASR, see [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span>

<span data-ttu-id="e64ea-182">**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-182">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-183">La chaîne du nom de l’enregistreur pour ce writer est « Enregistreur ASR ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-183">The writer name string for this writer is "ASR Writer".</span></span>

<span data-ttu-id="e64ea-184">L’ID d’enregistreur pour l’Enregistreur ASR est BE000CBE-11FE-4426-9C58-531AA6355FC4.</span><span class="sxs-lookup"><span data-stu-id="e64ea-184">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4.</span></span>

## <a name="background-intelligent-transfer-service-bits-writer"></a><span data-ttu-id="e64ea-185">Enregistreur Service de transfert intelligent en arrière-plan (BITS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-185">Background Intelligent Transfer Service (BITS) Writer</span></span>

<span data-ttu-id="e64ea-186">Le writer BITS utilise la clé de Registre **FilesNotToBackup** pour exclure des fichiers du dossier de cache bits.</span><span class="sxs-lookup"><span data-stu-id="e64ea-186">The BITS writer uses the **FilesNotToBackup** registry key to exclude files from the BITS cache folder.</span></span> <span data-ttu-id="e64ea-187">L’emplacement du cache par défaut est% AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ cache.</span><span class="sxs-lookup"><span data-stu-id="e64ea-187">The default cache location is %AllUsersProfile%\\Microsoft\\Network\\Downloader\\Cache.</span></span>

<span data-ttu-id="e64ea-188">**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-188">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-189">En outre, l’enregistreur BITS exclut les fichiers suivants de la sauvegarde : les fichiers d’État du service BITS (Qmgr0. dat et Qmgr1. dat), le fichier journal de débogage BITS et les fichiers BITS partiellement téléchargés.</span><span class="sxs-lookup"><span data-stu-id="e64ea-189">In addition, the BITS writer excludes the following files from backup: the BITS state files (qmgr0.dat and qmgr1.dat), the BITS debug log file, and BITS partially downloaded files.</span></span>

<span data-ttu-id="e64ea-190">Si le fichier de destination de téléchargement BITS est un fichier SMB, le compte client doit avoir une relation d’approbation avec le serveur, sinon les sauvegardes peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="e64ea-190">If the BITS download destination file is an SMB file, the client account must have a trust relationship to the server, or else backups may fail.</span></span>

<span data-ttu-id="e64ea-191">La chaîne du nom de l’enregistreur pour ce writer est « Writer BITS ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-191">The writer name string for this writer is "BITS Writer".</span></span>

<span data-ttu-id="e64ea-192">L’ID d’enregistreur pour le writer BITS est 4969D978-BE47-48B0-B100-F328F07AC1E0.</span><span class="sxs-lookup"><span data-stu-id="e64ea-192">The writer ID for the BITS writer is 4969D978-BE47-48B0-B100-F328F07AC1E0.</span></span>

## <a name="certificate-authority-writer"></a><span data-ttu-id="e64ea-193">Auteur de l’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="e64ea-193">Certificate Authority Writer</span></span>

<span data-ttu-id="e64ea-194">Ce writer est responsable de l’énumération des fichiers de données pour le serveur de certificats.</span><span class="sxs-lookup"><span data-stu-id="e64ea-194">This writer is responsible for enumerating the data files for the Certificate Server.</span></span>

<span data-ttu-id="e64ea-195">La chaîne du nom de l’enregistreur pour ce writer est « Certificate Authority ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-195">The writer name string for this writer is "Certificate Authority".</span></span>

<span data-ttu-id="e64ea-196">**Windows XP :** La chaîne du nom de l’enregistreur pour ce writer est « Certificate Server Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-196">**Windows XP:** The writer name string for this writer is "Certificate Server Writer".</span></span>

<span data-ttu-id="e64ea-197">L’ID d’enregistreur du writer est 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span><span class="sxs-lookup"><span data-stu-id="e64ea-197">The writer ID for the writer is 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span></span>

## <a name="cluster-service-writer"></a><span data-ttu-id="e64ea-198">Rédacteur de service de cluster</span><span class="sxs-lookup"><span data-stu-id="e64ea-198">Cluster Service Writer</span></span>

<span data-ttu-id="e64ea-199">L’enregistreur VSS du service de cluster est documenté dans la documentation de l’API du [service de cluster](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .</span><span class="sxs-lookup"><span data-stu-id="e64ea-199">The Cluster Service VSS writer is documented in the [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API documentation.</span></span>

<span data-ttu-id="e64ea-200">**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge avant Windows Vista avec Service Pack 1 (SP1) et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e64ea-200">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="cluster-shared-volume-csv-vss-writer"></a><span data-ttu-id="e64ea-201">Enregistreur VSS Volume partagé de cluster (CSV)</span><span class="sxs-lookup"><span data-stu-id="e64ea-201">Cluster Shared Volume (CSV) VSS Writer</span></span>

<span data-ttu-id="e64ea-202">Ce writer signale les fichiers de données Volume partagé de cluster (CSV).</span><span class="sxs-lookup"><span data-stu-id="e64ea-202">This writer reports the Cluster Shared Volume (CSV) data files.</span></span> <span data-ttu-id="e64ea-203">Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-203">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="e64ea-204">**Windows server 2008 R2, Windows server 2008 et Windows server 2003 :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-204">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-205">La chaîne du nom de l’enregistreur pour ce writer est « Volume partagé de cluster VSS Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-205">The writer name string for this writer is "Cluster Shared Volume VSS Writer".</span></span>

<span data-ttu-id="e64ea-206">L’ID d’enregistreur du writer est 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span><span class="sxs-lookup"><span data-stu-id="e64ea-206">The writer ID for the writer is 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span></span>

## <a name="com-class-registration-database-writer"></a><span data-ttu-id="e64ea-207">Enregistreur de base de données d’inscription de classe COM+</span><span class="sxs-lookup"><span data-stu-id="e64ea-207">COM+ Class Registration Database Writer</span></span>

<span data-ttu-id="e64ea-208">Ce writer est responsable du contenu du \\ répertoire d’inscription% systemroot%.</span><span class="sxs-lookup"><span data-stu-id="e64ea-208">This writer is responsible for the contents of the %SystemRoot%\\Registration directory.</span></span> <span data-ttu-id="e64ea-209">Le catalogue COM+ est un fichier de l’inscription% SystemRoot% \\ avec un nom qui suit le modèle R *xxxxxxxxxxxx*. CLB, où *xxxxxxxxxxxx* est un nombre hexadécimal à 12 chiffres.</span><span class="sxs-lookup"><span data-stu-id="e64ea-209">The COM+ catalog is a file in %SystemRoot%\\Registration with a name that follows the pattern R *xxxxxxxxxxxx*.clb, where *xxxxxxxxxxxx* is a 12-digit hexadecimal number.</span></span> <span data-ttu-id="e64ea-210">Il peut y avoir plusieurs fichiers de ce type si des applications COM+ ont été configurées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e64ea-210">There can potentially be multiple such files if COM+ applications have been configured on the computer.</span></span> <span data-ttu-id="e64ea-211">Le fichier qui contient le catalogue COM+ actuel est le fichier ayant la plus grande valeur *xxxxxxxxxxxx*.</span><span class="sxs-lookup"><span data-stu-id="e64ea-211">The file that contains the current COM+ catalog is the file with the largest value of *xxxxxxxxxxxx*.</span></span>

<span data-ttu-id="e64ea-212">**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-212">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-213">La base de données d’inscription de classe COM+ dépend d’une clé de Registre sauvegardée et doit donc être sauvegardée et restaurée avec le registre.</span><span class="sxs-lookup"><span data-stu-id="e64ea-213">The COM+ class registration database depends on a registry key being backed up and hence needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="e64ea-214">Pour restaurer la base de données d’inscription COM+, une application de sauvegarde (demandeur) doit appeler la méthode [**ICOMAdminCatalog :: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="e64ea-214">To restore the COM+ Registration Database, a backup application (requester) must call the [**ICOMAdminCatalog::RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="e64ea-215">La chaîne du nom de l’enregistreur pour ce writer est « COM+ REGDB Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-215">The writer name string for this writer is "COM+ REGDB Writer".</span></span>

<span data-ttu-id="e64ea-216">L’ID d’enregistreur pour le writer de base de données d’inscription de classe COM+ est 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span><span class="sxs-lookup"><span data-stu-id="e64ea-216">The writer ID for the COM+ class registration database writer is 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span></span>

## <a name="data-deduplication-writer"></a><span data-ttu-id="e64ea-217">Enregistreur de déduplication des données</span><span class="sxs-lookup"><span data-stu-id="e64ea-217">Data Deduplication Writer</span></span>

<span data-ttu-id="e64ea-218">L’enregistreur VSS de la déduplication des données est documenté dans la documentation de l’API de [déduplication des données](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) .</span><span class="sxs-lookup"><span data-stu-id="e64ea-218">The Data Deduplication VSS writer is documented in the [Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API documentation.</span></span> <span data-ttu-id="e64ea-219">Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-219">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="e64ea-220">**Windows server 2008 R2, Windows server 2008 et Windows server 2003 :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-220">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

## <a name="distributed-file-system-replication-dfsr"></a><span data-ttu-id="e64ea-221">Réplication du système de fichiers distribués (DFSR)</span><span class="sxs-lookup"><span data-stu-id="e64ea-221">Distributed File System Replication (DFSR)</span></span>

<span data-ttu-id="e64ea-222">Le composant suivant comprend un enregistreur VSS : [réplication de système de fichiers DFS (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span><span class="sxs-lookup"><span data-stu-id="e64ea-222">The following component includes a VSS writer: [Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span></span>

<span data-ttu-id="e64ea-223">**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e64ea-223">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a><span data-ttu-id="e64ea-224">Enregistreur DHCP (Dynamic Host Configuration Protocol)</span><span class="sxs-lookup"><span data-stu-id="e64ea-224">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>

<span data-ttu-id="e64ea-225">Ce writer est responsable de l’énumération des fichiers requis pour le rôle serveur DHCP.</span><span class="sxs-lookup"><span data-stu-id="e64ea-225">This writer is responsible for enumerating files required for the DHCP server role.</span></span> <span data-ttu-id="e64ea-226">Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-226">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="e64ea-227">La chaîne du nom de l’enregistreur pour ce writer est « Writer jet DHCP ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-227">The writer name string for this writer is "Dhcp Jet Writer".</span></span>

<span data-ttu-id="e64ea-228">L’ID d’enregistreur pour ce writer est BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span><span class="sxs-lookup"><span data-stu-id="e64ea-228">The writer ID for this writer is BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span></span>

## <a name="file-replication-service-frs"></a><span data-ttu-id="e64ea-229">Service de réplication de fichiers (FRS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-229">File Replication Service (FRS)</span></span>

<span data-ttu-id="e64ea-230">Le rédacteur du service de réplication de fichiers est documenté dans [sauvegarde et restauration d’un dossier SYSVOL FRS-Replicated](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span><span class="sxs-lookup"><span data-stu-id="e64ea-230">The File Replication Service writer is documented in [Backing Up and Restoring an FRS-Replicated SYSVOL Folder](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span></span>

<span data-ttu-id="e64ea-231">**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e64ea-231">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="file-server-resource-manager-fsrm-writer"></a><span data-ttu-id="e64ea-232">Enregistreur de Gestionnaire des ressources du serveur de fichiers (FSRM)</span><span class="sxs-lookup"><span data-stu-id="e64ea-232">File Server Resource Manager (FSRM) Writer</span></span>

<span data-ttu-id="e64ea-233">Ce writer énumère les fichiers de configuration FSRM utilisés pour la sauvegarde de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-233">This writer enumerates the FSRM configuration files that are used for system state backup.</span></span> <span data-ttu-id="e64ea-234">Pendant les opérations de restauration, il empêche les modifications dans la configuration de FSRM et interrompt temporairement l’application des quotas et des filtres de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e64ea-234">During restore operations it prevents changes in FSRM configuration and temporarily halts enforcement of quotas and file screens.</span></span> <span data-ttu-id="e64ea-235">Une fois la restauration terminée, l’enregistreur actualise FSRM avec la configuration qui a été restaurée.</span><span class="sxs-lookup"><span data-stu-id="e64ea-235">After the restore is complete, the writer refreshes FSRM with the configuration that was restored.</span></span> <span data-ttu-id="e64ea-236">Ce writer est présent uniquement lorsque FSRM (partie du rôle Services de fichiers) est installé et en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e64ea-236">This writer is only present when FSRM (part of File Services role) is both installed and running.</span></span> <span data-ttu-id="e64ea-237">Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-237">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="e64ea-238">**Windows Server 2003 :** Ce Writer n’est pas pris en charge avant Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="e64ea-238">**Windows Server 2003:** This writer is not supported until Windows Server 2003 R2.</span></span>

<span data-ttu-id="e64ea-239">La chaîne du nom de l’enregistreur pour ce writer est « scripteur FSRM ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-239">The writer name string for this writer is "FSRM Writer".</span></span>

<span data-ttu-id="e64ea-240">L’ID d’enregistreur pour ce writer est 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span><span class="sxs-lookup"><span data-stu-id="e64ea-240">The writer ID for this writer is 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span></span>

## <a name="hyper-v-writer"></a><span data-ttu-id="e64ea-241">Enregistreur Hyper-V</span><span class="sxs-lookup"><span data-stu-id="e64ea-241">Hyper-V Writer</span></span>

<span data-ttu-id="e64ea-242">L’enregistreur VSS Hyper-V est documenté dans la documentation de l’API [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) .</span><span class="sxs-lookup"><span data-stu-id="e64ea-242">The Hyper-V VSS writer is documented in the [Hyper-V](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API documentation.</span></span> <span data-ttu-id="e64ea-243">Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-243">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="e64ea-244">**Windows Server 2003 :** Ce Writer n’est pas pris en charge avant Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e64ea-244">**Windows Server 2003:** This writer is not supported until Windows Server 2008.</span></span>

## <a name="iis-configuration-writer"></a><span data-ttu-id="e64ea-245">Rédacteur de configuration IIS</span><span class="sxs-lookup"><span data-stu-id="e64ea-245">IIS Configuration Writer</span></span>

<span data-ttu-id="e64ea-246">L’enregistreur de configuration IIS est chargé d’énumérer les fichiers de configuration IIS.</span><span class="sxs-lookup"><span data-stu-id="e64ea-246">The IIS configuration writer is responsible for enumerating the IIS configuration files.</span></span>

<span data-ttu-id="e64ea-247">**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e64ea-247">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="e64ea-248">Les demandeurs doivent sauvegarder les fichiers de configuration IIS, y compris le fichier de machine.config .NET FX ou le fichier de web.config racine ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="e64ea-248">Requesters are required to back up the IIS configuration files, including the .NET FX machine.config file or the ASP.NET root web.config file.</span></span>

<span data-ttu-id="e64ea-249">Ce writer ne sauvegarde pas le fichier de machine.config .NET FX ou le fichier de web.config racine ASP.NET, car ces fichiers sont énumérés par l’enregistreur de système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-249">This writer does not back up the .NET FX machine.config file or the ASP.NET root web.config file because these files are enumerated by the System Writer.</span></span>

<span data-ttu-id="e64ea-250">Ce writer sauvegarde tous les fichiers qui se trouvent dans les répertoires% windir% \\ system32 \\ inetsrv \\ config \\ et% windir% \\ system32 \\ inetsrv \\ config, à l’exception des fichiers qui sont énumérés par l’enregistreur de système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-250">This writer backs up all files that are in the %windir%\\system32\\inetsrv\\config\\schema and %windir%\\system32\\inetsrv\\config directories, except for files that are enumerated by the System Writer.</span></span>

<span data-ttu-id="e64ea-251">L’ID d’enregistreur pour l’enregistreur de configuration IIS est 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span><span class="sxs-lookup"><span data-stu-id="e64ea-251">The writer ID for the IIS configuration writer is 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span></span>

## <a name="iis-metabase-writer"></a><span data-ttu-id="e64ea-252">Enregistreur de la métabase IIS</span><span class="sxs-lookup"><span data-stu-id="e64ea-252">IIS Metabase Writer</span></span>

<span data-ttu-id="e64ea-253">L’enregistreur de métabase Internet Information Server (IIS) est chargé d’énumérer le fichier de la métabase IIS.</span><span class="sxs-lookup"><span data-stu-id="e64ea-253">The Internet Information Server (IIS) metabase writer is responsible for enumerating the IIS metabase file.</span></span>

<span data-ttu-id="e64ea-254">**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e64ea-254">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="e64ea-255">Les demandeurs doivent sauvegarder le fichier de la métabase IIS.</span><span class="sxs-lookup"><span data-stu-id="e64ea-255">Requesters are required to back up the IIS metabase file.</span></span>

<span data-ttu-id="e64ea-256">L’ID d’enregistreur pour l’enregistreur de métabase IIS est 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span><span class="sxs-lookup"><span data-stu-id="e64ea-256">The writer ID for the IIS metabase writer is 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span></span>

## <a name="microsoft-message-queuing-msmq-writer"></a><span data-ttu-id="e64ea-257">Enregistreur Microsoft Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="e64ea-257">Microsoft Message Queuing (MSMQ) Writer</span></span>

<span data-ttu-id="e64ea-258">Ce writer signale les fichiers de données Microsoft Message Queuing (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="e64ea-258">This writer reports the Microsoft Message Queuing (MSMQ) data files.</span></span>

<span data-ttu-id="e64ea-259">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-260">La chaîne de nom de l’enregistreur pour ce writer est « MSMQ Writer (*SvcName*) », où *SvcName* est le nom du service MSMQ auquel le writer est associé.</span><span class="sxs-lookup"><span data-stu-id="e64ea-260">The writer name string for this writer is "MSMQ Writer (*SvcName*)", where *SvcName* is the name of the MSMQ service the writer is associated with.</span></span> <span data-ttu-id="e64ea-261">Pour l’installation par défaut, le nom du service est « MSMQ ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-261">For default installation, the service name is "MSMQ".</span></span> <span data-ttu-id="e64ea-262">Pour les instances en cluster, le nom du service est MSMQ $*resourceName*, où *resourceName* est le nom de la ressource MSMQ en cluster.</span><span class="sxs-lookup"><span data-stu-id="e64ea-262">For clustered instances, the service name is MSMQ$*ResourceName*, where *ResourceName* is the clustered MSMQ resource name.</span></span>

<span data-ttu-id="e64ea-263">L’ID d’enregistreur pour ce writer est 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span><span class="sxs-lookup"><span data-stu-id="e64ea-263">The writer ID for this writer is 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span></span>

## <a name="mssearch-service-writer"></a><span data-ttu-id="e64ea-264">Rédacteur MSSearch service</span><span class="sxs-lookup"><span data-stu-id="e64ea-264">MSSearch Service Writer</span></span>

<span data-ttu-id="e64ea-265">Ce writer existe pour supprimer les fichiers d’index de recherche des clichés instantanés après la création.</span><span class="sxs-lookup"><span data-stu-id="e64ea-265">This writer exists to delete search index files from shadow copies after creation.</span></span> <span data-ttu-id="e64ea-266">Cela permet de réduire l’impact des e/s de copie sur écriture pendant les e/s normales sur ces fichiers sur le volume copié par cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="e64ea-266">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span>

<span data-ttu-id="e64ea-267">**Windows Server 2003 :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-267">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-268">Pour installer ce writer sur le serveur, vous devez installer le rôle Services de fichiers et activer le Search Service Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-268">To install this writer on the server, you must install the File Services role and enable the Windows Search Service.</span></span>

<span data-ttu-id="e64ea-269">La chaîne du nom de l’enregistreur pour ce writer est « VSS service Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-269">The writer name string for this writer is "MSSearch Service Writer".</span></span>

<span data-ttu-id="e64ea-270">L’ID d’enregistreur pour l’enregistreur du service MSSearch est CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span><span class="sxs-lookup"><span data-stu-id="e64ea-270">The writer ID for the MSSearch service writer is CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span></span>

## <a name="nps-vss-writer"></a><span data-ttu-id="e64ea-271">Enregistreur VSS NPS</span><span class="sxs-lookup"><span data-stu-id="e64ea-271">NPS VSS Writer</span></span>

<span data-ttu-id="e64ea-272">L’enregistreur NPS est chargé d’énumérer les fichiers de configuration du serveur NPS (Network Policy Server) pour les serveurs sur lesquels le rôle Services de stratégie et d’accès réseau est installé.</span><span class="sxs-lookup"><span data-stu-id="e64ea-272">The NPS writer is responsible for enumerating the Network Policy Server (NPS) configuration files for servers that have the Network Policy and Access Services role installed.</span></span>

<span data-ttu-id="e64ea-273">**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e64ea-273">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

<span data-ttu-id="e64ea-274">La chaîne du nom de l’enregistreur pour ce writer est « l’enregistreur VSS NPS ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-274">The writer name string for this writer is "NPS VSS Writer".</span></span>

<span data-ttu-id="e64ea-275">L’ID d’enregistreur pour l’enregistreur VSS NPS est 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span><span class="sxs-lookup"><span data-stu-id="e64ea-275">The writer ID for the NPS VSS writer is 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span></span>

## <a name="performance-counters-writer"></a><span data-ttu-id="e64ea-276">Enregistreur des compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="e64ea-276">Performance Counters Writer</span></span>

<span data-ttu-id="e64ea-277">Ce writer signale les fichiers de configuration du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="e64ea-277">This writer reports the performance counter configuration files.</span></span> <span data-ttu-id="e64ea-278">Ces fichiers sont modifiés uniquement lors de l’installation de l’application et doivent être sauvegardés et restaurés au cours des sauvegardes et restaurations de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-278">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

<span data-ttu-id="e64ea-279">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-279">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="e64ea-280">Les demandeurs doivent sauvegarder ces fichiers manuellement.</span><span class="sxs-lookup"><span data-stu-id="e64ea-280">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="e64ea-281">(Voir [sauvegarde et restauration de l’état du système](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="e64ea-281">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="e64ea-282">La chaîne du nom de l’enregistreur pour ce writer est « enregistreur des compteurs de performance ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-282">The writer name string for this writer is "Performance Counters Writer".</span></span>

<span data-ttu-id="e64ea-283">L’ID d’enregistreur pour l’enregistreur des compteurs de performance est 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span><span class="sxs-lookup"><span data-stu-id="e64ea-283">The writer ID for the Performance Counters Writer is 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span></span>

## <a name="registry-writer"></a><span data-ttu-id="e64ea-284">Enregistreur du Registre</span><span class="sxs-lookup"><span data-stu-id="e64ea-284">Registry Writer</span></span>

<span data-ttu-id="e64ea-285">Le rédacteur du registre fait état des fichiers du Registre Windows pour activer les sauvegardes et les restaurations sur place du Registre.</span><span class="sxs-lookup"><span data-stu-id="e64ea-285">The registry writer is reports the Windows registry files to enable in-place backups and restores of the registry.</span></span> <span data-ttu-id="e64ea-286">Il ne signale pas les ruches utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e64ea-286">It does not report user hives.</span></span>

<span data-ttu-id="e64ea-287">**Windows Server 2003 :** Dans Windows Server 2003, ce writer utilise un fichier de référentiel intermédiaire (parfois appelé « fichier de fractionnement ») pour stocker les données de registre.</span><span class="sxs-lookup"><span data-stu-id="e64ea-287">**Windows Server 2003:** In Windows Server 2003, this writer uses an intermediate repository file (sometimes called a "spit file") to store registry data.</span></span> <span data-ttu-id="e64ea-288">(Voir [opérations de sauvegarde et de restauration du Registre sous VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="e64ea-288">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="e64ea-289">**Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-289">**Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="e64ea-290">(Voir [opérations de sauvegarde et de restauration du Registre sous VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="e64ea-290">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="e64ea-291">La chaîne du nom de l’enregistreur pour ce writer est « Registry Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-291">The writer name string for this writer is "Registry Writer".</span></span>

<span data-ttu-id="e64ea-292">L’ID du writer du Registre est AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span><span class="sxs-lookup"><span data-stu-id="e64ea-292">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a><span data-ttu-id="e64ea-293">Enregistreur VSS de la passerelle Services Bureau à distance (services Terminal Server)</span><span class="sxs-lookup"><span data-stu-id="e64ea-293">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>

<span data-ttu-id="e64ea-294">Ce writer est chargé d’énumérer les fichiers de passerelle Services Bureau à distance (services Terminal Server) pour les serveurs qui ont Bureau à distance passerelle, un sous-rôle du rôle Services Bureau à distance, installé.</span><span class="sxs-lookup"><span data-stu-id="e64ea-294">This writer is responsible for enumerating the Remote Desktop Services (Terminal Services) Gateway files for servers that have Remote Desktop Gateway, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="e64ea-295">**Windows Server 2003 :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-295">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-296">Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-296">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="e64ea-297">La passerelle Services Bureau à distance dépend de plusieurs clés de Registre sauvegardées et doit donc être sauvegardée et restaurée en même temps que le registre.</span><span class="sxs-lookup"><span data-stu-id="e64ea-297">The Remote Desktop Services Gateway depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="e64ea-298">La chaîne du nom de l’enregistreur pour ce writer est « rédacteur de passerelle TS ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-298">The writer name string for this writer is "TS Gateway Writer".</span></span>

<span data-ttu-id="e64ea-299">L’ID d’enregistreur pour ce writer est 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span><span class="sxs-lookup"><span data-stu-id="e64ea-299">The writer ID for this writer is 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span></span>

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a><span data-ttu-id="e64ea-300">Enregistreur VSS du gestionnaire de licences des Services Bureau à distance (services Terminal Server)</span><span class="sxs-lookup"><span data-stu-id="e64ea-300">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="e64ea-301">Ce writer est chargé d’énumérer les fichiers de licences des services Bureau à distance (CAL) ou de licences des services Terminal Server (gestionnaire de licences TS) pour Services Bureau à distance les serveurs qui ont Bureau à distance licence, un sous-rôle du rôle Services Bureau à distance, installé.</span><span class="sxs-lookup"><span data-stu-id="e64ea-301">This writer is responsible for enumerating the Remote Desktop Services Licensing (RD Licensing) or Terminal Services Licensing (TS Licensing) files for servers that have Remote Desktop Licensing, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="e64ea-302">**Windows Server 2003 :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-302">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-303">Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.</span><span class="sxs-lookup"><span data-stu-id="e64ea-303">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="e64ea-304">Services Bureau à distance la gestion des licences dépend de plusieurs clés de Registre sauvegardées et doivent donc être sauvegardées et restaurées avec le registre.</span><span class="sxs-lookup"><span data-stu-id="e64ea-304">Remote Desktop Services Licensing depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="e64ea-305">La chaîne du nom de l’enregistreur pour ce writer est « TermServLicensing ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-305">The writer name string for this writer is "TermServLicensing".</span></span>

<span data-ttu-id="e64ea-306">L’ID d’enregistreur pour ce writer est 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span><span class="sxs-lookup"><span data-stu-id="e64ea-306">The writer ID for this writer is 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span></span>

## <a name="shadow-copy-optimization-writer"></a><span data-ttu-id="e64ea-307">Enregistreur d’optimisation des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="e64ea-307">Shadow Copy Optimization Writer</span></span>

<span data-ttu-id="e64ea-308">Ce writer supprime certains fichiers des clichés instantanés de volume.</span><span class="sxs-lookup"><span data-stu-id="e64ea-308">This writer deletes certain files from volume shadow copies.</span></span> <span data-ttu-id="e64ea-309">Cela permet de réduire l’impact des e/s de copie sur écriture pendant les e/s normales sur ces fichiers sur le volume copié par cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="e64ea-309">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span> <span data-ttu-id="e64ea-310">Les fichiers qui sont supprimés sont généralement des fichiers temporaires ou des fichiers qui ne contiennent pas d’utilisateur ou d’État du système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-310">The files that are deleted are typically temporary files or files that do not contain user or system state.</span></span>

<span data-ttu-id="e64ea-311">**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-311">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-312">La chaîne du nom de l’enregistreur pour ce writer est « enregistreur d’optimisation du cliché instantané ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-312">The writer name string for this writer is "Shadow Copy Optimization Writer".</span></span>

<span data-ttu-id="e64ea-313">L’ID d’enregistreur pour le writer d’optimisation du cliché instantané est 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span><span class="sxs-lookup"><span data-stu-id="e64ea-313">The writer ID for the shadow copy optimization writer is 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span></span>

## <a name="sync-share-service-writer"></a><span data-ttu-id="e64ea-314">Rédacteur de service de partage de synchronisation</span><span class="sxs-lookup"><span data-stu-id="e64ea-314">Sync Share Service Writer</span></span>

<span data-ttu-id="e64ea-315">**Windows Server 2012 R2 :** Ce writer est inclus dans Windows Server 2012 R2 et les versions ultérieures du serveur.</span><span class="sxs-lookup"><span data-stu-id="e64ea-315">**Windows Server 2012 R2:** This writer is included with Windows Server 2012 R2 and newer server versions.</span></span> <span data-ttu-id="e64ea-316">Elle n’est pas compatible avec les versions de bureau.</span><span class="sxs-lookup"><span data-stu-id="e64ea-316">It is not compatible with desktop versions.</span></span>

<span data-ttu-id="e64ea-317">Ce writer est chargé d’énumérer les partages de synchronisation sur les serveurs sur lesquels le service de partage de synchronisation est installé, et de garantir la cohérence des métadonnées et des données pendant la sauvegarde et la restauration.</span><span class="sxs-lookup"><span data-stu-id="e64ea-317">This writer is responsible for enumerating the sync shares on servers that have the Sync Share Service installed, and for ensuring that their metadata and data remain consistent during backup and restore.</span></span>

<span data-ttu-id="e64ea-318">Ce writer est présent uniquement lorsque le service de partage de synchronisation est installé et en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e64ea-318">This writer is only present when Sync Share Service is both installed and running.</span></span>

<span data-ttu-id="e64ea-319">Il y aura un composant enregistreur VSS pour chaque partage de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e64ea-319">There will be one VSS writer component for each sync share.</span></span> <span data-ttu-id="e64ea-320">Cela comprend les métadonnées et les chemins de données.</span><span class="sxs-lookup"><span data-stu-id="e64ea-320">This includes the metadata and data paths.</span></span> <span data-ttu-id="e64ea-321">Ils doivent être sauvegardés ensemble pour des fins de cohérence.</span><span class="sxs-lookup"><span data-stu-id="e64ea-321">These must be backed up together for consistency.</span></span>

<span data-ttu-id="e64ea-322">La chaîne du nom de l’enregistreur est « Sync share service VSS Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-322">The writer name string is "Sync Share Service VSS writer".</span></span>

<span data-ttu-id="e64ea-323">L’ID d’enregistreur est D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span><span class="sxs-lookup"><span data-stu-id="e64ea-323">The writer ID is D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span></span>

## <a name="system-writer"></a><span data-ttu-id="e64ea-324">Enregistreur du système</span><span class="sxs-lookup"><span data-stu-id="e64ea-324">System Writer</span></span>

<span data-ttu-id="e64ea-325">Le rédacteur du système énumère tous les fichiers binaires du système d’exploitation et du pilote, et il est requis pour une sauvegarde de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-325">The system writer enumerates all operating system and driver binaries and it is required for a system state backup.</span></span>

<span data-ttu-id="e64ea-326">**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-326">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-327">Ce writer s’exécute dans le cadre du service de services de chiffrement (CryptSvc).</span><span class="sxs-lookup"><span data-stu-id="e64ea-327">This writer runs as part of the Cryptographic Services (CryptSvc) service.</span></span> <span data-ttu-id="e64ea-328">L’enregistreur de système génère une liste de fichiers qui contient les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="e64ea-328">The system writer generates a file list that contains the following files:</span></span>

-   <span data-ttu-id="e64ea-329">Tous les fichiers statiques qui ont été installés.</span><span class="sxs-lookup"><span data-stu-id="e64ea-329">All static files that have been installed.</span></span> <span data-ttu-id="e64ea-330">Un fichier statique est un fichier qui est listé dans le manifeste de composant avec l’attribut de fichier **writeableType** défini sur « static » ou «».</span><span class="sxs-lookup"><span data-stu-id="e64ea-330">A static file is a file that is listed in the component manifest with the **writeableType** file attribute set to "static" or "".</span></span> <span data-ttu-id="e64ea-331">Les fichiers statiques incluent tous les fichiers protégés par Protection des ressources Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="e64ea-331">Static files include all files that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="e64ea-332">Toutefois, tous les fichiers statiques ne sont pas des fichiers protégés par WRP.</span><span class="sxs-lookup"><span data-stu-id="e64ea-332">However, not all static files are WRP-protected files.</span></span> <span data-ttu-id="e64ea-333">Par exemple, les fichiers de jeu sont statiques mais pas protégés par WRP pour permettre aux administrateurs de modifier les paramètres de contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="e64ea-333">For example, game files are static but not WRP-protected so that administrators can change parental control settings.</span></span>
-   <span data-ttu-id="e64ea-334">Le contenu du répertoire côte à côte (WinSxS) de Windows, y compris tous les manifestes, les composants facultatifs et les fichiers Win32 tiers.</span><span class="sxs-lookup"><span data-stu-id="e64ea-334">The contents of the Windows Side-by-Side (WinSxS) directory, including all manifests, optional components, and third-party Win32 files.</span></span>
    > [!Note]  
    > <span data-ttu-id="e64ea-335">La plupart des fichiers du répertoire% windir% \\ system32 sont des liens physiques vers des fichiers dans le répertoire winsxs.</span><span class="sxs-lookup"><span data-stu-id="e64ea-335">Many of the files in the %windir%\\system32 directory are hard links to files in the WinSxS directory.</span></span>

     

-   <span data-ttu-id="e64ea-336">Tous les fichiers PnP pour les pilotes installés (détenus par PnP).</span><span class="sxs-lookup"><span data-stu-id="e64ea-336">All PnP files for installed drivers (owned by PnP).</span></span>
-   <span data-ttu-id="e64ea-337">Tous les services en mode utilisateur et tous les pilotes non Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="e64ea-337">All user-mode services and non-PnP drivers.</span></span>
-   <span data-ttu-id="e64ea-338">Tous les catalogues appartenant à CryptSvc.</span><span class="sxs-lookup"><span data-stu-id="e64ea-338">All catalogs owned by CryptSvc.</span></span>

<span data-ttu-id="e64ea-339">L’application de restauration est chargée de définir les fichiers et le registre, et de définir les listes de contrôle d’accès pour qu’elles correspondent au cliché instantané du système.</span><span class="sxs-lookup"><span data-stu-id="e64ea-339">The restore application is responsible for laying down the files and registry and setting ACLs to match the system shadow copy.</span></span> <span data-ttu-id="e64ea-340">Les liens physiques appropriés doivent également être créés pour que la restauration de l’état du système aboutisse.</span><span class="sxs-lookup"><span data-stu-id="e64ea-340">The appropriate hard links must also be created for a system state restore to succeed.</span></span>

<span data-ttu-id="e64ea-341">La chaîne du nom de l’enregistreur pour ce writer est « System Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-341">The writer name string for this writer is "System Writer".</span></span>

<span data-ttu-id="e64ea-342">L’ID d’enregistreur pour l’enregistreur de système est E8132975-6F93-4464-A53E-1050253AE220.</span><span class="sxs-lookup"><span data-stu-id="e64ea-342">The writer ID for the system writer is E8132975-6F93-4464-A53E-1050253AE220.</span></span>

## <a name="task-scheduler-writer"></a><span data-ttu-id="e64ea-343">Rédacteur de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e64ea-343">Task Scheduler Writer</span></span>

<span data-ttu-id="e64ea-344">Ce writer signale les fichiers de tâches du planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="e64ea-344">This writer reports the task scheduler's task files.</span></span>

<span data-ttu-id="e64ea-345">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-345">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="e64ea-346">Les demandeurs doivent sauvegarder ces fichiers manuellement.</span><span class="sxs-lookup"><span data-stu-id="e64ea-346">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="e64ea-347">(Voir [sauvegarde et restauration de l’état du système](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="e64ea-347">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="e64ea-348">La chaîne du nom de l’enregistreur pour ce writer est « Planificateur de tâches Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-348">The writer name string for this writer is "Task Scheduler Writer".</span></span>

<span data-ttu-id="e64ea-349">L’ID d’enregistreur du writer est D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span><span class="sxs-lookup"><span data-stu-id="e64ea-349">The writer ID for the writer is D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span></span>

## <a name="vss-metadata-store-writer"></a><span data-ttu-id="e64ea-350">Enregistreur du magasin de métadonnées VSS</span><span class="sxs-lookup"><span data-stu-id="e64ea-350">VSS Metadata Store Writer</span></span>

<span data-ttu-id="e64ea-351">Ce writer signale les fichiers de métadonnées de l’enregistreur pour tous les enregistreurs VSS Express.</span><span class="sxs-lookup"><span data-stu-id="e64ea-351">This writer reports the writer metadata files for all VSS express writers.</span></span>

<span data-ttu-id="e64ea-352">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-352">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-353">La chaîne du nom de l’enregistreur pour ce writer est « VSS Express Writer Metadata Store Writer ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-353">The writer name string for this writer is "VSS Express Writer Metadata Store Writer".</span></span>

<span data-ttu-id="e64ea-354">L’ID d’enregistreur du writer est 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span><span class="sxs-lookup"><span data-stu-id="e64ea-354">The writer ID for the writer is 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span></span>

## <a name="windows-deployment-services-wds-writer"></a><span data-ttu-id="e64ea-355">Enregistreur des services de déploiement Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="e64ea-355">Windows Deployment Services (WDS) Writer</span></span>

<span data-ttu-id="e64ea-356">Ce writer signale les fichiers de données des services de déploiement Windows (WDS).</span><span class="sxs-lookup"><span data-stu-id="e64ea-356">This writer reports the Windows Deployment Services (WDS) data files.</span></span>

<span data-ttu-id="e64ea-357">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-357">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-358">La chaîne du nom de l’enregistreur pour ce writer est « enregistreur VSS WDS ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-358">The writer name string for this writer is "WDS VSS Writer".</span></span>

<span data-ttu-id="e64ea-359">L’ID d’enregistreur pour ce writer est 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span><span class="sxs-lookup"><span data-stu-id="e64ea-359">The writer ID for this writer is 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span></span>

## <a name="windows-internal-database-wid-writer"></a><span data-ttu-id="e64ea-360">Enregistreur de base de données interne Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="e64ea-360">Windows Internal Database (WID) Writer</span></span>

<span data-ttu-id="e64ea-361">Ce writer signale les fichiers de données de la base de données interne Windows (WID).</span><span class="sxs-lookup"><span data-stu-id="e64ea-361">This writer reports the Windows Internal Database (WID) data files.</span></span>

<span data-ttu-id="e64ea-362">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-363">La chaîne du nom de l’enregistreur pour ce writer est « WIDWriter ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-363">The writer name string for this writer is "WIDWriter".</span></span>

<span data-ttu-id="e64ea-364">L’ID d’enregistreur pour ce writer est 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span><span class="sxs-lookup"><span data-stu-id="e64ea-364">The writer ID for this writer is 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span></span>

## <a name="windows-internet-name-service-wins-writer"></a><span data-ttu-id="e64ea-365">Enregistreur WINS (Windows Internet Name Service)</span><span class="sxs-lookup"><span data-stu-id="e64ea-365">Windows Internet Name Service (WINS) Writer</span></span>

<span data-ttu-id="e64ea-366">Ce writer est responsable de l’énumération des fichiers requis pour WINS.</span><span class="sxs-lookup"><span data-stu-id="e64ea-366">This writer is responsible for enumerating files required for WINS.</span></span>

<span data-ttu-id="e64ea-367">**Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-367">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-368">La chaîne du nom de l’enregistreur pour ce writer est « enregistreur jet WINS ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-368">The writer name string for this writer is "WINS Jet Writer".</span></span>

<span data-ttu-id="e64ea-369">L’ID d’enregistreur pour ce writer est F08C1483-8407-4A26-8C26-6C267A629741.</span><span class="sxs-lookup"><span data-stu-id="e64ea-369">The writer ID for this writer is F08C1483-8407-4A26-8C26-6C267A629741.</span></span>

## <a name="wmi-writer"></a><span data-ttu-id="e64ea-370">Rédacteur WMI</span><span class="sxs-lookup"><span data-stu-id="e64ea-370">WMI Writer</span></span>

<span data-ttu-id="e64ea-371">Ce writer est utilisé pour identifier l’État et les données spécifiques à WMI lors des opérations de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="e64ea-371">This writer is used for identifying WMI-specific state and data during backup operations.</span></span> <span data-ttu-id="e64ea-372">Les données incluent des fichiers du référentiel WBEM.</span><span class="sxs-lookup"><span data-stu-id="e64ea-372">The data includes files from the WBEM repository.</span></span>

<span data-ttu-id="e64ea-373">**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e64ea-373">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="e64ea-374">La chaîne du nom de l’enregistreur pour ce writer est « Writer WMI ».</span><span class="sxs-lookup"><span data-stu-id="e64ea-374">The writer name string for this writer is "WMI Writer".</span></span>

<span data-ttu-id="e64ea-375">L’ID d’enregistreur pour ce writer est A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span><span class="sxs-lookup"><span data-stu-id="e64ea-375">The writer ID for this writer is A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span></span>

 

 
