---
description: Ces attributs et modificateurs sont utilisés par WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Indicateurs d’informations de requête (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8a7f95f0e093f175901e4bed30f4055a04b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013162"
---
# <a name="query-info-flags-winhttph"></a>Indicateurs d’informations de requête (Winhttp.h)

Ces attributs et modificateurs sont utilisés par [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).

Les indicateurs d’attribut sont utilisés par [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) pour indiquer les informations à récupérer. La plupart des indicateurs d’attribut sont directement mappés à un en-tête HTTP spécifique. Il existe également des indicateurs spéciaux, tels que \_ \_ les en-têtes de requête WinHTTP bruts \_ , qui ne sont pas associés à un en-tête spécifique.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**acceptation de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère les types de médias acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**jeu de caractères d' \_ acceptation de requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère les jeux de caractères acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**encodage d' \_ acceptation de requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère les valeurs de codage de contenu acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**langue d’acceptation de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère les langages naturels acceptables pour la réponse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_plages d' \_ acceptation des requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère les types des demandes de plage acceptées pour une ressource.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_âge des requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère le champ d’en-tête de réponse d’âge, qui contient l’estimation de la durée de l’expéditeur depuis la génération de la réponse au niveau du serveur d’origine.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**autorisation de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit les [**verbes HTTP**](glossary.md) pris en charge par le serveur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ informations d’authentification de la requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère l’en-tête de Authentication-Info.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_autorisation de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère les informations d’identification utilisées pour une demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ contrôle du cache des requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère les directives de contrôle de cache.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**connexion à la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère toutes les options spécifiées pour une connexion particulière et ne doit pas être communiquée par les proxys sur des connexions supplémentaires.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_base de \_ contenu de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère le Uniform Resource Identifier de base (URI) pour résoudre des URL relatives dans l’entité.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**Description du contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSITION du contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**encodage du contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère le codage de contenu supplémentaire qui a été appliqué à l’ensemble de la ressource.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**ID de contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère l’identification du contenu.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**langue de contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère la langue dans laquelle le contenu est écrit.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**longueur du contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère la taille de la ressource, en octets.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**emplacement du contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère l’emplacement de la ressource de l’entité incluse dans le message.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**MD5 du contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère un condensé MD5 du corps d’entité afin de fournir une vérification de l’intégrité des messages de bout en bout pour le corps de l’entité. Pour plus d’informations, consultez la [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**plage de contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère l’emplacement dans le corps de l’entité complète où le corps de l’entité partielle doit être inséré et la taille totale du corps de l’entité complète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**encodage de transfert de contenu de \_ requête WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Récupère une transformation d’encodage applicable à un corps d’entité. Il est possible qu’il ait déjà été appliqué, qu’il doive être appliqué ou éventuellement applicable.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TYPE de contenu de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Reçoit le type de contenu de la ressource, tel que texte ou html.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_cookie de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère tous les cookies associés à la requête.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_coût des requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Non pris en charge.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**\_requête WinHTTP \_ personnalisée**
</dt> <dd> <dl> <dt>



Fait en sorte que [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) recherche le nom d’en-tête spécifié dans le paramètre *pwszName* et stocke les informations d’en-tête dans *lpBuffer*. Une application peut utiliser **l' \_ option WinHTTP \_ recevoir le \_ \_ délai de réponse** pour limiter la durée maximale pendant laquelle cette requête attend que tous les en-têtes soient reçus.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**Date de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit la date et l’heure d’origine du message.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_requête WinHTTP \_ dérivée \_ de**
</dt> <dd> <dl> <dt>



Non pris en charge.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère la balise d’entité de l’entité associée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_requête WinHTTP \_ attendue**
</dt> <dd> <dl> <dt>



Récupère l’en-tête Expect, qui indique si l’application cliente doit attendre des réponses de série 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**expiration de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit la date et l’heure après lesquelles la ressource doit être considérée comme obsolète.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_requête WinHTTP \_ transférée**
</dt> <dd> <dl> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_requête WinHTTP \_ à partir de**
</dt> <dd> <dl> <dt>



Récupère l’adresse de messagerie de l’utilisateur qui contrôle l' [*agent utilisateur*](glossary.md) demandeur si l’en-tête from est donné.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_hôte de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère l’hôte Internet et le numéro de port de la ressource demandée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_requête WinHTTP \_ si \_ correspondance**
</dt> <dd> <dl> <dt>



Récupère le contenu du champ d’en-tête de demande If-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_requête WinHTTP \_ si \_ modifiée \_ depuis**
</dt> <dd> <dl> <dt>



Récupère le contenu de l’en-tête If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_requête WinHTTP \_ si \_ aucune ne \_ correspond**
</dt> <dd> <dl> <dt>



Récupère le contenu du champ d’en-tête de demande If-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**\_requête WinHTTP \_ si la \_ plage**
</dt> <dd> <dl> <dt>



Récupère le contenu du champ d’en-tête de demande If-Range. Cet en-tête permet à l’application cliente de vérifier si l’entité liée à une copie partielle de l’entité dans le cache de l’application cliente n’a pas été mise à jour. Si l’entité n’a pas été mise à jour, envoyez les composants que l’application cliente est manquante. Si l’entité a été mise à jour, envoyez la totalité de l’entité mise à jour.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**\_requête WinHTTP \_ si non \_ modifiée \_ depuis**
</dt> <dd> <dl> <dt>



Récupère le contenu du champ d’en-tête de demande If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_lien de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ dernière \_ modification de la requête WinHTTP**
</dt> <dd> <dl> <dt>



Reçoit la date et l’heure de la dernière modification de la ressource. La date et l’heure sont déterminées par le serveur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**emplacement de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère l’URI absolu utilisé dans un en-tête de réponse d’emplacement.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**Max. des \_ requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Indique la valeur maximale d’une \_ valeur de requête WinHTTP \_ \* . N’est pas un indicateur de requête.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ nombre maximal de transferts de requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère le nombre de proxies ou de passerelles qui peuvent transférer la requête vers le serveur entrant suivant.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ID de \_ message de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Non pris en charge.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ version MIME de la requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit la version du protocole MIME (Multipurpose Internet Mail Extensions) qui a été utilisée pour construire le message.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ URI orig de la requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit les directives spécifiques à l’implémentation qui peuvent s’appliquer à n’importe quel destinataire le long de la chaîne de requête/réponse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_authentification du \_ proxy de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère le schéma et le domaine d’authentification retournés par le proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_autorisation du \_ proxy de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère l’en-tête utilisé pour identifier l’utilisateur sur un proxy qui requiert une authentification. Cet en-tête ne peut être récupéré que si la demande est envoyée au serveur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ connexion proxy de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère l’en-tête de Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ prise en charge du proxy de requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère l’en-tête de Proxy-Support.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**\_requête WinHTTP \_ publique**
</dt> <dd> <dl> <dt>



Reçoit les verbes HTTP disponibles sur ce serveur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_plage de requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère la plage d’octets d’une entité.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ en-têtes bruts de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit tous les en-têtes retournés par le serveur. Chaque en-tête se termine par « \\ 0 ». Un « \\ 0 » supplémentaire termine la liste des en-têtes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_ \_ en-têtes bruts de requête WinHTTP \_ \_ CRLF**
</dt> <dd> <dl> <dt>



Reçoit tous les en-têtes retournés par le serveur. Chaque en-tête est séparé par une séquence de retour chariot/saut de ligne (CR/LF).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_référenceur de requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit l’URI de la ressource dans laquelle l’URI demandé a été obtenu.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_actualisation des requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_méthode de \_ demande de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit le verbe HTTP qui est utilisé dans la demande, en général, obtenir ou poster.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_nouvelle tentative de requête WinHTTP \_ \_ après**
</dt> <dd> <dl> <dt>



Récupère la durée pendant laquelle le service est censé ne pas être disponible.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_serveur de requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère des informations sur le logiciel utilisé par le serveur d’origine pour traiter la demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_cookie de \_ jeu de requêtes WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit la valeur du cookie défini pour la demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**CODE d’état de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Reçoit le code d’état retourné par le serveur. Pour obtenir la liste des valeurs possibles, consultez [**codes d’État http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**texte d’état de la \_ requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Reçoit du texte supplémentaire retourné par le serveur sur la ligne de réponse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**titre de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsolète. Conservé pour la compatibilité des applications héritées.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**encodage de \_ transfert de requêtes WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Récupère le type de transformation qui a été appliqué au corps du message afin qu’il puisse être transféré en toute sécurité entre l’expéditeur et le destinataire.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_requête WinHTTP \_ sauf \_ modification \_ depuis**
</dt> <dd> <dl> <dt>



Récupère l’en-tête If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_ \_ mise à niveau des requêtes WinHTTP**
</dt> <dd> <dl> <dt>



Récupère les protocoles de communication supplémentaires pris en charge par le serveur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Reçoit tout ou partie de l’URI par lequel la ressource d’URI de requête peut être identifiée.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ agent utilisateur de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère des informations sur l’agent utilisateur qui a effectué la demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**variation de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère l’en-tête qui indique que l’entité a été sélectionnée à partir de plusieurs représentations disponibles de la réponse à l’aide de la négociation pilotée par le serveur.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**VERSION de la \_ requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère la version HTTP qui est présente dans la ligne d’État.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_requête WinHTTP \_ via**
</dt> <dd> <dl> <dt>



Récupère les protocoles et destinataires intermédiaires entre l’agent utilisateur et le serveur sur les demandes, et entre le serveur d’origine et le client sur les réponses.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_avertissement de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Récupère des informations supplémentaires sur l’état d’une réponse qui n’est peut-être pas reflétée par le code d’état de réponse.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**\_interrogation \_ WinHTTP \_ authentification Web**
</dt> <dd> <dl> <dt>



Récupère le schéma et le domaine d’authentification retournés par le serveur.


</dt> </dl> </dd> </dl>

Les indicateurs de modificateur sont utilisés conjointement avec un indicateur d’attribut pour modifier la requête. Les indicateurs de modificateur modifient le format des données retournées ou indiquent où la fonction [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) doit rechercher les informations.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**Numéro de l' \_ indicateur de requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Retourne les données sous la forme d’un nombre 32 bits pour les en-têtes dont la valeur est un nombre, tel que le code d’État.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_ \_ \_ en-têtes de demande d’indicateur de requête WinHTTP \_**
</dt> <dd> <dl> <dt>



Interroge uniquement les en-têtes de demande.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_indicateur de requête WinHTTP \_ \_ SystemTime**
</dt> <dd> <dl> <dt>



Retourne la valeur d’en-tête en tant que structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) , ce qui ne nécessite pas que l’application analyse les données. Utilisez pour les en-têtes dont la valeur est une chaîne de date/heure, telle que « Last-modified-Time ».


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**codes de fin de l' \_ indicateur de requête WinHTTP \_ \_**
</dt> <dd> <dl> <dt>


Requêtes de codes de fin de réponse. Avant d’interroger des codes de fin de réponse, vous devez appeler [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) jusqu’à ce qu’il retourne 0 octet lu.


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**encodage de câble de l' \_ indicateur de requête WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>


Par défaut, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) effectue une conversion Unicode avant de retourner l’en-tête qui a été interrogé. Si cet indicateur est défini, WinHttp retourne l’en-tête à l’appelant sans effectuer cette conversion.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]      |
| Serveur minimal pris en charge | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]   |
| En-tête                   | <dl> <dt>WinHTTP. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

* [Versions de WinHTTP](winhttp-versions.md)
