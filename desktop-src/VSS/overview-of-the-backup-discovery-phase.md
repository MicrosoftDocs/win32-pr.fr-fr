---
description: 'Après l’appel de IVssBackupComponents :: GatherWriterMetadata, un demandeur utilise l’instance de l’interface IVssAsync retournée à partir de cet appel pour déterminer quand tous les enregistreurs sur le système ont terminé de construire leurs documents de métadonnées d’écriture.'
ms.assetid: 04658d50-04f0-4189-8b88-ff152f1bf482
title: Vue d’ensemble de la phase de découverte de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d2a2d05220ecf3e25c77c18cc62b07726964f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413364"
---
# <a name="overview-of-the-backup-discovery-phase"></a>Vue d’ensemble de la phase de découverte de sauvegarde

Après l’appel de [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), un demandeur utilise l’instance de l’interface [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) retournée à partir de cet appel pour déterminer quand tous les enregistreurs sur le système ont terminé de construire leurs documents de métadonnées d’écriture. Pour plus d’informations, consultez [vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md).

À ce stade, le demandeur peut commencer une phase de découverte, examiner les métadonnées pour déterminer les applications en cours d’exécution et les volumes qui doivent faire l’objet de clichés instantanés pour obtenir une sauvegarde complète. Le tableau suivant présente la séquence des actions et des événements qui sont requis pour la phase de découverte de la sauvegarde.



| Action du demandeur                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Événement | Action d’écriture                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------|
| Récupérez les documents de métadonnées de l’enregistreur (consultez [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata), [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)).                                                                                                                                                                                                                                                                                                                                                 | None  | Pendant cette période, les rédacteurs peuvent être en mesure de continuer à fonctionner normalement. |
| Utilisez la liste des composants et leurs [*jeux de fichiers*](vssgloss-f.md), ainsi que les fichiers exclus, pour obtenir la liste des volumes et des fichiers impliqués dans la sauvegarde (voir [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)).                                                                                                                                                                                                                                                                      | None  | None                                                                              |
| Choisissez les composants dans le document de métadonnées de l’enregistreur du writer à sauvegarder. Appelez [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour chaque composant pour l’ajouter au document composants de sauvegarde. (Voir [utilisation de la sélectivité pour la sauvegarde](working-with-selectability-for-backup.md) et [utilisation du document sur les composants de sauvegarde](working-with-the-backup-components-document.md).)                                                                                                                      | None  | None                                                                              |
| Initialiser le jeu de clichés instantanés, le contexte et vérifier les volumes pris en charge (consultez [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset), [**IVssBackupComponents :: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)).                                                                                                                                                                                                                                                                                   | None  | None                                                                              |
| Si vous effectuez une sauvegarde sans composant, ajoutez les volumes cibles souhaités à partir du document de métadonnées de l’enregistreur au jeu de clichés instantanés en appelant [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) pour chaque volume. Dans le cas contraire, pour les composants du document de métadonnées de l’enregistreur qui ont déjà été ajoutés au document des composants de sauvegarde (en appelant [**addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), le demandeur doit également appeler **IVssBackupComponents :: AddToSnapshotSet** pour chaque volume affecté. | None  | None                                                                              |



 

## <a name="writer-actions-during-the-discovery-phase"></a>Actions d’écriture au cours de la phase de découverte

Étant donné que la phase de découverte d’une sauvegarde se compose principalement d’un demandeur qui traite les informations récupérées à partir de documents de métadonnées d’écriture, il n’y a que peu d’exigences sur un writer.

En théorie, un enregistreur peut continuer à s’exécuter normalement à ce stade. Toutefois, il peut être souhaitable pour les rédacteurs de commencer les préparations pour les opérations de sauvegarde et de cliché instantané à venir.

## <a name="requester-actions-during-the-discovery-phase"></a>Actions du demandeur pendant la phase de découverte

Un demandeur utilise les objets [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenus via [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) pour itérer sur toutes les métadonnées des enregistreurs et sélectionner les Writers dont il envisage de sauvegarder les données.

À ce stade, le demandeur doit générer une liste initiale des candidats de sauvegarde de chaque enregistreur en effectuant une itération sur les composants du writer à l’aide de [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Cela fournit au demandeur des objets [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) , à partir desquels vous pouvez obtenir les spécifications pour les fichiers à sauvegarder à l’aide de [**IVssWMComponent :: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent :: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)et [**IVssWMComponent :: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).

Étant donné que l’objet [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) peut utiliser des caractères génériques pour stocker des informations d’emplacement de fichier, il peut être nécessaire d’utiliser des fonctions telles que [**FindFirstFile**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/win32/api/fileapi/nf-fileapi-findfirstfileexa)et [**FindNextFile**](/windows/win32/api/fileapi/nf-fileapi-findnextfilea).

Tant que le cliché instantané n’est pas terminé, il est toujours possible pour les rédacteurs d’ajouter ou de supprimer des fichiers sur le disque au cours normal de leur travail. vous ne devez donc pas générer la liste réelle des fichiers à sauvegarder pour l’instant.

Au lieu de cela, vous trouverez la liste initiale des fichiers et volumes à sauvegarder à ce stade en procédant comme suit :

1.  L’examen de tous les composants sélectionnables pour la sauvegarde et les composants non sélectionnables dans le document de métadonnées d’écriture de chaque enregistreur (à l’aide de [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) et leur organisation dans des [*jeux de composants*](vssgloss-c.md) utilisent le [*chemin logique*](vssgloss-l.md) (voir [utilisation de la sélectivité et des chemins logiques](working-with-selectability-and-logical-paths.md))
2.  [*Inclusion explicite*](vssgloss-e.md) de tous les composants requis (non sélectionnables pour les composants de sauvegarde sans sélection pour les ancêtres de sauvegarde) dans le document des composants de sauvegarde à l’aide de [ **IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)
3.  Choisir d’inclure explicitement sélectionnables facultatifs pour les composants de sauvegarde qui ne définissent pas un jeu de composants (à l’aide de [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent))
4.  Sélection [*de jeux de composants*](vssgloss-c.md) pour la participation à une sauvegarde en ajoutant explicitement leur élément pouvant être défini pour la sauvegarde (à l’aide de [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), qui [*comprend implicitement*](vssgloss-i.md) les sous- [*composants*](vssgloss-s.md)de l’ensemble de composants.
5.  À l’aide des informations du [*jeu de fichiers*](vssgloss-f.md) dans le document des métadonnées de l’enregistreur des enregistreurs sélectionnés et des fonctions de gestion du volume, un demandeur détermine les chemins d’accès des fichiers à sauvegarder et les volumes dont les clichés instantanés doivent être copiés.

Notez que seuls les composants inclus explicitement (à l’aide de [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) dans la sauvegarde et dans le document composants de sauvegarde auront des instances de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ajoutées à ce document. Ces instances sont utilisées pour examiner et modifier les paramètres des composants inclus explicitement et des sous-composants inclus implicitement (voir [sélectivité et utilisation des propriétés de composant](selectability-and-working-with-component-properties.md)).

Si un writer comprend l’un des composants d’un enregistreur, il doit ajouter tous ses composants requis. Toutefois, un demandeur est également libre d’ignorer complètement tous les jeux de composants d’un enregistreur. Si aucun des composants d’un enregistreur n’est explicitement sélectionné, le Writer n’est pas sélectionné et VSS empêche ce writer de participer au reste de l’opération de sauvegarde.

Le demandeur initie le jeu de clichés instantanés qui contiendra les volumes sélectionnés en appelant [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Si le volume peut participer à un cliché instantané (qui peut être vérifié avec [**IVssBackupComponents :: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)), le demandeur peut ajouter ce volume au jeu de clichés instantanés à l’aide de [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Bien qu’il ne soit généralement pas utile, un demandeur peut parfois également choisir le [*fournisseur*](vssgloss-p.md) qui maintiendra le cliché instantané pour un volume donné (pour plus d’informations, consultez [sélection de fournisseurs](selecting-providers.md) ).

Une attention particulière doit être accordée au traitement d’un volume contenant des dossiers montés ou des points d’analyse. Un dossier monté ou un point d’analyse peut apparaître dans un cliché instantané et peut être sauvegardé. Toutefois, un dossier monté ou un point d’analyse ne peut pas être parcouru sur le volume des clichés instantanés (voir [utilisation des dossiers montés et des points d’analyse](working-with-reparse-and-mount-points.md)).

À ce stade de la sauvegarde, le document des composants de sauvegarde est initialisé et rempli. Dans les opérations futures, les rédacteurs et les demandeurs peuvent utiliser l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) pour communiquer entre eux.

Les enregistreurs ont accès à l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) lors du traitement des événements [*PrepareForBackup*](vssgloss-p.md), [*PostSnapshot*](vssgloss-p.md)et [*BackupComplete*](vssgloss-b.md) .

 

 
