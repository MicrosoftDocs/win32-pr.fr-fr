---
title: Indicateurs d’option (Wininet. h)
description: Les indicateurs d’option suivants sont utilisés avec les fonctions InternetQueryOption et InternetSetOption. Tous les indicateurs d’option valides ont une valeur supérieure ou égale à INTERNET \_ First \_ option et sont inférieures ou égales à Internet \_ Last \_ option.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516104"
---
# <a name="option-flags-winineth"></a>Indicateurs d’option (Wininet. h)

Les indicateurs d’option suivants sont utilisés avec les fonctions [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) . Tous les indicateurs d’option valides ont une valeur supérieure ou égale à **Internet \_ First \_ option** et sont inférieures ou égales à **Internet \_ Last \_ option**.

<dl> <dt>

<span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**\_option Internet \_ ALTER \_ Identity**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Non implémenté


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**\_option Internet \_ Async**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ ID Async de l’option Internet \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_option Internet \_ \_ priorité asynchrone**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**\_option Internet \_ Ignorer \_ l' \_ entrée modifiée**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Définit ou récupère la valeur booléenne qui détermine si le système doit vérifier si le réseau dispose d’un contenu plus récent et remplacer les entrées du cache modifiées si une version plus récente est trouvée. Si la valeur est **true**, le système vérifie que le contenu du réseau est plus récent et remplace l’entrée de cache modifiée par la version plus récente. La valeur par défaut est **false**, ce qui indique que l’entrée de cache modifiée doit être utilisée sans vérification du réseau. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Elle est valide uniquement dans Microsoft Internet Explorer 5 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**\_ \_ \_ descripteur du flux de cache des options Internet \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



N'est plus pris en charge.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**\_ \_ horodateurs du cache des options Internet \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Récupère une structure [**d' \_ \_ horodateurs de cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) qui contient l’heure de la LastModified et l’heure d’expiration de la ressource stockée dans le cache Internet. Cette valeur est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**\_rappel d’option Internet \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Définit ou récupère l’adresse de la fonction de rappel définie pour ce handle. Cette option peut être utilisée sur tous les descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) . Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_filtre de \_ rappel d’option Internet \_**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_contexte de \_ \_ certificat client \_ de l’option Internet**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Cet indicateur n’est pas pris en charge par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Le paramètre *lpBuffer* doit être un pointeur vers une structure de [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) et non un pointeur vers un pointeur de **\_ contexte de certificat** . Si une application reçoit un certificat d' **\_ authentification de \_ client Internet \_ \_ \_ requis**, elle doit appeler [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ou utiliser [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pour fournir un certificat avant de retenter la demande. [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) est ensuite appelé afin que le contexte de certificat passé puisse être libéré indépendamment par l’application.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**page de codes de l' \_ option Internet \_**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Par défaut, la partie hôte ou autorité de l’URL Unicode est encodée en fonction de la spécification IDN. Si vous définissez cette option sur la demande, ou sur le descripteur de connexion, lorsque l’IDN est désactivé, spécifie un schéma d’encodage de page de codes pour la partie hôte de l’URL. Le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contient la page de codes DBCS souhaitée. Si aucune page de codes n’est spécifiée dans *lpBuffer*, Wininet utilise la page de codes système par défaut (CP \_ ACP). Remarque : cette option est ignorée si l’IDN n’est pas désactivé. Pour plus d’informations sur la désactivation de l’IDN, consultez l’option **Internet \_ \_ IDN** .

**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.

**Version :** Nécessite Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**chemin de la page de codes de l' \_ option Internet \_ \_**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Par défaut, la partie chemin d’accès de l’URL est encodée en UTF8. L’API WinINet exécute un caractère d’échappement (%) encodage sur les caractères étendus. La définition de cette option sur la demande, ou le descripteur de connexion, désactive l’encodage UTF8 et définit une page de codes spécifique. Le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contient la page de codes DBCS souhaitée pour le chemin d’accès. Si aucune page de codes n’est spécifiée dans *lpBuffer*, Wininet utilise la valeur par défaut de CP \_ UTF8.

**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.

**Version :** Nécessite Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**page de codes de l' \_ option Internet \_ \_ extra**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Par défaut, la partie chemin d’accès de l’URL est la page de codes système par défaut (CP \_ ACP). Caractère d’échappement (%) les conversions ne sont pas effectuées sur la partie supplémentaire. La définition de cette option sur la demande ou sur le descripteur de connexion désactive le \_ codage ACP ACP. Le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contient la page de codes DBCS souhaitée pour la partie supplémentaire de l’URL. Si aucune page de codes n’est spécifiée dans *lpBuffer*, Wininet utilise la page de codes système par défaut (CP \_ ACP).

**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.

**Version :** Nécessite Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_longueur du \_ \_ contenu compressé des options \_ Internet** 
</dt> <dd> <dl> <dt>

147
</dt> <dt>



Pour une demande dans laquelle WinInet décompresse l’encodage de contenu fourni par le serveur, récupère la longueur de contenu signalée par le serveur du corps de la réponse en tant que ULONGLONG. Pris en charge dans Windows 10, version 1507 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_option Internet \_ connexion-interruption \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**\_ \_ nouvelles tentatives de connexion des options Internet \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient le nombre de fois que WinINet tente de résoudre et de se connecter à un hôte. Elle tente une seule fois par adresse IP. Par exemple, si vous tentez de vous connecter à un hôte à hébergement multiple qui possède dix adresses IP et que \_ les nouvelles tentatives de connexion d’option Internet ont \_ \_ la valeur 7, Wininet tente uniquement de résoudre les sept premières adresses IP et de s’y connecter. À l’inverse, étant donné le même ensemble de dix adresses IP, si l' \_ option Internet \_ Connect \_ tentativess est définie sur 20, Wininet tente chacune des dix une seule fois. Si un ordinateur hôte n’a qu’une seule adresse IP et que la première tentative de connexion échoue, il n’y a pas d’autres tentatives. Si une tentative de connexion échoue encore après le nombre de tentatives spécifié, la demande est annulée. La valeur par défaut pour \_ les \_ nouvelles tentatives de connexion des options Internet est de \_ cinq tentatives. Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** . Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**heure de connexion de l' \_ option Internet \_ \_**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_ \_ délai d’attente de connexion des options Internet \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, à utiliser pour les demandes de connexion Internet. La définition de cette option sur Infinite (0xFFFFFFFF) désactive ce minuteur.

Si une demande de connexion prend plus de temps que cette valeur de délai d’attente, la demande est annulée. Lorsque vous tentez de vous connecter à plusieurs adresses IP pour un seul hôte (un hôte multirésident), le délai d’expiration est cumulatif pour toutes les adresses IP. Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** . Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**\_ \_ état connecté de l’option Internet \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient l’état connecté. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**valeur de contexte de l' \_ option Internet \_ \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Définit ou récupère un PTR DWORD \_ qui contient l’adresse de la valeur de contexte associée à ce handle [**HINTERNET**](appendix-a-hinternet-handles.md) . Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) . Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Précédemment, cette valeur définit la valeur de contexte sur l’adresse stockée dans le pointeur **lpBuffer** . Cela a été corrigé afin que la valeur stockée dans la mémoire tampon soit utilisée et que l’indicateur de [ \_ valeur de \_ contexte \_ d’option Internet](/windows) se voit attribuer une nouvelle valeur. L’ancienne valeur, 10, a été conservée afin que les applications écrites pour l’ancien comportement soient toujours prises en charge.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_délai de \_ \_ réception du contrôle \_ d’option Internet**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Identique au [ \_ \_ \_ délai d’attente de réception des options Internet](/windows). Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_ \_ \_ \_ délai d’attente d’envoi du contrôle d’option Internet**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Identique au [ \_ \_ \_ délai d’attente d’envoi des options Internet](/windows). Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_délai de \_ réception des données des options Internet \_ \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour recevoir une réponse à une demande pour le canal de données d’une transaction FTP. Si la réponse prend plus de temps que cette valeur de délai d’attente, la demande est annulée. Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** . Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Cet indicateur n’a aucun impact sur la fonctionnalité HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_ \_ \_ délai d’envoi des données des options Internet \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé, en millisecondes, qui contient la valeur du délai d’attente pour envoyer une demande pour le canal de données d’une transaction FTP. Si l’envoi prend plus de temps que cette valeur de délai d’attente, l’envoi est annulé. Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** . Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Cet indicateur n’a aucun impact sur la fonctionnalité HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**\_nom du \_ fichier de fichier de l’option Internet \_**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Récupère une valeur de chaîne qui contient le nom du fichier qui stocke une entité téléchargée. Cet indicateur est valide après la fin de [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) . Cette option ne peut être interrogée que par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**\_extension du \_ fichier de fichier de l’option Internet \_**
</dt> <dd> <dl> <dt>

96
</dt> <dt>



Définit une valeur de chaîne qui contient l’extension du fichier qui stocke une entité téléchargée. Cet indicateur doit être défini avant d’appeler [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). Cette option peut uniquement être définie par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**\_ \_ \_ informations sur le socket de diagnostic des options Internet \_**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Récupère une structure [**d' \_ \_ \_ informations de socket de diagnostic Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) qui contient les données relatives à une requête http spécifiée. Cet indicateur est utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

**Windows 7 :** Cette option n’est plus prise en charge.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**\_option Internet \_ Digest \_ auth \_ Unload**
</dt> <dd> <dl> <dt>

76
</dt> <dt>



Fait en sorte que le système se déconnecte du package SSPI d’authentification Digest, en vidant toutes les informations d’identification créées pour le processus. Aucune mémoire tampon n’est requise pour cette option. Elle est utilisée par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**\_option Internet \_ désactiver la \_ numérotation automatique**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**\_délai d’attente de l’option Internet \_ déconnectée \_**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**\_option Internet \_ activer \_ le \_ protocole http**
</dt> <dd> <dl> <dt>

148
</dt> <dt>



Définit un masque de réinitialisation DWORD des versions HTTP avancées acceptables. Peut être défini sur n’importe quel type de handle. Les valeurs possibles sont les suivantes :

-   \_ \_ Indicateur de protocole http \_ http2 (0X2). Pris en charge sur Windows 10, version 1507 et versions ultérieures.

Les versions héritées de HTTP (1,1 et versions antérieures) ne peuvent pas être désactivées à l’aide de cette option. La valeur par défaut est 0x0. Pris en charge dans Windows 10, version 1507 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**\_option Internet \_ activer \_ la \_ lecture du cache de redirection \_**
</dt> <dd> <dl> <dt>

122
</dt> <dt>



Sur un handle de demande, définit un booléen qui contrôle si les redirections sont retournées à partir du cache WinInet pour une demande donnée. La valeur par défaut est FALSE. Pris en charge dans Windows 8 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**\_option Internet \_ coder \_ extra**
</dt> <dd> <dl> <dt>

155
</dt> <dt>



Obtient/définit une valeur BOOLÉENNE indiquant si les caractères non-ASCII de la chaîne de requête doivent être encodés en pourcentage. La valeur par défaut est FALSE. Pris en charge dans Windows 8.1 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**\_option Internet \_ fin \_ de \_ session du navigateur**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Vide les entrées qui ne sont pas utilisées à partir du cache de mot de passe sur le disque dur. Réinitialise également le temps de cache utilisé lorsque le mode de synchronisation est une fois par session. Aucune mémoire tampon n’est requise pour cette option. Utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_masque d' \_ erreur des options Internet \_**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Définit une valeur d’entier long non signé qui contient les masques d’erreur qui peuvent être gérés par l’application cliente. Il peut s’agir d’une combinaison des valeurs suivantes :

<dl> <dt>

<span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>\_ \_ \_ \_ certificat sec combiné au masque d’erreurs Internet \_
</dt> <dd>

0x2

Indique que toutes les erreurs de certificat doivent être signalées à l’aide du même retour d’erreur, à savoir les **\_ Erreurs de certificat Error Internet \_ s \_ \_**. Si cet indicateur est défini, appelez **InternetErrorDlg** lors de la réception de l’erreur erreur **\_ Internet \_ s \_ CERT \_** Errors, afin que l’utilisateur puisse répondre à une boîte de dialogue familière décrivant le problème.

> [!Caution]  
> Le fait de ne pas informer l’utilisateur de cette erreur expose l’utilisateur à des attaques d’usurpation d’identité potentielles.

 

</dd> <dt>

<span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>masque d’erreur INTERNET- \_ \_ Insérer un CD- \_ \_ ROM
</dt> <dd>

0x1

Indique que l’application cliente peut gérer le code d’erreur d’insertion dans le **\_ \_ \_ cdrom Internet** .

</dd> <dt>

<span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>échec de connexion au masque d’erreur INTERNET afficher le corps de l' \_ \_ \_ \_ \_ \_ entité \_
</dt> <dd>

0x8

Indique que l’application cliente peut gérer l' **erreur Échec de la connexion Internet afficher le code d’erreur \_ \_ \_ \_ \_ \_ du corps** de l’entité.

</dd> <dt>

<span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>le \_ masque d’erreurs Internet a \_ besoin de \_ \_ MSN \_ SSPI \_ pkg
</dt> <dd>

0x4

Non implémenté.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**\_contexte d' \_ entreprise \_ option Internet**
</dt> <dd> <dl> <dt>

159
</dt> <dt>



Définit un PWSTR contenant l’ID d’entreprise (voir https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) qui s’applique à la demande. Pris en charge dans Windows 10, version 1507 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_ \_ erreur étendue de l’option Internet \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Récupère une valeur d’entier long non signé qui contient un code d’erreur Winsock mappé à l’erreur messages d’erreur **\_ Internet \_** retournés dans ce contexte de thread. Cette option est utilisée sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_option Internet \_ du \_ délai d’expiration du cache \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Définit ou récupère la valeur d’entier long non signé A1N qui contient la durée pendant laquelle le système doit attendre une réponse à une demande réseau avant de vérifier le cache pour une copie de la ressource. Si une requête réseau prend plus de temps que l’heure spécifiée et que la ressource demandée est disponible dans le cache, la ressource est récupérée à partir du cache. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**TYPE de handle de l' \_ option Internet \_ \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Récupère une valeur d’entier long non signé qui contient le type des handles [**HINTERNET**](appendix-a-hinternet-handles.md) passés. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) sur n’importe quel handle [HINTERNET](appendix-a-hinternet-handles.md) . Les valeurs de retour possibles sont les suivantes.

<dl> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>\_type de descripteur Internet \_ \_ connecter \_ FTP
</dt> <dd>

2

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>\_type de descripteur Internet \_ \_ connecter \_ Gopher
</dt> <dd>

3

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>\_type de descripteur Internet \_ \_ Connect \_ http
</dt> <dd>

4

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_demande de \_ fichier de type de handle Internet \_ \_
</dt> <dd>

14

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>\_ \_ fichier FTP de type descripteur Internet \_ \_
</dt> <dd>

7

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>\_type de descripteur Internet \_ \_ \_ fichier FTP \_ HTML
</dt> <dd>

8

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>\_ \_ recherche FTP du type de descripteur Internet \_ \_
</dt> <dd>

5

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>\_type de descripteur Internet \_ \_ FTP \_ Rechercher \_ HTML
</dt> <dd>

6

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>\_type de descripteur Internet- \_ \_ \_ fichier Gopher
</dt> <dd>

11

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>\_type de descripteur Internet du \_ \_ \_ fichier Gopher \_ HTML
</dt> <dd>

12

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>\_ \_ recherche Gopher du type de descripteur Internet \_ \_
</dt> <dd>

9

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>\_type de descripteur Internet \_ \_ Gopher \_ Rechercher \_ HTML
</dt> <dd>

10

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ requête HTTP de type descripteur Internet \_ \_
</dt> <dd>

13

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>\_type de descripteur Internet \_ \_ Internet
</dt> <dd>

1

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**\_option Internet \_ HSTS**
</dt> <dd> <dl> <dt>

157
</dt> <dt>



Obtient/définit une valeur BOOLÉENNE qui indique si WinInet doit suivre les directives HSTS (HTTP strict transport Security) des serveurs. Si cette option est activée, les demandes de https://mises en cache pour les domaines qui ont une stratégie HSTS mise en cache par WinInet sont redirigées vers les URL https://correspondantes. La valeur par défaut est FALSE. Pris en charge dans Windows 8.1 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**\_décodage http des options Internet \_ \_**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Permet à WinINet d’effectuer le décodage pour les schémas d’encodage gzip et deflate. Pour plus d’informations, consultez [**encodage du contenu**](content-encoding.md).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**\_option Internet \_ \_ protocole http \_ utilisée**
</dt> <dd> <dl> <dt>

149
</dt> <dt>



Obtient une valeur DWORD qui indique quelle version HTTP avancée a été utilisée sur une demande donnée. Les valeurs possibles sont les suivantes :

-   \_ \_ Indicateur de protocole http \_ http2 (0X2). Pris en charge sur Windows 10, version 1507 et versions ultérieures.

0x0 indique HTTP/1.1 ou une version antérieure ; consultez \_ la version http de l’option Internet \_ si une \_ plus grande précision est nécessaire pour déterminer quelle version héritée a été utilisée. Pris en charge sur Windows 10, version 1507 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**\_ \_ version http de l’option Internet \_**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Définit ou récupère une structure [**d' \_ \_ informations de version http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) qui contient la version http prise en charge. Elle doit être utilisée sur un handle **null** . Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Sur Windows 7, Windows Server 2008 R2 et versions ultérieures, la valeur du membre **dwMinorVersion** dans la structure info de la [**\_ version \_ http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) est remplacée par les paramètres d’Internet Explorer. **EnableHttp1 \_ 1** est une valeur de Registre sous **HKLM \\ Software \\ Microsoft \\ InternetExplorer \\ AdvacnedOptions \\ http \\ GENABLE** contrôlé par les options Internet définies dans Internet Explorer pour le système. La valeur **EnableHttp1 \_ 1** est définie par défaut sur 1. La structure des **\_ \_ informations de version http** est ignorée pour toute VERSION http inférieure à 1,1 si **EnableHttp1 \_ 1** est défini sur 1.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**identité de l' \_ option Internet \_**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**\_ \_ état inactif des options Internet \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**\_IDN des options Internet \_**
</dt> <dd> <dl> <dt>

102
</dt> <dt>



Par défaut, la partie hôte ou autorité de l’URL est encodée en fonction de la spécification IDN pour les connexions directes et par proxy. Cette option peut être utilisée sur la demande ou sur le descripteur de connexion pour activer ou désactiver les IDN. Lorsque l’IDN est désactivé, WinINet utilise la page de codes du système pour encoder la partie hôte ou autorité de l’URL. Pour désactiver la conversion de l’hôte IDN, définissez le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) sur zéro. Pour activer la conversion d’IDN uniquement sur la connexion directe, spécifiez les **\_ indicateurs Internet \_ IDN \_ directs** dans le paramètre *lpBuffer* de l’appel à **InternetSetOption**. Pour activer la conversion IDN uniquement sur la connexion proxy, spécifiez le **\_ proxy d’indicateur Internet \_ \_ IDN** dans le paramètre *lpBuffer* de l’appel à **InternetSetOption**.

**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.

**Version :** Nécessite Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**\_option Internet \_ Ignorer \_ hors connexion**
</dt> <dd> <dl> <dt>

77
</dt> <dt>



Définit ou récupère une valeur indiquant si l’indicateur global Offline doit être ignoré pour le handle de requête spécifié. Aucune mémoire tampon n’est requise pour cette option. Cela est utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) avec un handle de demande. Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**\_option Internet \_ conserver la \_ connexion**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_ \_ \_ délai d’attente d’écoute des options Internet**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**\_Option Internet \_ Max \_ Conns \_ par \_ \_ serveur 1 0 \_**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur HTTP/1.0. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**\_option Internet \_ Max \_ Conns \_ par \_ proxy**
</dt> <dd> <dl> <dt>

103
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par proxy CERN. Lorsque cette option est définie ou récupérée, le paramètre *hInternet* doit être défini sur une valeur de handle **null** . Une valeur de handle **null** indique que l’option doit être définie ou interrogée pour le processus actuel. Lors de l’appel de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) avec cette option, tous les objets proxy existants recevront la nouvelle valeur. Cette valeur est limitée à une plage comprise entre 2 et 128 inclus.

**Version :** Nécessite Internet Explorer 8,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**\_option Internet \_ Max \_ Conns \_ par \_ serveur**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**\_option Internet \_ \_ en mode hors connexion**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ sémantiques hors connexion des options Internet \_**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_option Internet \_ OPT \_ dans \_ une \_ signature faible**
</dt> <dd> <dl> <dt>

176
</dt> <dt>



Abonnez-vous à des signatures faibles (par exemple, SHA-1) pour qu’elles soient considérées comme non sécurisées. Cela indique à WinInet d’appeler [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) à l’aide de la **\_ chaîne \_ de certificats opt dans le paramètre \_ de \_ \_ signature faible** .


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ handle parent de l’option Internet \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Récupère le handle parent de ce handle. Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**\_ \_ mot de passe de l’option Internet**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Définit ou récupère une valeur de chaîne qui contient le mot de passe associé à un handle retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**option \_ Internet \_ par \_ option de connexion \_**
</dt> <dd> <dl> <dt>

75
</dt> <dt>



Définit ou récupère une structure de liste d’options [**Internet \_ par \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) qui spécifie une liste d’options pour une connexion particulière. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.

> [!Note]  
> **Internet \_ Option \_ per \_ Connection \_** entraîne la modification des paramètres à l’échelle du système lorsqu’un descripteur **null** est utilisé dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Pour actualiser les paramètres de proxy globaux, vous devez appeler **InternetSetOption** avec l’indicateur option d’actualisation de l' **\_ option \_ Internet** .

 

> [!Note]  
> Pour modifier les informations de proxy pour l’ensemble du processus sans affecter les paramètres globaux dans Internet Explorer 5 et versions ultérieures, utilisez cette option sur le descripteur renvoyé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). L’exemple de code suivant modifie le proxy pour l’ensemble du processus, même si le handle [**HINTERNET**](appendix-a-hinternet-handles.md) est fermé et n’est utilisé par aucune demande.

 

Pour plus d’informations et d’exemples de code, consultez [l’article 226473](https://support.microsoft.com/kb/226473)de la base de connaissances.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_stratégie d’option Internet \_**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_proxy d’option Internet \_**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Définit ou récupère une structure [**d' \_ \_ informations de proxy Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) qui contient les données de proxy pour un handle [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) existant lorsque le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) n’a pas la **valeur null**. Si le handle [**HINTERNET**](appendix-a-hinternet-handles.md) a la **valeur null**, la fonction définit ou interroge les données de proxy globales. Cette option peut être utilisée sur le handle retourné par **InternetOpen**. Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

> [!Note]  
> Il est recommandé \_ d’utiliser l’option option Internet \_ par \_ connexion à la place de l’option \_ Internet \_ \_ proxy. Pour plus d’informations, consultez [l’article 226473](https://support.microsoft.com/kb/226473)de la base de connaissances.

 


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_ \_ mot de passe du proxy de l’option Internet \_**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Définit ou récupère une valeur de chaîne qui contient le mot de passe utilisé pour accéder au proxy. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Cette option peut être définie sur le descripteur renvoyé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**paramètres de proxy de l' \_ option Internet \_ \_ \_ modifiés**
</dt> <dd> <dl> <dt>

95 
</dt> <dt>



Alerte l’instance WinInet actuelle que les paramètres de proxy ont changé et qu’ils doivent mettre à jour avec les nouveaux paramètres. Pour alerter toutes les instances WinInet disponibles, définissez le paramètre *buffer* de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) sur **null** et *BufferLength* sur 0 lors du passage de cette option. Cette option peut être définie sur le descripteur renvoyé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_ \_ \_ nom d’utilisateur du proxy de l’option Internet**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Définit ou récupère une valeur de chaîne qui contient le nom d’utilisateur utilisé pour accéder au proxy. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Cette option peut être définie sur le descripteur renvoyé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon de lecture des options Internet \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la taille de la mémoire tampon de lecture. Cette option peut être utilisée sur les handles [**HINTERNET**](appendix-a-hinternet-handles.md) retournés par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)et [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (session FTP uniquement). Cette option est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**\_débit de \_ réception des options Internet \_**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_délai de \_ réception des options Internet \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour recevoir une réponse à une demande. Si la réponse prend plus de temps que cette valeur de délai d’attente, la demande est annulée. Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** . Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Cette option n’est pas destinée à représenter un délai d’expiration immédiat et précis. Vous pouvez vous attendre à ce que le délai d’attente se produise jusqu’à six secondes après la valeur définie pour Timeout.

Lorsqu’elle est utilisée en référence à une transaction FTP, cette option fait référence au canal de contrôle.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**\_actualisation des options Internet \_**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Entraîne la relecture des données du proxy à partir du Registre pour un descripteur. Aucune mémoire tampon n’est requise. Cette option peut être utilisée sur le handle [**HINTERNET**](appendix-a-hinternet-handles.md) retourné par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Elle est utilisée par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**\_option Internet \_ Supprimer l' \_ identité**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_indicateurs de \_ demande d’option Internet \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Récupère une valeur d’entier long non signé qui contient les indicateurs d’État spéciaux qui indiquent l’état du téléchargement en cours. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). L’option d' [ \_ indicateurs de \_ demande \_ d’option Internet](/windows) peut prendre l’une des valeurs suivantes :

<dl> <dt>

<span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET \_ REQFLAG \_ Async
</dt> <dd>

0x00000002

Non implémenté.

</dd> <dt>

<span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>\_ \_ écriture du cache Internet REQFLAG \_ \_ désactivée
</dt> <dd>

0x00000040

La demande Internet ne peut pas être mise en cache (une requête HTTPs, par exemple).

</dd> <dt>

<span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET \_ REQFLAG \_ à partir du \_ cache
</dt> <dd>

0x00000001

La réponse provient du cache.

</dd> <dt>

<span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>\_ \_ \_ délai d’expiration réseau Internet REQFLAG
</dt> <dd>

0x00000080

Délai d’attente de la demande Internet dépassé.

</dd> <dt>

<span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET \_ REQFLAG \_ aucun \_ en-tête
</dt> <dd>

0x00000008

La réponse d’origine ne contenait aucun en-tête.

</dd> <dt>

<span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET \_ REQFLAG \_ passif
</dt> <dd>

0x00000010

Non implémenté.

</dd> <dt>

<span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET \_ REQFLAG \_ via le \_ proxy
</dt> <dd>

0x00000004

La demande a été effectuée via un proxy.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**priorité de la \_ demande d’option Internet \_ \_**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la priorité des demandes qui sont en concurrence pour une connexion sur un handle HTTP. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_option Internet \_ Réinitialiser \_ la \_ session URLCACHE**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Démarre une nouvelle session de cache pour le processus. Aucune mémoire tampon n’est requise. Utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Cette option est réservée à un usage interne uniquement.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_clé de \_ \_ cache secondaire \_ de l’option Internet**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Définit ou récupère une valeur de chaîne qui contient la clé de cache secondaire. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Cette option est réservée à un usage interne uniquement.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**certificat de sécurité de l' \_ option Internet \_ \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Récupère le certificat pour un serveur de technologie de communications SSL/PCT (SSL (Secure Sockets Layer)/Private) dans une chaîne formatée. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_structure de \_ certificat de sécurité \_ \_ de l’option Internet**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Récupère le certificat pour un serveur SSL/PCT dans la structure des \_ informations de certificat Internet \_ . Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**indicateurs de sécurité de l' \_ option Internet \_ \_**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Récupère une valeur d’entier long non signé qui contient les indicateurs de sécurité d’un handle. Cette option est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Il peut s’agir d’une combinaison des valeurs suivantes.

<dl> <dt>

<span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>Indicateur de sécurité \_ \_ 128 bits
</dt> <dd>

0x20000000

Identique à la valeur par défaut intensité de l' [indicateur de sécurité \_ \_ \_ forte](/windows). Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>Indicateur de sécurité \_ \_ 40BIT
</dt> <dd>

0x10000000

Identique à la valeur préférée [force de l’indicateur de sécurité \_ \_ \_ faible](/windows). Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>Indicateur de sécurité \_ \_ 56BIT
</dt> <dd>

0x40000000

Identique au niveau de performance de l’indicateur de sécurité de valeur par défaut. [ \_ \_ \_ ](/windows) Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>indicateur de sécurité \_ \_ Fortezza
</dt> <dd>

0x08000000

Indique que Fortezza a été utilisé pour assurer le secret, l’authentification et/ou l’intégrité de la connexion spécifiée.

</dd> <dt>

<span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>Indicateur de sécurité \_ \_ IETFSSL4
</dt> <dd>

0x00000020

Non implémenté.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>indicateur de sécurité ignorer le nom \_ \_ commun du \_ certificat \_ \_ non valide
</dt> <dd>

0x00001000

Ignore le message d’erreur erreur [ \_ \_ \_ \_ \_ non valide du certificat d’Internet s](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>indicateur de sécurité \_ \_ ignore la \_ Date de certificat \_ \_ non valide
</dt> <dd>

0x00002000

Ignore le message d’erreur [erreur \_ Internet \_ s \_ CERT \_ date \_ non valide](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_indicateur \_ de sécurité ignorer \_ la redirection \_ vers \_ http
</dt> <dd>

0x00008000

Ignore l' [erreur \_ Internet \_ https \_ à \_ http \_ sur le message d’erreur de \_ ReDim](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_indicateur \_ de sécurité ignorer \_ la redirection \_ vers \_ https
</dt> <dd>

0x00004000

Ignore l' [erreur \_ Internet \_ http \_ à \_ https \_ sur le message d’erreur de \_ ReDim](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>indicateur de sécurité \_ \_ ignore la \_ révocation
</dt> <dd>

0x00000080

Ignore les problèmes de révocation de certificat.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>indicateur de sécurité \_ \_ ignorer l’autorité de \_ \_ certification inconnue
</dt> <dd>

0x00000100

Ignore les problèmes d’autorité de certification inconnus.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>indicateur de sécurité \_ \_ ignorer la \_ \_ signature faible
</dt> <dd>

0x00010000

Ignore les problèmes de signature de certificat faible.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>indicateur de sécurité \_ \_ ignorant \_ l’utilisation incorrecte \_
</dt> <dd>

0x00000200

Ignore les problèmes d’utilisation incorrects.

</dd> <dt>

<span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>indicateur de sécurité \_ \_ NORMALBITNESS
</dt> <dd>

0x10000000

Identique à la valeur [ \_ \_ \_ faible force](/windows)de l’indicateur de sécurité. Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>indicateur de sécurité \_ \_ PCT
</dt> <dd>

0x00000008

Non implémenté.

</dd> <dt>

<span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>Indicateur de sécurité \_ \_ PCT4
</dt> <dd>

0x00000010

Non implémenté.

</dd> <dt>

<span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>indicateur de sécurité \_ \_ sécurisé
</dt> <dd>

0x00000001

Utilise des transferts sécurisés. Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>indicateur de sécurité \_ \_ SSL
</dt> <dd>

0x00000002

Non implémenté.

</dd> <dt>

<span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>Indicateur de sécurité \_ \_ SSL3
</dt> <dd>

0x00000004

Non implémenté.

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>niveau de force de l’indicateur de sécurité \_ \_ \_
</dt> <dd>

0x40000000

Utilise le chiffrement moyen (56 bits). Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>force de l’indicateur de sécurité \_ \_ \_ Strong
</dt> <dd>

0x20000000

Utilise le chiffrement fort (128 bits). Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>force de l’indicateur de sécurité \_ \_ \_ faible
</dt> <dd>

0x10000000

Utilise un chiffrement faible (40 bits). Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>indicateur de sécurité \_ \_ UNKNOWNBIT
</dt> <dd>

0x80000000

La taille en bits utilisée dans le chiffrement est inconnue. Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> </dl>

Sachez que les données récupérées de cette façon sont liées à une transaction qui s’est produite, dont le niveau de sécurité ne peut plus être modifié.

</dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**nombre de bits de la clé de sécurité de l' \_ option Internet \_ \_ \_**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Récupère une valeur d’entier long non signé qui contient la taille en bits de la clé de chiffrement. Plus le nombre est élevé, plus la force de chiffrement utilisée est élevée. Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Sachez que les données récupérées de cette façon sont liées à une transaction qui s’est déjà produite, dont le niveau de sécurité ne peut plus être modifié.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_débit d' \_ envoi des options Internet \_**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_ \_ \_ délai d’attente d’envoi des options Internet**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé, en millisecondes, qui contient la valeur du délai d’attente pour envoyer une demande. Si l’envoi prend plus de temps que cette valeur de délai d’attente, l’envoi est annulé. Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** . Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Lorsqu’elle est utilisée en référence à une transaction FTP, cette option fait référence au canal de contrôle.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**\_contexte de \_ chaîne du certificat du serveur d’options Internet \_ \_ \_**
</dt> <dd> <dl> <dt>

105
</dt> <dt>



Récupère le contexte de la chaîne de certificats du serveur en tant que [ \_ \_ contexte de chaîne PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)en double. Vous pouvez passer ce contexte dupliqué à toute fonction API de chiffrement qui prend [un \_ \_ contexte de chaîne PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context). Vous devez appeler [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) sur le [contexte de \_ chaîne \_ PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) retourné lorsque vous avez terminé avec le contexte de la chaîne de certificats.

**Version :** Nécessite Internet Explorer 8,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**\_paramètres d’option Internet \_ \_ modifiés**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Informe le système que les paramètres du Registre ont été modifiés afin qu’il vérifie les paramètres lors de l’appel suivant à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_option Internet \_ supprimer \_ l' \_ authentification du serveur**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Définit un objet de requête HTTP de sorte qu’il ne se connecte pas aux serveurs d’origine, mais effectue une ouverture de session automatique sur les serveurs proxy HTTP. Cette option diffère de l’indicateur de requête **Internet \_ Flag \_ no \_ auth**, qui empêche l’authentification aux serveurs proxy et aux serveurs d’origine.

En définissant ce mode, vous supprimez l’utilisation de tout document d’informations d’identification (nom d’utilisateur/mot de passe ou certificat SSL client précédemment fourni) lors de la communication avec un serveur d’origine. Toutefois, si la demande doit transiter via un proxy d’authentification, WinINet effectue toujours l’authentification automatique sur le proxy HTTP en fonction des paramètres de la zone Intranet de l’utilisateur. Le paramètre de zone Intranet par défaut permet d’autoriser l’ouverture de session automatique à l’aide des informations d’identification par défaut de l’utilisateur.

Pour garantir la suppression de toutes les informations d’identification, l’appelant doit combiner l' **\_ option Internet option \_ Supprimer l' \_ \_ authentification du serveur** avec l’indicateur de requête **Internet \_ indicateur \_ aucun \_ cookie** .

Cette option ne peut être définie que sur des objets de requête avant d’être envoyés. Toute tentative de définition de cette option après l’envoi de la demande retourne l' **État d’erreur du \_ \_ \_ handle \_ Internet incorrect**.

Aucune mémoire tampon n’est requise pour cette option. Cela est utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) sur les handles retournés par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uniquement.

**Version :** Nécessite Internet Explorer 8,0 ou une version ultérieure.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**\_comportement de \_ suppression des options Internet \_**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Option à usage général utilisée pour supprimer les comportements à l’échelle du processus. Le paramètre *lpBuffer* de la fonction doit être un pointeur vers une valeur DWORD contenant le comportement spécifique à supprimer. Cette option ne peut pas être interrogée avec [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Les valeurs autorisées sont les suivantes :

<dl> <dt>

<span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>\_suppression Internet \_ Réinitialiser \_ tout
</dt> <dd>

0

Désactive toutes les suppressions, réactivation des comportements par défaut et configurés. Cette option est équivalente à la configuration de la **\_ \_ \_ \_ réinitialisation** de la stratégie de cookies par Internet et à la **\_ \_ \_ \_ réinitialisation permanente des cookies Internet** .

**Version :** Nécessite Internet Explorer 6,0 ou une version ultérieure.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>\_stratégie de \_ cookies supprimée par Internet \_ 
</dt> <dd>

1

Ignore toutes les stratégies de cookie configurées et autorise la définition des cookies.

**Version :** Nécessite Internet Explorer 6,0 ou une version ultérieure.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>suppression d’INTERNET \_ Supprimer la \_ stratégie de cookie \_ \_ 
</dt> <dd>

2

Désactive la suppression d' **Internet \_ supprimer \_ la \_ stratégie de cookie** , en autorisant l’évaluation des cookies en fonction de la stratégie de cookie configurée.

**Version :** Nécessite Internet Explorer 6,0 ou une version ultérieure.

</dd> <dt>

<span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> le \_ cookie supprimé par Internet est \_ \_ conservé
</dt> <dd>

3

Supprime la persistance des cookies, même si le serveur les a spécifiés comme persistants.

**Version :** Nécessite Internet Explorer 8,0 ou une version ultérieure.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>\_ \_ \_ réinitialisation permanente des cookies supprimés d’Internet \_
</dt> <dd>

4

Désactive la suppression de **la \_ \_ \_ conservation de cookie Internet** , réactivation de la persistance des cookies. Les cookies précédemment supprimés ne sont pas persistants.

**Version :** Nécessite Internet Explorer 8,0 ou une version ultérieure.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**URL de l' \_ option Internet \_**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Récupère une valeur de chaîne qui contient l’URL complète d’une ressource téléchargée. Si l’URL d’origine contenait des données supplémentaires, telles que des chaînes ou des ancres de recherche, ou si l’appel a été redirigé, l’URL retournée est différente de l’original. Cette option est valide sur les handles [**HINTERNET**](appendix-a-hinternet-handles.md) retournés par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**\_option Internet \_ \_ agent utilisateur**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Définit ou récupère la chaîne de l’agent utilisateur sur les handles fournis par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) et utilisés dans les fonctions [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) suivantes, à condition qu’elles ne soient pas remplacées par un en-tête ajouté par [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) ou [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**\_ \_ nom d’utilisateur de l’option Internet**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Définit ou récupère une chaîne qui contient le nom d’utilisateur associé à un handle retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**VERSION de l' \_ option Internet \_**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Récupère une structure **d' \_ \_ informations de version Internet** qui contient le numéro de version de Wininet.dll. Cette option peut être utilisée sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon d’écriture des options Internet \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la taille, en octets, de la mémoire tampon d’écriture. Cette option peut être utilisée sur les handles [**HINTERNET**](appendix-a-hinternet-handles.md) retournés par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (session FTP uniquement). Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                   |
| En-tête<br/>                   | <dl> <dt>Wininet. h ; </dt> <dt>Winineti. h</dt> </dl> |



 

