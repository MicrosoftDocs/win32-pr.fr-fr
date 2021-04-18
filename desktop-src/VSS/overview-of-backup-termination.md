---
description: Le tableau suivant montre la séquence des actions et des événements qui sont requis pour terminer une opération de sauvegarde. Pour plus d’informations, consultez vue d’ensemble du traitement d’une sauvegarde sous VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Vue d’ensemble de l’arrêt de la sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9268bd8fd4ec51be2ee7a891d4dffb3a5cb1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519857"
---
# <a name="overview-of-backup-termination"></a>Vue d’ensemble de l’arrêt de la sauvegarde

Le tableau suivant montre la séquence des actions et des événements qui sont requis pour terminer une opération de sauvegarde. Pour plus d’informations, consultez [vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md).



| Action du demandeur                                                                                                                                                                                                              | Événement                                                                 | Action d’écriture                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le demandeur termine le cliché instantané en libérant l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ou en appelant [**IVssBackupComponents ::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | Aucune                                                                  | Aucune                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) est libéré en appelant [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | Le writer gère l’événement avec [**CVssWriter :: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), ce qui lui permet de nettoyer tout état relatif au jeu de clichés instantanés. Si l’opération de sauvegarde a échoué (c’est-à-dire qu’elle n’a pas généré d’événement [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) ), l’enregistreur peut également avoir besoin d’effectuer la gestion des erreurs. Pour plus d’informations, consultez [gestion des événements BackupShutdown](handling-backupshutdown-events.md) . |



 

Étant donné qu’une interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ne peut pas être réutilisée et que le destructeur de l’interface termine les clichés instantanés, il n’y a généralement aucune raison d’appeler [**IVssBackupComponents ::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). Cette méthode est conçue pour être utilisée conjointement avec la gestion des erreurs et l’abandon des sauvegardes (consultez [abandon des opérations VSS](aborting-vss-operations.md)).

 

 
