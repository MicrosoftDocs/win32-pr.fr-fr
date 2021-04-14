---
description: Décrit les codes d’erreur 500-999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Codes d’erreur système (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201063"
---
# <a name="system-error-codes-500-999"></a>Codes d’erreur système (500-999)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 500 à 999). Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERREUR \_ de \_ chargement du profil utilisateur \_**
</dt> <dd> <dl> <dt>

500 (0x1F4)
</dt> <dt>



Impossible de charger le profil utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_dépassement arithmétique de l’erreur \_**
</dt> <dd> <dl> <dt>

534 (0x216)
</dt> <dt>



Le résultat arithmétique a dépassé 32 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**canal d’erreur \_ \_ connecté**
</dt> <dd> <dl> <dt>

535 (0x217)
</dt> <dt>



Il existe un processus à l’autre extrémité du canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**\_écoute du canal d’erreur \_**
</dt> <dd> <dl> <dt>

536 (0x218)
</dt> <dt>



En attente d’un processus pour ouvrir l’autre extrémité du canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**arrêt du vérificateur d’erreurs \_ \_**
</dt> <dd> <dl> <dt>

537 (0x219)
</dt> <dt>



Le vérificateur d’applications a rencontré une erreur dans le processus en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**erreur \_ ABIOS \_ erreur**
</dt> <dd> <dl> <dt>

538 (0x21A)
</dt> <dt>



Une erreur s’est produite dans le sous-système ABIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**\_Avertissement WX86 d’erreur \_**
</dt> <dd> <dl> <dt>

539 (0x21B)
</dt> <dt>



Un avertissement s’est produit dans le sous-système WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Erreur \_ WX86 \_ erreur**
</dt> <dd> <dl> <dt>

540 (0x21C)
</dt> <dt>



Une erreur s’est produite dans le sous-système WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_minuteur d’erreur \_ non \_ annulé**
</dt> <dd> <dl> <dt>

541 (0x21D)
</dt> <dt>



Une tentative a été effectuée pour annuler ou définir un minuteur associé à un APC et le thread d’objet n’est pas le thread qui a défini à l’origine le minuteur avec une routine APC associée.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERREUR lors du \_ déroulement**
</dt> <dd> <dl> <dt>

542 (0x21E)
</dt> <dt>



Code d’exception de déroulement.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERREUR \_ pile incorrecte \_**
</dt> <dd> <dl> <dt>

543 (0x21F)
</dt> <dt>



Une pile non valide ou non alignée a été rencontrée lors d’une opération de déroulement.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERREUR d’une \_ cible de déroulement non valide \_ \_**
</dt> <dd> <dl> <dt>

544 (0x220)
</dt> <dt>



Une cible de déroulement non valide a été rencontrée pendant une opération de déroulement.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**\_attributs de \_ port non valides d’erreur \_**
</dt> <dd> <dl> <dt>

545 (0x221)
</dt> <dt>



Attributs d’objet non valides spécifiés pour NtCreatePort ou les attributs de port non valides spécifiés à NtConnectPort


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**MESSAGE de port d’erreur \_ \_ \_ trop \_ long**
</dt> <dd> <dl> <dt>

546 (0x222)
</dt> <dt>



La longueur du message transmis à NtRequestPort ou NtRequestWaitReplyPort était plus longue que le message maximal autorisé par le port.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERREUR \_ de \_ quota non valide \_ inférieure**
</dt> <dd> <dl> <dt>

547 (0x223)
</dt> <dt>



Une tentative a été effectuée pour réduire une limite de quota au-dessous de l’utilisation actuelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**périphérique d’erreur \_ \_ déjà \_ attaché**
</dt> <dd> <dl> <dt>

548 (0x224)
</dt> <dt>



Une tentative d’attachement à un appareil déjà attaché à un autre périphérique a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ALIGNEMENT incorrect de l’instruction d’erreur \_ \_**
</dt> <dd> <dl> <dt>

549 (0x225)
</dt> <dt>



Une tentative a été effectuée pour exécuter une instruction à une adresse non alignée et le système hôte ne prend pas en charge les références d’instruction non alignées.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**le \_ profilage des erreurs \_ n' \_ a pas démarré**
</dt> <dd> <dl> <dt>

550 (0x226)
</dt> <dt>



Le profilage n’a pas démarré.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERREUR de \_ profilage \_ non \_ arrêté**
</dt> <dd> <dl> <dt>

551 (0x227)
</dt> <dt>



Le profilage n’est pas arrêté.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**l’erreur \_ n’a \_ pas pu être \_ interprétée**
</dt> <dd> <dl> <dt>

552 (0x228)
</dt> <dt>



La liste de contrôle d’accès passée ne contenait pas les informations minimales requises.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERREUR \_ de profilage \_ à la \_ limite**
</dt> <dd> <dl> <dt>

553 (0x229)
</dt> <dt>



Le nombre d’objets de profilage actifs est au maximum et il n’est plus possible de démarrer.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERREUR \_ Impossible d' \_ attendre**
</dt> <dd> <dl> <dt>

554 (0x22A)
</dt> <dt>



Permet d’indiquer qu’une opération ne peut pas continuer sans blocage pour les e/s.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERREUR \_ Impossible de \_ se terminer \_ automatiquement**
</dt> <dd> <dl> <dt>

555 (0x22B)
</dt> <dt>



Indique qu’un thread a tenté de se terminer lui-même par défaut (appelé NtTerminateThread avec **null**) et qu’il s’agissait du dernier thread du processus en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERREUR \_ \_ mm inattendu \_ créer \_ Err**
</dt> <dd> <dl> <dt>

556 (0x22C)
</dt> <dt>



Si une erreur MM non définie dans le filtre standard FsRtl est renvoyée, elle est convertie en l’une des erreurs suivantes, qui est garantie comme étant dans le filtre. Dans ce cas, les informations sont perdues, mais le filtre gère correctement l’exception.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**erreur \_ de \_ carte mm inattendue \_ \_**
</dt> <dd> <dl> <dt>

557 (0x22D)
</dt> <dt>



Si une erreur MM non définie dans le filtre standard FsRtl est renvoyée, elle est convertie en l’une des erreurs suivantes, qui est garantie comme étant dans le filtre. Dans ce cas, les informations sont perdues, mais le filtre gère correctement l’exception.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERREUR de l' \_ \_ \_ extension mm inattendu \_**
</dt> <dd> <dl> <dt>

558 (0x22E)
</dt> <dt>



Si une erreur MM non définie dans le filtre standard FsRtl est renvoyée, elle est convertie en l’une des erreurs suivantes, qui est garantie comme étant dans le filtre. Dans ce cas, les informations sont perdues, mais le filtre gère correctement l’exception.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERREUR \_ de \_ table de fonction incorrecte \_**
</dt> <dd> <dl> <dt>

559 (0x22F)
</dt> <dt>



Une table de fonctions incorrecte a été rencontrée lors d’une opération de déroulement.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERREUR \_ aucune \_ traduction de GUID \_**
</dt> <dd> <dl> <dt>

560 (0X230)
</dt> <dt>



Indique qu’une tentative d’attribution d’une protection à un répertoire ou à un fichier du système de fichiers a été effectuée et que l’un des SID du descripteur de sécurité n’a pas pu être traduit dans un GUID pouvant être stocké par le système de fichiers. Cela provoque l’échec de la tentative de protection, ce qui peut entraîner l’échec d’une tentative de création de fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERREUR \_ de \_ taille de LDT non valide \_**
</dt> <dd> <dl> <dt>

561 (0x231)
</dt> <dt>



Indique qu’une tentative a été effectuée pour augmenter une LDT en définissant sa taille, ou que la taille n’est pas un nombre pair de sélecteurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERREUR \_ de \_ décalage de LDT non valide \_**
</dt> <dd> <dl> <dt>

563 (0x233)
</dt> <dt>



Indique que la valeur de départ des informations LDT n’était pas un multiple entier de la taille du sélecteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERREUR \_ de \_ \_ descripteur LDT non valide**
</dt> <dd> <dl> <dt>

564 (0x234)
</dt> <dt>



Indique que l’utilisateur a fourni un descripteur non valide lors de la tentative de configuration des descripteurs LDT.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERREUR \_ trop \_ grand nombre de \_ threads**
</dt> <dd> <dl> <dt>

565 (0x235)
</dt> <dt>



Indique qu’un processus dispose d’un trop grand nombre de threads pour exécuter l’action demandée. Par exemple, l’assignation d’un jeton principal ne peut être effectuée que lorsqu’un processus a zéro ou un thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_thread \_ d’erreur non dans le \_ \_ processus**
</dt> <dd> <dl> <dt>

566 (0x236)
</dt> <dt>



Une tentative a été effectuée pour fonctionner sur un thread dans un processus spécifique, mais le thread spécifié n’est pas dans le processus spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERREUR \_ de \_ dépassement du quota du fichier d’échange \_**
</dt> <dd> <dl> <dt>

567 (0x237)
</dt> <dt>



Le quota du fichier d’échange a été dépassé.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERREUR \_ de \_ conflit de serveur d’ouverture de session \_**
</dt> <dd> <dl> <dt>

568 (0x238)
</dt> <dt>



Le service Netlogon ne peut pas démarrer, car un autre service Netlogon en cours d’exécution dans le domaine est en conflit avec le rôle spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**synchronisation des erreurs \_ \_ requise**
</dt> <dd> <dl> <dt>

569 (0x239)
</dt> <dt>



La base de données SAM sur un serveur Windows n’est pas très synchronisée avec la copie sur le contrôleur de domaine. Une synchronisation complète est nécessaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERREUR \_ NET \_ Open \_ échec**
</dt> <dd> <dl> <dt>

570 (0x23A)
</dt> <dt>



Échec de l’API NtCreateFile. Cette erreur ne doit jamais être renvoyée à une application, il s’agit d’un espace réservé pour le redirecteur Windows LAN Manager à utiliser dans ses routines de mappage des erreurs internes.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERREUR \_ d' \_ échec du privilège d’e/s \_**
</dt> <dd> <dl> <dt>

571 (0x23B)
</dt> <dt>



{Échec du privilège} Les autorisations d’e/s pour le processus n’ont pas pu être modifiées.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**contrôle d’erreur \_ \_ C \_ Exit**
</dt> <dd> <dl> <dt>

572 (0x23C)
</dt> <dt>



{Quitter l’application par CTRL + C} L’application s’est arrêtée à la suite d’un CTRL + C.


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERREUR \_ manquant \_ SYSTEMFILE**
</dt> <dd> <dl> <dt>

573 (0x23D)
</dt> <dt>



{Fichier système manquant} Le fichier système requis% HS est incorrect ou manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERREUR d' \_ exception non gérée \_**
</dt> <dd> <dl> <dt>

574 (0x23E)
</dt> <dt>



{Erreur d’application} L’exception% s (0x% 08lX) s’est produite dans l’application à l’emplacement 0x% 08lX.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**échec de l’initialisation de l’application d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

575 (0x23F)
</dt> <dt>



{Erreur d’application} L’application n’a pas pu démarrer correctement (0x% LX). Cliquez sur OK pour fermer l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERREUR lors de la \_ création du fichier d’échange \_ \_**
</dt> <dd> <dl> <dt>

576 (0x240)
</dt> <dt>



{Impossible de créer le fichier d’échange} Échec de la création du fichier d’échange% HS (% LX). La taille demandée était de% LD.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERREUR \_ de \_ hachage d’image non valide \_**
</dt> <dd> <dl> <dt>

577 (0x241)
</dt> <dt>



Windows ne peut pas vérifier la signature numérique de ce fichier. Une modification récente du matériel ou des logiciels a peut-être installé un fichier qui est signé de manière incorrecte ou endommagée, ou qui peut être un logiciel malveillant provenant d’une source inconnue.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERREUR \_ aucun \_ fichier d’échange**
</dt> <dd> <dl> <dt>

578 (0x242)
</dt> <dt>



{Aucun fichier d’échange spécifié} Aucun fichier d’échange n’a été spécifié dans la configuration du système.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERREUR \_ de \_ contexte flottant non conforme \_**
</dt> <dd> <dl> <dt>

579 (0x243)
</dt> <dt>



TITRE Une application en mode réel a émis une instruction à virgule flottante et un matériel à virgule flottante n’est pas présent.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERREUR \_ aucune \_ paire d’événements \_**
</dt> <dd> <dl> <dt>

580 (0x244)
</dt> <dt>



Une opération de synchronisation de paire d’événements a été effectuée à l’aide de l’objet de paire d’événements client/serveur spécifique au thread, mais aucun objet de paire d’événements n’a été associé au thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**\_erreur de \_ configuration du \_ domaine d’erreur \_**
</dt> <dd> <dl> <dt>

581 (0x245)
</dt> <dt>



La configuration d’un serveur Windows est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERREUR \_ \_ caractère illégal**
</dt> <dd> <dl> <dt>

582 (0x246)
</dt> <dt>



Un caractère non conforme a été rencontré. Pour un jeu de caractères multioctets, cela comprend un octet de tête sans l’octet de fin suivant. Pour le jeu de caractères Unicode, cela comprend les caractères 0xFFFF et 0xFFFE.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**\_caractère non défini d' \_ erreur**
</dt> <dd> <dl> <dt>

583 (0x247)
</dt> <dt>



Le caractère Unicode n’est pas défini dans le jeu de caractères Unicode installé sur le système.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**\_volume de disquette d’erreur \_**
</dt> <dd> <dl> <dt>

584 (0x248)
</dt> <dt>



Le fichier d’échange ne peut pas être créé sur une disquette.


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**erreur \_ lors \_ \_ de la \_ connexion de l' \_ interruption par le BIOS**
</dt> <dd> <dl> <dt>

585 (0x249)
</dt> <dt>



Le BIOS du système n’a pas pu connecter une interruption système à l’appareil ou au bus pour lequel l’appareil est connecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERREUR \_ de \_ contrôleur de sauvegarde**
</dt> <dd> <dl> <dt>

586 (0x24A)
</dt> <dt>



Cette opération est autorisée uniquement pour le contrôleur de domaine principal du domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERREUR \_ de \_ limite de mutant \_ dépassée**
</dt> <dd> <dl> <dt>

587 (0x24B)
</dt> <dt>



Une tentative a été effectuée pour acquérir un mutant de telle sorte que son nombre maximal aurait été dépassé.


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**pilote d’erreur \_ FS \_ \_ requis**
</dt> <dd> <dl> <dt>

588 (0x24C)
</dt> <dt>



Un volume a fait l’accès à un pilote de système de fichiers qui n’a pas encore été chargé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERREUR \_ Impossible de \_ charger le \_ fichier de Registre \_**
</dt> <dd> <dl> <dt>

589 (0x24D)
</dt> <dt>



{Échec du fichier du Registre} Le registre ne peut pas charger la ruche (fichier) :% HS ou son journal ou un autre fichier journal. Elle est endommagée, absente ou non accessible en écriture.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERREUR \_ échec du débogage de l' \_ attachement \_**
</dt> <dd> <dl> <dt>

590 (0x24E)
</dt> <dt>



{Défaillance inattendue dans [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Une erreur inattendue s’est produite lors du traitement d’une demande d’API **DebugActiveProcess** . Vous pouvez choisir OK pour mettre fin au processus ou annuler pour ignorer l’erreur.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERREUR \_ de \_ processus système \_ terminé**
</dt> <dd> <dl> <dt>

591 (0x24F)
</dt> <dt>



{Erreur système irrécupérable} Le processus système% HS s’est arrêté de façon inattendue avec l’état 0x% 08X (0x% 08X 0x% 08X). Le système a été arrêté.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**données d’erreur \_ \_ non \_ acceptées**
</dt> <dd> <dl> <dt>

592 (0x250)
</dt> <dt>



{Données non acceptées} Le client TDI n’a pas pu traiter les données reçues pendant une indication.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERREUR de matériel d’erreur \_ VDM \_ \_**
</dt> <dd> <dl> <dt>

593 (0x251)
</dt> <dt>



NTVDM a rencontré une erreur matérielle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**\_ \_ \_ délai d’annulation du pilote d’erreur**
</dt> <dd> <dl> <dt>

594 (0x252)
</dt> <dt>



{Cancel Timeout} Le pilote% HS n’a pas pu terminer une requête d’e/s annulée dans le délai imparti.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**incompatibilité de message de réponse d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

595 (0x253)
</dt> <dt>



{Concordance des messages de réponse} Une tentative de réponse à un message LPC a été effectuée, mais le thread spécifié par l’ID client dans le message n’attendait pas ce message.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERREUR de \_ perte de \_ \_ données WRITEBEHIND**
</dt> <dd> <dl> <dt>

596 (0x254)
</dt> <dt>



{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS. Les données ont été perdues. Cette erreur peut être due à une défaillance du matériel de votre ordinateur ou de la connexion réseau. Essayez d’enregistrer ce fichier ailleurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERREUR \_ de \_ paramètres du serveur client \_ \_ non valide**
</dt> <dd> <dl> <dt>

597 (0x255)
</dt> <dt>



Le ou les paramètres transmis au serveur dans la fenêtre de mémoire partagée client/serveur ne sont pas valides. Une trop grande quantité de données a peut-être été placée dans la fenêtre mémoire partagée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERREUR \_ de \_ flux non Tiny \_**
</dt> <dd> <dl> <dt>

598 (0x256)
</dt> <dt>



Le flux n’est pas un flux minuscule.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**dépassement de la pile des erreurs \_ \_ \_ en lecture**
</dt> <dd> <dl> <dt>

599 (0x257)
</dt> <dt>



La requête doit être gérée par le code de dépassement de capacité de la pile.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERREUR \_ \_ de conversion en \_ grande**
</dt> <dd> <dl> <dt>

600 (0x258)
</dt> <dt>



Codes d’État OFS internes indiquant comment une opération d’allocation est gérée. Soit une nouvelle tentative est effectuée après le déplacement du onode conteneur, soit le flux d’étendue est converti en un flux volumineux.


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERREUR \_ trouvée \_ hors \_ de l' \_ étendue**
</dt> <dd> <dl> <dt>

601 (0x259)
</dt> <dt>



La tentative de recherche de l’objet a trouvé un objet correspondant à l’ID sur le volume, mais il n’est pas dans l’étendue du descripteur utilisé pour l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERREUR d' \_ allocation du \_ compartiment**
</dt> <dd> <dl> <dt>

602 (0x25A)
</dt> <dt>



Le tableau de compartiments doit être augmenté. Nouvelle tentative de transaction.


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERREUR de \_ marshaling de \_ dépassement**
</dt> <dd> <dl> <dt>

603 (0x25B)
</dt> <dt>



La mémoire tampon de marshaling utilisateur/noyau a débordé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERREUR \_ Variant non valide \_**
</dt> <dd> <dl> <dt>

604 (0x25C)
</dt> <dt>



La structure de variante fournie contient des données non valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERREUR \_ de \_ mémoire tampon de compression incorrecte \_**
</dt> <dd> <dl> <dt>

605 (0x25D)
</dt> <dt>



La mémoire tampon spécifiée contient des données incorrectes.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**\_échec de l’audit d’erreurs \_**
</dt> <dd> <dl> <dt>

606 (0x25E)
</dt> <dt>



{Échec de l’audit} Une tentative de génération d’un audit de sécurité a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**résolution de l’horloge d’erreur \_ \_ \_ non \_ définie**
</dt> <dd> <dl> <dt>

607 (0x25F)
</dt> <dt>



La résolution de la minuterie n’a pas été définie précédemment par le processus en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERREUR \_ \_ d’informations d’ouverture de session insuffisantes \_**
</dt> <dd> <dl> <dt>

608 (0x260)
</dt> <dt>



Les informations de compte sont insuffisantes pour vous connecter.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERREUR \_ de \_ point d’entrée de dll erroné \_**
</dt> <dd> <dl> <dt>

609 (0x261)
</dt> <dt>



{EntryPoint DLL non valide} La bibliothèque de liens dynamiques% HS n’est pas écrite correctement. Le pointeur de pile a été laissé dans un état incohérent. Le point d’entrée doit être déclaré en tant que WINAPI ou STDCALL. Sélectionnez Oui pour faire échouer le chargement de la DLL. Sélectionnez non pour poursuivre l’exécution. La sélection de l’option non peut entraîner un fonctionnement incorrect de l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERREUR \_ de \_ point d’entrée de service incorrect \_**
</dt> <dd> <dl> <dt>

610 (0x262)
</dt> <dt>



{Point d’entrée de rappel de service non valide} Le service% HS n’est pas écrit correctement. Le pointeur de pile a été laissé dans un état incohérent. Le point d’entrée de rappel doit être déclaré en tant que WINAPI ou STDCALL. Si vous sélectionnez OK, le service continue de fonctionner. Toutefois, le processus de service peut ne pas fonctionner correctement.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERREUR \_ d' \_ adresse IP \_ CONFLICT1**
</dt> <dd> <dl> <dt>

611 (0x263)
</dt> <dt>



Il existe un conflit d’adresse IP avec un autre système sur le réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERREUR \_ d' \_ adresse IP \_ CONFLICT2**
</dt> <dd> <dl> <dt>

612 (0x264)
</dt> <dt>



Il existe un conflit d’adresse IP avec un autre système sur le réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_limite de \_ quota du registre des erreurs \_**
</dt> <dd> <dl> <dt>

613 (0x265)
</dt> <dt>



{Espace du Registre insuffisant} Le système a atteint la taille maximale autorisée pour la partie système du Registre. Les demandes de stockage supplémentaires seront ignorées.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERREUR \_ aucun \_ rappel \_ actif**
</dt> <dd> <dl> <dt>

614 (0x266)
</dt> <dt>



Impossible d’exécuter un service système de retour de rappel quand aucun rappel n’est actif.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERREUR \_ Pwd \_ trop \_ brève**
</dt> <dd> <dl> <dt>

615 (0x267)
</dt> <dt>



Le mot de passe fourni est trop petit pour respecter la stratégie de votre compte d’utilisateur. Veuillez choisir un mot de passe plus long.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERREUR \_ Pwd \_ trop \_ récente**
</dt> <dd> <dl> <dt>

616 (0x268)
</dt> <dt>



La stratégie de votre compte d’utilisateur ne vous permet pas de modifier les mots de passe trop fréquemment. Cela permet d’empêcher les utilisateurs de revenir à un mot de passe connu, mais potentiellement découvert. Si vous pensez que votre mot de passe a été compromis, contactez immédiatement votre administrateur pour lui attribuer un nouveau.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERREUR \_ de \_ conflit historique pwd \_**
</dt> <dd> <dl> <dt>

617 (0x269)
</dt> <dt>



Vous avez tenté de remplacer votre mot de passe par un mot de passe que vous avez utilisé par le passé. La stratégie de votre compte d’utilisateur ne l’autorise pas. Veuillez sélectionner un mot de passe que vous n’avez pas utilisé précédemment.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERREUR de \_ compression non prise en charge \_**
</dt> <dd> <dl> <dt>

618 (0x26A)
</dt> <dt>



Le format de compression spécifié n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERREUR \_ \_ Profil matériel non valide \_**
</dt> <dd> <dl> <dt>

619 (0x26B)
</dt> <dt>



La configuration du profil matériel spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERREUR de chemin de l' \_ \_ appareil PLUGPLAY non valide \_ \_**
</dt> <dd> <dl> <dt>

620 (0x26C)
</dt> <dt>



Le chemin d’accès de l’appareil du Registre Plug-and-Play spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**Liste des quotas d’erreurs \_ \_ \_ incohérente**
</dt> <dd> <dl> <dt>

621 (0x26D)
</dt> <dt>



La liste de quotas spécifiée est incohérente en interne avec son descripteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**EXPIRATION de l’évaluation de l’erreur \_ \_**
</dt> <dd> <dl> <dt>

622 (0x26E)
</dt> <dt>



{Notification d’évaluation Windows} La période d’évaluation de cette installation de Windows a expiré. Ce système s’arrêtera dans 1 heure. Pour restaurer l’accès à cette installation de Windows, mettez à niveau cette installation à l’aide d’une distribution sous licence de ce produit.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERREUR \_ de \_ réadressage de dll non conforme \_**
</dt> <dd> <dl> <dt>

623 (0x26F)
</dt> <dt>



{Réadressage de DLL système non conforme} La DLL système% HS a été déplacée en mémoire. L’application ne s’exécutera pas correctement. Le réadressage s’est produit parce que la DLL% HS occupait une plage d’adresses réservée aux DLL système Windows. Le fournisseur qui fournit la DLL doit être contacté pour obtenir une nouvelle DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**échec de l’initialisation de la dll d’erreur \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

624 (0x270)
</dt> <dt>



{Échec de l’initialisation de la DLL} L’application n’a pas pu s’initialiser en raison de l’arrêt de la station Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERREUR de validation de la \_ \_ poursuite**
</dt> <dd> <dl> <dt>

625 (0x271)
</dt> <dt>



Le processus de validation doit passer à l’étape suivante.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERREUR \_ \_ plus aucune \_ correspondance**
</dt> <dd> <dl> <dt>

626 (0x272)
</dt> <dt>



Il n’y a plus de correspondances pour l’énumération d’index actuelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_conflit de \_ liste de plages d’erreurs \_**
</dt> <dd> <dl> <dt>

627 (0x273)
</dt> <dt>



La plage n’a pas pu être ajoutée à la liste de plages en raison d’un conflit.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**incompatibilité de SID de serveur d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

628 (0x274)
</dt> <dt>



Le processus serveur s’exécute sous un SID différent de celui requis par le client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERREUR \_ Impossible d' \_ activer \_ Deny \_ uniquement**
</dt> <dd> <dl> <dt>

629 (0x275)
</dt> <dt>



Il n’est pas possible d’activer un groupe marqué utiliser pour un refus uniquement.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERREUR \_ - \_ plusieurs \_ Erreurs flottantes**
</dt> <dd> <dl> <dt>

630 (0x276)
</dt> <dt>



TITRE Erreurs à virgule flottante multiples.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERREUR \_ flottant \_ plusieurs \_ interruptions**
</dt> <dd> <dl> <dt>

631 (0x277)
</dt> <dt>



TITRE Interruptions multiples à virgule flottante.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERREUR \_ NOinterface**
</dt> <dd> <dl> <dt>

632 (0x278)
</dt> <dt>



L’interface demandée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**échec de la mise en veille du pilote d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

633 (0x279)
</dt> <dt>



{Échec du système de mise en veille} Le pilote% HS ne prend pas en charge le mode veille. La mise à jour de ce pilote peut permettre au système de passer en mode veille.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERREUR \_ de \_ fichier système endommagé \_**
</dt> <dd> <dl> <dt>

634 (0x27A)
</dt> <dt>



Le fichier système %1 est devenu endommagé et a été remplacé.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERREUR d' \_ engagement \_ minimum**
</dt> <dd> <dl> <dt>

635 (0x27B)
</dt> <dt>



{Mémoire virtuelle minimale trop faible} La mémoire virtuelle de votre système est insuffisante. Windows est l’extension de la taille de votre fichier d’échange de mémoire virtuelle. Pendant ce processus, les demandes de mémoire pour certaines applications peuvent être refusées. Pour plus d’informations, consultez l’aide de.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERREUR \_ d' \_ énumération du redémarrage PNP \_**
</dt> <dd> <dl> <dt>

636 (0x27C)
</dt> <dt>



Un appareil a été supprimé. l’énumération doit donc être redémarrée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERREUR \_ de \_ \_ signature incorrecte de l’image système \_**
</dt> <dd> <dl> <dt>

637 (0x27D)
</dt> <dt>



{Erreur système irrécupérable} L’image système% s n’est pas correctement signée. Le fichier a été remplacé par le fichier signé. Le système a été arrêté.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERREUR \_ de \_ redémarrage PNP \_ requis**
</dt> <dd> <dl> <dt>

638 (0x27E)
</dt> <dt>



L’appareil ne démarre pas sans redémarrage.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERREUR \_ d’alimentation insuffisante \_**
</dt> <dd> <dl> <dt>

639 (0x27F)
</dt> <dt>



Il n’y a pas suffisamment de puissance pour terminer l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERREUR \_ - \_ violation de plusieurs erreurs \_**
</dt> <dd> <dl> <dt>

640 (0x280)
</dt> <dt>



ERREUR \_ - \_ violation de plusieurs erreurs \_


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERREUR lors de l' \_ arrêt du système \_**
</dt> <dd> <dl> <dt>

641 (0x281)
</dt> <dt>



Le système est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**PORT d’erreur \_ \_ non \_ défini**
</dt> <dd> <dl> <dt>

642 (0x282)
</dt> <dt>



Une tentative de suppression d’un processus a été effectuée, mais aucun port n’est déjà associé au processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERREUR de vérification de la \_ version du service d’annuaire \_ \_ \_**
</dt> <dd> <dl> <dt>

643 (0x283)
</dt> <dt>



Cette version de Windows n’est pas compatible avec la version de comportement de la forêt de l’annuaire, du domaine ou du contrôleur de domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_plage d' \_ Erreurs \_ introuvable**
</dt> <dd> <dl> <dt>

644 (0x284)
</dt> <dt>



La plage spécifiée est introuvable dans la liste des plages.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERREUR de \_ non- \_ \_ pilote en mode sans échec \_**
</dt> <dd> <dl> <dt>

646 (0x286)
</dt> <dt>



Le pilote n’a pas été chargé, car le système démarre en mode sans échec.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERREUR lors de l' \_ \_ entrée du pilote \_**
</dt> <dd> <dl> <dt>

647 (0x287)
</dt> <dt>



Le pilote n’a pas été chargé car son appel d’initialisation a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**erreur \_ d' \_ énumération des périphériques d’erreur \_**
</dt> <dd> <dl> <dt>

648 (0x288)
</dt> <dt>



« % HS » a rencontré une erreur lors de l’application de la puissance ou de la lecture de la configuration de l’appareil. Cela peut être dû à une défaillance de votre matériel ou à une mauvaise connexion.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**POINT de montage d’erreur \_ \_ \_ non \_ résolu**
</dt> <dd> <dl> <dt>

649 (0x289)
</dt> <dt>



L’opération de création a échoué, car le nom contenait au moins un point de montage qui correspond à un volume auquel l’objet périphérique spécifié n’est pas attaché.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERREUR \_ de \_ \_ paramètre d’objet appareil non valide \_**
</dt> <dd> <dl> <dt>

650 (0x28A)
</dt> <dt>



Le paramètre d’objet d’appareil n’est pas un objet d’appareil valide ou n’est pas attaché au volume spécifié par le nom de fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**une erreur MCA s’est \_ \_ produite**
</dt> <dd> <dl> <dt>

651 (0x28B)
</dt> <dt>



Une erreur de vérification de l’ordinateur s’est produite. Pour plus d’informations, consultez le journal des événements système.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**erreur \_ \_ de base de données du pilote d’erreur \_**
</dt> <dd> <dl> <dt>

652 (0x28C)
</dt> <dt>



Une erreur %2 s’est produite pendant \[ \] le traitement de la base de données du pilote.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ruche du système d’erreur \_ \_ \_ trop \_ grande**
</dt> <dd> <dl> <dt>

653 (0x28D)
</dt> <dt>



La taille de la ruche système a dépassé sa limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**\_échec du \_ \_ \_ déchargement préalable du pilote d’erreur**
</dt> <dd> <dl> <dt>

654 (0x28E)
</dt> <dt>



Le pilote n’a pas pu être chargé car une version précédente du pilote est toujours en mémoire.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERREUR \_ VOLSNAP \_ préparer la \_ mise en veille prolongée**
</dt> <dd> <dl> <dt>

655 (0x28F)
</dt> <dt>



{Service VSS} Veuillez patienter pendant que le Service VSS prépare le volume% HS pour la mise en veille prolongée.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERREUR de \_ mise en veille prolongée \_**
</dt> <dd> <dl> <dt>

656 (0x290)
</dt> <dt>



Le système n’a pas pu se mettre en veille prolongée (le code d’erreur est% HS). La mise en veille prolongée est désactivée jusqu’au redémarrage du système.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERREUR \_ Pwd \_ trop \_ longue**
</dt> <dd> <dl> <dt>

657 (0x291)
</dt> <dt>



Le mot de passe fourni est trop long pour respecter la stratégie de votre compte d’utilisateur. Veuillez choisir un mot de passe plus petit.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_limitation du \_ système de fichiers d’erreur \_**
</dt> <dd> <dl> <dt>

665 (0x299)
</dt> <dt>



Impossible de terminer l’opération demandée du fait d’une limitation du système de fichiers.


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**\_échec d’assertion d’erreur \_**
</dt> <dd> <dl> <dt>

668 (0x29C)
</dt> <dt>



Un échec d’assertion s’est produit.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**erreur \_ ACPI \_ erreur**
</dt> <dd> <dl> <dt>

669 (0x29D)
</dt> <dt>



Une erreur s’est produite dans le sous-système ACPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERREUR \_ d' \_ assertion WOW**
</dt> <dd> <dl> <dt>

670 (0x29E)
</dt> <dt>



Erreur d’assertion WOW.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERREUR \_ PNP \_ \_ table MPS incorrecte \_**
</dt> <dd> <dl> <dt>

671 (0x29F)
</dt> <dt>



Il manque un appareil dans la table MPS du BIOS système. Ce périphérique ne sera pas utilisé. Contactez le fournisseur de votre système pour obtenir la mise à jour du BIOS système.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERREUR \_ échec de la \_ traduction PNP \_**
</dt> <dd> <dl> <dt>

672 (0x2A0)
</dt> <dt>



Un traducteur n’a pas réussi à traduire les ressources.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERREUR \_ échec de la \_ traduction IRQ PNP \_ \_**
</dt> <dd> <dl> <dt>

673 (0x2A1)
</dt> <dt>



Un traducteur d’IRQ n’a pas pu traduire les ressources.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERREUR \_ PNP \_ ID non valide \_**
</dt> <dd> <dl> <dt>

674 (0x2A2)
</dt> <dt>



Le pilote %2 a retourné un ID non valide pour un appareil enfant (%3).


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERREUR de \_ sortie du \_ \_ débogueur système**
</dt> <dd> <dl> <dt>

675 (0x2A3)
</dt> <dt>



{Le débogueur du noyau est réveillé} le débogueur système a été réveillé par une interruption.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_Handles d’erreur \_ fermés**
</dt> <dd> <dl> <dt>

676 (0x2A4)
</dt> <dt>



{Handles fermés} Les handles des objets ont été fermés automatiquement à la suite de l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERREUR \_ informations superflues \_**
</dt> <dd> <dl> <dt>

677 (0x2A5)
</dt> <dt>



{Trop d’informations} La liste de contrôle d’accès (ACL) spécifiée contient plus d’informations que prévu.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERREUR \_ RXACT \_ validation \_ nécessaire**
</dt> <dd> <dl> <dt>

678 (0x2A6)
</dt> <dt>



Cet état de niveau d’avertissement indique que l’état de transaction existe déjà pour la sous-arborescence du Registre, mais qu’une validation de transaction a été abandonnée précédemment. La validation n’a pas été effectuée, mais elle n’a pas été annulée (par conséquent, elle peut toujours être validée si vous le souhaitez).


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_vérification du support d’erreur \_**
</dt> <dd> <dl> <dt>

679 (0x2A7)
</dt> <dt>



{Media Changed} Le support a peut-être changé.


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**substitution du GUID d’erreur \_ \_ \_ effectuée**
</dt> <dd> <dl> <dt>

680 (0x2A8)
</dt> <dt>



{Substitution de GUID} Lors de la traduction d’un identificateur global (GUID) vers un ID de sécurité Windows (SID), aucun préfixe GUID défini administrativement n’a été trouvé. Un préfixe de remplacement a été utilisé, ce qui ne compromettra pas la sécurité du système. Toutefois, cela peut fournir un accès plus restrictif que prévu.


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERREUR \_ arrêtée \_ sur le \_ lien symbolique**
</dt> <dd> <dl> <dt>

681 (0x2A9)
</dt> <dt>



L’opération de création s’est arrêtée après avoir atteint un lien symbolique.


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERREUR \_ LONGJUMP**
</dt> <dd> <dl> <dt>

682 (0x2AA)
</dt> <dt>



Un saut long a été exécuté.


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERREUR \_ de \_ requête PLUGPLAY \_ refusée**
</dt> <dd> <dl> <dt>

683 (0x2AB)
</dt> <dt>



L’opération de requête de Plug-and-Play a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERREUR lors du déroulement de la \_ \_ consolidation**
</dt> <dd> <dl> <dt>

684 (0x2AC)
</dt> <dt>



Une consolidation de frame a été exécutée.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERREUR de récupération de la \_ ruche du Registre \_ \_**
</dt> <dd> <dl> <dt>

685 (0x2AD)
</dt> <dt>



{Ruche du Registre Récupérée} La ruche du Registre (fichier) :% HS a été endommagée et a été récupérée. Certaines données ont peut-être été perdues.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**la \_ dll d’erreur \_ est peut- \_ être \_ non sécurisée**
</dt> <dd> <dl> <dt>

686 (0x2AE)
</dt> <dt>



L’application tente d’exécuter du code exécutable à partir du module% HS. Cela peut être non sécurisé. Une alternative,% HS, est disponible. L’application doit-elle utiliser le module sécurisé% HS ?


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**la \_ dll d’erreur \_ est peut- \_ être \_ incompatible**
</dt> <dd> <dl> <dt>

687 (0x2AF)
</dt> <dt>



L’application charge le code exécutable à partir du module% HS. Cela est sécurisé, mais peut être incompatible avec les versions précédentes du système d’exploitation. Une alternative,% HS, est disponible. L’application doit-elle utiliser le module sécurisé% HS ?


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERREUR de l' \_ \_ exception dbg \_ non \_ gérée**
</dt> <dd> <dl> <dt>

688 (0x2B0)
</dt> <dt>



Le débogueur n’a pas géré l’exception.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERREUR \_ dbg \_ répondre \_ plus tard**
</dt> <dd> <dl> <dt>

689 (0x2B1)
</dt> <dt>



Le débogueur répondra plus tard.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERREUR \_ dbg \_ Impossible \_ de \_ fournir le \_ descripteur**
</dt> <dd> <dl> <dt>

690 (0x2B2)
</dt> <dt>



Le débogueur ne peut pas fournir de handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERREUR \_ dbg de \_ fin de \_ thread**
</dt> <dd> <dl> <dt>

691 (0x2B3)
</dt> <dt>



Thread du débogueur terminé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERREUR \_ du \_ processus de fin de dbg \_**
</dt> <dd> <dl> <dt>

692 (0x2B4)
</dt> <dt>



Le débogueur a terminé le processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERREUR \_ dbg dans \_ le contrôle \_ C**
</dt> <dd> <dl> <dt>

693 (0x2B5)
</dt> <dt>



Le débogueur a obtenu le contrôle C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERREUR \_ dbg \_ PRINTEXCEPTION \_ C**
</dt> <dd> <dl> <dt>

694 (0x2B6)
</dt> <dt>



Exception imprimée du débogueur sur le contrôle C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERREUR \_ dbg \_ RIPEXCEPTION**
</dt> <dd> <dl> <dt>

695 (0x2B7)
</dt> <dt>



Le débogueur a reçu une exception RIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERREUR \_ de \_ saut de contrôle dbg \_**
</dt> <dd> <dl> <dt>

696 (0x2B8)
</dt> <dt>



Le débogueur a reçu un arrêt de contrôle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERREUR \_ de \_ commande \_ dbg**
</dt> <dd> <dl> <dt>

697 (0x2B9)
</dt> <dt>



Exception de communication de commande du débogueur.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**le nom de l’objet d’erreur \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

698 (0x2BA)
</dt> <dt>



{Object Exists} Une tentative de création d’un objet a été effectuée et le nom de l’objet existait déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**le \_ thread d’erreur \_ a été \_ suspendu**
</dt> <dd> <dl> <dt>

699 (0x2BB)
</dt> <dt>



{Thread suspendu} Une interruption de thread s’est produite pendant l’interruption du thread. Le thread a été repris et l’arrêt s’est poursuivi.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**IMAGE d’erreur \_ \_ non \_ au niveau de la \_ base**
</dt> <dd> <dl> <dt>

700 (0x2BC)
</dt> <dt>



{Image relocalisée} Un fichier image n’a pas pu être mappé à l’adresse spécifiée dans le fichier image. Les corrections locales doivent être effectuées sur cette image.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERREUR \_ d' \_ État RXACT \_ créé**
</dt> <dd> <dl> <dt>

701 (0x2BD)
</dt> <dt>



Cet état de niveau d’information indique qu’un état de transaction de sous-arborescence de Registre spécifié n’existait pas encore et devait être créé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notification de segment d’erreur \_**
</dt> <dd> <dl> <dt>

702 (0x2BE)
</dt> <dt>



{Chargement de segment} Une machine virtuelle DOS (VDM) charge, décharge ou déplace une image de segment de programme MS-DOS ou Win16. Une exception est déclenchée pour qu’un débogueur puisse charger, décharger ou suivre des symboles et des points d’arrêt dans ces segments 16 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERREUR \_ de \_ répertoire actif incorrect \_**
</dt> <dd> <dl> <dt>

703 (0x2BF)
</dt> <dt>



{Répertoire actif non valide} Le processus ne peut pas basculer vers le répertoire de démarrage% HS. Sélectionnez OK pour définir le répertoire actif à% HS, ou cliquez sur Annuler pour quitter.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERREUR \_ ft \_ \_ de lecture de la récupération \_ à partir d’une \_ sauvegarde**
</dt> <dd> <dl> <dt>

704 (0x2C0)
</dt> <dt>



{Lecture redondante} Pour répondre à une demande de lecture, le système de fichiers à tolérance de panne NT lit correctement les données demandées à partir d’une copie redondante. Cela est dû au fait que le système de fichiers a rencontré une défaillance sur un membre du volume à tolérance de panne, mais qu’il n’a pas pu réaffecter la zone défaillante de l’appareil.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERREUR \_ de \_ récupération en écriture ft \_**
</dt> <dd> <dl> <dt>

705 (0x2C1)
</dt> <dt>



{Écriture redondante} Pour répondre à une demande d’écriture, le système de fichiers à tolérance de panne NT a écrit avec succès une copie redondante des informations. Cela est dû au fait que le système de fichiers a rencontré une défaillance sur un membre du volume à tolérance de panne, mais qu’il n’a pas été en mesure de réassigner la zone défaillante de l’appareil.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de type d’ordinateur d’image \_**
</dt> <dd> <dl> <dt>

706 (0x2C2)
</dt> <dt>



{Incompatibilité de type d’ordinateur} Le fichier image% HS est valide, mais il est destiné à un type d’ordinateur autre que l’ordinateur actuel. Sélectionnez OK pour continuer ou annuler pour faire échouer le chargement de la DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERREUR de \_ réception \_ partielle**
</dt> <dd> <dl> <dt>

707 (0x2C3)
</dt> <dt>



{Données partielles reçues} Le transport réseau a renvoyé des données partielles à son client. Les données restantes seront envoyées ultérieurement.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**réception d’erreur \_ envoyée \_**
</dt> <dd> <dl> <dt>

708 (0x2C4)
</dt> <dt>



{Données expédiées reçues} Le transport réseau a renvoyé à son client des données qui ont été marquées comme expédiées par le système distant.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERREUR de \_ réception \_ partielle \_ expédiée**
</dt> <dd> <dl> <dt>

709 (0x2C5)
</dt> <dt>



{Données expédiées partielles reçues} Le transport réseau a renvoyé des données partielles à son client et ces données ont été marquées comme expédiées par le système distant. Les données restantes seront envoyées ultérieurement.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**événement d’erreur \_ \_ effectué**
</dt> <dd> <dl> <dt>

710 (0x2C6)
</dt> <dt>



{Événement TDI effectué} L’indication TDI s’est terminée avec succès.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**événement d’erreur \_ \_ en attente**
</dt> <dd> <dl> <dt>

711 (0x2C7)
</dt> <dt>



{Événement TDI en attente} L’indication TDI est passée à l’État en attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERREUR lors de la \_ vérification du \_ système de fichiers \_**
</dt> <dd> <dl> <dt>

712 (0x2C8)
</dt> <dt>



Vérification du système de fichiers sur% wZ.


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERREUR de sortie de l' \_ \_ application irrécupérable \_**
</dt> <dd> <dl> <dt>

713 (0x2C9)
</dt> <dt>



{Sortie d’application irrécupérable}% hs.


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_handle prédéfini d’erreur \_**
</dt> <dd> <dl> <dt>

714 (0x2CA)
</dt> <dt>



La clé de Registre spécifiée est référencée par un handle prédéfini.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**l’erreur \_ a été \_ déverrouillée**
</dt> <dd> <dl> <dt>

715 (0x2CB)
</dt> <dt>



{Page déverrouillé} La protection de page d’une page verrouillée a été remplacée par « aucun accès » et la page a été déverrouillée de la mémoire et du processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notification de service d’erreur \_**
</dt> <dd> <dl> <dt>

716 (0x2CC)
</dt> <dt>



% HS


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**l’erreur \_ a été \_ verrouillée**
</dt> <dd> <dl> <dt>

717 (0x2CD)
</dt> <dt>



{Page verrouillée} L’une des pages à verrouiller a déjà été verrouillée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**erreur \_ matérielle du journal des erreurs \_ \_**
</dt> <dd> <dl> <dt>

718 (0x2CE)
</dt> <dt>



Fenêtre contextuelle de l’application : %1 : %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERREUR \_ déjà \_ Win32**
</dt> <dd> <dl> <dt>

719 (0x2CF)
</dt> <dt>



ERREUR \_ déjà \_ Win32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERREUR \_ d' \_ incompatibilité de type d’ordinateur d’image \_ \_ \_ exe**
</dt> <dd> <dl> <dt>

720 (0x2D0)
</dt> <dt>



{Incompatibilité de type d’ordinateur} Le fichier image% HS est valide, mais il est destiné à un type d’ordinateur autre que l’ordinateur actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERREUR \_ aucun \_ rendement \_ effectué**
</dt> <dd> <dl> <dt>

721 (0x2D1)
</dt> <dt>



Une exécution de rendement a été effectuée et aucun thread n’était disponible pour l’exécution.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**\_reprise du minuteur d’erreur \_ \_ ignorée**
</dt> <dd> <dl> <dt>

722 (0x2D2)
</dt> <dt>



L’indicateur pouvant être repris sur une API de minuteur a été ignoré.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**arbitrage d’erreur \_ \_ non géré**
</dt> <dd> <dl> <dt>

723 (0x2D3)
</dt> <dt>



L’arbitre a différé l’arbitrage de ces ressources à son parent.


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERREUR \_ CardBus \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

724 (0x2D4)
</dt> <dt>



Impossible de démarrer l’appareil CardBus inséré en raison d’une erreur de configuration sur « % HS ».


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de processeur MP \_**
</dt> <dd> <dl> <dt>

725 (0x2D5)
</dt> <dt>



Les processeurs de ce système multiprocesseur ne sont pas tous du même niveau de révision. Pour utiliser tous les processeurs, le système d’exploitation se limite aux fonctionnalités du processeur le moins performant du système. Si des problèmes se produisent avec ce système, contactez le fabricant du processeur pour déterminer si cette combinaison de processeurs est prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERREUR de \_ mise en veille prolongée**
</dt> <dd> <dl> <dt>

726 (0x2D6)
</dt> <dt>



Le système a été mis en veille prolongée.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERREUR de reprise de la \_ \_ mise en veille prolongée**
</dt> <dd> <dl> <dt>

727 (0x2D7)
</dt> <dt>



Le système a repris de la mise en veille prolongée.


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**microprogramme d’erreur \_ \_ mis à jour**
</dt> <dd> <dl> <dt>

728 (0x2D8)
</dt> <dt>



Windows a détecté que le microprogramme système (BIOS) a été mis à jour la \[ date du microprogramme précédent = %2, date du microprogramme actuel %3 \] .


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**pilotes d’erreur avec \_ \_ fuite de \_ pages verrouillées \_**
</dt> <dd> <dl> <dt>

729 (0x2D9)
</dt> <dt>



Un pilote de périphérique perd des pages d’e/s verrouillées, provoquant une dégradation du système. Le système a automatiquement activé le code de suivi afin d’essayer d’intercepter le coupable.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERREUR de \_ réveil du \_ système**
</dt> <dd> <dl> <dt>

730 (0x2DA)
</dt> <dt>



Le système a activé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERREUR d' \_ attente \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2DB)
</dt> <dt>



ERREUR d' \_ attente \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERREUR d' \_ attente \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2DC)
</dt> <dt>



ERREUR d' \_ attente \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERREUR d' \_ attente \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2DD)
</dt> <dt>



ERREUR d' \_ attente \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERREUR d' \_ attente \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2DE)
</dt> <dt>



ERREUR d' \_ attente \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERREUR \_ d' \_ attente abandonnée \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2DF)
</dt> <dt>



ERREUR \_ d' \_ attente abandonnée \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERREUR \_ d' \_ attente abandonnée \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2E0)
</dt> <dt>



ERREUR \_ d' \_ attente abandonnée \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERREUR de l' \_ utilisateur \_ APC**
</dt> <dd> <dl> <dt>

737 (0x2E1)
</dt> <dt>



ERREUR de l' \_ utilisateur \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERREUR de \_ noyau \_ APC**
</dt> <dd> <dl> <dt>

738 (0x2E2)
</dt> <dt>



ERREUR de \_ noyau \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERREUR \_ signalée**
</dt> <dd> <dl> <dt>

739 (0x2E3)
</dt> <dt>



ERREUR \_ signalée


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**élévation d’erreur \_ \_ requise**
</dt> <dd> <dl> <dt>

740 (0x2E4)
</dt> <dt>



L’opération demandée requiert une élévation.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERREUR d' \_ analyse**
</dt> <dd> <dl> <dt>

741 (0x2E5)
</dt> <dt>



Une analyse doit être effectuée par le gestionnaire d’objets, car le nom du fichier a entraîné un lien symbolique.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERREUR \_ \_ de rupture \_ de verrou OPLOCK en \_ cours**
</dt> <dd> <dl> <dt>

742 (0x2E6)
</dt> <dt>



Une opération d’ouverture/de création est terminée alors qu’une interruption oplock est en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**VOLUME d’erreurs \_ \_ monté**
</dt> <dd> <dl> <dt>

743 (0x2E7)
</dt> <dt>



Un nouveau volume a été monté par un système de fichiers.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERREUR \_ RXACT \_ validée**
</dt> <dd> <dl> <dt>

744 (0x2E8)
</dt> <dt>



Cet état du niveau de réussite indique que l’état de la transaction existe déjà pour la sous-arborescence du Registre, mais qu’une validation de transaction a été abandonnée précédemment. La validation est maintenant terminée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERREUR de \_ notification de \_ nettoyage**
</dt> <dd> <dl> <dt>

745 (0x2E9)
</dt> <dt>



Cela indique qu’une demande de notification de modification a été effectuée en raison de la fermeture du handle qui a effectué la demande de notification de modification.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERREUR \_ échec de la connexion au \_ transport principal \_ \_**
</dt> <dd> <dl> <dt>

746 (0x2EA)
</dt> <dt>



{Échec de la connexion sur le transport principal} Une tentative de connexion au serveur distant% HS sur le transport principal a été effectuée, mais la connexion a échoué. L’ordinateur a pu se connecter à un transport secondaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transition de \_ défaillance de page d’erreur \_**
</dt> <dd> <dl> <dt>

747 (0x2EB)
</dt> <dt>



L’erreur de page était une erreur de transition.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**Page d’erreur de \_ \_ \_ la demande de défaillance \_ zéro**
</dt> <dd> <dl> <dt>

748 (0x2EC)
</dt> <dt>



L’erreur de page était une erreur nulle à la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**\_ \_ \_ copie d’erreur \_ de page d’erreur lors de l' \_ écriture**
</dt> <dd> <dl> <dt>

749 (0x2ED)
</dt> <dt>



L’erreur de page était une erreur nulle à la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**Page d’erreur page de garde des erreurs \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

750 (0x2EE)
</dt> <dt>



L’erreur de page était une erreur nulle à la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_fichier de \_ \_ pagination \_ des erreurs de page d’erreur**
</dt> <dd> <dl> <dt>

751 (0x2EF)
</dt> <dt>



L’erreur de page a été satisfaite par la lecture à partir d’un périphérique de stockage secondaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**PAGE de cache des erreurs \_ \_ \_ verrouillée**
</dt> <dd> <dl> <dt>

752 (0x2F0)
</dt> <dt>



La page mise en cache a été verrouillée pendant l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERREUR \_ de \_ vidage sur incident**
</dt> <dd> <dl> <dt>

753 (0x2F1)
</dt> <dt>



Le vidage sur incident existe dans le fichier d’échange.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**tampon d’erreur- \_ \_ tous les \_ zéros**
</dt> <dd> <dl> <dt>

754 (0x2F2)
</dt> <dt>



La mémoire tampon spécifiée ne contient que des zéros.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERREUR d’analyse de l' \_ \_ objet**
</dt> <dd> <dl> <dt>

755 (0x2F3)
</dt> <dt>



Une analyse doit être effectuée par le gestionnaire d’objets, car le nom du fichier a entraîné un lien symbolique.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**Erreurs de ressources d’erreur \_ \_ \_ modifiées**
</dt> <dd> <dl> <dt>

756 (0x2F4)
</dt> <dt>



L’appareil a réussi une requête-stop et ses besoins en ressources ont changé.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**traduction d’erreur \_ \_ terminée**
</dt> <dd> <dl> <dt>

757 (0x2F5)
</dt> <dt>



Le traducteur a traduit ces ressources dans l’espace global et aucune autre traduction ne doit être effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_aucune erreur \_ à \_ terminer**
</dt> <dd> <dl> <dt>

758 (0x2F6)
</dt> <dt>



Un processus en cours d’arrêt n’a aucun thread à arrêter.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**le \_ processus \_ d’erreur n’est pas \_ dans le \_ travail**
</dt> <dd> <dl> <dt>

759 (0x2F7)
</dt> <dt>



Le processus spécifié ne fait pas partie d’un travail.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_traitement \_ des erreurs dans le \_ travail**
</dt> <dd> <dl> <dt>

760 (0x2F8)
</dt> <dt>



Le processus spécifié fait partie d’un travail.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERREUR \_ VOLSNAP \_ prêt pour la mise en veille prolongée \_**
</dt> <dd> <dl> <dt>

761 (0x2F9)
</dt> <dt>



{Service VSS} Le système est maintenant prêt pour la mise en veille prolongée.


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERREUR \_ FSFILTER \_ op \_ s’est terminée \_ avec succès**
</dt> <dd> <dl> <dt>

762 (0x2FA)
</dt> <dt>



Un système de fichiers ou un pilote de filtre de système de fichiers a réussi une opération FsFilter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**vecteur d’interruption d’erreur \_ \_ \_ déjà \_ connecté**
</dt> <dd> <dl> <dt>

763 (0x2FB)
</dt> <dt>



Le vecteur d’interruption spécifié était déjà connecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**interruption d’erreur \_ \_ toujours \_ connectée**
</dt> <dd> <dl> <dt>

764 (0x2FC)
</dt> <dt>



Le vecteur d’interruption spécifié est toujours connecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**\_attente \_ d’erreur pour \_ OPLOCK**
</dt> <dd> <dl> <dt>

765 (0x2FD)
</dt> <dt>



Une opération est bloquée en attente d’un oplock.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERREUR de gestion de l' \_ \_ exception dbg \_**
</dt> <dd> <dl> <dt>

766 (0x2FE)
</dt> <dt>



Exception gérée par le débogueur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERREUR \_ dbg \_ continue**
</dt> <dd> <dl> <dt>

767 (0x2FF)
</dt> <dt>



Le débogueur a continué.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_ \_ pile contextuelle de rappel d’erreur \_**
</dt> <dd> <dl> <dt>

768 (0x300)
</dt> <dt>



Une exception s’est produite dans un rappel en mode utilisateur et la trame de rappel du noyau doit être supprimée.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**COMPRESSION des erreurs \_ \_ désactivée**
</dt> <dd> <dl> <dt>

769 (0x301)
</dt> <dt>



La compression est désactivée pour ce volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERREUR \_ CANTFETCHBACKWARDS**
</dt> <dd> <dl> <dt>

770 (0x302)
</dt> <dt>



Le fournisseur de données ne peut pas extraire vers l’arrière à travers un jeu de résultats.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERREUR \_ CANTSCROLLBACKWARDS**
</dt> <dd> <dl> <dt>

771 (0x303)
</dt> <dt>



Le fournisseur de données ne peut pas faire défiler vers l’arrière d’un jeu de résultats.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERREUR \_ ROWSNOTRELEASED**
</dt> <dd> <dl> <dt>

772 (0x304)
</dt> <dt>



Le fournisseur de données exige que les données précédemment extraites soient libérées avant de demander des données supplémentaires.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**\_indicateurs d' \_ accesseur d’erreur incorrects \_**
</dt> <dd> <dl> <dt>

773 (0x305)
</dt> <dt>



Le fournisseur de données n’a pas pu interpréter les indicateurs définis pour une liaison de colonne dans un accesseur.


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_Erreurs \_ rencontrées**
</dt> <dd> <dl> <dt>

774 (0x306)
</dt> <dt>



Une ou plusieurs erreurs se sont produites lors du traitement de la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERREUR \_ non \_ possible**
</dt> <dd> <dl> <dt>

775 (0x307)
</dt> <dt>



L’implémentation ne peut pas effectuer la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_demande \_ d’erreur \_ hors \_ séquence**
</dt> <dd> <dl> <dt>

776 (0x308)
</dt> <dt>



Le client d’un composant a demandé une opération qui n’est pas valide compte tenu de l’état de l’instance du composant.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**erreur d’analyse de la version d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

777 (0x309)
</dt> <dt>



Impossible d’analyser un numéro de version.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERREUR \_ BADSTARTPOSITION**
</dt> <dd> <dl> <dt>

778 (0x30A)
</dt> <dt>



La position de début de l’itérateur n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERREUR de \_ mémoire \_ matérielle**
</dt> <dd> <dl> <dt>

779 (0x30B)
</dt> <dt>



Le matériel a signalé une erreur de mémoire incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERREUR \_ de \_ réparation de disque \_ désactivée**
</dt> <dd> <dl> <dt>

780 (0x30C)
</dt> <dt>



L’opération tentée a nécessité l’activation de la réparation spontanée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERREUR \_ de ressource insuffisante \_ \_ pour la \_ \_ taille de section partagée spécifiée \_ \_**
</dt> <dd> <dl> <dt>

781 (0x30D)
</dt> <dt>



Le tas du Bureau a rencontré une erreur lors de l’allocation de la mémoire de la session. Le journal des événements système contient des informations supplémentaires.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**erreur \_ de \_ transition de POWERSTATE du système d’erreur \_**
</dt> <dd> <dl> <dt>

782 (0x30E)
</dt> <dt>



L’état d’alimentation du système passe de %2 à %3.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**erreur \_ de \_ \_ transition complexe \_ POWERSTATE du système d’erreur**
</dt> <dd> <dl> <dt>

783 (0x30F)
</dt> <dt>



L’état d’alimentation du système passe de %2 à %3, mais peut entrer %4.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERREUR \_ MCA \_ exception**
</dt> <dd> <dl> <dt>

784 (0x310)
</dt> <dt>



Un thread est distribué avec une EXCEPTION MCA en raison de MCA.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**\_audit d’accès aux erreurs \_ \_ par \_ stratégie**
</dt> <dd> <dl> <dt>

785 (0x311)
</dt> <dt>



L’accès à %1 est analysé par la règle de stratégie %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**\_accès aux erreurs \_ désactivé \_ non \_ protégé \_ par \_ la \_ stratégie**
</dt> <dd> <dl> <dt>

786 (0x312)
</dt> <dt>



L’accès à %1 a été restreint par votre administrateur par la règle de stratégie %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERREUR lors de l' \_ abandon de \_ HIBERFILE**
</dt> <dd> <dl> <dt>

787 (0x313)
</dt> <dt>



Un fichier de mise en veille prolongée valide a été invalidé et doit être abandonné.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERREUR de \_ perte du \_ réseau de données WRITEBEHIND \_ \_ \_ déconnecté**
</dt> <dd> <dl> <dt>

788 (0x314)
</dt> <dt>



{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS ; les données ont été perdues. Cette erreur peut être due à des problèmes de connectivité réseau. Essayez d’enregistrer ce fichier ailleurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERREUR lors de la perte du serveur de \_ \_ \_ données WRITEBEHIND \_ \_ \_**
</dt> <dd> <dl> <dt>

789 (0x315)
</dt> <dt>



{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS ; les données ont été perdues. Cette erreur a été retournée par le serveur sur lequel se trouve le fichier. Essayez d’enregistrer ce fichier ailleurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERREUR lors de la \_ perte du \_ \_ \_ disque local de données WRITEBEHIND \_ \_**
</dt> <dd> <dl> <dt>

790 (0x316)
</dt> <dt>



{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS ; les données ont été perdues. Cette erreur peut se produire si l’appareil a été supprimé ou si le média est protégé en écriture.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERREUR \_ de \_ table MCFG incorrecte \_**
</dt> <dd> <dl> <dt>

791 (0x317)
</dt> <dt>



Les ressources requises pour cet appareil sont en conflit avec la table MCFG.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERREUR \_ de \_ réparation de disque \_ redirigée**
</dt> <dd> <dl> <dt>

792 (0x318)
</dt> <dt>



La réparation du volume n’a pas pu être effectuée tant qu’il est en ligne. Planifiez la mise hors connexion du volume afin qu’il puisse être réparé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ÉCHEC de la \_ réparation du disque erreur \_ \_**
</dt> <dd> <dl> <dt>

793 (0x319)
</dt> <dt>



La réparation du volume a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERREUR \_ de \_ saturation du journal \_**
</dt> <dd> <dl> <dt>

794 (0x31A)
</dt> <dt>



L’un des journaux d’altération du volume est plein. Les dommages qui peuvent être détectés ne seront pas consignés.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERREUR \_ de \_ journal \_ endommagé endommagé**
</dt> <dd> <dl> <dt>

795 (0x31B)
</dt> <dt>



L’un des journaux d’altération du volume est endommagé en interne et doit être recréé. Le volume peut contenir des altérations non détectées et doit être analysé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERREUR \_ de \_ journal endommagé \_ non disponible**
</dt> <dd> <dl> <dt>

796 (0x31C)
</dt> <dt>



L’un des journaux d’altération de volume n’est pas disponible pour être utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERREUR \_ \_ fichier journal endommagé \_ supprimé \_**
</dt> <dd> <dl> <dt>

797 (0x31D)
</dt> <dt>



L’un des journaux d’altération du volume a été supprimé tout en conservant des enregistrements d’altération. Le volume contient des altérations détectées et doit être analysé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERREUR \_ de \_ journal \_ endommagé**
</dt> <dd> <dl> <dt>

798 (0x31E)
</dt> <dt>



L’un des journaux d’altération du volume a été effacé par CHKDSK et ne contient plus de dommages réels.


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERREUR \_ \_ nom orphelin \_ épuisé**
</dt> <dd> <dl> <dt>

799 (0x31F)
</dt> <dt>



Des fichiers orphelins existent sur le volume mais n’ont pas pu être récupérés car aucun nouveau nom n’a pu être créé dans le répertoire de récupération. Les fichiers doivent être déplacés à partir du répertoire de récupération.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERREUR \_ OPLOCK \_ basculée \_ vers le \_ nouveau \_ handle**
</dt> <dd> <dl> <dt>

800 (0x320)
</dt> <dt>



Le oplock associé à ce descripteur est maintenant associé à un autre handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**l’erreur \_ ne peut pas \_ accorder le \_ \_ OPLOCK demandé**
</dt> <dd> <dl> <dt>

801 (0x321)
</dt> <dt>



Un oplock du niveau demandé ne peut pas être accordé. Un oplock d’un niveau inférieur peut être disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERREUR \_ Impossible d' \_ interrompre \_ OPLOCK**
</dt> <dd> <dl> <dt>

802 (0x322)
</dt> <dt>



L’opération n’a pas abouti, car cela entraînerait la rupture d’un oplock. L’appelant a demandé que les verrous oplock existants ne soient pas rompus.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**descripteur OPLOCK de l’erreur \_ \_ \_ fermé**
</dt> <dd> <dl> <dt>

803 (0x323)
</dt> <dt>



Le handle avec lequel ce oplock est associé a été fermé. Le verrou oplock est maintenant rompu.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERREUR \_ aucune \_ \_ condition ACE**
</dt> <dd> <dl> <dt>

804 (0x324)
</dt> <dt>



L’entrée de contrôle d’accès (ACE) spécifiée ne contient pas de condition.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERREUR \_ de \_ condition ACE non valide \_**
</dt> <dd> <dl> <dt>

805 (0x325)
</dt> <dt>



L’entrée de contrôle d’accès (ACE) spécifiée contient une condition non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**HANDLE de fichier d’erreur \_ \_ \_ révoqué**
</dt> <dd> <dl> <dt>

806 (0x326)
</dt> <dt>



L’accès au descripteur de fichier spécifié a été révoqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**IMAGE d’erreur \_ \_ à une \_ \_ base différente**
</dt> <dd> <dl> <dt>

807 (0x327)
</dt> <dt>



Un fichier image a été mappé à une adresse différente de celle spécifiée dans le fichier image, mais les corrections sont toujours effectuées automatiquement sur l’image.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERREUR \_ EA \_ accès \_ refusé**
</dt> <dd> <dl> <dt>

994 (0x3E2)
</dt> <dt>



L’accès à l’attribut étendu a été refusé.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERREUR de l' \_ opération \_ abandonnée**
</dt> <dd> <dl> <dt>

995 (0x3E3)
</dt> <dt>



L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERREUR d' \_ e/s \_ incomplète**
</dt> <dd> <dl> <dt>

996 (0x3E4)
</dt> <dt>



L’événement d’e/s avec chevauchement n’est pas dans un état signalé.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERREUR d' \_ e/s \_ en attente**
</dt> <dd> <dl> <dt>

997 (0x3E5)
</dt> <dt>



L’opération d’e/s avec chevauchement est en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERREUR \_ NOaccess**
</dt> <dd> <dl> <dt>

998 (0x3E6)
</dt> <dt>



Accès non valide à l’emplacement de la mémoire.


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERREUR \_ SWAPERROR**
</dt> <dd> <dl> <dt>

999 (0x3E7)
</dt> <dt>



Erreur lors de l’exécution de l’opération InPage.


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

 

 
