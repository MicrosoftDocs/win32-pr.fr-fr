---
description: L’implémentation complète d’une sauvegarde nécessite la participation des enregistreurs du système.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Prise en charge du schéma de sauvegarde de l’enregistreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593df12f552f206d5d0eedbf8d021b69ef955c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201453"
---
# <a name="writer-backup-schema-support"></a>Prise en charge du schéma de sauvegarde de l’enregistreur

L’implémentation complète d’une sauvegarde nécessite la participation des enregistreurs du système. Les différents types de sauvegardes prises en charge sont appelés schémas et sont indiqués par un masque de bits (ou une opération or au niveau du bit) des membres de l’énumération du [**\_ \_ schéma de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) . Les schémas valides actuellement pris en charge sont les suivants :

-   Schéma par défaut : complet (VSS \_ BS \_ non défini) : indique qu’un writer prend en charge une sauvegarde où tous les fichiers seront sauvegardés quelle que soit leur date de dernière sauvegarde. L’historique de sauvegarde de chaque fichier peut être mis à jour par le demandeur, et les enregistreurs qui prennent en charge la \_ \_ valeur d’énumération VSS BS timestamp stockent un horodatage mis à jour auprès du demandeur. Ce schéma de sauvegarde peut être utilisé comme base d’une sauvegarde incrémentielle ou différentielle.

    La restauration d’une sauvegarde complète nécessite une seule image de sauvegarde.

-   La sauvegarde de copie (VSS \_ BS \_ Copy), comme \_ le \_ schéma de sauvegarde complète VSS BS, indique qu’un writer prend en charge une sauvegarde où tous les fichiers seront sauvegardés quelle que soit leur date de dernière sauvegarde. Toutefois, l’historique de sauvegarde de chaque fichier n’est pas mis à jour par le demandeur ou l’enregistreur, et ce type de sauvegarde ne peut pas être utilisé comme base d’une sauvegarde incrémentielle ou différentielle.
-   Fichier journal (VSS \_ BS \_ log) : seuls les fichiers journaux d’un enregistreur doivent être sauvegardés. Pour ce faire, un enregistreur doit avoir ajouté au moins un fichier à au moins un composant à l’aide de la méthode [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . Ce type de sauvegarde est spécifique à VSS.
-   Emplacements de restauration personnalisés ( \_ l' \_ enregistreur VSS BS \_ prend en charge \_ \_ la nouvelle cible) : indique la prise en charge de l’enregistreur pour un demandeur qui change, au moment de la restauration, où ses fichiers sont restaurés. Cela signifie qu’un writer a été codé pour vérifier ce réadressage (à l’aide de [**IVssComponent :: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)) et qu’il dispose de la capacité nécessaire pour travailler avec des fichiers déplacés.
-   Restore with Move (VSS \_ BS \_ writer \_ prend en charge \_ Restore \_ with \_ Move) : indique que le writer prend en charge l’exécution de plusieurs instances d’écriture avec le même ID de classe et qu’il prend en charge le déplacement d’un composant vers une instance de writer différente au moment de la restauration. L’instance de writer est spécifiée à l’aide d’un nom d’instance d’enregistreur persistant qui a été passé comme paramètre *wszWriterInstanceName* à la méthode [**CVssWriter :: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) . Un demandeur peut obtenir le nom de l’instance du writer à l’aide de [**IVssExamineWriterMetadataEx :: GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) et déplacer les composants pendant la restauration à l’aide de [**IVssBackupComponentsEx :: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex).

    **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge tant que Windows Server 2003 avec Service Pack 1 (SP1) n’est pas pris en charge.

-   Incrémentielle (VSS \_ BS \_ incrémentielle) : indique que le writer utilise l’API VSS pour aider le demandeur, en veillant à ce que seuls les fichiers qui ont été modifiés ou ajoutés depuis la dernière sauvegarde complète ou incrémentielle soient copiés sur un support de stockage.

    La restauration d’une sauvegarde incrémentielle nécessite l’image de sauvegarde d’origine et toutes les images de sauvegarde incrémentielles effectuées depuis la sauvegarde initiale.

-   Differential (VSS \_ BS \_ Differential) : indique que le writer utilise l’API VSS pour permettre au demandeur de s’assurer que seuls les fichiers qui ont été modifiés ou ajoutés depuis la dernière sauvegarde complète doivent être copiés sur un support de stockage ; toutes les informations de sauvegarde intermédiaires sont ignorées.

    La restauration d’une sauvegarde différentielle nécessite l’image de sauvegarde d’origine et l’image de sauvegarde différentielle la plus récente effectuée depuis la dernière sauvegarde complète.

-   Incrémentielle/différentielle : prise en charge de l’horodatage (VSS \_ BS \_ horodaté) : indique qu’un enregistreur prend en charge l’utilisation du mécanisme d’horodatage VSS pour inclure des fichiers dans des opérations incrémentielles ou différentielles. Lors de la sauvegarde, l’enregistreur doit stocker le tampon [*de sauvegarde d’un jeu de fichiers*](vssgloss-f.md) avec la méthode [**IVssComponent :: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) , et à la restauration, le récupérer avec [**IVssComponent :: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).
-   Incremental/Differential : heure de la dernière modification de la prise en charge (VSS \_ BS \_ dernière \_ modification) : indique que lors de l’implémentation de sauvegardes incrémentielles ou différentielles avec des fichiers différenciés, un enregistreur peut fournir des informations de date et d’heure de dernière modification de manière indépendante. Ces informations peuvent être fournies à un demandeur par le biais de la méthode [**IVssComponent :: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) .
-   Incremental/Differential : limitation de prise en charge (VSS \_ BS \_ exclusive \_ INCREMENTAL \_ Differential) : indique la prise en charge de l’enregistreur des schémas de sauvegarde différentielle ou incrémentielle, mais uniquement : par exemple, vous ne pouvez pas suivre une sauvegarde incrémentielle avec une sauvegarde différentielle.
-   État du système indépendant (VSS \_ BS \_ Independent \_ System \_ State) : indique que le writer prend en charge la sauvegarde des données qui font partie de l’état du système, mais qui peuvent également être sauvegardées indépendamment de l’état du système.

    **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge jusqu’à Windows Vista.

-   Roll-Forward Restore (VSS \_ BS \_ restauration par progression \_ Restore) : indique que le writer prend en charge le paramètre d’un demandeur de restauration par progression à l’aide de [**IVssBackupComponentsEx2 :: SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward).

    **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge jusqu’à Windows Vista.

-   Restore Rename (renommer VSS \_ BS \_ \_ ) : indique que le writer prend en charge un demandeur de nom de restauration à l’aide de [**IVssBackupComponentsEx2 :: SetRestoreName**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename).

    **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge jusqu’à Windows Vista.

-   Restauration faisant autorité (VSS \_ BS \_ faisant autorité \_ ) : indique que le writer prend en charge un paramètre de demandeur faisant autorité de la restauration à l’aide de [**IVssBackupComponentsEx2 :: SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore).

Les rédacteurs définissent leurs schémas à l’aide de la méthode [**IVssCreateWriterMetadata :: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) , et un demandeur obtient le schéma de chaque enregistreur en appelant [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



