---
Description: Les indicateurs d’option suivants sont pris en charge par WinHttpQueryOption et WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Indicateurs d’option (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395414"
---
# <a name="option-flags"></a>Indicateurs d’option

Les indicateurs d’option suivants sont pris en charge par [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPTION WINHTTP assurée par les \_ \_ \_ \_ rappels non bloquants \_**
</dt> <dd> <dl> <dt>



La valeur par défaut est FALSE. Si la valeur est TRUE, WinHTTP ne garantit pas la progression si les rappels d’État sont bloqués par l’application cliente.

L’application cliente doit être particulièrement prudente pour effectuer des opérations minimales dans le rappel sans blocage, ce qui revient le plus rapidement possible et, en particulier, ne doit pas attendre d’appels WinHTTP ultérieurs. S’il ne suit pas ces instructions, il est probable qu’il y ait un impact négatif sur les performances ou qu’une application potentielle se bloque. Si elle est utilisée de la manière prescrite, cette option peut améliorer les performances.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**stratégie d’accès automatique aux \_ options WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Définit une valeur d’entier long non signé qui spécifie la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md) avec l’une des valeurs suivantes.

| Terme | Description |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>niveau de sécurité de l' \_ AUTOLOGO WINHTTP WinHTTP \_ \_ \_ élevé | Les informations d’identification par défaut ne sont pas utilisées. Notez que cet indicateur prend effet uniquement si vous spécifiez le serveur par le nom de l’ordinateur réel. Elle ne prend pas effet si vous spécifiez le serveur par « localhost » ou par adresse IP. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>niveau de sécurité de l’ouverture de certification WINHTTP \_ \_ \_ \_ bas | Une ouverture de session authentifiée à l’aide des informations d’identification par défaut est effectuée pour toutes les demandes. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>niveau de sécurité de la \_ protection d’accès réseau WinHTTP \_ \_ \_ moyen | Une connexion authentifiée à l’aide des informations d’identification par défaut est exécutée uniquement pour les demandes sur l’intranet local. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**\_connexions en \_ arrière-plan des options WinHTTP \_**
</dt> <dd> <dl> <dt>

Lorsque vous définissez cette option sur un handle de session, vous devez transmettre le nombre de connexions que vous souhaitez ouvrir. Ensuite, lors de la première envoi d’une demande, au lieu d’ouvrir une seule connexion, WinHttp ouvre plusieurs connexions en parallèle. Cela peut améliorer les performances des demandes suivantes adressées à la même destination, ce qui n’entraîne pas la surcharge liée à l’établissement de la connexion.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_rappel d’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère le pointeur vers la fonction de rappel définie avec [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexte de \_ \_ certificat client \_ de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit le contexte du certificat client. Si une application reçoit un certificat d' [**\_ authentification de \_ client WinHTTP \_ \_ \_ nécessaire**](error-messages.md), elle doit appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour fournir un certificat avant de retenter la demande. Dans le cadre du traitement de cette option, WinHttp appelle [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) sur le contexte de certificat fourni par l’appelant afin que le contexte de certificat puisse être libéré indépendamment par l’appelant.

> [!Note]
> L’application ne doit pas tenter de fermer le magasin de certificats avec l’indicateur de fermeture de l' \_ \_ indicateur de fin de magasin de certificats \_ de l' \_ appel à [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) sur le magasin de certificats à partir duquel le contexte de certificat a été récupéré. Une violation d’accès peut se produire.

Lorsque le serveur demande un certificat client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne une erreur message d' [**authentification du \_ \_ client WinHTTP \_ \_ \_ requis**](error-messages.md) . Si le serveur demande le certificat mais n’en a pas besoin, l’application peut spécifier cette option pour indiquer qu’elle n’a pas de certificat. Le serveur peut choisir un autre schéma d’authentification ou autoriser un accès anonyme au serveur. L’application fournit la macro de **contexte de certificat du \_ client WinHTTP no \_ client \_ \_** dans le paramètre *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , comme indiqué dans l’exemple de code suivant.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Si le serveur a besoin d’un certificat client, il peut envoyer un code d’état HTTP 403 en réponse. Pour plus d’informations, consultez l’option **WinHTTP \_ \_ liste d' \_ \_ émetteurs \_ de certificats client** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_option WinHTTP \_ \_ liste d’émetteurs de certificats client \_ \_**
</dt> <dd> <dl> <dt>



Récupère une structure [**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) lorsque l’erreur de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) est un **\_ certificat d' \_ authentification client WinHTTP \_ \_ \_ nécessaire**. La liste d’émetteurs de la structure contient une liste d’autorités de certification (CA) acceptables du serveur. L’application cliente peut filtrer la liste des autorités de certification pour récupérer le certificat client pour l’authentification SSL.

En revanche, si le serveur demande le certificat client, mais ne l’exige pas, l’application peut appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l' **option \_ WinHTTP \_ \_ \_ contexte de certificat client CERT** . Pour plus d’informations, consultez l’option de **\_ \_ \_ \_ contexte certificat du client de l’option WinHTTP** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**page de codes de l' \_ option WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit la [*page de codes*](glossary.md) utilisée pour traiter l’URL (c’est-à-dire, la chaîne de requête). La valeur par défaut est UTF-8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_option WinHTTP \_ configurer \_ l' \_ authentification Passport**
</dt> <dd> <dl> <dt>



Définit une valeur d’entier long non signé qui spécifie si [l’authentification Passport dans](passport-authentication-in-winhttp.md) l’authentification WinHTTP est activée. Il peut s'agir de l'une des valeurs suivantes :

| Terme | Description |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP- \_ désactiver l' \_ \_ authentification Passport | L’authentification Microsoft Passport est désactivée. Il s’agit de la valeur par défaut. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP-désactiver le porte- \_ \_ \_ clés Passport | Le porte-clés Passport est désactivé. Il s’agit de la valeur par défaut. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>activation de WINHTTP avec l' \_ \_ \_ authentification Passport | L’authentification Passport est activée. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP activer le porte- \_ \_ \_ clés Passport | Le porte-clés Passport est activé. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ nouvelles tentatives de connexion de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient le nombre de tentatives de connexion de timesWinHTTP à un hôte. Les services HTTP Microsoft Windows (WinHTTP) ne tentent qu’une seule fois par adresse IP (Internet Protocol). Par exemple, si vous tentez de vous connecter à un hôte multirésident qui a 10 adresses IP et que les **\_ \_ \_ nouvelles tentatives de connexion de l’option WinHTTP** ont la valeur 7, WinHTTP tente uniquement de se connecter aux sept premières adresses IP. Étant donné le même jeu de 10 adresses IP, si l' **\_ option de connexion des \_ \_ nouvelles tentatives WinHTTP** est définie sur 20, WinHTTP tente chacune des 10 une seule fois. Si une tentative de connexion échoue encore après le nombre spécifié de tentatives, ou si le délai de connexion a expiré avant, la demande est annulée. La valeur par défaut pour les **\_ \_ \_ nouvelles tentatives de connexion de l’option WinHTTP** est de cinq tentatives.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**délai de connexion de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes. La définition de cette option sur Infinite (0xFFFFFFFF) désactive ce minuteur.

Si une demande de connexion TCP prend plus de temps que cette valeur de délai d’attente, la demande est annulée. Le délai d’attente par défaut est de 60 secondes. Lorsque vous tentez de vous connecter à plusieurs adresses IP pour un seul hôte (un hôte multirésident), le délai d’expiration est fixé pour chaque connexion individuelle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**informations de connexion de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère l’adresse IP source et de destination, ainsi que le port de la demande qui a généré la réponse quand [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne. L’application appelle [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) avec l’option **WinHTTP \_ option \_ Connection \_ info** , et fournit la structure des [**\_ \_ informations de connexion WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) dans le paramètre *lpBuffer* . Pour plus d’informations, **consultez \_ \_ informations de connexion WinHTTP**.

**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cet indicateur est obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Statistiques de connexion des options WinHTTP \_ \_ \_ v0**
</dt> <dd> <dl> <dt>



Extrait le struct d' [**\_ informations TCP \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) pour la connexion sous-jacente utilisée par la demande. La structure retournée peut contenir des statistiques des requêtes précédentes envoyées sur la même connexion.

> [!Note]
> Cette option a été remplacée par les **statistiques de connexion de l' \_ option WinHTTP \_ \_ \_ v1**.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Statistiques de connexion des options WinHTTP \_ \_ \_ v1**
</dt> <dd> <dl> <dt>



Extrait le struct d' [**\_ informations TCP \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) pour la connexion sous-jacente utilisée par la demande. La structure retournée peut contenir des statistiques des requêtes précédentes envoyées sur la même connexion.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**valeur de contexte de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Définit ou récupère un **\_ ptr DWORD** qui contient un pointeur vers la valeur de contexte associée à ce handle [HINTERNET](hinternet-handles-in-winhttp.md) . La valeur stockée dans la mémoire tampon est utilisée et la nouvelle valeur est assignée à l’indicateur d’option de la valeur de contexte de l' **\_ option \_ \_ WinHTTP** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**décompression des \_ options WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit un DWORD d’indicateurs qui déterminent si WinHTTP décompresse automatiquement les corps de réponse avec les encodages de contenu compressés. WinHTTP définira également un en-tête de Accept-Encoding approprié, en remplaçant tout fourni par l’appelant. Les valeurs prises en charge sont les suivantes :

| Terme | Description |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_indicateur de décompression WinHTTP, \_ \_ gzip | Décompresser Content-Encoding : réponses gzip. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_indicateur de décompression WinHTTP \_ \_ deflate | Décompresser le contenu-encodage : réponses décompressées. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_indicateur de décompression WinHTTP \_ \_ tout | Décompressez les réponses avec tout encodage de contenu pris en charge. |

Par défaut, WinHTTP remet les réponses compressées à l’appelant sans les modifier.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**OPTION WINHTTP- \_ désactiver la génération de \_ \_ chaîne de certificats \_ \_**
</dt> <dd> <dl> <dt>


La définition de cette option sur un handle de session WinHttp vous permet d’activer ou de désactiver la génération de la chaîne de certificats du serveur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_fonctionnalité de \_ désactivation de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit une valeur d’entier long non signé qui spécifie les fonctionnalités qui sont désactivées avec un ou plusieurs des indicateurs suivants. N’oubliez pas que cette fonctionnalité doit être transmise uniquement à [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) sur les handles de requête après la création du handle de demande avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), et avant l’envoi de la demande avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

| Terme | Description |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>\_désactiver \_ l’authentification WinHTTP | L’authentification automatique est désactivée. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>désactivation des \_ \_ cookies WinHTTP | L’ajout automatique d’en-têtes de cookie aux demandes est désactivé. En outre, les cookies retournés ne sont pas automatiquement ajoutés à la base de données de cookies. La désactivation des cookies peut entraîner des performances médiocres pour l’authentification Passport. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_désactiver \_ Keep \_ Alive dans WinHTTP | Désactive la sémantique Keep-Alive pour la connexion. La sémantique Keep-Alive est requise pour MSN, NTLM et d’autres types d’authentification. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>désactivation des \_ \_ redirections WinHTTP | La redirection automatique est désactivée lors de l’envoi de demandes avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Si la redirection automatique est désactivée, une application doit inscrire une fonction de rappel pour que l’authentification Passport aboutisse. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_option WinHTTP \_ désactiver \_ le \_ protocole sécurisé de \_ secours**
</dt> <dd> <dl> <dt>



Empêche WinHTTP de retenter une connexion avec une version antérieure du protocole de sécurité en cas d’échec de la négociation de protocole initiale.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPTION WINHTTP- \_ \_ désactiver la \_ \_ file d’attente de flux**
</dt> <dd> <dl> <dt>



Autorise les nouvelles demandes à ouvrir une connexion HTTP/2 supplémentaire lorsque la limite de flux simultané maximale est atteinte, plutôt que d’attendre le flux disponible suivant sur une connexion existante.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_option WinHTTP \_ activer la \_ fonctionnalité**
</dt> <dd> <dl> <dt>



Définit une valeur d’entier long non signé qui spécifie les fonctionnalités actuellement activées. Il peut s’agir de l’une des valeurs suivantes.

| Terme | Description |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ activer \_ l' \_ emprunt d' \_ identité par le biais de SSL | S’il est activé, WinHTTP rétablit temporairement l’emprunt d’identité du client pendant la durée des opérations d’authentification du certificat SSL. Cette valeur ne peut être définie que sur le descripteur de session. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ activer \_ la \_ révocation SSL | Si cette option est activée, WinHTTP autorise la révocation SSL. Cette valeur peut être définie uniquement sur le handle de demande. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_option WinHTTP \_ activer \_ le \_ protocole http**
</dt> <dd> <dl> <dt>



Définit un masque de réinitialisation DWORD des versions HTTP avancées acceptables. Les valeurs possibles sont les suivantes :

| Terme | Description |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ Indicateur de protocole WinHTTP \_ http2 (0x1) | Active HTTP/2 pour la requête. |
| Aucun (0x0) | Limite la demande à HTTP/1.1 et antérieur. |

Les versions héritées de HTTP (1,1 et versions antérieures) ne peuvent pas être désactivées à l’aide de cette option. La valeur par défaut est 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**\_Option WinHTTP \_ activer \_ le \_ certificat du client http2 plus \_ \_**
</dt> <dd> <dl> <dt>


Cette option peut être définie sur un handle de session WinHttp pour permettre à WinHttp d’utiliser le contexte de certificat client fourni par l’appelant lorsque le protocole HTTP/2 est utilisé.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_option WinHTTP \_ EnableTracing,**
</dt> <dd> <dl> <dt>



Définit une valeur **bool** qui spécifie si le traçage est actuellement activé. Pour plus d’informations sur la fonctionnalité de trace dans WinHTTP, consultez [WinHTTP trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md). Cette option ne peut être définie que sur un handle **HINTERNET** **null** .


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_option WinHTTP \_ coder \_ extra**
</dt> <dd> <dl> <dt>



Active l’encodage de pourcentage d’URL pour le chemin d’accès et la chaîne de requête.

Vous pouvez également encoder en pourcentage avant d’appeler WinHttp.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**expiration de la connexion de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Cette option ne peut être définie que sur un handle de demande qui est toujours actif (envoi ou réception). La définition de cette option indique à WinHttp d’arrêter de servir les demandes sur la connexion associée au handle de demande passé. La connexion sera fermée après le handle de requête. cette option est appelée avec est terminée. Cette option ne prend aucun paramètre.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ erreur étendue de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère une valeur d’entier long non signé qui contient un code d’erreur Microsoft Windows Sockets qui a été mappé à l’erreur \_ WinHTTP \_ \* messages d’erreur retournés dans ce contexte de thread. Vous pouvez passer **null** comme valeur de handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**\_option WinHTTP \_ première \_ \_ connexion disponible**
</dt> <dd> <dl> <dt>


Par défaut, lorsque WinHttp envoie une demande, si aucune connexion n’est disponible pour répondre à la demande, WinHttp tente d’établir une nouvelle connexion et la demande est liée à cette nouvelle connexion. Lorsque vous définissez cette option, une telle demande est traitée à la première connexion qui devient disponible, et pas nécessairement celle qui est établie.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**identification \_ du \_ proxy global des options \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Prend un pointeur vers une structure d' [**\_ CREDS \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) d’identification WinHTTP avec le paramètre de fonction *hInternet* ayant la valeur **null**. Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**. Si cette clé de Registre n’est pas définie, WinHTTP retourne l' **\_ option erreur WinHTTP \_ non valide \_**. Cette clé de Registre n’est pas présente par défaut. Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP. Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet. Pour partager des informations d’identification de serveur en plus des informations d’identification de proxy, les utilisateurs doivent définir l' **\_ option WinHTTP utiliser les \_ \_ \_ \_ informations d’identification du serveur global** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_options WinHTTP \_ - \_ CREDS de serveur global \_**
</dt> <dd> <dl> <dt>



Prend un pointeur vers une structure d' [**\_ CREDS \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) d’identification WinHTTP avec le paramètre de fonction *hInternet* ayant la valeur **null**. Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**. Si cette clé de Registre n’est pas définie, WinHTTP retourne l' **\_ option erreur WinHTTP \_ non valide \_**. Cette clé de Registre n’est pas présente par défaut. Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP. Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet. Pour partager des informations d’identification de serveur en plus des informations d’identification de proxy, les utilisateurs doivent définir l' **\_ option WinHTTP utiliser les \_ \_ \_ \_ informations d’identification du serveur global** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TYPE de handle de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère une valeur d’entier long non signé qui contient le type du handle [HINTERNET](hinternet-handles-in-winhttp.md) passé. La valeur de retour peut être une des suivantes :

| Terme | Description |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_connexion au \_ type de handle WinHTTP \_ | Le descripteur est un handle de connexion. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_demande de \_ type de handle WinHTTP \_ | Le descripteur est un handle de demande. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_session de \_ type de handle WinHTTP \_ | Le descripteur est un handle de session. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_option WinHTTP \_ \_ protocole http \_ requis**
</dt> <dd> <dl> <dt>



Empêche l’utilisation de versions de protocole autres que celles activées par l' **\_ option WinHTTP activer le \_ \_ \_ protocole http** pour la demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_option WinHTTP \_ \_ protocole http \_ utilisé**
</dt> <dd> <dl> <dt>



Obtient une valeur DWORD qui indique quelle version HTTP avancée a été utilisée sur une demande donnée. Pour obtenir la liste des valeurs possibles, **consultez \_ option WinHTTP \_ activer le \_ \_ protocole http**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_ \_ version http de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une structure [**d' \_ \_ informations de version http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) qui contient la version http prise en charge. Il s’agit d’une option à l’ensemble du processus ; Utilisez la **valeur null** pour le descripteur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_Option WinHTTP \_ http2 \_ KeepAlive**
</dt> <dd> <dl> <dt>


Cette option peut être définie sur un handle de session pour que WinHttp utilise des trames PING HTTP/2 comme mécanisme KeepAlive. Les appelants spécifient un délai d’expiration en millisecondes et, après l’absence d’activité sur une connexion pour ce délai, WinHttp commence à envoyer des trames PING HTTP/2. Les appelants ne peuvent pas définir une valeur de délai d’expiration inférieure à 5000 millisecondes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**\_Option WinHTTP \_ http2 \_ plus \_ \_ encodage de transfert**
</dt> <dd> <dl> <dt>


Cette option peut être définie sur un handle de demande WinHttp pour contrôler la façon dont WinHttp se comporte lorsqu’une réponse HTTP/2 contient un en-tête « Transfer-Encoding ». Dans ce cas, WinHttp retourne une erreur si cette option a la valeur **false**.


</dt> </dl> </dd> <dt>


<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_option WinHTTP \_ Ignorer \_ la \_ révocation de certificat \_ hors connexion**
</dt> <dd> <dl> <dt>



Autorise les connexions sécurisées à utiliser des certificats de sécurité pour lesquels la liste de révocation de certificats n’a pas pu être téléchargée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Option WinHTTP \_ \_ Fast \_ Fallback IPv6**
</dt> <dd> <dl> <dt>



Active la connexion Fast de secours IPv6 (les yeux plus heureux) pour la connexion. Ce comportement est similaire au comportement de l’œil heureux décrit dans le [document RFC 6555](https://tools.ietf.org/html/rfc6555) pour améliorer les temps de connexion sur les réseaux où IPv6 n’est pas fiable.
- Si les adresses IPv6 et IPv4 sont résolues pour un hôte donné, WinHttp commence par se connecter à la première adresse IPv6 résolue avec un délai d’expiration court (300 mètres).
- En cas d’échec de cette connexion, WinHttp tente de se connecter à la première adresse IPv4 résolue avec le délai d’attente standard.
- En cas d’échec de la deuxième connexion, WinHttp réessaiera la première adresse IPv6 résolue avec le délai d’expiration standard.
- En cas d’échec de la troisième connexion, WinHttp rétablit le comportement par défaut pour toutes les adresses restantes, en tentant une connexion avec le délai d’expiration standard jusqu’à ce qu’une connexion soit établie ou qu’aucune adresse ne soit conservée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**l' \_ option WinHTTP \_ est une \_ \_ réponse de connexion proxy \_**
</dt> <dd> <dl> <dt>



Obtient une valeur indiquant si une réponse de connexion de retour de proxy peut être récupérée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Option WinHTTP \_ nombre de Conn. \_ \_ par \_ \_ serveur 1 0 \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur HTTP/1.0. La valeur par défaut est **infinite**.

**Windows Vista avec SP1 et Windows Server 2008 :** Cet indicateur est obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_option WinHTTP \_ nombre maximal de \_ conn. \_ par \_ serveur**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur. La valeur par défaut est **infinite**.

Lorsque cette option a la valeur zéro, WinHTTP définit la limite du nombre de connexions à 2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_option WinHTTP \_ nombre maximal de \_ \_ \_ redirections http automatiques**
</dt> <dd> <dl> <dt>



Définit le nombre maximal de redirections que WinHTTP suit ; la valeur par défaut est 10. Cette limite empêche les sites non autorisés de suspendre le client WinHTTP après un grand nombre de redirections.

**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_ \_ État http max de l’option WinHTTP \_ \_ \_ continue**
</dt> <dd> <dl> <dt>



Le nombre maximal de réponses du code d’État 100-199 est ignoré avant de renvoyer le code d’état final au client WinHTTP. Les codes d’État informations 100-199 peuvent être envoyés par le serveur avant le code d’état final et sont décrits dans la spécification pour HTTP/1.1 (pour plus d’informations, consultez [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). La valeur par défaut est de 10.

**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_option WinHTTP \_ taille maximale de \_ \_ drainage \_ de la réponse**
</dt> <dd> <dl> <dt>



Lié sur la quantité de données vidées des réponses afin de réutiliser une connexion, spécifiée en octets. La valeur par défaut est 1 Mo.

**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ taille maximale d' \_ \_ en-tête de réponse \_ de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Une limite définie sur la taille maximale de la partie en-tête de la réponse du serveur, spécifiée en octets. Cette liaison protège le client contre les tentatives de blocage du client par un serveur non autorisé en envoyant une réponse avec une quantité infinie de données d’en-tête. La valeur par défaut est 64 Ko.

**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ handle parent de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère le handle parent de ce handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**OPTION WINHTTP du texte de la \_ \_ \_ comarketingisation Passport \_**
</dt> <dd> <dl> <dt>



Récupère une chaîne qui contient le texte de [*copersonnalisation*](glossary.md) fourni par le serveur d’ouverture de session Passport. Cette option doit être récupérée immédiatement après que le serveur d’ouverture de session a répondu avec un code d’état 401. Une application doit passer une taille de mémoire tampon, en octets, qui est suffisamment grande pour contenir la chaîne retournée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL de \_ la \_ comarketing de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère une chaîne qui contient une URL pour un graphique de [*copersonnalisation*](glossary.md) fourni par le serveur d’ouverture de session Passport. Cette option doit être récupérée immédiatement après que le serveur d’ouverture de session a répondu avec un code d’état 401. Une application doit passer une taille de mémoire tampon, en octets, qui est suffisamment grande pour contenir la chaîne retournée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_URL de \_ \_ retour Passport \_ de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit une option en lecture seule sur un handle de demande qui récupère l’URL de retour Passport.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**déconnexion de l’option WINHTTP de \_ \_ Passport \_ \_**
</dt> <dd> <dl> <dt>



Définit l’option sur un handle de session pour se déconnecter de toutes les connexions Passport. Une application doit transmettre l’URL de retour Passport qui a été récupérée avec l' **\_ option WinHTTP \_ \_ \_ URL de renvoi Passport**. Tous les cookies associés à l’URL de renvoi sont effacés.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ mot de passe de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur de chaîne qui contient le mot de passe associé à un handle de demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy d’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une structure [**d' \_ \_ informations de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) qui contient les données de proxy sur un handle de session ou un handle de demande existant. Lors de la récupération de données de proxy, une application doit libérer les chaînes **lpszProxy** et **lpszProxyBypass** contenues dans cette structure (si elles n’ont pas la **valeur null**) à l’aide de la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Une application peut interroger les données de proxy globales (le proxy par défaut) en passant un handle **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ \_ mot de passe proxy de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur de chaîne qui contient le mot de passe utilisé pour accéder au proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**nom de principal du proxy de l' \_ option WinHTTP \_ \_ \_ utilisé**
</dt> <dd> <dl> <dt>



Obtient le nom principal du serveur proxy que WinHTTP a fourni à SSPI pendant l’authentification. Cette valeur de chaîne est usefor transmettant à [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) après un échec d’authentification.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_ \_ \_ nom d’utilisateur proxy de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur de chaîne qui contient le nom d’utilisateur utilisé pour accéder au proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon de lecture de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Cette option est dépréciée ; elle n’a aucun effet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**réponse de la connexion du proxy de réception de l' \_ option WinHTTP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Définit si l’entité de réponse du proxy peut être récupérée. Cette option est désactivée par défaut.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_délai de \_ réponse de réception \_ \_ de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, à attendre pour recevoir tous les en-têtes de réponse d’une demande. Si WinHTTP ne parvient pas à recevoir tous les en-têtes dans ce délai, la demande est annulée. La valeur du délai d’attente par défaut est de 90 secondes.

Ce délai d’expiration est vérifié uniquement lorsque des données sont reçues du Socket. Par conséquent, lorsque le délai d’attente expire, l’application cliente n’est pas notifiée tant que davantage de données n’arrivent pas sur le serveur. Si aucune donnée n’arrive à partir du serveur, le délai entre l’expiration du délai d’attente et la notification de l’application cliente peut être aussi important que celui défini à l’aide du paramètre *dwReceiveTimeout* de la fonction [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_délai de \_ réception des options WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour recevoir une réponse partielle à une demande ou lire des données. Si la réponse prend plus de temps que cette valeur de délai d’attente, la demande est annulée. La valeur de délai d'attente par défaut est de 30 secondes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_stratégie de \_ redirection des options WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit le comportement de WinHTTP en ce qui concerne la gestion d’un code d’état de redirection HTTP 30. Cette option peut être définie sur une session ou un handle de demande sur l’une des valeurs suivantes :

| Terme | Description |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_la stratégie de REdirection de l’option WinHTTP est \_ \_ \_ toujours | Toutes les redirections sont suivies automatiquement. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ la stratégie de redirection des options WinHTTP \_ \_ interdit \_ https \_ à \_ http | Toutes les redirections sont suivies, à l’exception de celles qui proviennent d’une URL sécurisée (https) vers une URL non sécurisée (http). Il s'agit du paramètre par défaut. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_stratégie de \_ redirection des options WinHTTP \_ \_ jamais | Les redirections ne sont jamais suivies. L’état de 30 est renvoyé à l’application. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_option WinHTTP \_ Reject \_ USERPWD \_ dans l' \_ URL**
</dt> <dd> <dl> <dt>



Rejette les URL qui contiennent un nom d’utilisateur et un mot de passe. Cette option rejette également les URL qui contiennent la sémantique *username : password* , même si aucun nom d’utilisateur ou mot de passe n’est spécifié. Par exemple, « u:p@hostname », « :@hostname », « u:@hostname » et « :p@hostname » sont tous marqués comme étant non valides. Si une URL non valide est transmise à la fonction, elle retourne l' [erreur \_ WinHTTP \_ \_ URL non valide](error-messages.md). Cette option est désactivée par défaut.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**priorité des demandes de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Cette option est dépréciée ; elle n’a aucun effet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_statistiques des \_ demandes d’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Extrait les statistiques de la demande.  Pour obtenir la liste des statistiques disponibles, consultez [**\_ \_ statistiques des demandes WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_ \_ durées de demande de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Informations de minutage extrait pour la requête. Pour obtenir la liste des minutages disponibles, consultez [**\_ \_ durée des requêtes WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**l' \_ option WinHTTP \_ nécessite une \_ fin de flux \_**
</dt> <dd> <dl> <dt>


Cette option indique à WinHttp d’ignorer les en-têtes de réponse « Content-Length » et de continuer à recevoir sur un flux jusqu’à ce que l’indicateur END_STREAM soit reçu.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**\_nom d' \_ hôte de résolution de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>


Cette option peut être définie sur un handle de demande WinHttp avant son envoi. Si cette valeur est définie, WinHttp utilise la chaîne fournie par l’appelant comme nom d’hôte pour la résolution DNS.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**délai de résolution de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour résoudre un nom d’hôte. La valeur par défaut du délai d’attente est **infinie**. Si une valeur non définie par défaut est spécifiée, il existe une surcharge liée à la création d’un thread par la résolution de noms.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_ \_ protocoles sécurisés option WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit une valeur d’entier long non signé qui spécifie les protocoles sécurisés qui sont acceptables. Par défaut, les paramètres SSL3 et TLS1 sont activés uniquement dans Windows 7 et Windows 8. Par défaut, les protocoles SSL3, TLS 1.0, TLS 1.1 et TLS 1.2 sont activés dans Windows 8.1 et Windows 10. La valeur peut être une combinaison d’une ou plusieurs des valeurs suivantes.

| Terme | Description |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_indicateur WinHTTP \_ \_ tout protocole \_ sécurisé | Les protocoles SSL (Secure Sockets Layer) (SSL) 2,0, SSL 3,0 et TLS (Transport Layer Security) 1,0 peuvent être utilisés. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_SSL2 de \_ \_ protocole sécurisé d’indicateur \_ WinHTTP | Le protocole SSL 2,0 peut être utilisé. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>\_Indicateur WinHTTP \_ \_ protocole sécurisé \_ SSL3 | Le protocole SSL 3,0 peut être utilisé. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>\_TLS1 de \_ \_ protocole sécurisé d’indicateur \_ WinHTTP | Le protocole TLS 1,0 peut être utilisé. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Protocole sécurisé d’indicateur WinHTTP \_ \_ \_ TLS1 \_ 1 | Le protocole TLS 1,1 peut être utilisé. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Indicateur WinHTTP \_ \_ protocole sécurisé \_ TLS1 \_ 2 | Le protocole TLS 1,2 peut être utilisé. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_structure de \_ certificat de sécurité option \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère le certificat pour un serveur SSL/TLS dans la structure [**des \_ \_ informations de certificat WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . L’application doit libérer les membres **lpszSubjectInfo** et **lpszIssuerInfo** avec [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**indicateurs de sécurité de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient les indicateurs de sécurité d’un handle. Il peut s’agir d’une combinaison de ces valeurs :

| Terme | Description |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>indicateur de sécurité ignorer le nom \_ \_ commun du \_ certificat \_ \_ non valide |Autorise un nom commun non valide dans un certificat ; autrement dit, le nom du serveur spécifié par l’application ne correspond pas au nom commun dans le certificat. Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP certificat de rappel \_ \_ \_ \_ \_ \_ non valide** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>indicateur de sécurité \_ \_ ignore la \_ Date de certificat \_ \_ non valide |Autorise une date de certificat non valide, c’est-à-dire un certificat arrivé à expiration ou qui n’est pas encore efficace. Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP signaler la date de rappel de \_ \_ \_ \_ certificat \_ \_ non valide** . |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>indicateur de sécurité \_ \_ ignorer l’autorité de \_ \_ certification inconnue | Autorise une autorité de certification non valide. Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP un rappel d' \_ autorité de \_ \_ \_ \_ certification non valide** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>indicateur de sécurité \_ \_ Ignorer \_ \_ \_ l’utilisation incorrecte du certificat | Autorise l’établissement de l’identité d’un serveur à l’aide d’un certificat non-serveur (par exemple, un certificat client). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>indicateur de sécurité \_ \_ ignorer la \_ \_ signature faible | Permet d’ignorer une signature faible.<br/>Cet indicateur est disponible dans la mise à jour cumulative pour chaque système d’exploitation à partir de Windows 7 et de Windows Server 2008 R2. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>indicateur de sécurité \_ \_ sécurisé | Utilise des transferts sécurisés. Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>niveau de force de l’indicateur de sécurité \_ \_ \_ | Utilise le chiffrement moyen (56 bits). Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>force de l’indicateur de sécurité \_ \_ \_ Strong | Utilise le chiffrement fort (128 bits). Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>force de l’indicateur de sécurité \_ \_ \_ faible | Utilise un chiffrement faible (40 bits). Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**informations de sécurité de l' \_ option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Extrait les informations de chiffrement et de connexion SChannel pour une demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**nombre de bits de la clé de sécurité de l' \_ option WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Récupère une valeur d’entier long non signé qui contient la force de chiffrement de la clé de chiffrement. Un nombre plus élevé indique un chiffrement de niveau de chiffrement renforcé.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ \_ délai d’attente d’envoi des options WinHTTP**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour envoyer une demande ou écrire des données. Si l’envoi de la demande prend plus de temps que le délai d’attente, l’opération d’envoi est annulée. Le délai d’attente par défaut est de 30 secondes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_serveur d’option WinHTTP \_ \_ CBT**
</dt> <dd> <dl> <dt>



Obtient un pointeur vers une structure de [**\_ liaisons SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) qui spécifie un jeton de liaison de canal (CBT).

Un jeton de liaison de canal est une propriété d’un canal de transport sécurisé et est utilisé pour lier un canal d’authentification au canal de transport sécurisé. Ce jeton ne peut être obtenu que par cette option après l’établissement d’une connexion SSL.

> [!Note]
> Le passage de cette option et d’une valeur **null** pour *lpBuffer* à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) renvoie une erreur \_ mémoire tampon insuffisante \_ et la taille d’octet requise pour la mémoire tampon dans le paramètre *lpdwBufferLength* . La valeur de la taille de la mémoire tampon retournée peut être passée dans un appel ultérieur à Query pour le jeton de liaison de canal. Ces étapes sont nécessaires lors \_ \_ de la gestion de \_ la demande d’état de rappel WinHTTP si vous souhaitez modifier les en-têtes de requête en fonction du jeton de liaison de canal. Notez que Windows XP et Vista ne prennent pas en charge la modification des en-têtes de demande pendant ce rappel.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_contexte de \_ chaîne du certificat de serveur d’option WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Récupère le contexte de la chaîne de certification du serveur. **WinHTTP \_ L' \_ option \_ \_ \_ contexte de chaîne de certificat serveur** peut être passée pour obtenir un pointeur dupliqué vers le **\_ \_ contexte de chaîne** de certificat pour une chaîne de certificats de serveur reçue pendant une connexion SSL négociée. Le client doit appeler [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sur le pointeur de \_ contexte PCCERT retourné qui est rempli dans la mémoire tampon.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_contexte de \_ certificat de serveur d’option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère le contexte de certification du serveur. **WinHTTP \_ Le \_ \_ \_ contexte** du certificat de serveur d’option peut être passé pour obtenir un pointeur dupliqué vers le [**contexte**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificat pour un certificat de serveur reçu pendant une connexion SSL négociée. Le client doit appeler [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sur le pointeur de \_ contexte PCCERT retourné qui est rempli dans la mémoire tampon.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**nom principal de service du \_ serveur option WinHTTP \_ \_ \_ utilisé**
</dt> <dd> <dl> <dt>



Obtient le nom principal du serveur serveur que WinHTTP a fourni à SSPI pendant l’authentification. Cette valeur de chaîne peut être passée à [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) après un échec d’authentification.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN de l' \_ option WinHTTP \_**
</dt> <dd> <dl> <dt>



Permet d’inclure ou de supprimer le numéro de port du serveur lorsque le SPN (nom de principal du service) est créé pour l’authentification Kerberos ou Negotiate Kerberos. Cet indicateur est l’une des valeurs suivantes :

| Terme | Description |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_port du \_ serveur de nom principal de service WinHTTP désactivé \_ \_ | Supprime le numéro de port du serveur. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_port du \_ serveur de nom principal de service WinHTTP activé \_ \_ | Comprend le numéro de port du serveur. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**\_code d' \_ erreur de flux d’options WinHTTP \_ \_**
</dt> <dd> <dl> <dt>


Cette option peut être interrogée sur un handle de demande WinHttp et retourne le code d’erreur indiqué par une RST_STREAM Frame reçue sur un flux HTTP.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_option WinHTTP \_ TCP \_ Fast \_ Open**
</dt> <dd> <dl> <dt>



Active TCP Fast Open pour la connexion.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_option WinHTTP \_ TCP \_ KeepAlive**
</dt> <dd> <dl> <dt>



Cette option peut être définie sur un handle de session WinHttp pour activer le comportement TCP Keep-Alive sur le Socket sous-jacent. Prend un struct [**TCP \_ KeepAlive**](/windows/win32/winsock/sio-keepalive-vals) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPTION WINHTTP-début de la \_ \_ \_ valeur TLS false \_**
</dt> <dd> <dl> <dt>



Active le démarrage TLS false pour la connexion.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**\_option WinHTTP \_ \_ protocole TLS \_ non sécurisé de \_ secours**
</dt> <dd> <dl> <dt>



Cette option peut être définie sur un handle de session WinHttp pour contrôler si le recours à TLS 1,0 est autorisé en cas d’échec de la liaison TLS avec une version de protocole plus récente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_événement de \_ notification de déchargement d’option WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Prend un événement qui sera défini lorsque le dernier rappel est terminé pour une session particulière. Cet indicateur doit être utilisé sur un handle de session. L’événement ne peut pas être fermé tant qu’il n’a pas été défini par WinHTTP.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_option WinHTTP \_ \_ -analyse d’en-tête non sécurisé \_**
</dt> <dd> <dl> <dt>



Cette option est réservée à un usage interne et ne doit pas être appelée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_option WinHTTP \_ mettre à niveau \_ vers \_ Web \_ Socket**
</dt> <dd> <dl> <dt>



Demande à la pile de démarrer un processus d’établissement de liaison WebSocket avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Cette option n’accepte aucun paramètre.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL de l' \_ option WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère une valeur de chaîne qui contient l’URL complète d’une ressource téléchargée. Si l’URL d’origine contenait des données supplémentaires, telles que des chaînes ou des ancres de recherche, ou si l’appel a été redirigé, l’URL retournée est différente de l’original. L’application doit passer une mémoire tampon, dimensionnée en octets, qui est suffisamment grande pour contenir l’URL retournée en caractères larges.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_option WinHTTP \_ utiliser \_ les \_ \_ informations d’identification du serveur global**
</dt> <dd> <dl> <dt>



Prend un **bool** et ne peut être défini qu’avec un handle de session. Il se propage uniquement aux descripteurs créés à partir du descripteur de session après que l’option a été définie. Si la **valeur est true**, cette option entraîne, en dernier recours, l’utilisation d’informations d’identification de serveur globales qui ont été transférées depuis wininet. La valeur par défaut de cette option est **false**. Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**. Cette clé de Registre n’est pas présente par défaut. Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP. Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ agent utilisateur de \_ l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit ou récupère la chaîne de l' [*agent utilisateur*](glossary.md) sur les handles fournis par [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) et utilisés dans les fonctions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) suivantes, à condition qu’elles ne soient pas remplacées par un en-tête ajouté par [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ou **WinHttpSendRequest**. Lors de la récupération d’un agent utilisateur, l’application doit passer une mémoire tampon, dimensionnée en octets, qui est suffisamment grande pour contenir l’URL retournée en caractères larges. Lors de la définition de l’agent utilisateur, la taille de la mémoire tampon correspond à la longueur de la chaîne, en caractères, plus la marque de fin **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_option WinHTTP \_ nom d’utilisateur**
</dt> <dd> <dl> <dt>



Définit ou récupère une chaîne qui contient le nom d’utilisateur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ \_ délai d’attente de fermeture du socket Web de l’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit le délai, en millisecondes, pendant lequel [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) doit attendre pour terminer le protocole de transfert de fermeture. La valeur par défaut est 10 secondes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_intervalle de \_ conservation \_ de \_ conservation de socket Web \_ d’option WinHTTP**
</dt> <dd> <dl> <dt>



Définit l’intervalle, en millisecondes, pour envoyer un paquet Keep-Alive sur la connexion. L’intervalle par défaut est de 30000 (30 secondes). L’intervalle minimal est 15000 (15 secondes). L’utilisation de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour définir une valeur inférieure à 15000 retourne **le \_ \_ paramètre error non valide**.

> [!Note]
> La valeur par défaut de l' **option WinHTTP de l’intervalle de \_ \_ \_ conservation de socket \_ \_ Web** est lue à partir de **HKLM : \\ Software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**. Si aucune valeur n’est définie, la valeur par défaut 30000 est utilisée. Il n’est pas possible d’avoir un intervalle KeepAlive inférieur à 15000 millisecondes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon de réception du socket Web \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur DWORD qui spécifie la taille de la mémoire tampon de réception à utiliser sur les connexions WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon d’envoi du socket Web \_**
</dt> <dd> <dl> <dt>



Définit ou récupère une valeur DWORD qui spécifie la taille de la mémoire tampon d’envoi à utiliser sur les connexions WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_nombre de \_ \_ threads de travail option WinHTTP \_**
</dt> <dd> <dl> <dt>



Définit une valeur d’entier long non signé qui spécifie le nombre de threads de travail que le pool de threads doit utiliser pour les saisies semi-automatiques asynchrones. La valeur par défaut de cette option est zéro, ce qui indique que le nombre de threads de travail est égal au nombre de processeurs sur le système. Cette option ne peut être définie que sur un handle [HINTERNET](hinternet-handles-in-winhttp.md) **null** avant qu’une opération asynchrone se produise.   Cette option ne peut être définie qu’une seule fois.

**Windows Server 2008 R2 et Windows 7 :** Cet indicateur est obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon d’écriture de l’option WinHTTP \_**
</dt> <dd> <dl> <dt>



Cette option est dépréciée ; elle n’a aucun effet.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Le tableau suivant répertorie les indicateurs d’option en spécifiant les descripteurs sur lesquels ils peuvent agir, s’ils peuvent être interrogés et définis, ainsi que le type de données utilisé. Un « X » indique que l’indicateur d’option est valide pour une utilisation avec la fonction ou le handle, alors que « - » spécifie que l’indicateur d’option n’est pas valide.

Si vous tentez de définir ou d’interroger un indicateur d’option sur une version de Windows où il n’est pas pris en charge, l' **\_ \_ \_ option WinHTTP non valide** est générée.

| Indicateur d’option et type de données | Handle de session | Handle de demande | Option de requête | Option Set | Version minimale de Windows |
|-|-|-|-|-|-|
| OPTION WINHTTP assurée par les \_ \_ \_ \_ rappels non bloquants \_<br/>**Boolean** | X | \- | \- | X | \- |
| stratégie d’accès automatique aux \_ options WinHTTP \_ \_<br/>**GRANDE** | \- | X | \- | X | \- |
| \_connexions en \_ arrière-plan des options WinHTTP \_<br/>**GRANDE** | X | \- | \- | X | Windows 10 version 21H1 |
| \_rappel d’option WinHTTP \_<br/>**LPVOID** | X | X | X | X | \- |
| \_contexte de \_ \_ certificat client \_ de l’option WinHTTP<br/>[**contexte du certificat \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| \_option WinHTTP \_ \_ liste d’émetteurs de certificats client \_ \_<br/>[**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| page de codes de l' \_ option WinHTTP \_<br/>**GRANDE** | X | \- | \- | X | \- |
| \_option WinHTTP \_ configurer \_ l' \_ authentification Passport<br/>**GRANDE** | X | \- | \- | X | \- |
| \_ \_ nouvelles tentatives de connexion de l’option WinHTTP \_<br/>**GRANDE** | X | X | X | X | \- |
| délai de connexion de l' \_ option WinHTTP \_ \_<br/>**GRANDE** | X | X | X | X | \- |
| informations de connexion de l' \_ option WinHTTP \_ \_<br/>[**\_informations de connexion WinHTTP \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| \_Statistiques de connexion des options WinHTTP \_ \_ \_ v0<br/>[**\_Informations TCP \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 version 1903 |
| \_Statistiques de connexion des options WinHTTP \_ \_ \_ v1<br/>[**\_Informations TCP \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 version 2004 |
| valeur de contexte de l' \_ option WinHTTP \_ \_<br/>**\_ptr DWORD** | X | X | X | X | \- |
| décompression des \_ options WinHTTP \_<br/>**GRANDE** | X | X | \- | X | Windows 8.1 |
| OPTION WINHTTP- \_ désactiver la génération de \_ \_ chaîne de certificats \_ \_<br/>**Boolean** | X | \- | \- | X | Windows 10 version 21H1 |
| \_fonctionnalité de \_ désactivation de l’option WinHTTP \_<br/>**GRANDE** | \- | X | \- | X | \- |
| \_option WinHTTP \_ désactiver \_ le \_ protocole sécurisé de \_ secours<br/>**Boolean** | X | \- | \- | X | Windows 10 version 1903 |
| OPTION WINHTTP- \_ \_ désactiver la \_ \_ file d’attente de flux<br/>**Boolean** | X | X | \- | X | Windows 10 version 1809 |
| \_option WinHTTP \_ activer la \_ fonctionnalité<br/>**GRANDE** | \* | \* | \- | X | \- |
| \_option WinHTTP \_ activer \_ le \_ protocole http<br/>**GRANDE** | X | X | \- | X | Windows 10 version 1607 |
| \_Option WinHTTP \_ activer \_ le \_ \_ contexte de \_ certificat client http2 plus \_<br/>**Boolean** | X | \- | \- | X | Windows 10 version 21H1 |
| \_option WinHTTP \_ EnableTracing,<br/>**GRANDE** | \- | \- | X | X | \- |
| \_option WinHTTP \_ coder \_ extra<br/>**Boolean** | X | X | \- | X | Windows 10 version 1803 |
| expiration de la connexion de l' \_ option WinHTTP \_ \_<br/>N/A | \- | X | \- | X | Windows 10 version 1903 |
| \_ \_ erreur étendue de l’option WinHTTP \_<br/>**GRANDE** | X | X | X | \- | \- |
| \_option WinHTTP \_ première \_ \_ connexion disponible<br/>**Boolean** | X | \- | \- | X | Windows 10 version 21H1 |
| identification \_ du \_ proxy global des options \_ WinHTTP \_<br/>[**\_références WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| \_options WinHTTP \_ - \_ CREDS de serveur global \_<br/>[**\_références WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| TYPE de handle de l' \_ option WinHTTP \_ \_<br/>**GRANDE** | X | X | X | \- | \- |
| \_option WinHTTP \_ \_ protocole http \_ requis<br/>**Boolean** | X | X | \- | X | Windows 10 version 1903 |
| \_option WinHTTP \_ \_ protocole http \_ utilisé<br/>**GRANDE** | \- | X | X | \- | Windows 10 version 1607 |
| \_ \_ version http de l’option WinHTTP \_<br/>[**\_informations sur la version http \_**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| \_Option WinHTTP \_ http2 \_ KeepAlive<br/>**GRANDE** | X | \- | \- | X | Windows 10 version 21H1 |
| \_Option WinHTTP \_ http2 \_ plus \_ \_ encodage de transfert<br/>**Boolean** | X | X | \- | X | Windows 10 version 21H1 |
| \_option WinHTTP \_ Ignorer \_ la \_ révocation de certificat \_ hors connexion<br/>**Boolean** | \- | X | \- | X | Windows 10 version 2004 |
| \_Option WinHTTP \_ \_ Fast \_ Fallback IPv6<br/>**Boolean** | X | \- | \- | X | Windows 10 version 1903 |
| l' \_ option WinHTTP \_ est une \_ \_ réponse de connexion proxy \_<br/>**Boolean** | X | X | X | \- | \- |
| \_Option WinHTTP \_ nombre de Conn. \_ \_ par \_ \_ serveur 1 0 \_<br/>**GRANDE** | X | \- | X | X | \- |
| \_option WinHTTP \_ nombre maximal de \_ conn. \_ par \_ serveur<br/>**GRANDE** | X | \- | X | X | \- |
| \_option WinHTTP \_ nombre maximal de \_ \_ \_ redirections http automatiques<br/>**GRANDE** | X | X | X | X | \- |
| \_ \_ État http max de l’option WinHTTP \_ \_ \_ continue<br/>**GRANDE** | X | X | X | X | \- |
| \_option WinHTTP \_ taille maximale de \_ \_ drainage \_ de la réponse<br/>**GRANDE** | X | X | X | X | \- |
| \_ \_ taille maximale d' \_ \_ en-tête de réponse \_ de l’option WinHTTP<br/>**GRANDE** | X | X | X | X | \- |
| \_ \_ handle parent de l’option WinHTTP \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| OPTION WINHTTP du texte de la \_ \_ \_ comarketingisation Passport \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_URL de \_ la \_ comarketing de l’option WinHTTP \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_URL de \_ \_ retour Passport \_ de l’option WinHTTP<br/>**LPVOID** | \- | X | X | \- | \- |
| déconnexion de l’option WINHTTP de \_ \_ Passport \_ \_<br/>**LPVOID** | X | \- | \- | X | \- |
| \_ \_ mot de passe de l’option WinHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| \_proxy d’option WinHTTP \_<br/>[**\_informations sur le proxy WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| \_ \_ \_ mot de passe proxy de l’option WinHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| nom de principal du proxy de l' \_ option WinHTTP \_ \_ \_ utilisé<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ \_ nom d’utilisateur proxy de l’option WinHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| \_taille de \_ la \_ mémoire tampon de lecture de l’option WinHTTP \_<br/>**GRANDE** | \- | X | X | X | \- |
| réponse de la connexion du proxy de réception de l' \_ option WinHTTP \_ \_ \_ \_<br/>**Boolean** | X | X | \- | X | \- |
| \_délai de \_ réponse de réception \_ \_ de l’option WinHTTP<br/>**GRANDE** | X | X | X | X | \- |
| \_délai de \_ réception des options WinHTTP \_<br/>**GRANDE** | X | X | X | X | \- |
| \_stratégie de \_ redirection des options WinHTTP \_<br/>**GRANDE** | X | X | X | X | \- |
| \_option WinHTTP \_ Reject \_ USERPWD \_ dans l' \_ URL<br/>**Boolean** | \- | X | \- | X | \- |
| priorité des demandes de l' \_ option WinHTTP \_ \_<br/>**GRANDE** | \- | X | X | X | \- |
| \_statistiques des \_ demandes d’option WinHTTP \_<br/>[**\_statistiques des demandes WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 version 1903 |
| \_ \_ durées de demande de l’option WinHTTP \_<br/>[**\_durées des requêtes WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 version 1903 |
| l' \_ option WinHTTP \_ nécessite une \_ fin de flux \_<br/>**Boolean** | X | X | \- | X | Windows 10 version 21H1 |
| \_nom d' \_ hôte de résolution de l’option WinHTTP \_<br/>**LPWSTR** | \- | X | \- | X | Windows 10 version 21H1 |
| délai de résolution de l' \_ option WinHTTP \_ \_<br/>**GRANDE** | X | X | X | X | \- |
| \_ \_ protocoles sécurisés option WinHTTP \_<br/>**GRANDE** | X | \- | \- | X | \- |
| \_structure de \_ certificat de sécurité option \_ WinHTTP \_<br/>[**\_informations de certificat WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| indicateurs de sécurité de l' \_ option WinHTTP \_ \_<br/>**GRANDE** | \- | X | X | X | \- |
| informations de sécurité de l' \_ option WinHTTP \_ \_<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 version 2004 |
| nombre de bits de la clé de sécurité de l' \_ option WinHTTP \_ \_ \_<br/>**GRANDE** | \- | X | X | \- | \- |
| \_ \_ \_ délai d’attente d’envoi des options WinHTTP<br/>**GRANDE** | X | X | X | X | \- |
| \_serveur d’option WinHTTP \_ \_ CBT<br/>[**\_Liaisons SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| \_contexte de \_ chaîne du certificat de serveur d’option WinHTTP \_ \_ \_<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 version 2004 |
| \_contexte de \_ certificat de serveur d’option WinHTTP \_ \_<br/>[**CONTEXTE DU CERTIFICAT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| nom principal de service du \_ serveur option WinHTTP \_ \_ \_ utilisé<br/>**LPWSTR** | \- | X | X | \- | \- |
| SPN de l' \_ option WinHTTP \_<br/>**GRANDE** | \- | X | \- | X | \- |
| \_code d' \_ erreur de flux d’options WinHTTP \_ \_<br/>**GRANDE** | \- | X | X | \- | Windows 10 version 21H1 |
| \_option WinHTTP \_ TCP \_ Fast \_ Open<br/>**Boolean** | X | \- | \- | X | Windows 10 version 2004 |
| \_option WinHTTP \_ TCP \_ KeepAlive<br/>[**\_KeepAlive TCP**](/windows/win32/winsock/sio-keepalive-vals) | X | \- | \- | X | Windows 10 version 2004 |
| OPTION WINHTTP-début de la \_ \_ \_ valeur TLS false \_<br/>**Boolean** | X | \- | \- | X | Windows 10 version 2004 |
| \_option WinHTTP \_ \_ protocole TLS \_ non sécurisé de \_ secours<br/>**Boolean** | X | \- | \- | X | Windows 10 version 21H1 |
| \_événement de \_ notification de déchargement d’option WinHTTP \_ \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| \_option WinHTTP \_ \_ -analyse d’en-tête non sécurisé \_<br/>**GRANDE** | \- | X | \- | X | \- |
| \_option WinHTTP \_ mettre à niveau \_ vers \_ Web \_ Socket<br/>N/A | \- | X | \- | X | \- |
| URL de l' \_ option WinHTTP \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_option WinHTTP \_ utiliser \_ les \_ \_ informations d’identification du serveur global<br/>**Boolean** | X | X | \- | X | \- |
| \_ \_ agent utilisateur de \_ l’option WinHTTP<br/>**LPWSTR** | X | \- | X | X | \- |
| \_option WinHTTP \_ nom d’utilisateur<br/>**LPWSTR** | \- | X | X | X | \- |
| \_ \_ \_ \_ \_ délai d’attente de fermeture du socket Web de l’option WinHTTP<br/>**GRANDE** | \- | \- | X | X | \- |
| \_intervalle de \_ conservation \_ de \_ conservation de socket Web \_ d’option WinHTTP<br/>**GRANDE** | \- | \- | X | X | \- |
| OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon de réception du socket Web \_<br/>**GRANDE** | X | X | X | X | Windows 8.1 |
| OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon d’envoi du socket Web \_<br/>**GRANDE** | X | X | X | X | Windows 8.1 |
| \_nombre de \_ \_ threads de travail option WinHTTP \_<br/>**GRANDE** | \- | \- | \- | X | \- |
| \_taille de \_ la \_ mémoire tampon d’écriture de l’option WinHTTP \_<br/>**GRANDE** | \- | X | X | X | \- |

> [!Note]
> Pour Windows XP et Windows 2000, consultez [Configuration requise](winhttp-start-page.md)pour l’exécution.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|--------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]            |
| Serveur minimal pris en charge | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]         |
| Composant redistribuable          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000. |
| En-tête                   | WinHTTP. h                                                                       |

## <a name="see-also"></a>Voir aussi

[Versions de WinHTTP](winhttp-versions.md)
