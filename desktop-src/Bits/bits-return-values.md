---
title: Valeurs de retour BITS
description: Le fichier Bitsmsg. h contient les constantes de valeur de retour suivantes.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- BITS d’erreur
- BITS d’erreur, codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941237"
---
# <a name="bits-return-values"></a>Valeurs de retour BITS

Le fichier Bitsmsg. h contient les constantes de valeur de retour suivantes. Les constantes représentent des valeurs de retour que BITS génère et des valeurs de retour HTTP que BITS capture. Toutes les autres valeurs de retour que vous pouvez recevoir sont COM, RPC ou les valeurs de retour Windows converties (BITS utilise le [HRESULT de la macro \_ \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) pour convertir les valeurs de retour Windows en valeurs HRESULT).

Notez que le fichier Bitsmsg. h contient des valeurs de retour supplémentaires non listées ci-dessous.

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>\_ \_ Fin partielle BG S \_ (0x00200017)
</dt> <dd>

Un sous-ensemble des fichiers du travail a été transféré correctement avant l’appel de la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Ceux qui n’ont pas été terminés ont été supprimés.

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ ne peut pas \_ \_ Supprimer les \_ fichiers (0x0020001A)
</dt> <dd>

Impossible de supprimer tous les fichiers temporaires associés au travail.

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ remplacé \_ par la \_ stratégie (0x00200055)
</dt> <dd>

La préférence de configuration a été enregistrée avec succès, mais la préférence n’est pas utilisée, car un paramètre de stratégie de groupe configuré remplace la préférence.

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ \_ introuvable (0x80200001)
</dt> <dd>

La tâche demandée est introuvable.

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_État BG E \_ non valide \_ (0x80200002)
</dt> <dd>

L’opération demandée n’est pas autorisée dans l’état actuel du travail.

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ vide (0x80200003)
</dt> <dd>

Le travail doit contenir un ou plusieurs fichiers avant de pouvoir reprendre le travail.

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_Fichier BG \_ E \_ non \_ disponible (0x80200004)
</dt> <dd>

Les informations de fichier ne sont pas disponibles, car l’erreur n’est pas associée à un fichier local ou distant.

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Protocole BG \_ E \_ non \_ disponible (0x80200005)
</dt> <dd>

Les informations de protocole ne sont pas disponibles, car l’erreur n’est pas associée au protocole de transfert spécifié.

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>\_Destination BG \_ E \_ verrouillée (0x8020000D)
</dt> <dd>

Le volume du système de fichiers de destination, spécifié dans le nom de fichier local, est verrouillé.

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>\_Volume E \_ BG \_ modifié (0x8020000E)
</dt> <dd>

Le volume de destination, spécifié dans le nom de fichier local, a changé. Par exemple, la disquette d’origine a été remplacée par une autre disquette.

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_Informations d’erreur BG E \_ \_ \_ non disponibles (0x8020000F)
</dt> <dd>

Les informations d’erreur sont disponibles uniquement lorsque l’état du travail est \_ erreur d’état de la tâche BG \_ \_ . Les informations sur l’erreur ne sont pas disponibles une fois que le service BITS a commencé à transférer les données du travail ou que le client se ferme.

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>\_Réseau BG \_ E \_ déconnecté (0x80200010)
</dt> <dd>

La carte réseau est inactive ou déconnectée. Toutes les tâches sont placées dans \_ l' \_ \_ État d' \_ erreur temporaire de l’état de travail BG.

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>\_ \_ Taille de fichier manquante BG E \_ \_ (0x80200011)
</dt> <dd>

Le serveur n’a pas retourné la taille du fichier. BITS transfère uniquement le contenu statique et nécessite que le serveur HTTP retourne l’en-tête Content-Length. La demande de transfert échoue si l’URL pointe vers du contenu dynamique.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>\_ \_ \_ Prise en charge http insuffisante de BG E \_ (0x80200012)
</dt> <dd>

Le serveur ne prend pas en charge le protocole HTTP/1.1.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_ \_ Prise en charge de la plage BG E insuffisante \_ \_ (0x80200013)
</dt> <dd>

Le serveur ne prend pas en charge l’en-tête Content-Range. En règle générale, cette erreur s’affiche lorsque vous essayez de télécharger du contenu dynamique. Vous pouvez également recevoir cette erreur si un proxy intermédiaire supprime l’en-tête Content-Range ou Content-Length.

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E \_ Remote \_ non \_ pris en charge (0x80200014)
</dt> <dd>

L’utilisation à distance de BITS n’est pas prise en charge. Pour plus d’informations, consultez [utilisateurs et connexions réseau](users-and-network-connections.md).

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>\_ \_ Mappage diff du nouveau propriétaire BG E \_ \_ \_ (0x80200015)
</dt> <dd>

Le mappage de lecteur réseau pour le fichier local est différent pour le propriétaire actuel que pour le propriétaire précédent.

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ nouveau \_ propriétaire \_ aucun \_ \_ accès aux fichiers (0x80200016)
</dt> <dd>

Le nouveau propriétaire ne dispose pas des autorisations suffisantes pour les fichiers de tâche temporaires.

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>\_ \_ Liste de proxy BG E \_ \_ trop \_ grande (0x80200018)
</dt> <dd>

La liste de proxy HTTP est trop longue. La liste ne doit pas dépasser 32 Ko.

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>\_ \_ Liste de contournement du proxy BG E \_ \_ \_ trop \_ grande (0x80200019)
</dt> <dd>

La liste de contournement du proxy HTTP est trop longue. La liste ne doit pas dépasser 32 Ko.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ \_ \_ de fichiers trop nombreux (0x8020001C)
</dt> <dd>

Vous ne pouvez pas ajouter plusieurs fichiers à un travail de chargement.

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_ \_ Fichier local BG \_ E \_ modifié (0x8020001D)
</dt> <dd>

Le contenu du fichier local a été modifié après le début du processus de transfert. Le contenu du fichier local ne peut pas être modifié après le début du processus de transfert sur un travail de chargement ou de chargement-réponse.

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ trop \_ grande (0x80200020)
</dt> <dd>

La taille du fichier de chargement dépasse la taille de téléchargement maximale autorisée spécifiée sur le serveur.

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>\_Chaîne BG \_ E \_ trop \_ longue (0x80200021)
</dt> <dd>

La chaîne spécifiée est trop longue.

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>\_Incompatibilité \_ de protocole du serveur client BG E \_ \_ \_ (0x80200022)
</dt> <dd>

Le client et le serveur n’ont pas pu négocier un protocole à utiliser pour le travail de chargement.

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>\_Exécution du serveur BG E \_ \_ \_ activée (0x80200023)
</dt> <dd>

Les autorisations de script ou d’exécution sont activées sur le répertoire virtuel IIS associé au travail. Pour charger des fichiers dans le répertoire virtuel, désactivez les autorisations de script et d’exécution sur le répertoire virtuel.

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>\_ \_ Nom d’utilisateur BG E \_ trop \_ grand (0x80200025)
</dt> <dd>

Le nom d’utilisateur ne peut pas dépasser 300 caractères.

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>\_ \_ Mot de passe BG E \_ trop \_ grand (0x80200026)
</dt> <dd>

Le mot de passe ne peut pas dépasser 65535 caractères.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ cible d’authentification non valide \_ \_ (0x80200027)
</dt> <dd>

La cible d’authentification spécifiée n’est pas valide.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ schéma d’authentification non valide \_ \_ (0x80200028)
</dt> <dd>

Le schéma d’authentification spécifié n’est pas valide.

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>\_Plage BG E \_ non valide \_ (0x8020002B)
</dt> <dd>

La plage d’octets spécifiée n’est pas valide. La plage d’octets doit exister dans le fichier distant spécifié.

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_ \_ Plages superposées BG E \_ (0x8020002C)
</dt> <dd>

La liste de plages d’octets contient des plages qui se chevauchent ou qui ne sont pas prises en charge.

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ bloqué \_ par la \_ stratégie (0x8020003E)
</dt> <dd>

Stratégie de groupe paramètres empêchent l’exécution des tâches en arrière-plan pour l’instant. Pour plus d’informations, consultez la stratégie [MaxInternetBandwidth](group-policies.md) .

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>\_ \_ Informations de proxy BG E non valide \_ \_ (0x8020003F)
</dt> <dd>

Erreur d’exécution qui indique la liste de proxy ou la liste de contournement du proxy que vous avez spécifiée à l’aide de la méthode [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) n’est pas valide.

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ \_ informations d’identification non valides (0x80200040)
</dt> <dd>

Le format des informations d’identification de sécurité fournies n’est pas valide.

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>\_Enregistrement BG \_ E \_ supprimé (0x80200042)
</dt> <dd>

L’enregistrement du cache a été supprimé. La tentative de mise à jour a été abandonnée.

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_Erreur de plug-in BG E \_ \_ (0x80200045)
</dt> <dd>

Une erreur UPnP (Universal Plug-and-Play) s’est produite. Vérifiez votre périphérique de passerelle Internet.

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>En \_ - \_ cache BG E \_ désactivé (0x80200047)
</dt> <dd>

La mise en cache d’homologue est désactivée.

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)
</dt> <dd>

L’enregistrement du cache est en cours d’utilisation et ne peut pas être modifié ou supprimé. Réessayez après quelques secondes.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ trop \_ \_ de travaux \_ par \_ utilisateur (0x80200049)
</dt> <dd>

Le nombre de tâches pour l’utilisateur a dépassé la limite de tâches par utilisateur définie par le paramètre de stratégie de groupe MaxJobsPerUser.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ trop \_ \_ de travaux \_ par \_ ordinateur (0x80200050)
</dt> <dd>

Le nombre de tâches de l’ordinateur a dépassé la limite par ordinateur définie par le paramètre de stratégie de groupe MaxJobsPerMachine.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ \_ \_ de fichiers trop nombreux dans le \_ \_ travail (0x80200051)
</dt> <dd>

Le nombre de fichiers pour le travail a dépassé la limite de fichiers par tâche définie par le paramètre de stratégie de groupe MaxFilesPerJob.

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ trop \_ \_ de plages \_ dans le \_ fichier (0x80200052)
</dt> <dd>

Le nombre de plages du fichier a dépassé la limite de plages par fichier définie par le paramètre de stratégie de groupe MaxRangesPerFile.

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>\_ \_ Échec de la validation BG E \_ (0x80200053)
</dt> <dd>

L’application a demandé des données à partir d’un site Web, mais la réponse n’est pas valide. Pour plus d’informations, utilisez observateur d’événements pour afficher le \\ Journal des opérations des journaux des applications Microsoft \\ Windows \\ bits-client \\ .

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>\_ \_ \_ Délai d’expiration de MAXDOWNLOAD BG E (0x80200054)
</dt> <dd>

Le service BITS a dépassé le délai de téléchargement du travail. Le téléchargement ne s’est pas terminé dans le délai de téléchargement maximal défini sur le travail ou le paramètre de stratégie de groupe MaxDownloadTime.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>\_Erreur BG \_ E \_ http \_ 400 (0x80190190)
</dt> <dd>

Le serveur n’a pas pu traiter la demande de transfert car la syntaxe du nom de fichier distant n’est pas valide.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>\_Erreur BG \_ E \_ http \_ 401 (0x80190191)
</dt> <dd>

L’utilisateur n’a pas l’autorisation d’accéder au fichier distant. La ressource demandée nécessite l'authentification des utilisateurs.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>\_Erreur BG \_ E \_ http \_ 404 (0x80190194)
</dt> <dd>

L’URL demandée n’existe pas sur le serveur.

Dans IIS 7, cette erreur peut indiquer

-   Les téléchargements BITS ne sont pas activés sur le répertoire virtuel (vdir) sur le serveur.
-   Que la taille de téléchargement dépasse la limite maximale de chargement (pour plus d’informations, consultez la propriété d’extension IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) ).

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>\_Erreur BG \_ E \_ http \_ 407 (0x80190197)
</dt> <dd>

L’utilisateur n’a pas l’autorisation d’accéder au proxy. Le proxy requiert l’authentification de l’utilisateur.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>\_Erreur BG \_ E \_ http \_ 414 (0x8019019E)
</dt> <dd>

Le serveur ne peut pas traiter la demande de transfert. Le Uniform Resource Identifier (URI) dans le nom de fichier distant est plus long que le serveur ne peut interpréter.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>\_Erreur BG \_ E \_ http \_ 501 (0x801901F5)
</dt> <dd>

Le serveur ne prend pas en charge les fonctionnalités requises pour satisfaire la demande. Dans IIS 6, cette erreur indique que les téléchargements BITS ne sont pas activés sur le répertoire virtuel (vdir) sur le serveur.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>\_Erreur BG \_ E \_ http \_ 503 (0x801901F7)
</dt> <dd>

Le service est temporairement surchargé et ne peut pas traiter la requête. Reprendre la tâche ultérieurement.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>\_Erreur BG \_ E \_ http \_ 504 (0x801901F8)
</dt> <dd>

La demande de transfert a expiré pendant l’attente d’une passerelle. Reprendre la tâche ultérieurement.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>\_Erreur BG \_ E \_ http \_ 505 (0x801901F9)
</dt> <dd>

Le serveur ne prend pas en charge la version du protocole HTTP spécifiée dans le nom du fichier distant.

</dd> </dl>

Le fichier d’en-tête Bitsmsg. h contient des valeurs de retour HTTP supplémentaires non listées ci-dessus que BITS utilise en interne. Pour plus d’informations sur ces valeurs et sur les autres valeurs de retour HTTP que vous pouvez recevoir, consultez la spécification RFC 2616 de la page IETF (Internet Engineering Task Force) à l’adresse [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .

 

 