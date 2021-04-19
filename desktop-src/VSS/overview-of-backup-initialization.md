---
description: 'Cette étape de la sauvegarde Initialise à la fois le writer et le demandeur, en remplissant leurs structures de données internes, en spécifiant la sauvegarde et établit la communication de l’enregistreur/du demandeur via l’appel requis à IVssBackupComponents :: GatherWriterMetadata. Pour plus d’informations, consultez vue d’ensemble du traitement d’une sauvegarde sous VSS.'
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Vue d’ensemble de l’initialisation de la sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fb97b43cf19ca60e3e4601899700e35bdad3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531887"
---
# <a name="overview-of-backup-initialization"></a>Vue d’ensemble de l’initialisation de la sauvegarde

Cette étape de la sauvegarde Initialise à la fois le writer et le demandeur, en remplissant leurs structures de données internes, en spécifiant la sauvegarde et établit la communication de l’enregistreur/du demandeur via l’appel requis à [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Pour plus d’informations, consultez [vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md).

Le tableau suivant présente la séquence des actions et des événements qui sont requis pour l’initialisation de la sauvegarde.



| Action du demandeur                                                                                                                                                                                                                                                                                                                            | Événement                                                     | Action d’écriture                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crée une interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) et l’initialise pour gérer une sauvegarde (consultez [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents :: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) et éventuellement pour activer ou désactiver les enregistreurs sur le système. | Aucune                                                      | Aucune                                                                                                                                                                                                                                                       |
| Vous pouvez éventuellement définir le contexte pour les opérations de clichés instantanés et interroger éventuellement le système sur les fournisseurs et les clichés instantanés qu’il prend en charge (consultez [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | Aucune                                                      | Aucune                                                                                                                                                                                                                                                       |
| Le demandeur peut fournir des informations supplémentaires sur la gestion des opérations de sauvegarde et de restauration (voir [**IVssBackupComponents :: SetBackupState).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)                                                                                                                                                        | Aucune                                                      | Aucune                                                                                                                                                                                                                                                       |
| Lance un contact asynchrone avec les enregistreurs (voir [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))                                                                                                                                                                                           | [*Repérer*](vssgloss-i.md) | Crée un document de métadonnées de l’enregistreur (consultez [utilisation du document de métadonnées de l’enregistreur](working-with-the-writer-metadata-document.md), [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) |



 

## <a name="requester-actions-during-backup-initialization"></a>Actions du demandeur pendant l’initialisation de la sauvegarde

Un objet [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ne peut être utilisé que pour une seule sauvegarde. Par conséquent, un demandeur doit passer à la fin de la sauvegarde, y compris la libération de l’interface **IVssBackupComponents** . Si la sauvegarde doit se terminer prématurément, le demandeur doit appeler [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) , puis libérer l’objet **IVssBackupComponents** (pour plus d’informations, consultez [abandon des opérations VSS](aborting-vss-operations.md) ). N’essayez pas de reprendre l’interface **IVssBackupComponents** .

En règle générale, le document sur les composants de sauvegarde d’un demandeur est initialisé comme vide. Un document de composants de sauvegarde stocké peut être chargé lors de l’appel de [**IVssBackupComponents :: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) , généralement pour la prise en charge des volumes de clichés instantanés transportables. Dans ce cas, la communication de l’enregistreur-demandeur est quelque peu différente de ce qui est décrit ci-dessous. (Pour plus d’informations, consultez [importation de volumes de clichés instantanés transportables](importing-transportable-shadow-copied-volumes.md) .)

Pour ajouter des volumes au jeu de clichés instantanés, un demandeur doit d’abord définir le contexte de l’opération de cliché instantané en appelant [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext). Si cette méthode n’est pas appelée, le contexte par défaut des clichés instantanés, la \_ sauvegarde VSS CTX \_ , est utilisé. Pour plus d’informations sur la définition du contexte de cliché instantané, consultez [configurations du contexte](shadow-copy-context-configurations.md)de cliché instantané.

Pour commencer l’installation avant la sauvegarde, un demandeur doit appeler [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). En procédant ainsi, un demandeur indique aux rédacteurs :

-   Type de sauvegarde (tel que défini dans [**le \_ \_ type de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type))
-   Indique si la sauvegarde comprend un État du système de démarrage
-   Si le demandeur prend en charge la sélection de composants individuels ou sauvegarde des volumes entiers.

Tous les demandeurs participant à des opérations de sauvegarde et de restauration doivent toujours appeler [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Cette méthode initie la communication du demandeur de l’enregistreur en générant un événement d' [*identification*](vssgloss-i.md) VSS, en réponse à un enregistreur qui crée son document de métadonnées.

Avant d’appeler [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), un demandeur a la possibilité d’activer ou de désactiver explicitement certains Writers et classes d’enregistreur spécifiques à l’aide de [**IVssBackupComponents :: EnableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses), [**IVssBackupComponents ::D Isablewriterinstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)et [**IVssBackupComponents ::D isablewriterclasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (toutes les classes sont activées par défaut). Après l’appel de **IVssBackupComponents :: GatherWriterMetadata** , ces appels n’ont aucun effet.

Étant donné qu’il n’existe aucun moyen d’obtenir une liste d’enregistreurs sur le système avant d’appeler [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), les demandeurs peuvent envisager de créer, puis de supprimer une deuxième instance de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) pour obtenir la liste.

Il n’est pas nécessaire d’appeler [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) après l’achèvement de [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Les enregistreurs qui ne parviennent pas à traiter l’événement d' [*identification*](vssgloss-i.md) généré par les appels ne feront pas partie de la liste des enregistreurs qui fournissent des métadonnées trouvées par [**IVssBackupComponents :: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) et [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consultez Détermination de l’état de l' [enregistreur](determining-writer-status.md)).

## <a name="writer-actions-during-backup-initialization"></a>Actions d’écriture pendant l’initialisation de la sauvegarde

En réponse à l’événement d’identification, VSS appelle la méthode de gestionnaire virtuelle de chaque enregistreur, [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify). Un enregistreur crée son document de métadonnées d’écriture en substituant l’implémentation par défaut de **CVssWriter :: OnIdentify** et en utilisant l’interface [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) .

Notez que les applications autres que le demandeur actuel (par exemple, les applications système) peuvent générer des événements d’identification qui doivent être gérés par le writer. En outre, il n’existe aucun moyen pour un writer de déterminer à partir de [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) l’application qui a généré l’événement d’identification.

C’est le cas, étant donné qu’un enregistreur peut recevoir plusieurs événements d’identification lors du traitement d’une opération de sauvegarde, un enregistreur ne doit jamais définir d’informations d’État dans le gestionnaire [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

Au lieu de cela, [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) doit effectuer un algorithme cohérent pour créer le document de métadonnées de l’enregistreur du writer, en particulier parce qu’après qu’un enregistreur a créé le document, ni le demandeur ni le writer ne peuvent le modifier. À partir de ce point, il s’agit d’un document en lecture seule.

Cela signifie que le nombre et le type de [*composants*](vssgloss-c.md) associés à un writer, les fichiers faisant partie de chaque composant et l’exclusion explicite des fichiers des opérations de sauvegarde ou de restauration ne peuvent pas être modifiés après le retour d’un writer du traitement de l’événement d’identification.

Tous les enregistreurs participant à VSS sont tenus d’effectuer les opérations suivantes :

1.  Indiquez une méthode de restauration pour tous les composants gérés par le writer à l’aide de [**IVssCreateWriterMetadata :: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
2.  Ajoutez au moins un composant à l’aide de [**IVssCreateWriterMetadata :: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) (pour plus d’informations sur la spécification des composants, consultez [définition des composants par les enregistreurs](definition-of-components-by-writers.md) ).

Un enregistreur indique les fichiers à prendre en compte dans une opération de sauvegarde ou de restauration en ajoutant des [*jeux de fichiers*](vssgloss-f.md)(combinaison d’un chemin d’accès, d’une spécification de fichier et d’un indicateur de récurrence) à un composant donné à l’aide de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles), selon le type (consultez [Ajout de fichiers aux composants](definition-of-components-by-writers.md)).

Un enregistreur peut également avoir un ou plusieurs composants vides, les composants auxquels aucun fichier n’a été ajouté. Ils sont très utiles pour organiser les composants de l’enregistreur. (Consultez [chemin logique des composants](logical-pathing-of-components.md).)

Un enregistreur utilise [**IVssCreateWriterMetadata :: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) pour empêcher explicitement l’inclusion de fichiers dans la sauvegarde. Cette exclusion explicite est utile, car les caractères génériques peuvent être utilisés pour spécifier des fichiers à inclure (voir [exclure la spécification de liste de fichiers](writer-metadata-document-contents.md)). Notez que la liste des fichiers d’exclusion est prioritaire sur les listes de fichiers de composants.

[**IVssCreateWriterMetadata :: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) est utilisé pour créer des [*mappages d’emplacements de remplacement*](vssgloss-a.md) pour les jeux de fichiers spécifiés qui ont été ajoutés à l’un des composants du writer. Ces mappages sont utilisés lors de la restauration de fichiers lorsque la restauration à l’emplacement d’origine d’un fichier n’est pas possible ou souhaitable. (Consultez [vue d’ensemble de la restauration des fichiers réels](overview-of-actual-file-restoration.md) et des [emplacements de sauvegarde et de restauration non par défaut](non-default-backup-and-restore-locations.md).)

Étant donné que le jeu de fichiers de sauvegarde est spécifié dans le document de métadonnées de l’enregistreur, il ne peut pas être modifié ultérieurement. Par conséquent, un enregistreur doit être codé de sorte que la définition du jeu de fichiers inclue tous les fichiers nécessaires à la sauvegarde, soit par nom, soit par caractères génériques. Il peut s’agir d’un certain nombre de fichiers qui peuvent être créés après l’événement d’identification.

 

 



