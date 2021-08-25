---
description: 'La participation d’un enregistreur à des sauvegardes incrémentielles et différentielles s’effectue généralement lors du traitement des événements identify (CVssWriter :: OnIdentify), PrepareForBackup (CVssWriter : OnPrepareBackup) et PostSnapshot (CVssWriter : OnPostSnapshot).'
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Rôle d’écriture dans VSS sauvegardes incrémentielles et différentielles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3c84245c21a47ba5535eccdfcbf10e988cf72b30ea99ee92086a9ca8f65647
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863869"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Rôle d’écriture dans VSS sauvegardes incrémentielles et différentielles

La participation d’un enregistreur à des sauvegardes incrémentielles et différentielles s’effectue généralement lors du traitement des événements [*identify*](vssgloss-i.md) ([**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)), [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter : OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) et *PostSnapshot* (CVssWriter [**: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)). Le mode de participation d’un writer est formé par le fait qu’il prenne en charge les tampons de sauvegarde et les heures de dernière modification, et si le demandeur qui exécute la sauvegarde prend en charge les [*opérations de fichiers partielles*](vssgloss-p.md).

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Gestion des événements d’identification lors des sauvegardes incrémentielles et différentielles

Lors du traitement de l’événement d’identification, les rédacteurs établissent leur architecture de base pour l’opération de sauvegarde incrémentielle et différentielle par le biais des masques schéma de sauvegarde ([**\_ \_ schéma de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) et spécification de fichier ([**\_ \_ \_ \_ type**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)de sauvegarde de spécification de fichier VSS).

Un writer indique les opérations qu’il prend en charge dans son document de métadonnées d’écriture en créant un masque de bits des valeurs de [**\_ \_ schéma de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) et en le passant à la méthode [**IVssCreateWriterMetadata :: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) . Dans ce cas, un enregistreur peut indiquer s’il prend en charge les éléments suivants :

-   Sauvegardes incrémentielles (**VSS \_ BS \_ incrémentielles**)
-   Sauvegardes différentielles (**VSS \_ BS \_ différentiel**)
-   Les sauvegardes incrémentielles et différentielles ne peuvent pas être mélangées (**\_ différentielle VSS BS \_ exclusive \_ incrémentielle \_**)
-   Sauvegardes incrémentielles et différentielles à l’aide de tampons de sauvegarde (**VSS \_ BS \_ horodaté**)
-   Sauvegardes incrémentielles et différentielles sur la base des informations sur la dernière modification d’un fichier (**VSS \_ BS \_ dernière \_ modification**)

Les enregistreurs utilisent le masque de type de sauvegarde spécification de fichier pour fournir des informations au niveau du jeu de fichiers aux demandeurs sur l’inclusion de fichiers dans une sauvegarde incrémentielle ou différentielle.

Un enregistreur peut définir le masque de type de sauvegarde d’une spécification de fichier d’un jeu de fichiers lorsqu’il ajoute le jeu de fichiers à un composant en créant un masque de bits des valeurs de [**\_ \_ \_ \_ type de sauvegarde spec de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) et en le passant à [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup).

Trois valeurs « Backup required » de l’énumération du [**\_ \_ \_ \_ type de sauvegarde spec du fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) affectent les sauvegardes différentielles et incrémentielles :

-   **\_sauvegarde VSS FSBT \_ toutes les \_ sauvegardes \_ requises**
-   **\_sauvegarde VSS FSBT \_ \_ \_ requise**
-   **\_ \_ sauvegarde différentielle FSBT \_ VSS \_ requise**

Il existe trois valeurs « cliché instantané requis » :

-   **\_FSBT VSS \_ tous les \_ instantanés \_ requis**
-   **\_instantané FSBT \_ incrémentiel VSS \_ \_ requis**
-   **\_ \_ instantané différentiel FSBT \_ VSS \_ requis**

Jeux de fichiers marqués avec un type de sauvegarde de spécification de fichier « cliché instantané requis » indiquez si un demandeur doit copier des données à partir d’un cliché instantané lors de l’exécution d’opérations de sauvegarde incrémentielle, différentielle ou tout (qui incluent à la fois des opérations incrémentielles et différentielles).

L’indicateur « Backup required », appliqué aux opérations INCRÉMENTIELLEs, DIFFÉRENTIELles ou de sauvegarde, indique que le writer attend qu’une copie de la version actuelle du jeu de fichiers soit disponible après la restauration d’une opération de sauvegarde. En général, cela signifie que si un jeu de fichiers est marqué avec « Backup required », tous ses membres sont copiés sur le support de sauvegarde lors d’une sauvegarde incrémentielle ou différentielle, quel que soit le moment de la dernière sauvegarde ou modification.

Par défaut, les jeux de fichiers sont ajoutés aux composants avec un type de sauvegarde de spécification de fichier **VSS \_ FSBT \_ toutes les \_ sauvegardes \_ nécessaires** \| **VSS \_ FSBT \_ tous les \_ instantanés \_ requis**. Par conséquent, à moins qu’un développeur auteur ne décide de ne pas utiliser la valeur par défaut (en choisissant un autre type de sauvegarde de spécification de fichier, en utilisant des opérations de fichiers partielles ou en utilisant des fichiers différenciés), les fichiers de la plupart des jeux de fichiers sont généralement copiés dans leur intégralité sur le support de sauvegarde.

À ce stade, le document de métadonnées de l’enregistreur du writer est entièrement rempli avec la plupart des informations dont un demandeur aura besoin pour démarrer une sauvegarde différentielle ou incrémentielle. La spécification de l’ajout d’informations sur le jeu de fichiers ou le niveau de fichier pour prendre en charge la sauvegarde sera gérée pendant l’événement [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Gestion des événements PrepareForBackup lors des sauvegardes incrémentielles et différentielles

Avant de poursuivre l’opération de sauvegarde réelle, les rédacteurs peuvent modifier la spécification d’une sauvegarde [*incrémentielle*](vssgloss-i.md) ou [*différentielle*](vssgloss-d.md) en modifiant le document des composants de sauvegarde du demandeur par le biais de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Étant donné que les enregistreurs utilisent l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , ils effectuent généralement ces préparatifs tout en gérant l’événement [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

Dans [**CVssWriter : OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), les enregistreurs peuvent spécifier plus précisément la manière dont certains fichiers doivent être évalués pour la sauvegarde, spécifier les mécanismes à utiliser pour les sauvegarder et éventuellement définir des tampons de sauvegarde.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>Fichiers partiels
</dt> <dd>

Si un demandeur les prend en charge, un enregistreur peut choisir d’implémenter une sauvegarde incrémentielle ou différentielle en utilisant des opérations de fichier partielles. (Les enregistreurs peuvent déterminer si un demandeur prend en charge les opérations de fichiers partielles en appelant [**CVssWriter :: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled).)

Les enregistreurs utilisent [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) pour indiquer les portions des fichiers sélectionnés à sauvegarder pendant l’opération incrémentielle ou différentielle. Les demandeurs doivent respecter cette spécification et doivent toujours sauvegarder les sections spécifiées des fichiers. (Pour plus d’informations sur les opérations de fichiers partielles, consultez [utilisation de fichiers partiels](working-with-partial-files.md) .)

À l’aide de [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile), un enregistreur peut ajouter un fichier à la sauvegarde qui n’a pas été précédemment ajouté à l’un de ses jeux de composants (par [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) en tant que fichier partiel. Les nouveaux fichiers ajoutés à la sauvegarde de cette manière doivent se trouver sur un volume qui est déjà en cours de clichés instantanés pour cette sauvegarde.

Si un fichier est impliqué dans des opérations de fichiers partielles, cela remplace n’importe quel type de sauvegarde de spécification de fichier, ce qui est ignoré.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>Fichiers différenciés
</dt> <dd>

Les writers qui prennent en charge un schéma de sauvegarde de dernière modification (**\_ \_ schéma VSS BS**) peuvent ajouter des [*fichiers différenciés*](vssgloss-d.md) à une sauvegarde incrémentielle ou différentielle.

En spécifiant un fichier différent, un writer utilise [**IVssComponent :: AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) et spécifie un chemin d’accès, un nom de fichier et un indicateur récursif ; Toutefois, ceux-ci ne doivent pas nécessairement correspondre à un jeu de fichiers inclus dans un composant.

En fait, un enregistreur peut ajouter un fichier qui n’a pas été précédemment ajouté à l’un de ses jeux de composants (par [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) à la sauvegarde sous la forme d’un fichier différent. Les nouveaux fichiers ajoutés à la sauvegarde de cette manière doivent se trouver sur un volume qui est déjà en cours de clichés instantanés pour cette sauvegarde.

En règle générale, un enregistreur spécifie également l’heure de la dernière modification lors de l’ajout d’un fichier différent, en fonction du mécanisme d’historique propre à l’enregistreur. L’heure de la dernière modification, si elle est spécifiée, doit toujours être utilisée par les demandeurs pour déterminer si un fichier doit être inclus dans une sauvegarde incrémentielle ou différentielle.

Un enregistreur peut choisir de ne pas spécifier l’heure de la dernière modification lors de l’ajout d’un fichier différent à un jeu de sauvegarde différentiel ou incrémentiel. Si c’est le cas, les demandeurs sont libres d’utiliser leurs propres mécanismes (par exemple, les journaux de sauvegardes précédentes ou d’informations de système de fichiers) pour déterminer si le fichier différent doit être inclus dans une sauvegarde incrémentielle ou différentielle.

Le type de sauvegarde de spécification de fichier d’un fichier différent est ignoré.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Tampons de sauvegarde
</dt> <dd>

Les enregistreurs qui prennent en charge les tampons de sauvegarde (**\_ \_ horodatage VSS BS**) ont leur propre format privé pour stocker des informations sur le moment où une sauvegarde s’est produite en dernier. Ces informations sont générées par le writer lors de la sauvegarde.

Le tampon de sauvegarde est stocké dans le document des composants de sauvegarde sous forme de chaîne par la méthode [**IVssComponent :: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) . Le tampon de sauvegarde s’applique à tous les jeux de fichiers du composant (ou jeu de composants) correspondant à l’instance du [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Si un demandeur a accès au tampon de sauvegarde d’une sauvegarde précédente, il l’aura mis à la disposition du rédacteur en appelant [**IVssBackupComponents :: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp).

Un enregistreur peut ensuite examiner cet horodatage à l’aide de [**IVssComponent :: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).

Notez que le demandeur stocke simplement et retourne la chaîne contenant le tampon de sauvegarde. Il ne sait rien sur le format de la chaîne ni sur son utilisation ; seul l’enregistreur a ces informations.

Un enregistreur peut choisir de mettre à jour le tampon de sauvegarde actuel à l’aide de [**IVssComponent :: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) après avoir appelé [**IVssComponent :: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp), enregistrant ainsi dans son propre format la date de l’opération de sauvegarde incrémentielle ou différentielle actuelle.

</dd> </dl>

 

 



