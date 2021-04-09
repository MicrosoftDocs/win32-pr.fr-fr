---
description: Les valeurs d’erreur identifiées dans cette rubrique sont retournées par GetLastError en cas d’échec de l’une des fonctions des services HTTP Microsoft Windows (WinHTTP).
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Messages d’erreur (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866233"
---
# <a name="error-messages-winhttph"></a>Messages d’erreur (WinHTTP. h)

Les valeurs d’erreur répertoriées ci-dessous sont retournées par [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque l’une des fonctions des services http Microsoft Windows (WinHTTP) échoue, et elles sont également retournées dans les 16 bits d’erreur de [**HRESULT**](../com/structure-of-com-error-codes.md) inférieurs renvoyés par l’objet [**WinHttpRequest**](winhttprequest.md) .

Les valeurs d’erreur dont les noms commencent par « erreur \_ WinHTTP \_ » sont spécifiques aux fonctions WinHTTP. Les fonctions WinHTTP retournent également des messages d’erreur Windows, le cas échéant.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERREUR \_ de \_ \_ service de proxy automatique \_ WinHTTP \_**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Retourné par [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) lorsqu’un proxy pour l’URL spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERREUR lors de la \_ détection automatique WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Retourné par [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) si WinHTTP n’a pas pu découvrir l’URL du fichier de configuration automatique de proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERREUR \_ WinHTTP \_ \_ script de \_ proxy \_ automatique incorrect**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Une erreur s’est produite lors de l’exécution du code de script dans le fichier de configuration automatique de proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ après l' \_ ouverture**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une option spécifiée ne peut pas être demandée après l’appel de la méthode [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ après l' \_ envoi**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une opération demandée ne peut pas être effectuée après l’appel de la méthode [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ avant l' \_ ouverture**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une opération demandée ne peut pas être exécutée avant d’appeler la méthode [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ avant \_ Send**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une opération demandée ne peut pas être exécutée avant d’appeler la méthode [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ se connecter**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Retourné si la connexion au serveur a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERREUR \_ du \_ certificat d’authentification du client WinHTTP \_ \_ \_ nécessaire**
</dt> <dd> <dl> <dt>



Le serveur requiert l’authentification du client SSL. L’application récupère la liste des émetteurs de certificats en appelant [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) à l’aide de l’option **WinHTTP \_ \_ \_ \_ \_ liste d’émetteurs** de certificats client. Pour plus d’informations, consultez l’option **WinHTTP \_ \_ liste d' \_ \_ émetteurs \_ de certificats client** .

Si le serveur demande le certificat client, mais ne l’exige pas, l’application peut également appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l’option **WinHTTP \_ \_ \_ \_ contexte CERT client** . Dans ce cas, l’application spécifie la \_ \_ macro de contexte de certificat non client WinHTTP \_ \_ dans le paramètre *lpBuffer* de **WinHttpSetOption**. Pour plus d’informations, consultez l’option de **\_ \_ \_ \_ contexte certificat du client de l’option WinHTTP** .

**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERREUR \_ de \_ certificat client WinHTTP \_ \_ aucune \_ \_ clé privée d’accès \_**
</dt> <dd> <dl> <dt>



L’application ne dispose pas des privilèges nécessaires pour accéder à la clé privée associée au certificat client.

**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERREUR \_ de \_ certificat client WinHTTP \_ \_ sans \_ \_ clé privée**
</dt> <dd> <dl> <dt>



Aucune clé privée n’est associée au contexte du certificat client SSL. Le certificat client a peut-être été importé sur l’ordinateur sans la clé privée.

**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERREUR \_ WinHTTP \_ dépassement de \_ \_ taille d’en-tête de codage mémorisé en bloc \_ \_**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsqu’une condition de dépassement de capacité se produit au cours de l’analyse du codage mémorisé en bloc.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERREUR \_ du \_ certificat d’authentification du client WinHTTP \_ \_ \_ nécessaire**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsque le serveur demande l’authentification du client.

**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERREUR \_ de \_ connexion \_ WinHTTP erreur**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La connexion avec le serveur a été réinitialisée ou terminée, ou un protocole SSL incompatible a été rencontré. Par exemple, WinHTTP version 5,1 ne prend pas en charge SSL2, sauf si le client l’active spécifiquement.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**l' \_ \_ en-tête WinHTTP d’erreur \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Périmé n’est plus utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERREUR \_ du \_ nombre d’en-têtes WinHTTP \_ \_ dépassé**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsqu’un plus grand nombre d’en-têtes étaient présents dans une réponse que WinHTTP pouvait recevoir.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERREUR de l' \_ \_ en-tête WinHTTP \_ \_ introuvable**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



L’en-tête demandé est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERREUR \_ de \_ \_ dépassement de taille d’en-tête WinHTTP \_**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsque la taille des en-têtes reçus dépasse la limite du handle de demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERREUR \_ WinHTTP \_ \_ État de handle incorrect \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Impossible d’effectuer l’opération demandée, car le handle fourni n’est pas dans l’état correct.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERREUR \_ WinHTTP \_ \_ type de handle incorrect \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Le type de handle fourni est incorrect pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERREUR \_ WinHTTP \_ interne \_ erreur**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Une erreur interne s'est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERREUR \_ WinHTTP \_ non valide, \_ option**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Une requête à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) A spécifié une valeur d’option non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERREUR \_ WinHTTP requête de \_ requête non valide \_ \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Périmé n’est plus utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERREUR \_ WinHTTP \_ \_ réponse du serveur non valide \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



La réponse du serveur ne peut pas être analysée.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERREUR \_ WinHTTP \_ URL non valide \_**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



L’URL n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERREUR \_ d' \_ échec de connexion WinHTTP \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



La tentative de connexion a échoué. Lorsque cette erreur se produit, le descripteur de demande doit être fermé avec [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). Un nouveau descripteur de demande doit être créé avant de retenter la fonction qui a produit cette erreur à l’origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERREUR \_ de \_ nom WinHTTP \_ non \_ résolue**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Impossible de résoudre le nom du serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERREUR \_ WinHTTP \_ non \_ initialisée**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Périmé n’est plus utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERREUR de l' \_ \_ opération WinHTTP \_ annulée**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



L’opération a été annulée, généralement parce que le descripteur sur lequel la demande a été exécutée a été fermé avant la fin de l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERREUR \_ WinHTTP \_ \_ non \_ définissable**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



L’option demandée ne peut pas être définie, uniquement interrogée.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERREUR \_ WinHTTP \_ hors \_ des \_ Handles**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Périmé n’est plus utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERREUR lors de \_ \_ la redirection WinHTTP \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



La redirection a échoué parce que le schéma a été modifié ou que toutes les tentatives de redirection ont échoué (cinq tentatives par défaut).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERREUR \_ WinHTTP de \_ renvoi de \_ demande**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Échec de la fonction WinHTTP. La fonction souhaitée peut être retentée sur le même handle de demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERREUR de dépassement du drainage de la \_ \_ réponse WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Retourné lorsqu’une réponse entrante dépasse une limite de taille WinHTTP interne.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERREUR \_ d' \_ exécution du script WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Une erreur s’est produite lors de l’exécution d’un script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERREUR \_ WinHTTP \_ \_ \_ non valide du certificat sécurisé \_ WinHTTP**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Retourné lorsqu’un nom de nom commun de certificat ne correspond pas à la valeur transmise (équivalent à une erreur **CERT \_ E \_ CN \_ no \_ match** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERREUR \_ WinHTTP \_ sécurité de \_ certificat sécurisé \_ \_ non valide**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Indique qu’un certificat requis n’est pas dans sa période de validité lors de la vérification par rapport à l’horloge système actuelle ou à l’horodateur du fichier signé, ou que les périodes de validité de la chaîne de certification ne s’imbriquent pas correctement (équivalent à un **certificat \_ e \_ expiré** ou à une erreur de **certificat \_ e \_ VALIDITYPERIODNESTING** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERREUR \_ WinHTTP \_ échec de la \_ révision du certificat sécurisé \_ \_**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Indique que la révocation ne peut pas être vérifiée, car le serveur de révocation était hors connexion (ce qui équivaut à **Crypter \_ E \_ Revocation \_ hors connexion**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERREUR \_ de \_ certificat sécurisé WinHTTP \_ \_ révoqué**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Indique qu’un certificat a été révoqué (ce qui équivaut à **Crypter \_ E \_ révoqué**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERREUR \_ d' \_ \_ \_ utilisation incorrecte du certificat sécurisé WinHTTP \_**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Indique qu’un certificat n’est pas valide pour l’utilisation demandée (équivalent au certificat **\_ E \_ \_ utilisation incorrecte**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**erreur \_ de \_ canal sécurisé WinHTTP \_ \_ erreur**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Indique qu’une erreur s’est produite avec un canal sécurisé (équivalent aux codes d’erreur commençant par « SEC \_ e \_ » et « sec \_ I \_ » figurant dans le fichier d’en-tête « winerror. h »).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERREUR \_ WinHTTP \_ Secure \_ Failure**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Une ou plusieurs erreurs ont été détectées dans le certificat SSL (Secure Sockets Layer) (SSL) envoyé par le serveur. Pour déterminer le type d’erreur rencontré, recherchez une notification de [**\_ \_ \_ \_ défaillance sécurisée d’état de rappel WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) dans une fonction de rappel d’État. Pour plus d’informations, voir [**WinHTTP \_ Status \_ callback**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERREUR \_ WinHTTP \_ sécurisée \_ non valide pour l' \_ autorité de certification**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Indique qu’une chaîne de certificats a été traitée, mais s’est terminée dans un certificat racine qui n’est pas approuvé par le fournisseur d’approbation (équivalent au **CERT \_ E \_ UNTRUSTEDROOT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERREUR \_ WinHTTP \_ sécuriser le \_ certificat non valide \_**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Indique qu’un certificat n’est pas valide (équivalent à des erreurs telles que le **\_ \_ rôle CERT e**, **CERT \_ e \_ PATHLENCONST**, CERT e **\_ \_ Critical**, **CERT \_ e \_ Purpose**, **CERT \_ e \_ ISSUERCHAINING**, **CERT \_ e \_ incorrecte** et le **\_ \_ chaînage e Cert**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERREUR \_ d' \_ arrêt WinHTTP**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



La prise en charge de la fonction WinHTTP est en cours d’arrêt ou de déchargement.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERREUR \_ WinHTTP de \_ dépassement de délai**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Le délai d'attente de la requête a expiré.

Cette erreur peut être retournée à la suite du comportement du délai d’expiration TCP/IP, quelles que soient les valeurs de délai d’attente définies dans les services HTTP Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERREUR \_ WinHTTP \_ Impossible \_ de \_ Télécharger le \_ script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Impossible de télécharger le fichier PAC. Par exemple, le serveur référencé par l’URL PAC n’a peut-être pas été accessible ou le serveur a retourné une réponse 404 introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERREUR \_ de \_ type de script non géré WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Le type de script n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERREUR \_ de \_ schéma WinHTTP non reconnu \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



L’URL a spécifié un schéma autre que « http : » ou « https : ».


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERREUR \_ de \_ mémoire insuffisante \_**
</dt> <dd> <dl> <dt>



Mémoire disponible insuffisante pour terminer l’opération demandée.

**En-tête :** Déclaré dans Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERREUR \_ de \_ mémoire tampon insuffisante**
</dt> <dd> <dl> <dt>



La taille, en octets, de la mémoire tampon fournie à une fonction était insuffisante pour contenir les données retournées. Pour plus d’informations, consultez la fonction spécifique.

**En-tête :** Déclaré dans Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**HANDLE d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>



Le descripteur passé à l’interface de programmation d’applications (API) a été invalidé ou fermé.

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


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERREUR \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>



La pile de protocoles requise n’est pas chargée et l’application ne peut pas démarrer WinSock.

**En-tête :** Déclaré dans Winerror. h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| En-tête<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

