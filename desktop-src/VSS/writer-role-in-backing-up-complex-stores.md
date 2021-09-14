---
description: En savoir plus sur le rôle d’écriture dans les sauvegardes incrémentielles et différentielles, qui nécessitent une coopération étroite entre les demandeurs et les writers.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Rôle d’écriture dans la sauvegarde de magasins complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e34952cc4a2184d2f9abcc43283d24f64bdcc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191844"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Rôle d’écriture dans la sauvegarde de magasins complexes

Comme avec toutes les opérations importantes sous VSS, les sauvegardes [*incrémentielles*](vssgloss-i.md) et [*différentielles*](vssgloss-d.md) requièrent une coopération étroite entre les demandeurs et les rédacteurs.

## <a name="backup-types"></a>Types de sauvegarde

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

Les rédacteurs indiquent le type de sauvegardes prises en charge en appelant [**IVssCreateWriterMetadata :: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) lors du traitement de l’événement d' [*identification*](vssgloss-i.md) . Le paramètre *dsSchemaMask* de la méthode **IVssCreateWriterMetadata :: SetBackupSchema** est un masque de bits indiquant les types de sauvegarde pris en charge. Tous les enregistreurs doivent prendre en charge les sauvegardes complètes.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**VSS \_ BS \_ différentiel**
</dt> <dd>

Indique la prise en charge des sauvegardes différentielles.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**VSS \_ BS \_ incrémentiel**
</dt> <dd>

Indique la prise en charge des sauvegardes incrémentielles.

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**\_Journal VSS BS \_**
</dt> <dd>

Indique la prise en charge des sauvegardes de fichiers journaux.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**\_copie VSS BS \_**
</dt> <dd>

Indique la prise en charge des sauvegardes de copie.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**\_ \_ \_ différentielle incrémentielle VSS BS exclusive \_**
</dt> <dd>

Indique qu’un enregistreur ne prend pas en charge le mélange de sauvegardes incrémentielles avec des sauvegardes différentielles.

</dd> </dl>

Le writer peut déterminer le type de sauvegarde en cours d’exécution en appelant [**CVssWriter :: GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype). Le point le plus à l’origine de cette opération est le traitement de l’événement PrepareForBackup. **CVssWriter :: GetBackupType** retourne un membre de l’énumération du [**\_ \_ type de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) . Si le type de sauvegarde n’est pas pris en charge par le writer, le writer doit traiter la sauvegarde comme une sauvegarde complète.

## <a name="backup-stamps"></a>Tampons de sauvegarde

Les sauvegardes incrémentielles et différentielles sont toujours liées à une sauvegarde précédente. Il existe deux façons de lier des sauvegardes. Pour les magasins de données simples, le demandeur peut effectuer le suivi de la corrélation entre les sauvegardes. Toutefois, pour les magasins de données plus complexes, l’enregistreur doit conserver son propre horodatage avec la sauvegarde. cet horodateur peut assurer le suivi de la position du journal, des informations de point de contrôle, etc. Un enregistreur indique qu’il a besoin de ses propres horodateurs en définissant le bit **VSS \_ BS \_ horodaté** lorsqu’il appelle [**IVssCreateWriterMetadata :: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema).

Un enregistreur peut stocker un horodateur avec chaque composant en cours de sauvegarde. L’enregistreur stocke l’horodateur en appelant [**IVssComponent :: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)et en passant une représentation sous forme de chaîne de l’horodatage pour le paramètre *wszBackupStamp* . En règle générale, un enregistreur appellera cette méthode lors du traitement de l’événement [*PostSnapshot*](vssgloss-p.md) . Toutefois, pour les sauvegardes qui n’impliquent pas de cliché instantané, l’événement PostSnapshot ne sera pas envoyé. Dans ce cas, **IVssComponent :: SetBackupStamp** doit être appelé lors du traitement de l’événement [*PrepareForBackup*](vssgloss-p.md) .

Lorsqu’une sauvegarde incrémentielle ou différentielle est effectuée, le demandeur indique au writer le tampon de sauvegarde de la sauvegarde précédente qui sert de base pour cette sauvegarde. L’enregistreur peut accéder à ce tampon de sauvegarde précédent lors du traitement de l’événement PrepareForBackup ou PostSnapshot, en appelant [**IVssComponent :: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Le writer peut utiliser l’horodatage retourné pour déterminer ce qui doit être sauvegardé.

## <a name="backup-strategies"></a>Stratégies de sauvegarde

### <a name="file-backup-files-strategies"></a>Stratégies de fichiers de sauvegarde de fichiers

Souvent, certains fichiers signalés dans les métadonnées de l’enregistreur doivent être sauvegardés uniquement lors de l’exécution de certains types de sauvegarde. Certains fichiers peuvent être requis uniquement lorsque vous effectuez une sauvegarde complète. D’autres fichiers peuvent uniquement être requis lors de l’exécution d’une sauvegarde incrémentielle ou différentielle. VSS fournit une méthode permettant aux rédacteurs d’indiquer ces informations au demandeur. Lors de l’ajout de fichiers à des composants à l’aide de [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), le paramètre *dwBackupTypeMask* indique pour quels types de sauvegarde ces fichiers doivent être sauvegardés. Le masque peut contenir une ou plusieurs des valeurs suivantes :

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

L’un des moyens pour un writer d’indiquer les fichiers qui ont changé est d’utiliser le mécanisme de fichier différent. Un enregistreur peut spécifier que certains fichiers d’un composant ne doivent être sauvegardés que s’ils ont été modifiés depuis un certain temps. Le writer appelle [**IVssComponent :: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) avec une spécification de fichier et une heure de dernière modification. **IVssComponent :: AddDifferencedFilesByLastModifyTime** est généralement appelé lors du traitement de l’événement PostSnapshot, bien qu’il puisse être appelé lors du traitement de l’événement PrepareForBackup. Le demandeur doit ensuite sauvegarder tous les fichiers correspondant à la spécification de fichier qui ont été modifiés depuis l’heure spécifiée. Si le writer utilise le mécanisme de tampon de sauvegarde, cette dernière heure de modification sera déterminée en fonction du tampon de sauvegarde précédent dans le document de sauvegarde. Le writer peut également passer la valeur zéro pour l’heure de la dernière modification, ce qui indique que le demandeur est chargé de déterminer l’heure de la dernière sauvegarde et que les fichiers ont été modifiés depuis ce moment.

### <a name="partial-file-backup"></a>Sauvegarde de fichiers partielle

Une autre façon pour un enregistreur d’indiquer des modifications au demandeur est d’utiliser le mécanisme de fichier partiel. Un enregistreur peut spécifier des plages d’octets dans des fichiers de composants qui doivent être sauvegardés ; l’enregistreur peut spécifier ces plages de fichiers lors du traitement de l’événement PostSnapshot ou PrepareForBackup. Le writer appelle [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) pour ajouter des spécifications de fichier partielles à la sauvegarde. Une spécification de fichier partielle se compose d’un chemin d’accès et d’un nom de fichier, ainsi que d’informations sur les plages du fichier qui doivent être sauvegardées.

### <a name="file-specification-rules"></a>Règles de spécification de fichier

[**IVssComponent :: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) ou [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) peuvent être utilisés pour modifier les spécifications de fichier fournies pendant l’événement d’identification, ou pour ajouter des fichiers entièrement nouveaux à la spécification. Si le writer modifie le jeu d’informations pendant l’événement d’identification à l’aide de **IVssComponent :: AddDifferencedFilesByLastModifyTime**, la spécification de fichier doit correspondre exactement à l’une des spécifications de fichier dans le composant actuel. La spécification de fichier ne doit pas chevaucher partiellement des fichiers dans le composant actuel et ne doit pas correspondre à des fichiers dans d’autres composants. Toutefois, les fichiers spécifiés à l’aide de **IVssComponent :: AddPartialFile** peuvent chevaucher partiellement une autre spécification de fichier. Les informations définies par **IVssComponent :: AddDifferencedFilesByLastModifyTime** ou **IVssComponent :: AddPartialFile** remplacent le jeu d’informations précédemment à l’aide de l’interface [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) en réponse à l’événement d’identification.

Les spécifications de fichier générales peuvent avoir une valeur d’emplacement secondaire (définie par le paramètre *wszAlternateLocation* de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) qui indique un autre emplacement à partir duquel obtenir le fichier au moment de la sauvegarde. Si la spécification de fichier définie par le biais des mécanismes de fichier de différences ou de fichiers partiels correspond à une spécification de fichier existante qui a un autre emplacement, l’application de sauvegarde obtiendra les données à partir de cet autre emplacement.

Si la spécification de fichier définie dans [**IVssComponent :: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) ou dans [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) ne correspond pas aux fichiers du composant en cours de sauvegarde, tous les fichiers correspondants sont ajoutés à la sauvegarde. Vous devez veiller à ce que l’enregistreur ajoute uniquement des fichiers qui existent sur un volume qui est déjà en cours de copie fantôme au cours de cette tâche. dans le cas contraire, le demandeur peut ne pas réussir à sauvegarder ces fichiers. Si ces fonctions sont appelées lors du traitement de l’événement PostSnapshot, cela peut être déterminé à l’aide de la méthode [**CVssWriter :: IsPathAffected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) . En cas d’appel lors de la gestion de l’événement PrepareForBackup, le writer doit effectuer cette détermination à l’aide d’une autre méthode.

### <a name="backup-without-a-shadow-copy"></a>Sauvegarde sans cliché instantané

Certains types de fichiers n’ont peut-être pas besoin d’être sauvegardés sur un volume de clichés instantanés. Par exemple, cela est souvent vrai pour les fichiers journaux de base de données. Étant donné que les fichiers journaux augmentent de manière monotone et qu’un enregistreur peut spécifier exactement les portions du fichier à sauvegarder à l’aide de fichiers partiels, il est souvent possible de sauvegarder la déconnexion du volume d’origine. En guise d’optimisation, un enregistreur peut marquer les fichiers qui requièrent des clichés instantanés pour différents types de sauvegarde à l’aide des indicateurs définis dans le paramètre *dwBackupTypeMask* de [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup). Les indicateurs pris en charge sont les suivants :

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

## <a name="backup-cleanup"></a>Nettoyage de sauvegarde

Si le writer doit effectuer une troncation du journal ou un autre nettoyage après la sauvegarde, l’emplacement approprié pour effectuer cette opération s’effectue lors du traitement de l’événement [*BackupComplete*](vssgloss-b.md) . L’événement [*BackupShutdown*](vssgloss-b.md) sera envoyé un peu plus tard après BackupComplete. un nettoyage peut également être effectué dans le gestionnaire d’événements BackupShutdown.

L’événement BackupShutdown est toujours envoyé après l’arrêt d’une sauvegarde. Si le demandeur se termine anormalement lors de l’exécution d’une sauvegarde, BackupShutdown est envoyé immédiatement, sans envoyer d’abord BackupComplete. Si le writer doit nettoyer un État, cela peut être fait ici ; Toutefois, la troncation du journal ne doit pas se produire dans cet événement, car la sauvegarde ne s’est pas nécessairement terminée.

## <a name="restore-strategies"></a>Stratégies de restauration

Les tâches de base des enregistreurs à la restauration sont de vérifier que la restauration peut se produire dans la gestion de l’événement de prérestauration et que la restauration s’est produite dans la gestion de l’événement PostRestore. Les magasins plus complexes effectuent également un processus de récupération dans le gestionnaire PostRestore. Si la restauration fait partie d’une restauration incrémentielle ou différentielle, le rédacteur souhaite généralement retarder ce processus de récupération jusqu’à ce que toutes les restaurations incrémentielles ou différentielles aient été effectuées. [**IVssComponent :: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) indique s’il s’agit de la dernière restauration de ce composant, ou s’il y a plus de restaurations à venir. Si **IVssComponent :: GetAdditionalRestores** retourne la **valeur true**, l’enregistreur ne doit pas exécuter sa procédure de récupération sur ce composant.

## <a name="new-targets"></a>Nouvelles cibles

S’il est pris en charge par l’enregistreur, le demandeur peut restaurer les fichiers de données dans un emplacement autre que l’emplacement d’origine de la sauvegarde. Un enregistreur indique la prise en charge de ce mode de restauration, car il **prend en charge le nouveau bit \_ \_ \_ \_ \_ cible** dans le paramètre *dsSchemaMask* lors de l’appel de [**IVssCreateWriterMetadata :: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema). Un enregistreur obtient les nouveaux emplacements pour les fichiers de composant au moment de la restauration en appelant [**IVssComponent :: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) et [**IVssComponent :: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget).

## <a name="directed-targets"></a>Cibles dirigées

Pour les scénarios de restauration complexes, un enregistreur peut souhaiter mapper des plages d’un fichier sauvegardé sur différentes plages du même fichier ou d’un fichier différent. Pour ce faire, vous pouvez utiliser le mécanisme de cible dirigée. Pour ce faire, un enregistreur doit d’abord indiquer que cela se produit en appelant [**IVssComponent :: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget), en transmettant le paramètre *cible* dans **VSS \_ RT \_** . Ensuite, pour chaque mappage, le writer appelle [**IVssComponent :: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget). Cette méthode prend un chemin d’accès complet à un fichier source sur la sauvegarde et un chemin d’accès complet à un fichier de destination qui sera restauré vers. Elle prend également une liste de plages pour chacun de ces fichiers. Le writer appelle ces fonctions lors de la gestion de l’événement de prérestauration, et le demandeur est ensuite chargé de restaurer les plages spécifiées dans le fichier source vers les plages mappées dans le fichier de destination. Le format de la chaîne de plages est le même que dans [ **IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Métadonnées de l’enregistreur privé

Il est souvent utile pour un enregistreur de conserver les métadonnées privées avec une sauvegarde pour effectuer correctement une restauration incrémentielle ou différentielle. Un enregistreur peut appeler [**IVssComponent :: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) tout en gérant PrepareForBackup ou PostSnapshot pour stocker les métadonnées. Ces métadonnées sont accessibles par le writer pendant la prérestauration ou l’PostRestore en appelant [**IVssComponent :: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata). Les métadonnées peuvent également être stockées avec une spécification de fichier partielle à l’aide du paramètre *wszMetadata* de [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile); Ces métadonnées sont accessibles par le biais du paramètre *pbstrMetadata* de [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Le writer peut également passer des métadonnées à lui-même entre [**CVssWriter :: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) et [**CVssWriter :: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). Dans **CVssWriter :: OnPreRestore**, les métadonnées sont définies en appelant [**IVssComponent :: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata). Dans **CVssWriter :: OnPostRestore**, les métadonnées sont récupérées en appelant [**IVssComponent :: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata).

-   [Rôle d’écriture dans VSS sauvegardes incrémentielles et différentielles](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Rôle demandeur dans VSS sauvegardes incrémentielles et différentielles](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



