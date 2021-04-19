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
# <a name="in-box-vss-writers"></a>Enregistreurs VSS intégrés

Le système d’exploitation Windows comprend un ensemble d’enregistreurs VSS chargés d’énumérer les données nécessaires aux différentes fonctionnalités Windows. On parle alors d’enregistreurs « intégrés ».

> [!Note]  
> Le writer intégré MSDE n’est pas disponible dans Windows Vista, Windows Server 2008 et versions ultérieures. Au lieu de cela, le writer SQL doit être utilisé pour sauvegarder les bases de données SQL Server. Seuls les SQL Server 2005 SP2 et versions ultérieures sont pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.

 

-   [Enregistreur VSS Active Directory Domain Services (NTDS)](#active-directory-domain-services-ntds-vss-writer)
-   [Rédacteur de services de fédération Active Directory (AD FS)](#active-directory-federation-services-writer)
-   [Enregistreur VSS services AD LDS (Active Directory Lightweight Directory Services) (LDS)](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Enregistreur services AD RMS (Active Directory Rights Management Services) (AD RMS)](#active-directory-rights-management-services-ad-rms-writer)
-   [Rédacteur de récupération automatique du système (ASR)](#automated-system-recovery-asr-writer)
-   [Enregistreur Service de transfert intelligent en arrière-plan (BITS)](#background-intelligent-transfer-service-bits-writer)
-   [Auteur de l’autorité de certification](#certificate-authority-writer)
-   [Rédacteur de service de cluster](#cluster-service-writer)
-   [Enregistreur VSS Volume partagé de cluster (CSV)](#cluster-shared-volume-csv-vss-writer)
-   [Enregistreur de base de données d’inscription de classe COM+](#com-class-registration-database-writer)
-   [Enregistreur de déduplication des données](#data-deduplication-writer)
-   [Réplication du système de fichiers distribués (DFSR)](#distributed-file-system-replication-dfsr)
-   [Enregistreur DHCP (Dynamic Host Configuration Protocol)](#dynamic-host-configuration-protocol-dhcp-writer)
-   [Service de réplication de fichiers (FRS)](#file-replication-service-frs)
-   [Enregistreur de Gestionnaire des ressources du serveur de fichiers (FSRM)](#file-server-resource-manager-fsrm-writer)
-   [Enregistreur Hyper-V](#hyper-v-writer)
-   [Rédacteur de configuration IIS](#iis-configuration-writer)
-   [Enregistreur de la métabase IIS](#iis-metabase-writer)
-   [Enregistreur Microsoft Message Queuing (MSMQ)](#microsoft-message-queuing-msmq-writer)
-   [Rédacteur MSSearch service](#mssearch-service-writer)
-   [Enregistreur VSS NPS](#nps-vss-writer)
-   [Enregistreur des compteurs de performances](#performance-counters-writer)
-   [Enregistreur du Registre](#registry-writer)
-   [Enregistreur VSS de la passerelle Services Bureau à distance (services Terminal Server)](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Enregistreur VSS du gestionnaire de licences des Services Bureau à distance (services Terminal Server)](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Enregistreur d’optimisation des clichés instantanés](#shadow-copy-optimization-writer)
-   [Rédacteur de service de partage de synchronisation](#sync-share-service-writer)
-   [Enregistreur du système](#system-writer)
-   [Rédacteur de Planificateur de tâches](#task-scheduler-writer)
-   [Enregistreur du magasin de métadonnées VSS](#vss-metadata-store-writer)
-   [Enregistreur des services de déploiement Windows (WDS)](#windows-deployment-services-wds-writer)
-   [Enregistreur de base de données interne Windows (WID)](#windows-internal-database-wid-writer)
-   [Enregistreur WINS (Windows Internet Name Service)](#windows-internet-name-service-wins-writer)
-   [Rédacteur WMI](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Enregistreur VSS Active Directory Domain Services (NTDS)

Ce writer signale le fichier de base de données NTDS (NTDS. dit) et les fichiers journaux associés. Ces fichiers sont nécessaires pour restaurer correctement l’Active Directory.

Il n’existe qu’un seul fichier Ntds. dit par contrôleur de domaine et il est signalé dans les métadonnées de l’enregistreur comme dans l’exemple suivant :

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Voici un exemple qui montre comment répertorier les composants dans les métadonnées du writer :

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

Au moment de la sauvegarde, l’enregistreur définit l’heure d’expiration de la sauvegarde dans les métadonnées de sauvegarde du writer. Les demandeurs doivent récupérer ces métadonnées à l’aide de [**IVssComponent :: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) pour déterminer si la base de données a expiré. Les bases de données expirées ne peuvent pas être restaurées.

Si l’ordinateur qui contient la base de données NTDS est un contrôleur de domaine, l’application de sauvegarde doit toujours effectuer une sauvegarde de l’état du système sur tous les volumes contenant des informations d’État du système critiques. Au moment de la restauration, l’application doit d’abord redémarrer l’ordinateur en mode de restauration des services d’annuaire, puis effectuer une restauration de l’état du système.

La chaîne du nom de l’enregistreur pour ce writer est « NTDS ».

L’ID d’enregistreur pour ce writer est B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Rédacteur de services de fédération Active Directory (AD FS)

Ce writer signale les fichiers de données services de fédération Active Directory (AD FS) (ADFS).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « l’enregistreur VSS ADFS ».

L’ID d’enregistreur pour ce writer est 772C45F8-AE01-4F94-940C-94961864ACAD.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Enregistreur VSS services AD LDS (Active Directory Lightweight Directory Services) (LDS)

Ce writer signale le fichier de base de données ADAM (fichier Adamntds. dit) et les fichiers journaux associés pour chaque instance dans% Program Files% \\ Microsoft Adam \\ instance *n* \\ Data, où *N* est le numéro d’instance ADAM. Ces fichiers journaux de base de données sont requis pour restaurer les instances ADAM.

**Windows XP :** Ce Writer n’est pas pris en charge.

Voici un exemple qui montre comment répertorier les composants dans les métadonnées du writer :

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

Au moment de la sauvegarde, l’enregistreur définit l’heure d’expiration de la sauvegarde dans les métadonnées de sauvegarde. Les applications de sauvegarde doivent récupérer ces métadonnées à l’aide de la méthode [**IVssComponent :: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) pour déterminer si la base de données a expiré. Les bases de données expirées ne peuvent pas être restaurées.

La chaîne du nom de l’enregistreur pour ce writer est « ADAM (instance *N*) writer », où *N* est le numéro de l’instance ADAM, par exemple « Adam (instance1) writer », « Adam (Instance2) writer », et ainsi de suite.

L’ID d’enregistreur pour ce writer est DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD. Cet ID d’enregistreur est le même pour toutes les instances.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Enregistreur services AD RMS (Active Directory Rights Management Services) (AD RMS)

Ce writer signale les fichiers de données du service de Active Directory Rights Management (AD RMS).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « AD RMS Writer ».

L’ID d’enregistreur pour ce writer est 886C43B1-D455-4428-A37F-4D6B9E43F50F.

## <a name="automated-system-recovery-asr-writer"></a>Rédacteur de récupération automatique du système (ASR)

L’Enregistreur ASR stocke la configuration des disques sur le système. Ce writer signale la base de données de configuration de démarrage (BCD) et est également chargé de démonter la ruche de Registre qui représente le BCD lors de la création de clichés instantanés. L’Enregistreur ASR doit être inclus dans toutes les sauvegardes requises pour la récupération complète. Pour plus d’informations sur ASR, consultez [utilisation de la récupération automatique du système VSS pour la récupération d’urgence](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « Enregistreur ASR ».

L’ID d’enregistreur pour l’Enregistreur ASR est BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>Enregistreur Service de transfert intelligent en arrière-plan (BITS)

Le writer BITS utilise la clé de Registre **FilesNotToBackup** pour exclure des fichiers du dossier de cache bits. L’emplacement du cache par défaut est% AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ cache.

**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

En outre, l’enregistreur BITS exclut les fichiers suivants de la sauvegarde : les fichiers d’État du service BITS (Qmgr0. dat et Qmgr1. dat), le fichier journal de débogage BITS et les fichiers BITS partiellement téléchargés.

Si le fichier de destination de téléchargement BITS est un fichier SMB, le compte client doit avoir une relation d’approbation avec le serveur, sinon les sauvegardes peuvent échouer.

La chaîne du nom de l’enregistreur pour ce writer est « Writer BITS ».

L’ID d’enregistreur pour le writer BITS est 4969D978-BE47-48B0-B100-F328F07AC1E0.

## <a name="certificate-authority-writer"></a>Auteur de l’autorité de certification

Ce writer est responsable de l’énumération des fichiers de données pour le serveur de certificats.

La chaîne du nom de l’enregistreur pour ce writer est « Certificate Authority ».

**Windows XP :** La chaîne du nom de l’enregistreur pour ce writer est « Certificate Server Writer ».

L’ID d’enregistreur du writer est 6F5B15B5-DA24-4D88-B737-63063E3A1F86.

## <a name="cluster-service-writer"></a>Rédacteur de service de cluster

L’enregistreur VSS du service de cluster est documenté dans la documentation de l’API du [service de cluster](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .

**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge avant Windows Vista avec Service Pack 1 (SP1) et Windows Server 2008.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Enregistreur VSS Volume partagé de cluster (CSV)

Ce writer signale les fichiers de données Volume partagé de cluster (CSV). Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.

**Windows server 2008 R2, Windows server 2008 et Windows server 2003 :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « Volume partagé de cluster VSS Writer ».

L’ID d’enregistreur du writer est 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.

## <a name="com-class-registration-database-writer"></a>Enregistreur de base de données d’inscription de classe COM+

Ce writer est responsable du contenu du \\ répertoire d’inscription% systemroot%. Le catalogue COM+ est un fichier de l’inscription% SystemRoot% \\ avec un nom qui suit le modèle R *xxxxxxxxxxxx*. CLB, où *xxxxxxxxxxxx* est un nombre hexadécimal à 12 chiffres. Il peut y avoir plusieurs fichiers de ce type si des applications COM+ ont été configurées sur l’ordinateur. Le fichier qui contient le catalogue COM+ actuel est le fichier ayant la plus grande valeur *xxxxxxxxxxxx*.

**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La base de données d’inscription de classe COM+ dépend d’une clé de Registre sauvegardée et doit donc être sauvegardée et restaurée avec le registre.

Pour restaurer la base de données d’inscription COM+, une application de sauvegarde (demandeur) doit appeler la méthode [**ICOMAdminCatalog :: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

La chaîne du nom de l’enregistreur pour ce writer est « COM+ REGDB Writer ».

L’ID d’enregistreur pour le writer de base de données d’inscription de classe COM+ est 542DA469-D3E1-473C-9F4F-7847F01FC64F.

## <a name="data-deduplication-writer"></a>Enregistreur de déduplication des données

L’enregistreur VSS de la déduplication des données est documenté dans la documentation de l’API de [déduplication des données](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) . Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.

**Windows server 2008 R2, Windows server 2008 et Windows server 2003 :** Ce Writer n’est pas pris en charge.

## <a name="distributed-file-system-replication-dfsr"></a>Réplication du système de fichiers distribués (DFSR)

Le composant suivant comprend un enregistreur VSS : [réplication de système de fichiers DFS (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>Enregistreur DHCP (Dynamic Host Configuration Protocol)

Ce writer est responsable de l’énumération des fichiers requis pour le rôle serveur DHCP. Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.

La chaîne du nom de l’enregistreur pour ce writer est « Writer jet DHCP ».

L’ID d’enregistreur pour ce writer est BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>Service de réplication de fichiers (FRS)

Le rédacteur du service de réplication de fichiers est documenté dans [sauvegarde et restauration d’un dossier SYSVOL FRS-Replicated](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).

**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.

## <a name="file-server-resource-manager-fsrm-writer"></a>Enregistreur de Gestionnaire des ressources du serveur de fichiers (FSRM)

Ce writer énumère les fichiers de configuration FSRM utilisés pour la sauvegarde de l’état du système. Pendant les opérations de restauration, il empêche les modifications dans la configuration de FSRM et interrompt temporairement l’application des quotas et des filtres de fichiers. Une fois la restauration terminée, l’enregistreur actualise FSRM avec la configuration qui a été restaurée. Ce writer est présent uniquement lorsque FSRM (partie du rôle Services de fichiers) est installé et en cours d’exécution. Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.

**Windows Server 2003 :** Ce Writer n’est pas pris en charge avant Windows Server 2003 R2.

La chaîne du nom de l’enregistreur pour ce writer est « scripteur FSRM ».

L’ID d’enregistreur pour ce writer est 12CE4370-5BB7-4C58-A76A-E5D5097E3674.

## <a name="hyper-v-writer"></a>Enregistreur Hyper-V

L’enregistreur VSS Hyper-V est documenté dans la documentation de l’API [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) . Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.

**Windows Server 2003 :** Ce Writer n’est pas pris en charge avant Windows Server 2008.

## <a name="iis-configuration-writer"></a>Rédacteur de configuration IIS

L’enregistreur de configuration IIS est chargé d’énumérer les fichiers de configuration IIS.

**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008. Les demandeurs doivent sauvegarder les fichiers de configuration IIS, y compris le fichier de machine.config .NET FX ou le fichier de web.config racine ASP.NET.

Ce writer ne sauvegarde pas le fichier de machine.config .NET FX ou le fichier de web.config racine ASP.NET, car ces fichiers sont énumérés par l’enregistreur de système.

Ce writer sauvegarde tous les fichiers qui se trouvent dans les répertoires% windir% \\ system32 \\ inetsrv \\ config \\ et% windir% \\ system32 \\ inetsrv \\ config, à l’exception des fichiers qui sont énumérés par l’enregistreur de système.

L’ID d’enregistreur pour l’enregistreur de configuration IIS est 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.

## <a name="iis-metabase-writer"></a>Enregistreur de la métabase IIS

L’enregistreur de métabase Internet Information Server (IIS) est chargé d’énumérer le fichier de la métabase IIS.

**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008. Les demandeurs doivent sauvegarder le fichier de la métabase IIS.

L’ID d’enregistreur pour l’enregistreur de métabase IIS est 59B1f0CF-90EF-465F-9609-6CA8B2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>Enregistreur Microsoft Message Queuing (MSMQ)

Ce writer signale les fichiers de données Microsoft Message Queuing (MSMQ).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne de nom de l’enregistreur pour ce writer est « MSMQ Writer (*SvcName*) », où *SvcName* est le nom du service MSMQ auquel le writer est associé. Pour l’installation par défaut, le nom du service est « MSMQ ». Pour les instances en cluster, le nom du service est MSMQ $*resourceName*, où *resourceName* est le nom de la ressource MSMQ en cluster.

L’ID d’enregistreur pour ce writer est 7E47B561-971A-46E6-96B9-696EEAA53B2A.

## <a name="mssearch-service-writer"></a>Rédacteur MSSearch service

Ce writer existe pour supprimer les fichiers d’index de recherche des clichés instantanés après la création. Cela permet de réduire l’impact des e/s de copie sur écriture pendant les e/s normales sur ces fichiers sur le volume copié par cliché instantané.

**Windows Server 2003 :** Ce Writer n’est pas pris en charge.

Pour installer ce writer sur le serveur, vous devez installer le rôle Services de fichiers et activer le Search Service Windows.

La chaîne du nom de l’enregistreur pour ce writer est « VSS service Writer ».

L’ID d’enregistreur pour l’enregistreur du service MSSearch est CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>Enregistreur VSS NPS

L’enregistreur NPS est chargé d’énumérer les fichiers de configuration du serveur NPS (Network Policy Server) pour les serveurs sur lesquels le rôle Services de stratégie et d’accès réseau est installé.

**Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge jusqu’à Windows Vista avec SP1 et Windows Server 2008.

La chaîne du nom de l’enregistreur pour ce writer est « l’enregistreur VSS NPS ».

L’ID d’enregistreur pour l’enregistreur VSS NPS est 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Enregistreur des compteurs de performances

Ce writer signale les fichiers de configuration du compteur de performance. Ces fichiers sont modifiés uniquement lors de l’installation de l’application et doivent être sauvegardés et restaurés au cours des sauvegardes et restaurations de l’état du système.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge. Les demandeurs doivent sauvegarder ces fichiers manuellement. (Voir [sauvegarde et restauration de l’état du système](locating-additional-system-files.md).)

La chaîne du nom de l’enregistreur pour ce writer est « enregistreur des compteurs de performance ».

L’ID d’enregistreur pour l’enregistreur des compteurs de performance est 0BADA1DE-01A9-4625-8278-69E735F39DD2.

## <a name="registry-writer"></a>Enregistreur du Registre

Le rédacteur du registre fait état des fichiers du Registre Windows pour activer les sauvegardes et les restaurations sur place du Registre. Il ne signale pas les ruches utilisateur.

**Windows Server 2003 :** Dans Windows Server 2003, ce writer utilise un fichier de référentiel intermédiaire (parfois appelé « fichier de fractionnement ») pour stocker les données de registre. (Voir [opérations de sauvegarde et de restauration du Registre sous VSS](registry-backup-and-restore-operations-under-vss.md).)

**Windows XP :** Ce Writer n’est pas pris en charge. (Voir [opérations de sauvegarde et de restauration du Registre sous VSS](registry-backup-and-restore-operations-under-vss.md).)

La chaîne du nom de l’enregistreur pour ce writer est « Registry Writer ».

L’ID du writer du Registre est AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>Enregistreur VSS de la passerelle Services Bureau à distance (services Terminal Server)

Ce writer est chargé d’énumérer les fichiers de passerelle Services Bureau à distance (services Terminal Server) pour les serveurs qui ont Bureau à distance passerelle, un sous-rôle du rôle Services Bureau à distance, installé.

**Windows Server 2003 :** Ce Writer n’est pas pris en charge.

Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.

La passerelle Services Bureau à distance dépend de plusieurs clés de Registre sauvegardées et doit donc être sauvegardée et restaurée en même temps que le registre.

La chaîne du nom de l’enregistreur pour ce writer est « rédacteur de passerelle TS ».

L’ID d’enregistreur pour ce writer est 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Enregistreur VSS du gestionnaire de licences des Services Bureau à distance (services Terminal Server)

Ce writer est chargé d’énumérer les fichiers de licences des services Bureau à distance (CAL) ou de licences des services Terminal Server (gestionnaire de licences TS) pour Services Bureau à distance les serveurs qui ont Bureau à distance licence, un sous-rôle du rôle Services Bureau à distance, installé.

**Windows Server 2003 :** Ce Writer n’est pas pris en charge.

Ce writer est un enregistreur intégré pour les versions de système d’exploitation Windows Server ; elle n’est pas fournie avec le client Windows.

Services Bureau à distance la gestion des licences dépend de plusieurs clés de Registre sauvegardées et doivent donc être sauvegardées et restaurées avec le registre.

La chaîne du nom de l’enregistreur pour ce writer est « TermServLicensing ».

L’ID d’enregistreur pour ce writer est 5382579C-98DF-47A7-AC6C-98A6D7106E09.

## <a name="shadow-copy-optimization-writer"></a>Enregistreur d’optimisation des clichés instantanés

Ce writer supprime certains fichiers des clichés instantanés de volume. Cela permet de réduire l’impact des e/s de copie sur écriture pendant les e/s normales sur ces fichiers sur le volume copié par cliché instantané. Les fichiers qui sont supprimés sont généralement des fichiers temporaires ou des fichiers qui ne contiennent pas d’utilisateur ou d’État du système.

**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « enregistreur d’optimisation du cliché instantané ».

L’ID d’enregistreur pour le writer d’optimisation du cliché instantané est 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.

## <a name="sync-share-service-writer"></a>Rédacteur de service de partage de synchronisation

**Windows Server 2012 R2 :** Ce writer est inclus dans Windows Server 2012 R2 et les versions ultérieures du serveur. Elle n’est pas compatible avec les versions de bureau.

Ce writer est chargé d’énumérer les partages de synchronisation sur les serveurs sur lesquels le service de partage de synchronisation est installé, et de garantir la cohérence des métadonnées et des données pendant la sauvegarde et la restauration.

Ce writer est présent uniquement lorsque le service de partage de synchronisation est installé et en cours d’exécution.

Il y aura un composant enregistreur VSS pour chaque partage de synchronisation. Cela comprend les métadonnées et les chemins de données. Ils doivent être sauvegardés ensemble pour des fins de cohérence.

La chaîne du nom de l’enregistreur est « Sync share service VSS Writer ».

L’ID d’enregistreur est D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>Enregistreur du système

Le rédacteur du système énumère tous les fichiers binaires du système d’exploitation et du pilote, et il est requis pour une sauvegarde de l’état du système.

**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

Ce writer s’exécute dans le cadre du service de services de chiffrement (CryptSvc). L’enregistreur de système génère une liste de fichiers qui contient les fichiers suivants :

-   Tous les fichiers statiques qui ont été installés. Un fichier statique est un fichier qui est listé dans le manifeste de composant avec l’attribut de fichier **writeableType** défini sur « static » ou «». Les fichiers statiques incluent tous les fichiers protégés par Protection des ressources Windows (WRP). Toutefois, tous les fichiers statiques ne sont pas des fichiers protégés par WRP. Par exemple, les fichiers de jeu sont statiques mais pas protégés par WRP pour permettre aux administrateurs de modifier les paramètres de contrôle parental.
-   Le contenu du répertoire côte à côte (WinSxS) de Windows, y compris tous les manifestes, les composants facultatifs et les fichiers Win32 tiers.
    > [!Note]  
    > La plupart des fichiers du répertoire% windir% \\ system32 sont des liens physiques vers des fichiers dans le répertoire winsxs.

     

-   Tous les fichiers PnP pour les pilotes installés (détenus par PnP).
-   Tous les services en mode utilisateur et tous les pilotes non Plug-and-Play.
-   Tous les catalogues appartenant à CryptSvc.

L’application de restauration est chargée de définir les fichiers et le registre, et de définir les listes de contrôle d’accès pour qu’elles correspondent au cliché instantané du système. Les liens physiques appropriés doivent également être créés pour que la restauration de l’état du système aboutisse.

La chaîne du nom de l’enregistreur pour ce writer est « System Writer ».

L’ID d’enregistreur pour l’enregistreur de système est E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Rédacteur de Planificateur de tâches

Ce writer signale les fichiers de tâches du planificateur de tâches.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge. Les demandeurs doivent sauvegarder ces fichiers manuellement. (Voir [sauvegarde et restauration de l’état du système](locating-additional-system-files.md).)

La chaîne du nom de l’enregistreur pour ce writer est « Planificateur de tâches Writer ».

L’ID d’enregistreur du writer est D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>Enregistreur du magasin de métadonnées VSS

Ce writer signale les fichiers de métadonnées de l’enregistreur pour tous les enregistreurs VSS Express.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « VSS Express Writer Metadata Store Writer ».

L’ID d’enregistreur du writer est 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.

## <a name="windows-deployment-services-wds-writer"></a>Enregistreur des services de déploiement Windows (WDS)

Ce writer signale les fichiers de données des services de déploiement Windows (WDS).

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « enregistreur VSS WDS ».

L’ID d’enregistreur pour ce writer est 82CB5521-68DB-4626-83A4-7FC6F88853E9.

## <a name="windows-internal-database-wid-writer"></a>Enregistreur de base de données interne Windows (WID)

Ce writer signale les fichiers de données de la base de données interne Windows (WID).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « WIDWriter ».

L’ID d’enregistreur pour ce writer est 8D5194E1-E455-434A-B2E5-51296CCE67DF.

## <a name="windows-internet-name-service-wins-writer"></a>Enregistreur WINS (Windows Internet Name Service)

Ce writer est responsable de l’énumération des fichiers requis pour WINS.

**Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « enregistreur jet WINS ».

L’ID d’enregistreur pour ce writer est F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>Rédacteur WMI

Ce writer est utilisé pour identifier l’État et les données spécifiques à WMI lors des opérations de sauvegarde. Les données incluent des fichiers du référentiel WBEM.

**Windows Server 2003 et Windows XP :** Ce Writer n’est pas pris en charge.

La chaîne du nom de l’enregistreur pour ce writer est « Writer WMI ».

L’ID d’enregistreur pour ce writer est A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
