---
description: La liste suivante décrit les fonctionnalités nouvelles et mises à jour pour Windows Server 2012 et Windows Server 2012 R2. Pour plus d’informations sur les nouvelles technologies Windows 8 et Windows 8.1, voir technologies Windows 8 et Windows 8.1.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Nouveautés : Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ba276ea8256299c5e667cbb5a1d2b0872bb282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866622"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Nouveautés : Windows Server 2012 R2 & Windows Server 2012

La liste suivante décrit les fonctionnalités nouvelles et mises à jour pour Windows Server 2012 et Windows Server 2012 R2. Pour plus d’informations sur les nouvelles technologies Windows 8 et Windows 8.1, voir [technologies Windows 8 et Windows 8.1](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>Nouveautés de Windows Server 2012 R2

-   [Déduplication des données](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    La déduplication des données détecte et supprime les doublons dans les données d’un volume, tout en veillant à ce que les données restent correctes et complètes. Elle permet ainsi de stocker davantage de données de fichier sur un volume en prenant moins d'espace. Pour Windows Server 2012 R2, un certain nombre de paramètres et de codes d’erreur ont été activés, et la classe [**\_ DedupFileMetadata msft**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) a été ajoutée.

-   [Journalisation de l’inventaire logiciel](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Nouveau !** La journalisation de l’inventaire logiciel recueille les données de licence relatives aux logiciels installés sur un serveur Windows et fournit un accès à distance aux données afin de pouvoir les agréger facilement par un centre de données.

-   [Serveur cible iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    L’API du serveur cible iSCSI fournit des fournisseurs de Windows Management Instrumentation (WMI) pour la gestion du serveur cible Microsoft iSCSI, tels que la création de disques virtuels, et pour leur présentation au client. Un certain nombre de nouvelles fonctionnalités ont été ajoutées pour Windows Server 2012 R2.

-   [Inscription de la gestion des périphériques mobiles](../mdmreg/mobile-device-management-registration-portal.md)

    **Nouveau !** Une tendance du secteur s’est développée dans laquelle les employés connectent leurs appareils informatiques mobiles personnels au réseau d’entreprise et aux ressources (localement ou dans le Cloud) pour effectuer des tâches d’espace de travail. Cette tendance nécessite une prise en charge pour faciliter la configuration du réseau et des ressources, de telle sorte que les employés puissent inscrire des appareils personnels auprès de l’entreprise à des fins professionnelles. Les applications et la technologie pour la prise en charge de la configuration simplifiée doivent également permettre aux professionnels de l’informatique de gérer les risques associés à la connexion d’appareils non contrôlés au réseau d’entreprise. L’inscription de la gestion des appareils mobiles (MDM) inscrit un appareil dans un service de gestion.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell est un interpréteur de ligne de commande basé sur des tâches et un langage de script conçu spécialement pour l’administration du système. Nouveauté de Windows Server 2012 R2, Windows PowerShell v4 prend en charge la configuration d’état souhaité, qui est une nouvelle plateforme de gestion dans Windows PowerShell qui permet de déployer et de gérer des données de configuration pour les services logiciels et de gérer l’environnement dans lequel ces services s’exécutent.

## <a name="whats-new-for-windows-server-2012"></a>Nouveautés de Windows Server 2012

-   [Clustering Windows](/previous-versions/windows/desktop/mscs/windows-clustering)

    Le clustering Windows vous permet de gérer à la fois les clusters avec équilibrage de charge réseau et les clusters de basculement. De nombreuses nouvelles fonctionnalités ont été ajoutées dans cette version, notamment les nouvelles fonctionnalités de gestion de groupe, les propriétés communes et l’intégration avec WMI.

-   [Journalisation des accès utilisateur](/previous-versions/windows/desktop/ual/user-access-logging)

    **Nouveau !** La journalisation des accès utilisateur est un Framework commun pour les rôles Windows Server afin de signaler leurs mesures de consommation respectives. Ce Framework de base est un composant fondamental et essentiel de la solution de gestion des licences plus étendue.

-   [Gestion à distance de Windows](../winrm/portal.md)

    La gestion à distance de Windows (WinRM) est l’implémentation Microsoft du protocole Gestion des services Web, un protocole SOAP (Simple Object Access Protocol) standard, compatible avec un pare-feu qui permet l’interaction entre du matériel et des systèmes d’exploitation de différents fabricants. Windows Server 2012 comprend un certain nombre d’API de connexion qui se concentrent sur l’interaction avec les instances et les shells en cours d’exécution.

-   [Infrastructure de gestion Windows](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Nouveau !** Les fonctionnalités de l’infrastructure de gestion Windows (MI) représentent la dernière version des technologies Windows Management Instrumentation (WMI), qui sont basées sur la norme CIM de la DMTF (Distributed Management Task Force). MI est entièrement compatible avec les versions précédentes de WMI et fournit un hôte de fonctionnalités et d’avantages qui facilitent la conception et le développement de fournisseurs et de clients.

-   [Déduplication des données](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Nouveau !** La déduplication des données détecte et supprime les doublons dans les données d’un volume, tout en veillant à ce que les données restent correctes et complètes. Elle permet ainsi de stocker davantage de données de fichier sur un volume en prenant moins d'espace.

-   [Serveur cible iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Nouveau !** L’API du serveur cible iSCSI fournit des fournisseurs de Windows Management Instrumentation (WMI) pour la gestion du serveur cible Microsoft iSCSI, tels que la création de disques virtuels, et pour leur présentation au client.

-   [Fournisseur NFS pour WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Nouveau !** Le fournisseur NFS WMI offre un moyen de gérer les paramètres du serveur et du client NFS, les partages de fichiers, les groupes de serveurs et les groupes de clients.

-   [Fichiers hors connexion](../devnotes/offline-files.md)

    L’API Fichiers hors connexion permet aux applications de contrôler et de surveiller le comportement de Fichiers hors connexion par programmation. Windows Server 2012 ajoute les fonctions [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) et [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) .

-   [Gestion SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Nouveau !** L’API de gestion SMB fournit des classes et des méthodes WMI pour gérer les partages et l’accès au partage.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server fournit les options d’installation minimale du serveur pour les ordinateurs qui exécutent le système d’exploitation Windows Server 2008 ou version ultérieure. Windows Server 2012 offre Server Core comme une configuration et des options d’installation.

-   [Sauvegarde Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    La fonctionnalité de Sauvegarde Windows Server sauvegarde et restaure automatiquement les données d’application. Windows Server 2012 comprend l’API du fournisseur de sauvegarde Cloud.

-   [Partage de bureau Windows](/previous-versions/windows/desktop/rdp/rdp-portal)

    Le partage de bureau Windows est une technologie de partage d’écran à plusieurs tiers. Windows Server 2012 implémente cette technologie à l’aide de l’API de duplication Windows.

-   [Services Bureau à distance](../termserv/terminal-services-portal.md)

    Le partage de bureau Windows permet à l’utilisateur d’accéder à distance à une instance du système d’exploitation. Windows Server 2012 inclut un certain nombre de nouvelles fonctionnalités, notamment les sessions enfants, la redirection de média RemoteFX et le client Bureau à distance Broker.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell est un interpréteur de ligne de commande basé sur des tâches et un langage de script conçu spécialement pour l’administration du système. Nouveauté de Windows Server 2012, Windows PowerShell v3 prend en charge le flux de travail Windows PowerShell, qui tire parti des avantages de Windows Workflow Foundation pour permettre l’automatisation des tâches de longue durée.

-   [OData de gestion](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Nouveau !** Également connu sous le nom de Windows PowerShell Web services, Management OData, nouveauté de Windows PowerShell v3, permet la création d’un point de terminaison de service Web ASP.NET qui expose les données de gestion, les ACE par le biais de commandes Windows PowerShell, en tant qu’entités de service Web OData.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Server 2012 R2 sur TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 et Windows Server 2012 sur la bibliothèque TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 sur Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
