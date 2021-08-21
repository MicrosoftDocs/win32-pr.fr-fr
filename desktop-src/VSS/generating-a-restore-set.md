---
description: Un jeu de restauration est une liste de tous les fichiers à restaurer et des emplacements vers lesquels ils seront restaurés.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Génération d’un jeu de restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85dd620869614420e5073f47ef4ac8732b1e2c0d0d218ea0e94ae690cb9f773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958449"
---
# <a name="generating-a-restore-set"></a>Génération d’un jeu de restauration

Un jeu de restauration est une liste de tous les fichiers à restaurer et des emplacements vers lesquels ils seront restaurés.

Comme lors de la génération de la liste des fichiers de sauvegarde (consultez [génération d’un jeu de sauvegarde](generating-a-backup-set.md)), un algorithme permettant de déterminer les fichiers à restaurer et l’emplacement de leur restauration doit effectuer l' [*instance*](vssgloss-w.md) de l’enregistreur par l’instance de Writer et, par composant, pour chaque instance du writer.

Il est nécessaire d’associer chaque fichier sur le support de sauvegarde au composant qui l’a géré. Il est également nécessaire d’obtenir la [*méthode de restauration*](vssgloss-r.md)du composant de gestion, les informations sur la [*cible de restauration*](vssgloss-r.md) du fichier et ses [*mappages d’emplacements secondaires*](vssgloss-a.md) (le cas échéant).

Certains fichiers peuvent également nécessiter des opérations de [*fichiers partielles*](vssgloss-p.md) ou des [*cibles dirigées*](vssgloss-d.md) pour la restauration.

En examinant la [*sélectivité des composants pour la sauvegarde*](vssgloss-s.md) et les [*chemins logiques*](vssgloss-l.md) (voir [utilisation de la sélectivité et des chemins logiques](working-with-selectability-and-logical-paths.md)), un demandeur est en mesure de déterminer la structure du composant de l’opération de sauvegarde qu’il va restaurer.

Avec la structure de composant de la sauvegarde établie, le demandeur peut obtenir les informations sur le [*jeu de fichiers*](vssgloss-f.md) de chaque composant (spécification de fichier, chemin d’accès et indicateur de récurrence). Un demandeur peut ensuite générer un jeu de restauration.

Les fichiers nécessitant des [*fichiers partiels*](vssgloss-p.md)ou des [*cibles dirigées*](vssgloss-d.md) fournissent leurs propres instructions de restauration détaillées (consultez emplacements de restauration [et de sauvegarde non définis par défaut](non-default-backup-and-restore-locations.md)), qui peuvent ensuite être ajoutés au jeu de restauration.

Un mécanisme classique de génération d’un jeu de restauration pour les fichiers qui ne sont pas impliqués dans des opérations de fichiers partiels, ou les [*cibles dirigées*](vssgloss-d.md) peut se poursuivre en procédant comme suit :

1.  Obtenez la liste des fichiers sur le support de sauvegarde, y compris leurs chemins d’accès d’origine.

2.  Identifiez la [*classe de writer*](vssgloss-w.md) et le composant pour chaque fichier sur le support de sauvegarde en procédant comme suit :

    -   Pour chaque enregistreur, obtenez les informations sur le composant ([**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) en appelant [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) sur tous ses composants.
    -   Pour chaque composant, obtenez les informations de descripteur de fichier ([**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) pour chaque ensemble de fichiers que le composant contient (selon les types de données que le composant contient en appelant [**IVssWMComponent :: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent :: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)et [**IVssWMComponent :: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).
    -   Comparez les informations de nom et de chemin d’accès du fichier à celles retournées par les informations de chemin d’accès contenues dans le descripteur de fichier pour chaque ensemble de fichiers dans un composant (retourné par [**IVssWMFiledesc :: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc :: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)et [**IVssWMFiledesc :: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)) par rapport aux informations de chemin des fichiers stockés pour déterminer si le fichier fait partie du composant.
        > [!Note]  
        > Vous devez ignorer les autres informations sur l’emplacement dans le descripteur de fichier récupéré à partir d’un composant trouvé dans un document de métadonnées de l’enregistreur stocké (autrement dit, [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) ne retourne pas la **valeur null**). Cet autre emplacement est le [*chemin alternatif*](vssgloss-a.md), qui est utilisé uniquement lors de la sauvegarde.

         

3.  Obtenez d’autres informations de mappage pour chaque fichier sur le support de sauvegarde :

    -   Les mappages de fichiers de remplacement sont stockés au moment de l’écriture, et non au niveau du composant, et sont obtenus à partir de l’objet [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) retourné par [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).
    -   Vous pouvez déterminer si un fichier particulier possède un autre mappage d’emplacement en vérifiant le chemin d’accès et le nom du fichier par rapport au chemin d’accès et à la spécification de fichier contenus dans le mappage de l’emplacement de remplacement retourné par [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), via [**IVssWMFiledesc :: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc :: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)et [**IVssWMFiledesc :: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). (Si un autre chemin d’accès a été utilisé lors de la sauvegarde, ces informations doivent être ignorées au cours de cette vérification du traitement d’une restauration.)
    -   Si un fichier et un emplacement de remplacement mappent les descripteurs de fichiers à, vous utilisez la méthode [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) de l’objet [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) retourné par [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) pour Rechercher l’autre emplacement vers lequel vous pouvez restaurer le fichier.
    -   Le mappage de l’autre emplacement obtenu de cette façon n’accepte pas nécessairement celui renvoyé par le document des composants de sauvegarde par [**IVssComponent :: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). La valeur [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) n’est pas vide uniquement si le mappage d’emplacement secondaire est utilisé pour un fichier.

4.  Avec ces informations de fichier et de composant, le document composants de sauvegarde peut être interrogé pour obtenir des informations sur les cibles de restauration, les options et les nouveaux emplacements de restauration pour chaque fichier. Ces informations peuvent être associées à la liste des fichiers, composants et emplacements secondaires.

5.  Les fichiers non protégés par les rédacteurs peuvent être sélectionnés de manière cohérente avec les opérations de restauration traditionnelles.

À ce stade, un demandeur doit avoir une liste de tous les fichiers dont il a besoin pour la restauration, ainsi que des instructions sur la façon de les restaurer et de commencer à restaurer des fichiers sur la base de :

-   Si des mappages d’emplacements de substitution, ou l’emplacement de fichier d’origine doivent être utilisés comme cible pour la restauration, dépend de la présence ou de l’absence d’un fichier à cet emplacement cible et des paramètres de composant de la [**\_ \_ cible de restauration VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) et de l' [**\_ \_ énumération VSS RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) (consultez [emplacements de sauvegarde et de restauration non définis par défaut](non-default-backup-and-restore-locations.md)).
-   Le fait qu’une tentative de restauration aboutisse dépende de problèmes tels que les autorisations d’accès de la cible, si les fichiers cibles sont verrouillés et d’autres problèmes conventionnels liés à la restauration des fichiers.
-   La réussite ou l’échec de la restauration d’un composant donné pour une instance de writer donnée doit être conservé dans le document des composants de sauvegarde en appelant [**IVssBackupComponents :: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). Cela rendra les informations accessibles aux enregistreurs lors du traitement de l’événement PostRestore.
-   Si un fichier est restauré vers un autre mappage d’emplacement, le demandeur doit appeler [**IVssBackupComponents :: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping). Cela permettra aux rédacteurs de déterminer si leurs fichiers ont été restaurés à d’autres emplacements via [**IVssComponent :: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Les demandeurs peuvent trouver qu’il est souhaitable de restaurer les fichiers à de nouveaux emplacements. Cela est acceptable, mais le demandeur doit l’indiquer à l’enregistreur à l’aide de la méthode [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) .

 

 



