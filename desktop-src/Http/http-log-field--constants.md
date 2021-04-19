---
title: Constantes HTTP_LOG_FIELD_ (http. h)
description: Définissez les champs dans le journal W3C et les journaux d’erreurs.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511553"
---
# <a name="http_log_field_-constants"></a><span data-ttu-id="4f2ca-103">\_ \_ Constantes de champ de journal http \_</span><span class="sxs-lookup"><span data-stu-id="4f2ca-103">HTTP\_LOG\_FIELD\_ Constants</span></span>

<span data-ttu-id="4f2ca-104">Les constantes de **\_ \_ \_ champ de journal http** définissent les champs dans le journal W3C et les journaux d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-104">The **HTTP\_LOG\_FIELD\_** constants define the fields in the W3C log and the error logs.</span></span>

<span data-ttu-id="4f2ca-105">Ces constantes sont utilisées dans la structure des [**\_ \_ informations de journalisation http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="4f2ca-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="4f2ca-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_date du \_ champ du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP\_LOG\_FIELD\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-107">Date à laquelle l’activité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-107">The date on which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_heure du \_ champ du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP\_LOG\_FIELD\_TIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-109">Heure, au format UTC (temps universel coordonné), à laquelle l’activité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-109">The time, in coordinated universal time (UTC), at which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_IP du \_ client du champ du journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP\_LOG\_FIELD\_CLIENT\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-111">Adresse IP du client à l’origine de la demande.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-111">The IP address of the client that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_nom d' \_ utilisateur du champ de journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP\_LOG\_FIELD\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-113">Nom de l’utilisateur authentifié qui a accédé à votre serveur.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-113">The name of the authenticated user who accessed your server.</span></span> <span data-ttu-id="4f2ca-114">Les utilisateurs anonymes sont indiqués par un trait d'union.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-114">Anonymous users are indicated by a hyphen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_nom du \_ site du champ du journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP\_LOG\_FIELD\_SITE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-116">Nom du site sur lequel l’entrée de fichier journal a été générée.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-116">The name of the site on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Protocole http \_ \_nom d' \_ ordinateur \_ du champ de journal**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span> **HTTP\_LOG\_FIELD\_COMPUTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-118">Nom de l’ordinateur sur lequel l’entrée de fichier journal a été générée.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-118">The name of the computer on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_ \_ \_ adresse IP du serveur de champs du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP\_LOG\_FIELD\_SERVER\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-120">Adresse IP du serveur sur lequel l’entrée de fichier journal a été générée.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-120">The IP address of the server on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_méthode de \_ champ de journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP\_LOG\_FIELD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-122">Action demandée, par exemple, une méthode d’extraction.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-122">The requested action, for example, a get method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Protocole http \_ \_ \_ \_ ressource URI du champ de journal**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span> **HTTP\_LOG\_FIELD\_URI\_STEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-124">La cible de l’action, par exemple, Default.htm.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-124">The target of the action, for example, Default.htm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_ \_ requête URI de champ de journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP\_LOG\_FIELD\_URI\_QUERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-126">Requête, le cas échéant, que le client essayait d’exécuter.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-126">The query, if any, that the client was trying to perform.</span></span> <span data-ttu-id="4f2ca-127">Une requête URI est nécessaire uniquement pour les pages dynamiques.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-127">A Universal Resource Identifier (URI) query is necessary only for dynamic pages.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_État du \_ champ du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP\_LOG\_FIELD\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-129">Code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-129">The HTTP status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_ \_ État Win32 du champ de journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP\_LOG\_FIELD\_WIN32\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-131">Code d’État Windows.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-131">The Windows status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_octets du champ du journal http \_ \_ \_ envoyés**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP\_LOG\_FIELD\_BYTES\_SENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-133">Nombre, en octets, envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-133">The number, in bytes, sent by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_octets du champ du journal http \_ \_ \_ reçus**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP\_LOG\_FIELD\_BYTES\_RECV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-135">Nombre, en octets, reçu par le serveur.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-135">The number, in bytes, received by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_temps de champ du journal http \_ \_ \_ pris**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**HTTP\_LOG\_FIELD\_TIME\_TAKEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-137">Durée, en millisecondes, de l’action.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-137">The time, in milliseconds, of the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_port du \_ serveur de champs du journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP\_LOG\_FIELD\_SERVER\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-139">Numéro de port du serveur configuré pour le service.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-139">The server port number that is configured for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Protocole http \_ \_ \_ \_ agent utilisateur du champ de journal**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span> **HTTP\_LOG\_FIELD\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-141">L’application utilisée par le client.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-141">The application that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_cookie de \_ champ de journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP\_LOG\_FIELD\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-143">Contenu du cookie envoyé ou reçu, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-143">The content of the cookie sent or received, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_Référence du \_ champ de journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP\_LOG\_FIELD\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-145">Site que l’utilisateur a visité pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-145">The site that the user last visited.</span></span> <span data-ttu-id="4f2ca-146">Ce site a fourni un lien vers le site actuel.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-146">This site provided a link to the current site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_version du \_ champ du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP\_LOG\_FIELD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-148">Version du protocole HTTP utilisée par le client.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-148">The HTTP protocol version that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_hôte de \_ champ de journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP\_LOG\_FIELD\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-150">Nom de l’en-tête de l’hôte, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-150">The host header name, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_sous- \_ État du champ du journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP\_LOG\_FIELD\_SUB\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-152">Code d’erreur du sous-état.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-152">The substatus error code.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="4f2ca-153">Les constantes suivantes sont utilisées pour la journalisation des erreurs HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-153">The following constants are used for HTTP error logging.</span></span>

<dl> <dt>

<span data-ttu-id="4f2ca-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_ \_ port client du champ du journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP\_LOG\_FIELD\_CLIENT\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-155">Numéro de port du client à partir duquel la demande est reçue.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-155">The client port number from which the request is received.</span></span> <span data-ttu-id="4f2ca-156">Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-156">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI du \_ champ de journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP\_LOG\_FIELD\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-158">URI reçu dans la demande, y compris la partie de la requête.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-158">The URI received in the request including the query portion.</span></span> <span data-ttu-id="4f2ca-159">Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-159">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ID de \_ site du champ du journal http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP\_LOG\_FIELD\_SITE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-161">ID numérique spécifique à l’application du groupe d’URL sur lequel la demande est routée.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-161">The application-specific numeric ID of the URL Group on which the request is routed.</span></span> <span data-ttu-id="4f2ca-162">Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-162">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_raison du \_ champ du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP\_LOG\_FIELD\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-164">Expression de raison de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-164">The error reason phrase.</span></span> <span data-ttu-id="4f2ca-165">Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-165">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_nom de \_ la \_ file d’attente du champ du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP\_LOG\_FIELD\_QUEUE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-167">Nom de la file d’attente de demandes vers laquelle la demande est distribuée.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-167">The name of the request queue to which the request is dispatched.</span></span> <span data-ttu-id="4f2ca-168">Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-168">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f2ca-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_champ du journal http \_ \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP\_LOG\_FIELD\_STREAMID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4f2ca-170">ID du flux.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-170">The stream id.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f2ca-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f2ca-171">Requirements</span></span>



| <span data-ttu-id="4f2ca-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f2ca-172">Requirement</span></span> | <span data-ttu-id="4f2ca-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f2ca-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4f2ca-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f2ca-174">Minimum supported client</span></span><br/> | <span data-ttu-id="4f2ca-175">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f2ca-175">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f2ca-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f2ca-176">Minimum supported server</span></span><br/> | <span data-ttu-id="4f2ca-177">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f2ca-177">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4f2ca-178">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f2ca-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f2ca-179"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f2ca-179"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f2ca-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f2ca-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f2ca-181">Constantes de la version 2,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="4f2ca-181">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="4f2ca-182">**\_informations de journalisation http \_**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-182">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="4f2ca-183">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-183">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="4f2ca-184">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-184">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="4f2ca-185">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-185">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="4f2ca-186">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-186">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





