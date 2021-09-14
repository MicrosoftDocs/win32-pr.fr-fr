---
description: Décrit les codes d’erreur 0-499 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Codes d’erreur système (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114557"
---
# <a name="system-error-codes-0-499"></a>Codes d’erreur système (0-499)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs comprises entre 0 et 499). Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERREUR de \_ réussite**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



L’opération s’est terminée avec succès.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**fonction d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Fonction incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_fichier d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Le système ne peut pas trouver le fichier spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_chemin d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Le système ne peut pas trouver le chemin spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERREUR \_ trop \_ de \_ \_ fichiers ouverts**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Le système ne peut pas ouvrir le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERREUR d' \_ accès \_ refusé**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



L’accès est refusé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**HANDLE d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Le handle n'est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERREUR de la \_ \_ Corbeille**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Les blocs de contrôle de stockage ont été détruits.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERREUR \_ de \_ mémoire insuffisante \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Nombre de ressources mémoire disponibles insuffisant pour traiter cette commande.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**bloc d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



L’adresse du bloc de contrôle de stockage n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERREUR \_ d' \_ environnement incorrect**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



L’environnement est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**\_format incorrect de l’erreur \_**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Tentative de chargement d’un programme au format incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERREUR \_ d' \_ accès non valide**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Le code d’accès n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERREUR de \_ données non valides \_**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Les données ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERREUR \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Espace de stockage insuffisant pour terminer cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERREUR \_ de \_ lecteur non valide**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Le système ne trouve pas le lecteur spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERREUR dans le \_ \_ répertoire actuel**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Le répertoire ne peut pas être supprimé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERREUR sur le \_ \_ même \_ appareil**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Le système ne peut pas déplacer le fichier vers un autre lecteur de disque.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERREUR \_ \_ plus aucun \_ fichier**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Il n’y a plus de fichiers.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERREUR \_ de \_ protection en écriture**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Le média est protégé en écriture.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERREUR \_ unité incorrecte \_**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Le système ne peut pas trouver l’appareil spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERREUR \_ non \_ prête**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Le périphérique n’est pas prêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERREUR de \_ commande incorrecte \_**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



L’appareil ne reconnaît pas la commande.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**ERREUR \_ CRC**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Erreur de données (vérification de redondance cyclique).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERREUR de \_ longueur incorrecte \_**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Le programme a émis une commande, mais la longueur de la commande est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**recherche d’erreur \_**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Le lecteur ne peut pas localiser une zone ou une piste spécifique sur le disque.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERREUR \_ \_ : disque non DOS \_**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Impossible d’accéder au disque ou à la disquette spécifiés.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_secteur d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Le lecteur ne peut pas trouver le secteur demandé.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERREUR \_ \_ de dépassement du \_ papier**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



L’imprimante n’est plus imprimée.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**erreur d’écriture d’erreur \_ \_**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



Le système ne peut pas écrire sur le périphérique spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**erreur de lecture de l’erreur \_ \_**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



Le système ne peut pas lire à partir du périphérique spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**\_échec de génération d’erreur \_**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Un appareil attaché au système ne fonctionne pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_violation de partage d’erreurs \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Le processus ne peut pas accéder au fichier car ce fichier est utilisé par un autre processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_violation de verrouillage d’erreur \_**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



Le processus ne peut pas accéder au fichier, car un autre processus a verrouillé une partie du fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERREUR \_ disque incorrect \_**
</dt> <dd> <dl> <dt>

34 (0X22)
</dt> <dt>



La mauvaise disquette est dans le lecteur. Insérez %2 (numéro de série du volume : %3) dans le lecteur %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**\_mémoire tampon de partage des erreurs \_ \_ dépassée**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Trop de fichiers ouverts pour le partage.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**\_EOF de handle d’erreur \_**
</dt> <dd> <dl> <dt>

38 (égale 0x26)
</dt> <dt>



La fin du fichier a été atteinte.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**HANDLE d’erreur \_ \_ disque \_ plein**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



Le disque est plein.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERREUR \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



La demande n'est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERREUR \_ REM \_ non \_ List**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Windows ne peut pas trouver le chemin d’accès réseau. Vérifiez que le chemin d’accès réseau est correct et que l’ordinateur de destination n’est pas occupé ou désactivé. si Windows ne parvient toujours pas à trouver le chemin d’accès réseau, contactez votre administrateur réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**nom de l’erreur \_ DUP \_**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



Vous n’êtes pas connecté, car il existe un nom dupliqué sur le réseau. Si vous joignez un domaine, accédez à système dans le panneau de configuration pour modifier le nom de l’ordinateur, puis réessayez. Si vous joignez un groupe de travail, choisissez un autre nom de groupe de travail.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERREUR \_ \_ netpath incorrect**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



Le chemin d’accès réseau est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERREUR \_ réseau \_ occupée**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



Le réseau est occupé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERREUR \_ de \_ développement \_ inexistant**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



La ressource réseau ou l’appareil spécifié n’est plus disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERREUR \_ trop \_ de \_ Cmds**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



La limite de commandes du BIOS réseau a été atteinte.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERREUR \_ adap \_ HDW \_ Err**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Une erreur matérielle de la carte réseau s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERREUR \_ de \_ réponse nette incorrecte \_**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



Le serveur spécifié ne peut pas exécuter l'opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERREUR \_ UNEXP \_ NET \_ Err**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Une erreur réseau inattendue s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERREUR \_ mauvais \_ REM \_ adap**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



La carte à distance n’est pas compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERREUR \_ PRINTQ \_ complète**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



La file d’attente de l’imprimante est pleine.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERREUR \_ aucun \_ espace de spouleur \_**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



L’espace de stockage du fichier en attente d’impression n’est pas disponible sur le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERREUR d' \_ impression \_ annulée**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



Votre fichier en attente d’impression a été supprimé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERREUR \_ NetName \_ supprimé**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Le nom de réseau spécifié n’est plus disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERREUR \_ \_ accès réseau \_ refusé**
</dt> <dd> <dl> <dt>

65 (0x41 vers)
</dt> <dt>



Accès réseau refusé.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERREUR \_ \_ type de développement incorrect \_**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



Le type de ressource réseau n’est pas correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERREUR \_ \_ nom de réseau incorrect \_**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



Le nom du réseau est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERREUR \_ de \_ noms trop nombreux \_**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



La limite de noms de la carte réseau de l’ordinateur local a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERREUR \_ trop \_ de \_ sess**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



La limite de session du BIOS réseau a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**partage d’erreurs \_ \_ suspendu**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



Le serveur distant a été suspendu ou est en cours de démarrage.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERREUR \_ req \_ non \_ ACCEP**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



Aucune autre connexion ne peut être établie à cet ordinateur distant pour l’instant, car il existe déjà autant de connexions que l’ordinateur peut accepter.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**l’inverseur d’erreur est \_ \_ suspendu**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



L’imprimante ou le périphérique de disque spécifié a été suspendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**le \_ fichier d’erreur \_ existe**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



Le fichier existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERREUR \_ Impossible d' \_ effectuer**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



Impossible de créer le répertoire ou le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERREUR d' \_ échec \_ i24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Échec sur INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**erreur \_ lors \_ de l’extraction des \_ structures**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



Stockage pour traiter cette demande n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERREUR \_ déjà \_ assignée**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



Le nom de l’appareil local est déjà utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERREUR \_ \_ de mot de passe non valide**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



Le mot de passe réseau spécifié n’est pas correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**paramètre d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



Le paramètre est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERREUR \_ d' \_ écriture réseau de l’erreur \_**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Une erreur d’écriture s’est produite sur le réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERREUR \_ aucun \_ emplacement de proc. \_**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



Le système ne peut pas démarrer un autre processus pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERREUR \_ trop \_ de \_ sémaphores**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



Impossible de créer un autre sémaphore système.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERREUR \_ excl avec le \_ SEM \_ déjà \_ détenu**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



Le sémaphore exclusif appartient à un autre processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERREUR \_ SEM \_ \_ définie**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



Le sémaphore est défini et ne peut pas être fermé.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERREUR \_ trop \_ de \_ \_ demandes SEM**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



Le sémaphore ne peut pas être de nouveau défini.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERREUR \_ non valide \_ au moment de l' \_ interruption \_**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



Impossible de demander des sémaphores exclusifs au moment de l’interruption.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERREUR \_ SEM \_ propriétaire \_ mort**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



La propriété précédente de ce sémaphore s’est terminée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERREUR \_ de \_ limite utilisateur SEM \_**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Insérez la disquette pour le lecteur %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERREUR \_ de \_ modification du disque**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



Le programme s’est arrêté, car une autre disquette n’a pas été insérée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**lecteur d’erreur \_ \_ verrouillé**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



Le disque est en cours d’utilisation ou verrouillé par un autre processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERREUR \_ de \_ canal rompu**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



Le canal est terminé.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**échec de l’ouverture de l’erreur \_ \_**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



Le système ne peut pas ouvrir le fichier ou l’appareil spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_dépassement de mémoire tampon d’erreur \_**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



Le nom du fichier est trop long.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**disque d’erreur \_ \_ plein**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



Espace insuffisant sur le disque.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERREUR \_ aucun \_ autre \_ handle de recherche \_**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



Aucun autre identificateur de fichier interne n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERREUR \_ de \_ handle cible non valide \_**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



L’identificateur de fichier interne cible est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**catégorie d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



L’appel IOCTL effectué par le programme d’application n’est pas correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERREUR \_ de \_ vérification du commutateur non valide \_**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



La valeur du paramètre de vérification à l’écriture n’est pas correcte.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERREUR \_ de \_ niveau de pilote incorrect \_**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



Le système ne prend pas en charge la commande demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**appel d’erreur \_ \_ non \_ implémenté**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Cette fonction n’est pas prise en charge sur ce système.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERREUR \_ SEM \_ timeout**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



Le délai d’expiration du sémaphore a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERREUR \_ de \_ mémoire tampon insuffisante**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



La zone de données passée à un appel système est insuffisante.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERREUR \_ nom non valide \_**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



La syntaxe du nom de fichier, du nom de répertoire ou de l’étiquette de volume est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**niveau d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



Le niveau d’appel système est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERREUR \_ aucun \_ nom de volume \_**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



Le disque n’a pas de nom de volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**la modification de l’erreur est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



Le module spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**PROC de l’erreur \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



La procédure spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERREUR d' \_ attente \_ aucun \_ enfant**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Il n’y a aucun processus enfant à attendre.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**l' \_ enfant d’erreur \_ n’est pas \_ terminé**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



L’application %1 ne peut pas être exécutée en mode Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_handle d' \_ accès \_ direct d’erreur**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Tentative d’utilisation d’un descripteur de fichier sur une partition de disque ouverte pour une opération autre que des e/s de disque brutes.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERREUR \_ de \_ recherche négative**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Une tentative de déplacement du pointeur de fichier avant le début du fichier a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**\_recherche \_ d’erreur sur l' \_ appareil**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



Impossible de définir le pointeur de fichier sur le périphérique ou le fichier spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**l’erreur \_ est une \_ cible de jointure \_**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



Une commande JOIN ou SUBSt ne peut pas être utilisée pour un lecteur qui contient des lecteurs précédemment joints.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**l’erreur \_ est \_ jointe**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Une tentative d’utilisation d’une commande JOIN ou SUBSt sur un lecteur qui a déjà été jointe a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERREUR \_ \_ subst**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Une tentative d’utilisation d’une commande JOIN ou SUBSt sur un lecteur qui a déjà été remplacé a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERREUR \_ non \_ jointe**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



Le système a tenté de supprimer la jointure d’un lecteur qui n’est pas joint.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERREUR \_ non \_ subsante**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



Le système a essayé de supprimer la substitution d’un lecteur qui n’est pas substitué.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**erreur \_ lors \_ de \_ la jointure**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



Le système a essayé de joindre un lecteur à un répertoire sur un lecteur joint.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERREUR \_ de substitution \_ à \_ subst**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



Le système a essayé de remplacer un lecteur par un répertoire sur un lecteur substitué.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**erreur \_ lors \_ de la jointure à \_ subst**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



Le système a essayé de joindre un lecteur à un répertoire sur un lecteur substitué.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERREUR \_ de substitution \_ pour la \_ jointure**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



Le système a tenté de SUBSTITUer un lecteur à un répertoire sur un lecteur joint.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERREUR \_ de \_ lecteur occupé**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



Le système ne peut pas effectuer de jointure ou de substitution pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERREUR du \_ même \_ lecteur**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



Le système ne peut pas joindre ou substituer un lecteur à ou à un répertoire sur le même lecteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERREUR \_ Rép \_ non \_ racine**
</dt> <dd> <dl> <dt>

144 (0X90)
</dt> <dt>



Le répertoire n’est pas un sous-répertoire du répertoire racine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**le \_ répertoire d’erreur \_ n’est pas \_ vide**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



Le répertoire n'est pas vide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERREUR \_ : \_ subst \_ path**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



Le chemin d’accès spécifié est utilisé dans un substitut.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**l’erreur \_ est un \_ chemin de jointure \_**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



Les ressources disponibles sont insuffisantes pour traiter cette commande.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**\_chemin d’erreur \_ occupé**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



Le chemin d’accès spécifié ne peut pas être utilisé pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**l’erreur \_ est la \_ cible subst \_**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



Une tentative a été faite pour joindre ou remplacer un lecteur pour lequel un répertoire sur le lecteur est la cible d’un substitut précédent.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_suivi du système d’erreur \_**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



Les informations de trace système n’ont pas été spécifiées dans votre fichier CONFIG.SYS, ou le suivi n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**nombre d’événements d’erreur \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



Le nombre d’événements sémaphores spécifiés pour DosMuxSemWait n’est pas correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERREUR \_ trop \_ de \_ MUXWAITERS**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



DosMuxSemWait ne s’est pas exécutée ; trop de sémaphores sont déjà définis.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**\_format de \_ liste non valide d’erreur \_**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



La liste DosMuxSemWait n’est pas correcte.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**étiquette d’erreur \_ \_ trop \_ longue**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



Le nom de volume que vous avez entré dépasse la limite de caractères d’étiquette du système de fichiers cible.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERREUR \_ trop \_ de \_ TCBS**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



Impossible de créer un autre thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**SIGNAL d’erreur \_ \_ refusé**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



Le processus du destinataire a refusé le signal.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERREUR \_ ignorée**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



Le segment est déjà ignoré et ne peut pas être verrouillé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERREUR \_ non \_ verrouillée**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



Le segment est déjà déverrouillé.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**erreur de l’adresse de l’erreur \_ \_ THREADID \_**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



L’adresse de l’ID de thread est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERREUR d' \_ arguments incorrects \_**
</dt> <dd> <dl> <dt>

160 (0xA0)
</dt> <dt>



Un ou plusieurs arguments ne sont pas corrects.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERREUR \_ de \_ nom de chemin incorrect**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



Le chemin d’accès spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**SIGNAL d’erreur \_ \_ en attente**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Un signal est déjà en attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERREUR \_ Max \_ THRDS \_ atteinte**
</dt> <dd> <dl> <dt>

164 (0xA4)
</dt> <dt>



Aucun thread supplémentaire ne peut être créé dans le système.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_échec du verrouillage de l’erreur \_**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



Impossible de verrouiller une région d’un fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERREUR de \_ disponibilité**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



La ressource demandée est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERREUR \_ \_ de prise en charge \_ des périphériques en \_ cours**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



La détection de la prise en charge des commandes de l’appareil est en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERREUR d' \_ annulation de \_ violation**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



Aucune demande de verrou n’était en suspens pour la région d’annulation fournie.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERREUR \_ les \_ verrous atomiques \_ ne sont pas \_ pris en charge**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



Le système de fichiers ne prend pas en charge les modifications atomiques du type de verrou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERREUR \_ \_ numéro de segment non valide \_**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



Le système a détecté un numéro de segment qui n’était pas correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERREUR \_ ordinal non valide \_**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**l' \_ erreur \_ existe déjà**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



Impossible de créer un fichier lorsque ce fichier existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERREUR \_ \_ numéro d’indicateur non valide \_**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



L’indicateur passé n’est pas correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERREUR \_ SEM \_ non \_ trouvée**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



Le nom du sémaphore système spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERREUR \_ de \_ démarrage de CODESEG non valide \_**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERREUR \_ STACKSEG non valide \_**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERREUR \_ MODULETYPE non valide \_**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERREUR \_ de \_ signature exe non valide \_**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



Impossible d’exécuter %1 en mode Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERREUR \_ exe \_ marquée comme \_ non valide**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERREUR \_ \_ format exe \_ erroné**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 n’est pas une application Win32 valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Les \_ données itérées de l’erreur \_ \_ dépassent \_ 64 Ko**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERREUR \_ MINALLOCSIZE non valide \_**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERREUR \_ DynLink \_ de \_ l' \_ anneau non valide**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter ce programme d’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERREUR \_ iopl \_ non \_ activée**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



Le système d’exploitation n’est actuellement pas configuré pour exécuter cette application.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERREUR \_ SEGDPL non valide \_**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**L’erreur \_ AUTODATASEG \_ dépasse \_ 64 Ko**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter ce programme d’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**L’erreur \_ RING2SEG \_ doit \_ être \_ mobile**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



Le segment de code ne peut pas être supérieur ou égal à 64 Ko.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERREUR de \_ chaîne de réadressage \_ \_ XEEDS \_ SEGLIM**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERREUR \_ INFLOOP \_ dans la \_ chaîne de réadressage \_**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



Le système d’exploitation ne peut pas exécuter %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERREUR \_ ENVVAR \_ \_ introuvable**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



Le système n’a pas pu trouver l’option d’environnement qui a été entrée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERREUR \_ aucun \_ signal \_ envoyé**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Aucun processus dans la sous-arborescence de commandes n’a de gestionnaire de signal.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERREUR de \_ nom de fichier \_ EXCED \_ plage**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



Le nom de fichier ou l’extension est trop long.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERREUR \_ \_ de pile RING2 \_ en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



La pile Ring 2 est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERREUR lors de l' \_ \_ expansion meta \_ trop \_ longue**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



Les caractères de nom de fichier globaux, \* ou ?, sont entrés de manière incorrecte ou un trop grand nombre de caractères de nom de fichier Global sont spécifiés.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERREUR \_ \_ numéro de signal non valide \_**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



Le signal en cours de publication n’est pas correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERREUR \_ thread \_ 1 \_ inactive**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



Impossible de définir le gestionnaire de signal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERREUR \_ verrouillée**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



Le segment est verrouillé et ne peut pas être réalloué.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERREUR \_ trop \_ de \_ modules**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



Un trop grand nombre de modules de lien dynamique sont attachés à ce programme ou à ce module de liaison dynamique.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_imbrication d’erreurs \_ non \_ autorisée**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



Impossible d’imbriquer des appels à LoadModule.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de type d’ordinateur exe \_**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



cette version de %1 n’est pas compatible avec la version de Windows que vous exécutez. Vérifiez les informations système de votre ordinateur, puis contactez l’éditeur du logiciel.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**l’erreur \_ exe \_ ne peut pas \_ modifier le \_ \_ binaire signé**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



Le fichier image %1 est signé, impossible à modifier.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**l’erreur \_ exe \_ ne peut pas \_ modifier un \_ \_ binaire signé fort \_**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



Le fichier image %1 est signé avec une signature forte, impossible à modifier.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**fichier d’erreur \_ \_ extrait \_**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



Ce fichier est extrait ou verrouillé pour modification par un autre utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**récupération d’erreur \_ \_ requise**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



Le fichier doit être extrait avant d’enregistrer les modifications.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERREUR \_ de \_ type de fichier incorrect \_**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



Le type de fichier en cours d’enregistrement ou de récupération a été bloqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**fichier d’erreur \_ \_ trop \_ volumineux**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



La taille du fichier dépasse la limite autorisée et ne peut pas être enregistrée.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**authentification par formulaire d’erreur \_ \_ \_ obligatoire**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Accès refusé. Avant d’ouvrir des fichiers à cet emplacement, vous devez d’abord ajouter le site Web à votre liste de sites de confiance, accéder au site Web et sélectionner l’option de connexion automatique.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**VIRUS d’erreur \_ \_ infecté**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



L’opération n’a pas abouti car le fichier contient un virus ou un logiciel potentiellement indésirable.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**VIRUS d’erreur \_ \_ supprimé**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Ce fichier contient un virus ou un logiciel potentiellement indésirable et ne peut pas être ouvert. En raison de la nature de ce virus ou d’un logiciel potentiellement indésirable, le fichier a été supprimé de cet emplacement.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**canal d’erreur \_ \_ local**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



Le canal est local.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERREUR \_ de \_ canal incorrect**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



L’état du canal n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**canal d’erreur \_ \_ occupé**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Toutes les instances de canal sont occupées.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERREUR \_ aucune \_ donnée**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



Le canal est en cours de fermeture.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**canal d’erreur \_ \_ non \_ connecté**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



Aucun traitement à l'autre extrémité du canal


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERREUR \_ plus de \_ données**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



More data is available.


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERREUR \_ VC \_ déconnectée**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



La session a été annulée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERREUR \_ \_ nom EA non valide \_**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



Le nom d’attribut étendu spécifié n’était pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERREUR de \_ liste d’EA non \_ \_ cohérente**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Les attributs étendus sont incohérents.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_délai d’attente**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Expiration du délai d'attente de l'opération d'attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERREUR \_ aucun \_ autre \_ élément**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



Aucune donnée n'est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**\_Impossible de \_ copier l’erreur**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



Les fonctions de copie ne peuvent pas être utilisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**Répertoire d’erreurs \_**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



Le nom du répertoire n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERREUR \_ EAS \_ examinera \_**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Les attributs étendus ne tiennent pas dans la mémoire tampon.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERREUR \_ EA \_ fichier \_ endommagé**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



Le fichier d’attributs étendus sur le système de fichiers monté est endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERREUR \_ de \_ table EA \_ complète**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



Le fichier de la table des attributs étendus est plein.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERREUR \_ de \_ handle EA non valide \_**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



Le handle d’attribut étendu spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERREUR \_ EAS \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



Le système de fichiers monté ne prend pas en charge les attributs étendus.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERREUR \_ non \_ propriétaire**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Tentative de libération du mutex qui n’appartient pas à l’appelant.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERREUR \_ trop \_ de \_ publications**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Un trop grand nombre de publications a été effectué sur un sémaphore.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERREUR \_ de \_ copie partielle**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Seule une partie d’une requête ReadProcessMemory ou WriteProcessMemory a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERREUR \_ OPLOCK \_ non \_ accordée**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



La demande oplock est refusée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERREUR \_ de \_ protocole OPLOCK non valide \_**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



Un accusé de réception oplock non valide a été reçu par le système.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**disque d’erreur \_ \_ trop \_ fragmenté**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



Le volume est trop fragmenté pour terminer cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERREUR de \_ suppression \_ en attente**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



Impossible d’ouvrir le fichier, car il est en cours de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERREUR \_ d’incompatibilité \_ avec le \_ paramètre de \_ \_ Registre de nom abrégé \_ global \_**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



Les paramètres de nom abrégé ne peuvent pas être modifiés sur ce volume en raison du paramètre de registre global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_noms courts \_ \_ d’erreur non \_ activés \_ sur le \_ volume**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



Les noms courts ne sont pas activés sur ce volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**le \_ flux de sécurité d’erreur \_ \_ est \_ incohérent**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



Le flux de sécurité du volume donné est dans un état incohérent. Exécutez CHKDSK sur le volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERREUR \_ de \_ plage de verrouillage non valide \_**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



Une opération de verrouillage de fichier demandée ne peut pas être traitée en raison d’une plage d’octets non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_ \_ sous-système d’image d' \_ erreur absent \_**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



Le sous-système nécessaire pour prendre en charge le type d’image n’est pas présent.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID de notification d’erreur \_ \_ \_ déjà \_ défini**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



Un GUID de notification est déjà associé au fichier spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERREUR \_ de \_ Gestionnaire d’exceptions non valide \_**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



Une routine de gestionnaire d’exceptions non valide a été détectée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**privilèges d’erreur \_ dupliqués \_**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Des privilèges en double ont été spécifiés pour le jeton.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERREUR \_ aucune \_ plage \_ traitée**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



Aucune plage pour l’opération spécifiée n’a pu être traitée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERREUR \_ non \_ autorisée \_ sur \_ le \_ fichier système**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



L’opération n’est pas autorisée sur un fichier interne du système de fichiers.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERREURS \_ de \_ ressources de disque \_ épuisées**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Les ressources physiques de ce disque ont été épuisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERREUR \_ de \_ jeton non valide**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



Le jeton représentant les données n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**fonctionnalité de périphérique d’erreur \_ \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



L’appareil ne prend pas en charge la fonctionnalité de commande.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERREUR \_ Mr \_ Mid \_ \_ introuvable**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



Le système ne trouve pas de texte de message pour le numéro de message 0x %1 dans le fichier de message pour %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**étendue de l’erreur \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



L’étendue spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**\_étendue non définie par \_ erreur**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



La stratégie d’accès centralisée spécifiée n’est pas définie sur l’ordinateur cible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERREUR \_ Cap non valide \_**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



La stratégie d’accès centralisée obtenue à partir de Active Directory n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERREUR de \_ périphérique \_ inaccessible**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



L’appareil est inaccessible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**périphérique d’erreur- \_ \_ aucune \_ ressource**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



L’appareil cible ne dispose pas de ressources suffisantes pour terminer l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**erreur \_ de \_ somme de contrôle des données d’erreur \_**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Une erreur de somme de contrôle d’intégrité des données s’est produite. Les données du flux de fichier sont endommagées.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERREUR de l' \_ \_ \_ Opération EA \_ du noyau intermixed**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



Une tentative a été effectuée pour modifier à la fois un noyau et un attribut étendu normal (EA) dans la même opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**\_suppression du niveau de fichier erreur \_ \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



L’appareil ne prend pas en charge la suppression au niveau du fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERREUR d' \_ alignement du décalage de l’erreur \_ \_**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



La commande a spécifié un décalage de données qui n’est pas aligné sur la granularité/l’alignement de l’appareil.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**\_champ d’erreur non valide \_ dans la \_ \_ liste de paramètres \_**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



La commande a spécifié un champ non valide dans sa liste de paramètres.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERREUR \_ \_ de l’opération en \_ cours**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



Une opération est actuellement en cours avec l’appareil.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERREUR de chemin de l' \_ appareil incorrect \_ \_**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



Une tentative d’envoi de la commande via un chemin d’accès non valide à l’appareil cible a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERREUR \_ trop \_ nombreux \_ descripteurs**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



La commande a spécifié plusieurs descripteurs qui ont dépassé le nombre maximal pris en charge par l’appareil.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERREUR de \_ nettoyage des \_ données \_ désactivée**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



Le nettoyage est désactivé sur le fichier spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERREUR \_ de \_ stockage non redondant \_**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



Le périphérique de stockage ne fournit pas de redondance.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_fichier résident \_ erroné \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



Une opération n’est pas prise en charge sur un fichier résident.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERREUR \_ \_ fichier compressé \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



Une opération n’est pas prise en charge sur un fichier compressé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**Répertoire d’erreurs \_ \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



Une opération n’est pas prise en charge sur un répertoire.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**erreur \_ lors \_ de la lecture \_ de la \_ copie**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



Impossible de lire la copie spécifiée des données demandées.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERREUR d' \_ échec \_ NoAction de \_ redémarrage**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



Aucune action n’a été effectuée, car un redémarrage du système est nécessaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERREUR lors de l' \_ \_ arrêt**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



Échec de l’opération d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**\_échec du \_ redémarrage de l’erreur**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



L’opération de redémarrage a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERREUR \_ Max \_ sessions \_ atteintes**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



Le nombre maximal de sessions a été atteint.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**le \_ mode thread d’erreur est \_ \_ déjà en \_ arrière-plan**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



Le thread est déjà en mode de traitement en arrière-plan.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**MODE de thread d’erreur \_ \_ \_ non en \_ arrière-plan**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



Le thread n’est pas en mode de traitement en arrière-plan.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**le mode de traitement des erreurs est \_ \_ \_ déjà en \_ arrière-plan**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



Le processus est déjà en mode de traitement en arrière-plan.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**erreur de mode de traitement d’erreur \_ \_ \_ non en \_ arrière-plan**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



Le processus n’est pas en mode de traitement en arrière-plan.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**\_adresse non valide de l’erreur \_**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Tentative d’accès à une adresse non valide.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>WinError. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur système](system-error-codes.md)
</dt> </dl>

 

 




