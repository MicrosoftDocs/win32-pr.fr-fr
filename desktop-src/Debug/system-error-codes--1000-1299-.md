---
description: Décrit les codes d’erreur 1000-1299 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Codes d’erreur système (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523716"
---
# <a name="system-error-codes-1000-1299"></a>Codes d’erreur système (1000-1299)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 1000 à 1299. Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_dépassement de pile d’erreur \_**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Récurrence trop profonde ; dépassement de capacité de la pile.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**MESSAGE d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



La fenêtre ne peut pas agir sur le message envoyé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**l' \_ erreur \_ ne peut pas se \_ terminer**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



Impossible d’effectuer cette fonction.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**indicateurs d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Indicateurs non valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERREUR de \_ volume non reconnu \_**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



Le volume ne contient pas de système de fichiers reconnu. Assurez-vous que tous les pilotes de système de fichiers requis sont chargés et que le volume n’est pas endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**fichier d’erreur \_ \_ non valide**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



Le volume d’un fichier a été modifié en externe, de sorte que le fichier ouvert n’est plus valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERREUR \_ de \_ mode plein écran**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



L’opération demandée ne peut pas être exécutée en mode plein écran.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERREUR \_ aucun \_ jeton**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



Une tentative de référence à un jeton qui n’existe pas a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERREUR \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



La base de données de registre de configuration est endommagée.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERREUR \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



La clé de registre de configuration n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERREUR \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



Impossible d’ouvrir la clé de registre de configuration.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERREUR \_ CANTREAD**
</dt> <dd> <dl> <dt>

1012 (égal à 0x3f4)
</dt> <dt>



Impossible de lire la clé de registre de configuration.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERREUR \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



Impossible d’écrire la clé de registre de configuration.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERREUR \_ de \_ récupération du Registre**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



L’un des fichiers de la base de données du registre a dû être récupéré à l’aide d’un journal ou d’une copie de remplacement. La récupération a réussi.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**Registre des erreurs \_ \_ endommagé**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



Le Registre est endommagé. La structure de l’un des fichiers contenant les données du Registre est endommagée, l’image mémoire du système du fichier est endommagée, ou le fichier n’a pas pu être récupéré parce que l’autre copie ou le même journal est absent ou endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERREUR \_ échec de l' \_ e/s du Registre \_**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Une opération d’e/s initiée par le registre a échoué de façon irrécupérable. Le registre n’a pas pu lire ou écrire, ou vider, l’un des fichiers qui contiennent l’image du Registre du système.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERREUR \_ non \_ fichier du Registre \_**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



Le système a tenté de charger ou de restaurer un fichier dans le registre, mais le fichier spécifié n’est pas dans un format de fichier du Registre.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**clé d’erreur \_ \_ supprimée**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Opération non conforme tentée sur une clé de Registre marquée pour suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERREUR \_ aucun \_ espace du journal \_**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



Le système n’a pas pu allouer l’espace requis dans un journal du Registre.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**la \_ clé d’erreur \_ a des \_ enfants**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



Impossible de créer un lien symbolique dans une clé de Registre qui a déjà des sous-clés ou des valeurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**l' \_ enfant d’erreur \_ doit \_ être \_ volatile**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



Impossible de créer une sous-clé stable sous une clé parent volatile.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERREUR de notification de l' \_ \_ énumération \_ dir**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



Une demande de notification de modification est en cours d’exécution et les informations ne sont pas retournées dans la mémoire tampon de l’appelant. L’appelant doit à présent énumérer les fichiers pour rechercher les modifications.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_services dépendants d’erreurs \_ \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



Un contrôle d’arrêt a été envoyé à un service dont dépendent d’autres services en cours d’exécution.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERREUR \_ de \_ contrôle de service non valide \_**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



Le contrôle demandé n’est pas valide pour ce service.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERREUR \_ de \_ \_ délai d’expiration de la demande de service**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



Le service n'a pas répondu à temps à la requête de démarrage ou de contrôle.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**SERVICE d’erreur \_ \_ sans \_ thread**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



Impossible de créer un thread pour le service.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**\_base de données du service d’erreur \_ \_ verrouillée**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



La base de données du service est verrouillée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**SERVICE d’erreur \_ \_ déjà \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Une instance du service est déjà en cours d’exécution.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERREUR \_ de \_ compte de service non valide \_**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



Le nom du compte n’est pas valide ou n’existe pas, ou le mot de passe n’est pas valide pour le nom de compte spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**SERVICE d’erreur \_ \_ désactivé**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



Le service ne peut pas être démarré parce qu’il est désactivé ou qu’aucun appareil activé ne lui est associé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**\_dépendance circulaire d’erreur \_**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



Une dépendance de service circulaire a été spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**le \_ service d’erreur \_ n' \_ \_ existe pas**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



Le service spécifié n’existe pas en tant que service installé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**le \_ service d’erreur \_ ne peut pas \_ accepter la \_ touche Ctrl**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



Le service ne peut pas accepter les messages de contrôle pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**\_service d' \_ erreur \_ inactif**
</dt> <dd> <dl> <dt>

1062 (0x426)
</dt> <dt>



Le service n'a pas été démarré.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERREUR \_ échec \_ de \_ connexion du contrôleur de service \_**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



Le processus de service n’a pas pu se connecter au contrôleur de service.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_exception \_ d’erreur dans le \_ service**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



Une exception s’est produite dans le service lors du traitement de la demande de contrôle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**la \_ base de données d’erreurs \_ n' \_ \_ existe pas**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



La base de données spécifiée n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**erreur \_ spécifique au service d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1066 (0x42A)
</dt> <dt>



Le service a retourné un code d’erreur spécifique au service.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**\_arrêt du processus d’erreur \_**
</dt> <dd> <dl> <dt>

1067 (0x42B)
</dt> <dt>



Le processus s’est arrêté de manière inattendue.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**échec de la dépendance du service d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

1068 (0x42C)
</dt> <dt>



Le service ou le groupe de dépendances n’a pas pu démarrer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**échec de l' \_ ouverture de session du service \_ \_**
</dt> <dd> <dl> <dt>

1069 (0x42D)
</dt> <dt>



Le service n'a pas démarré en raison d'une erreur d'ouverture de session.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERREUR de \_ démarrage du service d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1070 (0x42E)
</dt> <dt>



Après le démarrage, le service est suspendu dans un état de démarrage.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERREUR \_ de \_ verrou de service non valide \_**
</dt> <dd> <dl> <dt>

1071 (0x42F)
</dt> <dt>



Le verrou de base de données de service spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_service \_ d’erreur marqué \_ pour \_ suppression**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



Le service spécifié a été marqué pour suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**le \_ service d’erreur \_ existe**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



Le service spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERREUR lors de l' \_ \_ exécution de \_ correcte connue**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



Le système est en cours d’exécution avec la dernière bonne configuration connue.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dépendance de service d’erreur \_ \_ \_ supprimée**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



Le service de dépendances n’existe pas ou a été marqué pour suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERREUR de \_ démarrage \_ déjà \_ acceptée**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



Le démarrage actuel a déjà été accepté pour une utilisation en tant que dernier jeu de contrôle connu.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**le \_ service d’erreur \_ n' \_ a jamais démarré**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



Aucune tentative de démarrage du service n’a été effectuée depuis le dernier démarrage.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERREUR \_ de \_ nom de service dupliqué \_**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



Le nom est déjà utilisé en tant que nom de service ou nom d’affichage de service.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERREUR \_ de \_ compte de service différent \_**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



Le compte spécifié pour ce service est différent du compte spécifié pour les autres services s’exécutant dans le même processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERREUR \_ Impossible de \_ détecter la \_ défaillance du pilote \_**
</dt> <dd> <dl> <dt>

1080 (0x438)
</dt> <dt>



Les actions d’échec ne peuvent être définies que pour les services Win32, et non pour les pilotes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERREUR \_ Impossible de \_ détecter l' \_ abandon du processus \_**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Ce service s’exécute dans le même processus que le gestionnaire de contrôle des services. Par conséquent, le gestionnaire de contrôle des services ne peut pas agir si le processus de ce service se termine de manière inattendue.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERREUR \_ pas \_ de \_ programme de récupération**
</dt> <dd> <dl> <dt>

1082 (0x43A)
</dt> <dt>



Aucun programme de récupération n’a été configuré pour ce service.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERREUR \_ \_ de service introuvable \_ dans l' \_ exe**
</dt> <dd> <dl> <dt>

1083 (0x43B)
</dt> <dt>



Le programme exécutable dans lequel ce service est configuré pour s’exécuter n’implémente pas le service.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERREUR \_ non \_ - \_ service SafeBoot**
</dt> <dd> <dl> <dt>

1084 (0x43C)
</dt> <dt>



Ce service ne peut pas être démarré en mode sans échec.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_fin \_ du \_ support d’erreur**
</dt> <dd> <dl> <dt>

1100 (0x44C)
</dt> <dt>



La fin physique de la bande a été atteinte.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**marque d’erreur \_ \_ détectée**
</dt> <dd> <dl> <dt>

1101 (0x44D)
</dt> <dt>



Un accès à la bande a atteint un marqueur.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERREUR \_ \_ de début de \_ support**
</dt> <dd> <dl> <dt>

1102 (0x44E)
</dt> <dt>



Le début de la bande ou d’une partition a été rencontré.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERREUR \_ SETMARK \_ détectée**
</dt> <dd> <dl> <dt>

1103 (0x44F)
</dt> <dt>



Un accès à la bande a atteint la fin d’un ensemble de fichiers.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERREUR \_ aucune \_ donnée \_ détectée**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



Il n’y a plus de données sur la bande.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**\_échec de partition d’erreur \_**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



La bande n’a pas pu être partitionnée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERREUR \_ de \_ longueur de bloc non valide \_**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



Lors de l’accès à une nouvelle bande d’une partition multivolume, la taille de bloc actuelle est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERREUR de \_ périphérique \_ non \_ partitionné**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



Les informations de partition de bande sont introuvables lors du chargement d’une bande.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERREUR \_ Impossible \_ de \_ verrouiller le \_ support**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



Impossible de verrouiller le mécanisme d’éjection de support.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERREUR \_ Impossible \_ de \_ décharger le \_ média**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



Impossible de décharger le média.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**le \_ support d’erreur \_ a changé**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



Le support présent dans le lecteur a peut-être changé.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**réinitialisation du bus d’erreurs \_ \_**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



Le bus des e/s a été réinitialisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERREUR \_ aucun \_ média \_ dans le \_ lecteur**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



Aucun média dans le lecteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERREUR \_ aucune \_ \_ traduction Unicode**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



Il n’existe aucun mappage pour le caractère Unicode dans la page de codes multi-octets cible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**échec de l’initialisation de la dll d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

1114 (0x45A)
</dt> <dt>



Échec de la routine d’initialisation d’une bibliothèque de liens dynamiques (DLL).


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERREUR \_ \_ d’arrêt en \_ cours**
</dt> <dd> <dl> <dt>

1115 (0x45B)
</dt> <dt>



Un arrêt du système est en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERREUR \_ aucun \_ arrêt \_ en \_ cours**
</dt> <dd> <dl> <dt>

1116 (0x45C)
</dt> <dt>



Impossible d’abandonner l’arrêt du système, car aucun arrêt n’était en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERREUR d' \_ e/s \_ périphérique**
</dt> <dd> <dl> <dt>

1117 (0x45D)
</dt> <dt>



La requête n'a pas pu être exécutée en raison d'une erreur de périphérique d'E/S.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERREUR \_ série \_ aucun \_ appareil**
</dt> <dd> <dl> <dt>

1118 (0x45E)
</dt> <dt>



Aucun appareil série n’a été correctement initialisé. Le pilote série sera déchargé.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERREUR \_ IRQ \_ Busy**
</dt> <dd> <dl> <dt>

1119 (0x45F)
</dt> <dt>



Impossible d’ouvrir un appareil qui partageait une requête d’interruption (IRQ) avec d’autres appareils. Au moins un autre périphérique qui utilise cette IRQ a déjà été ouvert.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERREUR \_ plus d' \_ Écritures**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Une opération d’e/s série a été effectuée par une autre écriture sur le port série. Le compteur de l' \_ XOFF série IOCTL a \_ \_ atteint zéro.)


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_ \_ délai d’attente du compteur d’erreurs**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Une opération d’e/s série s’est terminée, car le délai d’attente a expiré. Le \_ compteur de série \_ XOFF IOCTL \_ n’a pas atteint zéro.)


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERREUR de \_ marque d’ID de disquette \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



Aucune marque d’adresse d’ID n’a été trouvée sur la disquette.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERREUR de \_ disque- \_ cylindre incorrect \_**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Discordance entre le champ d’ID de secteur de disquette et l’adresse de piste du contrôleur de disquette.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**erreur de \_ disquette \_ inconnue \_**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



Le contrôleur de disquette a signalé une erreur qui n’est pas reconnue par le pilote de disquette.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**Erreurs de \_ registres de disquettes \_ erronées \_**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



Le contrôleur de disquette a retourné des résultats incohérents dans ses registres.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**échec de l’étalonnage du disque d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



Lors de l’accès au disque dur, une opération de recalibrage a échoué, même après une nouvelle tentative.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERREUR Échec de l’opération sur le \_ disque \_ \_**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



Lors de l’accès au disque dur, une opération de disque a échoué même après une nouvelle tentative.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERREUR \_ échec de la \_ réinitialisation du disque \_**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



Lors de l’accès au disque dur, une réinitialisation du contrôleur de disque était nécessaire, mais même cela a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERREUR \_ FDM de \_ dépassement**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Fin de bande physique rencontrée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERREUR \_ de \_ mémoire insuffisante sur le \_ serveur \_**
</dt> <dd> <dl> <dt>

1130 (0x46A)
</dt> <dt>



Mémoire insuffisante sur le serveur pour traiter cette commande.


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERREUR \_ possible \_ blocage**
</dt> <dd> <dl> <dt>

1131 (0x46B)
</dt> <dt>



Une condition potentielle de blocage a été détectée.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERREUR d' \_ \_ alignement mappé**
</dt> <dd> <dl> <dt>

1132 (0x46C)
</dt> <dt>



L’adresse de base ou le décalage de fichier spécifié n’a pas l’alignement approprié.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERREUR de définition de l' \_ \_ État d’alimentation \_ \_ refusé**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Une tentative de modification de l’état d’alimentation du système a été refusée par une autre application ou un autre pilote.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**échec de définition de l' \_ \_ État d’alimentation \_ \_**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



Le BIOS du système n’a pas pu tenter de modifier l’état d’alimentation du système.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERREUR \_ d' \_ un trop grand nombre de \_ liens**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



Une tentative a été effectuée pour créer davantage de liens sur un fichier que celui pris en charge par le système de fichiers.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERREUR \_ d' \_ ancienne \_ version Win**
</dt> <dd> <dl> <dt>

1150 (0x47E)
</dt> <dt>



Le programme spécifié requiert une version plus récente de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERREUR \_ de \_ \_ système d’exploitation incorrect**
</dt> <dd> <dl> <dt>

1151 (0x47F)
</dt> <dt>



Le programme spécifié n'est pas un programme Windows ou MS-DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**\_application à \_ instance \_ unique d’erreur**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Impossible de démarrer plusieurs instances du programme spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERREUR \_ d' \_ application RMODE**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



Le programme spécifié a été écrit pour une version antérieure de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERREUR \_ dll non valide \_**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



L’un des fichiers de bibliothèque requis pour exécuter cette application est endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERREUR \_ aucune \_ Association**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



Aucune application n’est associée au fichier spécifié pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERREUR \_ DDE \_ échec**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Une erreur s’est produite lors de l’envoi de la commande à l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_dll d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



L’un des fichiers de bibliothèque requis pour exécuter cette application est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERREUR \_ \_ plus de \_ \_ Handles utilisateur**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



Le processus en cours a utilisé toute l’allocation système des descripteurs pour les objets du gestionnaire de fenêtrage.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**synchronisation des messages d’erreur \_ \_ \_ uniquement**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



Le message ne peut être utilisé qu’avec des opérations synchrones.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_élément source d’erreur \_ \_ vide**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



L’élément source indiqué n’a pas de support.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERREUR de l' \_ élément de destination \_ \_ complet**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



L’élément de destination indiqué contient déjà un média.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERREUR \_ d' \_ adresse d’élément non conforme \_**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



L’élément indiqué n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERREUR \_ magazine \_ \_ absente**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



L’élément indiqué fait partie d’un magazine qui n’est pas présent.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERREUR \_ de \_ réinitialisation de périphérique \_ requise**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



L’appareil indiqué requiert une réinitialisation en raison d’erreurs matérielles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**l' \_ appareil d’erreur \_ nécessite un \_ nettoyage**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



L’appareil a indiqué que le nettoyage est nécessaire avant toute tentative d’opérations.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERREUR d’ouverture de la \_ porte du périphérique \_ \_**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



L’appareil a indiqué que sa porte est ouverte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**périphérique d’erreur \_ \_ non \_ connecté**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



L’appareil n’est pas connecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERREUR \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Element not found.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERREUR \_ aucune \_ correspondance**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Aucune correspondance n’a été trouvée pour la clé spécifiée dans l’index.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERREUR \_ de \_ jeu \_ introuvable**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



Le jeu de propriétés spécifié n’existe pas sur l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_point d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



Le point passé à GetMouseMovePoints n’est pas dans la mémoire tampon.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERREUR \_ aucun \_ service de suivi \_**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



Le service de suivi (station de travail) n’est pas en cours d’exécution.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERREUR \_ aucun \_ ID de volume \_**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



L’ID de volume est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERREUR \_ Impossible \_ de \_ supprimer le \_ remplacement**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Impossible de supprimer le fichier à remplacer.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERREUR \_ Impossible \_ de \_ déplacer le \_ remplacement**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Impossible de déplacer le fichier de remplacement dans le fichier à remplacer. Le fichier à remplacer a conservé son nom d’origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERREUR \_ Impossible \_ de \_ déplacer le \_ remplacement \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Impossible de déplacer le fichier de remplacement dans le fichier à remplacer. Le fichier à remplacer a été renommé à l’aide du nom de la sauvegarde.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ suppression du journal \_ des erreurs en \_ cours**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



Le journal de modification du volume est en cours de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**\_Journal des \_ Erreurs \_ inactif**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



Le journal des modifications de volume n’est pas actif.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_fichier potentiel d’erreur \_ \_ trouvé**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



Un fichier a été trouvé, mais il n’est peut-être pas le bon fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**entrée du journal des erreurs \_ \_ \_ supprimée**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



L’entrée du journal a été supprimée du journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**l’arrêt de l’erreur \_ \_ est \_ planifié**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



Un arrêt du système a déjà été planifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**erreur \_ lors \_ de l’arrêt \_ des utilisateurs connectés \_**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



Impossible d’initier l’arrêt du système, car d’autres utilisateurs sont connectés à l’ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERREUR \_ de \_ périphérique incorrect**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



Le nom d’appareil spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERREUR de \_ connexion \_ indispo.**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



L’appareil n’est pas connecté actuellement, mais il s’agit d’une connexion mémorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERREUR de l' \_ appareil \_ déjà \_ mémorisé**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



Le nom de l’appareil local a une connexion mémorisée à une autre ressource réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERREUR \_ non \_ NET \_ ou \_ \_ chemin d’accès incorrect**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



Le chemin d’accès réseau n’a pas été correctement tapé, n’existe pas ou le fournisseur réseau n’est pas disponible actuellement. Essayez de retaper le chemin d’accès ou contactez votre administrateur réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERREUR \_ fournisseur incorrect \_**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



Le nom du fournisseur réseau spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERREUR \_ Impossible d' \_ ouvrir le \_ profil**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



Impossible d’ouvrir le profil de connexion réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERREUR \_ de \_ Profil incorrect**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



Le profil de connexion réseau est endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERREUR \_ non \_ conteneur**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



Impossible d’énumérer un non-conteneur.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**erreur \_ étendue d’erreur \_**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Une erreur étendue s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERREUR \_ GroupName non valide \_**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



Le format du nom de groupe spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERREUR \_ ComputerName non valide \_**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



Le format du nom d’ordinateur spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERREUR \_ NomÉvénement non valide \_**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



Le format du nom d’événement spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERREUR \_ nomdomaine non valide \_**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



Le format du nom de domaine spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERREUR \_ ServiceName non valide \_**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



Le format du nom de service spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERREUR \_ \_ NetName non valide**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



Le format du nom réseau spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERREUR \_ de \_ Nom_Partage non valide**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



Le format du nom de partage spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERREUR \_ PASSWORDNAME non valide \_**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



Le format du mot de passe spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERREUR \_ MESSAGENAME non valide \_**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



Le format du nom du message spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERREUR \_ MESSAGEDEST non valide \_**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



Le format de la destination de message spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERREUR \_ de \_ conflit d’informations d’identification de session \_**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



L’utilisation de plusieurs connexions à un serveur ou à une ressource partagée par le même utilisateur, à l’aide de plusieurs noms d’utilisateur, n’est pas autorisée. Déconnectez toutes les connexions précédentes au serveur ou à la ressource partagée, puis réessayez.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERREUR \_ limite de session à distance \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



Une tentative a été effectuée pour établir une session sur un serveur réseau, mais il existe déjà trop de sessions établies sur ce serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERREUR \_ DUP \_ nomdomaine**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



Le groupe de travail ou le nom de domaine est déjà utilisé par un autre ordinateur sur le réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERREUR \_ aucun \_ réseau**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



Le réseau n’est pas présent ou n’a pas démarré.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERREUR \_ annulée**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



L’opération a été annulée par l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERREUR \_ \_ fichier mappé utilisateur \_**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



L’opération demandée ne peut pas être effectuée sur un fichier dont la section mappée par l’utilisateur est ouverte.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERREUR de \_ connexion \_ refusée**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



L’ordinateur distant a refusé la connexion réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERREUR \_ de \_ déconnexion normale**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



La connexion réseau a été fermée normalement.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**adresse d’erreur \_ \_ déjà \_ associée**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



Un point de terminaison de transport réseau est déjà associé à une adresse.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**adresse d’erreur \_ \_ non \_ associée**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



Une adresse n’a pas encore été associée au point de terminaison réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**connexion d’erreur \_ \_ non valide**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



Une opération a été tentée sur une connexion réseau inexistante.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**connexion d’erreur \_ \_ active**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



Une opération non valide a été tentée sur une connexion réseau active.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERREUR \_ réseau \_ inaccessible**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



L’emplacement réseau ne peut pas être atteint. Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**hôte d’erreur \_ \_ inaccessible**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



L’emplacement réseau ne peut pas être atteint. Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**protocole d’erreur \_ \_ inaccessible**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



L’emplacement réseau ne peut pas être atteint. Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**PORT d’erreur \_ \_ inaccessible**
</dt> <dd> <dl> <dt>

1234 (0x4D2)
</dt> <dt>



Aucun service ne fonctionne sur le point de terminaison du réseau de destination sur le système distant.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**demande d’erreur \_ \_ abandonnée**
</dt> <dd> <dl> <dt>

1235 (0x4D3)
</dt> <dt>



La demande a été abandonnée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERREUR de \_ connexion \_ abandonnée**
</dt> <dd> <dl> <dt>

1236 (0x4D4)
</dt> <dt>



La connexion réseau a été abandonnée par le système local.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**\_nouvelle tentative d’erreur**
</dt> <dd> <dl> <dt>

1237 (0x4D5)
</dt> <dt>



L'opération n'a pas pu être terminée. Une nouvelle tentative doit être effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_limite du \_ nombre de connexions d’erreur \_**
</dt> <dd> <dl> <dt>

1238 (0x4D6)
</dt> <dt>



Une connexion au serveur n’a pas pu être établie, car la limite du nombre de connexions simultanées pour ce compte a été atteinte.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**\_restriction d' \_ heure de connexion d’erreur \_**
</dt> <dd> <dl> <dt>

1239 (0x4D7)
</dt> <dt>



Tentative de connexion pendant une période de temps non autorisée pour ce compte.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERREUR de \_ connexion wksta de connexion \_ \_**
</dt> <dd> <dl> <dt>

1240 (0x4D8)
</dt> <dt>



Le compte n’est pas autorisé à se connecter à partir de cette station.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERREUR d' \_ adresse incorrecte \_**
</dt> <dd> <dl> <dt>

1241 (0x4D9)
</dt> <dt>



L’adresse réseau n’a pas pu être utilisée pour l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERREUR \_ déjà \_ inscrite**
</dt> <dd> <dl> <dt>

1242 (0x4DA)
</dt> <dt>



Le service est déjà inscrit.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_service d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

1243 (0x4DB)
</dt> <dt>



Le service spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERREUR \_ non \_ authentifiée**
</dt> <dd> <dl> <dt>

1244 (0x4DC)
</dt> <dt>



L’opération demandée n’a pas été effectuée car l’utilisateur n’a pas été authentifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERREUR \_ non \_ connectée \_**
</dt> <dd> <dl> <dt>

1245 (0x4DD)
</dt> <dt>



L’opération demandée n’a pas été effectuée car l’utilisateur ne s’est pas connecté au réseau. Le service spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**l’erreur se \_ poursuit**
</dt> <dd> <dl> <dt>

1246 (0x4DE)
</dt> <dt>



Poursuivez le travail en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERREUR \_ déjà \_ initialisée**
</dt> <dd> <dl> <dt>

1247 (0x4DF)
</dt> <dt>



Une tentative a été effectuée pour effectuer une opération d’initialisation alors que l’initialisation a déjà été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERREUR \_ \_ plus aucun \_ appareil**
</dt> <dd> <dl> <dt>

1248 (0x4E0)
</dt> <dt>



Il n’y a plus d’appareils locaux.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERREUR \_ aucun \_ site de ce type \_**
</dt> <dd> <dl> <dt>

1249 (0x4E1)
</dt> <dt>



Le site spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**le \_ contrôleur de domaine d’erreur \_ \_ existe**
</dt> <dd> <dl> <dt>

1250 (0x4E2)
</dt> <dt>



Un contrôleur de domaine portant le nom spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERREUR \_ uniquement \_ si \_ connecté**
</dt> <dd> <dl> <dt>

1251 (0x4E3)
</dt> <dt>



Cette opération est prise en charge uniquement lorsque vous êtes connecté au serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERREUR lors du \_ remplacement des \_ nochanges**
</dt> <dd> <dl> <dt>

1252 (0x4E4)
</dt> <dt>



L’infrastructure de stratégie de groupe doit appeler l’extension même si aucune modification n’est apportée.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERREUR \_ de \_ profil utilisateur incorrect \_**
</dt> <dd> <dl> <dt>

1253 (0x4E5)
</dt> <dt>



L’utilisateur spécifié n’a pas de profil valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERREUR \_ non \_ prise en charge \_ sur \_ SBS**
</dt> <dd> <dl> <dt>

1254 (0x4E6)
</dt> <dt>



Cette opération n’est pas prise en charge sur un ordinateur exécutant Windows Server 2003 pour Small Business Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**\_ \_ arrêt du serveur \_ d’erreur en \_ cours**
</dt> <dd> <dl> <dt>

1255 (0x4E7)
</dt> <dt>



L’ordinateur serveur est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERREUR de l' \_ hôte \_**
</dt> <dd> <dl> <dt>

1256 (0x4E8)
</dt> <dt>



Le système distant n’est pas disponible. Pour plus d’informations sur la résolution des problèmes réseau, consultez l’aide de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERREUR \_ \_ sid sans compte \_**
</dt> <dd> <dl> <dt>

1257 (0x4E9)
</dt> <dt>



L’identificateur de sécurité fourni ne provient pas d’un domaine de compte.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERREUR \_ non liée au \_ \_ sid**
</dt> <dd> <dl> <dt>

1258 (0x4EA)
</dt> <dt>



L’identificateur de sécurité fourni n’a pas de composant de domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERREUR \_ APPHELP, \_ bloc**
</dt> <dd> <dl> <dt>

1259 (0x4EB)
</dt> <dt>



La boîte de dialogue AppHelp a été annulée, ce qui empêche le démarrage de l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_accès aux erreurs \_ désactivé par la \_ \_ stratégie**
</dt> <dd> <dl> <dt>

1260 (0x4EC)
</dt> <dt>



Ce programme est bloqué par la stratégie de groupe. Pour plus d’informations, contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERREUR \_ de \_ consommation NAT reg \_**
</dt> <dd> <dl> <dt>

1261 (0x4ED)
</dt> <dt>



Un programme tente d’utiliser une valeur de Registre non valide. Normalement dû à un registre non initialisé. Cette erreur est spécifique à Itanium.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERREUR \_ CSCSHARE \_ hors connexion**
</dt> <dd> <dl> <dt>

1262 (0x4EE)
</dt> <dt>



Le partage est actuellement hors connexion ou n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERREUR \_ PKINIT en \_ échec**
</dt> <dd> <dl> <dt>

1263 (0x4EF)
</dt> <dt>



Le protocole Kerberos a rencontré une erreur lors de la validation du certificat KDC lors de la connexion par carte à puce. Le journal des événements système contient des informations supplémentaires.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERREUR \_ de \_ défaillance du sous-système de la carte à puce \_**
</dt> <dd> <dl> <dt>

1264 (0x4F0)
</dt> <dt>



Le protocole Kerberos a rencontré une erreur lors de la tentative d’utilisation du sous-système de carte à puce.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERREUR de \_ rétrogradation \_ détectée**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



Le système ne peut pas contacter un contrôleur de domaine pour traiter la demande d’authentification. Veuillez réessayer plus tard.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERREUR de verrouillage de l' \_ ordinateur \_**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option forcer.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**le rappel d’erreur a \_ \_ fourni des \_ données non valides \_**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Un rappel défini par l’application a donné des données non valides lorsqu’il est appelé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERREUR de \_ synchronisation de \_ premier plan \_ \_ requise**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



L’infrastructure de stratégie de groupe doit appeler l’extension dans l’actualisation synchrone de la stratégie de premier plan.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**pilote d’erreur \_ \_ bloqué**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



Le chargement de ce pilote a été bloqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**erreur \_ lors \_ de l’importation \_ d’une \_ \_ dll non valide**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Une bibliothèque de liens dynamiques (DLL) a référencé un module qui n’était ni une DLL ni l’image exécutable du processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**\_WebBlade désactivé pour l’accès aux erreurs \_ \_**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



Windows ne peut pas ouvrir ce programme, car il a été désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERREUR d' \_ accès à la \_ \_ WebBlade désactivée pour l’accès \_**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



Windows ne peut pas ouvrir ce programme, car le système d’application de la licence a été falsifié ou endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**échec de la récupération d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Une récupération de transaction a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERREUR \_ déjà \_ Fiber**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



Le thread actuel a déjà été converti en fibre.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERREUR \_ déjà \_ thread**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



Le thread actuel a déjà été converti à partir d’une fibre.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_dépassement de \_ mémoire tampon \_ de la pile d’erreur**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



Le système a détecté un dépassement de mémoire tampon basée sur la pile dans cette application. Ce dépassement peut permettre à un utilisateur malveillant de prendre le contrôle de cette application.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**QUOTA de paramètres d’erreur \_ \_ \_ dépassé**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



Les données présentes dans l’un des paramètres sont plus que la fonction peut fonctionner sur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**débogueur d’erreur \_ \_ inactif**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Une tentative d’exécution d’une opération sur un objet de débogage a échoué, car l’objet est en cours de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**\_échec du \_ chargement du délai d’erreur \_**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Une tentative de retarder le chargement d’un fichier. dll ou l’extraction d’une adresse de fonction dans un fichier. dll à chargement différé a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERREUR \_ VDM non \_ autorisée**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 est une application 16 bits. Vous ne disposez pas des autorisations nécessaires pour exécuter des applications 16 bits. Vérifiez vos autorisations avec votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**erreur non \_ identifiée \_**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Des informations insuffisantes existent pour identifier la cause de l’échec.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERREUR \_ de \_ paramètre CRUNTIME non valide \_**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



Le paramètre passé à une fonction Runtime C est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERREUR \_ au-delà de \_ VDL**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



L’opération s’est produite au-delà de la longueur de données valide du fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERREUR de \_ type de SID de service INcompatible \_ \_ \_**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



Le démarrage du service a échoué car un ou plusieurs services du même processus ont un paramètre de type de SID de service incompatible. Un service avec un type de SID de service restreint ne peut coexister que dans le même processus avec d’autres services avec un type de SID restreint. Si le type de SID de service de ce service vient d’être configuré, le processus d’hébergement doit être redémarré pour pouvoir démarrer ce service.

Sur Windows Server 2003 et Windows XP, un service non restreint ne peut pas coexister dans le même processus avec d’autres services. Le service avec le type de SID de service non restreint doit être déplacé vers un processus détenu pour pouvoir démarrer ce service.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**\_arrêt du \_ processus de pilote d’erreur \_**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



Le processus qui héberge le pilote de cet appareil a été arrêté.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_limite d’implémentation d’erreur \_**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Une opération a tenté de dépasser une limite définie par l’implémentation.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**le \_ processus d’erreur \_ est \_ protégé**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



Soit le processus cible, soit le processus conteneur du thread cible, est un processus protégé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERREUR de \_ service de notification de \_ \_ retard du client \_**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



Le client de notification de service est trop en retard par rapport à l’état actuel des services de l’ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**QUOTA de disque d’erreur \_ \_ \_ dépassé**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



L’opération de fichier demandée a échoué, car le quota de stockage a été dépassé. Pour libérer de l’espace disque, déplacez les fichiers vers un autre emplacement ou supprimez les fichiers inutiles. Pour plus d’informations, contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**contenu de l’erreur \_ \_ bloqué**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



L’opération de fichier demandée a échoué, car la stratégie de stockage bloque ce type de fichier. Pour plus d’informations, contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**privilège de service d’erreur \_ INcompatible \_ \_**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Un privilège requis par le service pour fonctionner correctement n’existe pas dans la configuration du compte de service. Vous pouvez utiliser le composant logiciel enfichable MMC (Microsoft Management Console) des services (services. msc) et le composant logiciel enfichable MMC paramètres de sécurité locale (secpol. msc) pour afficher la configuration du service et la configuration du compte.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERREUR de blocage de l' \_ application \_**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Un thread impliqué dans cette opération semble ne pas répondre.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**étiquette d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Indique qu’un ID de sécurité particulier ne peut pas être assigné en tant qu’étiquette d’un objet.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur système](system-error-codes.md)
</dt> </dl>

 

 




