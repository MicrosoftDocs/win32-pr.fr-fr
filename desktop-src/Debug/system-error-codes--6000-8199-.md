---
description: Décrit les codes d’erreur 6000-8199 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Codes d’erreur système (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: d24a165798f0d4bf8a3ed534880cd3f9ad1f2b8b85d072e8a4d7aae8e6345508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131659"
---
# <a name="system-error-codes-6000-8199"></a>Codes d’erreur système (6000-8199)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 6000 à 8199). Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**\_échec du chiffrement de l’erreur \_**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



Le fichier spécifié n’a pas pu être chiffré.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_échec du déchiffrement de l’erreur \_**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



Impossible de déchiffrer le fichier spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**fichier d’erreur \_ \_ chiffré**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



Le fichier spécifié est chiffré et l’utilisateur n’a pas la possibilité de le déchiffrer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERREUR \_ aucune \_ stratégie de récupération \_**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



Aucune stratégie de récupération de chiffrement valide n’est configurée pour ce système.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERREUR \_ non \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



Le pilote de chiffrement requis n’est pas chargé pour ce système.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERREUR \_ EFS incorrect \_**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



Le fichier a été chiffré avec un autre pilote de chiffrement que celui actuellement chargé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERREUR \_ aucune \_ \_ clé utilisateur**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



Aucune clé EFS n’est définie pour l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**fichier d’erreur \_ \_ non \_ chiffré**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



Le fichier spécifié n’est pas chiffré.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERREUR lors de l' \_ \_ exportation du \_ format**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



Le fichier spécifié n’est pas dans le format d’exportation EFS défini.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**fichier d’erreur \_ \_ en lecture \_ seule**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



Le fichier spécifié est en lecture seule.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERREUR dans le \_ répertoire \_ EFS non \_ autorisé**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



Le répertoire a été désactivé pour le chiffrement.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERREUR \_ \_ serveur EFS \_ non \_ approuvé**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



Le serveur n’est pas approuvé pour l’opération de chiffrement à distance.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERREUR \_ de \_ stratégie de récupération incorrecte \_**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



La stratégie de récupération configurée pour ce système contient un certificat de récupération non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERREUR \_ EFS \_ ALG \_ \_ trop \_ volumineux**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



L’algorithme de chiffrement utilisé sur le fichier source a besoin d’une mémoire tampon de clé supérieure à celle du fichier de destination.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**le \_ volume d’erreurs \_ ne \_ prend pas en charge \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



La partition de disque ne prend pas en charge le chiffrement de fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERREUR \_ EFS \_ désactivée**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Cet ordinateur est désactivé pour le chiffrement de fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERREUR \_ \_ \_ non \_ prise en charge par la version EFS**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Un système plus récent est nécessaire pour déchiffrer ce fichier chiffré.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERREUR \_ de \_ chiffrement de la \_ réponse du serveur non valide \_ \_ CS**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



Le serveur distant a envoyé une réponse non valide pour un fichier ouvert avec le chiffrement côté client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERREUR \_ de \_ chiffrement du \_ serveur non pris en charge par le chiffrement cs \_**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



Le chiffrement côté client n’est pas pris en charge par le serveur distant, même s’il prétend le prendre en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERREUR \_ du \_ chiffrement du \_ \_ fichier chiffré existant \_ du CS**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



Le fichier est chiffré et doit être ouvert en mode de chiffrement côté client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERREUR \_ cs \_ chiffrement du \_ nouveau \_ \_ fichier chiffré**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



Un nouveau fichier chiffré est créé et un $EFS doit être fourni.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERREUR \_ du \_ fichier de chiffrement cs \_ \_ non \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



Le client SMB a demandé un FSCTL CSE sur un fichier non-CSE.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**la \_ stratégie de chiffrement des erreurs \_ refuse l' \_ \_ opération**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



L’opération demandée a été bloquée par la stratégie. Pour plus d’informations, contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERREUR \_ aucun \_ serveur de navigateur \_ \_ trouvé**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



La liste des serveurs de ce groupe de travail n’est pas disponible actuellement.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**\_service sched \_ E \_ non \_ LOCALSYSTEM**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



Le service de Planificateur de tâches doit être configuré pour s’exécuter dans le compte système pour fonctionner correctement. Des tâches individuelles peuvent être configurées pour s’exécuter dans d’autres comptes.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**secteur du journal des erreurs \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



Le service de journalisation a rencontré un secteur de journal non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**parité du secteur du journal des erreurs \_ \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



Le service de journalisation a rencontré un secteur de journal avec parité de bloc non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**Journal des erreurs- \_ \_ secteur \_ remappé**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



Le service de journalisation a rencontré un secteur de journal remappé.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**bloc du journal des erreurs \_ \_ \_ incomplet**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



Le service de journalisation a rencontré un bloc de journal partiel ou incomplet.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ plage non valide du journal des erreurs \_**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



Le service de journalisation a rencontré une tentative d’accès aux données en dehors de la plage de journal active.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**blocs de journal des erreurs \_ \_ \_ épuisés**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



Les mémoires tampons de tri de l’utilisateur du service de journalisation sont épuisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**contexte de lecture du journal des erreurs \_ \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



Le service de journalisation a rencontré une tentative de lecture à partir d’une zone de marshaling avec un contexte de lecture non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**redémarrage du journal des erreurs \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



Le service de journalisation a rencontré une zone de redémarrage du journal non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_version du \_ bloc du journal des erreurs \_**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



Le service de journalisation a rencontré une version de bloc de journal non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**bloc du journal des erreurs \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



Le service de journalisation a rencontré un bloc de journal non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**MODE de lecture du journal des erreurs \_ \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



Le service de journalisation a rencontré une tentative de lecture du journal avec un mode de lecture non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**Journal des erreurs- \_ \_ \_ redémarrage non**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



Le service de journalisation a rencontré un flux de journal sans zone de reprise.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**\_métadonnées du journal des erreurs \_ \_ endommagées**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



Le service de journalisation a rencontré un fichier de métadonnées endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**\_métadonnées du journal des erreurs \_ \_ non valides**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



Le service de journalisation a rencontré un fichier de métadonnées qui n’a pas pu être créé par le système de fichiers journaux.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**\_métadonnées du journal des erreurs \_ \_ incohérentes**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



Le service de journalisation a rencontré un fichier de métadonnées avec des données incohérentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**réservation du journal des erreurs \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



Le service de journalisation a rencontré une tentative d’allocation ou de suppression d’espace de réservation.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**erreur \_ de \_ suppression du journal des erreurs \_**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



Le service de journalisation ne peut pas supprimer le fichier journal ou le conteneur du système de fichiers.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**limite du conteneur du journal des erreurs \_ \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



Le service de journalisation a atteint le nombre maximal de conteneurs autorisés alloués à un fichier journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**journal \_ des erreurs- \_ début \_ du \_ Journal**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



Le service de journalisation a tenté de lire ou d’écrire vers l’arrière au-delà du début du journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**stratégie du journal des erreurs \_ \_ \_ déjà \_ installée**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



La stratégie du journal n’a pas pu être installée car une stratégie du même type est déjà présente.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**stratégie du journal des erreurs \_ \_ \_ non \_ installée**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



La stratégie de journalisation en question n’a pas été installée au moment de la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**stratégie du journal des erreurs \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



Le jeu de stratégies installé sur le journal n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflit de \_ stratégie du journal des erreurs \_**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Une stratégie sur la connexion en question A empêché l’exécution de l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_fin de \_ l' \_ archivage épinglé du journal des erreurs \_**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



Impossible de récupérer l’espace du journal car le journal est épinglé par la fin de l’archivage.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**enregistrement du journal des erreurs \_ \_ \_ inexistant**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



L’enregistrement du journal n’est pas un enregistrement dans le fichier journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**enregistrements du journal des erreurs \_ \_ \_ réservés \_ non valides**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



Le nombre d’enregistrements de journal réservés ou l’ajustement du nombre d’enregistrements de journal réservés n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**espace du journal des erreurs \_ \_ \_ réservé \_ non valide**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



L’espace du journal réservé ou la modification de l’espace du journal n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**fin du journal des erreurs \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Une fin ou base d’archive nouvelle ou existante du journal actif n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**Journal des erreurs \_ \_ complet**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



L’espace du journal est épuisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERREUR \_ Impossible \_ de \_ redimensionner le \_ Journal**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



Le journal n’a pas pu être défini à la taille demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**Journal des erreurs \_ \_ multiplexé**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



Le journal est multiplexé, aucune écriture directe dans le journal physique n’est autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**Journal des erreurs \_ \_ dédié**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



L’opération a échoué, car le journal est un journal dédié.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_ \_ Archive du journal \_ des erreurs non \_ en \_ cours**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



L’opération requiert un contexte d’archivage.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ Archive du journal \_ des erreurs en \_ cours**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



Archivage des journaux en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**Journal des erreurs \_ \_ éphémère**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



L’opération nécessite un journal non éphémère, mais le journal est éphémère.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**le \_ Journal des erreurs \_ ne dispose pas de \_ suffisamment de \_ conteneurs**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



Le journal doit avoir au moins deux conteneurs pour pouvoir être lu ou écrit.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**Journal des erreurs \_ \_ client \_ déjà \_ inscrit**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Un client de journal a déjà été inscrit sur le flux.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**Journal des erreurs \_ \_ client \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



Un client de journal n’a pas été inscrit sur le flux.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ Gestionnaire complet du journal \_ des erreurs en \_ cours**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



Une demande a déjà été effectuée pour gérer la condition de journal saturé.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**\_échec de \_ lecture du conteneur du journal des erreurs \_ \_**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



Le service de journalisation a rencontré une erreur lors de la tentative de lecture d’un conteneur de journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**échec de l’écriture du conteneur du \_ Journal des erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



Le service de journalisation a rencontré une erreur lors de la tentative d’écriture dans un conteneur de journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**échec de l’ouverture du conteneur du \_ Journal des erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



Le service de journalisation a rencontré une erreur lors de la tentative d’ouverture d’un conteneur de journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**État du conteneur du journal des erreurs \_ \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



Le service de journalisation a rencontré un état de conteneur non valide lors de la tentative d’action demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**État du journal des erreurs \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



Le service de journalisation n’est pas dans l’état approprié pour effectuer une action demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**Journal des erreurs \_ \_ épinglé**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



Impossible de récupérer l’espace du journal car le journal est épinglé.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_échec du \_ vidage des métadonnées du journal des \_ Erreurs \_**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Le vidage des métadonnées du journal a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**Journal des erreurs- \_ \_ sécurité incohérente \_**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



La sécurité du journal et de ses conteneurs est incohérente.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**\_échec du \_ vidage du \_ Journal des erreurs \_**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



Des enregistrements ont été ajoutés au journal ou des modifications de réservation ont été apportées, mais le journal n’a pas pu être vidé.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ réservation épinglée du journal des erreurs \_**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



Le journal est épinglé en raison d’une réservation consommant la plus grande partie de l’espace du journal. Libérez des enregistrements réservés pour libérer de l’espace.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERREUR \_ de \_ transaction non valide**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



Le descripteur de transaction associé à cette opération n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**TRANSACTION d’erreur \_ \_ non \_ active**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



L’opération demandée a été effectuée dans le contexte d’une transaction qui n’est plus active.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**demande de transaction d’erreur \_ \_ \_ non \_ valide**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



L’opération demandée n’est pas valide sur l’objet de transaction dans son état actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**TRANSACTION d’erreur \_ \_ non \_ demandée**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



L’appelant a appelé une API de réponse, mais la réponse n’est pas attendue car le gestionnaire de la requête n’a pas émis la demande correspondante à l’appelant.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**TRANSACTION d’erreur \_ \_ déjà \_ abandonnée**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



Il est trop tard pour effectuer l’opération demandée, car la transaction a déjà été abandonnée.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**TRANSACTION d’erreur \_ \_ déjà \_ validée**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



Il est trop tard pour effectuer l’opération demandée, car la transaction a déjà été validée.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**\_échec de \_ l’initialisation du gestionnaire de l’erreur \_**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



Le gestionnaire de transactions n’a pas pu être initialisé correctement. Les opérations traitées ne sont pas prises en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERREUR \_ RESOURCEMANAGER \_ lecture \_ seule**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



Le ResourceManager spécifié n’a apporté aucune modification ou mise à jour à la ressource dans le cadre de cette transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**TRANSACTION d’erreur \_ \_ non \_ jointe**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



Le gestionnaire de ressources a tenté de préparer une transaction qui n’a pas été correctement jointe.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**l’erreur de la \_ transaction \_ supérieure \_ existe**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



L’objet de transaction a déjà une inscription supérieure, et l’appelant a tenté une opération qui aurait créé un nouveau supérieur. Seul un enrôlement supérieur est autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERREUR \_ le \_ protocole \_ CRM \_ existe déjà**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



Le gestionnaire de transactions a essayé d’inscrire un protocole qui existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**échec de la propagation de la transaction d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



La tentative de propagation de la transaction a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERREUR \_ de \_ protocole \_ CRM \_ introuvable**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



Le protocole de propagation demandé n’a pas été inscrit en tant que CRM.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**la \_ transaction d’erreur \_ est une \_ mémoire tampon de Marshall non valide \_**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



Le format de la mémoire tampon transmise à PushTransaction ou PullTransaction n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERREUR \_ transaction en cours \_ \_ non \_ valide**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



Le contexte de transaction actuel associé au thread n’est pas un handle valide pour un objet de transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_transaction d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



Impossible d’ouvrir l’objet de transaction spécifié, car il est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERREUR \_ RESOURCEMANAGER \_ \_ introuvable**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



Impossible d’ouvrir l’objet ResourceManager spécifié, car il est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**INSCRIPTION d’erreur \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



Impossible d’ouvrir l’objet d’inscription spécifié, car il est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERREUR \_ TRANSACTIONMANAGER \_ \_ introuvable**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



L’objet TransactionManager spécifié n’a pas pu être ouvert, car il est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERREUR \_ TRANSACTIONMANAGER \_ non \_ connecté**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



Impossible de créer ou d’ouvrir l’objet spécifié, car son TransactionManager associé n’est pas en ligne. Le TransactionManager doit être entièrement en ligne en appelant RecoverTransactionManager pour effectuer une récupération à la fin de son fichier journal avant que les objets de sa transaction ou de ses espaces de noms ResourceManager puissent être ouverts. En outre, les erreurs d’écriture d’enregistrements dans son fichier journal peuvent entraîner la mise hors connexion d’un TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERREUR \_ du \_ nom de récupération du TRANSACTIONMANAGER. \_ \_**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



L’TransactionManager spécifié n’a pas pu créer les objets contenus dans son fichier journal dans l’espace de noms ob. Par conséquent, l’TransactionManager n’a pas pu être récupéré.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**TRANSACTION d’erreur \_ \_ non \_ racine**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



L’appel pour créer une inscription supérieure sur cet objet de transaction n’a pas pu aboutir, car l’objet de transaction spécifié pour l’inscription est une branche subordonnée de la transaction. Seule la racine de la transaction peut être inscrite en tant que supérieur.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**objet de transaction d’erreur \_ \_ \_ expiré**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Étant donné que le gestionnaire de transactions ou le gestionnaire de ressources associé a été fermé, le descripteur n’est plus valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**réponse de la transaction d’erreur \_ \_ \_ non \_ inscrite**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



L’opération spécifiée n’a pas pu être effectuée sur cet enrôlement supérieur, car l’inscription n’a pas été créée avec la réponse d’achèvement correspondante dans le NotificationMask.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**l’enregistrement de la transaction d’erreur est \_ \_ \_ trop \_ long**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



Impossible d’effectuer l’opération spécifiée, car l’enregistrement qui serait enregistré était trop long. Cela peut se produire pour deux raisons : soit il y a trop d’enlistions sur cette transaction, soit le RecoveryInformation combiné qui est enregistré pour le compte de ces enlistions est trop long.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**\_transaction implicite d’erreur \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



La transaction implicite n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERREUR d’intégrité de la \_ transaction non \_ \_ respectée**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



Le gestionnaire de transactions du noyau devait abandonner ou oublier la transaction, car elle a bloqué la progression vers l’avant.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERREUR \_ d' \_ incompatibilité d’identité TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



L’identité TransactionManager qui a été fournie ne correspondait pas à celle enregistrée dans le fichier journal de l’TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**l’erreur \_ RM \_ ne peut pas \_ être \_ figée \_ pour l' \_ instantané**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



Cette opération d’instantané ne peut pas continuer, car un gestionnaire de ressources de transaction ne peut pas être figé dans son état actuel. Recommencez.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**la \_ transaction d’erreur \_ doit \_ WRITETHROUGH**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



La transaction ne peut pas être inscrite dans avec le EnlistmentMask spécifié, car la transaction a déjà terminé la phase de prépréparation. Pour garantir l’exactitude, ResourceManager doit basculer vers un mode d’écriture et arrêter la mise en cache des données dans cette transaction. L’inscription pour uniquement les phases de transaction suivantes peut encore échouer.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**TRANSACTION d’erreur \_ \_ non \_ supérieure**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



La transaction n’a pas d’inscription supérieure.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**erreur heuristique d’erreur d' \_ \_ endommagement \_**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



La tentative de validation de la transaction est terminée, mais il est possible qu’une partie de l’arborescence des transactions n’ait pas été validée en raison de l’heuristique. Par conséquent, il est possible que certaines données modifiées dans la transaction ne soient pas validées, ce qui entraîne une incohérence transactionnelle. Si possible, vérifiez la cohérence des données associées.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERREUR de \_ conflit transactionnel \_**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



La fonction a tenté d’utiliser un nom qui est réservé pour être utilisé par une autre transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERREUR \_ RM \_ non \_ active**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



La prise en charge des transactions dans le gestionnaire de ressources spécifié n’est pas démarrée ou a été arrêtée en raison d’une erreur.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERREUR \_ de \_ métadonnées RM \_ endommagées**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



Les métadonnées de la RM ont été endommagées. Le RM ne fonctionnera pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**Répertoire d’erreurs \_ \_ non \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



Le répertoire spécifié ne contient pas de gestionnaire de ressources.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**TRANSACTIONS d’erreur \_ \_ à distance non prises en charge \_**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



Le serveur ou partage distant ne prend pas en charge les opérations de fichiers transactionnelles.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**taille du journal des erreurs \_ \_ \_ taille non valide \_**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



La taille de journal demandée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**l' \_ objet d’erreur \_ n' \_ \_ existe plus**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



L’objet (fichier, flux, lien) correspondant au descripteur a été supprimé par une restauration de point de enregistrement de transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**le \_ flux d’erreurs \_ MINIVERSION est \_ \_ introuvable**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



Le fichier miniversion spécifié est introuvable pour ce fichier Traité ouvert.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**MINIVERSION de flux d’erreurs \_ \_ \_ non \_ valide**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



Le fichier spécifié miniversion a été trouvé mais n’a pas été validé. La cause la plus probable est la restauration d’un point de enregistrement de transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERREUR \_ MINIVERSION \_ inaccessible \_ à partir de la \_ \_ transaction spécifiée**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Un miniversion peut uniquement être ouvert dans le contexte de la transaction qui l’a créé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERREUR \_ Impossible \_ \_ d’ouvrir \_ MINIVERSION \_ avec \_ intention de modification**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



Il n’est pas possible d’ouvrir un miniversion avec l’accès en modification.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERREUR \_ Impossible de \_ créer \_ plus de \_ flux \_ MINIVERSIONS**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



Il n’est pas possible de créer d’autres miniversions pour ce flux.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de version de fichier distant \_**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



Le serveur distant a envoyé un numéro de version ou un FID qui ne correspond pas à un fichier ouvert avec des transactions.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**le \_ descripteur d’erreur \_ n' \_ est plus \_ valide**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



Le descripteur a été invalidé par une transaction. La cause la plus probable est la présence d’un mappage de mémoire sur un fichier ou d’un descripteur ouvert lorsque la transaction se termine ou est restaurée sur un point d’enregistrement.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERREUR \_ aucune \_ \_ métadonnée TxF**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



Il n’y a pas de métadonnées de transaction sur le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**CORRUPTION du journal des erreurs \_ \_ \_ détectée**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



Les données du journal sont endommagées.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERREUR \_ Impossible \_ \_ de récupérer avec le \_ handle \_ ouvert**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



Impossible de récupérer le fichier, car un descripteur est toujours ouvert dessus.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERREUR \_ RM \_ déconnectée**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



Le résultat de la transaction n’est pas disponible, car le gestionnaire de ressources qui en est responsable s’est déconnecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**INSCRIPTION d’erreur \_ \_ non \_ supérieure**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



La demande a été rejetée, car l’inscription en question n’est pas une inscription supérieure.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**récupération d’erreur \_ \_ non \_ nécessaire**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



Le gestionnaire de ressources de transaction est déjà cohérent. La récupération n’est pas nécessaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERREUR \_ RM \_ déjà \_ démarrée**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



Le gestionnaire de ressources de transaction a déjà été démarré.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**l' \_ identité du fichier d’erreur \_ n’est \_ pas \_ persistante**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



Impossible d’ouvrir le fichier de façon transactionnelle, car son identité dépend du résultat d’une transaction non résolue.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERREUR \_ Impossible de \_ rompre la \_ \_ dépendance transactionnelle**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



L’opération ne peut pas être effectuée, car une autre transaction dépend du fait que cette propriété ne changera pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERREUR de déconnexion de la \_ \_ \_ limite inter RM \_**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



L’opération implique un seul fichier avec deux gestionnaires de ressources transactionnels et n’est donc pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERREUR \_ TxF \_ dir \_ non \_ vide**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



Le répertoire de $Txf doit être vide pour que cette opération aboutisse.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**des \_ transactions INCERTAINES erronées \_ \_ existent**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



L’opération laisse un gestionnaire de ressources transactionnelles dans un état incohérent et n’est donc pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERREUR du gestionnaire de mémoire \_ \_ volatile**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



L’opération n’a pas pu aboutir car le gestionnaire de transactions n’a pas de journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERREUR de restauration de la \_ \_ minuterie \_ expirée**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



Une restauration n’a pas pu être planifiée, car une restauration précédemment planifiée a déjà été exécutée ou a été mise en file d’attente pour l’exécution.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERREUR de l' \_ \_ attribut TxF \_ endommagé**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



L’attribut de métadonnées transactionnelles sur le fichier ou le répertoire est endommagé et illisible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERREUR \_ EFS \_ non \_ autorisée \_ dans la \_ transaction**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



L’opération de chiffrement n’a pas pu aboutir car une transaction est active.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERREUR \_ transaction \_ Open \_ non \_ autorisée**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



Cet objet ne peut pas être ouvert dans une transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**échec de la croissance du journal des erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Une tentative de création d’espace dans le journal du gestionnaire des ressources transactionnelles a échoué. L’état de l’échec a été enregistré dans le journal des événements.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERREUR de \_ mappage des transactions \_ \_ distantes non prises en charge \_**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



Le mappage de mémoire (création d’une section mappée) d’un fichier distant sous une transaction n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERREUR \_ de \_ métadonnées TxF \_ déjà \_ présentes**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



Les métadonnées de transaction sont déjà présentes dans ce fichier et ne peuvent pas être remplacées.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**\_rappels d’étendue de transaction d’erreur \_ \_ \_ non \_ définis**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



Une étendue de transaction n’a pas pu être entrée, car le gestionnaire de portée n’a pas été initialisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**PROMOTION de la transaction d’erreur \_ \_ requise \_**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



La promotion était nécessaire pour permettre à Resource Manager de s’inscrire, mais la transaction a été définie pour l’interdire.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERREUR \_ Impossible \_ d’exécuter le \_ fichier \_ dans la \_ transaction**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Ce fichier est ouvert pour modification dans une transaction non résolue et peut être ouvert pour une exécution uniquement par un lecteur traité.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**TRANSACTIONS d’erreur \_ \_ non \_ figées**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



La demande de libération des transactions gelées a été ignorée, car les transactions n’avaient pas été figées précédemment.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**\_ \_ blocage de la transaction d’erreur \_ en \_ cours**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



Les transactions ne peuvent pas être figées, car un blocage est déjà en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERREUR \_ non \_ snapshot du \_ volume**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



Le volume cible n’est pas un volume d’instantané. Cette opération n’est valide que sur un volume monté en tant qu’instantané.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERREUR \_ aucun \_ point \_ de enregistrement avec les \_ \_ fichiers ouverts**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



L’opération de point d’enregistrement a échoué car des fichiers sont ouverts sur la transaction. Cela n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERREUR de \_ réparation de données \_ perdues \_**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



Windows a détecté une altération dans un fichier et que ce fichier a été réparé depuis. Une perte de données est peut-être survenue.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERREUR \_ épars \_ non \_ autorisée \_ dans la \_ transaction**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



L’opération éparse n’a pas pu aboutir car une transaction est active sur le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de l’identité du gestionnaire \_**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



L’appel pour créer un objet TransactionManager a échoué, car l’identité de TM stockée dans le fichier journal ne correspond pas à l’identité TM qui a été transmise en tant qu’argument.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERREUR de \_ section flottante \_**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



Des e/s ont été tentées sur un objet de section qui a été dissocié à la suite d’une transaction se terminant. Il n’y a pas de données valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**l’erreur \_ ne peut pas \_ accepter le \_ \_ travail traité**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



Le gestionnaire de ressources transactionnelles ne peut pas actuellement accepter le travail transactionnel en raison d’une condition temporaire telle que des ressources insuffisantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERREUR \_ Impossible d' \_ abandonner les \_ transactions**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



Le gestionnaire de ressources de transaction a trop d’transactions en suspens qui n’ont pas pu être abandonnés. Le gestionnaire de ressources de transaction a été arrêté.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERREUR \_ de \_ clusters incorrects**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



L’opération n’a pas pu aboutir en raison de clusters incorrects sur le disque.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_compression \_ d’erreur non \_ autorisée dans la \_ \_ transaction**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



L’opération de compression n’a pas pu aboutir car une transaction est active sur le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**\_intégrité du volume d’erreurs \_**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



L’opération n’a pas pu aboutir car le volume est impropre. Exécutez CHKDSK et réessayez.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERREUR \_ aucun \_ \_ suivi \_ de lien dans la \_ transaction**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



Impossible d’effectuer l’opération de suivi des liaisons, car une transaction est active.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_l’opération \_ d’erreur n’est pas \_ prise en charge \_ dans la \_ transaction**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Cette opération ne peut pas être effectuée dans une transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERREUR \_ de \_ handle expiré**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



Le descripteur n’est plus correctement associé à sa transaction. Il a peut-être été ouvert dans un gestionnaire de ressources de transaction qui a été ensuite forcé à redémarrer. Fermez le descripteur et ouvrez-en un nouveau.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**TRANSACTION d’erreur \_ \_ non \_ inscrite**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



Impossible d’effectuer l’opération spécifiée, car le gestionnaire de ressources n’est pas inscrit dans la transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERREUR \_ nom de la \_ station de \_ nom \_ non valide**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



Le nom de session spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERREUR \_ CTX \_ le \_ PD non valide**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



Le pilote de protocole spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERREUR \_ CTX \_ PD \_ non \_ trouvée**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



Le pilote de protocole spécifié est introuvable dans le chemin d’accès système.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERREUR \_ CTX \_ WD \_ \_ introuvable**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



Le pilote de connexion de terminal spécifié est introuvable dans le chemin d’accès système.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERREUR \_ CTX \_ Impossible de \_ créer l' \_ \_ entrée EventLog**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



Impossible de créer une clé de Registre pour la journalisation des événements pour cette session.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERREUR \_ de \_ \_ collision de nom de service CTX \_**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Un service du même nom existe déjà sur le système.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERREUR \_ CTX \_ fermeture \_ en attente**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



Une opération de fermeture est en attente sur la session.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERREUR \_ CTX \_ non \_ OUTBUF**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



Aucune mémoire tampon de sortie libre n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERREUR \_ de \_ modem CTX \_ fichier INF \_ \_ introuvable**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



Le MODEM. Fichier INF introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERREUR \_ CTX \_ MODEMNAME non valide \_**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



Le nom du modem est introuvable dans le fichier MODEM. INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**erreur \_ de \_ réponse du modem CTX \_ \_**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



Le modem n’a pas accepté la commande qui lui a été envoyée. Vérifiez que le nom du modem configuré correspond au modem attaché.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERREUR \_ de \_ \_ réponse \_ du modem CTX**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



Le modem n’a pas répondu à la commande qui lui a été envoyée. Vérifiez que le modem est correctement câblé et sous tension.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERREUR \_ de \_ réponse du modem CTX \_ \_ non \_ transporteur**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



La détection de porteuse a échoué ou le transporteur a été abandonné en raison d’une déconnexion.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERREUR \_ de \_ réponse du modem CTX \_ pas de \_ \_ tonalité**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



Tonalité non détectée dans le délai imparti. Vérifiez que le câble téléphonique est correctement attaché et fonctionnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERREUR \_ de \_ réponse du modem CTX \_ \_ occupée**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Signal occupé détecté sur le site distant lors du rappel.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERREUR \_ de \_ réponse du modem CTX \_ \_**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Voix détectée sur le site distant lors du rappel.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**erreur de l’erreur \_ CTX \_ TD \_**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Erreur du pilote de transport.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERREUR \_ CTX \_ station \_ de \_ recherche introuvable**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



La session spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**une erreur de la \_ \_ station de terminal CTX \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



Le nom de session spécifié est déjà utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERREUR CTX de la station de l' \_ \_ \_ activité**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



La tâche que vous essayez d’effectuer ne peut pas être effectuée car Services Bureau à distance est actuellement occupé. Réessayez dans quelques minutes. Les autres utilisateurs doivent toujours être en mesure d’ouvrir une session.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERREUR \_ CTX \_ \_ mode vidéo incorrect \_**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



Une tentative a été effectuée pour se connecter à une session dont le mode vidéo n’est pas pris en charge par le client actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERREUR \_ \_ graphiques CTX \_ non valide**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



L’application a essayé d’activer le mode graphique DOS. Le mode graphique DOS n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERREUR \_ \_ d’ouverture de session CTX \_ désactivée**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



Votre privilège d’ouverture de session interactive a été désactivé. Contactez l'administrateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERREUR \_ CTX \_ non \_ console**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



L’opération demandée ne peut être effectuée que sur la console système. C’est généralement le résultat d’un pilote ou d’une DLL système nécessitant un accès direct à la console.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERREUR \_ d’expiration de la \_ requête cliente CTX \_ \_**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



Le client n’a pas pu répondre au message de connexion au serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERREUR \_ de \_ déconnexion de la console CTX \_**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



La déconnexion de la session de la console n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERREUR de connexion à la \_ \_ console CTX \_**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



La reconnexion d’une session déconnectée à la console n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERREUR de l' \_ \_ ombre CTX \_ refusée**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



La demande de contrôle d’une autre session à distance a été refusée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERREUR \_ de \_ \_ l’accès à la station de message CTX \_**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



L’accès à la session demandé est refusé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERREUR \_ CTX \_ WD non valide \_**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



Le pilote de connexion Terminal Server spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERREUR de l' \_ \_ ombre CTX \_ non valide**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



La session demandée ne peut pas être contrôlée à distance. Cela peut être dû au fait que la session est déconnectée ou qu’aucun utilisateur n’est actuellement connecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERREUR de l' \_ \_ ombre CTX \_ désactivée**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



La session demandée n’est pas configurée pour autoriser le contrôle à distance.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERREUR \_ \_ \_ de licence client CTX \_ en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



Votre demande de connexion à ce Terminal Server a été rejetée. Votre numéro de licence client Terminal Server est actuellement utilisé par un autre utilisateur. Contactez votre administrateur système pour obtenir un numéro de licence unique.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERREUR de la \_ \_ licence client CTX \_ \_ non \_ définie**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



Votre demande de connexion à ce Terminal Server a été rejetée. Votre numéro de licence client Terminal Server n’a pas été entré pour cette copie du client Terminal Server. Contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERREUR \_ de \_ licence CTX \_ non \_ disponible**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



Le nombre de connexions à cet ordinateur est limité et toutes les connexions sont actuellement utilisées. Essayez de vous connecter ultérieurement ou contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERREUR \_ de \_ licence CTX \_ client \_ non valide**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



Le client que vous utilisez n’a pas de licence d’utilisation de ce système. Votre demande d’ouverture de session est refusée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERREUR d’expiration de la \_ \_ licence CTX \_**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



La licence du système a expiré. Votre demande d’ouverture de session est refusée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERREUR de l' \_ \_ ombre CTX \_ non \_ exécutée**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



Impossible d’arrêter le contrôle à distance, car la session spécifiée n’est pas actuellement contrôlée à distance.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**erreur \_ lors \_ de \_ la \_ \_ modification du mode par l’ombre \_ CTX**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



Le contrôle à distance de la console a été interrompu, car le mode d’affichage a été modifié. La modification du mode d’affichage dans une session de contrôle à distance n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**\_nombre d’activations d’erreur \_ \_ dépassé**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



L’activation a déjà été réinitialisée le nombre maximal de fois pour cette installation. Votre minuteur d’activation n’est pas effacé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERREUR \_ CTX \_ WINSTATIONS \_ désactivée**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Les connexions distantes sont actuellement désactivées.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERREUR \_ \_ niveau de chiffrement CTX \_ \_ requis**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



Vous ne disposez pas du niveau de chiffrement approprié pour accéder à cette session.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERREUR \_ \_ de session CTX \_ en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



L’utilisateur% s \\ \\ % s est actuellement connecté à cet ordinateur. Seul l’utilisateur actuel ou un administrateur peut se connecter à cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERREUR \_ CTX \_ non \_ forcer la \_ fermeture de session**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



L’utilisateur% s \\ \\ % s est déjà connecté à la console de cet ordinateur. Vous n’êtes pas autorisé à vous connecter pour l’instant. Pour résoudre ce problème, contactez% s \\ \\ % s et demandez-leur de fermer la session.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERREUR \_ de \_ restriction de compte CTX \_**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



Impossible de vous connecter en raison d’une restriction de compte.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**erreur \_ de \_ protocole \_ RDP**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



Le composant de protocole RDP %2 a détecté une erreur dans le flux de protocole et a déconnecté le client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERREUR \_ CTX \_ CDM \_ Connect**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



Le service de mappage de lecteur client s’est connecté à la connexion de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERREUR \_ de \_ \_ déconnexion de CTX**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



Le service de mappage de lecteur client s’est déconnecté de la connexion de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**erreur \_ de \_ couche de sécurité CTX \_ erreur \_**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



La couche de sécurité Terminal Server a détecté une erreur dans le flux de protocole et a déconnecté le client.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERREUR \_ de \_ sessions incompatibles TS \_**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



La session cible est incompatible avec la session active.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**erreur \_ de \_ \_ sous-système d’erreur TS vidéo \_**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



Windows ne pouvez pas vous connecter à votre session, car un problème s’est produit dans le sous-système Windows vidéo. Essayez de vous reconnecter ultérieurement, ou contactez l’administrateur du serveur pour obtenir de l’aide.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_séquence d' \_ API non valide de l’erreur FRS \_ \_**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



L’API du service de réplication de fichiers a été appelée de manière incorrecte.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**\_service de \_ démarrage d’Err FRS \_**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



Impossible de démarrer le service de réplication de fichiers.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**\_service d' \_ arrêt d’erreur FRS \_**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



Impossible d’arrêter le service de réplication de fichiers.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interne FRS \_ Err**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



L’API du service de réplication de fichiers a mis fin à la requête. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**\_erreur FRS \_ interne**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



Le service de réplication de fichiers a mis fin à la requête. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_ \_ comm service FRS \_ Err**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



Impossible de contacter le service de réplication de fichiers. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**\_erreur FRS \_ insuffisante \_ priv**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



Le service de réplication de fichiers ne peut pas satisfaire la requête, car l’utilisateur ne dispose pas de privilèges suffisants. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**authentification FRS de \_ \_ l’erreur**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



Le service de réplication de fichiers ne peut pas satisfaire la requête, car le RPC authentifié n’est pas disponible. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**le parent de l’Err FRS est \_ \_ \_ insuffisant \_**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



Le service de réplication de fichiers ne peut pas satisfaire la requête, car l’utilisateur ne dispose pas de privilèges suffisants sur le contrôleur de domaine. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ authentification parente Err FRS \_**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



Le service de réplication de fichiers ne peut pas satisfaire la requête, car le RPC authentifié n’est pas disponible sur le contrôleur de domaine. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**réplication \_ \_ d’un enfant Err vers un \_ \_ \_ comm parent**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



Le service de réplication de fichiers ne peut pas communiquer avec le service de réplication de fichiers sur le contrôleur de domaine. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**réplication \_ de l’erreur \_ \_ du parent de la \_ comm. enfant \_**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



Le service de réplication de fichiers sur le contrôleur de domaine ne peut pas communiquer avec le service de réplication de fichiers sur cet ordinateur. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_ \_ remplissage SYSVOL de l’erreur FRS \_**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



Le service de réplication de fichiers ne peut pas remplir le volume système en raison d’une erreur interne. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ \_ délai d’attente de remplissage SYSVOL de l’erreur FRS**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



Le service de réplication de fichiers ne peut pas remplir le volume système en raison d’un délai d’attente interne. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**le \_ volume d’erreur FRS \_ \_ est \_ occupé**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



Le service de réplication de fichiers ne peut pas traiter la demande. Le volume système est occupé par une demande précédente.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ Err \_ SYSVOL \_ rétrograder**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



Le service de réplication de fichiers ne peut pas arrêter la réplication du volume système en raison d’une erreur interne. Le journal des événements peut contenir plus d’informations.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_paramètre de service FRS Err \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



Le service de réplication de fichiers a détecté un paramètre non valide.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur système](system-error-codes.md)
</dt> </dl>

 

 




