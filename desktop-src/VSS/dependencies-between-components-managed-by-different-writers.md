---
description: Dans certains cas, les données d’un enregistreur dépendent de données gérées par un autre writer. Dans ce cas, vous devez sauvegarder ou restaurer les données à partir des deux enregistreurs.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Dépendances entre les composants gérés par différents Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d50e88e13899951802b2ec3aa0bd9e651c16928b9f57409329035a28cfa1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122152"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Dépendances entre les composants gérés par différents Writers

Dans certains cas, les données d’un enregistreur dépendent de données gérées par un autre writer. Dans ce cas, vous devez sauvegarder ou restaurer les données à partir des deux enregistreurs.

VSS gère ce problème à l’aide de la notion de dépendance explicite du composant Writer et de l’interface [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) .

Un enregistreur ajoute une ou plusieurs dépendances lors de la création du document de métadonnées de l’enregistreur à l’aide de la méthode [**IVssCreateWriterMetadata :: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) . Le writer passe à la méthode le nom et le chemin d’accès logique du composant dépendant (qu’il gère), ainsi que le nom et le chemin d’accès logique et l' [*ID de classe du writer*](vssgloss-w.md) (GUID identifiant la classe) du composant dont il dépend.

Une fois établie, cette dépendance informe le demandeur qu’au cours d’une opération de sauvegarde ou de restauration, le composant dépendant et les cibles de ses dépendances doivent participer.

Un composant donné peut avoir plusieurs dépendances, ce qui nécessite qu’il et toutes ses cibles dépendantes participent à la sauvegarde et à la restauration.

Le composant dépendant et/ou la ou les cibles de ses dépendances peuvent être inclus [*explicitement*](vssgloss-e.md) ou [*implicitement*](vssgloss-i.md) dans une opération de sauvegarde ou de restauration.

Le mécanisme de dépendance du composant d’écriture explicite ne doit pas être utilisé pour créer une dépendance entre deux composants sur le même Writer. Les règles de sélection peuvent fournir la même fonctionnalité plus efficacement sans risque de dépendances circulaires.

Par exemple, [**IVssCreateWriterMetadata :: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) peut être utilisé pour définir la dépendance du composant writerData (avec le chemin d’accès logique « ») de l’enregistreur MyWriter sur le composant internetData (avec le chemin d’accès logique «Connections ») d’un writer nommé InternetConnector avec un ID de classe de writer X. (même s’il est possible que plusieurs rédacteurs ayant le même ID de classe se trouvent simultanément sur le système, la confusion est évitée car la combinaison du chemin d’accès logique et du nom du composant est unique sur le système sous VSS.)

Un enregistreur ajoute plusieurs dépendances à un composant donné simplement en appelant [**IVssCreateWriterMetadata :: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) répété avec des composants différents de rédacteurs différents. Vous pouvez trouver le nombre d’autres composants dont dépend un composant donné en examinant le membre **cDependencies** de la structure [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) .

Un rédacteur ou un demandeur récupère des instances de l’interface [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) avec [**IVssWMComponent :: GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). **IVssWMDependency** retourne le nom du composant, le chemin d’accès logique et l’ID de classe du writer qui gère le composant qui est la cible de la dépendance.

Le mécanisme de dépendance ne régit pas un ordre de préférence particulier entre le composant dépendant et les cibles de ses dépendances. Comme indiqué ci-dessus, toute dépendance indique qu’à chaque fois qu’un composant donné est sauvegardé ou restauré, le ou les composants dont il dépend doivent être également sauvegardés ou restaurés. L’implémentation exacte de la dépendance est à la discrétion de l’application de sauvegarde.

Par exemple, dans le cas ci-dessus, le composant writerData (chemin logique « ») dépend du composant InternetConnector («connexions » du chemin logique). Un demandeur est libre d’interpréter cela de l’une des manières suivantes :

-   Si le composant dépendant, writerData, est sélectionné (implicitement ou explicitement) pour la sauvegarde ou la restauration, le demandeur doit sélectionner (implicitement ou explicitement) la cible de sa dépendance, internetData
-   Si la cible de sa dépendance, internetData, n’est pas sélectionnée pour la sauvegarde, alors le composant dépendant, writerData, ne doit pas être sélectionné.

Toutefois, lors du développement de la prise en charge des dépendances, les développeurs de demandeurs doivent savoir qu’il n’existe aucun moyen pour un writer de déterminer si l’un de ses composants est la cible d’une dépendance.

## <a name="declaring-remote-dependencies"></a>Déclaration de dépendances distantes

Une application distribuée est une application qui peut être configurée pour utiliser un ou plusieurs ordinateurs à la fois. En règle générale, l’application s’exécute sur un ou plusieurs ordinateurs de serveur d’applications et communique avec (mais peut ne pas s’exécuter sur) un ou plusieurs serveurs de base de données. Cette configuration est parfois appelée déploiement multi-système. Souvent, la même application peut également être configurée pour s’exécuter sur un seul ordinateur exécutant à la fois un serveur d’applications et un serveur de base de données. Une telle configuration est appelée déploiement à système unique. Dans les deux configurations, le serveur d’applications et le serveur de base de données ont chacun leurs propres enregistreurs VSS indépendants.

Dans un déploiement multi-système, si un composant géré par le writer de l’application dépend d’un composant distant géré par l’enregistreur du serveur de base de données, il s’agit d’une dépendance distante. (Un déploiement de système unique, en revanche, n’a que des dépendances locales.)

à titre d’exemple de déploiement multi-système, considérez un serveur d’applications qui utilise un serveur de base de données SQL Server comme un magasin de données. Les données spécifiques à l’application, y compris les composants WebPart, les fichiers de contenu Web et la métabase IIS, résident sur un ou plusieurs ordinateurs, appelés serveurs Web frontaux. le magasin de données SQL réel, qui comprend la base de données de configuration et plusieurs bases de données de contenu, réside sur un ou plusieurs autres ordinateurs, appelés serveurs de bases de données principaux. Chacun des serveurs Web frontaux contient le même contenu et la même configuration spécifiques à l’application. Chacun des serveurs de base de données principaux peut héberger n’importe quelle base de données de contenu ou la base de données de configuration. Le logiciel d’application s’exécute uniquement sur les serveurs Web frontaux, et non sur les serveurs de base de données. dans cette configuration, l’enregistreur VSS de l’application a des dépendances distantes sur les composants gérés par l’enregistreur de SQL.

Un enregistreur peut déclarer une dépendance distante en appelant la méthode [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) , en préen ajoutant « \\ \\ *remotecomputername* \\ », où *remotecomputername* est le nom de l’ordinateur sur lequel se trouve le composant distant, et le chemin logique dans le paramètre *wszOnLogicalPath* . La valeur de *remotecomputername* peut être une adresse IP ou un nom d’ordinateur retourné par la fonction [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

**Windows Server 2003 :** un enregistreur ne peut pas déclarer de dépendances distantes tant que Windows Server 2003 avec Service Pack 1 (SP1).

Pour identifier une dépendance, un demandeur appelle les méthodes [**GetWriterId**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)et [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) de l’interface [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) . Le demandeur doit examiner le nom du composant retourné par **GetComponentName** dans le paramètre *pbstrComponentName* . Si le nom du composant commence par « \\ \\ », le demandeur doit supposer qu’il spécifie une dépendance distante et que le premier composant suivant « \\ \\ » est le *remotecomputername* qui a été spécifié lorsque le writer a appelé [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency). Si le nom du composant ne commence pas par « \\ \\ », le demandeur doit supposer qu’il spécifie une dépendance locale.

S’il existe une dépendance distante, le demandeur doit sauvegarder le composant distant lorsqu’il sauvegarde le composant local. Pour sauvegarder le composant distant, le demandeur doit avoir un agent sur l’ordinateur distant et doit lancer la sauvegarde sur l’ordinateur distant.

## <a name="structuring-remote-dependencies"></a>Structuration des dépendances distantes

Il est important de comprendre qu’une dépendance n’est pas un composant dans et de lui-même. Un composant est nécessaire pour contenir la dépendance.

Les exemples suivants illustrent deux façons de structurer un ensemble de dépendances.

``` syntax
Example 1:
    Writer 1
        Component A
            File A
            File B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")

Example 2:
    Writer 2
        Component A
            File A
            File B
        Component B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")
```

Dans l’exemple 1, les dépendances sont détenues par le composant A. Étant donné que seuls les composants peuvent être sélectionnés, et non des fichiers individuels, la structuration des dépendances de composant A nécessiterait que le composant entier, à la fois les fichiers et les dépendances, doive toujours être sauvegardé et restauré ensemble. Ils ne peuvent pas être sauvegardés ou restaurés individuellement.

Dans l’exemple 2, les composants distincts (composants A et B) contiennent chacune des dépendances. Dans ce cas, les deux composants peuvent être sélectionnés indépendamment, et donc sauvegardés et restaurés indépendamment. La structuration des dépendances de cette façon offre à une application distribuée une plus grande flexibilité dans la gestion de ses dépendances distantes.

## <a name="supporting-remote-dependencies"></a>Prise en charge des dépendances distantes

Un demandeur peut fournir une prise en charge complète ou partielle des dépendances distantes.

Pour assurer une prise en charge complète, le demandeur doit effectuer les opérations suivantes au moment de la sauvegarde et de la restauration.

Au moment de la sauvegarde, le demandeur doit démarrer la sauvegarde sur l’ordinateur frontal (local), déterminer les dépendances existantes et mettre en attente les tâches de sauvegarde supplémentaires pour capturer les bases de données principales. Le demandeur doit attendre la fin des tâches de sauvegarde principales sur l’ordinateur distant avant d’appeler les méthodes [**IVssBackupComponents :: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) et [**IVssBackupComponents :: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) . Si le demandeur attend que la sauvegarde des composants principaux soit terminée avant d’appeler **BackupComplete**, cela génère une sauvegarde plus facile à récupérer pour un enregistreur qui implémente des améliorations supplémentaires, telles que le verrouillage de la topologie, par exemple, pendant la sauvegarde. La procédure suivante décrit ce que le demandeur doit faire :

1.  Sur l’ordinateur local, le demandeur appelle les méthodes [**IVssBackupComponents :: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents ::P Repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)et [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .
2.  Une fois le cliché instantané local terminé, mais avant la fin de la sauvegarde, le demandeur met en attente les tâches de sauvegarde supplémentaires en envoyant une demande à son agent sur l’ordinateur distant.
3.  Sur l’ordinateur distant, l’agent du demandeur effectue la séquence de sauvegarde mise en attente en appelant [**InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)et [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).
4.  Lorsque l’agent du demandeur a terminé les travaux mis en file d’attente sur l’ordinateur distant, le demandeur termine la séquence de sauvegarde en appelant [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) et [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Au moment de la restauration, le demandeur doit démarrer la restauration impliquant l’ordinateur frontal (local), sélectionner les composants et leurs dépendances à restaurer, puis envoyer l’événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) en appelant la méthode de **rerestauration IVssBackupComponents ::P** . Le demandeur doit ensuite mettre en file d’attente les travaux de restauration du serveur principal sur l’ordinateur distant et appeler la méthode [**IVssBackupComponents ::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) lorsque les restaurations du serveur principal sont terminées. Cette exigence confère à l’enregistreur frontal un contrôle accru sur l’expérience de restauration et une meilleure expérience utilisateur d’administrateur. Étant donné que les sauvegardes sur chacun des systèmes ne se produisent pas au même point dans le temps, le rédacteur frontal doit effectuer un nettoyage des données principales. Dans l’exemple d’application abordé dans le précédent « déclaration des dépendances distantes », l’enregistreur doit lancer un remappage ou une réindexation de site après la restauration d’une des bases de données principales. Pour ce faire, le rédacteur doit recevoir des événements sur le serveur frontal. La procédure suivante décrit ce que le demandeur doit faire :

1.  Sur l’ordinateur local, le demandeur appelle [**IVssBackupComponents :: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (ou [**IVssBackupComponentsEx :: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) et la [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).
2.  Une fois la phase de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) terminée, mais avant le début de la phase [**postRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , le demandeur met en attente des travaux de restauration supplémentaires en envoyant une demande à son agent sur l’ordinateur distant.
3.  Sur l’ordinateur distant, l’agent du demandeur effectue les travaux de restauration mis en attente en appelant [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore), [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (ou [**SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) et [**postRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).
4.  Lorsque l’agent du demandeur a terminé les travaux mis en file d’attente sur l’ordinateur distant, le demandeur termine la séquence de restauration en appelant [**IVssBackupComponents :: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) et [**postRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Pour assurer la prise en charge partielle des dépendances distantes, le demandeur doit suivre les dépendances distantes et les inclure dans le cadre de la sauvegarde, mais le classement des événements sur les systèmes frontaux et principaux, comme détaillé dans les deux procédures précédentes, n’est pas nécessaire. Pour un demandeur qui implémente uniquement la prise en charge partielle, le demandeur doit faire référence à la documentation sur la sauvegarde/restauration de l’application de Writer pour comprendre quels scénarios peuvent être pris en charge.

 

 
