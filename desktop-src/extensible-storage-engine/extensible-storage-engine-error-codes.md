---
description: en savoir plus sur les Codes d’erreur du moteur d’Stockage Extensible
title: Codes d’erreur du moteur de Stockage Extensible
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c6854b23a7399abb12f8eebb37c03aacde9ef11
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983182"
---
# <a name="extensible-storage-engine-error-codes"></a>Codes d’erreur du moteur de Stockage Extensible


_**S’applique à :** Windows | Windows Serveurs_

## <a name="extensible-storage-engine-error-codes"></a>Codes d’erreur du moteur de Stockage Extensible

les codes d’erreur (indicateurs) suivants sont utilisés par les fonctions de l’API du moteur d’Stockage Extensible.

Une [JET_ERR](./jet-err.md) valeur de zéro doit être interprétée comme une réussite.


| <p>Succès</p> | <p>Description</p> | 
|----------------|--------------------|
| <p>JET_errSuccess 0</p> | <p>La fonction a réussi.</p> | 



Une valeur [JET_ERR](./jet-err.md) supérieure à zéro doit être interprétée comme un avertissement.


| <p>Avertissements</p> | <p>Description</p> | 
|-----------------|--------------------|
| <p>JET_wrnRemainingVersions<br />321</p> | <p>La Banque des versions est toujours active. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_wrnUniqueKey<br />345</p> | <p>Une recherche sur un index non unique a produit une clé unique. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_wrnSeparateLongValue<br />406</p> | <p>Une colonne de base de données est une valeur long séparée. Cette erreur est retournée par le gestionnaire d’enregistrements.</p> | 
| <p>JET_wrnExistingLogFileHasBadSignature<br />558</p> | <p>La signature du fichier journal existant est incorrecte.</p> | 
| <p>JET_wrnExistingLogFileIsNotContiguous<br />559</p> | <p>Le fichier journal existant n’est pas contigu.</p> | 
| <p>JET_wrnSkipThisRecord<br />564</p> | <p>Cette erreur est réservée à un usage interne uniquement.</p> | 
| <p>JET_wrnTargetInstanceRunning<br />578</p> | <p>Le TargetInstance spécifié pour la restauration est en cours d’exécution.</p> | 
| <p>JET_wrnDatabaseRepaired<br />595</p> | <p>La base de données endommagée a été réparée.</p> | 
| <p>JET_wrnColumnNull<br />1004</p> | <p>La colonne a une valeur <strong>null</strong> .</p> | 
| <p>JET_wrnBufferTruncated<br />1006</p> | <p>La mémoire tampon est insuffisante pour les données.</p> | 
| <p>JET_wrnDatabaseAttached<br />1007</p> | <p>La base de données est déjà attachée.</p> | 
| <p>JET_wrnSortOverflow<br />1009</p> | <p>Le tri en cours de tentative ne dispose pas de suffisamment de mémoire pour se terminer.</p> | 
| <p>JET_wrnSeekNotEqual<br />1039</p> | <p>Une correspondance exacte n’a pas été trouvée pendant une recherche.</p> | 
| <p>JET_wrnRecordFoundGreater<br />JET_wrnSeekNotEqual</p> | <p>Une correspondance exacte n’a pas été trouvée pendant une recherche. Cette erreur est retournée par le gestionnaire d’enregistrements.</p> | 
| <p>JET_wrnRecordFoundLess<br />JET_wrnSeekNotEqual</p> | <p>Une correspondance exacte n’a pas été trouvée pendant une recherche. Cette erreur est retournée par le gestionnaire d’enregistrements.</p> | 
| <p>JET_wrnNoErrorInfo<br />1055</p> | <p>Il n’y a pas d’informations d’erreur étendues.</p> | 
| <p>JET_wrnNoIdleActivity<br />1058</p> | <p>Aucune activité inactive ne s’est produite.</p> | 
| <p>JET_wrnNoWriteLock<br />1067</p> | <p>Il n’existe aucun verrou d’écriture au niveau de la transaction 0.</p> | 
| <p>JET_wrnColumnSetNull<br />1068</p> | <p>La colonne est définie sur une valeur <strong>null</strong> .</p> | 
| <p>JET_wrnTableEmpty<br />1301</p> | <p>Une table vide a été ouverte.</p> | 
| <p>JET_wrnTableInUseBySystem<br />1327</p> | <p>Le nettoyage du système a un curseur ouvert sur la table.</p> | 
| <p>JET_wrnCorruptIndexDeleted<br />1415</p> | <p>L’index obsolète doit être supprimé.</p> | 
| <p>JET_wrnColumnMaxTruncated<br />1512</p> | <p>La longueur maximale est trop grande et a été tronquée.</p> | 
| <p>JET_wrnCopyLongValue<br />1520</p> | <p>Une valeur d’objet BLOB a été déplacée de l’enregistrement dans un stockage distinct d’objets BLOB volumineux.</p><p><strong>Remarque</strong> Cette erreur est réservée à un usage interne uniquement.</p> | 
| <p>JET_wrnColumnSkipped<br />1531</p> | <p>Les valeurs de colonne n’ont pas été retournées, car l’ID de colonne ou le membre <em>itagSequence</em> correspondant de la structure <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> qui a été demandée pour l’énumération a la valeur null.</p> | 
| <p>JET_wrnColumnNotLocal<br />1532</p> | <p>Les valeurs de colonne n’ont pas été retournées, car elles n’ont pas pu être reconstruites à partir des données existantes.</p> | 
| <p>JET_wrnColumnMoreTags<br />1533</p> | <p>Les valeurs de colonne existantes n’ont pas été demandées pour l’énumération.</p> | 
| <p>JET_wrnColumnTruncated<br />1534</p> | <p>La valeur de colonne a été tronquée à la limite de taille demandée pendant l’énumération.</p> | 
| <p>JET_wrnColumnPresent<br />1535</p> | <p>Les valeurs de colonne existent mais n’ont pas été retournées par la demande.</p> | 
| <p>JET_wrnColumnSingleValue<br />1536</p> | <p>La valeur de colonne a été retournée dans JET_COLUMNENUM à la suite de la définition de la JET_bitEnumerateCompressOutput.</p> | 
| <p>JET_wrnColumnDefault<br />1537</p> | <p>La valeur de la colonne est définie sur la valeur par défaut de la colonne.</p> | 
| <p>JET_wrnDataHasChanged<br />1610</p> | <p>Les données ont changé.</p> | 
| <p>JET_wrnKeyChanged<br />1618</p> | <p>Une nouvelle clé est utilisée.</p> | 
| <p>JET_wrnFileOpenReadOnly<br />1813</p> | <p>Le fichier de base de données est en lecture seule.</p> | 
| <p>JET_wrnIdleFull<br />1908</p> | <p>Le registre inactif est plein.</p> | 
| <p>JET_wrnDefragAlreadyRunning<br />2000</p> | <p>Une défragmentation en ligne est déjà en cours d’exécution sur la base de données spécifiée.</p> | 
| <p>JET_wrnDefragNotRunning<br />2001</p> | <p>Une défragmentation en ligne n’est pas en cours d’exécution sur la base de données spécifiée.</p> | 
| <p>JET_wrnCallbackNotRegistered<br />2100</p> | <p>Une fonction de rappel inexistante n’a pas été inscrite.</p> | 



Une valeur [JET_ERR](./jet-err.md) inférieure à zéro doit être interprétée comme une erreur.


| <p>Errors</p> | <p>Description</p> | 
|---------------|--------------------|
| <p>JET_wrnNyi<br />-1</p> | <p>La fonction n’est pas encore implémentée.</p> | 
| <p>JET_errRfsFailure<br />-100</p> | <p>Le simulateur d’échec de ressource a échoué.</p> | 
| <p>JET_errRfsNotArmed<br />-101</p> | <p>Le simulateur d’échec de ressource n’a pas été initialisé.</p> | 
| <p>JET_errFileClose<br />-102</p> | <p>Impossible de fermer le fichier.</p> | 
| <p>JET_errOutOfThreads<br />-103</p> | <p>Le thread n’a pas pu être démarré.</p> | 
| <p>JET_errTooManyIO<br />-105</p> | <p>Le système est occupé en raison d’un trop grand nombre d’IOs.</p> | 
| <p>JET_errTaskDropped<br />-106</p> | <p>Impossible d’exécuter la tâche asynchrone demandée.</p> | 
| <p>JET_errInternalError<br />-107</p> | <p>Une erreur interne irrécupérable s’est produite.</p> | 
| <p>JET_errDatabaseBufferDependenciesCorrupted<br />-255</p> | <p>Les dépendances de mémoire tampon ont été définies de manière incorrecte et un échec de récupération s’est produite.</p> | 
| <p>JET_errPreviousVersion<br />-322</p> | <p>La version existait déjà et un échec de récupération s’est produite. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errPageBoundary<br />-323</p> | <p>La limite de la page a été atteinte. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errKeyBoundary<br />-324</p> | <p>La limite de la clé a été atteinte. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errBadPageLink<br />-327</p> | <p>La base de données est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errBadBookmark<br />-328</p> | <p>Le signet n’a pas d’adresse correspondante dans la base de données. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errNTSystemCallFailed<br />-334</p> | <p>L’appel au système d’exploitation a échoué. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errBadParentPageLink<br />-338</p> | <p>Une base de données parente est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errSPAvailExtCacheOutOfSync<br />-340</p> | <p>Le cache AvailExt ne correspond pas à l’arborescence B +. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errSPAvailExtCorrupted<br />-341</p> | <p>L’arborescence de l’espace AllAvailExt est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errSPAvailExtCacheOutOfMemory<br />-342</p> | <p>Une erreur de mémoire insuffisante s’est produite lors de l’allocation d’un nœud de cache AvailExt. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errSPOwnExtCorrupted<br />-343</p> | <p>L’arborescence de l’espace OwnExt est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errDbTimeCorrupted<br />-344</p> | <p>La valeur dbTime sur la page actuelle est supérieure à la valeur dbTime de la base de données globale. Cette erreur est retournée par le gestionnaire de répertoire.</p> | 
| <p>JET_errKeyTruncated<br />-346</p> | <p>Une tentative de création d’une clé pour une entrée d’index a échoué, car la clé aurait été tronquée et la définition de l’index interdit la troncation de clé.</p> | 
| <p>JET_errKeyTooBig<br />-408</p> | <p>La clé est trop grande. Cette erreur est retournée par le gestionnaire d’enregistrements.</p> | 
| <p>JET_errInvalidLoggedOperation<br />-500</p> | <p>L’opération journalisée ne peut pas être rétablie.</p> | 
| <p>JET_errLogFileCorrupt<br />-501</p> | <p>Le fichier journal est endommagé.</p> | 
| <p>JET_errNoBackupDirectory<br />-503</p> | <p>Un répertoire de sauvegarde n’a pas été fourni.</p> | 
| <p>JET_errBackupDirectoryNotEmpty<br />-504</p> | <p>Le répertoire de sauvegarde n’est pas vide.</p> | 
| <p>JET_errBackupInProgress<br />-505</p> | <p>La sauvegarde est déjà active.</p> | 
| <p>JET_errRestoreInProgress<br />-506</p> | <p>Une restauration est en cours.</p> | 
| <p>JET_errMissingPreviousLogFile<br />-509</p> | <p>Le fichier journal est manquant pour le point de vérification.</p> | 
| <p>JET_errLogWriteFail<br />-510</p> | <p>Une erreur s’est produite lors de l’écriture dans le fichier journal.</p> | 
| <p>JET_errLogDisabledDueToRecoveryFailure<br />-511</p> | <p>La tentative d’écriture dans le journal après la récupération a échoué.</p> | 
| <p>JET_errCannotLogDuringRecoveryRedo<br />-512</p> | <p>La tentative d’écriture dans le journal pendant le rétablissement de la récupération a échoué.</p> | 
| <p>JET_errLogGenerationMismatch<br />-513</p> | <p>Le nom du fichier journal ne correspond pas au numéro de génération interne.</p> | 
| <p>JET_errBadLogVersion<br />-514</p> | <p>La version du fichier journal n’est pas compatible avec la version ESE.</p> | 
| <p>JET_errInvalidLogSequence<br />-515</p> | <p>L’horodateur dans le journal suivant ne correspond pas à l’horodatage attendu.</p> | 
| <p>JET_errLoggingDisabled<br />-516</p> | <p>Le journal n’est pas actif.</p> | 
| <p>JET_errLogBufferTooSmall<br />-517</p> | <p>Le tampon du journal est trop petit pour la récupération.</p> | 
| <p>JET_errLogSequenceEnd<br />-519</p> | <p>Le nombre maximal de fichiers journaux a été dépassé.</p> | 
| <p>JET_errNoBackup<br />-520</p> | <p>Aucune sauvegarde n’est en cours.</p> | 
| <p>JET_errInvalidBackupSequence<br />-521</p> | <p>L’appel de sauvegarde est hors séquence.</p> | 
| <p>JET_errBackupNotAllowedYet<br />-523</p> | <p>Une sauvegarde ne peut pas être effectuée pour l’instant.</p> | 
| <p>JET_errDeleteBackupFileFail<br />-524</p> | <p>Un fichier de sauvegarde n’a pas pu être supprimé.</p> | 
| <p>JET_errMakeBackupDirectoryFail<br />-525</p> | <p>Impossible de créer le répertoire temporaire de sauvegarde.</p> | 
| <p>JET_errInvalidBackup<br />-526</p> | <p>La journalisation circulaire est activée ; Impossible d’effectuer une sauvegarde incrémentielle.</p> | 
| <p>JET_errRecoveredWithErrors<br />-527</p> | <p>Les données ont été restaurées avec des erreurs.</p> | 
| <p>JET_errMissingLogFile<br />-528</p> | <p>Le fichier journal actuel est manquant.</p> | 
| <p>JET_errLogDiskFull<br />-529</p> | <p>Le disque journal est saturé.</p> | 
| <p>JET_errBadLogSignature<br />-530</p> | <p>La signature d’un fichier journal est incorrecte.</p> | 
| <p>JET_errBadDbSignature<br />-531</p> | <p>La signature d’un fichier de base de données est incorrecte.</p> | 
| <p>JET_errBadCheckpointSignature<br />-532</p> | <p>La signature d’un fichier de point de contrôle est incorrecte.</p> | 
| <p>JET_errCheckpointCorrupt<br />-533</p> | <p>Le fichier de point de contrôle est introuvable ou endommagé.</p> | 
| <p>JET_errMissingPatchPage<br />-534</p> | <p>La page du fichier de correctif de base de données est introuvable lors de la récupération.</p> | 
| <p>JET_errBadPatchPage<br />-535</p> | <p>La page du fichier de correctif de base de données n’est pas valide.</p> | 
| <p>JET_errRedoAbruptEnded<br />-536</p> | <p>Le rétablissement s’est soudainement arrêté en raison d’une défaillance soudaine lors de la lecture des journaux à partir du fichier journal.</p> | 
| <p>JET_errBadSLVSignature<br />-537</p> | <p>Cet indicateur est réservé.</p> | 
| <p>JET_errPatchFileMissing<br />-538</p> | <p>La restauration matérielle a détecté qu’un fichier correctif de base de données est manquant dans le jeu de sauvegarde.</p> | 
| <p>JET_errDatabaseLogSetMismatch<br />-539</p> | <p>La base de données n’appartient pas à l’ensemble actuel de fichiers journaux.</p> | 
| <p>JET_errDatabaseStreamingFileMismatch<br />-540</p> | <p>Cet indicateur est réservé.</p> | 
| <p>JET_errLogFileSizeMismatch<br />-541</p> | <p>La taille réelle du fichier journal ne correspond pas à <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p> | 
| <p>JET_errCheckpointFileNotFound<br />-542</p> | <p>Le fichier de point de contrôle est introuvable.</p> | 
| <p>JET_errRequiredLogFilesMissing<br />-543</p> | <p>Les fichiers journaux requis pour la récupération sont absents.</p> | 
| <p>JET_errSoftRecoveryOnBackupDatabase<br />-544</p> | <p>Une récupération logicielle va être utilisée sur une base de données de sauvegarde lorsqu’une restauration doit être utilisée à la place.</p> | 
| <p>JET_errLogFileSizeMismatchDatabasesConsistent<br />-545</p> | <p>Les bases de données ont été récupérées, mais la taille du fichier journal utilisée lors de la récupération ne correspond pas à <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p> | 
| <p>JET_errLogSectorSizeMismatch<br />-546</p> | <p>La taille des secteurs du fichier journal ne correspond pas à la taille des secteurs du volume actuel.</p> | 
| <p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />-547</p> | <p>Les bases de données ont été récupérées, mais la taille des secteurs du fichier journal (utilisée lors de la récupération) ne correspond pas à la taille des secteurs du volume actuel.</p> | 
| <p>JET_errLogSequenceEndDatabasesConsistent<br />-548</p> | <p>Les bases de données ont été récupérées, mais toutes les générations de journaux possibles dans la séquence actuelle ont été utilisées. Tous les fichiers journaux et le fichier de point de contrôle doivent être supprimés et les bases de données doivent être sauvegardées avant de continuer.</p> | 
| <p>JET_errStreamingDataNotLogged<br />-549</p> | <p>Une tentative illégale de relecture d’une opération de lecture de fichier de diffusion en continu a été effectuée, où les données n’étaient pas journalisées. Cela est probablement dû à une tentative de restauration par progression avec la journalisation circulaire activée.</p> | 
| <p>JET_errDatabaseDirtyShutdown<br />-550</p> | <p>La base de données n’a pas été arrêtée correctement. Une récupération doit d’abord être exécutée pour terminer correctement les opérations de base de données pour l’arrêt précédent.</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>Cette erreur est obsolète et a été remplacée par JET_errDatabaseDirtyShutdown.</p> | 
| <p>JET_errConsistentTimeMismatch<br />-551</p> | <p>L’heure de la dernière cohérence pour la base de données n’a pas été mise en correspondance.</p> | 
| <p>JET_errDatabasePatchFileMismatch<br />-552</p> | <p>Le fichier de correctif de base de données n’est pas généré à partir de cette sauvegarde.</p> | 
| <p>JET_errEndingRestoreLogTooLow<br />-553</p> | <p>Le numéro de journal de début est trop faible pour la restauration.</p> | 
| <p>JET_errStartingRestoreLogTooHigh<br />-554</p> | <p>Le numéro de journal de début est trop élevé pour la restauration.</p> | 
| <p>JET_errGivenLogFileHasBadSignature<br />-555</p> | <p>La signature du fichier journal de restauration est incorrecte.</p> | 
| <p>JET_errGivenLogFileIsNotContiguous<br />-556</p> | <p>Le fichier journal de restauration n’est pas contigu.</p> | 
| <p>JET_errMissingRestoreLogFiles<br />-557</p> | <p>Certains fichiers journaux de restauration sont manquants.</p> | 
| <p>JET_errMissingFullBackup<br />-560</p> | <p>La base de données a manqué une sauvegarde complète précédente avant de tenter d’effectuer une sauvegarde incrémentielle.</p> | 
| <p>JET_errBadBackupDatabaseSize<br />-561</p> | <p>La taille de la base de données de sauvegarde n’est pas un multiple de la taille de la page de la base de données.</p> | 
| <p>JET_errDatabaseAlreadyUpgraded<br />-562</p> | <p>La tentative actuelle de mise à niveau d’une base de données a été arrêtée, car la base de données est déjà à jour.</p> | 
| <p>JET_errDatabaseIncompleteUpgrade<br />-563</p> | <p>La base de données n’a été convertie que partiellement au format actuel. La base de données doit être restaurée à partir d’une sauvegarde.</p> | 
| <p>JET_errMissingCurrentLogFiles<br />-565</p> | <p>Certains fichiers journaux sont manquants pour la restauration continue.</p> | 
| <p>JET_errDbTimeTooOld<br />-566</p> | <p>L’dbtime sur une page est plus petite que le dbtimeBefore dans l’enregistrement.</p> | 
| <p>JET_errDbTimeTooNew<br />-567</p> | <p>L’dbtime sur une page est à l’avance du dbtimeBefore dans l’enregistrement.</p> | 
| <p>JET_errMissingFileToBackup<br />-569</p> | <p>Certains fichiers de correctifs de base de données ou de journal étaient manquants pendant la sauvegarde.</p> | 
| <p>JET_errLogTornWriteDuringHardRestore<br />-570</p> | <p>Une écriture endommagée a été détectée dans une sauvegarde qui a été définie lors d’une restauration matérielle.</p> | 
| <p>JET_errLogTornWriteDuringHardRecovery<br />-571</p> | <p>Une écriture endommagée a été détectée lors d’une récupération matérielle (le journal ne fait pas partie d’un jeu de sauvegarde).</p> | 
| <p>JET_errLogCorruptDuringHardRestore<br />-573</p> | <p>Une altération a été détectée dans un jeu de sauvegarde lors d’une restauration matérielle.</p> | 
| <p>JET_errLogCorruptDuringHardRecovery<br />-574</p> | <p>Une altération a été détectée pendant la récupération matérielle (le journal ne fait pas partie d’un jeu de sauvegarde).</p> | 
| <p>JET_errMustDisableLoggingForDbUpgrade<br />-575</p> | <p>Impossible d’activer la journalisation lors de la tentative de mise à niveau d’une base de données.</p> | 
| <p>JET_errBadRestoreTargetInstance<br />-577</p> | <p>Le TargetInstance spécifié pour la restauration n’a pas été trouvé ou les fichiers journaux ne correspondent pas.</p> | 
| <p>JET_errRecoveredWithoutUndo<br />-579</p> | <p>Le moteur de base de données a relu toutes les opérations du journal des transactions pour effectuer une récupération après incident, mais l’appelant a choisi d’arrêter la récupération sans restaurer les mises à jour non validées.</p> | 
| <p>JET_errDatabasesNotFromSameSnapshot<br />-580</p> | <p>Les bases de données à restaurer ne proviennent pas de la même sauvegarde de clichés instantanés.</p> | 
| <p>JET_errSoftRecoveryOnSnapshot<br />-581</p> | <p>Il existe une récupération logicielle sur une base de données à partir d’un jeu de sauvegarde de clichés instantanés.</p> | 
| <p>JET_errUnicodeTranslationBufferTooSmall<br />-601</p> | <p>La mémoire tampon de traduction Unicode est trop petite.</p> | 
| <p>JET_errUnicodeTranslationFail<br />-602</p> | <p>Échec de la normalisation Unicode.</p> | 
| <p>JET_errUnicodeNormalizationNotSupported<br />-603</p> | <p>Le système d’exploitation ne prend pas en charge la normalisation Unicode et aucun rappel de normalisation n’a été spécifié.</p> | 
| <p>JET_errExistingLogFileHasBadSignature<br />-610</p> | <p>La signature du fichier journal existant est incorrecte.</p> | 
| <p>JET_errExistingLogFileIsNotContiguous<br />-611</p> | <p>Un fichier journal existant n’est pas contigu.</p> | 
| <p>JET_errLogReadVerifyFailure<br />-612</p> | <p>Une erreur de somme de contrôle a été trouvée dans le fichier journal lors de la sauvegarde.</p> | 
| <p>JET_errSLVReadVerifyFailure<br />-613</p> | <p>Cet indicateur est réservé.</p> | 
| <p>JET_errCheckpointDepthTooDeep<br />-614</p> | <p>Il y a trop de générations en suspens entre le point de contrôle et la génération actuelle.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase<br />-615</p> | <p>Une récupération matérielle a été tentée sur une base de données qui n’était pas une base de données de sauvegarde.</p> | 
| <p>JET_errInvalidGrbit<br />-900</p> | <p>Un paramètre Grbit n’est pas valide.</p> | 
| <p>JET_errTermInProgress<br />-1 000</p> | <p>Arrêt en cours.</p> | 
| <p>JET_errFeatureNotAvailable<br />-1001</p> | <p>Cet élément d’API n’est pas pris en charge.</p> | 
| <p>JET_errInvalidName<br />-1002</p> | <p>Un nom non valide est utilisé.</p> | 
| <p>JET_errInvalidParameter<br />-1003</p> | <p>Un paramètre d’API non valide est utilisé.</p> | 
| <p>JET_errDatabaseFileReadOnly<br />-1008</p> | <p>Une tentative d’attachement à un fichier de base de données en lecture seule a été tentée pour les opérations de lecture/écriture.</p> | 
| <p>JET_errInvalidDatabaseId<br />-1010</p> | <p>Un ID de base de données n’est pas valide.</p> | 
| <p>JET_errOutOfMemory<br />-1011</p> | <p>La mémoire du système est insuffisante.</p> | 
| <p>JET_errOutOfDatabaseSpace<br />-1012</p> | <p>La taille maximale de la base de données a été atteinte.</p> | 
| <p>JET_errOutOfCursors<br />-1013</p> | <p>La table est hors des curseurs.</p> | 
| <p>JET_errOutOfBuffers<br />-1014</p> | <p>La base de données est en dehors des tampons de page.</p> | 
| <p>JET_errTooManyIndexes<br />-1015</p> | <p>Le nombre d’index est trop important.</p> | 
| <p>JET_errTooManyKeys<br />-1016</p> | <p>Le nombre de colonnes dans un index est trop important.</p> | 
| <p>JET_errRecordDeleted<br />-1017</p> | <p>L’enregistrement a été supprimé.</p> | 
| <p>JET_errReadVerifyFailure<br />-1018</p> | <p>Une page de base de données contient une erreur de somme de contrôle.</p> | 
| <p>JET_errPageNotInitialized<br />-1019</p> | <p>Il y a une page de base de données vide.</p> | 
| <p>JET_errOutOfFileHandles<br />-1020</p> | <p>Il n’y a aucun descripteur de fichier.</p> | 
| <p>JET_errDiskIO<br />-1022</p> | <p>Il y a une erreur d’e/s disque.</p> | 
| <p>JET_errInvalidPath<br />-1023</p> | <p>Un chemin d’accès au fichier n’est pas valide.</p> | 
| <p>JET_errInvalidSystemPath<br />-1024</p> | <p>Le chemin d’accès au système est incorrect.</p> | 
| <p>JET_errInvalidLogDirectory<br />-1025</p> | <p>Le répertoire de journal n’est pas valide.</p> | 
| <p>JET_errRecordTooBig<br />-1026</p> | <p>L’enregistrement est plus grand que la taille maximale.</p> | 
| <p>JET_errTooManyOpenDatabases<br />-1027</p> | <p>Le nombre de bases de données ouvertes est trop important.</p> | 
| <p>JET_errInvalidDatabase<br />-1028</p> | <p>Il ne s’agit pas d’un fichier de base de données.</p> | 
| <p>JET_errNotInitialized<br />-1029</p> | <p>Le moteur de base de données n’a pas été initialisé.</p> | 
| <p>JET_errAlreadyInitialized<br />-1030</p> | <p>Le moteur de base de données est déjà initialisé.</p> | 
| <p>JET_errInitInProgress<br />-1031</p> | <p>Le moteur de base de données est en cours d’initialisation.</p> | 
| <p>JET_errFileAccessDenied<br />-1032</p> | <p>Impossible d’accéder au fichier, car le fichier est verrouillé ou en cours d’utilisation.</p> | 
| <p>JET_errBufferTooSmall<br />-1038</p> | <p>La mémoire tampon est insuffisante.</p> | 
| <p>JET_errTooManyColumns<br />-1040</p> | <p>Trop de colonnes sont définies.</p> | 
| <p>JET_errContainerNotEmpty<br />-1043</p> | <p>Le conteneur n’est pas vide.</p> | 
| <p>JET_errInvalidFilename<br />-1044</p> | <p>Le nom de fichier n’est pas valide.</p> | 
| <p>JET_errInvalidBookmark<br />-1045</p> | <p>Il y a un signet non valide.</p> | 
| <p>JET_errColumnInUse<br />-1046</p> | <p>La colonne utilisée se trouve dans un index.</p> | 
| <p>JET_errInvalidBufferSize<br />-1047</p> | <p>La mémoire tampon de données ne correspond pas à la taille de colonne.</p> | 
| <p>JET_errColumnNotUpdatable<br />-1048</p> | <p>La valeur de la colonne ne peut pas être définie.</p> | 
| <p>JET_errIndexInUse<br />-1051</p> | <p>L’index est en cours d’utilisation.</p> | 
| <p>JET_errLinkNotSupported<br />-1052</p> | <p>La prise en charge des liens n’est pas disponible.</p> | 
| <p>JET_errNullKeyDisallowed<br />-1053</p> | <p>Les clés NULL ne sont pas autorisées sur un index.</p> | 
| <p>JET_errNotInTransaction<br />-1054</p> | <p>L’opération doit se produire dans une transaction.</p> | 
| <p>JET_errTooManyActiveUsers<br />-1059</p> | <p>Le nombre d’utilisateurs de base de données actifs est trop important</p> | 
| <p>JET_errInvalidCountry<br />-1061</p> | <p>Code de pays non valide ou inconnu.</p> | 
| <p>JET_errInvalidLanguageId<br />-1062</p> | <p>ID de langue non valide ou inconnu.</p> | 
| <p>JET_errInvalidCodePage<br />-1063</p> | <p>Une page de codes n’est pas valide ou est inconnue.</p> | 
| <p>JET_errInvalidLCMapStringFlags<br />-1064</p> | <p>Des indicateurs non valides sont utilisés pour <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</p> | 
| <p>JET_errVersionStoreEntryTooBig<br />-1065</p> | <p>Une tentative de création d’une entrée de la Banque des versions (RCE) supérieure à celle d’un compartiment de version a été tentée.</p> | 
| <p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />-1066</p> | <p>La Banque des versions ne dispose pas de suffisamment de mémoire et la tentative de nettoyage a échoué.</p> | 
| <p>JET_errVersionStoreOutOfMemory<br />-1069</p> | <p>La Banque des versions ne dispose pas de suffisamment de mémoire et une tentative de nettoyage a déjà été effectuée.</p> | 
| <p>JET_errCannotIndex<br />-1071</p> | <p>Les colonnes tiers de confiance et SLV ne peuvent pas être indexées.</p> | 
| <p>JET_errRecordNotDeleted<br />-1072</p> | <p>L’enregistrement n’a pas été supprimé.</p> | 
| <p>JET_errTooManyMempoolEntries<br />-1073</p> | <p>Trop d’entrées mempool ont été demandées.</p> | 
| <p>JET_errOutOfObjectIDs<br />-1074</p> | <p>La base de données est en dehors de l’arbre B + ObjectIDs, de sorte qu’une défragmentation hors connexion doit être effectuée pour récupérer des ObjectIds libérés ou inutilisés.</p> | 
| <p>JET_errOutOfLongValueIDs<br />-1075</p> | <p>Le compteur de l’ID de valeur long a atteint la valeur maximale. Une défragmentation hors connexion doit être effectuée pour récupérer des LongValueIDs libres ou inutilisés.</p> | 
| <p>JET_errOutOfAutoincrementValues<br />-1076</p> | <p>Le compteur d’incrémentation automatique a atteint la valeur maximale. Une défragmentation hors connexion ne sera pas en mesure de récupérer des valeurs d’incrémentation automatique libres ou inutilisées.</p> | 
| <p>JET_errOutOfDbtimeValues<br />-1077</p> | <p>Le compteur dbtime a atteint la valeur maximale. Une défragmentation hors connexion doit être effectuée pour récupérer des valeurs dbtime libres ou inutilisées.</p> | 
| <p>JET_errOutOfSequentialIndexValues<br />-1078</p> | <p>Un compteur d’index séquentiels a atteint la valeur maximale. Une défragmentation hors connexion doit être effectuée pour récupérer des valeurs SequentialIndex libres ou inutilisées.</p> | 
| <p>JET_errRunningInOneInstanceMode<br />-1080</p> | <p>Le mode d’instance unique est activé pour cet appel multi-instance.</p> | 
| <p>JET_errRunningInMultiInstanceMode<br />-1081</p> | <p>L’appel à instance unique est activé pour le mode multi-instance.</p> | 
| <p>JET_errSystemParamsAlreadySet<br />-1082</p> | <p>Les paramètres globaux du système ont déjà été définis.</p> | 
| <p>JET_errSystemPathInUse<br />-1083</p> | <p>Le chemin d’accès système est déjà utilisé par une autre instance de base de données.</p> | 
| <p>JET_errLogFilePathInUse<br />-1084</p> | <p>Le chemin d’accès du fichier journal est déjà utilisé par une autre instance de base de données.</p> | 
| <p>JET_errTempPathInUse<br />-1085</p> | <p>Le chemin d’accès à la base de données temporaire est déjà utilisé par une autre instance de base de données.</p> | 
| <p>JET_errInstanceNameInUse<br />-1086</p> | <p>Le nom de l’instance est déjà utilisé.</p> | 
| <p>JET_errInstanceUnavailable<br />-1090</p> | <p>Cette instance ne peut pas être utilisée car elle a rencontré une erreur irrécupérable.</p> | 
| <p>JET_errDatabaseUnavailable<br />-1091</p> | <p>Impossible d’utiliser cette base de données, car elle a rencontré une erreur irrécupérable.</p> | 
| <p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />-1092</p> | <p>Cette instance ne peut pas être utilisée car elle a rencontré une erreur log-Disk-Full lors de l’exécution d’une opération (par exemple, une restauration de transaction) qui n’a pas pu tolérer d’échec.</p> | 
| <p>JET_errOutOfSessions<br />-1101</p> | <p>La base de données est en dehors des sessions.</p> | 
| <p>JET_errWriteConflict<br />-1102</p> | <p>Le verrou d’écriture a échoué en raison de l’existence d’un verrou d’écriture en attente.</p> | 
| <p>JET_errTransTooDeep<br />-1103</p> | <p>Les transactions sont imbriquées trop profondément.</p> | 
| <p>JET_errInvalidSesid<br />-1104</p> | <p>Un descripteur de session n’est pas valide.</p> | 
| <p>JET_errWriteConflictPrimaryIndex<br />-1105</p> | <p>Une mise à jour a été tentée sur un index principal non validé.</p> | 
| <p>JET_errInTransaction<br />-1108</p> | <p>L’opération n’est pas autorisée dans une transaction.</p> | 
| <p>JET_errRollbackRequired<br />-1109</p> | <p>La transaction en cours doit être restaurée. Elle ne peut pas être validée et une nouvelle ne peut pas être démarrée.</p> | 
| <p>JET_errTransReadOnly<br />-1110</p> | <p>Une transaction en lecture seule a tenté de modifier la base de données.</p> | 
| <p>JET_errSessionWriteConflict<br />-1111</p> | <p>Tentative de remplacement du même enregistrement par deux curseurs différents dans la même session.</p> | 
| <p>JET_errRecordTooBigForBackwardCompatibility<br />-1112</p> | <p>L’enregistrement est trop grand s’il est représenté dans un format de base de données à partir d’une version précédente de jet.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort<br />-1113</p> | <p>La table temporaire n’a pas pu être créée en raison de paramètres qui sont en conflit avec JET_bitTTForwardOnly.</p> | 
| <p>JET_errSesidTableIdMismatch<br />-1114</p> | <p>Le descripteur de session ne peut pas être utilisé avec l’ID de table, car il n’a pas été utilisé pour le créer.</p> | 
| <p>JET_errInvalidInstance<br />-1115</p> | <p>Le descripteur d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</p> | 
| <p>JET_errReadLostFlushVerifyFailure<br />-1119</p> | <p>La page de base de données lue à partir du disque avait une écriture précédente non représentée sur la page. disponible sur Windows 8 et versions ultérieures pour le client, et Windows Server 2012 et versions ultérieures pour le serveur.</p> | 
| <p>JET_errDatabaseDuplicate<br />-1201</p> | <p>La base de données existe déjà.</p> | 
| <p>JET_errDatabaseInUse<br />-1202</p> | <p>Base de données en cours d’utilisation.</p> | 
| <p>JET_errDatabaseNotFound<br />-1203</p> | <p>Il n’existe aucune base de données de ce type.</p> | 
| <p>JET_errDatabaseInvalidName<br />-1204</p> | <p>Le nom de la base de données n’est pas valide.</p> | 
| <p>JET_errDatabaseInvalidPages<br />-1205</p> | <p>Le nombre de pages est incorrect.</p> | 
| <p>JET_errDatabaseCorrupted<br />-1206</p> | <p>Il n’existe pas de fichier de base de données ou de base de données endommagée.</p> | 
| <p>JET_errDatabaseLocked<br />-1207</p> | <p>La base de données est verrouillée en mode exclusif.</p> | 
| <p>JET_errCannotDisableVersioning<br />-1208</p> | <p>Le contrôle de version de cette base de données ne peut pas être désactivé.</p> | 
| <p>JET_errInvalidDatabaseVersion<br />-1209</p> | <p>Le moteur de base de données est incompatible avec la base de données.</p> | 
| <p>JET_errDatabase200Format<br />-1210</p> | <p>La base de données est dans un format plus ancien (200). Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini. Windows Client NT uniquement.</p> | 
| <p>JET_errDatabase400Format<br />-1211</p> | <p>La base de données est dans un format plus ancien (400). Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini. Windows Client NT uniquement.</p> | 
| <p>JET_errDatabase500Format<br />-1212</p> | <p>La base de données est dans un format plus ancien (500). Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini. Windows Client NT uniquement.</p> | 
| <p>JET_errPageSizeMismatch<br />-1213</p> | <p>La taille de la page de la base de données ne correspond pas au moteur.</p> | 
| <p>JET_errTooManyInstances<br />-1214</p> | <p>Aucune instance de base de données supplémentaire ne peut être démarrée.</p> | 
| <p>JET_errDatabaseSharingViolation<br />-1215</p> | <p>Une autre instance de base de données utilise cette base de données.</p> | 
| <p>JET_errAttachedDatabaseMismatch<br />-1216</p> | <p>Une pièce jointe de base de données en attente a été détectée au début ou à la fin de la récupération, mais la base de données est manquante ou ne correspond pas aux informations de la pièce jointe.</p> | 
| <p>JET_errDatabaseInvalidPath<br />-1217</p> | <p>Le chemin d’accès au fichier de base de données spécifié n’est pas autorisé.</p> | 
| <p>JET_errDatabaseIdInUse<br />-1218</p> | <p>Un ID qui est déjà en cours d’utilisation est assigné à une base de données.</p> | 
| <p>JET_errForceDetachNotAllowed<br />-1219</p> | <p>Le détachement forcé est autorisé uniquement après l’arrêt du détachement normal en raison d’une erreur.</p> | 
| <p>JET_errCatalogCorrupted<br />-1220</p> | <p>Une altération a été détectée dans le catalogue.</p> | 
| <p>JET_errPartiallyAttachedDB<br />-1221</p> | <p>La base de données n’est attachée que partiellement et l’opération d’attachement ne peut pas être effectuée.</p> | 
| <p>JET_errDatabaseSignInUse<br />-1222</p> | <p>La base de données avec la même signature est déjà en cours d’utilisation.</p> | 
| <p>JET_errDatabaseCorruptedNoRepair<br />-1224</p> | <p>La base de données est endommagée, mais aucune réparation n’est autorisée.</p> | 
| <p>JET_errInvalidCreateDbVersion<br />-1225</p> | <p>Le moteur de base de données a tenté de relire une opération créer une base de données à partir du journal des transactions mais a échoué en raison d’une version incompatible de cette opération.</p> | 
| <p>JET_errTableLocked<br />-1302</p> | <p>La table est verrouillée en mode exclusif.</p> | 
| <p>JET_errTableDuplicate<br />-1303</p> | <p>La table existe déjà.</p> | 
| <p>JET_errTableInUse<br />-1304</p> | <p>La table est en cours d’utilisation et ne peut pas être verrouillée.</p> | 
| <p>JET_errObjectNotFound<br />-1305</p> | <p>Il n’existe pas de table ou d’objet de ce type.</p> | 
| <p>JET_errDensityInvalid<br />-1307</p> | <p>La densité d’un fichier ou d’un index est incorrecte.</p> | 
| <p>JET_errTableNotEmpty<br />-1308</p> | <p>La table n’est pas vide.</p> | 
| <p>JET_errInvalidTableId<br />-1310</p> | <p>L’ID de table n’est pas valide.</p> | 
| <p>JET_errTooManyOpenTables<br />-1311</p> | <p>Aucune autre table ne peut être ouverte, même après l’exécution de la tâche de nettoyage interne.</p> | 
| <p>JET_errIllegalOperation<br />-1312</p> | <p>L’opération n’est pas prise en charge sur la table.</p> | 
| <p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />-1313</p> | <p>Impossible d’ouvrir davantage de tables en raison de l’échec de la tentative de nettoyage.</p> | 
| <p>JET_errObjectDuplicate<br />-1314</p> | <p>Le nom de la table ou de l’objet est en cours d’utilisation.</p> | 
| <p>JET_errInvalidObject<br />-1316</p> | <p>L’objet n’est pas valide pour l’opération.</p> | 
| <p>JET_errCannotDeleteTempTable<br />-1317</p> | <p><a href="gg294087(v=exchg.10).md">JetCloseTable</a> doit être utilisé à la place de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> pour supprimer une table temporaire.</p> | 
| <p>JET_errCannotDeleteSystemTable<br />-1318</p> | <p>Tentative non autorisée de suppression d’une table système.</p> | 
| <p>JET_errCannotDeleteTemplateTable<br />-1319</p> | <p>Une tentative non autorisée de suppression d’une table de modèle a été créée.</p> | 
| <p>JET_errExclusiveTableLockRequired<br />-1322</p> | <p>Il doit y avoir un verrou exclusif sur la table.</p> | 
| <p>JET_errFixedDDL<br />-1323</p> | <p>Les opérations DDL sont interdites sur cette table.</p> | 
| <p>JET_errFixedInheritedDDL<br />-1324</p> | <p>Sur une table dérivée, les opérations DDL sont interdites sur la partie héritée du DDL.</p> | 
| <p>JET_errCannotNestDDL<br />-1325</p> | <p>L’imbrication du DDL hiérarchique n’est pas prise en charge actuellement.</p> | 
| <p>JET_errDDLNotInheritable<br />-1326</p> | <p>Une tentative d’héritage d’une DDL a été tentée à partir d’une table qui n’est pas marquée comme table de modèle.</p> | 
| <p>JET_errInvalidSettings<br />-1328</p> | <p>Les paramètres système ont été définis de manière incorrecte.</p> | 
| <p>JET_errClientRequestToStopJetService<br />-1329</p> | <p>Le client a demandé l’arrêt du service.</p> | 
| <p>JET_errCannotAddFixedVarColumnToDerivedTable<br />-1330</p> | <p>La table de modèle a été créée avec l’indicateur NoFixedVarColumnsInDerivedTables défini.</p> | 
| <p>JET_errIndexCantBuild<br />-1401</p> | <p>Échec de la génération de l’index.</p> | 
| <p>JET_errIndexHasPrimary<br />-1402</p> | <p>L’index primaire est déjà défini.</p> | 
| <p>JET_errIndexDuplicate<br />-1403</p> | <p>L’index est déjà défini.</p> | 
| <p>JET_errIndexNotFound<br />-1404</p> | <p>Il n’y a pas d’index de ce type.</p> | 
| <p>JET_errIndexMustStay<br />-1405</p> | <p>Impossible de supprimer l’index cluster.</p> | 
| <p>JET_errIndexInvalidDef<br />-1406</p> | <p>La définition de l’index n’est pas valide.</p> | 
| <p>JET_errInvalidCreateIndex<br />-1409</p> | <p>La création de la description de l’index n’est pas valide.</p> | 
| <p>JET_errTooManyOpenIndexes<br />-1410</p> | <p>La base de données est en dehors des blocs de description d’index.</p> | 
| <p>JET_errMultiValuedIndexViolation<br />-1411</p> | <p>Des clés d’index entre enregistrements non uniques ont été générées pour un index à valeurs multiples.</p> | 
| <p>JET_errIndexBuildCorrupted<br />-1412</p> | <p>Un index secondaire qui reflète correctement l’index primaire n’a pas pu être généré.</p> | 
| <p>JET_errPrimaryIndexCorrupted<br />-1413</p> | <p>L’index primaire est endommagé et la base de données doit être défragmentée.</p> | 
| <p>JET_errSecondaryIndexCorrupted<br />-1414</p> | <p>L’index secondaire est endommagé et la base de données doit être défragmentée.</p> | 
| <p>JET_errInvalidIndexId<br />-1416</p> | <p>L’ID d’index n’est pas valide.</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly<br />-1430</p> | <p>L’index de tuple ne peut être défini que sur un index secondaire.</p> | 
| <p>JET_errIndexTuplesTooManyColumns<br />-1431</p> | <p>La définition d’index de l’index de tuple contient plus de colonnes clés que le moteur de base de données peut prendre en charge.</p><p><strong>Remarque  </strong> L’erreur de JET_errIndexTuplesOneColumnOnly est obsolète et a été remplacée par JET_errIndexTuplesTooManyColumns.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly<br />-1432</p> | <p>L’index de tuple doit être un index non unique.</p> | 
| <p>JET_errIndexTuplesTextBinaryColumnsOnly<br />-1433</p> | <p>Une définition d’index de tuple ne peut contenir que des colonnes clés qui ont des types de colonnes texte ou binaires.</p><p><strong>Remarque  </strong> L’erreur de JET_errIndexTuplesTextColumnsOnly est obsolète et a été remplacée par JET_errIndexTuplesTextBinaryColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed<br />-1434</p> | <p>L’index du tuple n’autorise pas la définition de cbVarSegMac.</p> | 
| <p>JET_errIndexTuplesInvalidLimits<br />-1435</p> | <p>La longueur minimale/maximale du tuple ou le nombre maximal de caractères spécifiés pour un index ne sont pas valides.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex<br />-1436</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ne peut pas être appelé avec l’indicateur JET_bitRetrieveFromIndex défini lors de la récupération d’une colonne sur un index de Tuple.</p> | 
| <p>JET_errIndexTuplesKeyTooSmall<br />-1437</p> | <p>La clé spécifiée ne répond pas à la longueur minimale du tuple.</p> | 
| <p>JET_errColumnLong<br />-1501</p> | <p>La valeur de la colonne est longue.</p> | 
| <p>JET_errColumnNoChunk<br />-1502</p> | <p>Il n’existe pas de ce type de bloc dans une valeur long.</p> | 
| <p>JET_errColumnDoesNotFit<br />-1503</p> | <p>Le champ ne peut pas être contenu dans l’enregistrement.</p> | 
| <p>JET_errNullInvalid<br />-1504</p> | <p>NULL n’est pas valide.</p> | 
| <p>JET_errColumnIllegalNull<br />JET_errNullInvalid</p> | <p>NULL n’est pas valide. Cette erreur est retournée par le gestionnaire d’enregistrements.</p> | 
| <p>JET_errColumnIndexed-1505</p> | <p>La colonne est indexée et ne peut pas être supprimée.</p> | 
| <p>JET_errColumnTooBig-1506</p> | <p>La longueur du champ est supérieure à la longueur maximale autorisée.</p> | 
| <p>JET_errColumnNotFound-1507</p> | <p>Il n’existe aucune colonne de ce type.</p> | 
| <p>JET_errColumnDuplicate-1508</p> | <p>Ce champ est déjà défini.</p> | 
| <p>JET_errMultiValuedColumnMustBeTagged-1509</p> | <p>Une tentative de création d’une colonne à valeurs multiples a été effectuée, mais la colonne n’a pas été marquée.</p> | 
| <p>JET_errColumnRedundant-1510</p> | <p>Une deuxième colonne d’auto-incrémentation ou de version était présente.</p> | 
| <p>JET_errInvalidColumnType-1511</p> | <p>Le type de données de la colonne n’est pas valide.</p> | 
| <p>JET_errTaggedNotNULL-1514</p> | <p>Il n’existe aucune colonne avec balises non NULL.</p> | 
| <p>JET_errNoCurrentIndex-1515</p> | <p>La base de données n’est pas valide, car elle ne contient pas d’index en cours.</p> | 
| <p>JET_errKeyIsMade-1516</p> | <p>La clé est entièrement créée.</p> | 
| <p>JET_errBadColumnId-1517</p> | <p>L’ID de colonne est incorrect.</p> | 
| <p>JET_errBadItagSequence-1518</p> | <p>Il y a un mauvais itagSequence pour la colonne avec balises.</p> | 
| <p>JET_errColumnInRelationship-1519</p> | <p>Une colonne ne peut pas être supprimée, car elle fait partie d’une relation.</p> | 
| <p>JET_errCannotBeTagged-1521</p> | <p>Impossible d’étiqueter l’incrément et la version automatiques.</p> | 
| <p>JET_errDefaultValueTooBig-1524</p> | <p>La valeur par défaut dépasse la taille maximale.</p> | 
| <p>JET_errMultiValuedDuplicate-1525</p> | <p>Une valeur dupliquée a été détectée sur une colonne à valeurs multiples unique.</p> | 
| <p>JET_errLVCorrupted-1526</p> | <p>Une altération s’est produite dans une arborescence de valeurs longues.</p> | 
| <p>JET_errMultiValuedDuplicateAfterTruncation-1528</p> | <p>Une valeur dupliquée a été détectée sur une colonne à valeurs multiples unique une fois que les données ont été normalisées, et la normalisation des données a été tronquée avant la comparaison.</p> | 
| <p>JET_errDerivedColumnCorruption-1529</p> | <p>Il existe une colonne non valide dans la table dérivée.</p> | 
| <p>JET_errInvalidPlaceholderColumn-1530</p> | <p>Une tentative de conversion d’une colonne en espace réservé d’index principal a été effectuée, mais la colonne ne répond pas aux critères requis.</p> | 
| <p>JET_errRecordNotFound-1601</p> | <p>La clé est introuvable.</p> | 
| <p>JET_errRecordNoCopy-1602</p> | <p>Il n’existe aucune mémoire tampon de travail.</p> | 
| <p>JET_errNoCurrentRecord-1603</p> | <p>Aucun enregistrement actif.</p> | 
| <p>JET_errRecordPrimaryChanged-1604</p> | <p>La clé primaire n’est peut-être pas modifiée.</p> | 
| <p>JET_errKeyDuplicate-1605</p> | <p>Une clé dupliquée est incorrecte.</p> | 
| <p>JET_errAlreadyPrepared-1607</p> | <p>Une tentative a été effectuée pour mettre à jour un enregistrement alors qu’une mise à jour d’enregistrement était déjà en cours.</p> | 
| <p>JET_errKeyNotMade-1608</p> | <p>Aucun appel n’a été effectué à <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p> | 
| <p>JET_errUpdateNotPrepared-1609</p> | <p>Aucun appel n’a été effectué à <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p> | 
| <p>JET_errDataHasChanged-1611</p> | <p>Les données ont changé et l’opération a été abandonnée.</p> | 
| <p>JET_errLanguageNotSupported-1619</p> | <p>cette installation de Windows ne prend pas en charge la langue sélectionnée.</p> | 
| <p>JET_errTooManySorts-1701</p> | <p>Le nombre de processus de tri est trop important.</p> | 
| <p>JET_errInvalidOnSort-1702</p> | <p>Une opération non valide s’est produite pendant un tri.</p> | 
| <p>JET_errTempFileOpenError-1803</p> | <p>Impossible d’ouvrir le fichier temporaire.</p> | 
| <p>JET_errTooManyAttachedDatabases-1805</p> | <p>Un trop grand nombre de bases de données sont ouvertes.</p> | 
| <p>JET_errDiskFull-1808</p> | <p>Il n’y a pas d’espace disponible sur le disque.</p> | 
| <p>JET_errPermissionDenied-1809</p> | <p>Autorisation refusée.</p> | 
| <p>JET_errFileNotFound-1811</p> | <p>Ce fichier est introuvable.</p> | 
| <p>JET_errFileInvalidType-1812</p> | <p>Le type de fichier n’est pas valide.</p> | 
| <p>JET_errAfterInitialization-1850</p> | <p>Une restauration ne peut pas être démarrée après l’initialisation.</p> | 
| <p>JET_errLogCorrupted-1852</p> | <p>Les journaux n’ont pas pu être interprétés.</p> | 
| <p>JET_errInvalidOperation-1906</p> | <p>L’opération n’est pas valide.</p> | 
| <p>JET_errAccessDenied-1907</p> | <p>L’accès est refusé.</p> | 
| <p>JET_errTooManySplits-1909</p> | <p>Fractionnement infini.</p> | 
| <p>JET_errSessionSharingViolation-1910</p> | <p>Plusieurs threads utilisent la même session.</p> | 
| <p>JET_errEntryPointNotFound-1911</p> | <p>Impossible de trouver un point d’entrée dans une DLL requise.</p> | 
| <p>JET_errSessionContextAlreadySet-1912</p> | <p>La session spécifiée a déjà un contexte de session défini.</p> | 
| <p>JET_errSessionContextNotSetByThisThread-1913</p> | <p>Une tentative de réinitialisation du contexte de session a été effectuée, mais le thread actuel n’était pas celui d’origine qui définit le contexte de session.</p> | 
| <p>JET_errSessionInUse-1914</p> | <p>Une tentative a été effectuée pour mettre fin à la session en cours d’utilisation.</p> | 
| <p>JET_errRecordFormatConversionFailed-1915</p> | <p>Une erreur interne s’est produite lors d’une conversion de format d’enregistrement dynamique.</p> | 
| <p>JET_errOneDatabasePerSession-1916</p> | <p>Une seule base de données utilisateur ouverte par session est autorisée (comme indiqué par la définition de l’indicateur <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> lors de la création de la base de données).</p> | 
| <p>JET_errRollbackError-1917</p> | <p>Une erreur s’est produite lors de la restauration.</p> | 
| <p>JET_errCallbackFailed-2101</p> | <p>Un appel de fonction de rappel a échoué.</p> | 
| <p>JET_errCallbackNotResolved-2102</p> | <p>Impossible de trouver une fonction de rappel.</p> | 
| <p>JET_errOSSnapshotInvalidSequence-2401</p> | <p>L’API de cliché instantané du système d’exploitation a été utilisée dans une séquence non valide.</p> | 
| <p>JET_errOSSnapshotTimeOut-2402</p> | <p>Le cliché instantané du système d’exploitation s’est terminé avec un délai d’attente.</p> | 
| <p>JET_errOSSnapshotNotAllowed-2403</p> | <p>Le cliché instantané du système d’exploitation n’est pas autorisé, car une sauvegarde ou une récupération dans est en cours.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId-2404</p> | <p>L’opération a échoué, car le handle de cliché instantané du système d’exploitation spécifié n’était pas valide.</p> | 
| <p>JET_errLSCallbackNotSpecified-3000</p> | <p>Une tentative d’utilisation du stockage local a été effectuée sans qu’une fonction de rappel soit spécifiée.</p> | 
| <p>JET_errLSAlreadySet-3001</p> | <p>Une tentative a été effectuée pour définir le stockage local pour un objet déjà défini.</p> | 
| <p>JET_errLSNotSet-3002</p> | <p>Une tentative a été effectuée pour récupérer le stockage local d’un objet pour lequel il n’a pas été défini.</p> | 
| <p>JET_errFileIOSparse-4000</p> | <p>Une opération d’e/s a échoué, car elle a été tentée sur une zone non allouée d’un fichier.</p> | 
| <p>JET_errFileIOBeyondEOF-4001</p> | <p>Une lecture a été émise vers un emplacement situé au-delà de la EOF (les écritures vont développer le fichier).</p> | 
| <p>JET_errFileIOAbort-4002</p> | <p>Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK d’abandonner l’e/s spécifiée.</p> | 
| <p>JET_errFileIORetry-4003</p> | <p>Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK de retenter l’e/s spécifiée.</p> | 
| <p>JET_errFileIOFail-4004</p> | <p>Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK d’effectuer l’échec de l’e/s spécifiée.</p> | 
| <p>JET_errFileCompressed-4005</p> | <p>L’accès en lecture/écriture n’est pas pris en charge sur les fichiers compressés.</p> | 



### <a name="remarks"></a>Remarques

En général, une valeur supérieure à zéro doit être interprétée comme un avertissement, une valeur de zéro doit être interprétée comme une réussite et une valeur inférieure à zéro doit être interprétée comme une erreur. Aucun autre modèle dans ces valeurs, comme des plages de valeurs, ne doit être basé sur une application.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)
