---
title: Messages d’erreur (Wininet. h)
description: Les fonctions WinINet renvoient des codes d’erreur le cas échéant. Les erreurs suivantes sont spécifiques aux fonctions WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013125"
---
# <a name="error-messages-winineth"></a>Messages d’erreur (Wininet. h)

Les fonctions WinINet renvoient des codes d’erreur le cas échéant. Les erreurs suivantes sont spécifiques aux fonctions WinINet.

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERREUR \_ FTP \_ supprimée**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



L’opération FTP n’a pas été effectuée car la session a été abandonnée.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERREUR \_ FTP \_ aucun \_ \_ mode passif**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



Le mode passif n’est pas disponible sur le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERREUR \_ \_ de transfert FTP \_ en \_ cours**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



L’opération demandée ne peut pas être effectuée sur le descripteur de session FTP, car une opération est déjà en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERREUR \_ Gopher \_ \_ non \_ trouvée**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



L’attribut demandé est introuvable.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**erreur \_ de \_ données \_ Gopher**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



Une erreur a été détectée lors de la réception des données du serveur Gopher.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERREUR \_ Gopher \_ de la fin \_ des \_ données**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



La fin des données a été atteinte.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERREUR \_ Gopher \_ \_ type de localisateur incorrect \_**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



Le type du localisateur n’est pas correct pour cette opération.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERREUR \_ Gopher \_ - \_ localisateur non valide**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



Le localisateur fourni n’est pas valide.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERREUR \_ Gopher \_ not \_ file**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



La demande doit être effectuée pour un localisateur de fichier.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERREUR \_ Gopher \_ non \_ Gopher \_ plus**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



L’opération demandée ne peut être effectuée que sur un serveur Gopher +, ou avec un localisateur qui spécifie une opération Gopher +.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**erreur \_ de \_ protocole \_ Gopher**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



Une erreur a été détectée lors de l’analyse des données retournées par le serveur Gopher.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERREUR \_ Gopher \_ - \_ localisateur inconnu**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



Le type de localisateur est inconnu.

> [!Note]  
> Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERREUR \_ \_ cookie HTTP \_ refusé**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



Le cookie HTTP a été refusé par le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERREUR \_ de \_ confirmation du cookie HTTP \_ \_**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



Le cookie HTTP nécessite une confirmation.

> [!Note]  
> Windows Vista et Windows Server 2008 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERREUR \_ \_ serveur de niveau inférieur http \_**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



Le serveur n’a retourné aucun en-tête.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**l' \_ \_ en-tête http d’erreur \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Impossible d’ajouter l’en-tête, car il existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**l' \_ en-tête http de l’erreur est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



L’en-tête demandé est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERREUR \_ http \_ \_ -en-tête non valide**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



L’en-tête fourni n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERREUR \_ de \_ \_ requête de requête non valide http \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



La demande adressée à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERREUR \_ de \_ \_ réponse du serveur http non valide \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



La réponse du serveur n’a pas pu être analysée.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERREUR \_ http \_ non \_ redirigée**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



La requête HTTP n’a pas été redirigée.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERREUR \_ de \_ redirection \_ http**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



La redirection a échoué, car le schéma a changé (par exemple, HTTP en FTP) ou toutes les tentatives effectuées pour la redirection ont échoué (cinq tentatives par défaut).


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**l’erreur de \_ \_ redirection http \_ nécessite une \_ confirmation**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



La redirection requiert la confirmation de l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERREUR \_ \_ échec du \_ thread \_ asynchrone Internet**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



L’application n’a pas pu démarrer un thread asynchrone.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERREUR \_ Internet \_ mauvais \_ \_ script de proxy automatique \_**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Une erreur s’est produite dans le script de configuration automatique du proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERREUR \_ Internet-longueur de l' \_ option incorrecte \_ \_**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



La longueur d’une option fournie à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) est incorrecte pour le type d’option spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERREUR \_ de \_ \_ paramètre de registre Internet incorrect \_**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



Une valeur de registre requise a été trouvée, mais son type est incorrect ou sa valeur n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERREUR \_ Internet \_ ne peut pas \_ se connecter**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



La tentative de connexion au serveur a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERREUR \_ la \_ publication d’Internet CHG \_ \_ n’est \_ pas \_ sécurisée**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



L’application publie et tente de modifier plusieurs lignes de texte sur un serveur qui n’est pas sécurisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERREUR \_ de \_ certificat d’authentification du client Internet \_ \_ \_ requis**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Le serveur demande l’authentification du client.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERREUR \_ \_ d’authentification du client Internet \_ \_ non \_ configurée**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



L’autorisation du client n’est pas configurée sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERREUR \_ de \_ connexion Internet \_ abandonnée**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La connexion avec le serveur a été arrêtée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERREUR \_ de \_ réinitialisation de la connexion Internet \_**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



La connexion avec le serveur a été réinitialisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERREUR lors du \_ \_ décodage Internet \_**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



WinINet n’a pas pu effectuer le décodage du contenu sur la réponse. Pour plus d’informations, consultez la rubrique relative à l' [**encodage du contenu**](content-encoding.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**boîte de dialogue d’erreur \_ Internet \_ \_ en attente**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



Une boîte de dialogue de mot de passe est en cours pour un autre thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERREUR \_ Internet \_ déconnectée**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



La connexion Internet a été perdue.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**erreur \_ \_ étendue Internet \_**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



Une erreur étendue a été retournée par le serveur. Il s’agit généralement d’une chaîne ou d’une mémoire tampon contenant un message d’erreur détaillé. Appelez [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) pour récupérer le texte d’erreur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERREUR \_ Internet \_ failed \_ DUETOSECURITYCHECK**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



La fonction a échoué en raison d’une vérification de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERREUR \_ de \_ tentative Internet forcée \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



La fonction doit rétablir la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERREUR \_ de \_ connexion Internet Fortezza \_ \_ nécessaire**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



La ressource demandée requiert une authentification Fortezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERREUR \_ de \_ descripteur Internet \_**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



La requête a échoué, car le handle existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERREUR \_ Internet \_ http \_ à \_ https \_ sur le \_ ReDim**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



L’application est déplacée d’une connexion non-SSL vers une connexion SSL en raison d’une redirection.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERREUR \_ d' \_ envoi de \_ l' \_ \_ instruction http https http à Internet**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



Les données soumises à une connexion SSL sont redirigées vers une connexion non-SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERREUR \_ Internet \_ https \_ à \_ http \_ sur le \_ ReDim**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



L’application est déplacée d’une connexion SSL vers une connexion non-SSL en raison d’une redirection.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERREUR \_ de \_ format incorrect Internet \_**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



Le format de la demande n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERREUR \_ d' \_ \_ État de handle incorrect Internet \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Impossible d’effectuer l’opération demandée, car le handle fourni n’est pas dans l’état correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERREUR \_ de \_ \_ type de descripteur incorrect Internet \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Le type de handle fourni est incorrect pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERREUR \_ \_ \_ de mot de passe incorrect Internet**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



La demande de connexion et d’ouverture de session sur un serveur FTP n’a pas pu aboutir car le mot de passe fourni est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERREUR \_ Internet \_ \_ nom d’utilisateur incorrect \_**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



La demande de connexion et d’ouverture de session sur un serveur FTP n’a pas pu aboutir car le nom d’utilisateur fourni est incorrect.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERREUR d' \_ insertion Internet dans le \_ \_ cdrom**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



La demande nécessite l’insertion d’un CD-ROM dans le lecteur de CD-ROM pour localiser la ressource demandée.

> [!Note]  
> Windows Vista et Windows Server 2008 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**erreur \_ \_ interne Internet \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Une erreur interne s'est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERREUR \_ Internet \_ non valide \_**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



La fonction ne connaît pas l’autorité de certification qui a généré le certificat du serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERREUR \_ Internet \_ non valide \_**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



L’opération demandée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**\_option Internet \_ non valide \_ d’erreur**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Une requête à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) A spécifié une valeur d’option non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERREUR \_ de \_ \_ demande de proxy non valide Internet \_**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



La demande adressée au proxy n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERREUR \_ \_ URL non valide Internet \_**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



L’URL n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERREUR \_ Internet \_ élément \_ \_ introuvable**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



L’élément demandé est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERREUR \_ de \_ connexion \_ Internet**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



La demande de connexion et d’ouverture de session sur un serveur FTP a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERREUR \_ de \_ connexion \_ Internet \_ afficher \_ le \_ corps de l’entité**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



L’en-tête Digest MS-Logoff a été retourné à partir du site Web. Cet en-tête demande spécifiquement au package de résumé de purger les informations d’identification du domaine associé. Cette erreur est renvoyée uniquement si l’option le corps d’entité de l' [échec de connexion de \_ masque d’erreur \_ \_ \_ \_ \_ \_ Internet](option-flags.md) est définie ; sinon, l' **erreur de \_ \_ connexion Internet \_** est retournée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERREUR \_ de \_ sécurité mixte Internet \_**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



Le contenu n’est pas entièrement sécurisé. Une partie du contenu affiché peut provenir de serveurs non sécurisés.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERREUR \_ de \_ nom Internet \_ non \_ résolu**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Impossible de résoudre le nom du serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERREUR \_ Internet \_ besoin de \_ MSN \_ SSPI \_ pkg**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



Actuellement non implémenté.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERREUR \_ Internet \_ nécessitant une \_ interface utilisateur**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



Une interface utilisateur ou une autre opération de blocage a été demandée.

> [!Note]  
> Windows Vista et Windows Server 2008 et versions antérieures uniquement.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERREUR \_ Internet \_ aucun \_ rappel**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



Une requête asynchrone n’a pas pu être effectuée, car aucune fonction de rappel n’a été définie.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERREUR \_ Internet \_ aucun \_ contexte**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



Une requête asynchrone n’a pas pu être effectuée, car une valeur de contexte zéro a été fournie.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERREUR \_ Internet \_ aucun \_ \_ accès direct**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



L’accès direct au réseau ne peut pas être effectué pour le moment.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERREUR \_ Internet \_ non \_ initialisée**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



L’initialisation de l’API WinINet n’a pas eu lieu. Indique qu’une fonction de niveau supérieur, telle que [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), n’a pas encore été appelée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERREUR \_ Internet \_ not \_ proxy \_**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



La demande ne peut pas être effectuée via un proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERREUR de l' \_ \_ opération Internet \_ annulée**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



L’opération a été annulée, généralement parce que le descripteur sur lequel la demande a été exécutée a été fermé avant la fin de l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERREUR \_ Internet \_ \_ non \_ définissable**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



L’option demandée ne peut pas être définie, uniquement interrogée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERREUR \_ Internet \_ hors \_ des \_ Handles**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Aucun autre handle n’a pu être généré pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERREUR \_ Internet \_ poster \_ \_ non \_ sécurisée**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



L’application publie des données sur un serveur qui n’est pas sécurisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERREUR \_ \_ protocole Internet \_ \_ introuvable**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



Le protocole demandé est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERREUR \_ \_ Impossible d' \_ atteindre le serveur proxy Internet \_**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



Impossible d’accéder au serveur proxy désigné.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERREUR \_ de \_ modification du schéma de redirection Internet \_ \_**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



La fonction n’a pas pu gérer la redirection, car le schéma a changé (par exemple, HTTP vers FTP).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERREUR de la \_ \_ valeur de registre Internet \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



Une valeur de registre requise n’a pas pu être localisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**\_requête Internet \_ \_ en attente d’erreur**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



L’opération requise n’a pas pu aboutir car une ou plusieurs demandes sont en attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_boîte de dialogue erreur Internet de \_ nouvelle tentative \_**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



La boîte de dialogue doit être retentée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERREUR \_ de \_ certificat CN de l’Internet s \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Le nom commun du certificat SSL (champ de nom d’hôte) est incorrect. par exemple, si vous avez entré www.server.com et que le nom commun sur le certificat indique www.different.com.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERREUR \_ Internet \_ sec \_ date du certificat \_ \_ non valide**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



La date de certificat SSL reçue du serveur est incorrecte. Le certificat a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_Erreurs de \_ certificat Internet s \_ \_**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



Le certificat SSL contient des erreurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERREUR \_ Internet \_ s \_ CERT \_ no \_ Rev**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



Le certificat SSL n’a pas été révoqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERREUR \_ Internet \_ seconde le \_ certificat \_ Rev \_ a échoué**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Échec de la révocation du certificat SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERREUR \_ Internet \_ sec \_ certificat \_ révoqué**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Le certificat SSL a été révoqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERREUR \_ Internet \_ s \_ certificat non valide \_**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Le certificat SSL n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**erreur \_ de \_ canal de sécurité Internet \_ \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



L’application a rencontré une erreur interne lors du chargement des bibliothèques SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERREUR \_ \_ serveur Internet \_ inaccessible**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



Le site Web ou le serveur indiqué est inaccessible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERREUR \_ d' \_ arrêt Internet**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



La prise en charge de WinINet est en cours d’arrêt ou de déchargement.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERREUR \_ Internet \_ tcpip \_ non \_ installée**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



La pile de protocoles requise n’est pas chargée et l’application ne peut pas démarrer WinSock.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERREUR \_ \_ d’expiration Internet**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Le délai d'attente de la requête a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERREUR \_ Internet \_ Impossible \_ de mettre \_ en cache le \_ fichier**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



La fonction n’a pas pu mettre en cache le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERREUR \_ Internet \_ Impossible \_ de \_ Télécharger le \_ script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Impossible de télécharger le script de configuration automatique du proxy. L’indicateur \_ de \_ demande de cache Internet doit être \_ \_ défini.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERREUR \_ de \_ schéma non reconnu Internet \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



Le schéma d’URL n’a pas pu être reconnu ou n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**HANDLE d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>



Le handle qui a été passé à l’API a été invalidé ou fermé.

**En-tête :** Déclaré dans Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERREUR \_ plus de \_ données**
</dt> <dd> <dl> <dt>



More data is available.

**En-tête :** Déclaré dans Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERREUR \_ \_ plus aucun \_ fichier**
</dt> <dd> <dl> <dt>



Aucun autre fichier n’a été trouvé.

**En-tête :** Déclaré dans Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERREUR \_ aucun \_ autre \_ élément**
</dt> <dd> <dl> <dt>



Aucun autre élément n’a été trouvé.

**En-tête :** Déclaré dans Winerror. h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

