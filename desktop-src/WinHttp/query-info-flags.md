---
description: Ces attributs et modificateurs sont utilisés par WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Indicateurs d’informations de requête (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8a7f95f0e093f175901e4bed30f4055a04b8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396624"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="39a2d-103">Indicateurs d’informations de requête (Winhttp.h)</span><span class="sxs-lookup"><span data-stu-id="39a2d-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="39a2d-104">Ces attributs et modificateurs sont utilisés par [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="39a2d-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="39a2d-105">Les indicateurs d’attribut sont utilisés par [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) pour indiquer les informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="39a2d-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="39a2d-106">La plupart des indicateurs d’attribut sont directement mappés à un en-tête HTTP spécifique.</span><span class="sxs-lookup"><span data-stu-id="39a2d-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="39a2d-107">Il existe également des indicateurs spéciaux, tels que \_ \_ les en-têtes de requête WinHTTP bruts \_ , qui ne sont pas associés à un en-tête spécifique.</span><span class="sxs-lookup"><span data-stu-id="39a2d-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="39a2d-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**acceptation de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-109">Récupère les types de médias acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**jeu de caractères d' \_ acceptation de requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-111">Récupère les jeux de caractères acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**encodage d' \_ acceptation de requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-113">Récupère les valeurs de codage de contenu acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**langue d’acceptation de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-115">Récupère les langages naturels acceptables pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_plages d' \_ acceptation des requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-117">Récupère les types des demandes de plage acceptées pour une ressource.</span><span class="sxs-lookup"><span data-stu-id="39a2d-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_âge des requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-119">Récupère le champ d’en-tête de réponse d’âge, qui contient l’estimation de la durée de l’expéditeur depuis la génération de la réponse au niveau du serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="39a2d-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**autorisation de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-121">Reçoit les [**verbes HTTP**](glossary.md) pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-121">Receives the [**HTTP verbs**](glossary.md) supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ informations d’authentification de la requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-123">Récupère l’en-tête de Authentication-Info.</span><span class="sxs-lookup"><span data-stu-id="39a2d-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_autorisation de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-125">Récupère les informations d’identification utilisées pour une demande.</span><span class="sxs-lookup"><span data-stu-id="39a2d-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ contrôle du cache des requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-127">Récupère les directives de contrôle de cache.</span><span class="sxs-lookup"><span data-stu-id="39a2d-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**connexion à la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-129">Récupère toutes les options spécifiées pour une connexion particulière et ne doit pas être communiquée par les proxys sur des connexions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="39a2d-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_base de \_ contenu de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-131">Récupère le Uniform Resource Identifier de base (URI) pour résoudre des URL relatives dans l’entité.</span><span class="sxs-lookup"><span data-stu-id="39a2d-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**Description du contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-133">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-133">Obsolete.</span></span> <span data-ttu-id="39a2d-134">Conservé pour la compatibilité des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="39a2d-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSITION du contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-136">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-136">Obsolete.</span></span> <span data-ttu-id="39a2d-137">Conservé pour la compatibilité des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="39a2d-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**encodage du contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-139">Récupère le codage de contenu supplémentaire qui a été appliqué à l’ensemble de la ressource.</span><span class="sxs-lookup"><span data-stu-id="39a2d-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**ID de contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-141">Récupère l’identification du contenu.</span><span class="sxs-lookup"><span data-stu-id="39a2d-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**langue de contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-143">Récupère la langue dans laquelle le contenu est écrit.</span><span class="sxs-lookup"><span data-stu-id="39a2d-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**longueur du contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-145">Récupère la taille de la ressource, en octets.</span><span class="sxs-lookup"><span data-stu-id="39a2d-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**emplacement du contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-147">Récupère l’emplacement de la ressource de l’entité incluse dans le message.</span><span class="sxs-lookup"><span data-stu-id="39a2d-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**MD5 du contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-149">Récupère un condensé MD5 du corps d’entité afin de fournir une vérification de l’intégrité des messages de bout en bout pour le corps de l’entité.</span><span class="sxs-lookup"><span data-stu-id="39a2d-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="39a2d-150">Pour plus d’informations, consultez la [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span><span class="sxs-lookup"><span data-stu-id="39a2d-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**plage de contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-152">Récupère l’emplacement dans le corps de l’entité complète où le corps de l’entité partielle doit être inséré et la taille totale du corps de l’entité complète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**encodage de transfert de contenu de \_ requête WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-154">Récupère une transformation d’encodage applicable à un corps d’entité.</span><span class="sxs-lookup"><span data-stu-id="39a2d-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="39a2d-155">Il est possible qu’il ait déjà été appliqué, qu’il doive être appliqué ou éventuellement applicable.</span><span class="sxs-lookup"><span data-stu-id="39a2d-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TYPE de contenu de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-157">Reçoit le type de contenu de la ressource, tel que texte ou html.</span><span class="sxs-lookup"><span data-stu-id="39a2d-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_cookie de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-159">Récupère tous les cookies associés à la requête.</span><span class="sxs-lookup"><span data-stu-id="39a2d-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_coût des requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-161">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="39a2d-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**\_requête WinHTTP \_ personnalisée**</span><span class="sxs-lookup"><span data-stu-id="39a2d-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-163">Fait en sorte que [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) recherche le nom d’en-tête spécifié dans le paramètre *pwszName* et stocke les informations d’en-tête dans *lpBuffer*.</span><span class="sxs-lookup"><span data-stu-id="39a2d-163">Causes [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="39a2d-164">Une application peut utiliser **l' \_ option WinHTTP \_ recevoir le \_ \_ délai de réponse** pour limiter la durée maximale pendant laquelle cette requête attend que tous les en-têtes soient reçus.</span><span class="sxs-lookup"><span data-stu-id="39a2d-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**Date de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-166">Reçoit la date et l’heure d’origine du message.</span><span class="sxs-lookup"><span data-stu-id="39a2d-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_requête WinHTTP \_ dérivée \_ de**</span><span class="sxs-lookup"><span data-stu-id="39a2d-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-168">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="39a2d-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-170">Récupère la balise d’entité de l’entité associée.</span><span class="sxs-lookup"><span data-stu-id="39a2d-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_requête WinHTTP \_ attendue**</span><span class="sxs-lookup"><span data-stu-id="39a2d-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-172">Récupère l’en-tête Expect, qui indique si l’application cliente doit attendre des réponses de série 100.</span><span class="sxs-lookup"><span data-stu-id="39a2d-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**expiration de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-174">Reçoit la date et l’heure après lesquelles la ressource doit être considérée comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_requête WinHTTP \_ transférée**</span><span class="sxs-lookup"><span data-stu-id="39a2d-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-176">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-176">Obsolete.</span></span> <span data-ttu-id="39a2d-177">Conservé pour la compatibilité des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="39a2d-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_requête WinHTTP \_ à partir de**</span><span class="sxs-lookup"><span data-stu-id="39a2d-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-179">Récupère l’adresse de messagerie de l’utilisateur qui contrôle l' [*agent utilisateur*](glossary.md) demandeur si l’en-tête from est donné.</span><span class="sxs-lookup"><span data-stu-id="39a2d-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_hôte de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-181">Récupère l’hôte Internet et le numéro de port de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="39a2d-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_requête WinHTTP \_ si \_ correspondance**</span><span class="sxs-lookup"><span data-stu-id="39a2d-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-183">Récupère le contenu du champ d’en-tête de demande If-Match.</span><span class="sxs-lookup"><span data-stu-id="39a2d-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_requête WinHTTP \_ si \_ modifiée \_ depuis**</span><span class="sxs-lookup"><span data-stu-id="39a2d-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-185">Récupère le contenu de l’en-tête If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="39a2d-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_requête WinHTTP \_ si \_ aucune ne \_ correspond**</span><span class="sxs-lookup"><span data-stu-id="39a2d-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-187">Récupère le contenu du champ d’en-tête de demande If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="39a2d-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**\_requête WinHTTP \_ si la \_ plage**</span><span class="sxs-lookup"><span data-stu-id="39a2d-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-189">Récupère le contenu du champ d’en-tête de demande If-Range.</span><span class="sxs-lookup"><span data-stu-id="39a2d-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="39a2d-190">Cet en-tête permet à l’application cliente de vérifier si l’entité liée à une copie partielle de l’entité dans le cache de l’application cliente n’a pas été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="39a2d-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="39a2d-191">Si l’entité n’a pas été mise à jour, envoyez les composants que l’application cliente est manquante.</span><span class="sxs-lookup"><span data-stu-id="39a2d-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="39a2d-192">Si l’entité a été mise à jour, envoyez la totalité de l’entité mise à jour.</span><span class="sxs-lookup"><span data-stu-id="39a2d-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**\_requête WinHTTP \_ si non \_ modifiée \_ depuis**</span><span class="sxs-lookup"><span data-stu-id="39a2d-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-194">Récupère le contenu du champ d’en-tête de demande If-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="39a2d-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_lien de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-196">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-196">Obsolete.</span></span> <span data-ttu-id="39a2d-197">Conservé pour la compatibilité des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="39a2d-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ dernière \_ modification de la requête WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="39a2d-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-199">Reçoit la date et l’heure de la dernière modification de la ressource.</span><span class="sxs-lookup"><span data-stu-id="39a2d-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="39a2d-200">La date et l’heure sont déterminées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**emplacement de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-202">Récupère l’URI absolu utilisé dans un en-tête de réponse d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="39a2d-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**Max. des \_ requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-204">Indique la valeur maximale d’une \_ valeur de requête WinHTTP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="39a2d-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="39a2d-205">N’est pas un indicateur de requête.</span><span class="sxs-lookup"><span data-stu-id="39a2d-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ nombre maximal de transferts de requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-207">Récupère le nombre de proxies ou de passerelles qui peuvent transférer la requête vers le serveur entrant suivant.</span><span class="sxs-lookup"><span data-stu-id="39a2d-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ID de \_ message de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-209">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="39a2d-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ version MIME de la requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-211">Reçoit la version du protocole MIME (Multipurpose Internet Mail Extensions) qui a été utilisée pour construire le message.</span><span class="sxs-lookup"><span data-stu-id="39a2d-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ URI orig de la requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-213">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-213">Obsolete.</span></span> <span data-ttu-id="39a2d-214">Conservé pour la compatibilité des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="39a2d-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-216">Reçoit les directives spécifiques à l’implémentation qui peuvent s’appliquer à n’importe quel destinataire le long de la chaîne de requête/réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_authentification du \_ proxy de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-218">Récupère le schéma et le domaine d’authentification retournés par le proxy.</span><span class="sxs-lookup"><span data-stu-id="39a2d-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_autorisation du \_ proxy de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-220">Récupère l’en-tête utilisé pour identifier l’utilisateur sur un proxy qui requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="39a2d-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="39a2d-221">Cet en-tête ne peut être récupéré que si la demande est envoyée au serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ connexion proxy de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-223">Récupère l’en-tête de Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="39a2d-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ prise en charge du proxy de requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-225">Récupère l’en-tête de Proxy-Support.</span><span class="sxs-lookup"><span data-stu-id="39a2d-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**\_requête WinHTTP \_ publique**</span><span class="sxs-lookup"><span data-stu-id="39a2d-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-227">Reçoit les verbes HTTP disponibles sur ce serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_plage de requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-229">Récupère la plage d’octets d’une entité.</span><span class="sxs-lookup"><span data-stu-id="39a2d-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ en-têtes bruts de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-231">Reçoit tous les en-têtes retournés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="39a2d-232">Chaque en-tête se termine par « \\ 0 ».</span><span class="sxs-lookup"><span data-stu-id="39a2d-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="39a2d-233">Un « \\ 0 » supplémentaire termine la liste des en-têtes.</span><span class="sxs-lookup"><span data-stu-id="39a2d-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_ \_ en-têtes bruts de requête WinHTTP \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="39a2d-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-235">Reçoit tous les en-têtes retournés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="39a2d-236">Chaque en-tête est séparé par une séquence de retour chariot/saut de ligne (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="39a2d-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_référenceur de requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-238">Reçoit l’URI de la ressource dans laquelle l’URI demandé a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="39a2d-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_actualisation des requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-240">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-240">Obsolete.</span></span> <span data-ttu-id="39a2d-241">Conservé pour la compatibilité des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="39a2d-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_méthode de \_ demande de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-243">Reçoit le verbe HTTP qui est utilisé dans la demande, en général, obtenir ou poster.</span><span class="sxs-lookup"><span data-stu-id="39a2d-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_nouvelle tentative de requête WinHTTP \_ \_ après**</span><span class="sxs-lookup"><span data-stu-id="39a2d-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-245">Récupère la durée pendant laquelle le service est censé ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="39a2d-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_serveur de requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-247">Récupère des informations sur le logiciel utilisé par le serveur d’origine pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="39a2d-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_cookie de \_ jeu de requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-249">Reçoit la valeur du cookie défini pour la demande.</span><span class="sxs-lookup"><span data-stu-id="39a2d-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**CODE d’état de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-251">Reçoit le code d’état retourné par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="39a2d-252">Pour obtenir la liste des valeurs possibles, consultez [**codes d’État http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="39a2d-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**texte d’état de la \_ requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-254">Reçoit du texte supplémentaire retourné par le serveur sur la ligne de réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**titre de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-256">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="39a2d-256">Obsolete.</span></span> <span data-ttu-id="39a2d-257">Conservé pour la compatibilité des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="39a2d-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**encodage de \_ transfert de requêtes WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-259">Récupère le type de transformation qui a été appliqué au corps du message afin qu’il puisse être transféré en toute sécurité entre l’expéditeur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="39a2d-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_requête WinHTTP \_ sauf \_ modification \_ depuis**</span><span class="sxs-lookup"><span data-stu-id="39a2d-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-261">Récupère l’en-tête If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="39a2d-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_ \_ mise à niveau des requêtes WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="39a2d-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-263">Récupère les protocoles de communication supplémentaires pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-265">Reçoit tout ou partie de l’URI par lequel la ressource d’URI de requête peut être identifiée.</span><span class="sxs-lookup"><span data-stu-id="39a2d-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ agent utilisateur de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-267">Récupère des informations sur l’agent utilisateur qui a effectué la demande.</span><span class="sxs-lookup"><span data-stu-id="39a2d-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**variation de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-269">Récupère l’en-tête qui indique que l’entité a été sélectionnée à partir de plusieurs représentations disponibles de la réponse à l’aide de la négociation pilotée par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**VERSION de la \_ requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-271">Récupère la version HTTP qui est présente dans la ligne d’État.</span><span class="sxs-lookup"><span data-stu-id="39a2d-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_requête WinHTTP \_ via**</span><span class="sxs-lookup"><span data-stu-id="39a2d-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-273">Récupère les protocoles et destinataires intermédiaires entre l’agent utilisateur et le serveur sur les demandes, et entre le serveur d’origine et le client sur les réponses.</span><span class="sxs-lookup"><span data-stu-id="39a2d-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_avertissement de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-275">Récupère des informations supplémentaires sur l’état d’une réponse qui n’est peut-être pas reflétée par le code d’état de réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**\_interrogation \_ WinHTTP \_ authentification Web**</span><span class="sxs-lookup"><span data-stu-id="39a2d-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-277">Récupère le schéma et le domaine d’authentification retournés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="39a2d-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="39a2d-278">Les indicateurs de modificateur sont utilisés conjointement avec un indicateur d’attribut pour modifier la requête.</span><span class="sxs-lookup"><span data-stu-id="39a2d-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="39a2d-279">Les indicateurs de modificateur modifient le format des données retournées ou indiquent où la fonction [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) doit rechercher les informations.</span><span class="sxs-lookup"><span data-stu-id="39a2d-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="39a2d-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**Numéro de l' \_ indicateur de requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-281">Retourne les données sous la forme d’un nombre 32 bits pour les en-têtes dont la valeur est un nombre, tel que le code d’État.</span><span class="sxs-lookup"><span data-stu-id="39a2d-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_ \_ \_ en-têtes de demande d’indicateur de requête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-283">Interroge uniquement les en-têtes de demande.</span><span class="sxs-lookup"><span data-stu-id="39a2d-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39a2d-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_indicateur de requête WinHTTP \_ \_ SystemTime**</span><span class="sxs-lookup"><span data-stu-id="39a2d-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39a2d-285">Retourne la valeur d’en-tête en tant que structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) , ce qui ne nécessite pas que l’application analyse les données.</span><span class="sxs-lookup"><span data-stu-id="39a2d-285">Returns the header value as a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="39a2d-286">Utilisez pour les en-têtes dont la valeur est une chaîne de date/heure, telle que « Last-modified-Time ».</span><span class="sxs-lookup"><span data-stu-id="39a2d-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="39a2d-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**codes de fin de l' \_ indicateur de requête WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**WINHTTP\_QUERY\_FLAG\_TRAILERS**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="39a2d-288">Requêtes de codes de fin de réponse.</span><span class="sxs-lookup"><span data-stu-id="39a2d-288">Queries response trailers.</span></span> <span data-ttu-id="39a2d-289">Avant d’interroger des codes de fin de réponse, vous devez appeler [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) jusqu’à ce qu’il retourne 0 octet lu.</span><span class="sxs-lookup"><span data-stu-id="39a2d-289">Prior to querying response trailers, you must call [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) until it returns 0 bytes read.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="39a2d-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**encodage de câble de l' \_ indicateur de requête WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39a2d-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**WINHTTP\_QUERY\_FLAG\_WIRE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="39a2d-291">Par défaut, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) effectue une conversion Unicode avant de retourner l’en-tête qui a été interrogé.</span><span class="sxs-lookup"><span data-stu-id="39a2d-291">By default, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) performs a Unicode conversion before returning the header that was queried.</span></span> <span data-ttu-id="39a2d-292">Si cet indicateur est défini, WinHttp retourne l’en-tête à l’appelant sans effectuer cette conversion.</span><span class="sxs-lookup"><span data-stu-id="39a2d-292">If this flag is set, WinHttp returns the header to the caller without performing this conversion.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39a2d-293">Spécifications</span><span class="sxs-lookup"><span data-stu-id="39a2d-293">Requirements</span></span>

| <span data-ttu-id="39a2d-294">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39a2d-294">Requirement</span></span> | <span data-ttu-id="39a2d-295">Valeur</span><span class="sxs-lookup"><span data-stu-id="39a2d-295">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39a2d-296">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39a2d-296">Minimum supported client</span></span> | <span data-ttu-id="39a2d-297">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39a2d-297">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>      |
| <span data-ttu-id="39a2d-298">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39a2d-298">Minimum supported server</span></span> | <span data-ttu-id="39a2d-299">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39a2d-299">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>   |
| <span data-ttu-id="39a2d-300">En-tête</span><span class="sxs-lookup"><span data-stu-id="39a2d-300">Header</span></span>                   | <dl> <span data-ttu-id="39a2d-301"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="39a2d-301"><dt>Winhttp.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="39a2d-302">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39a2d-302">See also</span></span>

* [<span data-ttu-id="39a2d-303">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="39a2d-303">WinHTTP Versions</span></span>](winhttp-versions.md)
