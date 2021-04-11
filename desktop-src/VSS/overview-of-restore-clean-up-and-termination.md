---
description: Après une restauration, les rédacteurs vérifient l’état de l’opération afin de pouvoir utiliser les données restaurées et traiter les erreurs.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Vue d’ensemble du nettoyage et de l’arrêt de la restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391e029cdb109589b42240b5482f6aba2ff43555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034344"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Vue d’ensemble du nettoyage et de l’arrêt de la restauration

Après une restauration, les rédacteurs vérifient l’état de l’opération afin de pouvoir utiliser les données restaurées et traiter les erreurs. Le demandeur doit attendre la fin de cette activité. Pour plus d’informations, consultez [vue d’ensemble du traitement d’une restauration sous VSS](overview-of-processing-a-restore-under-vss.md).

Le tableau suivant présente la séquence des actions et des événements qui sont requis après l’exécution d’une opération de restauration.



| Action du demandeur                                                                                                                                                                                                                                                                                                                                                              | Événement                                                           | Action d’écriture                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le demandeur indique la fin de la restauration (voir [**IVssBackupComponents ::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*PostRestore*](vssgloss-p.md) | L’enregistreur effectue un nettoyage après la restauration et gère les échecs de restauration et les fichiers qui ont été restaurés à des emplacements non standard (voir [**CVssWriter :: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| Le demandeur attend que les enregistreurs gèrent l’événement [**postRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) avec [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync). Il doit également vérifier l’état de l’enregistreur (consultez [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | Aucune                                                            | Aucune                                                                                                                                                                                                                                               |
| Le demandeur libère l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .                                                                                                                                                                                                                                                                                    | Aucune                                                            | Aucune                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Actions du demandeur pendant le nettoyage et l’arrêt

À ce stade, un demandeur indique la fin de ses activités de restauration de fichiers en générant un événement [*postRestore*](vssgloss-p.md) en appelant [**IVssBackupComponents ::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Les actions du demandeur sont limitées à l’attente sur les enregistreurs, ce qui peut nécessiter un nettoyage final et gérer les erreurs de restauration, ainsi que la libération de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) une fois que tous les enregistreurs sont retournés par la gestion de l’événement [*postRestore*](vssgloss-p.md) .

## <a name="writer-actions-during-cleanup-and-termination"></a>Actions d’écriture pendant le nettoyage et l’arrêt

L’événement [*postRestore*](vssgloss-p.md) est géré par la méthode virtuelle [**CVssWriter :: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). L’implémentation par défaut retourne simplement la **valeur true** sans entreprendre aucune action. Si un enregistreur doit exercer davantage de contrôle sur la situation postérieure à la restauration, il peut substituer cette méthode.

En plus de tout nettoyage normal (tel que la suppression des fichiers temporaires) qu’un writer peut effectuer dans [**CVssWriter :: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), il peut gérer la réussite ou l’échec des opérations de restauration.

La manière dont il gère les erreurs de restauration, les fichiers restaurés à un autre emplacement et la nécessité de restaurations ultérieures sont entièrement à la discrétion de l’auteur. Les actions classiques peuvent inclure la comparaison de fichiers dans d’autres emplacements ou de nouveaux emplacements avec les fichiers en cours d’utilisation, la fusion de données à partir de plusieurs fichiers ou le démarrage de nouvelles sessions connectées aux nouveaux fichiers de données. Le service VSS fournit les mécanismes suivants pour prendre en charge cette fonction composant par composant :

-   La réussite ou l’échec de la restauration d’un composant se trouve avec [**IVssComponent :: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   L’utilisation de mappages d’emplacements alternatifs dans la restauration des fichiers est indiquée par [**IVssComponent :: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Déterminer si une restauration est incrémentielle et nécessite des restaurations supplémentaires est effectuée en appelant [**IVssComponent :: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores). Les writers qui nécessitent une restauration complète de leurs données ne doivent pas redémarrer tant que cette méthode n’a pas retourné la valeur false.
-   Les enregistreurs peuvent déterminer si le demandeur a besoin de restaurer des fichiers à un emplacement non spécifié précédemment à l’aide de [**IVssComponent :: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) et [**IVssComponent :: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

(Pour plus d’informations sur la restauration de fichiers dans des emplacements autres que les emplacements par défaut, consultez [emplacements de sauvegarde et de restauration non définis par défaut](non-default-backup-and-restore-locations.md).)

Comme pour toute méthode [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , les informations retournées par une instance donnée s’appliquent aux composants [*explicitement inclus*](vssgloss-e.md) pour la sauvegarde et à l’un de ses sous-composants inclus [*implicitement*](vssgloss-i.md) pour les sous-composants de sauvegarde, y compris ceux inclus explicitement pour la restauration par le demandeur à l’aide de [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) (voir utilisation de la [sélectivité pour la restauration et](working-with-selectability-for-restore-and-subcomponents.md) des sous-composants)

Étant donné que les enregistreurs auront besoin d’accéder au document des composants de sauvegarde, il est important que le demandeur ne libère pas l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) jusqu’à la fin du traitement des writers.

 

 



