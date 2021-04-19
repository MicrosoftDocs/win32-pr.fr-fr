---
description: 'Pour prendre en charge une opération de sauvegarde incrémentielle ou différentielle, un demandeur doit effectuer les opérations suivantes :'
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: Rôle demandeur dans VSS sauvegardes incrémentielles et différentielles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718a5a0b22d9cc1cfa31404b3a0ac71a3a07731f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524604"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>Rôle demandeur dans VSS sauvegardes incrémentielles et différentielles

Pour prendre en charge une opération de sauvegarde [*incrémentielle*](vssgloss-i.md) ou [*différentielle*](vssgloss-d.md) , un demandeur doit effectuer les opérations suivantes :

1.  Déterminez le degré de prise en charge du writer disponible (à l’aide de [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) pour accéder aux informations contenues dans les documents de métadonnées de l’enregistreur), en particulier, déterminez quel schéma de sauvegarde est pris en charge ([**\_ \_ schéma de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)).
2.  Définissez un état de sauvegarde approprié.
3.  Obtenez des spécifications de niveau de fichier et de jeu de fichiers pour une sauvegarde incrémentielle ou différentielle.
4.  Effectuez la sauvegarde.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Détermination du demandeur de la prise en charge incrémentielle et différentielle et de la configuration

Un demandeur doit obtenir des informations sur la prise en charge de l’enregistreur avant de sélectionner les composants à inclure dans une sauvegarde incrémentielle ou différentielle ou de définir son propre État.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Détermination de la prise en charge de l’enregistreur
</dt> <dd>

Un demandeur détermine si un writer donné prend en charge les sauvegardes incrémentielles ou différentielles VSS en extrayant le masque de schéma de sauvegarde du writer à l’aide de la méthode [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) .

Le masque de schéma de sauvegarde d’un enregistreur prenant en charge les techniques incrémentielles ou différentielles VSS contient soit **VSS \_ BS \_ incrémentiel** , soit **VSS \_ BS \_ différentiel**, ou les deux. Les rédacteurs peuvent également indiquer des restrictions quant à leur participation à l’indicateur **\_ \_ \_ \_ différentiel incrémentiel exclusif VSS BS** . (Pour plus d’informations sur les schémas de sauvegarde, consultez [**\_ \_ schéma de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) ).

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Définition de l’état de sauvegarde du demandeur
</dt> <dd>

Un demandeur indique qu’une sauvegarde est une sauvegarde incrémentielle ou différentielle en définissant un type de sauvegarde sur **VSS \_ BT \_ INCREMENTAL** ou **VSS \_ BT \_ Differential** à l’aide de la méthode [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) avant de générer un événement [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

La méthode [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) est également utilisée pour indiquer si le demandeur fournit une [*prise en charge partielle des fichiers*](vssgloss-p.md), qui est fréquemment utilisée pour implémenter certaines opérations de sauvegarde et de restauration incrémentielles.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Obtention de spécifications d’enregistreur pour les sauvegardes incrémentielles et différentielles

Les informations de spécification de sauvegarde de fichier au niveau du jeu de fichiers ([**\_ \_ \_ \_ type de sauvegarde spec de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) contenues dans le document de métadonnées d’écriture de chaque Writer peuvent être examinées après le retour réussi de [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Toutefois, un enregistreur peut ajouter des [*fichiers différenciés*](vssgloss-d.md) ou demander la [*prise en charge de fichiers partiels*](vssgloss-p.md) jusqu’à la réussite de la gestion de l’événement [*PostSnapshot*](vssgloss-p.md) .

La spécification de la prise en charge de fichiers et de fichiers partiels peut remplacer le type de sauvegarde de spécification de fichier. par conséquent, les demandeurs peuvent souhaiter reporter une analyse complète de toutes les spécifications de l’enregistreur sur les sauvegardes incrémentielles et différentielles jusqu’à la fin du retour de [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Obtention d’informations sur les spécifications de sauvegarde de fichiers
</dt> <dd>

Les informations de spécification de sauvegarde de fichier au niveau du jeu de fichiers ([**\_ \_ \_ \_ type de sauvegarde spec de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) sont contenues dans le document de métadonnées de l’enregistreur de chaque Writer et peuvent être examinées immédiatement après le retour réussi de [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Les demandeurs doivent obtenir les masques de spécification de sauvegarde de fichiers ([**\_ \_ \_ \_ type de sauvegarde spec de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) pour chaque jeu de fichiers de chacun des composants d’un enregistreur à inclure dans la sauvegarde incrémentielle ou différentielle, que le composant ait été ou non [*explicitement*](vssgloss-e.md) ou [*implicitement*](vssgloss-i.md) inclus.

Un demandeur peut déterminer le document de métadonnées de l’enregistreur des Writers à l’aide de [**IVssBackupComponents :: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) et [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). L’instance de l’interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retournée par **IVssBackupComponents :: GetWriterComponents** fournit les informations relatives au writer par le biais de la méthode [**IVssWriterComponentsExt :: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo) .

Le demandeur obtient des informations sur les composants par le biais d’instances de l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondant à un composant inclus géré par un writer donné à l’aide de [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

Les informations sur les jeux de fichiers gérés par le composant correspondant à l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) sont obtenues par des appels à [**IVssWMComponent :: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent :: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)ou [**IVssWMComponent :: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (selon le cas).

Ces appels peuvent retourner des instances de l’interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) pour chaque jeu de fichiers d’un composant.

Le type de sauvegarde de spécification de fichier d’un jeu de fichiers est obtenu en appelant [**IVssWMFiledesc :: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask).

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Obtention d’informations de fichier partielles et de fichiers différenciés
</dt> <dd>

Un demandeur obtient des informations de fichier partielles et des informations de fichier différenciées par le biais de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Un demandeur peut itérer au sein de tous les enregistreurs inclus dans une sauvegarde à l’aide de [**IVssBackupComponents :: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) et [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L’instance d’une interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retournée par [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) permet d’accéder à toutes les instances de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant aux composants [*explicitement inclus*](vssgloss-e.md) d’un writer donné via les méthodes [**IVssWriterComponentsExt :: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) et [**IVssWriterComponentsExt :: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) .

Un demandeur devra parcourir toutes les instances de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) pour tous les enregistreurs dont le schéma prend en charge la sauvegarde incrémentielle ou différentielle, c’est-à-dire les enregistreurs dont le masque de schéma de sauvegarde, tel qu’il est retourné par [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), intègre **VSS \_ BS \_ INCREMENTAL** lorsque le type de sauvegarde est VSS **\_ BT \_ INCREMENTAL**, ou **VSS \_ BS \_ Differential** lorsque le type de **sauvegarde est \_ \_**

Les informations de fichier partielles sont obtenues en appelant [**IVssComponent :: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) et [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (consultez [utilisation de fichiers partiels](working-with-partial-files.md)).

Pour les writers qui prennent en charge les opérations de sauvegarde sur la base des données de la dernière modification d’un fichier (les enregistreurs dont le masque de schéma de la sauvegarde est retourné par [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), y compris **VSS \_ BS \_ dernière \_ modification**), les informations de fichier différenciées sont obtenues en appelant [**IVssComponent :: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) et [**IVssComponent :: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile).

Notez que les fichiers différenciés peuvent être de nouveaux fichiers, c’est-à-dire des fichiers qui ne sont pas membres d’un ensemble de fichiers actuellement dans le document de métadonnées d’écriture d’un writer donné.

Les demandeurs ne doivent pas trouver les fichiers inclus à la fois pour les opérations de fichier partiels et comme fichiers différenciés. Si un demandeur rencontre ce type de situation, il doit retourner et enregistrer une erreur d’écriture.

Un demandeur peut toujours choisir de procéder à la sauvegarde des fichiers du générateur de problèmes, mais dans ce cas, il doit le faire en fonction de la spécification figurant dans les informations de fichier différenciées.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Implémentation de sauvegardes incrémentielles ou différentielles

Avant d’implémenter une sauvegarde, les demandeurs doivent avoir des informations sur les auteurs qui prennent en charge une sauvegarde [*incrémentielle*](vssgloss-i.md) ou [*différentielle*](vssgloss-d.md) , toutes les opérations de fichiers partielles demandées, tous les fichiers différenciés et le type de sauvegarde de spécification de fichiers de tous les autres fichiers.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Writers non pris en charge
</dt> <dd>

Les enregistreurs dont le schéma ne prend pas en charge la sauvegarde incrémentielle ou différentielle (les enregistreurs dont le masque de schéma de la sauvegarde est retourné par [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), incluent **VSS \_ BS \_ INCREMENTAL** lorsque le type de sauvegarde est **VSS \_ BT \_ INCREMENTAL** ou n’incluent pas la **\_ \_ différence VSS BS** lorsque le type de sauvegarde est **VSS \_ BS \_ Differential**) ne peuvent pas fournir de support

Cela ne signifie pas nécessairement que les données des enregistreurs ne seront pas impliquées dans une opération de sauvegarde incrémentielle ou différentielle. Toutefois, le choix de ce que vous devez faire est à la discrétion du demandeur. Le demandeur peut effectuer l’une des opérations suivantes :

-   Sauvegarder aucun fichier appartenant aux enregistreurs non pris en charge (l’indique clairement à l’utilisateur)
-   Sauvegarder tous les fichiers des enregistreurs non pris en charge
-   Effectuez une sauvegarde incrémentielle à l’aide des données du système de fichiers et des journaux d’historique de ce demandeur.

La dernière alternative doit être utilisée avec une grande prudence et uniquement si le demandeur comprend si les rédacteurs impliqués peuvent prendre en charge la sauvegarde incrémentielle ou différentielle et la restauration de données indépendantes du mécanisme VSS.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Writers de prise en charge
</dt> <dd>

Un demandeur doit traiter (dans l’ordre) tous les [*fichiers différenciés*](vssgloss-d.md)d’un enregistreur, puis gérer les demandes de [*fichiers partielles*](vssgloss-p.md) , puis sauvegarder les fichiers restants en fonction de leur type de sauvegarde (spécification de fichier [**VSS \_ \_ \_ \_ type de sauvegarde**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

1.  **Sauvegarde des fichiers différenciés :**

    Pour les enregistreurs qui prennent en charge les opérations de sauvegarde sur la base des données de la dernière modification (les Writers dont le masque de schéma de sauvegarde est retourné par [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), y compris **VSS \_ BS \_ dernière \_ modification**), un demandeur utilise le chemin d’accès, la spécification de fichier et les informations d’indicateur de récurrence retournées par [**IVssComponent :**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

    [**IVssComponent :: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) peut également retourner l’heure de la dernière modification (exprimée sous la forme d’une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) ).

    Si l’heure de la dernière modification fournie par le writer est différente de zéro, le demandeur l’utilise comme base (plutôt que les informations du système de fichiers ou les données stockées du demandeur) pour déterminer si le fichier doit être inclus dans la sauvegarde [*incrémentielle*](vssgloss-i.md) ou [*différentielle*](vssgloss-d.md) .

    Par exemple, si l’heure de la dernière modification d’un fichier telle qu’elle est retournée par le writer était :

    -   Après la dernière sauvegarde complète, le fichier doit être inclus à la fois dans les sauvegardes incrémentielles et les sauvegardes différentielles.
    -   Après la dernière sauvegarde complète, mais avant la dernière sauvegarde incrémentielle, le fichier doit être inclus dans les opérations de sauvegarde incrémentielle, mais pas pour les sauvegardes différentielles.

    Si l’heure de la dernière modification fournie par le writer est égale à zéro, le demandeur doit utiliser les informations du système de fichiers et ses propres données stockées pour déterminer l’heure de modification du fichier différent.

2.  **Utilisation d’opérations de fichiers partielles :**

    Si un enregistreur a demandé qu’un fichier soit sauvegardé à l’aide d’une opération de fichier partielle, le demandeur utilise les informations de décalage de fichier pour enregistrer les segments de fichier indiqués sur le support de sauvegarde. (Pour plus d’informations sur les opérations de fichiers partielles, consultez [utilisation de fichiers partiels](working-with-partial-files.md) ).

    Comme indiqué ci-dessus, un enregistreur ne doit pas désigner un fichier à la fois comme un fichier différent et comme participant dans une opération de fichier partielle. Si un demandeur rencontre ce type de situation, il doit retourner et enregistrer une erreur d’écriture.

    Un demandeur peut toujours choisir de procéder à la sauvegarde des fichiers du générateur de problèmes, mais dans ce cas, il doit le faire en fonction de la spécification figurant dans les informations de fichier différenciées.

3.  **Utilisation du type de sauvegarde spécification de fichier :**

    Après avoir traité tous les fichiers différenciés et les opérations de fichiers partiels, le demandeur traite désormais tous les fichiers restants dans son jeu de sauvegarde en fonction de leur type de sauvegarde de spécification de fichier ([**\_ \_ \_ \_ type de sauvegarde spec de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Trois valeurs « Backup required » de l’énumération du [**\_ \_ \_ \_ type de sauvegarde spec du fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) affectent les sauvegardes différentielles et incrémentielles :

    -   \_sauvegarde VSS FSBT \_ toutes les \_ sauvegardes \_ requises
    -   \_sauvegarde VSS FSBT \_ \_ \_ requise
    -   \_ \_ sauvegarde différentielle FSBT \_ VSS \_ requise

    Il existe trois valeurs « cliché instantané requis » :

    -   \_FSBT VSS \_ tous les \_ instantanés \_ requis
    -   \_instantané FSBT \_ incrémentiel VSS \_ \_ requis
    -   \_ \_ instantané différentiel FSBT \_ VSS \_ requis

    Jeux de fichiers marqués avec un type de sauvegarde de spécification de fichier « cliché instantané requis » indique qu’un demandeur doit copier des données à partir d’un cliché instantané lors de l’exécution d’opérations de sauvegarde incrémentielle, différentielle ou tout (qui incluent à la fois des opérations incrémentielles et différentielles).

    L’indicateur « Backup required », appliqué aux opérations INCRÉMENTIELLEs, DIFFÉRENTIELles ou de sauvegarde, indique que le writer attend qu’une copie de la version actuelle du jeu de fichiers soit disponible après la restauration d’une opération de sauvegarde. En général, cela signifie que si un jeu de fichiers est marqué avec « Backup required », un demandeur copie tous ses membres sur le support de sauvegarde lors d’une sauvegarde incrémentielle ou différentielle, quelle que soit la date de la dernière sauvegarde ou modification.

    Par défaut, les jeux de fichiers sont ajoutés aux composants avec un type de sauvegarde de spécification de fichier VSS \_ FSBT \_ toutes les \_ sauvegardes \_ nécessaires \| VSS \_ FSBT \_ tous les \_ instantanés \_ requis. Par conséquent, à moins qu’un enregistreur ne définisse explicitement le type de sauvegarde spécification de fichier dans le cas contraire, les demandeurs doivent copier les fichiers qui ne sont pas gérés par les opérations de fichiers partiels ou les fichiers désignés désignés dans la plupart des jeux de fichiers sont généralement copiés dans leur intégralité sur le support de sauvegarde.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Tampons de sauvegarde
</dt> <dd>

Les enregistreurs qui prennent en charge les tampons de sauvegarde ( \_ horodatage VSS BS \_ ) peuvent choisir de générer des informations de tampon de sauvegarde à utiliser pour prendre en charge les futures opérations de sauvegarde et de restauration incrémentielles et différentielles.

Le format et les informations contenues dans des chaînes contenant des informations de tampon de sauvegarde sont privés pour l’enregistreur qui les génère ; le demandeur ne sait pas comment traiter ces informations.

Les auteurs de la prise en charge stockent le tampon de sauvegarde dans le document des composants de sauvegarde sous forme de chaîne à l’aide de la méthode [**IVssComponent :: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) .

Le rôle du demandeur dans la gestion des informations de tampon de sauvegarde est (s’il existe) de le rendre disponible pour le writer en appelant [**IVssBackupComponents :: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) dans une opération de sauvegarde ou de restauration ultérieure.

</dd> </dl>

 

 
