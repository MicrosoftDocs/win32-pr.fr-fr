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
ms.openlocfilehash: a9a30b5e136cdc7e2b570b58e0228bb7fc874a57ec389c3406735e7a481fa898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093699"
---
# <a name="extensible-storage-engine-error-codes"></a>Codes d’erreur du moteur de Stockage Extensible


_**S’applique à :** Windows | Windows Serveurs_

## <a name="extensible-storage-engine-error-codes"></a>Codes d’erreur du moteur de Stockage Extensible

les codes d’erreur (indicateurs) suivants sont utilisés par les fonctions de l’API du moteur d’Stockage Extensible.

Une [JET_ERR](./jet-err.md) valeur de zéro doit être interprétée comme une réussite.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Succès</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess 0</p></td>
<td><p>La fonction a réussi.</p></td>
</tr>
</tbody>
</table>


Une valeur [JET_ERR](./jet-err.md) supérieure à zéro doit être interprétée comme un avertissement.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Avertissements</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnRemainingVersions<br />
321</p></td>
<td><p>La Banque des versions est toujours active. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnUniqueKey<br />
345</p></td>
<td><p>Une recherche sur un index non unique a produit une clé unique. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeparateLongValue<br />
406</p></td>
<td><p>Une colonne de base de données est une valeur long séparée. Cette erreur est retournée par le gestionnaire d’enregistrements.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnExistingLogFileHasBadSignature<br />
558</p></td>
<td><p>La signature du fichier journal existant est incorrecte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnExistingLogFileIsNotContiguous<br />
559</p></td>
<td><p>Le fichier journal existant n’est pas contigu.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSkipThisRecord<br />
564</p></td>
<td><p>Cette erreur est réservée à un usage interne uniquement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTargetInstanceRunning<br />
578</p></td>
<td><p>Le TargetInstance spécifié pour la restauration est en cours d’exécution.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseRepaired<br />
595</p></td>
<td><p>La base de données endommagée a été réparée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull<br />
1004</p></td>
<td><p>La colonne a une valeur <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated<br />
1006</p></td>
<td><p>La mémoire tampon est insuffisante pour les données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached<br />
1007</p></td>
<td><p>La base de données est déjà attachée.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSortOverflow<br />
1009</p></td>
<td><p>Le tri en cours de tentative ne dispose pas de suffisamment de mémoire pour se terminer.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeekNotEqual<br />
1039</p></td>
<td><p>Une correspondance exacte n’a pas été trouvée pendant une recherche.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnRecordFoundGreater<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Une correspondance exacte n’a pas été trouvée pendant une recherche. Cette erreur est retournée par le gestionnaire d’enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnRecordFoundLess<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Une correspondance exacte n’a pas été trouvée pendant une recherche. Cette erreur est retournée par le gestionnaire d’enregistrements.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoErrorInfo<br />
1055</p></td>
<td><p>Il n’y a pas d’informations d’erreur étendues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnNoIdleActivity<br />
1058</p></td>
<td><p>Aucune activité inactive ne s’est produite.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoWriteLock<br />
1067</p></td>
<td><p>Il n’existe aucun verrou d’écriture au niveau de la transaction 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSetNull<br />
1068</p></td>
<td><p>La colonne est définie sur une valeur <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableEmpty<br />
1301</p></td>
<td><p>Une table vide a été ouverte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTableInUseBySystem<br />
1327</p></td>
<td><p>Le nettoyage du système a un curseur ouvert sur la table.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCorruptIndexDeleted<br />
1415</p></td>
<td><p>L’index obsolète doit être supprimé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated<br />
1512</p></td>
<td><p>La longueur maximale est trop grande et a été tronquée.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCopyLongValue<br />
1520</p></td>
<td><p>Une valeur d’objet BLOB a été déplacée de l’enregistrement dans un stockage distinct d’objets BLOB volumineux.</p>
<p><strong>Remarque</strong> Cette erreur est réservée à un usage interne uniquement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSkipped<br />
1531</p></td>
<td><p>Les valeurs de colonne n’ont pas été retournées, car l’ID de colonne ou le membre <em>itagSequence</em> correspondant de la structure <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> qui a été demandée pour l’énumération a la valeur null.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnNotLocal<br />
1532</p></td>
<td><p>Les valeurs de colonne n’ont pas été retournées, car elles n’ont pas pu être reconstruites à partir des données existantes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMoreTags<br />
1533</p></td>
<td><p>Les valeurs de colonne existantes n’ont pas été demandées pour l’énumération.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnTruncated<br />
1534</p></td>
<td><p>La valeur de colonne a été tronquée à la limite de taille demandée pendant l’énumération.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnPresent<br />
1535</p></td>
<td><p>Les valeurs de colonne existent mais n’ont pas été retournées par la demande.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSingleValue<br />
1536</p></td>
<td><p>La valeur de colonne a été retournée dans JET_COLUMNENUM à la suite de la définition de la JET_bitEnumerateCompressOutput.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnDefault<br />
1537</p></td>
<td><p>La valeur de la colonne est définie sur la valeur par défaut de la colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDataHasChanged<br />
1610</p></td>
<td><p>Les données ont changé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnKeyChanged<br />
1618</p></td>
<td><p>Une nouvelle clé est utilisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly<br />
1813</p></td>
<td><p>Le fichier de base de données est en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnIdleFull<br />
1908</p></td>
<td><p>Le registre inactif est plein.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragAlreadyRunning<br />
2000</p></td>
<td><p>Une défragmentation en ligne est déjà en cours d’exécution sur la base de données spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragNotRunning<br />
2001</p></td>
<td><p>Une défragmentation en ligne n’est pas en cours d’exécution sur la base de données spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCallbackNotRegistered<br />
2100</p></td>
<td><p>Une fonction de rappel inexistante n’a pas été inscrite.</p></td>
</tr>
</tbody>
</table>


Une valeur [JET_ERR](./jet-err.md) inférieure à zéro doit être interprétée comme une erreur.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Errors</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnNyi<br />
-1</p></td>
<td><p>La fonction n’est pas encore implémentée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRfsFailure<br />
-100</p></td>
<td><p>Le simulateur d’échec de ressource a échoué.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRfsNotArmed<br />
-101</p></td>
<td><p>Le simulateur d’échec de ressource n’a pas été initialisé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileClose<br />
-102</p></td>
<td><p>Impossible de fermer le fichier.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads<br />
-103</p></td>
<td><p>Le thread n’a pas pu être démarré.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyIO<br />
-105</p></td>
<td><p>Le système est occupé en raison d’un trop grand nombre d’IOs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaskDropped<br />
-106</p></td>
<td><p>Impossible d’exécuter la tâche asynchrone demandée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInternalError<br />
-107</p></td>
<td><p>Une erreur interne irrécupérable s’est produite.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseBufferDependenciesCorrupted<br />
-255</p></td>
<td><p>Les dépendances de mémoire tampon ont été définies de manière incorrecte et un échec de récupération s’est produite.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPreviousVersion<br />
-322</p></td>
<td><p>La version existait déjà et un échec de récupération s’est produite. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageBoundary<br />
-323</p></td>
<td><p>La limite de la page a été atteinte. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyBoundary<br />
-324</p></td>
<td><p>La limite de la clé a été atteinte. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadPageLink<br />
-327</p></td>
<td><p>La base de données est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadBookmark<br />
-328</p></td>
<td><p>Le signet n’a pas d’adresse correspondante dans la base de données. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNTSystemCallFailed<br />
-334</p></td>
<td><p>L’appel au système d’exploitation a échoué. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadParentPageLink<br />
-338</p></td>
<td><p>Une base de données parente est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfSync<br />
-340</p></td>
<td><p>Le cache AvailExt ne correspond pas à l’arborescence B +. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPAvailExtCorrupted<br />
-341</p></td>
<td><p>L’arborescence de l’espace AllAvailExt est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfMemory<br />
-342</p></td>
<td><p>Une erreur de mémoire insuffisante s’est produite lors de l’allocation d’un nœud de cache AvailExt. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPOwnExtCorrupted<br />
-343</p></td>
<td><p>L’arborescence de l’espace OwnExt est endommagée. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeCorrupted<br />
-344</p></td>
<td><p>La valeur dbTime sur la page actuelle est supérieure à la valeur dbTime de la base de données globale. Cette erreur est retournée par le gestionnaire de répertoire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated<br />
-346</p></td>
<td><p>Une tentative de création d’une clé pour une entrée d’index a échoué, car la clé aurait été tronquée et la définition de l’index interdit la troncation de clé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTooBig<br />
-408</p></td>
<td><p>La clé est trop grande. Cette erreur est retournée par le gestionnaire d’enregistrements.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLoggedOperation<br />
-500</p></td>
<td><p>L’opération journalisée ne peut pas être rétablie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogFileCorrupt<br />
-501</p></td>
<td><p>Le fichier journal est endommagé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackupDirectory<br />
-503</p></td>
<td><p>Un répertoire de sauvegarde n’a pas été fourni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupDirectoryNotEmpty<br />
-504</p></td>
<td><p>Le répertoire de sauvegarde n’est pas vide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress<br />
-505</p></td>
<td><p>La sauvegarde est déjà active.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress<br />
-506</p></td>
<td><p>Une restauration est en cours.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingPreviousLogFile<br />
-509</p></td>
<td><p>Le fichier journal est manquant pour le point de vérification.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail<br />
-510</p></td>
<td><p>Une erreur s’est produite lors de l’écriture dans le fichier journal.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDisabledDueToRecoveryFailure<br />
-511</p></td>
<td><p>La tentative d’écriture dans le journal après la récupération a échoué.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotLogDuringRecoveryRedo<br />
-512</p></td>
<td><p>La tentative d’écriture dans le journal pendant le rétablissement de la récupération a échoué.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogGenerationMismatch<br />
-513</p></td>
<td><p>Le nom du fichier journal ne correspond pas au numéro de génération interne.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogVersion<br />
-514</p></td>
<td><p>La version du fichier journal n’est pas compatible avec la version ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogSequence<br />
-515</p></td>
<td><p>L’horodateur dans le journal suivant ne correspond pas à l’horodatage attendu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLoggingDisabled<br />
-516</p></td>
<td><p>Le journal n’est pas actif.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogBufferTooSmall<br />
-517</p></td>
<td><p>Le tampon du journal est trop petit pour la récupération.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEnd<br />
-519</p></td>
<td><p>Le nombre maximal de fichiers journaux a été dépassé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup<br />
-520</p></td>
<td><p>Aucune sauvegarde n’est en cours.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence<br />
-521</p></td>
<td><p>L’appel de sauvegarde est hors séquence.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupNotAllowedYet<br />
-523</p></td>
<td><p>Une sauvegarde ne peut pas être effectuée pour l’instant.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDeleteBackupFileFail<br />
-524</p></td>
<td><p>Un fichier de sauvegarde n’a pas pu être supprimé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMakeBackupDirectoryFail<br />
-525</p></td>
<td><p>Impossible de créer le répertoire temporaire de sauvegarde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackup<br />
-526</p></td>
<td><p>La journalisation circulaire est activée ; Impossible d’effectuer une sauvegarde incrémentielle.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithErrors<br />
-527</p></td>
<td><p>Les données ont été restaurées avec des erreurs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingLogFile<br />
-528</p></td>
<td><p>Le fichier journal actuel est manquant.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDiskFull<br />
-529</p></td>
<td><p>Le disque journal est saturé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogSignature<br />
-530</p></td>
<td><p>La signature d’un fichier journal est incorrecte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadDbSignature<br />
-531</p></td>
<td><p>La signature d’un fichier de base de données est incorrecte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadCheckpointSignature<br />
-532</p></td>
<td><p>La signature d’un fichier de point de contrôle est incorrecte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt<br />
-533</p></td>
<td><p>Le fichier de point de contrôle est introuvable ou endommagé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingPatchPage<br />
-534</p></td>
<td><p>La page du fichier de correctif de base de données est introuvable lors de la récupération.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadPatchPage<br />
-535</p></td>
<td><p>La page du fichier de correctif de base de données n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRedoAbruptEnded<br />
-536</p></td>
<td><p>Le rétablissement s’est soudainement arrêté en raison d’une défaillance soudaine lors de la lecture des journaux à partir du fichier journal.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadSLVSignature<br />
-537</p></td>
<td><p>Cet indicateur est réservé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPatchFileMissing<br />
-538</p></td>
<td><p>La restauration matérielle a détecté qu’un fichier correctif de base de données est manquant dans le jeu de sauvegarde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLogSetMismatch<br />
-539</p></td>
<td><p>La base de données n’appartient pas à l’ensemble actuel de fichiers journaux.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseStreamingFileMismatch<br />
-540</p></td>
<td><p>Cet indicateur est réservé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatch<br />
-541</p></td>
<td><p>La taille réelle du fichier journal ne correspond pas à <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound<br />
-542</p></td>
<td><p>Le fichier de point de contrôle est introuvable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRequiredLogFilesMissing<br />
-543</p></td>
<td><p>Les fichiers journaux requis pour la récupération sont absents.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSoftRecoveryOnBackupDatabase<br />
-544</p></td>
<td><p>Une récupération logicielle va être utilisée sur une base de données de sauvegarde lorsqu’une restauration doit être utilisée à la place.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatchDatabasesConsistent<br />
-545</p></td>
<td><p>Les bases de données ont été récupérées, mais la taille du fichier journal utilisée lors de la récupération ne correspond pas à <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSectorSizeMismatch<br />
-546</p></td>
<td><p>La taille des secteurs du fichier journal ne correspond pas à la taille des secteurs du volume actuel.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />
-547</p></td>
<td><p>Les bases de données ont été récupérées, mais la taille des secteurs du fichier journal (utilisée lors de la récupération) ne correspond pas à la taille des secteurs du volume actuel.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEndDatabasesConsistent<br />
-548</p></td>
<td><p>Les bases de données ont été récupérées, mais toutes les générations de journaux possibles dans la séquence actuelle ont été utilisées. Tous les fichiers journaux et le fichier de point de contrôle doivent être supprimés et les bases de données doivent être sauvegardées avant de continuer.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStreamingDataNotLogged<br />
-549</p></td>
<td><p>Une tentative illégale de relecture d’une opération de lecture de fichier de diffusion en continu a été effectuée, où les données n’étaient pas journalisées. Cela est probablement dû à une tentative de restauration par progression avec la journalisation circulaire activée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseDirtyShutdown<br />
-550</p></td>
<td><p>La base de données n’a pas été arrêtée correctement. Une récupération doit d’abord être exécutée pour terminer correctement les opérations de base de données pour l’arrêt précédent.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>Cette erreur est obsolète et a été remplacée par JET_errDatabaseDirtyShutdown.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errConsistentTimeMismatch<br />
-551</p></td>
<td><p>L’heure de la dernière cohérence pour la base de données n’a pas été mise en correspondance.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabasePatchFileMismatch<br />
-552</p></td>
<td><p>Le fichier de correctif de base de données n’est pas généré à partir de cette sauvegarde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow<br />
-553</p></td>
<td><p>Le numéro de journal de début est trop faible pour la restauration.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh<br />
-554</p></td>
<td><p>Le numéro de journal de début est trop élevé pour la restauration.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errGivenLogFileHasBadSignature<br />
-555</p></td>
<td><p>La signature du fichier journal de restauration est incorrecte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errGivenLogFileIsNotContiguous<br />
-556</p></td>
<td><p>Le fichier journal de restauration n’est pas contigu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingRestoreLogFiles<br />
-557</p></td>
<td><p>Certains fichiers journaux de restauration sont manquants.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup<br />
-560</p></td>
<td><p>La base de données a manqué une sauvegarde complète précédente avant de tenter d’effectuer une sauvegarde incrémentielle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadBackupDatabaseSize<br />
-561</p></td>
<td><p>La taille de la base de données de sauvegarde n’est pas un multiple de la taille de la page de la base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseAlreadyUpgraded<br />
-562</p></td>
<td><p>La tentative actuelle de mise à niveau d’une base de données a été arrêtée, car la base de données est déjà à jour.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIncompleteUpgrade<br />
-563</p></td>
<td><p>La base de données n’a été convertie que partiellement au format actuel. La base de données doit être restaurée à partir d’une sauvegarde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingCurrentLogFiles<br />
-565</p></td>
<td><p>Certains fichiers journaux sont manquants pour la restauration continue.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeTooOld<br />
-566</p></td>
<td><p>L’dbtime sur une page est plus petite que le dbtimeBefore dans l’enregistrement.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDbTimeTooNew<br />
-567</p></td>
<td><p>L’dbtime sur une page est à l’avance du dbtimeBefore dans l’enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingFileToBackup<br />
-569</p></td>
<td><p>Certains fichiers de correctifs de base de données ou de journal étaient manquants pendant la sauvegarde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogTornWriteDuringHardRestore<br />
-570</p></td>
<td><p>Une écriture endommagée a été détectée dans une sauvegarde qui a été définie lors d’une restauration matérielle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogTornWriteDuringHardRecovery<br />
-571</p></td>
<td><p>Une écriture endommagée a été détectée lors d’une récupération matérielle (le journal ne fait pas partie d’un jeu de sauvegarde).</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorruptDuringHardRestore<br />
-573</p></td>
<td><p>Une altération a été détectée dans un jeu de sauvegarde lors d’une restauration matérielle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogCorruptDuringHardRecovery<br />
-574</p></td>
<td><p>Une altération a été détectée pendant la récupération matérielle (le journal ne fait pas partie d’un jeu de sauvegarde).</p></td>
</tr>
<tr class="even">
<td><p>JET_errMustDisableLoggingForDbUpgrade<br />
-575</p></td>
<td><p>Impossible d’activer la journalisation lors de la tentative de mise à niveau d’une base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadRestoreTargetInstance<br />
-577</p></td>
<td><p>Le TargetInstance spécifié pour la restauration n’a pas été trouvé ou les fichiers journaux ne correspondent pas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithoutUndo<br />
-579</p></td>
<td><p>Le moteur de base de données a relu toutes les opérations du journal des transactions pour effectuer une récupération après incident, mais l’appelant a choisi d’arrêter la récupération sans restaurer les mises à jour non validées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabasesNotFromSameSnapshot<br />
-580</p></td>
<td><p>Les bases de données à restaurer ne proviennent pas de la même sauvegarde de clichés instantanés.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSoftRecoveryOnSnapshot<br />
-581</p></td>
<td><p>Il existe une récupération logicielle sur une base de données à partir d’un jeu de sauvegarde de clichés instantanés.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationBufferTooSmall<br />
-601</p></td>
<td><p>La mémoire tampon de traduction Unicode est trop petite.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUnicodeTranslationFail<br />
-602</p></td>
<td><p>Échec de la normalisation Unicode.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeNormalizationNotSupported<br />
-603</p></td>
<td><p>Le système d’exploitation ne prend pas en charge la normalisation Unicode et aucun rappel de normalisation n’a été spécifié.</p></td>
</tr>
<tr class="even">
<td><p>JET_errExistingLogFileHasBadSignature<br />
-610</p></td>
<td><p>La signature du fichier journal existant est incorrecte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExistingLogFileIsNotContiguous<br />
-611</p></td>
<td><p>Un fichier journal existant n’est pas contigu.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure<br />
-612</p></td>
<td><p>Une erreur de somme de contrôle a été trouvée dans le fichier journal lors de la sauvegarde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSLVReadVerifyFailure<br />
-613</p></td>
<td><p>Cet indicateur est réservé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointDepthTooDeep<br />
-614</p></td>
<td><p>Il y a trop de générations en suspens entre le point de contrôle et la génération actuelle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase<br />
-615</p></td>
<td><p>Une récupération matérielle a été tentée sur une base de données qui n’était pas une base de données de sauvegarde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit<br />
-900</p></td>
<td><p>Un paramètre Grbit n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress<br />
-1 000</p></td>
<td><p>Arrêt en cours.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable<br />
-1001</p></td>
<td><p>Cet élément d’API n’est pas pris en charge.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName<br />
-1002</p></td>
<td><p>Un nom non valide est utilisé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter<br />
-1003</p></td>
<td><p>Un paramètre d’API non valide est utilisé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly<br />
-1008</p></td>
<td><p>Une tentative d’attachement à un fichier de base de données en lecture seule a été tentée pour les opérations de lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId<br />
-1010</p></td>
<td><p>Un ID de base de données n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory<br />
-1011</p></td>
<td><p>La mémoire du système est insuffisante.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDatabaseSpace<br />
-1012</p></td>
<td><p>La taille maximale de la base de données a été atteinte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors<br />
-1013</p></td>
<td><p>La table est hors des curseurs.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfBuffers<br />
-1014</p></td>
<td><p>La base de données est en dehors des tampons de page.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyIndexes<br />
-1015</p></td>
<td><p>Le nombre d’index est trop important.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyKeys<br />
-1016</p></td>
<td><p>Le nombre de colonnes dans un index est trop important.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted<br />
-1017</p></td>
<td><p>L’enregistrement a été supprimé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure<br />
-1018</p></td>
<td><p>Une page de base de données contient une erreur de somme de contrôle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageNotInitialized<br />
-1019</p></td>
<td><p>Il y a une page de base de données vide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfFileHandles<br />
-1020</p></td>
<td><p>Il n’y a aucun descripteur de fichier.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO<br />
-1022</p></td>
<td><p>Il y a une erreur d’e/s disque.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath<br />
-1023</p></td>
<td><p>Un chemin d’accès au fichier n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSystemPath<br />
-1024</p></td>
<td><p>Le chemin d’accès au système est incorrect.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogDirectory<br />
-1025</p></td>
<td><p>Le répertoire de journal n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig<br />
-1026</p></td>
<td><p>L’enregistrement est plus grand que la taille maximale.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenDatabases<br />
-1027</p></td>
<td><p>Le nombre de bases de données ouvertes est trop important.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabase<br />
-1028</p></td>
<td><p>Il ne s’agit pas d’un fichier de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized<br />
-1029</p></td>
<td><p>Le moteur de base de données n’a pas été initialisé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAlreadyInitialized<br />
-1030</p></td>
<td><p>Le moteur de base de données est déjà initialisé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInitInProgress<br />
-1031</p></td>
<td><p>Le moteur de base de données est en cours d’initialisation.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied<br />
-1032</p></td>
<td><p>Impossible d’accéder au fichier, car le fichier est verrouillé ou en cours d’utilisation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall<br />
-1038</p></td>
<td><p>La mémoire tampon est insuffisante.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns<br />
-1040</p></td>
<td><p>Trop de colonnes sont définies.</p></td>
</tr>
<tr class="even">
<td><p>JET_errContainerNotEmpty<br />
-1043</p></td>
<td><p>Le conteneur n’est pas vide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidFilename<br />
-1044</p></td>
<td><p>Le nom de fichier n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark<br />
-1045</p></td>
<td><p>Il y a un signet non valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInUse<br />
-1046</p></td>
<td><p>La colonne utilisée se trouve dans un index.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize<br />
-1047</p></td>
<td><p>La mémoire tampon de données ne correspond pas à la taille de colonne.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable<br />
-1048</p></td>
<td><p>La valeur de la colonne ne peut pas être définie.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInUse<br />
-1051</p></td>
<td><p>L’index est en cours d’utilisation.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLinkNotSupported<br />
-1052</p></td>
<td><p>La prise en charge des liens n’est pas disponible.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed<br />
-1053</p></td>
<td><p>Les clés NULL ne sont pas autorisées sur un index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction<br />
-1054</p></td>
<td><p>L’opération doit se produire dans une transaction.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyActiveUsers<br />
-1059</p></td>
<td><p>Le nombre d’utilisateurs de base de données actifs est trop important</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCountry<br />
-1061</p></td>
<td><p>Code de pays non valide ou inconnu.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId<br />
-1062</p></td>
<td><p>ID de langue non valide ou inconnu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCodePage<br />
-1063</p></td>
<td><p>Une page de codes n’est pas valide ou est inconnue.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLCMapStringFlags<br />
-1064</p></td>
<td><p>Des indicateurs non valides sont utilisés pour <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreEntryTooBig<br />
-1065</p></td>
<td><p>Une tentative de création d’une entrée de la Banque des versions (RCE) supérieure à celle d’un compartiment de version a été tentée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />
-1066</p></td>
<td><p>La Banque des versions ne dispose pas de suffisamment de mémoire et la tentative de nettoyage a échoué.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreOutOfMemory<br />
-1069</p></td>
<td><p>La Banque des versions ne dispose pas de suffisamment de mémoire et une tentative de nettoyage a déjà été effectuée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex<br />
-1071</p></td>
<td><p>Les colonnes tiers de confiance et SLV ne peuvent pas être indexées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotDeleted<br />
-1072</p></td>
<td><p>L’enregistrement n’a pas été supprimé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyMempoolEntries<br />
-1073</p></td>
<td><p>Trop d’entrées mempool ont été demandées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfObjectIDs<br />
-1074</p></td>
<td><p>La base de données est en dehors de l’arbre B + ObjectIDs, de sorte qu’une défragmentation hors connexion doit être effectuée pour récupérer des ObjectIds libérés ou inutilisés.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfLongValueIDs<br />
-1075</p></td>
<td><p>Le compteur de l’ID de valeur long a atteint la valeur maximale. Une défragmentation hors connexion doit être effectuée pour récupérer des LongValueIDs libres ou inutilisés.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfAutoincrementValues<br />
-1076</p></td>
<td><p>Le compteur d’incrémentation automatique a atteint la valeur maximale. Une défragmentation hors connexion ne sera pas en mesure de récupérer des valeurs d’incrémentation automatique libres ou inutilisées.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDbtimeValues<br />
-1077</p></td>
<td><p>Le compteur dbtime a atteint la valeur maximale. Une défragmentation hors connexion doit être effectuée pour récupérer des valeurs dbtime libres ou inutilisées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSequentialIndexValues<br />
-1078</p></td>
<td><p>Un compteur d’index séquentiels a atteint la valeur maximale. Une défragmentation hors connexion doit être effectuée pour récupérer des valeurs SequentialIndex libres ou inutilisées.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode<br />
-1080</p></td>
<td><p>Le mode d’instance unique est activé pour cet appel multi-instance.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode<br />
-1081</p></td>
<td><p>L’appel à instance unique est activé pour le mode multi-instance.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSystemParamsAlreadySet<br />
-1082</p></td>
<td><p>Les paramètres globaux du système ont déjà été définis.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemPathInUse<br />
-1083</p></td>
<td><p>Le chemin d’accès système est déjà utilisé par une autre instance de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFilePathInUse<br />
-1084</p></td>
<td><p>Le chemin d’accès du fichier journal est déjà utilisé par une autre instance de base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempPathInUse<br />
-1085</p></td>
<td><p>Le chemin d’accès à la base de données temporaire est déjà utilisé par une autre instance de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse<br />
-1086</p></td>
<td><p>Le nom de l’instance est déjà utilisé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable<br />
-1090</p></td>
<td><p>Cette instance ne peut pas être utilisée car elle a rencontré une erreur irrécupérable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseUnavailable<br />
-1091</p></td>
<td><p>Impossible d’utiliser cette base de données, car elle a rencontré une erreur irrécupérable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />
-1092</p></td>
<td><p>Cette instance ne peut pas être utilisée car elle a rencontré une erreur log-Disk-Full lors de l’exécution d’une opération (par exemple, une restauration de transaction) qui n’a pas pu tolérer d’échec.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfSessions<br />
-1101</p></td>
<td><p>La base de données est en dehors des sessions.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict<br />
-1102</p></td>
<td><p>Le verrou d’écriture a échoué en raison de l’existence d’un verrou d’écriture en attente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep<br />
-1103</p></td>
<td><p>Les transactions sont imbriquées trop profondément.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid<br />
-1104</p></td>
<td><p>Un descripteur de session n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflictPrimaryIndex<br />
-1105</p></td>
<td><p>Une mise à jour a été tentée sur un index principal non validé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction<br />
-1108</p></td>
<td><p>L’opération n’est pas autorisée dans une transaction.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackRequired<br />
-1109</p></td>
<td><p>La transaction en cours doit être restaurée. Elle ne peut pas être validée et une nouvelle ne peut pas être démarrée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly<br />
-1110</p></td>
<td><p>Une transaction en lecture seule a tenté de modifier la base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionWriteConflict<br />
-1111</p></td>
<td><p>Tentative de remplacement du même enregistrement par deux curseurs différents dans la même session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBigForBackwardCompatibility<br />
-1112</p></td>
<td><p>L’enregistrement est trop grand s’il est représenté dans un format de base de données à partir d’une version précédente de jet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotMaterializeForwardOnlySort<br />
-1113</p></td>
<td><p>La table temporaire n’a pas pu être créée en raison de paramètres qui sont en conflit avec JET_bitTTForwardOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSesidTableIdMismatch<br />
-1114</p></td>
<td><p>Le descripteur de session ne peut pas être utilisé avec l’ID de table, car il n’a pas été utilisé pour le créer.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance<br />
-1115</p></td>
<td><p>Le descripteur d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadLostFlushVerifyFailure<br />
-1119</p></td>
<td><p>La page de base de données lue à partir du disque avait une écriture précédente non représentée sur la page. disponible sur Windows 8 et versions ultérieures pour le client, et Windows Server 2012 et versions ultérieures pour le serveur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate<br />
-1201</p></td>
<td><p>La base de données existe déjà.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse<br />
-1202</p></td>
<td><p>Base de données en cours d’utilisation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound<br />
-1203</p></td>
<td><p>Il n’existe aucune base de données de ce type.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidName<br />
-1204</p></td>
<td><p>Le nom de la base de données n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages<br />
-1205</p></td>
<td><p>Le nombre de pages est incorrect.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted<br />
-1206</p></td>
<td><p>Il n’existe pas de fichier de base de données ou de base de données endommagée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked<br />
-1207</p></td>
<td><p>La base de données est verrouillée en mode exclusif.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDisableVersioning<br />
-1208</p></td>
<td><p>Le contrôle de version de cette base de données ne peut pas être désactivé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseVersion<br />
-1209</p></td>
<td><p>Le moteur de base de données est incompatible avec la base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase200Format<br />
-1210</p></td>
<td><p>La base de données est dans un format plus ancien (200). Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini. Windows Client NT uniquement.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format<br />
-1211</p></td>
<td><p>La base de données est dans un format plus ancien (400). Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini. Windows Client NT uniquement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format<br />
-1212</p></td>
<td><p>La base de données est dans un format plus ancien (500). Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini. Windows Client NT uniquement.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch<br />
-1213</p></td>
<td><p>La taille de la page de la base de données ne correspond pas au moteur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances<br />
-1214</p></td>
<td><p>Aucune instance de base de données supplémentaire ne peut être démarrée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation<br />
-1215</p></td>
<td><p>Une autre instance de base de données utilise cette base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAttachedDatabaseMismatch<br />
-1216</p></td>
<td><p>Une pièce jointe de base de données en attente a été détectée au début ou à la fin de la récupération, mais la base de données est manquante ou ne correspond pas aux informations de la pièce jointe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPath<br />
-1217</p></td>
<td><p>Le chemin d’accès au fichier de base de données spécifié n’est pas autorisé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIdInUse<br />
-1218</p></td>
<td><p>Un ID qui est déjà en cours d’utilisation est assigné à une base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errForceDetachNotAllowed<br />
-1219</p></td>
<td><p>Le détachement forcé est autorisé uniquement après l’arrêt du détachement normal en raison d’une erreur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCatalogCorrupted<br />
-1220</p></td>
<td><p>Une altération a été détectée dans le catalogue.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPartiallyAttachedDB<br />
-1221</p></td>
<td><p>La base de données n’est attachée que partiellement et l’opération d’attachement ne peut pas être effectuée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseSignInUse<br />
-1222</p></td>
<td><p>La base de données avec la même signature est déjà en cours d’utilisation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorruptedNoRepair<br />
-1224</p></td>
<td><p>La base de données est endommagée, mais aucune réparation n’est autorisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateDbVersion<br />
-1225</p></td>
<td><p>Le moteur de base de données a tenté de relire une opération créer une base de données à partir du journal des transactions mais a échoué en raison d’une version incompatible de cette opération.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableLocked<br />
-1302</p></td>
<td><p>La table est verrouillée en mode exclusif.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate<br />
-1303</p></td>
<td><p>La table existe déjà.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse<br />
-1304</p></td>
<td><p>La table est en cours d’utilisation et ne peut pas être verrouillée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound<br />
-1305</p></td>
<td><p>Il n’existe pas de table ou d’objet de ce type.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid<br />
-1307</p></td>
<td><p>La densité d’un fichier ou d’un index est incorrecte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableNotEmpty<br />
-1308</p></td>
<td><p>La table n’est pas vide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidTableId<br />
-1310</p></td>
<td><p>L’ID de table n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables<br />
-1311</p></td>
<td><p>Aucune autre table ne peut être ouverte, même après l’exécution de la tâche de nettoyage interne.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation<br />
-1312</p></td>
<td><p>L’opération n’est pas prise en charge sur la table.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />
-1313</p></td>
<td><p>Impossible d’ouvrir davantage de tables en raison de l’échec de la tentative de nettoyage.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectDuplicate<br />
-1314</p></td>
<td><p>Le nom de la table ou de l’objet est en cours d’utilisation.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidObject<br />
-1316</p></td>
<td><p>L’objet n’est pas valide pour l’opération.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTempTable<br />
-1317</p></td>
<td><p><a href="gg294087(v=exchg.10).md">JetCloseTable</a> doit être utilisé à la place de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> pour supprimer une table temporaire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeleteSystemTable<br />
-1318</p></td>
<td><p>Tentative non autorisée de suppression d’une table système.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable<br />
-1319</p></td>
<td><p>Une tentative non autorisée de suppression d’une table de modèle a été créée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired<br />
-1322</p></td>
<td><p>Il doit y avoir un verrou exclusif sur la table.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL<br />
-1323</p></td>
<td><p>Les opérations DDL sont interdites sur cette table.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL<br />
-1324</p></td>
<td><p>Sur une table dérivée, les opérations DDL sont interdites sur la partie héritée du DDL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL<br />
-1325</p></td>
<td><p>L’imbrication du DDL hiérarchique n’est pas prise en charge actuellement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable<br />
-1326</p></td>
<td><p>Une tentative d’héritage d’une DDL a été tentée à partir d’une table qui n’est pas marquée comme table de modèle.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSettings<br />
-1328</p></td>
<td><p>Les paramètres système ont été définis de manière incorrecte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService<br />
-1329</p></td>
<td><p>Le client a demandé l’arrêt du service.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotAddFixedVarColumnToDerivedTable<br />
-1330</p></td>
<td><p>La table de modèle a été créée avec l’indicateur NoFixedVarColumnsInDerivedTables défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexCantBuild<br />
-1401</p></td>
<td><p>Échec de la génération de l’index.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary<br />
-1402</p></td>
<td><p>L’index primaire est déjà défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate<br />
-1403</p></td>
<td><p>L’index est déjà défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound<br />
-1404</p></td>
<td><p>Il n’y a pas d’index de ce type.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexMustStay<br />
-1405</p></td>
<td><p>Impossible de supprimer l’index cluster.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef<br />
-1406</p></td>
<td><p>La définition de l’index n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateIndex<br />
-1409</p></td>
<td><p>La création de la description de l’index n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes<br />
-1410</p></td>
<td><p>La base de données est en dehors des blocs de description d’index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation<br />
-1411</p></td>
<td><p>Des clés d’index entre enregistrements non uniques ont été générées pour un index à valeurs multiples.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexBuildCorrupted<br />
-1412</p></td>
<td><p>Un index secondaire qui reflète correctement l’index primaire n’a pas pu être généré.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted<br />
-1413</p></td>
<td><p>L’index primaire est endommagé et la base de données doit être défragmentée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted<br />
-1414</p></td>
<td><p>L’index secondaire est endommagé et la base de données doit être défragmentée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId<br />
-1416</p></td>
<td><p>L’ID d’index n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly<br />
-1430</p></td>
<td><p>L’index de tuple ne peut être défini que sur un index secondaire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTooManyColumns<br />
-1431</p></td>
<td><p>La définition d’index de l’index de tuple contient plus de colonnes clés que le moteur de base de données peut prendre en charge.</p>
<p><strong>Remarque  </strong> L’erreur de JET_errIndexTuplesOneColumnOnly est obsolète et a été remplacée par JET_errIndexTuplesTooManyColumns.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly<br />
-1432</p></td>
<td><p>L’index de tuple doit être un index non unique.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextBinaryColumnsOnly<br />
-1433</p></td>
<td><p>Une définition d’index de tuple ne peut contenir que des colonnes clés qui ont des types de colonnes texte ou binaires.</p>
<p><strong>Remarque  </strong> L’erreur de JET_errIndexTuplesTextColumnsOnly est obsolète et a été remplacée par JET_errIndexTuplesTextBinaryColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed<br />
-1434</p></td>
<td><p>L’index du tuple n’autorise pas la définition de cbVarSegMac.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits<br />
-1435</p></td>
<td><p>La longueur minimale/maximale du tuple ou le nombre maximal de caractères spécifiés pour un index ne sont pas valides.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex<br />
-1436</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ne peut pas être appelé avec l’indicateur JET_bitRetrieveFromIndex défini lors de la récupération d’une colonne sur un index de Tuple.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall<br />
-1437</p></td>
<td><p>La clé spécifiée ne répond pas à la longueur minimale du tuple.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnLong<br />
-1501</p></td>
<td><p>La valeur de la colonne est longue.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNoChunk<br />
-1502</p></td>
<td><p>Il n’existe pas de ce type de bloc dans une valeur long.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDoesNotFit<br />
-1503</p></td>
<td><p>Le champ ne peut pas être contenu dans l’enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid<br />
-1504</p></td>
<td><p>NULL n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull<br />
JET_errNullInvalid</p></td>
<td><p>NULL n’est pas valide. Cette erreur est retournée par le gestionnaire d’enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIndexed-1505</p></td>
<td><p>La colonne est indexée et ne peut pas être supprimée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig-1506</p></td>
<td><p>La longueur du champ est supérieure à la longueur maximale autorisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound-1507</p></td>
<td><p>Il n’existe aucune colonne de ce type.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDuplicate-1508</p></td>
<td><p>Ce champ est déjà défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged-1509</p></td>
<td><p>Une tentative de création d’une colonne à valeurs multiples a été effectuée, mais la colonne n’a pas été marquée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnRedundant-1510</p></td>
<td><p>Une deuxième colonne d’auto-incrémentation ou de version était présente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType-1511</p></td>
<td><p>Le type de données de la colonne n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTaggedNotNULL-1514</p></td>
<td><p>Il n’existe aucune colonne avec balises non NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex-1515</p></td>
<td><p>La base de données n’est pas valide, car elle ne contient pas d’index en cours.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade-1516</p></td>
<td><p>La clé est entièrement créée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId-1517</p></td>
<td><p>L’ID de colonne est incorrect.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence-1518</p></td>
<td><p>Il y a un mauvais itagSequence pour la colonne avec balises.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInRelationship-1519</p></td>
<td><p>Une colonne ne peut pas être supprimée, car elle fait partie d’une relation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged-1521</p></td>
<td><p>Impossible d’étiqueter l’incrément et la version automatiques.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDefaultValueTooBig-1524</p></td>
<td><p>La valeur par défaut dépasse la taille maximale.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate-1525</p></td>
<td><p>Une valeur dupliquée a été détectée sur une colonne à valeurs multiples unique.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLVCorrupted-1526</p></td>
<td><p>Une altération s’est produite dans une arborescence de valeurs longues.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicateAfterTruncation-1528</p></td>
<td><p>Une valeur dupliquée a été détectée sur une colonne à valeurs multiples unique une fois que les données ont été normalisées, et la normalisation des données a été tronquée avant la comparaison.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDerivedColumnCorruption-1529</p></td>
<td><p>Il existe une colonne non valide dans la table dérivée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPlaceholderColumn-1530</p></td>
<td><p>Une tentative de conversion d’une colonne en espace réservé d’index principal a été effectuée, mais la colonne ne répond pas aux critères requis.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotFound-1601</p></td>
<td><p>La clé est introuvable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNoCopy-1602</p></td>
<td><p>Il n’existe aucune mémoire tampon de travail.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord-1603</p></td>
<td><p>Aucun enregistrement actif.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged-1604</p></td>
<td><p>La clé primaire n’est peut-être pas modifiée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate-1605</p></td>
<td><p>Une clé dupliquée est incorrecte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared-1607</p></td>
<td><p>Une tentative a été effectuée pour mettre à jour un enregistrement alors qu’une mise à jour d’enregistrement était déjà en cours.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade-1608</p></td>
<td><p>Aucun appel n’a été effectué à <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared-1609</p></td>
<td><p>Aucun appel n’a été effectué à <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDataHasChanged-1611</p></td>
<td><p>Les données ont changé et l’opération a été abandonnée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLanguageNotSupported-1619</p></td>
<td><p>cette installation de Windows ne prend pas en charge la langue sélectionnée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts-1701</p></td>
<td><p>Le nombre de processus de tri est trop important.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOnSort-1702</p></td>
<td><p>Une opération non valide s’est produite pendant un tri.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempFileOpenError-1803</p></td>
<td><p>Impossible d’ouvrir le fichier temporaire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases-1805</p></td>
<td><p>Un trop grand nombre de bases de données sont ouvertes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull-1808</p></td>
<td><p>Il n’y a pas d’espace disponible sur le disque.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied-1809</p></td>
<td><p>Autorisation refusée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound-1811</p></td>
<td><p>Ce fichier est introuvable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileInvalidType-1812</p></td>
<td><p>Le type de fichier n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAfterInitialization-1850</p></td>
<td><p>Une restauration ne peut pas être démarrée après l’initialisation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorrupted-1852</p></td>
<td><p>Les journaux n’ont pas pu être interprétés.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation-1906</p></td>
<td><p>L’opération n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAccessDenied-1907</p></td>
<td><p>L’accès est refusé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySplits-1909</p></td>
<td><p>Fractionnement infini.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation-1910</p></td>
<td><p>Plusieurs threads utilisent la même session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEntryPointNotFound-1911</p></td>
<td><p>Impossible de trouver un point d’entrée dans une DLL requise.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionContextAlreadySet-1912</p></td>
<td><p>La session spécifiée a déjà un contexte de session défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextNotSetByThisThread-1913</p></td>
<td><p>Une tentative de réinitialisation du contexte de session a été effectuée, mais le thread actuel n’était pas celui d’origine qui définit le contexte de session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionInUse-1914</p></td>
<td><p>Une tentative a été effectuée pour mettre fin à la session en cours d’utilisation.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordFormatConversionFailed-1915</p></td>
<td><p>Une erreur interne s’est produite lors d’une conversion de format d’enregistrement dynamique.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOneDatabasePerSession-1916</p></td>
<td><p>Une seule base de données utilisateur ouverte par session est autorisée (comme indiqué par la définition de l’indicateur <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> lors de la création de la base de données).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError-1917</p></td>
<td><p>Une erreur s’est produite lors de la restauration.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackFailed-2101</p></td>
<td><p>Un appel de fonction de rappel a échoué.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCallbackNotResolved-2102</p></td>
<td><p>Impossible de trouver une fonction de rappel.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSequence-2401</p></td>
<td><p>L’API de cliché instantané du système d’exploitation a été utilisée dans une séquence non valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut-2402</p></td>
<td><p>Le cliché instantané du système d’exploitation s’est terminé avec un délai d’attente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed-2403</p></td>
<td><p>Le cliché instantané du système d’exploitation n’est pas autorisé, car une sauvegarde ou une récupération dans est en cours.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId-2404</p></td>
<td><p>L’opération a échoué, car le handle de cliché instantané du système d’exploitation spécifié n’était pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified-3000</p></td>
<td><p>Une tentative d’utilisation du stockage local a été effectuée sans qu’une fonction de rappel soit spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet-3001</p></td>
<td><p>Une tentative a été effectuée pour définir le stockage local pour un objet déjà défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSNotSet-3002</p></td>
<td><p>Une tentative a été effectuée pour récupérer le stockage local d’un objet pour lequel il n’a pas été défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOSparse-4000</p></td>
<td><p>Une opération d’e/s a échoué, car elle a été tentée sur une zone non allouée d’un fichier.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIOBeyondEOF-4001</p></td>
<td><p>Une lecture a été émise vers un emplacement situé au-delà de la EOF (les écritures vont développer le fichier).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOAbort-4002</p></td>
<td><p>Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK d’abandonner l’e/s spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIORetry-4003</p></td>
<td><p>Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK de retenter l’e/s spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOFail-4004</p></td>
<td><p>Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK d’effectuer l’échec de l’e/s spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileCompressed-4005</p></td>
<td><p>L’accès en lecture/écriture n’est pas pris en charge sur les fichiers compressés.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Remarques

En général, une valeur supérieure à zéro doit être interprétée comme un avertissement, une valeur de zéro doit être interprétée comme une réussite et une valeur inférieure à zéro doit être interprétée comme une erreur. Aucun autre modèle dans ces valeurs, comme des plages de valeurs, ne doit être basé sur une application.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)
