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
# <a name="query-info-flags-winineth"></a><span data-ttu-id="67be2-103">Indicateurs d’informations de requête (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="67be2-103">Query Info Flags (Wininet.h)</span></span>

<span data-ttu-id="67be2-104">Les listes suivantes contiennent les attributs et les modificateurs utilisés par [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) et [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67be2-104">The following lists contain the attributes and modifiers used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) and [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span></span>

<span data-ttu-id="67be2-105">Les indicateurs d’attribut sont utilisés par [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) pour indiquer les données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="67be2-105">The attribute flags are used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) to indicate what data to retrieve.</span></span> <span data-ttu-id="67be2-106">La plupart des indicateurs d’attribut sont directement mappés à un en-tête HTTP spécifique.</span><span class="sxs-lookup"><span data-stu-id="67be2-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="67be2-107">Il existe également des indicateurs spéciaux, tels que [ \_ \_ \_ les en-têtes bruts de requête http](/windows), qui ne sont pas associés à un en-tête spécifique.</span><span class="sxs-lookup"><span data-stu-id="67be2-107">There are also some special flags, such as [HTTP\_QUERY\_RAW\_HEADERS](/windows), that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="67be2-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**acceptation de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-109">24</span><span class="sxs-lookup"><span data-stu-id="67be2-109">24</span></span>
</dt> <dt>



<span data-ttu-id="67be2-110">Récupère les types de médias acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="67be2-110">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**jeu de caractères d’acceptation de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-112">25</span><span class="sxs-lookup"><span data-stu-id="67be2-112">25</span></span>
</dt> <dt>



<span data-ttu-id="67be2-113">Récupère les jeux de caractères acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="67be2-113">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**encodage d’acceptation de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-115">26</span><span class="sxs-lookup"><span data-stu-id="67be2-115">26</span></span>
</dt> <dt>



<span data-ttu-id="67be2-116">Récupère les valeurs de codage de contenu acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="67be2-116">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**langue d’acceptation de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-118">27</span><span class="sxs-lookup"><span data-stu-id="67be2-118">27</span></span>
</dt> <dt>



<span data-ttu-id="67be2-119">Récupère les langages naturels acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="67be2-119">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**plages d’acceptation de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-121">42</span><span class="sxs-lookup"><span data-stu-id="67be2-121">42</span></span>
</dt> <dt>



<span data-ttu-id="67be2-122">Récupère les types des demandes de plage acceptées pour une ressource.</span><span class="sxs-lookup"><span data-stu-id="67be2-122">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**âge de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-124">48</span><span class="sxs-lookup"><span data-stu-id="67be2-124">48</span></span>
</dt> <dt>



<span data-ttu-id="67be2-125">Récupère le champ d’en-tête de réponse d’âge, qui contient l’estimation de la durée de l’expéditeur depuis la génération de la réponse sur le serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="67be2-125">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**autorisation de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-127">7</span><span class="sxs-lookup"><span data-stu-id="67be2-127">7</span></span>
</dt> <dt>



<span data-ttu-id="67be2-128">Reçoit les verbes HTTP pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-128">Receives the HTTP verbs supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorisation de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-130">28</span><span class="sxs-lookup"><span data-stu-id="67be2-130">28</span></span>
</dt> <dt>



<span data-ttu-id="67be2-131">Récupère les informations d’identification utilisées pour une demande.</span><span class="sxs-lookup"><span data-stu-id="67be2-131">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_contrôle de \_ cache de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-133">49</span><span class="sxs-lookup"><span data-stu-id="67be2-133">49</span></span>
</dt> <dt>



<span data-ttu-id="67be2-134">Récupère les directives de contrôle de cache.</span><span class="sxs-lookup"><span data-stu-id="67be2-134">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**connexion à la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-136">23</span><span class="sxs-lookup"><span data-stu-id="67be2-136">23</span></span>
</dt> <dt>



<span data-ttu-id="67be2-137">Récupère toutes les options spécifiées pour une connexion particulière et ne doit pas être communiquée par les proxys sur des connexions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="67be2-137">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**BASE de contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-139">50</span><span class="sxs-lookup"><span data-stu-id="67be2-139">50</span></span>
</dt> <dt>



<span data-ttu-id="67be2-140">Récupère l’URI de base (Uniform Resource Identifier) pour la résolution des URL relatives dans l’entité.</span><span class="sxs-lookup"><span data-stu-id="67be2-140">Retrieves the base URI (Uniform Resource Identifier) for resolving relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**Description du contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-142">4</span><span class="sxs-lookup"><span data-stu-id="67be2-142">4</span></span>
</dt> <dt>



<span data-ttu-id="67be2-143">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-143">Obsolete.</span></span> <span data-ttu-id="67be2-144">Conservé pour la compatibilité des applications héritées uniquement.</span><span class="sxs-lookup"><span data-stu-id="67be2-144">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**DISPOSITION du contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-146">47</span><span class="sxs-lookup"><span data-stu-id="67be2-146">47</span></span>
</dt> <dt>



<span data-ttu-id="67be2-147">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-147">Obsolete.</span></span> <span data-ttu-id="67be2-148">Conservé pour la compatibilité des applications héritées uniquement.</span><span class="sxs-lookup"><span data-stu-id="67be2-148">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**encodage du contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-150">29</span><span class="sxs-lookup"><span data-stu-id="67be2-150">29</span></span>
</dt> <dt>



<span data-ttu-id="67be2-151">Récupère tous les codages de contenu supplémentaires qui ont été appliqués à la ressource entière.</span><span class="sxs-lookup"><span data-stu-id="67be2-151">Retrieves any additional content codings that have been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**ID de contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-153">3</span><span class="sxs-lookup"><span data-stu-id="67be2-153">3</span></span>
</dt> <dt>



<span data-ttu-id="67be2-154">Récupère l’identification du contenu.</span><span class="sxs-lookup"><span data-stu-id="67be2-154">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**langage de contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-156">6</span><span class="sxs-lookup"><span data-stu-id="67be2-156">6</span></span>
</dt> <dt>



<span data-ttu-id="67be2-157">Récupère la langue dans laquelle se trouve le contenu.</span><span class="sxs-lookup"><span data-stu-id="67be2-157">Retrieves the language that the content is in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**longueur du contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-159">5</span><span class="sxs-lookup"><span data-stu-id="67be2-159">5</span></span>
</dt> <dt>



<span data-ttu-id="67be2-160">Récupère la taille de la ressource, en octets.</span><span class="sxs-lookup"><span data-stu-id="67be2-160">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**emplacement du contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-162">51</span><span class="sxs-lookup"><span data-stu-id="67be2-162">51</span></span>
</dt> <dt>



<span data-ttu-id="67be2-163">Récupère l’emplacement de la ressource de l’entité incluse dans le message.</span><span class="sxs-lookup"><span data-stu-id="67be2-163">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**MD5 du contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-165">52</span><span class="sxs-lookup"><span data-stu-id="67be2-165">52</span></span>
</dt> <dt>



<span data-ttu-id="67be2-166">Récupère un condensé MD5 du corps d’entité afin de fournir un MIC (message integrity check) de bout en bout pour le corps d’entité.</span><span class="sxs-lookup"><span data-stu-id="67be2-166">Retrieves an MD5 digest of the entity-body for the purpose of providing an end-to-end message integrity check (MIC) for the entity-body.</span></span> <span data-ttu-id="67be2-167">Pour plus d’informations, consultez RFC1864, le champ d’en-tête Content-MD5, à l’adresse [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .</span><span class="sxs-lookup"><span data-stu-id="67be2-167">For more information, see RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**plage de contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-169">53</span><span class="sxs-lookup"><span data-stu-id="67be2-169">53</span></span>
</dt> <dt>



<span data-ttu-id="67be2-170">Récupère l’emplacement dans le corps de l’entité complète où le corps de l’entité partielle doit être inséré et la taille totale du corps de l’entité complète.</span><span class="sxs-lookup"><span data-stu-id="67be2-170">Retrieves the location in the full entity-body where the partial entity-body should be inserted and the total size of the full entity-body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**encodage de transfert de contenu de \_ requête HTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-172">2</span><span class="sxs-lookup"><span data-stu-id="67be2-172">2</span></span>
</dt> <dt>



<span data-ttu-id="67be2-173">Reçoit le code de contenu supplémentaire qui a été appliqué à la ressource.</span><span class="sxs-lookup"><span data-stu-id="67be2-173">Receives the additional content coding that has been applied to the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**TYPE de contenu de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-175">1</span><span class="sxs-lookup"><span data-stu-id="67be2-175">1</span></span>
</dt> <dt>



<span data-ttu-id="67be2-176">Reçoit le type de contenu de la ressource (par exemple, text/html).</span><span class="sxs-lookup"><span data-stu-id="67be2-176">Receives the content type of the resource (such as text/html).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-178">44</span><span class="sxs-lookup"><span data-stu-id="67be2-178">44</span></span>
</dt> <dt>



<span data-ttu-id="67be2-179">Récupère tous les cookies associés à la requête.</span><span class="sxs-lookup"><span data-stu-id="67be2-179">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**coût de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-181">15</span><span class="sxs-lookup"><span data-stu-id="67be2-181">15</span></span>
</dt> <dt>



<span data-ttu-id="67be2-182">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="67be2-182">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_requête HTTP \_ personnalisée**</span><span class="sxs-lookup"><span data-stu-id="67be2-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-184">65535</span><span class="sxs-lookup"><span data-stu-id="67be2-184">65535</span></span>
</dt> <dt>



<span data-ttu-id="67be2-185">Fait en sorte que [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) recherche le nom d’en-tête spécifié dans *lpvBuffer* et stocke les données d’en-tête dans *lpvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="67be2-185">Causes [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to search for the header name specified in *lpvBuffer* and store the header data in *lpvBuffer*.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**Date de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-187">9</span><span class="sxs-lookup"><span data-stu-id="67be2-187">9</span></span>
</dt> <dt>



<span data-ttu-id="67be2-188">Reçoit la date et l’heure d’origine du message.</span><span class="sxs-lookup"><span data-stu-id="67be2-188">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_requête HTTP \_ dérivée \_ de**</span><span class="sxs-lookup"><span data-stu-id="67be2-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-190">14</span><span class="sxs-lookup"><span data-stu-id="67be2-190">14</span></span>
</dt> <dt>



<span data-ttu-id="67be2-191">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="67be2-191">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ en-têtes d’écho de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP\_QUERY\_ECHO\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-193">73</span><span class="sxs-lookup"><span data-stu-id="67be2-193">73</span></span>
</dt> <dt>



<span data-ttu-id="67be2-194">Actuellement non implémenté.</span><span class="sxs-lookup"><span data-stu-id="67be2-194">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_ \_ en-têtes de requête http Echo \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="67be2-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP\_QUERY\_ECHO\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-196">74</span><span class="sxs-lookup"><span data-stu-id="67be2-196">74</span></span>
</dt> <dt>



<span data-ttu-id="67be2-197">Actuellement non implémenté.</span><span class="sxs-lookup"><span data-stu-id="67be2-197">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**réponse d’écho de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP\_QUERY\_ECHO\_REPLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-199">72</span><span class="sxs-lookup"><span data-stu-id="67be2-199">72</span></span>
</dt> <dt>



<span data-ttu-id="67be2-200">Actuellement non implémenté.</span><span class="sxs-lookup"><span data-stu-id="67be2-200">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_demande d' \_ écho de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP\_QUERY\_ECHO\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-202">71</span><span class="sxs-lookup"><span data-stu-id="67be2-202">71</span></span>
</dt> <dt>



<span data-ttu-id="67be2-203">Actuellement non implémenté.</span><span class="sxs-lookup"><span data-stu-id="67be2-203">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**ETag de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-205">54</span><span class="sxs-lookup"><span data-stu-id="67be2-205">54</span></span>
</dt> <dt>



<span data-ttu-id="67be2-206">Récupère la balise d’entité de l’entité associée.</span><span class="sxs-lookup"><span data-stu-id="67be2-206">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_requête HTTP \_ attendue**</span><span class="sxs-lookup"><span data-stu-id="67be2-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-208">68</span><span class="sxs-lookup"><span data-stu-id="67be2-208">68</span></span>
</dt> <dt>



<span data-ttu-id="67be2-209">Récupère l’en-tête Expect, qui indique si l’application cliente doit attendre des réponses de série 100.</span><span class="sxs-lookup"><span data-stu-id="67be2-209">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**expiration de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-211">10</span><span class="sxs-lookup"><span data-stu-id="67be2-211">10</span></span>
</dt> <dt>



<span data-ttu-id="67be2-212">Reçoit la date et l’heure après lesquelles la ressource doit être considérée comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-212">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_requête HTTP \_ transférée**</span><span class="sxs-lookup"><span data-stu-id="67be2-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-214">30</span><span class="sxs-lookup"><span data-stu-id="67be2-214">30</span></span>
</dt> <dt>



<span data-ttu-id="67be2-215">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-215">Obsolete.</span></span> <span data-ttu-id="67be2-216">Conservé pour la compatibilité des applications héritées uniquement.</span><span class="sxs-lookup"><span data-stu-id="67be2-216">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_requête HTTP \_ à partir de**</span><span class="sxs-lookup"><span data-stu-id="67be2-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-218">31</span><span class="sxs-lookup"><span data-stu-id="67be2-218">31</span></span>
</dt> <dt>



<span data-ttu-id="67be2-219">Récupère l’adresse de messagerie de l’utilisateur humain qui contrôle l’agent utilisateur demandeur si l’en-tête from est donné.</span><span class="sxs-lookup"><span data-stu-id="67be2-219">Retrieves the email address for the human user who controls the requesting user agent if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_hôte de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-221">55</span><span class="sxs-lookup"><span data-stu-id="67be2-221">55</span></span>
</dt> <dt>



<span data-ttu-id="67be2-222">Récupère l’hôte Internet et le numéro de port de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="67be2-222">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_requête HTTP \_ si la correspondance est \_ trouvée**</span><span class="sxs-lookup"><span data-stu-id="67be2-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-224">56</span><span class="sxs-lookup"><span data-stu-id="67be2-224">56</span></span>
</dt> <dt>



<span data-ttu-id="67be2-225">Récupère le contenu du champ d’en-tête de demande If-Match.</span><span class="sxs-lookup"><span data-stu-id="67be2-225">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**requête HTTP en \_ \_ cas de \_ modification \_ depuis**</span><span class="sxs-lookup"><span data-stu-id="67be2-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-227">32</span><span class="sxs-lookup"><span data-stu-id="67be2-227">32</span></span>
</dt> <dt>



<span data-ttu-id="67be2-228">Récupère le contenu de l’en-tête If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="67be2-228">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_requête HTTP \_ si \_ aucune ne \_ correspond**</span><span class="sxs-lookup"><span data-stu-id="67be2-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-230">57</span><span class="sxs-lookup"><span data-stu-id="67be2-230">57</span></span>
</dt> <dt>



<span data-ttu-id="67be2-231">Récupère le contenu du champ d’en-tête de demande If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="67be2-231">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_requête HTTP \_ si la \_ plage**</span><span class="sxs-lookup"><span data-stu-id="67be2-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-233">58</span><span class="sxs-lookup"><span data-stu-id="67be2-233">58</span></span>
</dt> <dt>



<span data-ttu-id="67be2-234">Récupère le contenu du champ d’en-tête de demande If-Range.</span><span class="sxs-lookup"><span data-stu-id="67be2-234">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="67be2-235">Cet en-tête permet à l’application cliente de vérifier que l’entité liée à une copie partielle de l’entité dans le cache de l’application cliente n’a pas été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="67be2-235">This header enables the client application to verify that the entity related to a partial copy of the entity in the client application cache has not been updated.</span></span> <span data-ttu-id="67be2-236">Si l’entité n’a pas été mise à jour, envoyez les composants que l’application cliente est manquante.</span><span class="sxs-lookup"><span data-stu-id="67be2-236">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="67be2-237">Si l’entité a été mise à jour, envoyez la totalité de l’entité mise à jour.</span><span class="sxs-lookup"><span data-stu-id="67be2-237">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**requête HTTP si elle n’a pas été \_ \_ \_ modifiée \_ depuis**</span><span class="sxs-lookup"><span data-stu-id="67be2-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-239">59</span><span class="sxs-lookup"><span data-stu-id="67be2-239">59</span></span>
</dt> <dt>



<span data-ttu-id="67be2-240">Récupère le contenu du champ d’en-tête de demande If-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="67be2-240">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ dernière \_ modification de la requête http**</span><span class="sxs-lookup"><span data-stu-id="67be2-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**HTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-242">11</span><span class="sxs-lookup"><span data-stu-id="67be2-242">11</span></span>
</dt> <dt>



<span data-ttu-id="67be2-243">Reçoit la date et l’heure auxquelles le serveur estime que la ressource a été modifiée pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="67be2-243">Receives the date and time at which the server believes the resource was last modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**lien de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-245">16</span><span class="sxs-lookup"><span data-stu-id="67be2-245">16</span></span>
</dt> <dt>



<span data-ttu-id="67be2-246">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-246">Obsolete.</span></span> <span data-ttu-id="67be2-247">Conservé pour la compatibilité des applications héritées uniquement.</span><span class="sxs-lookup"><span data-stu-id="67be2-247">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**emplacement de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-249">33</span><span class="sxs-lookup"><span data-stu-id="67be2-249">33</span></span>
</dt> <dt>



<span data-ttu-id="67be2-250">Récupère le Uniform Resource Identifier absolu (URI) utilisé dans un en-tête de réponse d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="67be2-250">Retrieves the absolute Uniform Resource Identifier (URI) used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**Max. des \_ requêtes http \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-252">78</span><span class="sxs-lookup"><span data-stu-id="67be2-252">78</span></span>
</dt> <dt>



<span data-ttu-id="67be2-253">N’est pas un indicateur de requête.</span><span class="sxs-lookup"><span data-stu-id="67be2-253">Not a query flag.</span></span> <span data-ttu-id="67be2-254">Indique la valeur maximale d’une \_ valeur de requête HTTP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="67be2-254">Indicates the maximum value of an HTTP\_QUERY\_\* value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ transferts max. des requêtes http \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-256">60</span><span class="sxs-lookup"><span data-stu-id="67be2-256">60</span></span>
</dt> <dt>



<span data-ttu-id="67be2-257">Récupère le nombre de proxies ou de passerelles qui peuvent transférer la requête vers le serveur entrant suivant.</span><span class="sxs-lookup"><span data-stu-id="67be2-257">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ID du \_ message de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-259">12</span><span class="sxs-lookup"><span data-stu-id="67be2-259">12</span></span>
</dt> <dt>



<span data-ttu-id="67be2-260">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="67be2-260">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ version MIME de la requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-262">0</span><span class="sxs-lookup"><span data-stu-id="67be2-262">0</span></span>
</dt> <dt>



<span data-ttu-id="67be2-263">Reçoit la version du protocole MIME qui a été utilisée pour construire le message.</span><span class="sxs-lookup"><span data-stu-id="67be2-263">Receives the version of the MIME protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**URI d’origine de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-265">34</span><span class="sxs-lookup"><span data-stu-id="67be2-265">34</span></span>
</dt> <dt>



<span data-ttu-id="67be2-266">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-266">Obsolete.</span></span> <span data-ttu-id="67be2-267">Conservé pour la compatibilité des applications héritées uniquement.</span><span class="sxs-lookup"><span data-stu-id="67be2-267">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-269">17</span><span class="sxs-lookup"><span data-stu-id="67be2-269">17</span></span>
</dt> <dt>



<span data-ttu-id="67be2-270">Reçoit les directives spécifiques à l’implémentation qui peuvent s’appliquer à n’importe quel destinataire le long de la chaîne de requête/réponse.</span><span class="sxs-lookup"><span data-stu-id="67be2-270">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_authentification du \_ proxy de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-272">41</span><span class="sxs-lookup"><span data-stu-id="67be2-272">41</span></span>
</dt> <dt>



<span data-ttu-id="67be2-273">Récupère le schéma et le domaine d’authentification retournés par le proxy.</span><span class="sxs-lookup"><span data-stu-id="67be2-273">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_autorisation du \_ proxy de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-275">61</span><span class="sxs-lookup"><span data-stu-id="67be2-275">61</span></span>
</dt> <dt>



<span data-ttu-id="67be2-276">Récupère l’en-tête utilisé pour identifier l’utilisateur sur un proxy qui requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="67be2-276">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="67be2-277">Cet en-tête ne peut être récupéré que si la demande est envoyée au serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-277">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_ \_ connexion proxy de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-279">69</span><span class="sxs-lookup"><span data-stu-id="67be2-279">69</span></span>
</dt> <dt>



<span data-ttu-id="67be2-280">Récupère l’en-tête de Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="67be2-280">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_requête HTTP \_ publique**</span><span class="sxs-lookup"><span data-stu-id="67be2-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-282">8</span><span class="sxs-lookup"><span data-stu-id="67be2-282">8</span></span>
</dt> <dt>



<span data-ttu-id="67be2-283">Reçoit les méthodes disponibles sur ce serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-283">Receives methods available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_plage de requêtes http \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-285">62</span><span class="sxs-lookup"><span data-stu-id="67be2-285">62</span></span>
</dt> <dt>



<span data-ttu-id="67be2-286">Récupère la plage d’octets d’une entité.</span><span class="sxs-lookup"><span data-stu-id="67be2-286">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ en-têtes bruts de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-288">21</span><span class="sxs-lookup"><span data-stu-id="67be2-288">21</span></span>
</dt> <dt>



<span data-ttu-id="67be2-289">Reçoit tous les en-têtes retournés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-289">Receives all the headers returned by the server.</span></span> <span data-ttu-id="67be2-290">Chaque en-tête se termine par « \\ 0 ».</span><span class="sxs-lookup"><span data-stu-id="67be2-290">Each header is terminated by "\\0".</span></span> <span data-ttu-id="67be2-291">Un « \\ 0 » supplémentaire termine la liste des en-têtes.</span><span class="sxs-lookup"><span data-stu-id="67be2-291">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_ \_ en-têtes bruts de requête HTTP \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="67be2-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-293">22</span><span class="sxs-lookup"><span data-stu-id="67be2-293">22</span></span>
</dt> <dt>



<span data-ttu-id="67be2-294">Reçoit tous les en-têtes retournés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-294">Receives all the headers returned by the server.</span></span> <span data-ttu-id="67be2-295">Chaque en-tête est séparé par une séquence de retour chariot/saut de ligne (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="67be2-295">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**référant à la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-297">35</span><span class="sxs-lookup"><span data-stu-id="67be2-297">35</span></span>
</dt> <dt>



<span data-ttu-id="67be2-298">Reçoit le Uniform Resource Identifier (URI) de la ressource dans laquelle l’URI demandé a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="67be2-298">Receives the Uniform Resource Identifier (URI) of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_actualisation des requêtes http \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-300">46</span><span class="sxs-lookup"><span data-stu-id="67be2-300">46</span></span>
</dt> <dt>



<span data-ttu-id="67be2-301">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-301">Obsolete.</span></span> <span data-ttu-id="67be2-302">Conservé pour la compatibilité des applications héritées uniquement.</span><span class="sxs-lookup"><span data-stu-id="67be2-302">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**méthode de requête de \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-304">45</span><span class="sxs-lookup"><span data-stu-id="67be2-304">45</span></span>
</dt> <dt>



<span data-ttu-id="67be2-305">Reçoit le verbe HTTP qui est utilisé dans la demande, en général, obtenir ou poster.</span><span class="sxs-lookup"><span data-stu-id="67be2-305">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**\_nouvelle tentative de requête HTTP \_ \_ après**</span><span class="sxs-lookup"><span data-stu-id="67be2-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-307">36</span><span class="sxs-lookup"><span data-stu-id="67be2-307">36</span></span>
</dt> <dt>



<span data-ttu-id="67be2-308">Récupère la durée pendant laquelle le service est censé ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="67be2-308">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_serveur de requêtes http \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-310">37</span><span class="sxs-lookup"><span data-stu-id="67be2-310">37</span></span>
</dt> <dt>



<span data-ttu-id="67be2-311">Récupère les données relatives au logiciel utilisé par le serveur d’origine pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="67be2-311">Retrieves data about the software used by the origin server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie de \_ jeu de requêtes http \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-313">43</span><span class="sxs-lookup"><span data-stu-id="67be2-313">43</span></span>
</dt> <dt>



<span data-ttu-id="67be2-314">Reçoit la valeur du cookie défini pour la demande.</span><span class="sxs-lookup"><span data-stu-id="67be2-314">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**CODE d’état de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-316">19</span><span class="sxs-lookup"><span data-stu-id="67be2-316">19</span></span>
</dt> <dt>



<span data-ttu-id="67be2-317">Reçoit le code d’état retourné par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-317">Receives the status code returned by the server.</span></span> <span data-ttu-id="67be2-318">Pour plus d’informations et pour obtenir la liste des valeurs possibles, consultez [**codes d’État http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="67be2-318">For more information and a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**texte d’état de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-320">20</span><span class="sxs-lookup"><span data-stu-id="67be2-320">20</span></span>
</dt> <dt>



<span data-ttu-id="67be2-321">Reçoit tout texte supplémentaire retourné par le serveur sur la ligne de réponse.</span><span class="sxs-lookup"><span data-stu-id="67be2-321">Receives any additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**titre de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-323">38</span><span class="sxs-lookup"><span data-stu-id="67be2-323">38</span></span>
</dt> <dt>



<span data-ttu-id="67be2-324">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="67be2-324">Obsolete.</span></span> <span data-ttu-id="67be2-325">Conservé pour la compatibilité des applications héritées uniquement.</span><span class="sxs-lookup"><span data-stu-id="67be2-325">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**encodage de \_ transfert de requêtes http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-327">63</span><span class="sxs-lookup"><span data-stu-id="67be2-327">63</span></span>
</dt> <dt>



<span data-ttu-id="67be2-328">Récupère le type de transformation qui a été appliqué au corps du message afin qu’il puisse être transféré en toute sécurité entre l’expéditeur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="67be2-328">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_requête HTTP \_ sauf \_ modification \_ depuis**</span><span class="sxs-lookup"><span data-stu-id="67be2-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-330">70</span><span class="sxs-lookup"><span data-stu-id="67be2-330">70</span></span>
</dt> <dt>



<span data-ttu-id="67be2-331">Récupère l’en-tête If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="67be2-331">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_ \_ mise à niveau de la requête http**</span><span class="sxs-lookup"><span data-stu-id="67be2-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-333">64</span><span class="sxs-lookup"><span data-stu-id="67be2-333">64</span></span>
</dt> <dt>



<span data-ttu-id="67be2-334">Récupère les protocoles de communication supplémentaires pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-334">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-336">13</span><span class="sxs-lookup"><span data-stu-id="67be2-336">13</span></span>
</dt> <dt>



<span data-ttu-id="67be2-337">Reçoit tout ou partie des URI (Uniform Resource Identifier) par lesquels la ressource d’URI de requête peut être identifiée.</span><span class="sxs-lookup"><span data-stu-id="67be2-337">Receives some or all of the Uniform Resource Identifiers (URIs) by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_ \_ agent utilisateur de la requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-339">39</span><span class="sxs-lookup"><span data-stu-id="67be2-339">39</span></span>
</dt> <dt>



<span data-ttu-id="67be2-340">Récupère les données relatives à l’agent utilisateur qui a effectué la demande.</span><span class="sxs-lookup"><span data-stu-id="67be2-340">Retrieves data about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**la \_ requête HTTP \_ varie**</span><span class="sxs-lookup"><span data-stu-id="67be2-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-342">65</span><span class="sxs-lookup"><span data-stu-id="67be2-342">65</span></span>
</dt> <dt>



<span data-ttu-id="67be2-343">Récupère l’en-tête qui indique que l’entité a été sélectionnée à partir de plusieurs représentations disponibles de la réponse à l’aide de la négociation pilotée par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-343">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**VERSION de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-345">18</span><span class="sxs-lookup"><span data-stu-id="67be2-345">18</span></span>
</dt> <dt>



<span data-ttu-id="67be2-346">Reçoit le code de la dernière réponse renvoyée par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-346">Receives the last response code returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_requête HTTP \_ via**</span><span class="sxs-lookup"><span data-stu-id="67be2-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-348">66</span><span class="sxs-lookup"><span data-stu-id="67be2-348">66</span></span>
</dt> <dt>



<span data-ttu-id="67be2-349">Récupère les protocoles et destinataires intermédiaires entre l’agent utilisateur et le serveur sur les demandes, et entre le serveur d’origine et le client sur les réponses.</span><span class="sxs-lookup"><span data-stu-id="67be2-349">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_avertissement de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-351">67</span><span class="sxs-lookup"><span data-stu-id="67be2-351">67</span></span>
</dt> <dt>



<span data-ttu-id="67be2-352">Récupère des données supplémentaires sur l’état d’une réponse qui n’est peut-être pas reflétée par le code d’état de réponse.</span><span class="sxs-lookup"><span data-stu-id="67be2-352">Retrieves additional data about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_ \_ authentification Web de la requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-354">40</span><span class="sxs-lookup"><span data-stu-id="67be2-354">40</span></span>
</dt> <dt>



<span data-ttu-id="67be2-355">Récupère le schéma et le domaine d’authentification retournés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-355">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_options de \_ \_ type de contenu X \_ \_ de la requête http**</span><span class="sxs-lookup"><span data-stu-id="67be2-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP\_QUERY\_X\_CONTENT\_TYPE\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-357">79</span><span class="sxs-lookup"><span data-stu-id="67be2-357">79</span></span>
</dt> <dt>



<span data-ttu-id="67be2-358">Récupère la valeur d’en-tête X-Content-type-options.</span><span class="sxs-lookup"><span data-stu-id="67be2-358">Retrieves the X-Content-Type-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**P3P de la \_ requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP\_QUERY\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-360">80</span><span class="sxs-lookup"><span data-stu-id="67be2-360">80</span></span>
</dt> <dt>



<span data-ttu-id="67be2-361">Récupère la valeur d’en-tête P3P.</span><span class="sxs-lookup"><span data-stu-id="67be2-361">Retrieves the P3P header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Requête HTTP \_ X \_ P2P-P2P \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP\_QUERY\_X\_P2P\_PEERDIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-363">81</span><span class="sxs-lookup"><span data-stu-id="67be2-363">81</span></span>
</dt> <dt>



<span data-ttu-id="67be2-364">Récupère la valeur d’en-tête X-P2P-PeerDist.</span><span class="sxs-lookup"><span data-stu-id="67be2-364">Retrieves the X-P2P-PeerDist header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_traduction de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP\_QUERY\_TRANSLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-366">82</span><span class="sxs-lookup"><span data-stu-id="67be2-366">82</span></span>
</dt> <dt>



<span data-ttu-id="67be2-367">Récupère la valeur d’en-tête Translate.</span><span class="sxs-lookup"><span data-stu-id="67be2-367">Retrieves the translate header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_requête HTTP \_ X \_ \_ compatible avec UA**</span><span class="sxs-lookup"><span data-stu-id="67be2-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP\_QUERY\_X\_UA\_COMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-369">83</span><span class="sxs-lookup"><span data-stu-id="67be2-369">83</span></span>
</dt> <dt>



<span data-ttu-id="67be2-370">Récupère la valeur d’en-tête X-UA-compatible.</span><span class="sxs-lookup"><span data-stu-id="67be2-370">Retrieves the X-UA-Compatible header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ style par défaut de la requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP\_QUERY\_DEFAULT\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-372">84</span><span class="sxs-lookup"><span data-stu-id="67be2-372">84</span></span>
</dt> <dt>



<span data-ttu-id="67be2-373">Récupère la valeur d’en-tête Default-Style.</span><span class="sxs-lookup"><span data-stu-id="67be2-373">Retrieves the Default-Style header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_options de \_ \_ Frame X \_ de la requête http**</span><span class="sxs-lookup"><span data-stu-id="67be2-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP\_QUERY\_X\_FRAME\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-375">85 %</span><span class="sxs-lookup"><span data-stu-id="67be2-375">85</span></span>
</dt> <dt>



<span data-ttu-id="67be2-376">Récupère la valeur d’en-tête X-Frame-options.</span><span class="sxs-lookup"><span data-stu-id="67be2-376">Retrieves the X-Frame-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**\_requête HTTP \_ X \_ \_ Protection XSS**</span><span class="sxs-lookup"><span data-stu-id="67be2-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP\_QUERY\_X\_XSS\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-378">86</span><span class="sxs-lookup"><span data-stu-id="67be2-378">86</span></span>
</dt> <dt>



<span data-ttu-id="67be2-379">Récupère la valeur d’en-tête X-XSS-protection.</span><span class="sxs-lookup"><span data-stu-id="67be2-379">Retrieves the X-XSS-Protection header value.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="67be2-380">Les indicateurs de modificateur sont utilisés conjointement avec un indicateur d’attribut pour modifier la requête.</span><span class="sxs-lookup"><span data-stu-id="67be2-380">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="67be2-381">Les indicateurs de modificateur modifient le format des données retournées ou indiquent où [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) doit rechercher les données.</span><span class="sxs-lookup"><span data-stu-id="67be2-381">Modifier flags either modify the format of the data returned or indicate where [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) should search for the data.</span></span>

<dl> <dt>

<span data-ttu-id="67be2-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_fusion d' \_ indicateur de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP\_QUERY\_FLAG\_COALESCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-383">0x10000000</span><span class="sxs-lookup"><span data-stu-id="67be2-383">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="67be2-384">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="67be2-384">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**Numéro de l' \_ indicateur de requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-386">0x20000000</span><span class="sxs-lookup"><span data-stu-id="67be2-386">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="67be2-387">Retourne les données sous la forme d’un nombre 32 bits pour les en-têtes dont la valeur est un nombre, tel que le code d’État.</span><span class="sxs-lookup"><span data-stu-id="67be2-387">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_ \_ \_ en-têtes de demande d’indicateur de requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="67be2-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-389">0x80000000</span><span class="sxs-lookup"><span data-stu-id="67be2-389">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="67be2-390">Interroge uniquement les en-têtes de demande.</span><span class="sxs-lookup"><span data-stu-id="67be2-390">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67be2-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_indicateur de requête HTTP \_ \_ SystemTime**</span><span class="sxs-lookup"><span data-stu-id="67be2-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67be2-392">0x40000000</span><span class="sxs-lookup"><span data-stu-id="67be2-392">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="67be2-393">Retourne la valeur d’en-tête en tant que structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , ce qui ne nécessite pas que l’application analyse les données.</span><span class="sxs-lookup"><span data-stu-id="67be2-393">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="67be2-394">Utilisez pour les en-têtes dont la valeur est une chaîne de date/heure, telle que « Last-modified-Time ».</span><span class="sxs-lookup"><span data-stu-id="67be2-394">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67be2-395">Notes</span><span class="sxs-lookup"><span data-stu-id="67be2-395">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67be2-396">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="67be2-396">WinINet does not support server implementations.</span></span> <span data-ttu-id="67be2-397">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="67be2-397">In addition, it should not be used from a service.</span></span> <span data-ttu-id="67be2-398">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="67be2-398">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67be2-399">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67be2-399">Requirements</span></span>



| <span data-ttu-id="67be2-400">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67be2-400">Requirement</span></span> | <span data-ttu-id="67be2-401">Valeur</span><span class="sxs-lookup"><span data-stu-id="67be2-401">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="67be2-402">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67be2-402">Minimum supported client</span></span><br/> | <span data-ttu-id="67be2-403">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67be2-403">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="67be2-404">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67be2-404">Minimum supported server</span></span><br/> | <span data-ttu-id="67be2-405">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67be2-405">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="67be2-406">En-tête</span><span class="sxs-lookup"><span data-stu-id="67be2-406">Header</span></span><br/>                   | <dl> <span data-ttu-id="67be2-407"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="67be2-407"><dt>Wininet.h</dt></span></span> </dl> |



 

