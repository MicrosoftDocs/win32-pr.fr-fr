---
description: 'Au cours d’une opération de sauvegarde, le demandeur utilise IVssBackupComponents :: SetBackupState pour définir le type d’opération en cours.'
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: État de sauvegarde VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa9250139aee9f48f9880fd4a657fa7c6c4991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751565"
---
# <a name="vss-backup-state"></a>État de sauvegarde VSS

Au cours d’une opération de sauvegarde, le demandeur utilise [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) pour définir le type d’opération en cours.

Ces informations ne sont pas incluses dans un formulaire de récupération facile dans le document sur les composants de sauvegarde, de sorte que les développeurs de demandeurs doivent stocker ces informations indépendamment sur un support de sauvegarde.

L’état de sauvegarde contient les éléments suivants :

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Type de sauvegarde
</dt> <dd>

Le type de sauvegarde spécifie les critères d’identification des fichiers à sauvegarder. L’évaluation de ces critères doit être effectuée à l’aide de l’API VSS.

Lorsque vous choisissez le type de sauvegarde à poursuivre et les rédacteurs à utiliser, les demandeurs doivent examiner les genres (ou schémas, voir [prise en charge du schéma de sauvegarde](writer-backup-schema-support.md)de l’enregistreur) des opérations de sauvegarde prises en charge par chacun des Writers du système. Les sauvegardes sous VSS peuvent être des types suivants :

-   Full (VSS \_ BT \_ complet) : les fichiers sont sauvegardés quelle que soit leur date de dernière sauvegarde. L’historique de sauvegarde de chaque fichier est mis à jour, et ce type de sauvegarde peut être utilisé comme base d’une sauvegarde incrémentielle ou différentielle. La restauration d’une sauvegarde complète nécessite une seule image de sauvegarde.
-   Copie de sauvegarde (VSS \_ BT \_ Copy) : comme le \_ type de \_ sauvegarde complète VSS BT, les fichiers sont sauvegardés quelle que soit leur date de dernière sauvegarde. Toutefois, l’historique de sauvegarde de chaque fichier n’est pas mis à jour et ce type de sauvegarde ne peut pas être utilisé comme base d’une sauvegarde incrémentielle ou différentielle.
-   Incrémentielle (VSS \_ BT \_ Incremental) : l’API VSS est utilisée pour s’assurer que seuls les fichiers qui ont été modifiés ou ajoutés depuis la dernière sauvegarde complète ou incrémentielle doivent être copiés sur un support de stockage. La restauration d’une sauvegarde incrémentielle nécessite l’image de sauvegarde d’origine et toutes les images de sauvegarde incrémentielles effectuées depuis la sauvegarde initiale.
-   Differential (VSS \_ BT \_ Differential) : l’API VSS est utilisée pour s’assurer que seuls les fichiers qui ont été modifiés ou ajoutés depuis la dernière sauvegarde complète doivent être copiés sur un support de stockage ; toutes les informations de sauvegarde intermédiaires sont ignorées. La restauration d’une sauvegarde différentielle nécessite l’image de sauvegarde d’origine et l’image de sauvegarde différentielle la plus récente effectuée depuis la dernière sauvegarde complète.
-   Fichier journal ( \_ Journal BT VSS \_ ) : seuls les fichiers journaux d’un enregistreur (fichiers ajoutés à un composant avec la méthode [**IVssCreateWriterMetadata :: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) et récupérés par un appel à [**IVssWMComponent :: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) sont sauvegardés. Ce type de sauvegarde est spécifique à VSS.

Les demandeurs peuvent implémenter ces sauvegardes à l’aide d’informations et de méthodes en dehors de VSS. Ce n’est que lorsqu’un demandeur implémente une sauvegarde à l’aide de l’API VSS qu’il a l’un des types de sauvegardes listés. Par exemple, un demandeur participe à un \_ \_ type de sauvegarde de journal BT VSS uniquement s’il a utilisé les informations retournées par [**IVssWMComponent :: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) pour identifier les fichiers journaux. De même, les types différentiels de la copie incrémentielle et VSS de VSS \_ BT \_ \_ \_ s’appliquent uniquement aux opérations incrémentielles ou différentielles, comme décrit dans [sauvegardes incrémentielles et différentielles](incremental-and-differential-backups.md).

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Spécification sur la sélectivité
</dt> <dd>

Une sauvegarde VSS peut choisir de respecter les notions VSS de la sélectivité des composants : cette opération est appelée exécution en [*mode composant*](vssgloss-c.md), ou pour les ignorer.

Un exemple de non-exécution en mode composant consisterait à effectuer une sauvegarde de l’image système, où l’application de sauvegarde aurait besoin de la coopération de l’enregistreur pour garantir la stabilité des données, mais où la sélection des composants serait sans importance.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Enregistrement de l’état de démarrage
</dt> <dd>

VSS prend en charge l’enregistrement de l’état du système en cours d’exécution dans une configuration entièrement démarrable. Toutefois, cela n’est pas toujours nécessaire, et la préparation du writer pour enregistrer un état de démarrage peut parfois dégrader les performances en temps réel d’un système en cours d’exécution.

Par conséquent, les demandeurs indiquent si une sauvegarde doit inclure un État du système de démarrage en tant qu’argument de [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Les enregistreurs déterminent s’ils doivent prendre en charge l’enregistrement de l’état du système de démarrage en appelant [**CVssWriter :: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup).

Même si l’état du système de démarrage n’est pas sélectionné, les clichés instantanés des fichiers système sont créés et les fichiers peuvent être sauvegardés.

Toutefois, il est important de veiller à la restauration des fichiers système si la sauvegarde n’a pas enregistré l’état du système de démarrage (voir [sauvegarde et restauration de l’état du système dans Windows server 2003 R2 et Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)).

Il n’est pas possible de récupérer ces informations à partir d’un document de composants de sauvegarde récupérés, afin que les auteurs de demandeurs doivent stocker si le système a été sauvegardé avec un état système de démarrage.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Prise en charge partielle des fichiers
</dt> <dd>

Certains enregistreurs prennent en charge la restauration de fichiers par le biais du remplacement des parties des fichiers qu’ils gèrent. Un demandeur peut être conçu pour tirer parti de cela et, si tel est le cas, il indique cela en définissant les informations dans [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

 

 



