---
description: Il est parfois souhaitable de créer un cliché instantané sur un système, mais d’utiliser le cliché instantané sur un second système.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importation de volumes de clichés instantanés transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d259fbc047d088ee1f7064804a3ee98fe48da1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115163"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importation de volumes de clichés instantanés transportables

Il est parfois souhaitable de créer un cliché instantané sur un système, mais d’utiliser le cliché instantané sur un second système.

Considérez le cas où les données à sauvegarder sont normalement gérées par un système donné (*systemOne*) au cours d’opérations normales et que ces données sont stockées physiquement sur une baie de stockage ou un appareil.

Pour limiter les interruptions de *systemOne* (car les opérations de sauvegarde peuvent nécessiter de nombreuses ressources), il est préférable d’effectuer la sauvegarde à l’aide de *systemTwo*, un serveur de sauvegarde, qui a accès au même groupe de stockage que *systemOne*.

Pour garantir le bon cliché instantané, en coopérant avec les enregistreurs sur *systemOne* et en préservant l’état de manière appropriée pour les tâches en cours, le cliché instantané doit être exécuté par *systemOne*.

Par conséquent, *systemOne* doit créer un [*cliché instantané transportable*](vssgloss-t.md), que *systemTwo* va importer ensuite.

**Windows server 2003, Standard Edition, Windows server 2003, Web Edition et Windows XP :** Les jeux de clichés instantanés transportables ne sont pas pris en charge. Toutes les éditions de Windows Server 2003 avec Service Pack 1 (SP1) prennent en charge les jeux de clichés instantanés transportables.

Un exemple classique d’importation d’un cliché instantané transportable peut se poursuivre de la façon suivante :

1.  Initialement, l’unité logique (LUN) qui est fournie par le groupe de stockage est montée en tant que volume sur *systemOne* (par exemple, F :).
2.  Un demandeur qui s’exécute sur *systemOne* instancie une instance de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) et se poursuit comme s’il avait préparé une sauvegarde. (Pour plus d’informations, consultez [Présentation de l’initialisation de](overview-of-backup-initialization.md)la sauvegarde, [vue d’ensemble de la phase de découverte de la sauvegarde](overview-of-the-backup-discovery-phase.md)et [vue d’ensemble des tâches de pré-sauvegarde](overview-of-pre-backup-tasks.md) .)
3.  Le demandeur sur *systemOne* modifie le contexte de cliché instantané qui est généralement utilisé pour l’opération de sauvegarde locale (sauvegarde de l'**\_ \_ application \_ CTX VSS**) pour indiquer qu’un cliché instantané transportable sera créé (**VSS \_ VOLSNAP \_ attr \_ transportable**). L’attribut transportable peut également être ajouté à d’autres contextes de clichés instantanés.
4.  Avec un contexte de cliché instantané de la **\_ \_ \_ sauvegarde** VSS de l’application systemOne VSS \| **\_ VOLSNAP \_ attr \_ transportable**, le demandeur qui se trouve sur  crée un cliché instantané en appelant [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).
5.  *SystemOne* utilise [**IVssBackupComponents :: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) pour enregistrer l’état actuel du document des composants de sauvegarde et [**IVssExamineWriterMetadata :: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) pour enregistrer les documents de métadonnées de l’enregistreur du writer. Les chaînes XML qui contiennent ces documents sont ensuite mises à la disposition d’un demandeur qui s’exécute sur *systemTwo*.

    Le demandeur transfère le document des composants de sauvegarde vers *systemTwo*.

    Notez que le demandeur sur *systemOne* ne libère pas son instance de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) à ce stade si l’objectif du cliché instantané est pour la sauvegarde. L’interface doit rester ouverte jusqu’à ce que *systemTwo* termine correctement ses opérations de sauvegarde. Uniquement si le demandeur émet un événement [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , car certains enregistreurs tronquent les journaux et effectuent d’autres tâches après une sauvegarde réussie. Si l’objectif du cliché instantané est l’exploration de données ou à d’autres fins, l’interface peut être fermée à cette étape.

6.  Le demandeur sur *systemTwo* appelle ensuite [**IVssBackupComponents :: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) pour obtenir l’accès au cliché instantané qui a été créé par le demandeur sur *systemOne*.
    > [!Note]  
    > Le demandeur est responsable de la sérialisation de l’opération de cliché instantané de l’importation. En outre, si l’appel à [**IVssBackupComponents :: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) échoue, le service VSS ne nettoie pas les numéros d’unités logiques qui lui sont propres. Le demandeur doit lancer le nettoyage des numéros d’unités logiques.

     

7.  Le demandeur sur *systemTwo* procède à la sauvegarde du matériel des clichés instantanés exactement comme s’il sauvegardait un cliché instantané créé par lui-même (consultez [vue d’ensemble de la sauvegarde réelle des fichiers](overview-of-actual-backup-of-files.md)).

    Le demandeur sur *systemTwo* obtient l' [*objet appareil*](vssgloss-d.md) du cliché instantané à l’aide de [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) sur le cliché instantané importé et l’ajoute au début des chemins d’accès aux fichiers d’origine qui ont été obtenus à partir des métadonnées pour accéder aux fichiers à sauvegarder.

8.  Après avoir utilisé le cliché instantané, le demandeur sur *systemTwo* doit supprimer le cliché instantané. Comme pour les clichés instantanés non transportables, si le contexte de cliché instantané indique des clichés instantanés de mise en sortie automatique (par exemple, la sauvegarde de la copie de **\_ \_ sauvegarde de VSS**), le fait de libérer le [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sur *systemTwo* entraîne la suppression du cliché instantané par le service VSS. Dans le cas contraire, si le contexte indique un cliché instantané persistant (par exemple, la restauration de l' **\_ \_ application \_ CTX VSS**), le demandeur sur *systemTwo* doit supprimer explicitement le cliché instantané.

    Ensuite, le demandeur sur *systemTwo* signale au demandeur sur *systemOne* qu’il a fini de sauvegarder le cliché instantané transportable.

9.  Une fois que le demandeur sur *systemOne* a reçu une notification indiquant que le demandeur sur *systemTwo* a terminé la sauvegarde du cliché instantané transportable, il avertit les enregistreurs de son système en générant un événement [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) avec un appel à **IVssBackupComponents :: BackupComplete**. À ce stade, le demandeur sur *systemOne* est libre de libérer son instance de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

**Clichés instantanés transportables dans un cluster :** Les clichés instantanés transportables doivent être importés à partir de l’extérieur du cluster tant que le volume d’origine est monté au sein du cluster. Pour plus d’informations sur l’implémentation d’une récupération rapide dans un cluster, consultez [récupération rapide à l’aide de volumes de clichés instantanés transportables](fast-recovery-using-transportable-shadow-copied-volumes.md).

 

 



