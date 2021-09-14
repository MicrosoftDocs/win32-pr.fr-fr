---
description: Décrit les codes d’erreur 1300-1699 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Codes d’erreur système (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114550"
---
# <a name="system-error-codes-1300-1699"></a>Codes d’erreur système (1300-1699)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 1300 à 1699. Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERREUR \_ non \_ \_ assignée**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



Tous les privilèges ou groupes référencés ne sont pas assignés à l’appelant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERREUR \_ \_ non \_ mappée**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



Un mappage entre les noms de compte et les ID de sécurité n’a pas été effectué.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERREUR \_ aucun \_ quota \_ pour le \_ compte**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



Aucune limite de quota système n’est définie spécifiquement pour ce compte.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERREUR \_ de \_ \_ clé de session d’utilisateur local \_**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



Aucune clé de chiffrement n’est disponible. Une clé de chiffrement connue a été retournée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERREUR \_ \_ \_ de mot de passe LM null**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



Le mot de passe est trop complexe pour être converti en mot de passe LAN Manager. Le mot de passe du gestionnaire LAN Manager retourné est une chaîne **null** .


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERREUR \_ de \_ révision inconnue**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



Le niveau de révision est inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**incompatibilité de révision d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Indique que deux niveaux de révision sont incompatibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERREUR \_ propriétaire non valide \_**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



Cet ID de sécurité ne peut pas être assigné en tant que propriétaire de cet objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERREUR \_ de \_ groupe principal non valide \_**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Cet ID de sécurité ne peut pas être affecté en tant que groupe principal d’un objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERREUR \_ aucun \_ jeton d’emprunt d’identité \_**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



Une tentative a été effectuée pour fonctionner sur un jeton d’emprunt d’identité par un thread qui n’emprunte pas actuellement l’identité d’un client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERREUR \_ Impossible de \_ désactiver le \_ obligatoire**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



Le groupe n’est peut-être pas désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERREUR \_ aucun \_ serveur d’ouverture de session \_**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



Aucun serveur d’ouverture de session n’est actuellement disponible pour traiter la demande d’ouverture de session.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERREUR \_ aucune \_ \_ ouverture de session de ce type \_**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



Une session ouverte spécifiée n’existe pas. Elle a peut-être déjà été arrêtée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERREUR \_ non liée à \_ ce type de \_ privilège**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



Un privilège spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**privilège d’erreur \_ \_ non \_ détenu**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



Le client ne dispose pas d'un privilège qui est obligatoire.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERREUR \_ \_ nom de compte non valide \_**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



Le nom fourni n’est pas un nom de compte correctement formé.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**l’utilisateur de l’erreur \_ \_ existe**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



Le compte spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERREUR \_ non de \_ ce type d' \_ utilisateur**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



Le compte spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**le \_ groupe d’erreurs \_ existe**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



Le groupe spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERREUR \_ non liée à \_ ce \_ groupe**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



Le groupe spécifié n'existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_membre \_ d’erreur dans le \_ groupe**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



Soit le compte d’utilisateur spécifié est déjà membre du groupe spécifié, soit le groupe spécifié ne peut pas être supprimé parce qu’il contient un membre.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**\_membre \_ d’erreur non dans le \_ \_ groupe**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



Le compte d’utilisateur spécifié n’est pas membre du compte de groupe spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERREUR de la \_ dernière \_ administration**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Cette opération n’est pas autorisée, car elle peut entraîner la désactivation ou la suppression d’un compte d’administration ou l’impossibilité d’ouvrir une session.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**\_ \_ mot de passe erroné**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



Impossible de mettre à jour le mot de passe. La valeur fournie en tant que mot de passe actuel est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERREUR \_ \_ \_ de mot de passe incorrect**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



Impossible de mettre à jour le mot de passe. La valeur fournie pour le nouveau mot de passe contient des valeurs qui ne sont pas autorisées dans les mots de passe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_restriction de mot de passe d’erreur \_**
</dt> <dd> <dl> <dt>

1325 (0x52D)
</dt> <dt>



Impossible de mettre à jour le mot de passe. La valeur fournie pour le nouveau mot de passe ne répond pas aux exigences de longueur, de complexité ou d’historique du domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERREUR \_ d’ouverture de session \_**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



Le nom d'utilisateur ou le mot de passe est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_restriction de compte d’erreur \_**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



Les restrictions de compte empêchent cet utilisateur de se connecter. Par exemple : les mots de passe vides ne sont pas autorisés, les heures de connexion sont limitées ou une restriction de stratégie a été appliquée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERREUR \_ \_ d’heures d’ouverture de session non valide \_**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



Votre compte a des restrictions de temps qui vous empêchent de vous connecter pour le moment.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERREUR \_ de \_ station de travail non valide**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Cet utilisateur n’est pas autorisé à se connecter à cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**\_mot de passe d’erreur \_ expiré**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



Le mot de passe de ce compte a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**compte d’erreur \_ \_ désactivé**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Cet utilisateur ne peut pas se connecter, car ce compte est actuellement désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERREUR \_ aucune \_ mappée**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



Aucun mappage entre les noms de compte et les ID de sécurité n’a été effectué.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERREUR \_ trop \_ de \_ LUID \_ demandée**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Trop d’identificateurs d’utilisateur local (LUID) ont été demandés à un moment donné.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERREUR \_ LUID \_ épuisée**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



Aucun autre identificateur d’utilisateur local (LUID) n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERREUR \_ de \_ sous-autorité non valide \_**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



La partie sous-autorité d’un ID de sécurité n’est pas valide pour cette utilisation particulière.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERREUR \_ de \_ liste de contrôle d’accès non valide**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



La structure de la liste de contrôle d’accès (ACL) n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERREUR \_ sid non valide \_**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



La structure de l’ID de sécurité n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERREUR \_ de \_ Description de sécurité non valide \_**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



La structure du descripteur de sécurité n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERREUR \_ de \_ liste de contrôle d’héritage incorrect \_**
</dt> <dd> <dl> <dt>

1340 (0x53C)
</dt> <dt>



La liste de contrôle d’accès (ACL) ou l’entrée de contrôle d’accès (ACE) héritée n’a pas pu être créée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**serveur d’erreur \_ \_ désactivé**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



Le serveur est actuellement désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**serveur d’erreurs \_ \_ non \_ désactivé**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



Le serveur est actuellement activé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERREUR \_ \_ ID d' \_ autorité non valide**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



La valeur fournie est une valeur non valide pour une autorité d’identificateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERREUR de dépassement de l' \_ \_ espace alloué \_**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



Il n’y a plus de mémoire disponible pour les mises à jour des informations de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERREUR \_ d' \_ attributs de groupe non valide \_**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Les attributs spécifiés ne sont pas valides ou sont incompatibles avec les attributs du groupe dans son ensemble.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERREUR \_ de \_ niveau d’emprunt d’identité incorrect \_**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



Soit un niveau d'emprunt d'identité requis n'a pas été fourni, soit le niveau d'emprunt d'identité fourni n'est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERREUR \_ Impossible d' \_ ouvrir \_ anonyme**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



Impossible d’ouvrir un jeton de sécurité de niveau anonyme.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERREUR \_ , \_ classe de validation incorrecte \_**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



La classe d’informations de validation demandée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERREUR \_ de \_ type de jeton incorrect \_**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



Le type du jeton n’est pas approprié pour sa tentative d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERREUR \_ aucune \_ sécurité \_ sur l' \_ objet**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



Impossible d’effectuer une opération de sécurité sur un objet qui n’a pas de sécurité associée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERREUR \_ Impossible d' \_ accéder aux \_ informations de domaine \_**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



Impossible de lire les informations de configuration à partir du contrôleur de domaine, soit parce que l’ordinateur n’est pas disponible, soit parce que l’accès a été refusé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERREUR \_ d' \_ État du serveur non valide \_**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



Le gestionnaire de comptes de sécurité (SAM) ou le serveur de l’autorité de sécurité locale (LSA) est dans un état incorrect pour effectuer l’opération de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERREUR \_ d' \_ État de domaine non valide \_**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



Le domaine était dans un état incorrect pour effectuer l’opération de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERREUR \_ de \_ rôle de domaine non valide \_**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Cette opération est autorisée uniquement pour le contrôleur de domaine principal du domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERREUR \_ non de \_ ce type de \_ domaine**
</dt> <dd> <dl> <dt>

1355 (0x54B)
</dt> <dt>



Le domaine spécifié n’existe pas ou n’a pas pu être contacté.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**le \_ domaine d’erreur \_ existe**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



Le domaine spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**limite de domaine d’erreur \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

1357 (0x54D)
</dt> <dt>



Une tentative a été effectuée pour dépasser la limite du nombre de domaines par serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERREUR d’altération de la \_ \_ base de DB interne \_**
</dt> <dd> <dl> <dt>

1358 (0x54E)
</dt> <dt>



Impossible d’effectuer l’opération demandée en raison d’une panne de support catastrophique ou d’une corruption de la structure de données sur le disque.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**erreur \_ interne \_ erreur**
</dt> <dd> <dl> <dt>

1359 (0x54F)
</dt> <dt>



Une erreur interne s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERREUR \_ générique \_ non \_ mappée**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



Les types d’accès génériques étaient contenus dans un masque d’accès qui doit déjà être mappé à des types non génériques.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERREUR \_ de \_ format de descripteur incorrect \_**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Un descripteur de sécurité n’est pas dans le format approprié (absolu ou auto-relatif).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERREUR lors du \_ \_ processus d’ouverture de session \_**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



L’action demandée est restreinte pour une utilisation par les processus d’ouverture de session uniquement. Le processus appelant n’a pas été inscrit en tant que processus d’ouverture de session.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERREUR de \_ session d’ouverture de \_ session \_**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



Impossible de démarrer une nouvelle ouverture de session avec un ID qui est déjà en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERREUR \_ aucun \_ package de ce type \_**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Un package d’authentification spécifié est inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERREUR \_ \_ d’état de session de connexion incorrecte \_ \_**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



La session d’ouverture de session n’est pas dans un état cohérent avec l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERREUR \_ de \_ collision de session de connexion \_**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



L’ID de session d’ouverture de session est déjà utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERREUR \_ de \_ type d’ouverture de session non valide \_**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Une demande d’ouverture de session contenait une valeur de type d’ouverture de session non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERREUR \_ Impossible d' \_ emprunter l’identité**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



Impossible d’emprunter l’identité à l’aide d’un canal nommé tant que les données n’ont pas été lues à partir de ce canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERREUR \_ RXACT \_ État non valide \_**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



L’état de transaction d’une sous-arborescence du Registre est incompatible avec l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**erreur de validation d’erreur \_ RXACT \_ \_**
</dt> <dd> <dl> <dt>

1370 (0x55A)
</dt> <dt>



Une corruption de base de données de sécurité interne a été détectée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_compte spécial d’erreur \_**
</dt> <dd> <dl> <dt>

1371 (0x55B)
</dt> <dt>



Impossible d’effectuer cette opération sur les comptes intégrés.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**\_Groupe spécial d’erreur \_**
</dt> <dd> <dl> <dt>

1372 (0x55C)
</dt> <dt>



Impossible d’effectuer cette opération sur ce groupe spécial intégré.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_utilisateur spécial d’erreur \_**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



Impossible d’effectuer cette opération sur cet utilisateur spécial intégré.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**\_ \_ groupe principal d’erreurs membres \_**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



L’utilisateur ne peut pas être supprimé d’un groupe, car le groupe est actuellement le groupe principal de l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**\_jeton \_ d’erreur \_ déjà \_ utilisé**
</dt> <dd> <dl> <dt>

1375 (0x55F)
</dt> <dt>



Le jeton est déjà utilisé en tant que jeton principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERREUR \_ de \_ ce type d' \_ alias**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



Le groupe local spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**\_membre \_ d’erreur non \_ dans l' \_ alias**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



Le nom de compte spécifié n’est pas membre du groupe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_membre \_ d’erreur dans l' \_ alias**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



Le nom de compte spécifié est déjà membre du groupe.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**l' \_ alias d’erreur \_ existe**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



Le groupe local spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERREUR \_ d’ouverture de session \_ non \_ accordée**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Échec de l’ouverture de session : l’utilisateur n’a pas obtenu le type d’ouverture de session demandé sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERREUR \_ trop \_ de \_ secrets**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



Le nombre maximal de secrets qui peuvent être stockés dans un seul système a été dépassé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**SECRET d’erreur \_ \_ trop \_ long**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



La longueur d’un secret dépasse la longueur maximale autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**erreur \_ interne de la \_ base de \_**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



La base de données de l’autorité de sécurité locale contient une incohérence interne.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERREUR \_ trop \_ d' \_ ID de contexte \_**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Pendant une tentative de connexion, le contexte de sécurité de l’utilisateur a accumulé trop d’ID de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_type d’erreur d’ouverture de session \_ \_ non \_ accordé**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Échec de l’ouverture de session : l’utilisateur n’a pas obtenu le type d’ouverture de session demandé sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERREUR \_ de \_ \_ chiffrement croisé NT \_ requis**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Un mot de passe à chiffrement croisé est nécessaire pour modifier le mot de passe d’un utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERREUR \_ non \_ membre de ce type \_**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



Impossible d’ajouter ou de supprimer un membre du groupe local, car le membre n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERREUR \_ membre non valide \_**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



Impossible d’ajouter un nouveau membre à un groupe local, car le type de compte du membre est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERREUR \_ trop \_ de \_ sid**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Un trop grand nombre d’ID de sécurité a été spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERREUR \_ LM \_ de \_ chiffrement croisé \_ obligatoire**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Un mot de passe à chiffrement croisé est nécessaire pour modifier ce mot de passe utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERREUR \_ aucun \_ héritage**
</dt> <dd> <dl> <dt>

1391 (0x56F)
</dt> <dt>



Indique qu’une liste de contrôle d’accès ne contient aucun composant pouvant être hérité.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**fichier d’erreur \_ \_ endommagé**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



Le fichier ou le répertoire est endommagé et illisible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERREUR \_ disque \_ endommagé**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



La structure du disque est endommagée et illisible.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERREUR \_ aucune \_ \_ clé de session utilisateur \_**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



Il n’existe aucune clé de session utilisateur pour la session d’ouverture de session spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_dépassement du \_ quota de licences d’erreur \_**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



Le service auquel vous accédez a une licence pour un nombre particulier de connexions. Aucune autre connexion ne peut être établie au service pour l’instant, car il existe déjà autant de connexions que le service peut accepter.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERREUR \_ \_ nom cible \_ erroné**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



Le nom du compte cible est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERREUR \_ l' \_ authentification mutuelle \_ a échoué**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



L’authentification mutuelle a échoué. Le mot de passe du serveur est obsolète sur le contrôleur de domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**décalage de l’heure d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Il y a une différence de temps et/ou de date entre le client et le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERREUR \_ \_ domaine actuel \_ non \_ autorisé**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Cette opération ne peut pas être effectuée sur le domaine actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERREUR \_ de \_ handle de fenêtre non valide \_**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Handle de fenêtre non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERREUR \_ de \_ handle de menu non valide \_**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Descripteur de menu non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERREUR \_ de \_ handle de curseur non valide \_**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Handle de curseur non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERREUR \_ de \_ handle d’accélération non valide \_**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Handle de table d’accélérateurs non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERREUR \_ de \_ handle de hook non valide \_**
</dt> <dd> <dl> <dt>

1404 (0x57C)
</dt> <dt>



Handle de hook non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERREUR \_ de \_ handle DWP non valide \_**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Handle non valide vers une structure de position à plusieurs fenêtres.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERREUR \_ TLW \_ avec \_ WSCHILD**
</dt> <dd> <dl> <dt>

1406 (0x57E)
</dt> <dt>



Impossible de créer une fenêtre enfant de niveau supérieur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERREUR \_ Impossible de \_ trouver la \_ \_ classe WND**
</dt> <dd> <dl> <dt>

1407 (0x57F)
</dt> <dt>



Impossible de trouver la classe de fenêtre.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_fenêtre \_ d’erreur d’un \_ autre \_ thread**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Fenêtre non valide ; elle appartient à un autre thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERREUR de \_ raccourci \_ déjà \_ inscrit**
</dt> <dd> <dl> <dt>

1409 (0x581)
</dt> <dt>



La touche d’accès rapide est déjà inscrite.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**la \_ classe d’erreur \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



La classe existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**la \_ classe d’erreur \_ n' \_ \_ existe pas**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



La classe n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**la \_ classe Error \_ contient \_ Windows**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



La classe a toujours des fenêtres ouvertes.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERREUR \_ d' \_ index non valide**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Index non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**HANDLE d’icône d’erreur \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Handle d’icône non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERREUR \_ d' \_ index de boîte de dialogue privé \_**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Utilisation de mots de boîte de dialogue privés.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ID de zone de liste d’erreurs \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



L’identificateur de la zone de liste est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERREUR \_ aucun caractère \_ générique \_**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



Aucun caractère générique n’a été trouvé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERREUR \_ du presse-papiers \_ non \_ ouvert**
</dt> <dd> <dl> <dt>

1418 (0x58A)
</dt> <dt>



Le thread n’a pas de presse-papiers ouvert.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERREUR de \_ raccourci \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

1419 (0x58B)
</dt> <dt>



La touche d’accès rapide n’est pas inscrite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**fenêtre d’erreur, \_ \_ pas de boîte de \_ dialogue**
</dt> <dd> <dl> <dt>

1420 (0x58C)
</dt> <dt>



La fenêtre n’est pas une fenêtre de boîte de dialogue valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ID de contrôle d’erreur \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1421 (0x58D)
</dt> <dt>



ID de contrôle introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**MESSAGE d’erreur de \_ ComboBox non valide \_ \_**
</dt> <dd> <dl> <dt>

1422 (0x58E)
</dt> <dt>



Message non valide pour une zone de liste déroulante, car il ne dispose pas d’un contrôle d’édition.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**fenêtre d’erreur \_ \_ non \_ ComboBox**
</dt> <dd> <dl> <dt>

1423 (0x58F)
</dt> <dt>



La fenêtre n’est pas une zone de liste déroulante.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERREUR de modification de la \_ \_ hauteur non valide \_**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



La hauteur doit être inférieure à 256.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**\_DC d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Handle de contexte de périphérique (DC) non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERREUR \_ de \_ filtre de hook non valide \_**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Type de procédure de raccordement non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERREUR \_ de \_ procédure de filtre non valide \_**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Procédure de hook non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**raccordement d’erreur \_ \_ nécessitant \_ HMOD**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



Impossible de définir un hook non local sans un handle de module.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**\_crochet global \_ uniquement d’erreur \_**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Cette procédure de hook ne peut être définie que globalement.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_ensemble de \_ raccordements du journal des erreurs \_**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



La procédure de hook du journal est déjà installée.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**HOOK d’erreur \_ \_ non \_ installé**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



La procédure de hook n’est pas installée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERREUR \_ de \_ message lb non valide \_**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Message non valide pour une zone de liste à sélection unique.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERREUR \_ SETCOUNT \_ sur \_ Bad \_ lb**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



LB \_ SETCOUNT envoyé à une zone de liste non différée.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERREUR \_ lb \_ sans \_ TABSTOPS**
</dt> <dd> <dl> <dt>

1434 (0x59A)
</dt> <dt>



Cette zone de liste ne prend pas en charge les taquets de tabulation.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERREUR \_ \_ de destruction de l’objet d’un \_ \_ autre \_ thread**
</dt> <dd> <dl> <dt>

1435 (0x59B)
</dt> <dt>



Impossible de détruire un objet créé par un autre thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_menu de \_ fenêtre \_ enfant d’erreur**
</dt> <dd> <dl> <dt>

1436 (0x59C)
</dt> <dt>



Les fenêtres enfants ne peuvent pas avoir de menus.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERREUR \_ \_ \_ -menu système**
</dt> <dd> <dl> <dt>

1437 (0x59D)
</dt> <dt>



La fenêtre n’a pas de menu système.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERREUR \_ de \_ style MsgBox non valide \_**
</dt> <dd> <dl> <dt>

1438 (0x59E)
</dt> <dt>



Style de boîte de message non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERREUR \_ \_ valeur SPI non valide \_**
</dt> <dd> <dl> <dt>

1439 (0x59F)
</dt> <dt>



Paramètre au niveau du système (SPI) non valide \_ \* .


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**écran d’erreur \_ \_ déjà \_ verrouillé**
</dt> <dd> <dl> <dt>

1440 (0x5A0)
</dt> <dt>



Écran déjà verrouillé.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERREUR les \_ HWND \_ ont un \_ \_ parent diff**
</dt> <dd> <dl> <dt>

1441 (0x5A1)
</dt> <dt>



Tous les descripteurs de Windows dans une structure de position à fenêtres multiples doivent avoir le même parent.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**fenêtre d’erreur \_ non \_ enfant \_**
</dt> <dd> <dl> <dt>

1442 (0x5A2)
</dt> <dt>



La fenêtre n’est pas une fenêtre enfant.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERREUR \_ de \_ commande GW non valide \_**
</dt> <dd> <dl> <dt>

1443 (0x5A3)
</dt> <dt>



Commande GW non valide \_ \* .


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**\_ID de \_ thread non valide d’erreur \_**
</dt> <dd> <dl> <dt>

1444 (0x5A4)
</dt> <dt>



Identificateur de thread non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**\_fenêtre erreur non- \_ MDICHILD \_**
</dt> <dd> <dl> <dt>

1445 (0x5A5)
</dt> <dt>



Impossible de traiter un message à partir d’une fenêtre qui n’est pas une fenêtre d’interface multidocument (MDI).


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**\_fenêtre contextuelle d’erreur \_ déjà \_ active**
</dt> <dd> <dl> <dt>

1446 (0x5A6)
</dt> <dt>



Menu contextuel déjà actif.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERREUR \_ aucune \_ barre de défilement**
</dt> <dd> <dl> <dt>

1447 (0x5A7)
</dt> <dt>



La fenêtre n’a pas de barres de défilement.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERREUR \_ de \_ plage de barre de défilement non valide \_**
</dt> <dd> <dl> <dt>

1448 (0x5A8)
</dt> <dt>



La plage de la barre de défilement ne peut pas être supérieure à MAXLONG.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERREUR \_ de \_ commande SHOWWIN non valide \_**
</dt> <dd> <dl> <dt>

1449 (0x5A9)
</dt> <dt>



Impossible d’afficher ou de supprimer la fenêtre de la manière spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERREUR \_ aucune \_ \_ ressource système**
</dt> <dd> <dl> <dt>

1450 (0x5AA)
</dt> <dt>



Les ressources système sont insuffisantes pour terminer le service demandé.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**\_ressources système non paginées de l’erreur \_ \_**
</dt> <dd> <dl> <dt>

1451 (0x5AB)
</dt> <dt>



Les ressources système sont insuffisantes pour terminer le service demandé.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ressources système d’erreur \_ paginée \_ \_**
</dt> <dd> <dl> <dt>

1452 (0x5AC)
</dt> <dt>



Les ressources système sont insuffisantes pour terminer le service demandé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**QUOTA de la plage de travail des erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

1453 (0x5AD)
</dt> <dt>



Quota insuffisant pour terminer le service demandé.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERREUR de \_ quota du fichier d’échange \_**
</dt> <dd> <dl> <dt>

1454 (0x5AE)
</dt> <dt>



Quota insuffisant pour terminer le service demandé.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_limite d’engagement d’erreur \_**
</dt> <dd> <dl> <dt>

1455 (0x5AF)
</dt> <dt>



Le fichier d’échange est trop petit pour que cette opération se termine.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**élément de menu d’erreur \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1456 (0x5B0)
</dt> <dt>



Élément de menu introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERREUR \_ de \_ handle de clavier non valide \_**
</dt> <dd> <dl> <dt>

1457 (0x5B1)
</dt> <dt>



Handle de disposition de clavier non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**TYPE de raccordement d’erreur \_ \_ \_ non \_ autorisé**
</dt> <dd> <dl> <dt>

1458 (0x5B2)
</dt> <dt>



Type de raccordement non autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**l’erreur \_ requiert un \_ \_ WINDOWSTATION interactif**
</dt> <dd> <dl> <dt>

1459 (0x5B3)
</dt> <dt>



Cette opération nécessite une station Windows Interactive.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_délai d’erreur**
</dt> <dd> <dl> <dt>

1460 (0x5B4)
</dt> <dt>



Cette opération a été renvoyée car le délai d'attente a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERREUR \_ de \_ handle de moniteur non valide \_**
</dt> <dd> <dl> <dt>

1461 (0x5B5)
</dt> <dt>



Handle de moniteur non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERREUR de \_ taille incorrecte \_**
</dt> <dd> <dl> <dt>

1462 (0x5B6)
</dt> <dt>



Argument de taille incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERREUR \_ de \_ classe symlink \_ désactivée**
</dt> <dd> <dl> <dt>

1463 (0x5B7)
</dt> <dt>



Le lien symbolique ne peut pas être suivi, car son type est désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERREUR \_ symlink \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

1464 (0x5B8)
</dt> <dt>



Cette application ne prend pas en charge l’opération en cours sur les liens symboliques.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**erreur \_ d' \_ analyse XML d’erreur \_**
</dt> <dd> <dl> <dt>

1465 (0x5B9)
</dt> <dt>



Windows n’a pas pu analyser les données XML demandées.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**erreur \_ XMLDSIG \_ erreur XMLDSIG**
</dt> <dd> <dl> <dt>

1466 (0x5BA)
</dt> <dt>



Une erreur s’est produite lors du traitement d’une signature numérique XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERREUR de \_ redémarrage de l' \_ application**
</dt> <dd> <dl> <dt>

1467 (0x5BB)
</dt> <dt>



Cette application doit être redémarrée.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERREUR \_ de \_ compartiment incorrect**
</dt> <dd> <dl> <dt>

1468 (0x5BC)
</dt> <dt>



L’appelant a effectué la demande de connexion dans le compartiment de routage incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERREUR \_ AUTHIP \_ échec**
</dt> <dd> <dl> <dt>

1469 (0x5BD)
</dt> <dt>



Un échec AuthIP s’est produite lors de la tentative de connexion à l’hôte distant.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERREUR \_ aucune \_ \_ ressource NVRAM**
</dt> <dd> <dl> <dt>

1470 (0x5BE)
</dt> <dt>



Des ressources NVRAM insuffisantes existent pour terminer le service demandé. Un redémarrage peut être nécessaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERREUR \_ pas de traitement de l' \_ interface graphique \_**
</dt> <dd> <dl> <dt>

1471 (0x5BF)
</dt> <dt>



Impossible de terminer l’opération demandée, car le processus spécifié n’est pas un processus GUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERREUR \_ \_ fichier journal \_ endommagé**
</dt> <dd> <dl> <dt>

1500 (0x5DC)
</dt> <dt>



Le fichier journal des événements est endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERREUR \_ EventLog \_ Impossible de \_ Démarrer**
</dt> <dd> <dl> <dt>

1501 (0x5DD)
</dt> <dt>



Aucun fichier journal des événements n’a pu être ouvert. le service de journalisation des événements n’a donc pas démarré.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**\_fichier journal des erreurs \_ \_ plein**
</dt> <dd> <dl> <dt>

1502 (0x5DE)
</dt> <dt>



Le fichier journal des événements est plein.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERREUR \_ de \_ fichier EventLog \_ modifié**
</dt> <dd> <dl> <dt>

1503 (0x5DF)
</dt> <dt>



Le fichier journal des événements a changé entre les opérations de lecture.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERREUR \_ \_ nom de tâche non valide \_**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



Le nom de tâche spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERREUR \_ d' \_ index de tâche non valide \_**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



L’index de tâche spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_thread \_ d’erreur déjà dans la \_ \_ tâche**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



Le thread spécifié est déjà joint à une tâche.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERREUR lors de l’installation de l' \_ \_ échec du service \_**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



impossible d’accéder au Service Windows Installer. cela peut se produire si le Windows Installer n’est pas correctement installé. Contactez votre service de support technique pour obtenir de l’aide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERREUR lors de l' \_ installation de \_ USEREXIT**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



Installation annulée par l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERREUR d' \_ installation \_**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Erreur irrécupérable lors de l’installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERREUR d' \_ installation d' \_ interruption**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Installation interrompue, incomplète.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERREUR \_ de \_ produit inconnu**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Cette action est valide uniquement pour les produits actuellement installés.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**\_fonctionnalité inconnue d’erreur \_**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



L’ID de fonctionnalité n’est pas inscrit.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERREUR \_ de \_ composant inconnu**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



L’ID du composant n’est pas inscrit.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERREUR \_ , \_ propriété inconnue**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Propriété inconnue.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERREUR \_ d' \_ État de handle non valide \_**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



Le descripteur est dans un État non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERREUR de \_ configuration incorrecte \_**
</dt> <dd> <dl> <dt>

1610 (0x64A)
</dt> <dt>



Les données de configuration de ce produit sont endommagées. Contactez votre service de support technique.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**INDEX d’erreurs \_ \_ absent**
</dt> <dd> <dl> <dt>

1611 (0x64B)
</dt> <dt>



Qualificateur de composant absent.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERREUR d’installation de la \_ \_ source \_ absente**
</dt> <dd> <dl> <dt>

1612 (0x64C)
</dt> <dt>



La source d’installation de ce produit n’est pas disponible. Vérifiez que la source existe et que vous êtes en mesure d’y accéder.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERREUR d’installation de la \_ \_ version du package \_**
</dt> <dd> <dl> <dt>

1613 (0x64D)
</dt> <dt>



ce package d’installation ne peut pas être installé par le service Windows Installer. vous devez installer un Windows Service Pack qui contient une version plus récente du service Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERREUR de \_ produit \_ désinstallée**
</dt> <dd> <dl> <dt>

1614 (0x64E)
</dt> <dt>



Le produit est désinstallé.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERREUR \_ de \_ syntaxe de requête incorrecte \_**
</dt> <dd> <dl> <dt>

1615 (0x64F)
</dt> <dt>



la syntaxe de la requête de SQL n’est pas valide ou n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**champ d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



Le champ d’enregistrement n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**périphérique d’erreur \_ \_ supprimé**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



L’appareil a été supprimé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERREUR d' \_ installation \_ déjà \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



Une autre installation est déjà en cours. Terminez cette installation avant de procéder à cette installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERREUR \_ d' \_ \_ échec d’ouverture du package d’installation \_**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



Ce package d’installation n’a pas pu être ouvert. vérifiez que le package existe et que vous pouvez y accéder, ou contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de Windows Installer valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERREUR lors de l' \_ installation du \_ package \_ non valide**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



Ce package d’installation n’a pas pu être ouvert. contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de Windows Installer valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERREUR d' \_ installation de \_ l’interface utilisateur \_**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



une erreur s’est produite lors du démarrage de l’interface utilisateur du service Windows Installer. Contactez votre service de support technique.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERREUR d’installation de l' \_ \_ échec du journal \_**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



Erreur lors de l’ouverture du fichier journal d’installation. Vérifiez que l’emplacement du fichier journal spécifié existe et que vous pouvez y écrire.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERREUR d’installation de la \_ \_ langue \_ non prise en charge**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



Le langage de ce package d’installation n’est pas pris en charge par votre système.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERREUR lors de l’installation de l’échec de la \_ \_ transformation \_**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Erreur lors de l’application des transformations. Vérifiez que les chemins d’accès de transformation spécifiés sont valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERREUR lors de l' \_ installation du \_ package \_ rejeté**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Cette installation est interdite par la stratégie système. Contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**fonction d’erreur \_ \_ non \_ appelée**
</dt> <dd> <dl> <dt>

1626 (0x65A)
</dt> <dt>



Impossible d’exécuter la fonction.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**échec de la fonction d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1627 (0x65B)
</dt> <dt>



Échec de la fonction pendant l’exécution.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**TABLE d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

1628 (0x65C)
</dt> <dt>



Table spécifiée non valide ou inconnue.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**incompatibilité de type de données d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1629 (0x65D)
</dt> <dt>



Le type des données fournies est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**TYPE d’erreur \_ non pris en charge \_**
</dt> <dd> <dl> <dt>

1630 (0x65E)
</dt> <dt>



Les données de ce type ne sont pas prises en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**échec de la création d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1631 (0x65F)
</dt> <dt>



échec du démarrage du service Windows Installer. Contactez votre service de support technique.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERREUR lors de l' \_ installation de \_ temp \_**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



Le dossier temporaire se trouve sur un lecteur qui est saturé ou inaccessible. Libérez de l’espace sur le lecteur ou vérifiez que vous disposez de l’autorisation en écriture sur le dossier temporaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERREUR d' \_ installation de \_ plateforme \_ non prise en charge**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Ce package d’installation n’est pas pris en charge par ce type de processeur. Contactez le fournisseur de votre produit.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERREUR lors de l' \_ installation de \_ NOTUSED**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Composant non utilisé sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERREUR \_ échec de l’ouverture du \_ package correctif \_ \_**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



Impossible d’ouvrir ce package de mise à jour. vérifiez que le package de mise à jour existe et que vous pouvez y accéder, ou contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de mise à jour Windows Installer valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERREUR \_ de \_ package correctif \_ non valide**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



Impossible d’ouvrir ce package de mise à jour. contactez le fournisseur de l’application pour vérifier qu’il s’agit d’un package de mise à jour Windows Installer valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERREUR \_ \_ package correctif \_ non pris en charge**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



ce package de mise à jour ne peut pas être traité par le service Windows Installer. vous devez installer un Windows Service Pack qui contient une version plus récente du service Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_version du produit d’erreur \_**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Une autre version de ce produit est déjà installée. L’installation de cette version ne peut pas continuer. Pour configurer ou supprimer la version existante de ce produit, utilisez Ajout/suppression de programmes dans le panneau de configuration.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERREUR \_ \_ ligne de commande non valide \_**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Argument de ligne de commande non valide. pour obtenir une aide détaillée sur la ligne de commande, consultez le kit de développement logiciel Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERREUR d' \_ installation \_ distante non \_ autorisée**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Seuls les administrateurs ont l’autorisation d’ajouter, de supprimer ou de configurer le logiciel serveur pendant une session à distance des services Terminal Server. Si vous souhaitez installer ou configurer le logiciel sur le serveur, contactez votre administrateur réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERREUR \_ de \_ redémarrage de réussite \_ lancée**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



L’opération demandée s’est terminée avec succès. Le système va être redémarré pour que les modifications puissent être prises en compte.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERREUR de la \_ cible du correctif \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1642 (0x66A)
</dt> <dt>



la mise à niveau ne peut pas être installée par le service Windows Installer, car le programme à mettre à niveau est peut-être manquant ou la mise à niveau peut mettre à jour une autre version du programme. Vérifiez que le programme à mettre à niveau existe sur votre ordinateur et que vous disposez de la mise à niveau appropriée.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERREUR \_ de \_ rejet du package de correctifs \_**
</dt> <dd> <dl> <dt>

1643 (0x66B)
</dt> <dt>



Le package de mise à jour n’est pas autorisé par la stratégie de restriction logicielle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERREUR d’installation de la \_ \_ transformation \_ rejetée**
</dt> <dd> <dl> <dt>

1644 (0x66C)
</dt> <dt>



Une ou plusieurs personnalisations ne sont pas autorisées par la stratégie de restriction logicielle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERREUR \_ d' \_ installation \_ interdite à distance**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



le Windows Installer ne permet pas l’installation à partir d’un Connexion Bureau à distance.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERREUR \_ de \_ Suppression de correctif \_ non prise en charge**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



La désinstallation du package de mise à jour n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERREUR \_ de \_ correctif inconnu**
</dt> <dd> <dl> <dt>

1647 (0x66F)
</dt> <dt>



La mise à jour n’est pas appliquée à ce produit.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**correctif d’erreur- \_ \_ aucune \_ séquence**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



Aucune séquence valide n’a été trouvée pour l’ensemble de mises à jour.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERREUR de \_ Suppression de correctif non \_ \_ autorisée**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



La suppression de la mise à jour a été interdite par la stratégie.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERREUR \_ de \_ code XML de correctif non valide \_**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



Les données de mise à jour XML ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERREUR de mise à \_ jour du \_ \_ \_ produit publié**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows Le programme d’installation n’autorise pas la mise à jour des produits publiés gérés. Au moins une fonctionnalité du produit doit être installée avant l’application de la mise à jour.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERREUR lors de l' \_ installation du \_ service \_ SafeBoot**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



le service Windows Installer n’est pas accessible en Mode Coffre. réessayez si votre ordinateur n’est pas en Mode Coffre ou si vous pouvez utiliser la restauration du système pour ramener votre ordinateur à un état correct précédent.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**erreur d' \_ échec \_ FAST d' \_ EXCEPTION**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Une exception Fail Fast s’est produite. Les gestionnaires d’exceptions ne sont pas appelés et le processus se termine immédiatement.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERREUR d' \_ installation \_ rejetée**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



L’application que vous essayez d’exécuter n’est pas prise en charge sur cette version de Windows.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur système](system-error-codes.md)
</dt> </dl>

 

 




