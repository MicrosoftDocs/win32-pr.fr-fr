---
description: Après avoir effectué les actions décrites dans vue d’ensemble de l’initialisation de la restauration et vue d’ensemble de la préparation pour la restauration, le demandeur dispose de suffisamment d’informations pour commencer la restauration des fichiers.
ms.assetid: 15df39fa-1eb1-4e96-9e26-14470f391de4
title: Vue d’ensemble de la restauration réelle des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6527a10d0880b1e599377abb797449816019ab89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531888"
---
# <a name="overview-of-actual-file-restoration"></a>Vue d’ensemble de la restauration réelle des fichiers

Après avoir effectué les actions décrites dans [vue d’ensemble de l’initialisation](overview-of-restore-initialization.md) de la restauration et vue d' [ensemble de la préparation pour la restauration](overview-of-preparing-for-restore.md), le demandeur dispose de suffisamment d’informations pour commencer la restauration des fichiers. La restauration des fichiers n’implique pas les interactions de l’enregistreur ou la génération d’événements. Pour plus d’informations, consultez [vue d’ensemble du traitement d’une restauration sous VSS](overview-of-processing-a-restore-under-vss.md).

Le tableau suivant présente la séquence des actions et des événements qui sont nécessaires à la restauration des fichiers.



| Action du demandeur                                                                                                                                                                                                                                                                                                          | Événement | Action d’écriture |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------|
| Générer une liste de jeux de restauration pour les fichiers sur le support de sauvegarde.                                                                                                                                                                                                                                                                 | Aucune  | Aucune          |
| Gérez les [*cibles dirigées*](vssgloss-d.md) ou la restauration de [*fichiers partielle*](vssgloss-p.md) (consultez [**IVssComponent :: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget), [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)). | Aucune  | Aucune          |
| Si nécessaire, ignorez tous les emplacements de restauration spécifiés et restaurez un nouvel emplacement spécifié dans un appel antérieur à [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).                                                                                                                       | Aucune  | Aucune          |
| Si la restauration est incrémentielle et que d’autres restaurations sont nécessaires, indiquez (consultez [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) et [sauvegardes incrémentielles et différentielles](incremental-and-differential-backups.md)).                                                     | Aucune  | Aucune          |
| Pour savoir si un enregistreur a modifié le contenu du document des composants de sauvegarde, appelez [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). Par exemple, l’enregistreur a peut-être modifié la cible de restauration.                                                                 | Aucune  | Aucune          |



 

## <a name="requester-actions-during-restoring-files"></a>Actions du demandeur lors de la restauration des fichiers

Pour la plupart des fichiers sur le support de sauvegarde, le demandeur doit déterminer ses emplacements d’origine et les nouveaux emplacements ou mappages d’emplacements de remplacement qui s’y appliquent. (Pour plus d’informations sur les meilleures pratiques en matière de détermination des fichiers à restaurer et de leur restauration, consultez [génération d’un jeu de restauration](generating-a-restore-set.md) .)

En outre, certains fichiers peuvent avoir des [*cibles dirigées*](vssgloss-d.md) ou prendre en charge la restauration de [*fichiers partielle*](vssgloss-p.md) . Vous pouvez trouver le nombre de ces fichiers en appelant [**IVssComponent :: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) et [**IVssComponent :: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount). pour plus d’informations sur les instructions de restauration détaillées, appelez [**IVssComponent :: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) et [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). (Les fichiers partiels et les fichiers dirigés peuvent faire partie des composants ajoutés implicitement ou explicitement à la sauvegarde d’origine. pour plus d’informations, consultez Utilisation de la [sélectivité pour la restauration et](working-with-selectability-for-restore-and-subcomponents.md) les sous-composants.)

La réussite ou l’échec d’une restauration est indiqué composant par composant à l’aide de [**IVssBackupComponents :: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). La nécessité d’effectuer d’autres opérations de restauration (dans le cas de restaurations incrémentielles ou différentielles) est également indiquée par composant à l’aide de [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

En général, VSS ne spécifie pas de mécanisme pour récupérer des données à partir d’un support de stockage, choisir un support de stockage ou déterminer les fichiers à restaurer.

Toutefois, pour certains Writers, la restauration de fichiers peut impliquer l’utilisation d’une interface et d’une procédure personnalisées documentées. Les enregistreurs système Windows, qui requièrent actuellement une telle prise en charge, sont documentés dans des [cas d’utilisation VSS spéciaux](special-vss-usage-cases.md).

En général, il est recommandé de traiter les fichiers de chaque composant de chaque [*instance du writer*](vssgloss-w.md) comme une unité. Ce tutoriel requiert les éléments suivants :

-   Association de chaque fichier à restaurer avec le composant qui l’a géré. Cela nécessite l’utilisation de documents de métadonnées d’écriture.
-   Obtention des informations correctes sur la cible de restauration. Cela nécessite des informations du document sur les composants de sauvegarde.

 

 



