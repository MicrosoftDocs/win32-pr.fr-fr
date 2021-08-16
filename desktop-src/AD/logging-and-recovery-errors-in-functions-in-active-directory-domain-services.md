---
title: Erreurs de journalisation et de récupération dans les fonctions de Active Directory Domain Services
description: Cette rubrique répertorie les valeurs de retour d’erreur de journalisation et de récupération pour les fonctions de Active Directory Domain Services.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- Active Directory les erreurs de journalisation et de récupération AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b267b359b5244fddc0e8a9b2ddfbfb5d6e5f9ab0a7e647683d44759f8a7261b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186590"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Erreurs de journalisation et de récupération dans les fonctions de Active Directory Domain Services

Cette rubrique répertorie les valeurs de retour d’erreur de journalisation et de récupération pour les fonctions de Active Directory Domain Services.



| Valeur                                | Description                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | Le fichier journal est endommagé.                                                                                                         |
| **hrNoBackupDirectory**              | Aucun répertoire de sauvegarde n’a été spécifié.                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | Le répertoire de sauvegarde n’est pas vide.                                                                                               |
| **hrBackupInProgress**               | La sauvegarde est active.                                                                                                                |
| **hrMissingPreviousLogFile**         | Un fichier journal est manquant pour le point de contrôle.                                                                                        |
| **hrLogWriteFail**                   | Impossible d’écrire dans le fichier journal.                                                                                                 |
| **hrBadLogVersion**                  | la version du fichier journal n’est pas compatible avec la version de la base de données du Service d’annuaire Windows NT/Windows 2000 (NTDS). |
| **hrInvalidLogSequence**             | L’horodatage dans le journal suivant ne correspond pas à ce qui était attendu.                                                                 |
| **hrLoggingDisabled**                | Le journal n’est pas actif.                                                                                                           |
| **hrLogBufferTooSmall**              | Le tampon du journal est trop petit pour être récupéré.                                                                                     |
| **hrLogSequenceEnd**                 | Le nombre maximal de fichiers journaux a été dépassé.                                                                               |
| **hrNoBackup**                       | Aucune sauvegarde n’est en cours.                                                                                                  |
| **hrInvalidBackupSequence**          | L’appel de sauvegarde est hors séquence.                                                                                              |
| **hrBackupNotAllowedYet**            | Impossible d’effectuer une sauvegarde maintenant.                                                                                                  |
| **hrDeleteBackupFileFail**           | Impossible de supprimer le fichier de sauvegarde.                                                                                                |
| **hrMakeBackupDirectoryFail**        | Impossible de créer un répertoire temporaire de sauvegarde.                                                                                     |
| **hrInvalidBackup**                  | Une sauvegarde incrémentielle ne peut pas être effectuée lorsque l’enregistrement circulaire est activé.                                                      |
| **hrRecoveredWithErrors**            | Des erreurs se sont produites lors du processus de réparation.                                                                               |
| **hrMissingLogFile**                 | Le fichier journal actuel est manquant.                                                                                                 |
| **hrLogDiskFull**                    | Le disque journal est saturé.                                                                                                            |
| **hrBadLogSignature**                | Un fichier journal est endommagé.                                                                                                           |
| **hrBadDbSignature**                 | Un fichier de base de données est endommagé.                                                                                                      |
| **hrBadCheckpointSignature**         | Un fichier de point de contrôle est endommagé.                                                                                                    |
| **hrCheckpointCorrupt**              | Un fichier de point de contrôle est introuvable ou endommagé.                                                                       |
| **hrDatabaseInconsistent**           | La base de données est endommagée.                                                                                                         |
| **hrConsistentTimeMismatch**         | Il y a une incompatibilité dans l’heure de la dernière cohérence de la base de données.                                                                      |
| **hrPatchFileMismatch**              | Le fichier correctif n’est pas généré à partir de cette sauvegarde.                                                                                |
| **hrRestoreLogTooLow**               | Le numéro de journal de début est trop faible pour la restauration.                                                                              |
| **hrRestoreLogTooHigh**              | Le numéro de journal de début est trop élevé pour la restauration.                                                                             |
| **hrGivenLogFileHasBadSignature**    | Le fichier journal téléchargé à partir de la bande est endommagé.                                                                                |
| **hrGivenLogFileIsNotContiguous**    | Impossible de trouver un fichier journal obligatoire après le téléchargement de la bande.                                                               |
| **hrMissingRestoreLogFiles**         | Les données ne sont pas entièrement restaurées car certains fichiers journaux sont manquants.                                                               |
| **hrExistingLogFileHasBadSignature** | Le fichier journal dans le chemin d’accès du fichier journal est endommagé.                                                                                    |
| **hrExistingLogFileIsNotContiguous** | Impossible de trouver un fichier journal obligatoire dans le chemin d’accès du fichier journal.                                                                        |
| **hrMissingFullBackup**              | La base de données a manqué une sauvegarde complète précédente avant la sauvegarde incrémentielle.                                                        |
| **hrBadBackupDatabaseSize**          | La taille de la base de données de sauvegarde doit être un multiple de 4000 (4096 octets).                                                                |
| **hrTermInProgress**                 | La base de données est en cours d’arrêt.                                                                                                 |
| **hrFeatureNotAvailable**            | La fonctionnalité n’est pas disponible.                                                                                                    |
| **hrInvalidName**                    | Le nom n'est pas valide.                                                                                                             |
| **hrInvalidParameter**               | Le paramètre n’est pas valide.                                                                                                        |
| **hrColumnNull**                     | La valeur de la colonne est null.                                                                                                 |
| **hrBufferTruncated**                | La mémoire tampon est insuffisante pour les données.                                                                                                |
| **hrDatabaseAttached**               | La base de données est déjà attachée.                                                                                                |
| **hrInvalidDatabaseId**              | L’ID de base de données n’est pas valide.                                                                                                      |
| **hrOutOfMemory**                    | La mémoire de l’ordinateur est insuffisante.                                                                                                   |
| **hrOutOfDatabaseSpace**             | La base de données a atteint la taille maximale de 16 Go.                                                                              |
| **hrOutOfCursors**                   | Curseurs hors table.                                                                                                            |
| **hrOutOfBuffers**                   | Tampons de pages de base de données hors de la base de données.                                                                                                    |
| **hrTooManyIndexes**                 | Le nombre d’index est trop important.                                                                                                      |
| **hrTooManyKeys**                    | Le nombre de colonnes dans un index est trop important.                                                                                          |
| **hrRecordDeleted**                  | L’enregistrement a été supprimé.                                                                                                     |
| **hrReadVerifyFailure**              | Une erreur de vérification de lecture s’est produite.                                                                                              |
| **hrOutOfFileHandles**               | Descripteurs de fichiers insuffisants.                                                                                                             |
| **hrDiskIO**                         | Une erreur d’e/s disque s’est produite.                                                                                                       |
| **hrInvalidPath**                    | Le chemin d’accès au fichier n’est pas valide.                                                                                                 |
| **hrRecordTooBig**                   | L’enregistrement a dépassé la taille maximale.                                                                                        |
| **hrTooManyOpenDatabases**           | Le nombre de bases de données ouvertes est trop important.                                                                                               |
| **hrInvalidDatabase**                | Le fichier n’est pas un fichier de base de données.                                                                                                 |
| **hrNotInitialized**                 | La base de données n’a pas encore été appelée.                                                                                                 |
| **hrAlreadyInitialized**             | La base de données a déjà été appelée.                                                                                                 |
| **hrFileAccessDenied**               | Impossible d’accéder au fichier.                                                                                                       |
| **hrBufferTooSmall**                 | La mémoire tampon est insuffisante.                                                                                                         |
| **hrSeekNotEqual**                   | SeekLE ou SeekGE ne peut pas trouver une correspondance exacte.                                                                              |
| **hrTooManyColumns**                 | Trop de colonnes sont définies.                                                                                              |
| **hrContainerNotEmpty**              | Le conteneur n’est pas vide.                                                                                                      |
| **hrInvalidFilename**                | Le nom de fichier n’est pas valide.                                                                                                         |
| **hrInvalidBookmark**                | Le signet n’est pas valide.                                                                                                         |
| **hrColumnInUse**                    | La colonne est utilisée dans un index.                                                                                                  |
| **hrInvalidBufferSize**              | La mémoire tampon de données ne correspond pas à la taille de colonne.                                                                                  |
| **hrColumnNotUpdatable**             | Impossible de définir la valeur de la colonne.                                                                                                  |
| **hrIndexInUse**                     | L’index est en cours d’utilisation.                                                                                                             |
| **hrNullKeyDisallowed**              | Les clés NULL ne sont pas autorisées sur un index.                                                                                           |
| **hrNotInTransaction**               | L'opération doit être effectuée dans une transaction.                                                                                      |
| **hrNoIdleActivity**                 | Aucune activité inactive ne s’est produite.                                                                                                       |
| **hrTooManyActiveUsers**             | Le nombre d’utilisateurs de base de données actifs est trop important.                                                                                        |
| **hrInvalidCountry**                 | Le code du pays ou de la région n’est pas connu ou n’est pas valide.                                                                    |
| **hrInvalidLanguageId**              | L’ID de langue n’est pas connu ou n’est pas valide.                                                                               |
| **hrInvalidCodePage**                | La page de codes n’est pas connue ou n’est pas valide.                                                                                 |
| **hrNoWriteLock**                    | Il n’existe aucun verrou d’écriture au niveau de la transaction 0.                                                                                   |
| **hrColumnSetNull**                  | La valeur de la colonne est définie sur null.                                                                                                 |
| **hrVersionStoreOutOfMemory**        | LMaxVerPages dépassée (XJET uniquement).                                                                                           |
| **hrCurrencyStackOutOfMemory**       | Hors des curseurs.                                                                                                                  |
| **hrOutOfSessions**                  | Sessions insuffisantes.                                                                                                                 |
| **hrWriteConflict**                  | Le verrou d’écriture a échoué en raison d’un verrou d’écriture en attente.                                                                          |
| **hrTransTooDeep**                   | Les transactions sont imbriquées trop profondément.                                                                                          |
| **hrInvalidSesid**                   | Le descripteur de session n’est pas valide.                                                                                                   |
| **hrSessionWriteConflict**           | Une autre session a une version privée de la page.                                                                               |
| **hrInTransaction**                  | L’opération n’est pas autorisée dans une transaction.                                                                               |
| **hrDatabaseDuplicate**              | La base de données existe déjà.                                                                                                     |
| **hrDatabaseInUse**                  | La base de données est en cours d’utilisation.                                                                                                          |
| **hrDatabaseNotFound**               | La base de données n’existe pas.                                                                                                     |
| **hrDatabaseInvalidName**            | Le nom de la base de données n’est pas valide.                                                                                                    |
| **hrDatabaseInvalidPages**           | Le nombre de pages n’est pas valide.                                                                                                  |
| **hrDatabaseCorrupted**              | Le fichier de base de données est endommagé ou introuvable.                                                                          |
| **hrDatabaseLocked**                 | La base de données est verrouillée.                                                                                                          |
| **hrTableEmpty**                     | Une table vide a été ouverte.                                                                                                       |
| **hrTableLocked**                    | La table est verrouillée.                                                                                                             |
| **hrTableDuplicate**                 | La table existe déjà.                                                                                                        |
| **hrTableInUse**                     | Impossible de verrouiller la table, car elle est déjà en cours d’utilisation.                                                                           |
| **hrObjectNotFound**                 | La table ou l’objet n’existe pas.                                                                                              |
| **hrCannotRename**                   | Impossible de renommer le fichier temporaire.                                                                                             |
| **hrDensityInvalid**                 | La densité du fichier/de l’index n’est pas valide.                                                                                               |
| **hrTableNotEmpty**                  | Impossible de définir l’index cluster.                                                                                            |
| **hrInvalidTableId**                 | L’ID de table n’est pas valide.                                                                                                         |
| **hrTooManyOpenTables**              | Impossible d’ouvrir davantage de tables.                                                                                                  |
| **hrIllegalOperation**               | L’opération n’est pas prise en charge sur les tables.                                                                                        |
| **hrObjectDuplicate**                | Le nom de la table ou de l’objet est déjà utilisé.                                                                                  |
| **hrInvalidObject**                  | L’objet n’est pas valide pour l’opération.                                                                                             |
| **hrIndexCantBuild**                 | Impossible de créer un index cluster.                                                                                               |
| **hrIndexHasPrimary**                | L’index primaire est déjà défini.                                                                                            |
| **hrIndexDuplicate**                 | L’index est déjà défini.                                                                                                    |
| **hrIndexNotFound**                  | L’index n’existe pas.                                                                                                        |
| **hrIndexMustStay**                  | Impossible de supprimer un index cluster.                                                                                              |
| **hrIndexInvalidDef**                | La définition de l’index n’est pas conforme.                                                                                                 |
| **hrIndexHasClustered**              | L’index cluster est déjà défini.                                                                                          |
| **hrCreateIndexFailed**              | Impossible de créer l’index, car une erreur s’est produite lors de la création d’une table.                                                     |
| **hrTooManyOpenIndexes**             | Blocs de description d’index insuffisants.                                                                                                 |
| **hrColumnLong**                     | La valeur de la colonne est trop longue.                                                                                                    |
| **hrColumnDoesNotFit**               | Le champ ne peut pas être contenu dans l’enregistrement.                                                                                            |
| **hrNullInvalid**                    | La valeur ne peut pas être null.                                                                                                        |
| **hrColumnIndexed**                  | Suppression impossible, car la colonne est indexée.                                                                                  |
| **hrColumnTooBig**                   | La longueur du champ dépasse la longueur maximale de 255 octets.                                                                 |
| **hrColumnNotFound**                 | Impossible de trouver la colonne.                                                                                                       |
| **hrColumnDuplicate**                | Le champ est déjà défini.                                                                                                    |
| **hrColumn2ndSysMaint**              | Une seule colonne d’incrémentation automatique ou de version est autorisée par table.                                                                  |
| **hrInvalidColumnType**              | Le type de données de la colonne n’est pas valide.                                                                                                 |
| **hrColumnMaxTruncated**             | La colonne a été tronquée, car elle dépasse la longueur maximale de 255 octets.                                                    |
| **hrColumnCannotIndex**              | Impossible d’indexer une colonne de valeur longue.                                                                                             |
| **hrTaggedNotNULL**                  | Les colonnes avec balises ne peuvent pas être null.                                                                                                   |
| **hrNoCurrentIndex**                 | L’entrée n’est pas valide sans un index actuel.                                                                                    |
| **hrKeyIsMade**                      | La clé est terminée.                                                                                                             |
| **hrBadColumnId**                    | L’ID de colonne est incorrect.                                                                                                      |
| **hrBadItagSequence**                | Un identificateur d’instance est incorrect pour une colonne à valeurs multiples.                                                                     |
| **hrCannotBeTagged**                 | AutoIncrement et version ne peuvent pas avoir plusieurs valeurs.                                                                                 |
| **hrRecordNotFound**                 | Impossible de trouver la clé.                                                                                                          |
| **hrNoCurrentRecord**                | La devise n’est pas sur un enregistrement.                                                                                                 |
| **hrRecordClusteredChanged**         | Une clé en cluster ne peut pas être modifiée.                                                                                               |
| **hrKeyDuplicate**                   | La clé existe déjà.                                                                                                          |
| **hrAlreadyPrepared**                | L’entrée actuelle a déjà été copiée ou effacée.                                                                            |
| **hrKeyNotMade**                     | Aucune clé n’a été établie.                                                                                                                 |
| **hrUpdateNotPrepared**              | La mise à jour n’a pas été préparée.                                                                                                         |
| **hrwrnDataHasChanged**              | Les données ont changé.                                                                                                                |
| **hrerrDataHasChanged**              | L’opération a été abandonnée, car les données ont été modifiées.                                                                            |
| **hrKeyChanged**                     | Déplacé vers une nouvelle clé.                                                                                                              |
| **hrTooManySorts**                   | Le nombre de processus de tri est trop important.                                                                                               |
| **hrInvalidOnSort**                  | Une opération qui n’est pas valide s’est produite dans le tri.                                                                               |
| **hrTempFileOpenError**              | Impossible d’ouvrir le fichier temporaire.                                                                                               |
| **hrTooManyAttachedDatabases**       | Trop de bases de données sont ouvertes.                                                                                               |
| **hrDiskFull**                       | Le disque est plein.                                                                                                                |
| **hrPermissionDenied**               | Autorisation refusée.                                                                                                            |
| **hrFileNotFound**                   | Impossible de trouver le fichier.                                                                                                         |
| **hrFileOpenReadOnly**               | Le fichier de base de données est en lecture seule.                                                                                                  |
| **hrAfterInitialization**            | Restauration impossible après l’initialisation.                                                                                          |
| **hrLogCorrupted**                   | Les fichiers journaux de la base de données sont endommagés.                                                                                              |
| **hrInvalidOperation**               | L’opération n’est pas valide.                                                                                                        |
| **hrAccessDenied**                   | L’accès est refusé.                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Success](success.md)
</dt> <dt>

[Erreurs de sauvegarde dans Active Directory Domain Services](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Erreurs système dans Active Directory Domain Services](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Erreurs du gestionnaire de répertoires](directory-manager-errors.md)
</dt> <dt>

[Valeurs de retour pour les fonctions dans Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




