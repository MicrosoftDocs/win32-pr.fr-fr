---
title: Indicateurs d’informations de requête (Wininet. h)
description: Les listes suivantes contiennent les attributs et les modificateurs utilisés par HttpQueryInfo et QueryInfo.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517334"
---
# <a name="query-info-flags-winineth"></a>Indicateurs d’informations de requête (Wininet. h)

Les listes suivantes contiennent les attributs et les modificateurs utilisés par [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) et [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).

Les indicateurs d’attribut sont utilisés par [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) pour indiquer les données à récupérer. La plupart des indicateurs d’attribut sont directement mappés à un en-tête HTTP spécifique. Il existe également des indicateurs spéciaux, tels que [ \_ \_ \_ les en-têtes bruts de requête http](/windows), qui ne sont pas associés à un en-tête spécifique.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**acceptation de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Récupère les types de médias acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**jeu de caractères d’acceptation de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Récupère les jeux de caractères acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**encodage d’acceptation de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Récupère les valeurs de codage de contenu acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**langue d’acceptation de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Récupère les langages naturels acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**plages d’acceptation de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Récupère les types des demandes de plage acceptées pour une ressource.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**âge de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Récupère le champ d’en-tête de réponse d’âge, qui contient l’estimation de la durée de l’expéditeur depuis la génération de la réponse sur le serveur d’origine.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**autorisation de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Reçoit les verbes HTTP pris en charge par le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorisation de requête HTTP \_**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Récupère les informations d’identification utilisées pour une demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_contrôle de \_ cache de requête HTTP \_**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Récupère les directives de contrôle de cache.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**connexion à la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Récupère toutes les options spécifiées pour une connexion particulière et ne doit pas être communiquée par les proxys sur des connexions supplémentaires.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**BASE de contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Récupère l’URI de base (Uniform Resource Identifier) pour la résolution des URL relatives dans l’entité.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**Description du contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées uniquement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**DISPOSITION du contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées uniquement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**encodage du contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Récupère tous les codages de contenu supplémentaires qui ont été appliqués à la ressource entière.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**ID de contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Récupère l’identification du contenu.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**langage de contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Récupère la langue dans laquelle se trouve le contenu.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**longueur du contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Récupère la taille de la ressource, en octets.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**emplacement du contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Récupère l’emplacement de la ressource de l’entité incluse dans le message.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**MD5 du contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Récupère un condensé MD5 du corps d’entité afin de fournir un MIC (message integrity check) de bout en bout pour le corps d’entité. Pour plus d’informations, consultez RFC1864, le champ d’en-tête Content-MD5, à l’adresse [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**plage de contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Récupère l’emplacement dans le corps de l’entité complète où le corps de l’entité partielle doit être inséré et la taille totale du corps de l’entité complète.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**encodage de transfert de contenu de \_ requête HTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Reçoit le code de contenu supplémentaire qui a été appliqué à la ressource.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**TYPE de contenu de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Reçoit le type de contenu de la ressource (par exemple, text/html).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie de requête HTTP \_**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Récupère tous les cookies associés à la requête.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**coût de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



N'est plus pris en charge.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_requête HTTP \_ personnalisée**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



Fait en sorte que [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) recherche le nom d’en-tête spécifié dans *lpvBuffer* et stocke les données d’en-tête dans *lpvBuffer*.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**Date de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Reçoit la date et l’heure d’origine du message.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_requête HTTP \_ dérivée \_ de**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



N'est plus pris en charge.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ en-têtes d’écho de requête HTTP \_**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Actuellement non implémenté.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_ \_ en-têtes de requête http Echo \_ \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Actuellement non implémenté.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**réponse d’écho de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



Actuellement non implémenté.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_demande d' \_ écho de requête HTTP \_**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



Actuellement non implémenté.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**ETag de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Récupère la balise d’entité de l’entité associée.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_requête HTTP \_ attendue**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Récupère l’en-tête Expect, qui indique si l’application cliente doit attendre des réponses de série 100.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**expiration de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Reçoit la date et l’heure après lesquelles la ressource doit être considérée comme obsolète.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_requête HTTP \_ transférée**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées uniquement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_requête HTTP \_ à partir de**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Récupère l’adresse de messagerie de l’utilisateur humain qui contrôle l’agent utilisateur demandeur si l’en-tête from est donné.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_hôte de requête HTTP \_**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Récupère l’hôte Internet et le numéro de port de la ressource demandée.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_requête HTTP \_ si la correspondance est \_ trouvée**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Récupère le contenu du champ d’en-tête de demande If-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**requête HTTP en \_ \_ cas de \_ modification \_ depuis**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Récupère le contenu de l’en-tête If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_requête HTTP \_ si \_ aucune ne \_ correspond**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Récupère le contenu du champ d’en-tête de demande If-None-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_requête HTTP \_ si la \_ plage**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Récupère le contenu du champ d’en-tête de demande If-Range. Cet en-tête permet à l’application cliente de vérifier que l’entité liée à une copie partielle de l’entité dans le cache de l’application cliente n’a pas été mise à jour. Si l’entité n’a pas été mise à jour, envoyez les composants que l’application cliente est manquante. Si l’entité a été mise à jour, envoyez la totalité de l’entité mise à jour.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**requête HTTP si elle n’a pas été \_ \_ \_ modifiée \_ depuis**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Récupère le contenu du champ d’en-tête de demande If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ dernière \_ modification de la requête http**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Reçoit la date et l’heure auxquelles le serveur estime que la ressource a été modifiée pour la dernière fois.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**lien de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées uniquement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**emplacement de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Récupère le Uniform Resource Identifier absolu (URI) utilisé dans un en-tête de réponse d’emplacement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**Max. des \_ requêtes http \_**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



N’est pas un indicateur de requête. Indique la valeur maximale d’une \_ valeur de requête HTTP \_ \* .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ transferts max. des requêtes http \_**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Récupère le nombre de proxies ou de passerelles qui peuvent transférer la requête vers le serveur entrant suivant.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ID du \_ message de requête HTTP \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



N'est plus pris en charge.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ version MIME de la requête HTTP \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Reçoit la version du protocole MIME qui a été utilisée pour construire le message.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**URI d’origine de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées uniquement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma de requête HTTP \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Reçoit les directives spécifiques à l’implémentation qui peuvent s’appliquer à n’importe quel destinataire le long de la chaîne de requête/réponse.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_authentification du \_ proxy de requête HTTP \_**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Récupère le schéma et le domaine d’authentification retournés par le proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_autorisation du \_ proxy de requête HTTP \_**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Récupère l’en-tête utilisé pour identifier l’utilisateur sur un proxy qui requiert une authentification. Cet en-tête ne peut être récupéré que si la demande est envoyée au serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_ \_ connexion proxy de requête HTTP \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Récupère l’en-tête de Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_requête HTTP \_ publique**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Reçoit les méthodes disponibles sur ce serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_plage de requêtes http \_**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Récupère la plage d’octets d’une entité.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ en-têtes bruts de requête HTTP \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Reçoit tous les en-têtes retournés par le serveur. Chaque en-tête se termine par « \\ 0 ». Un « \\ 0 » supplémentaire termine la liste des en-têtes.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_ \_ en-têtes bruts de requête HTTP \_ \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Reçoit tous les en-têtes retournés par le serveur. Chaque en-tête est séparé par une séquence de retour chariot/saut de ligne (CR/LF).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**référant à la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Reçoit le Uniform Resource Identifier (URI) de la ressource dans laquelle l’URI demandé a été obtenu.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_actualisation des requêtes http \_**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées uniquement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**méthode de requête de \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Reçoit le verbe HTTP qui est utilisé dans la demande, en général, obtenir ou poster.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**\_nouvelle tentative de requête HTTP \_ \_ après**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Récupère la durée pendant laquelle le service est censé ne pas être disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_serveur de requêtes http \_**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Récupère les données relatives au logiciel utilisé par le serveur d’origine pour traiter la demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie de \_ jeu de requêtes http \_**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Reçoit la valeur du cookie défini pour la demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**CODE d’état de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Reçoit le code d’état retourné par le serveur. Pour plus d’informations et pour obtenir la liste des valeurs possibles, consultez [**codes d’État http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**texte d’état de la \_ requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Reçoit tout texte supplémentaire retourné par le serveur sur la ligne de réponse.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**titre de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées uniquement.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**encodage de \_ transfert de requêtes http \_ \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Récupère le type de transformation qui a été appliqué au corps du message afin qu’il puisse être transféré en toute sécurité entre l’expéditeur et le destinataire.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_requête HTTP \_ sauf \_ modification \_ depuis**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Récupère l’en-tête If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_ \_ mise à niveau de la requête http**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Récupère les protocoles de communication supplémentaires pris en charge par le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI de requête HTTP \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Reçoit tout ou partie des URI (Uniform Resource Identifier) par lesquels la ressource d’URI de requête peut être identifiée.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_ \_ agent utilisateur de la requête HTTP \_**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Récupère les données relatives à l’agent utilisateur qui a effectué la demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**la \_ requête HTTP \_ varie**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Récupère l’en-tête qui indique que l’entité a été sélectionnée à partir de plusieurs représentations disponibles de la réponse à l’aide de la négociation pilotée par le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**VERSION de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Reçoit le code de la dernière réponse renvoyée par le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_requête HTTP \_ via**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Récupère les protocoles et destinataires intermédiaires entre l’agent utilisateur et le serveur sur les demandes, et entre le serveur d’origine et le client sur les réponses.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_avertissement de requête HTTP \_**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Récupère des données supplémentaires sur l’état d’une réponse qui n’est peut-être pas reflétée par le code d’état de réponse.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_ \_ authentification Web de la requête HTTP \_**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Récupère le schéma et le domaine d’authentification retournés par le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_options de \_ \_ type de contenu X \_ \_ de la requête http**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Récupère la valeur d’en-tête X-Content-type-options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**P3P de la \_ requête HTTP \_**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Récupère la valeur d’en-tête P3P.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Requête HTTP \_ X \_ P2P-P2P \_**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Récupère la valeur d’en-tête X-P2P-PeerDist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_traduction de requête HTTP \_**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Récupère la valeur d’en-tête Translate.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_requête HTTP \_ X \_ \_ compatible avec UA**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Récupère la valeur d’en-tête X-UA-compatible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ style par défaut de la requête HTTP \_**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Récupère la valeur d’en-tête Default-Style.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_options de \_ \_ Frame X \_ de la requête http**
</dt> <dd> <dl> <dt>

85 %
</dt> <dt>



Récupère la valeur d’en-tête X-Frame-options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**\_requête HTTP \_ X \_ \_ Protection XSS**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Récupère la valeur d’en-tête X-XSS-protection.


</dt> </dl> </dd> </dl>

Les indicateurs de modificateur sont utilisés conjointement avec un indicateur d’attribut pour modifier la requête. Les indicateurs de modificateur modifient le format des données retournées ou indiquent où [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) doit rechercher les données.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_fusion d' \_ indicateur de requête HTTP \_**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Non implémenté.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**Numéro de l' \_ indicateur de requête HTTP \_ \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Retourne les données sous la forme d’un nombre 32 bits pour les en-têtes dont la valeur est un nombre, tel que le code d’État.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_ \_ \_ en-têtes de demande d’indicateur de requête HTTP \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Interroge uniquement les en-têtes de demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_indicateur de requête HTTP \_ \_ SystemTime**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Retourne la valeur d’en-tête en tant que structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , ce qui ne nécessite pas que l’application analyse les données. Utilisez pour les en-têtes dont la valeur est une chaîne de date/heure, telle que « Last-modified-Time ».


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

