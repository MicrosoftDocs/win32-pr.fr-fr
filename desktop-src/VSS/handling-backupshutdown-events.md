---
description: Il est possible qu’une application de sauvegarde (demandeur) se termine et ne génère pas d’événement BackupComplete.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Gestion des événements BackupShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939e8e64ca9ee463b0b8331e607f8068c3325d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519646"
---
# <a name="handling-backupshutdown-events"></a>Gestion des événements BackupShutdown

Il est possible qu’une application de sauvegarde (demandeur) se termine et ne génère pas d’événement [*BackupComplete*](vssgloss-b.md) . L’application de sauvegarde peut se bloquer ou être arrêtée (à partir du gestionnaire des tâches, par exemple) et ne pas être en mesure d’appeler [**IVssBackupComponents :: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Par conséquent, l’infrastructure VSS (plutôt que le demandeur) génère un événement [*BackupShutdown*](vssgloss-b.md) chaque fois qu’une instance de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) participant à une sauvegarde est libérée, qu’elle soit libérée par le demandeur ou par le système.

Si une sauvegarde se déroule correctement, un enregistreur reçoit un événement BackupComplete suivi d’un événement BackupShutdown.

Si l’opération est abandonnée (le demandeur génère un [*événement d’abandon*](vssgloss-a.md) en appelant [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) ou échoue brusquement, un enregistreur peut recevoir uniquement un événement BackupShutdown et il peut ne pas recevoir d’autres événements qui effectuent des opérations de nettoyage. Il revient à un enregistreur de déterminer si un événement BackupShutdown suit une séquence d’événements appropriée, ou représente une défaillance inattendue des opérations de sauvegarde.

Le gestionnaire d’événements BackupShutdown, [**CVssWriter :: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), reçoit l' \_ ID VSS (Guid) du jeu de clichés instantanés de l’opération de sauvegarde en cours d’arrêt. L’enregistreur peut l’utiliser pour déterminer l’opération de sauvegarde en cours d’arrêt, s’il a stocké l’ID du jeu de clichés instantanés pendant sa séquence de sauvegarde (par exemple, à partir de [**CVssWriter :: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), [**CVssWriter :: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)ou [**CVssWriter :: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) à l’aide de [**CVssWriter :: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid).

Toutefois, un enregistreur ne doit pas appeler [**CVssWriter :: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) à partir de [**CVssWriter :: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown). En outre, **CVssWriter :: GetCurrentSnapshotSetId** ne peut pas être appelé après le retour de [**CVssWriter :: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) .

Il est possible que le writer soit impliqué dans plusieurs opérations de sauvegarde, et si un événement BackupShutdown est appelé en raison d’un arrêt brutal d’un demandeur, l' \_ ID VSS renvoyé peut être celui d’une autre opération de sauvegarde à laquelle le writer participe.

 

 



