---
description: Un demandeur doit avoir une compréhension bien définie de l’état de l’enregistreur qui y participe pendant la création de clichés instantanés, ainsi que pendant les opérations de sauvegarde et de restauration.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Détermination de l’état de l’enregistreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211363"
---
# <a name="determining-writer-status"></a>Détermination de l’état de l’enregistreur

Un demandeur doit avoir une compréhension bien définie de l’état de l’enregistreur qui y participe pendant la création de clichés instantanés, ainsi que pendant les opérations de sauvegarde et de restauration. Pour ce faire, il est recommandé d’effectuer les opérations suivantes :

-   Les demandeurs utilisent [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents :: GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)et [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).
-   Comme décrit dans [vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md) et [vue d’ensemble du traitement d’une restauration sous VSS](overview-of-processing-a-restore-under-vss.md), ces méthodes sont particulièrement utiles lorsqu’elles sont appelées dans une séquence de sauvegarde ou de restauration bien définie. En général, cela signifie que les enregistreurs doivent être interrogés après qu’un demandeur a terminé l’une de ses tâches et a généré un événement VSS.

    Lors du traitement d’une sauvegarde, un demandeur doit interroger un enregistreur à la suite de l’exécution des méthodes suivantes. Les demandeurs doivent appeler [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) après avoir appelé [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) pour que la session de l’enregistreur soit définie sur un état terminé.

    > [!Note]  
    > Cela n’est nécessaire que sur Windows Server 2008 avec Service Pack 2 (SP2) et versions antérieures.

     

    <dl> <dt>

[**IVssBackupComponents ::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**IVssBackupComponents ::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

Pendant les opérations de restauration, un demandeur doit interroger un enregistreur après avoir terminé les méthodes suivantes :
<dl> <dt>

[**IVssBackupComponents ::P Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**IVssBackupComponents ::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   Les appels à [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) qui ne font pas partie d’une séquence de sauvegarde ou de restauration bien définie ne fournissent pas une image fiable de l’état de l’enregistreur, car ils peuvent refléter des conditions qui n’indiquent pas d’échec dans l’opération actuelle, par exemple :
    -   Échec de la création d’un cliché instantané précédent
    -   Erreur dans une opération de sauvegarde ou de restauration précoce
    -   Un enregistreur qui ne répond pas traite actuellement un événement

Par conséquent, les développeurs ne doivent pas s’appuyer sur l’état de l’enregistreur renvoyé par des processus autres que le demandeur ou tenter de surveiller la progression d’une instance de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) avec une autre (éventuellement dans un thread distinct).

Notez que pour les opérations de sauvegarde, où il est nécessaire d’examiner les documents de métadonnées de l’enregistreur des writers, il n’est pas nécessaire d’appeler [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) et [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) après la génération et la gestion de l’événement d' [*identification*](vssgloss-i.md) provoqué par [**IVssBackupComponents :: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

[**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) signale uniquement l’état des enregistreurs dont les métadonnées ont été fournies à VSS par les rédacteurs [*identifient*](vssgloss-i.md) les gestionnaires d’événements, [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (et retournés au demandeur par [**IVssBackupComponents :: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) et [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).

Si l’implémentation d’un writer de [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) échoue, les métadonnées de ce writer ne feront pas partie de la liste des documents de métadonnées de l’enregistreur fournis à VSS, aucune information d’État n’est disponible et l’appel est redondant.

Pour les opérations de restauration, où le demandeur n’a pas besoin d’examiner les documents de métadonnées de l’enregistreur des enregistreurs en cours d’exécution, l’appel de [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) et de [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) peut être un moyen plus efficace de déterminer les writers qui s’exécutent.

 

 



