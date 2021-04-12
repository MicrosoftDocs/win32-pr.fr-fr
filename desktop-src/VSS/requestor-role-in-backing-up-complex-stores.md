---
description: Comme avec toutes les opérations importantes sous VSS, les sauvegardes incrémentielles et différentielles requièrent une coopération étroite entre les demandeurs et les rédacteurs.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Rôle demandeur dans la sauvegarde de magasins complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197351e76b6861ee9b9d1e0589ef028c911430ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034342"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Rôle demandeur dans la sauvegarde de magasins complexes

Comme avec toutes les opérations importantes sous VSS, les sauvegardes [*incrémentielles*](vssgloss-i.md) et [*différentielles*](vssgloss-d.md) requièrent une coopération étroite entre les demandeurs et les rédacteurs.

## <a name="backup-type"></a>Type de sauvegarde

L’infrastructure fournit une prise en charge spéciale de cinq types de sauvegardes. En voici le détail :

-   Full (**VSS \_ BT \_ complet**). Les fichiers seront sauvegardés quelle que soit leur date de dernière sauvegarde. L’historique de sauvegarde de chaque fichier est mis à jour, et ce type de sauvegarde peut être utilisé comme base d’une sauvegarde incrémentielle ou différentielle. Si des fichiers journaux sont présents, ils peuvent être tronqués à la suite de cette sauvegarde.

    La restauration d’une sauvegarde complète nécessite une seule image de sauvegarde.

-   Différentielle (**\_ \_ différentielle BT VSS**). L’API VSS est utilisée pour s’assurer que seuls les fichiers qui ont été modifiés ou ajoutés depuis la dernière sauvegarde complète doivent être copiés sur un support de stockage. toutes les informations de sauvegarde intermédiaires sont ignorées. Cela peut inclure des fichiers entiers ou des plages spécifiques dans des fichiers. Une sauvegarde différentielle est associée à une sauvegarde complète et ne peut généralement pas être restaurée tant que la sauvegarde complète n’a pas été restaurée. Si des fichiers journaux sont présents, ils ne sont généralement pas tronqués à la suite de cette sauvegarde.

    La restauration d’une sauvegarde différentielle nécessite l’image de sauvegarde d’origine et l’image de sauvegarde différentielle la plus récente effectuée depuis la dernière sauvegarde complète.

-   Incrémentiel (**VSS \_ BT \_ incrémentiel**). L’API VSS est utilisée pour s’assurer que seuls les fichiers qui ont été modifiés ou ajoutés depuis la dernière sauvegarde complète ou incrémentielle doivent être copiés sur un support de stockage. Cela peut inclure des fichiers entiers ou des plages spécifiques dans des fichiers. Certains enregistreurs n’autorisent pas le mélange des sauvegardes incrémentielles avec les sauvegardes différentielles. Si des fichiers journaux sont présents, ils peuvent être tronqués à la suite de cette sauvegarde.

    La restauration d’une sauvegarde incrémentielle nécessite l’image de sauvegarde d’origine et toutes les images de sauvegarde incrémentielles effectuées depuis la sauvegarde initiale.

-   Sauvegarde de fichier journal (**\_ \_ Journal BT VSS**). Seuls les fichiers journaux d’un enregistreur (fichiers ajoutés à un composant avec la méthode [**IVssCreateWriterMetadata :: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) et récupérés par un appel à [**IVssWMComponent :: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) sont sauvegardés. Ce type de sauvegarde est spécifique à VSS. Les sauvegardes de fichier journal ont tendance à être effectuées très souvent. En règle générale, le fichier journal est tronqué à la suite de cette sauvegarde.
-   Copie de sauvegarde **( \_ \_ copie de VSS BT**). À l’instar du \_ \_ type de sauvegarde complète VSS BT, les fichiers sont sauvegardés quelle que soit leur date de dernière sauvegarde. Toutefois, l’historique de sauvegarde de chaque fichier n’est pas mis à jour et ce type de sauvegarde ne peut pas être utilisé comme base d’une sauvegarde incrémentielle ou différentielle. Les fichiers journaux ne doivent jamais être tronqués à la suite d’une sauvegarde de copie.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Prise en charge partielle des fichiers
</dt> <dd>

Certains enregistreurs prennent en charge la restauration de fichiers par le biais du remplacement des parties des fichiers qu’ils gèrent. Un demandeur peut être conçu pour tirer parti de cela et, si tel est le cas, il indique cela en définissant les informations dans [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

Le demandeur spécifie le type de sauvegarde en cours d’exécution par le biais du paramètre *backupType* de [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Différents rédacteurs prennent en charge différents types de sauvegardes. Après l’appel de [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , le demandeur peut déterminer les types de sauvegarde pris en charge par un writer donné en appelant [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). La valeur retournée est un masque de bits indiquant la prise en charge de différents types de sauvegarde. Service **VSS \_ BS \_ Differential** indique la prise en charge des sauvegardes différentielles, **VSS \_ BS \_ incrémentielle** pour les sauvegardes incrémentielles, le **\_ \_ Journal VSS BS** pour les sauvegardes de journaux et la **\_ \_ copie VSS BS** pour les sauvegardes de copie ; tous les enregistreurs doivent prendre en charge les sauvegardes complètes. Si un enregistreur ne prend pas en charge la combinaison de sauvegardes incrémentielles avec des sauvegardes différentielles, l’indicateur **\_ \_ \_ \_ différentiel incrémentiel exclusif VSS BS** est également ajouté. Si le demandeur effectue une sauvegarde incrémentielle ou différentielle et qu’un writer donné ne prend pas en charge ce type de sauvegarde, une sauvegarde complète doit être effectuée sur ce writer.

## <a name="backup-stamps"></a>Tampons de sauvegarde

Les sauvegardes incrémentielles et différentielles sont toujours liées à une sauvegarde précédente. Il existe deux façons de lier des sauvegardes. Pour les magasins de données simples, le demandeur peut effectuer le suivi de la corrélation entre les sauvegardes. Toutefois, pour les magasins de données plus complexes, l’enregistreur doit conserver son propre horodatage avec la sauvegarde. cet horodateur peut assurer le suivi de la position du journal, des informations de point de contrôle, etc. Le demandeur peut déterminer si un writer donné doit stocker son propre horodateur en vérifiant le bit **VSS \_ BS \_ horodaté** dans la valeur retournée par [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

Les enregistreurs qui stockent un horodateur dans une sauvegarde ajoutent l’horodateur lors du traitement de [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou lors du traitement de [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Le demandeur peut obtenir cet horodateur en appelant [**IVssComponent :: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp). Lorsque vous effectuez une sauvegarde incrémentielle ou différentielle, le demandeur doit lier la sauvegarde actuelle à une sauvegarde précédente. Pour ce faire, vous obtenez l’horodateur de la sauvegarde précédente d’un composant spécifique et le transmettez à la fonction [**IVssBackupComponents :: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) ; Cela doit être fait pour chaque composant qui a été sauvegardé dans la sauvegarde précédente.

## <a name="backing-up-files"></a>Sauvegarde des fichiers

### <a name="backing-up-files-reported-by-writer"></a>Sauvegarde des fichiers signalés par le writer

Chaque spécification de fichier qu’un enregistreur ajoute à ses métadonnées pendant la phase GatherWriterMetadata contient un masque de type de sauvegarde qui spécifie le moment où le fichier doit être sauvegardé. Le demandeur détermine ce qu’est le masque en appelant [**IVssWMFiledesc :: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask). Les valeurs de ce masque sont utilisées pour déterminer pour quels types de sauvegarde la spécification de fichier doit être sauvegardée. Le masque peut contenir une ou plusieurs des valeurs de bit suivantes :

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**\_ \_ sauvegarde complète VSS \_ FSBT \_ requise**
</dt> <dd>

Requis pour les sauvegardes complètes.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**\_ \_ sauvegarde différentielle FSBT \_ VSS \_ requise**
</dt> <dd>

Requis pour les sauvegardes différentielles.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**\_sauvegarde VSS FSBT \_ \_ \_ requise**
</dt> <dd>

Requis pour les sauvegardes incrémentielles.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**\_sauvegarde du \_ Journal FSBT VSS \_ \_ requise**
</dt> <dd>

Requis pour les sauvegardes de fichiers journaux.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**\_sauvegarde VSS FSBT \_ toutes les \_ sauvegardes \_ requises**
</dt> <dd>

Obligatoire pour tous les types de sauvegardes ; Il s’agit de la valeur par défaut.

</dd> </dl>

Cette spécification remplace la spécification de sélectivité du composant. Par exemple, imaginez un composant dont les fichiers sont tous marqués avec la **\_ sauvegarde de \_ fichier journal VSS FSBT \_ \_ obligatoire** , mais pas avec la **\_ \_ sauvegarde complète VSS FSBT \_ \_ requise**. Supposons que ce composant ne peut pas être sélectionné pour la sauvegarde (*bSelectable* a la valeur false lorsque [**IVssCreateWriterMetadata :: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) a été appelé). Dans le cas d’une sauvegarde de fichier journal, cela signifie que tous les fichiers de ce composant doivent toujours être sauvegardés. Toutefois, dans le cas d’une sauvegarde complète, aucun des fichiers ne doit être sauvegardé, bien que le fait que la sélectivité du composant indique qu’il doit être sauvegardé.

### <a name="backup-by-last-modify-time"></a>Sauvegarde par heure de la dernière modification

Les informations de spécification de fichier spécifiées dans la phase [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) ne fournissent pas d’informations sur le demandeur sur ce qui a changé depuis la dernière sauvegarde. L’un des moyens pour un enregistreur d’indiquer des modifications au demandeur est d’utiliser le mécanisme de fichier différent. Un enregistreur peut spécifier que certains fichiers d’un composant doivent être sauvegardés uniquement s’ils ont été modifiés depuis un certain temps ; l’enregistreur peut spécifier ces fichiers dans [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou dans [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un demandeur peut déterminer ces fichiers en appelant [**IVssComponent :: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) et [**IVssComponent :: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Si la spécification de fichier correspond à un jeu dans **IVssBackupComponents :: GatherWriterMetadata** (qui est actuellement valide en fonction du masque de type de sauvegarde), les informations de fichier différenciées remplacent les informations précédentes. autrement dit, les fichiers correspondant à cette spécification de fichier sont désormais sauvegardés uniquement s’ils ont été modifiés depuis l’heure spécifiée. L’heure de la dernière modification est communiquée à l’aide d’une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Si la valeur de cette structure est égale à zéro, cela signifie que l’heure de la dernière modification doit être déterminée en fonction de l’enregistrement du demandeur de l’heure de la dernière sauvegarde.

### <a name="partial-file-backup"></a>Sauvegarde de fichiers partielle

Une autre façon pour un enregistreur d’indiquer des modifications au demandeur consiste à utiliser le mécanisme de fichier partiel. Un enregistreur peut spécifier des plages d’octets dans des fichiers de composants qui doivent être sauvegardés ; l’enregistreur peut spécifier ces plages de fichiers dans [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou dans [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un demandeur peut déterminer ces fichiers en appelant [**IVssComponent :: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) et [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). **IVssComponent :: GetPartialFile** retourne un chemin d’accès et un nom de fichier pointant vers le fichier, et une chaîne de plages indiquant ce qui doit être sauvegardé dans le fichier. Comme avec les fichiers différenciés, si le chemin d’accès et le nom de fichier correspondent à une spécification de fichier définie par le writer dans [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), les informations de fichier partiel remplacent le paramètre précédent. La chaîne de plages peut avoir deux formats : elle peut soit spécifier les plages directement, soit spécifier un fichier contenant des informations sur les plages. Si vous spécifiez des plages directement, la syntaxe est une liste séparée par des virgules sous la forme offset1 : length1, offset2 : length2, où chaque décalage et longueur est un entier non signé 64 bits. Si vous spécifiez un fichier de plages, la chaîne de plages doit être définie sur file = *filename*, où *filename* est le chemin d’accès complet au fichier de plages. Le fichier de plages lui-même est un fichier binaire qui est mis en forme en tant que liste d’entiers non signés 64 bits. Le premier entier indique le nombre de plages qui sont représentées dans le fichier. Chaque paire d’entiers suivante représente le décalage et la longueur d’une plage. Le demandeur doit également s’occuper de sauvegarder et de restaurer ce fichier de plages.

### <a name="file-specification-rules"></a>Règles de spécification de fichier

Les spécifications de fichier ajoutées par le biais du fichier de différences et des mécanismes de fichiers partiels modifient les spécifications de fichier définies dans [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) ou ajoutent des fichiers entièrement nouveaux. Si vous modifiez les spécifications de fichiers définies dans **IVssBackupComponents :: GatherWriterMetadata** à l’aide du mécanisme de fichier partiel, un demandeur peut s’attendre à ce que la spécification de fichier corresponde exactement à l’une des spécifications de fichier définies dans le composant dans **IVssBackupComponents :: GatherWriterMetadata**. La spécification de fichier ne chevauche pas partiellement une autre spécification de fichier et ne correspond à aucune spécification de fichier dans les composants de ce writer. Les spécifications de fichiers ajoutées à l’aide du mécanisme de fichier partiel peuvent, toutefois, chevaucher partiellement une autre spécification de fichier. Lorsque la valeur est true, la spécification du fichier de différences ou du fichier partiel remplace la spécification définie dans **IVssBackupComponents :: GatherWriterMetadata**. Les spécifications de fichier générales peuvent avoir une valeur d’emplacement secondaire (retournée par [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) qui indique un autre emplacement à partir duquel obtenir le fichier au moment de la sauvegarde. Si les spécifications de fichier définies à l’aide des mécanismes de fichier de différences ou de fichiers partiels correspondent à une spécification de fichiers existante qui a un autre emplacement, les données doivent être récupérées à partir de cet autre emplacement. Si les spécifications de fichier définies à l’aide des mécanismes de fichier de différences ou de fichiers partiels ne correspondent pas à des spécifications existantes pour le composant, ces plages de fichiers doivent maintenant être ajoutées à la sauvegarde. Le demandeur peut s’attendre à ce que seuls les fichiers sur les volumes qui ont déjà été inclus dans le jeu de clichés instantanés soient ajoutés à l’aide de l’un de ces mécanismes.

### <a name="backup-without-a-shadow-copy"></a>Sauvegarde sans cliché instantané

Certains types de fichiers n’ont peut-être pas besoin d’être sauvegardés sur un volume de clichés instantanés. Par exemple, cela est souvent vrai pour les fichiers journaux de base de données. Étant donné que les fichiers journaux augmentent de manière monotone, et qu’un enregistreur peut spécifier exactement les portions du fichier à sauvegarder à l’aide de fichiers partiels, il est souvent possible de sauvegarder la journalisation du volume d’origine. En guise d’optimisation, un enregistreur peut marquer les fichiers qui nécessitent des clichés instantanés pour différents types de sauvegardes à l’aide du masque de type de sauvegarde. La valeur retournée par [**IVssWMFiledesc :: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) peut contenir une ou plusieurs des valeurs de bit suivantes :

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**\_ \_ instantané complet VSS \_ FSBT \_ requis**
</dt> <dd>

Cliché instantané requis pour les sauvegardes complètes.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**\_ \_ instantané différentiel FSBT \_ VSS \_ requis**
</dt> <dd>

Cliché instantané requis pour les sauvegardes différentielles.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**\_instantané FSBT \_ incrémentiel VSS \_ \_ requis**
</dt> <dd>

Cliché instantané requis pour les sauvegardes incrémentielles.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**\_instantané de \_ Journal FSBT VSS \_ \_ requis**
</dt> <dd>

Cliché instantané requis pour les sauvegardes de fichiers journaux.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**\_FSBT VSS \_ tous les \_ instantanés \_ requis**
</dt> <dd>

Cliché instantané requis pour tous les types de sauvegardes ; Il s’agit de la valeur par défaut.

</dd> </dl>

Si un volume spécifique contient uniquement des composants qui ne nécessitent pas de cliché instantané pour cette sauvegarde, le demandeur peut ignorer l’étape de création d’un cliché instantané pour ce volume. Toutes les données de ce volume peuvent être copiées sur le support de sauvegarde directement à partir du volume d’origine.

## <a name="restoring-files"></a>Restauration de fichiers

### <a name="sequential-restores"></a>Restaurations séquentielles

Une fois que le demandeur a effectué une opération de restauration, il envoie l’événement PostRestore à tous les enregistreurs. En règle générale, les enregistreurs gèrent cet événement en effectuant des opérations de récupération ou autres opérations consécutives à la restauration. La restauration des sauvegardes incrémentielles, cependant, se produit généralement sous la forme d’une séquence d’opérations de restauration, une par sauvegarde incrémentielle. Le demandeur doit informer le rédacteur qu’une telle restauration est en cours afin d’empêcher la récupération ou d’autres opérations indésirables jusqu’à ce que la restauration soit terminée. Pour ce faire, appelez [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores). Cette méthode est appelée par composant et indique au writer que d’autres restaurations sont destinées à ce composant. Pour la restauration finale dans la séquence, l’indicateur de restaurations supplémentaires doit être défini sur false (valeur par défaut), ce qui indique qu’il s’agit de la dernière restauration dans la séquence pour ce composant.

### <a name="new-targets"></a>Nouvelles cibles

S’il est pris en charge par l’enregistreur, le demandeur peut restaurer les fichiers de données dans un emplacement autre que l’emplacement d’origine de la sauvegarde. Le demandeur peut vérifier cette prise en charge en appelant [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). L' **\_ enregistreur VSS \_ BS \_ prend en charge le \_ nouveau bit \_ cible** si ce comportement est pris en charge par l’enregistreur. Le demandeur informe l’enregistreur du nouvel emplacement en appelant [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) pour chaque spécification de fichier déplacée. Le demandeur peut également décider de restaurer un fichier de plages spécifiques à un emplacement différent. Le demandeur informe l’auteur de cette modification en appelant [**IVssBackupComponents :: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

### <a name="directed-targets"></a>Cibles dirigées

Pour les scénarios de restauration complexes, un enregistreur peut souhaiter mapper des plages d’un fichier sauvegardé sur différentes plages du même fichier ou d’un fichier différent. Pour ce faire, vous pouvez utiliser le mécanisme cible dirigée. Le demandeur peut déterminer après la phase de [**Rerestauration IVssBackupComponents ::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) que ce mécanisme est utilisé pour un composant en appelant [**IVssComponent :: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) et en vérifiant qu’un retour de **VSS RT est \_ \_ dirigé**. Le demandeur peut obtenir toutes ces restaurations redirigées en appelant [**IVssComponent :: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) et [**IVssComponent :: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget). **IVssComponent :: GetDirectedTarget** retourne un chemin d’accès complet à un fichier source sur la sauvegarde et un chemin d’accès complet à un fichier de destination sur lequel sera restauré. Elle retourne également une liste de plages pour chacun de ces fichiers. Le demandeur est ensuite responsable de la restauration des plages spécifiées dans le fichier source vers les plages mappées dans le fichier de destination. Le format de la chaîne de plages est le même que dans [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).

-   [Rôle d’écriture dans VSS sauvegardes incrémentielles et différentielles](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Rôle demandeur dans VSS sauvegardes incrémentielles et différentielles](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
