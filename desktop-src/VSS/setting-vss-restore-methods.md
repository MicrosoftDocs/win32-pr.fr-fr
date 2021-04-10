---
description: La configuration des opérations de restauration commence en fait pendant la sauvegarde des données, lorsque les enregistreurs spécifient, dans leurs documents de métadonnées d’écriture, comment leurs données doivent être restaurées.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Définition des méthodes de restauration VSS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412cb699fb791a973e280f63fec03bd2854ccd1d
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211159"
---
# <a name="setting-vss-restore-methods"></a>Définition des méthodes de restauration VSS

La configuration des opérations de restauration commence en fait pendant la sauvegarde des données, lorsque les enregistreurs spécifient, dans leurs documents de métadonnées d’écriture, comment leurs données doivent être restaurées.

Ces spécifications, appelées méthodes de [*restauration*](vssgloss-r.md) ou cibles de [*restauration*](vssgloss-r.md)d’origine, peuvent être modifiées lors de la restauration par les rédacteurs définissant de nouvelles cibles de restauration ou par les demandeurs restaurant les nouveaux emplacements (voir [les emplacements de sauvegarde et de restauration non définis par défaut](non-default-backup-and-restore-locations.md)).

En appelant [**IVssCreateWriterMetadata :: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod), un writer indique quelle méthode de restauration doit être utilisée dans son document de métadonnées d’écriture. La méthode Restore est définie sur la valeur Writer et appliquée à tous les fichiers de tous les composants gérés par un writer.

Un demandeur obtient (et doit respecter) ces informations en appelant [**IVssExamineWriterMetadata :: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

La méthode Restore est définie par une énumération [**VSS \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) , qui est transmise à [**IVssCreateWriterMetadata :: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) et retournée à partir de [**IVssExamineWriterMetadata :: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Le document de métadonnées de l’enregistreur prend en charge les méthodes de restauration valides suivantes (une méthode de restauration de la \_ RME VSS \_ non définie indique une erreur d’écriture). Les figures résument la manière dont les différentes méthodes de restauration prises en charge et définies doivent être implémentées (VSS \_ RME \_ personnalisé n’a aucune figure associée, car, par définition, elle est spécifique à l’enregistreur et doit suivre les API et la documentation spécifiques du writer) :

-   VSS \_ RME \_ Restore \_ si ce \_ n’est pas le cas \_ . Restaurez les fichiers du composant sur le disque si aucun des fichiers ne se trouve déjà sur le disque. L’état du fichier cible doit être vérifié après un événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagramme qui montre une arborescence de résolution des problèmes pour VSS_RME_RESTORE_IF_NOT_THERE.](images/rint.png)
-   \_Restore RME VSS \_ \_ si \_ peut \_ remplacer. Restaurez les fichiers sur le disque si tous les fichiers peuvent être remplacés. L’état du fichier cible doit être vérifié après un événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagramme qui montre une arborescence de résolution des problèmes pour VSS_RME_RESTORE_IF_CAN_REPLACE.](images/ricr.png)
-   VSS \_ RME \_ arrêter le démarrage de la \_ restauration \_ . Un service sera arrêté avant la restauration des fichiers.
    ![Diagramme qui montre une arborescence de résolution des problèmes pour VSS_RME_STOP_RESTORE_START.](images/srr.png)
-   \_ \_ restauration de RME VSS vers un \_ \_ autre \_ emplacement. Restaurez les fichiers sur le disque à un autre emplacement. Les mappages d’emplacement de remplacement sont spécifiés dans le document de métadonnées de l’enregistreur.
    ![Diagramme qui montre une arborescence de résolution des problèmes pour VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.](images/rtal.png)
-   \_restauration RME \_ VSS \_ au \_ redémarrage. Entraîner la restauration des fichiers (remplacés) lors du redémarrage de l’ordinateur.
    ![Diagramme qui montre une arborescence de résolution des problèmes pour VSS_RME_RESTORE_AT_REBOOT.](images/rar.png)
-   \_restauration RME \_ VSS \_ au \_ redémarrage \_ si \_ ne peut pas être \_ remplacé. Si un fichier n’a pas pu être restauré sur le disque d’un système en cours d’exécution, il est restauré (remplacé) lors du redémarrage de l’ordinateur.
    ![Diagramme qui affiche une forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE de l’arborescence de résolution des problèmes. ](images/raricr.png)
-   \_RME VSS \_ personnalisé. Aucune des méthodes prédéfinies ne fonctionnera. l’application de sauvegarde doit utiliser des API spécialisées pour effectuer l’opération de restauration. Pour cette méthode de sauvegarde, le demandeur doit entièrement comprendre le writer en question. Consultez les [cas d’utilisation de VSS spéciaux](special-vss-usage-cases.md) pour les instances actuellement prises en charge.

 

 



