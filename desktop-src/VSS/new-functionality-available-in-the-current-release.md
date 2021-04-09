---
description: 'La version 2003 de Windows Server du Service VSS contient les nouvelles fonctionnalités suivantes :'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Nouvelles fonctionnalités disponibles dans Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5782ef6b24f208f69e50cdb992e12ba3212c47f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115159"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Nouvelles fonctionnalités disponibles dans Windows Server 2003

La version 2003 de Windows Server du Service VSS contient les nouvelles fonctionnalités suivantes :

-   Prise en charge de la sélectivité pour la [*restauration*](vssgloss-s.md) en plus et sur une base égale avec la [*sélectivité pour la sauvegarde*](vssgloss-s.md) (précédemment appelée « sélectivité »). Pour plus d’informations, consultez Utilisation de la [sélectivité et des chemins d’accès logiques](working-with-selectability-and-logical-paths.md) .
-   Introduction d’un événement [*BackupShutdown*](vssgloss-b.md) indiquant qu’une application de sauvegarde compatible VSS (demandeur) s’est arrêtée, que la tentative de sauvegarde soit terminée correctement ou non. Pour plus d’informations, consultez [gestion des événements BackupShutdown](handling-backupshutdown-events.md) .
-   Prise en charge des dépendances de composants Writer explicites. Un moyen de décrire et de prendre en charge les situations où un composant (et le jeu de composants qu’il définit) géré par un enregistreur ne peut pas être sauvegardé ou restauré indépendamment des composants gérés par d’autres enregistreurs. Pour plus d’informations, consultez [dépendances entre les composants gérés par différents enregistreurs](dependencies-between-components-managed-by-different-writers.md) .
-   Prise en charge complète des opérations de [*fichiers partiels*](vssgloss-p.md) . La sauvegarde et la restauration de segments de fichiers par les rédacteurs et les demandeurs sont désormais entièrement prises en charge. Pour plus d’informations sur les opérations de fichiers partielles, consultez [utilisation de fichiers partiels](working-with-partial-files.md) .
-   Introduction des [*fichiers différenciés*](vssgloss-d.md) pour prendre en charge les opérations de sauvegarde et de restauration incrémentielles. Pour plus d’informations [, consultez sauvegardes incrémentielles et différentielles](incremental-and-differential-backups.md) .
-   Présentation des schémas de sauvegarde en tant que concept qui indique le niveau de prise en charge du writer pour les types d’opérations de sauvegarde. Pour plus d’informations, consultez [**\_ \_ schéma de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) .
-   Prise en charge de la spécification du demandeur des nouvelles destinations de restauration de fichiers ([*nouveaux emplacements cibles*](vssgloss-n.md)) au cours des opérations de restauration. Pour plus d’informations, consultez [utilisation de nouvelles cibles pendant la restauration](working-with-new-targets-during-restore.md) .
-   Prise en charge de la restauration conditionnelle au moment du redémarrage. \_ \_ Pour plus d’informations, voir restauration de RME VSS \_ au \_ redémarrage \_ si \_ ne peut pas \_ remplacer ([**\_ \_ énumération VSE RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)).
-   Définition d’un état de restauration et d’un type de restauration. Pour plus d’informations, consultez [**\_ \_ type de restauration VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) et [État de restauration VSS](vss-restore-state.md) .
-   Prise en charge des requêtes d’écriture sur l’état des clichés instantanés. Pour plus d’informations, consultez [**CVssWriter :: GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) et [**CVssWriter :: GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename) .
-   Prise en charge des clichés instantanés transportables dans Windows Server 2003, Enterprise Edition et Windows Server 2003, Datacenter Edition. Pour plus d’informations, consultez [importation de volumes clichés instantanés transportables](importing-transportable-shadow-copied-volumes.md).

 

 



