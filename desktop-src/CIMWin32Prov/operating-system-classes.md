---
description: La catégorie de système d’exploitation regroupe les classes qui représentent des objets liés au système d’exploitation.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Classes du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f47df8a949e3ac07bf2099ea708d496bed87298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540808"
---
# <a name="operating-system-classes"></a>Classes du système d’exploitation

La catégorie de système d’exploitation regroupe les classes qui représentent des objets liés au système d’exploitation. Ils désignent les différentes configurations et paramètres qui définissent un environnement informatique. Voici quelques exemples : la configuration de démarrage, les paramètres COM (Component Object Model), les paramètres de l’environnement du bureau, les pilotes, les paramètres de sécurité, les paramètres utilisateur et les paramètres du Registre.

La catégorie système d’exploitation est regroupée dans les sous-catégories suivantes :

-   [COM](#com)
-   [Bureau](#desktop)
-   [Pilotes](#drivers)
-   [Journal des événements](#windows-event-log)
-   [Système de fichiers](#file-system)
-   [Objets de traitement](#job-objects)
-   [Mémoire et fichiers d’échange](#memory-and-page-files)
-   [Audio ou visuel multimédia](#multimedia-audio-or-visual)
-   [Mise en réseau](#networking)
-   [Événements du système d’exploitation](#operating-system-events)
-   [Paramètres du système d’exploitation](#operating-system-settings)
-   [Processus](#processes)
-   [Registre](#registry)
-   [Travaux du planificateur](#scheduler-jobs)
-   [Sécurité](#security)
-   [Services](#services)
-   [Partages](#shares)
-   [Menu Démarrer](#start-menu)
-   [Stockage](#storage)
-   [Utilisateurs](#users)
-   [Activation de produit Windows](#windows-product-activation)

## <a name="com"></a>COM

La sous-catégorie COM regroupe les classes qui représentent les paramètres COM et DCOM, les classes et les paramètres d’application cliente.



| Classe                                                                                           | Description                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ClassicCOMApplicationClasses Win32**](win32-classiccomapplicationclasses.md)               | Classe d’association<br/> Établit un lien entre une application DCOM et un composant COM groupé.<br/>                                                                             |
| [**\_ClassicCOMClass Win32**](win32-classiccomclass.md)                                         | Classe d’instance<br/> Représente les propriétés d’un composant COM.<br/>                                                                                                   |
| [**\_ClassicCOMClassSettings Win32**](win32-classiccomclasssettings.md)                         | Classe d’association<br/> Met en relation une classe COM et les paramètres utilisés pour configurer des instances de la classe COM.<br/>                                                           |
| [**\_ClientApplicationSetting Win32**](win32-clientapplicationsetting.md)                       | Classe d’association<br/> Met en relation un exécutable et une application DCOM qui contient les options de configuration DCOM pour le fichier exécutable.<br/>                           |
| [**Win32 \_ Comapplication**](win32-comapplication.md)                                           | Classe d’instance<br/> Représente une application COM.<br/>                                                                                                                   |
| [**\_COMApplicationClasses Win32**](win32-comapplicationclasses.md)                             | Classe d’association<br/> Met en relation un composant COM et l’application COM où il réside.<br/>                                                                            |
| [**\_COMApplicationSettings Win32**](win32-comapplicationsettings.md)                           | Classe d’association<br/> Établit une relation entre une application DCOM et ses paramètres de configuration.<br/>                                                                                   |
| [**Win32, \_ classe**](win32-comclass.md)                                                       | Classe d’instance<br/> Représente les propriétés d’un composant COM.<br/>                                                                                                   |
| [**\_ComClassAutoEmulator Win32**](win32-comclassautoemulator.md)                               | Classe d’association<br/> Met en relation une classe COM et une autre classe COM émulée automatiquement.<br/>                                                                    |
| [**\_ComClassEmulator Win32**](win32-comclassemulator.md)                                       | Classe d’association<br/> Met en relation deux versions d’une classe COM.<br/>                                                                                                         |
| [**\_ComponentCategory Win32**](win32-componentcategory.md)                                     | Classe d’instance<br/> Représente une catégorie de composant.<br/>                                                                                                                |
| [**Configuration de Win32 \_**](win32-comsetting.md)                                                   | Classe d’instance<br/> Représente les paramètres associés à un composant COM ou une application COM.<br/>                                                                     |
| [**\_DCOMApplication Win32**](win32-dcomapplication.md)                                         | Classe d’instance<br/> Représente les propriétés d’une application DCOM.<br/>                                                                                                |
| [**\_DCOMApplicationAccessAllowedSetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Classe d’association<br/> Met en relation l’instance [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) et les identificateurs de sécurité de l’utilisateur (SID) qui peuvent y accéder.<br/> |
| [**\_DCOMApplicationLaunchAllowedSetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Classe d’association<br/> Met en relation l’instance [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) et les SID d’utilisateur qui peuvent la lancer.<br/>                           |
| [**\_DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md)                           | Classe d’instance<br/> Représente les paramètres d’une application DCOM.<br/>                                                                                                  |
| [**\_ImplementedCategory Win32**](win32-implementedcategory.md)                                 | Classe d’association<br/> Met en relation une catégorie de composant et la classe COM à l’aide de ses interfaces.<br/>                                                                         |



 

## <a name="desktop"></a>Bureau

La sous-catégorie Desktop regroupe des classes qui représentent des objets qui définissent une configuration de bureau spécifique.



| Classe                                           | Description                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Bureau Win32**](win32-desktop.md)         | Classe d’instance<br/> Représente les caractéristiques communes du Bureau d’un utilisateur.<br/>                                    |
| [**\_Environnement Win32**](win32-environment.md) | Classe d’instance<br/> Représente un environnement ou un paramètre d’environnement système sur un système informatique exécutant Windows.<br/> |
| [**\_Fuseau horaire Win32**](win32-timezone.md)       | Classe d’instance<br/> Représente les informations de fuseau horaire pour un système informatique exécutant Windows.<br/>                   |
| [**\_UserDesktop Win32**](win32-userdesktop.md) | Classe d’association<br/> Met en relation un compte d’utilisateur et les paramètres de bureau qui lui sont spécifiques.<br/>                   |



 

## <a name="drivers"></a>Pilotes

La sous-catégorie des pilotes regroupe les classes qui représentent les pilotes de périphériques virtuels et les pilotes système pour les services de base.



| Classe                                             | Description                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_SystemDriver Win32**](win32-systemdriver.md) | Classe d’instance<br/> Représente le pilote système pour un service de base.<br/> |



 

## <a name="file-system"></a>Système de fichiers

La sous-catégorie du système de fichiers regroupe des classes qui représentent la façon dont un disque dur est organisé logiquement. Cela comprend le type de système de fichiers utilisé, la structure de répertoires et la façon dont le disque est partitionné.



| Classe                                                                               | Description                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CIMLogicalDeviceCIMDataFile Win32**](win32-cimlogicaldevicecimdatafile.md)     | Classe d’association<br/> Établit un lien entre les fichiers de données et les périphériques logiques, indiquant les fichiers de pilote utilisés par l’appareil.<br/>                                                      |
| [**\_Répertoire Win32**](win32-directory.md)                                         | Classe d’instance<br/> Représente une entrée de répertoire sur un système informatique exécutant Windows.<br/>                                                                              |
| [**\_DirectorySpecification Win32**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Classe d’instance<br/> Représente la disposition de répertoire pour le produit.<br/>                                                                                                |
| [**\_DiskDriveToDiskPartition Win32**](win32-diskdrivetodiskpartition.md)           | Classe d’association<br/> Met en relation un lecteur de disque et une partition existante.<br/>                                                                                         |
| [**\_DiskPartition Win32**](win32-diskpartition.md)                                 | Classe d’instance<br/> Représente les capacités et la capacité de gestion d’une zone partitionnée d’un disque physique sur un système informatique exécutant Windows.<br/>              |
| [**\_Diskquota Win32**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Classe d’association<br/> Effectue le suivi de l’utilisation de l’espace disque pour les volumes de système de fichiers NTFS.<br/>                                                                                        |
| [**\_Disque logique Win32**](win32-logicaldisk.md)                                     | Représente une source de données qui correspond à un périphérique de stockage local réel sur un système informatique exécutant Windows.<br/>                                                            |
| [**\_LogicalDiskRootDirectory Win32**](win32-logicaldiskrootdirectory.md)           | Classe d’association<br/> Établit une relation entre un disque logique et sa structure de répertoire.<br/>                                                                                          |
| [**\_LogicalDiskToPartition Win32**](win32-logicaldisktopartition.md)               | Classe d’association<br/> Met en relation un lecteur de disque logique et la partition de disque sur laquelle il se trouve.<br/>                                                                           |
| [**\_MappedLogicalDisk Win32**](win32-mappedlogicaldisk.md)                         | Représente les périphériques de stockage réseau mappés en tant que disques logiques sur le système d’ordinateur exécutant Windows.<br/>                                                               |
| [**\_OperatingSystemAutochkSetting Win32**](/previous-versions//aa394240(v=vs.85)) | Classe d’association<br/> Représente l’association entre une instance de l' [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) et les paramètres définis pour celle-ci.<br/> |
| [**\_QuotaSetting Win32**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Classe d’instance<br/> Contient des informations de paramètres pour les quotas de disque sur un volume.<br/>                                                                                       |
| [**\_ShortcutFile Win32**](win32-shortcutfile.md)                                   | Classe d’instance<br/> Représente des fichiers qui sont des raccourcis vers d’autres fichiers, répertoires et commandes.<br/>                                                                  |
| [**\_Sous-répertoire Win32**](win32-subdirectory.md)                                   | Classe d’association<br/> Met en relation un répertoire (dossier) et l’un de ses sous-répertoires (sous-dossiers).<br/>                                                                     |
| [**\_SystemPartitions Win32**](win32-systempartitions.md)                           | Classe d’association<br/> Établit une relation entre un système informatique et une partition de disque sur ce système.<br/>                                                                               |
| [**\_Volume Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Classe d’instance<br/> Représente une zone de stockage sur un disque dur.<br/>                                                                                                   |
| [**\_VolumeQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Classe d’association<br/> Met en relation un volume avec les paramètres de quota par volume.<br/>                                                                                           |
| [**\_VolumeQuotaSetting Win32**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Classe d’association<br/> Met en relation les paramètres de quota de disque avec un volume de disque spécifique.<br/>                                                                                     |
| [**\_VolumeUserQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Classe d’association<br/> Met en relation les quotas par utilisateur et les volumes prenant en charge les quotas.<br/>                                                                                            |



 

## <a name="job-objects"></a>Objets de traitement

La sous-catégorie objets de tâche regroupe des classes qui représentent des classes qui permettent d’instrumenter des objets de traitement nommés. Un objet de traitement sans nom ne peut pas être instrumenté.



| Classe                                                                               | Description                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CollectionStatistics Win32**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Classe d’association<br/> Met en relation une collection d’éléments système managés et la classe qui représente des informations statistiques sur la collection.<br/>                               |
| [**\_LUID Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Classe d’instance<br/> Représente un identificateur unique local (LUID)<br/>                                                                                                         |
| [**\_LUIDandAttributes Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Classe d’instance<br/> Représente un LUID et ses attributs.<br/>                                                                                                                 |
| [**\_NamedJobObject Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Classe d’instance<br/> Représente un objet de noyau utilisé pour regrouper des processus dans le but de contrôler la vie et les ressources des processus dans l’objet de traitement.<br/> |
| [**\_NamedJobObjectActgInfo Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Classe d’instance<br/> Représente les informations de gestion des e/s d’un objet de traitement.<br/>                                                                                           |
| [**\_NamedJobObjectLimit Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Classe d’instance<br/> Représente une association entre un objet de traitement et les paramètres de limite de l’objet de traitement.<br/>                                                                     |
| [**\_NamedJobObjectLimitSetting Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Classe d’instance<br/> Représente les paramètres de limite pour un objet de traitement.<br/>                                                                                                       |
| [**\_NamedJobObjectProcess Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Classe d’instance<br/> Met en relation un objet de traitement et le processus contenu dans l’objet de traitement.<br/>                                                                                     |
| [**\_NamedJobObjectSecLimit Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Classe d’instance<br/> Met en relation un objet de traitement et les paramètres de limite de sécurité de l’objet de traitement.<br/>                                                                                      |
| [**\_NamedJobObjectSecLimitSetting Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Classe d’instance<br/> Représente les paramètres de limite de sécurité pour un objet de traitement.<br/>                                                                                              |
| [**\_NamedJobObjectStatistics Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Classe d’instance<br/> Représente une association entre un objet de traitement et la classe d’informations de gestion des e/s des objets de traitement.<br/>                                                   |
| [**\_SIDandAttributes Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Classe d’instance<br/> Représente un identificateur de sécurité (SID) et ses attributs.<br/>                                                                                            |
| [**\_TokenGroups Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | Classe d'événements<br/> Représente des informations sur les SID de groupe dans un jeton d’accès.<br/>                                                                                          |
| [**\_TokenPrivileges Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | Classe d'événements<br/> Représente des informations sur un jeu de privilèges pour un jeton d’accès.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>Mémoire et fichiers d’échange

Les classes de sous-catégorie fichiers de mémoire et de page représentent les classes qui représentent les paramètres de configuration du fichier d’échange.



| Classe                                                                 | Description                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Fichier d’échange Win32**](win32-pagefile.md)                             | Classe d’instance<br/> Représente le fichier utilisé pour gérer l’échange de fichiers de mémoire virtuelle sur un système Windows.<br/>                  |
| [**\_PageFileElementSetting Win32**](win32-pagefileelementsetting.md) | Classe d’association<br/> Met en relation les paramètres initiaux d’un fichier d’échange et l’état de ces paramètres lors d’une utilisation normale.<br/>        |
| [**\_PageFileSetting Win32**](win32-pagefilesetting.md)               | Classe d’instance<br/> Représente les paramètres d’un fichier d’échange.<br/>                                                                  |
| [**\_PageFileUsage Win32**](win32-pagefileusage.md)                   | Classe d’instance<br/> Représente le fichier utilisé pour gérer l’échange de fichiers de mémoire virtuelle sur un système informatique exécutant Windows.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Audio ou visuel multimédia

La classe de la sous-catégorie audio ou visuelle multimédia représente les propriétés du codec audio ou vidéo installé sur le système informatique.



| Classe                                       | Description                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**\_CodecFile Win32**](win32-codecfile.md) | Classe d’instance<br/> Représente le codec audio ou vidéo installé sur le système informatique.<br/> |



 

## <a name="networking"></a>Mise en réseau

La sous-catégorie mise en réseau regroupe les classes qui représentent les connexions réseau, les clients réseau et les paramètres de connexion réseau, tels que le protocole utilisé.



| Classe                                                                            | Description                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_ActiveRoute Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Classe d’association<br/> Met en relation l’itinéraire adresse IP4 actuel avec la table d’itinéraires IP rendue persistante.<br/>                           |
| [**\_IP4PersistedRouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Classe d’instance<br/> Représente des itinéraires IP persistants.<br/>                                                             |
| [**\_IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Classe d’instance<br/> Représente des informations qui gouvernent le routage de paquets de données réseau.<br/>                    |
| [**\_IP4RouteTableEvent Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | Classe d'événements<br/> Représente les événements de changement d’itinéraire IP.<br/>                                                             |
| [**\_Networkclient Win32**](win32-networkclient.md)                              | Classe d’instance<br/> Représente un client réseau sur un système d’ordinateur exécutant Windows.<br/>                           |
| [**\_NetworkConnection Win32**](win32-networkconnection.md)                      | Classe d’instance<br/> Représente une connexion réseau active dans un environnement Windows.<br/>                           |
| [**\_NetworkProtocol Win32**](win32-networkprotocol.md)                          | Classe d’instance<br/> Représente un protocole et ses caractéristiques réseau sur un système informatique exécutant Windows.<br/> |
| [**\_NTDomain Win32**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Classe d’instance<br/> Représente un domaine Windows NT.<br/>                                                             |
| [**\_PingStatus Win32**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Classe d’instance<br/> Représente les valeurs retournées par la commande **ping** standard.<br/>                            |
| [**\_ProtocolBinding Win32**](win32-protocolbinding.md)                          | Classe d’association<br/> Établit une relation entre un pilote au niveau du système, un protocole réseau et une carte réseau.<br/>                    |



 

## <a name="operating-system-events"></a>Événements du système d'exploitation

La sous-catégorie événements du système d’exploitation regroupe des classes qui représentent les événements du système d’exploitation liés aux processus, aux threads et à l’arrêt du système.



| Classe                                                                                 | Description                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ComputerShutdownEvent Win32**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | Classe d'événements<br/> Représente les événements d’arrêt de l’ordinateur.<br/>                                                                                                   |
| [**\_ComputerSystemEvent Win32**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | Classe d'événements<br/> Représente les événements liés à un système informatique.<br/>                                                                                        |
| [**\_DeviceChangeEvent Win32**](win32-devicechangeevent.md)                           | Classe d'événements<br/> Représente les événements de changement d’appareil résultant de l’ajout, de la suppression ou de la modification d’appareils sur le système informatique.<br/>               |
| [**\_ModuleLoadTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | Classe d'événements<br/> Indique qu’un processus a chargé un nouveau module.<br/>                                                                                      |
| [**\_ModuleTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | Classe d'événements<br/> Événement de base pour les événements de module.<br/>                                                                                                          |
| [**\_ProcessStartTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | Classe d'événements<br/> Indique qu’un nouveau processus a démarré.<br/>                                                                                              |
| [**\_ProcessStopTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | Classe d'événements<br/> Indique qu’un processus s’est terminé.<br/>                                                                                               |
| [**\_ProcessTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | Classe d'événements<br/> Événement de base pour les événements de processus.<br/>                                                                                                         |
| [**\_SystemConfigurationChangeEvent Win32**](win32-systemconfigurationchangeevent.md) | Classe d'événements<br/> Indique que la liste des appareils sur le système a été actualisée (un appareil a été ajouté ou supprimé ou la configuration a été modifiée).<br/>    |
| [**\_SystemTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | Classe d'événements<br/> Classe de base pour tous les événements de trace système, y compris les suivis de module, de processus et de thread.<br/>                                                  |
| [**\_ThreadStartTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | Classe d'événements<br/> Indique qu’un nouveau thread a démarré.<br/>                                                                                                    |
| [**\_ThreadStopTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | Classe d'événements<br/> Indique qu’un thread s’est arrêté.<br/>                                                                                                   |
| [**\_ThreadTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | Classe d'événements<br/> Classe d’événements de base pour les événements de thread.<br/>                                                                                                    |
| [**\_VolumeChangeEvent Win32**](win32-volumechangeevent.md)                           | Classe d'événements<br/> Représente un événement de lecteur mappé au réseau résultant de l’ajout d’une lettre de lecteur réseau ou d’un lecteur monté sur le système informatique.<br/> |



 

## <a name="operating-system-settings"></a>Paramètres du système d'exploitation

La sous-catégorie paramètres du système d’exploitation regroupe des classes qui représentent le système d’exploitation et ses paramètres.



| Classe                                                                                       | Description                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BootConfiguration Win32**](win32-bootconfiguration.md)                                 | Classe d’instance<br/> Représente la configuration de démarrage d’un système informatique exécutant Windows.<br/>                                                                       |
| [**\_ComputerSystem Win32**](win32-computersystem.md)                                       | Classe d’instance<br/> Représente un système informatique fonctionnant dans un environnement Windows.<br/>                                                                              |
| [**\_ComputerSystemProcessor Win32**](win32-computersystemprocessor.md)                     | Classe d’association<br/> Établit une relation entre un système informatique et un processeur s’exécutant sur ce système.<br/>                                                                          |
| [**\_ComputerSystemProduct Win32**](win32-computersystemproduct.md)                         | Classe d’instance<br/> Représente un produit.<br/>                                                                                                                         |
| [**\_DependentService Win32**](win32-dependentservice.md)                                   | Classe d’association<br/> Met en relation deux services de base interdépendants.<br/>                                                                                                  |
| [**\_LoadOrderGroup Win32**](win32-loadordergroup.md)                                       | Classe d’instance<br/> Représente un groupe de services système qui définissent des dépendances d’exécution.<br/>                                                                     |
| [**\_LoadOrderGroupServiceDependencies Win32**](win32-loadordergroupservicedependencies.md) | Classe d’instance<br/> Représente une association entre un service de base et un groupe d’ordre de chargement dont dépend le service pour commencer à s’exécuter.<br/>                         |
| [**\_LoadOrderGroupServiceMembers Win32**](win32-loadordergroupservicemembers.md)           | Classe d’association<br/> Établit un lien entre un groupe d’ordre de chargement et un service de base.<br/>                                                                                             |
| [**\_OperatingSystem Win32**](win32-operatingsystem.md)                                     | Classe d’instance<br/> Représente un système d’exploitation installé sur un système informatique exécutant Windows.<br/>                                                                |
| [**\_OperatingSystemQFE Win32**](win32-operatingsystemqfe.md)                               | Classe d’association<br/> Met en relation le système d’exploitation et les mises à jour du produit appliquées comme représenté dans [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).<br/> |
| [**\_OSRecoveryConfiguration Win32**](win32-osrecoveryconfiguration.md)                     | Classe d’instance<br/> Représente les types d’informations qui seront collectées à partir de la mémoire en cas d’échec du système d’exploitation.<br/>                                        |
| [**\_QuickFixEngineering Win32**](win32-quickfixengineering.md)                             | Classe d’instance<br/> Représente le correctif logiciel (QFE) ou les mises à jour qui ont été appliqués au système d’exploitation actuel à l’aide du système.<br/>                         |
| [**\_StartupCommand Win32**](win32-startupcommand.md)                                       | Classe d’instance<br/> Représente une commande qui s’exécute automatiquement lorsqu’un utilisateur se connecte au système de l’ordinateur.<br/>                                                       |
| [**\_SystemBootConfiguration Win32**](win32-systembootconfiguration.md)                     | Classe d’association<br/> Établit une relation entre un système informatique et sa configuration de démarrage.<br/>                                                                                      |
| [**\_SystemDesktop Win32**](win32-systemdesktop.md)                                         | Classe d’association<br/> Établit une relation entre un système informatique et sa configuration de bureau.<br/>                                                                                   |
| [**\_SystemDevices Win32**](win32-systemdevices.md)                                         | Classe d’association<br/> Établit une relation entre un système informatique et un périphérique logique installé sur ce système.<br/>                                                                   |
| [**\_SystemLoadOrderGroups Win32**](win32-systemloadordergroups.md)                         | Classe d’association<br/> Établit une relation entre un système informatique et un groupe d’ordre de chargement.<br/>                                                                                          |
| [**\_SystemNetworkConnections Win32**](win32-systemnetworkconnections.md)                   | Classe d’association<br/> Établit une relation entre une connexion réseau et le système informatique sur lequel elle réside.<br/>                                                                  |
| [**\_SystemOperatingSystem Win32**](win32-systemoperatingsystem.md)                         | Classe d’association<br/> Établit une relation entre un système informatique et son système d’exploitation.<br/>                                                                                        |
| [**\_SystemProcesses Win32**](win32-systemprocesses.md)                                     | Classe d’association <br/> Établit une relation entre un système informatique et un processus s’exécutant sur ce système.<br/>                                                                           |
| [**\_SystemProgramGroups Win32**](win32-systemprogramgroups.md)                             | Classe d’association<br/> Établit une relation entre un système informatique et un groupe de programmes logique.<br/>                                                                                     |
| [**\_SystemResources Win32**](win32-systemresources.md)                                     | Classe d’association<br/> Établit une relation entre une ressource système et le système informatique sur lequel elle réside.<br/>                                                                           |
| [**\_SystemServices Win32**](win32-systemservices.md)                                       | Classe d’association<br/> Établit une relation entre un système informatique et un programme de service qui existe sur le système.<br/>                                                                 |
| [**\_SystemSetting Win32**](win32-systemsetting.md)                                         | Classe d’association<br/> Établit une relation entre un système informatique et un paramètre général sur ce système.<br/>                                                                            |
| [**\_SystemSystemDriver Win32**](win32-systemsystemdriver.md)                               | Classe d’association<br/> Établit une relation entre un système informatique et un pilote système s’exécutant sur ce système informatique.<br/>                                                             |
| [**\_SystemTimeZone Win32**](win32-systemtimezone.md)                                       | Classe d’association<br/> Établit une relation entre un système informatique et un fuseau horaire.<br/>                                                                                                 |
| [**\_SystemUsers Win32**](win32-systemusers.md)                                             | Classe d’association<br/> Établit une relation entre un système informatique et un compte d’utilisateur sur ce système.<br/>                                                                               |



 

## <a name="processes"></a>Processus

La sous-catégorie processus regroupe les classes qui représentent les processus système et les threads.



| Classe                                                 | Description                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_Processus Win32**](win32-process.md)               | Classe d’instance<br/> Représente une séquence d’événements sur un système informatique exécutant Windows.<br/>      |
| [**\_ProcessStartup Win32**](win32-processstartup.md) | Classe d’instance<br/> Représente la configuration de démarrage d’un système informatique exécutant Windows.<br/> |
| [**\_Thread Win32**](win32-thread.md)                 | Classe d’instance<br/> Représente un thread d’exécution.<br/>                                          |



 

## <a name="registry"></a>Registre

La classe de la sous-catégorie Registre représente le contenu du Registre Windows.



| Classe                                     | Description                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**\_Registre Win32**](win32-registry.md) | Classe d’instance<br/> Représente le registre système sur un système informatique exécutant Windows.<br/> |



 

## <a name="scheduler-jobs"></a>Tâches du planificateur

Les classes de sous-catégorie travaux du planificateur qui représentent les paramètres de tâche planifiée.



| Classe                                                | Description                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CurrentTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Classe abstraite<br/> Représente une instance dans le temps en tant que secondes du composant, minutes, jour de la semaine, et ainsi de suite.<br/>                                                                                                                                        |
| [**\_ScheduledJob Win32**](win32-scheduledjob.md)    | Classe d’instance<br/> Représente un travail planifié à l’aide du service de planification Windows.<br/>                                                                                                                                                                   |
| [**\_Localtime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Classe d’instance<br/> Représente un point dans le temps retourné en tant qu’objets [**\_ localtime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) qui résultent d’une requête. La propriété **Hour** est retournée comme heure locale au format 24 heures.<br/>                                |
| [**\_UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Classe d’instance<br/> Représente un point dans le temps qui est retourné en tant qu’objets [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) qui résultent d’une requête. La propriété **Hour** est retournée en temps UTC (Coordinated Universal Time) dans une horloge de 24 heures.<br/> |



 

## <a name="security"></a>Sécurité

La sous-catégorie de sécurité regroupe les classes qui représentent les paramètres de sécurité du système.



| Classe                                                                               | Description                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AccountSID Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Classe d’association<br/> Établit une relation entre une instance de compte de sécurité et une instance de descripteur de sécurité.<br/>                                             |
| [**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Classe d’instance<br/> Représente une entrée du contrôle d'accès.<br/>                                                                               |
| [**\_LogicalFileAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Classe d’association<br/> Met en relation les paramètres de sécurité d’un fichier ou d’un répertoire et un membre de sa liste de contrôle d’accès discrétionnaire (DACL).<br/> |
| [**\_LogicalFileAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Classe d’association<br/> Lie les paramètres de sécurité d’un fichier ou d’un répertoire à un membre de sa liste de contrôle d’accès système (SACL).<br/>            |
| [**\_LogicalFileGroup Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Classe d’association<br/> Met en relation les paramètres de sécurité d’un fichier ou d’un répertoire et de son groupe.<br/>                                                  |
| [**\_LogicalFileOwner Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Classe d’association<br/> Met en relation les paramètres de sécurité d’un fichier ou d’un répertoire et son propriétaire.<br/>                                                  |
| [**\_LogicalFileSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Classe d’instance<br/> Représente les paramètres de sécurité d’un fichier logique.<br/>                                                                        |
| [**\_LogicalShareAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Classe d’association<br/> Met en relation les paramètres de sécurité d’un partage et un membre de sa liste DACL.<br/>                                                 |
| [**\_LogicalShareAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Classe d’association<br/> Met en relation les paramètres de sécurité d’un partage et un membre de sa liste SACL.<br/>                                                 |
| [**\_LogicalShareSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Classe d’instance<br/> Représente les paramètres de sécurité d’un fichier logique.<br/>                                                                        |
| [**\_PrivilegesStatus Win32**](win32-privilegesstatus.md)                           | Classe d’instance<br/> Représente des informations sur les privilèges requis pour terminer une opération.<br/>                                          |
| [**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Classe d’instance<br/> Représente une représentation structurelle d’un [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor).<br/>                   |
| [**\_SecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Classe d’instance<br/> Représente les paramètres de sécurité d’un élément managé.<br/>                                                                     |
| [**\_SecuritySettingAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Classe d’instance<br/> Représente les droits accordés et refusés à un tiers de confiance pour un objet donné.<br/>                                               |
| [**\_SecuritySettingAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Classe d’instance<br/> Représente l’audit pour un tiers de confiance donné sur un objet donné.<br/>                                                          |
| [**\_SecuritySettingGroup Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Classe d’association<br/> Lie la sécurité d’un objet et de son groupe.<br/>                                                                     |
| [**\_SecuritySettingOfLogicalFile Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Classe d’instance<br/> Représente les paramètres de sécurité d’un objet de fichier ou de répertoire.<br/>                                                             |
| [**\_SecuritySettingOfLogicalShare Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Classe d’instance<br/> Représente les paramètres de sécurité d’un objet partagé.<br/>                                                                        |
| [**\_SecuritySettingOfObject Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Classe d’association<br/> Établit un lien entre un objet et ses paramètres de sécurité.<br/>                                                                          |
| [**\_SecuritySettingOwner Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Classe d’association<br/> Met en relation les paramètres de sécurité d’un objet et de son propriétaire.<br/>                                                            |
| [**\_Sid Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Classe d’instance<br/> Représente un SID arbitraire.<br/>                                                                                            |
| [**\_Confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Classe d’instance<br/> Représente un tiers de confiance.<br/>                                                                                                   |



 

## <a name="services"></a>Services

La sous-catégorie services regroupe les classes qui représentent les services et les services de base.



| Classe                                           | Description                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BaseService Win32**](win32-baseservice.md) | Classe d’instance<br/> Représente les objets exécutables qui sont installés dans une base de données de Registre gérée par le gestionnaire de contrôle des services.<br/> |
| [**\_Service Win32**](win32-service.md)         | Classe d’instance<br/> Représente un service sur un système informatique exécutant Windows.<br/>                                                         |



 

## <a name="shares"></a>Partages

Le partage les classes de sous-catégorie qui représentent les détails des ressources partagées, telles que les imprimantes et les dossiers.



| Classe                                                       | Description                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DFSNode Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Classe d’association<br/> Représente un nœud racine ou un nœud de jonction d’un système de fichiers DFS (Distributed File System) autonome ou basé sur un domaine.<br/>                                                           |
| [**\_DFSNodeTarget Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Classe d’association<br/> Représente la relation entre un nœud DFS et l’une de ses cibles.<br/>                                                                                             |
| [**\_DFSTarget Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Classe d’association<br/> Représente la cible d’un nœud DFS.<br/>                                                                                                                         |
| [**\_ServerConnection Win32**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Classe d’instance<br/> Représente les connexions établies à partir d’un ordinateur distant à une ressource partagée sur l’ordinateur local.<br/>                                                              |
| [**\_ServerSession Win32**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Classe d’instance<br/> Représente les sessions établies avec l’ordinateur local par les utilisateurs sur un ordinateur distant.<br/>                                                             |
| [**\_ConnectionShare Win32**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Classe d’association<br/> Établit une relation entre une ressource partagée sur l’ordinateur et la connexion établie avec la ressource partagée.<br/>                                                                    |
| [**\_PrinterShare Win32**](win32-printershare.md)           | Classe d’association<br/> Établit une relation entre une imprimante locale et le partage qui la représente lorsqu’elle est affichée sur un réseau.<br/>                                                                     |
| [**\_SessionConnection Win32**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Classe d’association<br/> Représente une association entre une session établie avec le serveur local par un utilisateur sur un ordinateur distant et les connexions qui dépendent de la session.<br/> |
| [**\_SessionProcess Win32**](win32-sessionprocess.md)       | Classe d’association<br/> Représente une association entre une ouverture de session et les processus associés à cette session.<br/>                                                            |
| [**\_ShareToDirectory Win32**](win32-sharetodirectory.md)   | Classe d’association<br/> Établit une relation entre une ressource partagée sur le système de l’ordinateur et le répertoire auquel elle est mappée.<br/>                                                                    |
| [**\_Partage Win32**](win32-share.md)                         | Classe d’instance<br/> Représente une ressource partagée sur un système d’ordinateur exécutant Windows.<br/>                                                                                              |



 

## <a name="start-menu"></a>Menu Démarrer

La sous-catégorie menu Démarrer regroupe des classes qui représentent des groupes de programmes.



| Classe                                                                                   | Description                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_LogicalProgramGroup Win32**](win32-logicalprogramgroup.md)                         | Classe d’instance<br/> Représente un groupe de programmes sur un système informatique exécutant Windows.<br/>                                                                    |
| [**\_LogicalProgramGroupDirectory Win32**](win32-logicalprogramgroupdirectory.md)       | Classe d’association<br/> Met en relation les groupes de programmes logiques (regroupements dans le menu Démarrer) et les répertoires de fichiers dans lesquels ils sont stockés.<br/>                 |
| [**\_LogicalProgramGroupItem Win32**](win32-logicalprogramgroupitem.md)                 | Classe d’instance<br/> Représente un élément contenu dans une instance de **\_ ProgramGroup Win32** , qui n’est pas elle-même une autre instance **\_ ProgramGroup Win32** .<br/> |
| [**\_LogicalProgramGroupItemDataFile Win32**](win32-logicalprogramgroupitemdatafile.md) | Classe d’association<br/> Met en relation les éléments de groupe de programmes du menu Démarrer et les fichiers dans lesquels ils sont stockés.<br/>                                       |
| [**\_ProgramGroupContents Win32**](win32-programgroupcontents.md)                       | Classe d’association<br/> Établit une relation entre une commande de groupe de programmes et un groupe de programmes ou un élément individuel qu’elle contient.<br/>                                           |
| [**\_ProgramGroupOrItem Win32**](win32-programgrouporitem.md)                           | Classe d’instance<br/> Représente un regroupement logique de programmes dans le menu démarrer les  \| **programmes** de l’utilisateur.<br/>                                               |



 

## <a name="storage"></a>Stockage

La sous-catégorie utilisateurs regroupe les classes qui représentent des informations de stockage.



| Classe                                                                   | Description                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ShadowBy Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Classe d’association<br/> Représente l’association entre un cliché instantané et le fournisseur qui crée le cliché instantané.<br/>      |
| [**\_ShadowContext Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Classe d’association<br/> Spécifie la manière dont un cliché instantané doit être créé, interrogé ou supprimé.<br/>                                   |
| [**\_Shadowcopy Win32**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Classe d’instance<br/> Représente une copie dupliquée du volume d’origine à un moment antérieur.<br/>                                  |
| [**\_ShadowDiffVolumeSupport Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Classe d’association<br/> Représente une association entre un fournisseur de clichés instantanés et un volume de stockage.<br/>                       |
| [**\_ShadowFor Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Classe d’association<br/> Représente une association entre un cliché instantané et le volume pour lequel le cliché instantané est créé.<br/> |
| [**\_ShadowOn Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Classe d’association<br/> Représente une association entre un cliché instantané et l’emplacement où les données différentielles sont écrites.<br/>          |
| [**\_ShadowProvider Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Classe d’association<br/> Représente un composant qui crée et représente des clichés instantanés de volume.<br/>                             |
| [**\_ShadowStorage Win32**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Classe d’association<br/> Représente une association entre un cliché instantané et l’emplacement où les données différentielles sont écrites.<br/>          |
| [**\_ShadowVolumeSupport Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Classe d’association<br/> Représente une association entre un fournisseur de clichés instantanés avec un volume pris en charge.<br/>                    |
| [**\_Volume Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Classe d’instance<br/> Représente une zone de stockage sur un disque dur.<br/>                                                           |
| [**\_VolumeUserQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Classe d’association<br/> Représente un volume pour les paramètres de quota par volume.<br/>                                                |



 

## <a name="users"></a>Utilisateurs

La sous-catégorie utilisateurs regroupe les classes qui représentent des informations sur le compte d’utilisateur, telles que les détails de l’appartenance au groupe.



| Classe                                                                 | Description                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Compte Win32**](win32-account.md)                               | Classe d’instance<br/> Représente des informations sur les comptes d’utilisateur et les comptes de groupe connus du système informatique exécutant Windows.<br/> |
| [**\_Groupe Win32**](win32-group.md)                                   | Classe d’instance<br/> Représente des données relatives à un compte de groupe.<br/>                                                                      |
| [**\_GroupInDomain Win32**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Classe d’association<br/> Identifie les comptes de groupe associés à un domaine Windows NT.<br/>                                       |
| [**\_GroupUser Win32**](win32-groupuser.md)                           | Classe d’association<br/> Met en relation un groupe et un compte qui est membre de ce groupe.<br/>                                           |
| [**\_LogonSession Win32**](win32-logonsession.md)                     | Classe d’instance<br/> Décrit la session de connexion ou les sessions associées à un utilisateur connecté à Windows.<br/>                        |
| [**\_LogonSessionMappedDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Classe d’instance<br/> Représente les disques logiques mappés associés à la session.<br/>                                            |
| [**\_NetworkLoginProfile Win32**](win32-networkloginprofile.md)       | Classe d’instance<br/> Représente les informations de connexion réseau d’un utilisateur spécifique sur un système informatique exécutant Windows.<br/>           |
| [**\_SystemAccount Win32**](win32-systemaccount.md)                   | Classe d’instance<br/> Représente un compte système.<br/>                                                                                |
| [**\_UserAccount Win32**](win32-useraccount.md)                       | Classe d’instance<br/> Représente des informations sur un compte d’utilisateur sur un système informatique exécutant Windows.<br/>                           |
| [**\_UserInDomain Win32**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Classe d’association<br/> Met en relation un compte d’utilisateur et un domaine Windows NT.<br/>                                                          |



 

## <a name="windows-event-log"></a>Journal des événements Windows

La sous-catégorie du journal des événements Windows regroupe des classes qui représentent des événements, des entrées du journal des événements, des paramètres de configuration du journal des événements, etc.



| Classe                                                         | Description                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NTEventlogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Classe d’instance<br/> Représente les données stockées dans un fichier journal des événements Windows.<br/>                                                                                      |
| [**\_NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Classe d’instance<br/> Représente les événements Windows.<br/>                                                                                                               |
| [**\_NTLogEventComputer Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Classe d’association<br/> Met en relation les instances de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) et [**Win32 \_ ComputerSystem**](win32-computersystem.md).<br/>         |
| [**\_NTLogEventLog Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Classe d’association<br/> Met en relation les instances des classes [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) et [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .<br/> |
| [**\_NTLogEventUser Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Classe d’association<br/> Met en relation les instances de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) et [**Win32 \_ UserAccount**](win32-useraccount.md).<br/>               |



 

## <a name="windows-product-activation"></a>Activation de produit Windows

L’activation de produit Windows (WPA) est une technologie anti-piratage qui réduit la copie occasionnelle des logiciels.



| Classe                                                                                                               | Description                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ComputerSystemWindowsProductActivationSetting Win32**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Classe d’association<br/> Met en relation les instances de [**Win32 \_ ComputerSystem**](win32-computersystem.md) et [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)).<br/> |
| [**\_Proxy Win32**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Classe d’instance<br/> Contient des propriétés et des méthodes pour interroger et configurer une connexion Internet relative à WPA.<br/>                                                                |
| [**\_WindowsProductActivation Win32**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Classe d’instance<br/> Contient des propriétés et des méthodes associées à WPA.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

