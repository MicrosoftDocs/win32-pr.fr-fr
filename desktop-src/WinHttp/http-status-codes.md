---
description: Ces constantes et valeurs correspondantes indiquent les codes d’état HTTP renvoyés par les serveurs sur Internet.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Codes d’état HTTP (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203548"
---
# <a name="http-status-codes-winhttph"></a><span data-ttu-id="a6c41-103">Codes d’état HTTP (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="a6c41-103">HTTP Status Codes (Winhttp.h)</span></span>

<span data-ttu-id="a6c41-104">Ces constantes et valeurs correspondantes indiquent les codes d’état HTTP renvoyés par les serveurs sur Internet.</span><span class="sxs-lookup"><span data-stu-id="a6c41-104">These constants and corresponding values indicate HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="a6c41-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_État http \_ continuer**</span><span class="sxs-lookup"><span data-stu-id="a6c41-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-106">100</span><span class="sxs-lookup"><span data-stu-id="a6c41-106">100</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-107">La demande peut être poursuivie.</span><span class="sxs-lookup"><span data-stu-id="a6c41-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocoles de \_ commutateur d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-109">101</span><span class="sxs-lookup"><span data-stu-id="a6c41-109">101</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-110">Le serveur a basculé les protocoles dans un en-tête de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="a6c41-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_État http \_ OK**</span><span class="sxs-lookup"><span data-stu-id="a6c41-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-112">200</span><span class="sxs-lookup"><span data-stu-id="a6c41-112">200</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-113">La demande s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="a6c41-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_État http \_ créé**</span><span class="sxs-lookup"><span data-stu-id="a6c41-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-115">201</span><span class="sxs-lookup"><span data-stu-id="a6c41-115">201</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-116">La demande a été traitée et a entraîné la création d’une nouvelle ressource.</span><span class="sxs-lookup"><span data-stu-id="a6c41-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_État http \_ accepté**</span><span class="sxs-lookup"><span data-stu-id="a6c41-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-118">202</span><span class="sxs-lookup"><span data-stu-id="a6c41-118">202</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-119">La demande a été acceptée pour traitement, mais le traitement n’a pas été effectué.</span><span class="sxs-lookup"><span data-stu-id="a6c41-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_État http \_ partiel**</span><span class="sxs-lookup"><span data-stu-id="a6c41-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-121">203</span><span class="sxs-lookup"><span data-stu-id="a6c41-121">203</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-122">Les méta-informations retournées dans l’en-tête d’entité ne sont pas le jeu définitif disponible à partir du serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="a6c41-122">The returned meta information in the entity-header is not the definitive set available from the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**état HTTP- \_ \_ aucun \_ contenu**</span><span class="sxs-lookup"><span data-stu-id="a6c41-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-124">204</span><span class="sxs-lookup"><span data-stu-id="a6c41-124">204</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-125">Le serveur a répondu à la demande, mais il n’existe aucune nouvelle information à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="a6c41-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenu de \_ réinitialisation de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-127">205</span><span class="sxs-lookup"><span data-stu-id="a6c41-127">205</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-128">La demande est terminée et le programme client doit réinitialiser la vue de document qui a provoqué l’envoi de la demande pour permettre à l’utilisateur de lancer facilement une autre action d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a6c41-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ contenu partiel de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-130">206</span><span class="sxs-lookup"><span data-stu-id="a6c41-130">206</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-131">Le serveur a rempli la requête d’extraction partielle pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="a6c41-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**état \_ http \_ \_ multi- \_ État WebDAV**</span><span class="sxs-lookup"><span data-stu-id="a6c41-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP\_STATUS\_WEBDAV\_MULTI\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-133">207</span><span class="sxs-lookup"><span data-stu-id="a6c41-133">207</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-134">Au cours d’une opération de création et de gestion de version (WebDAV) World Wide Web, il indique plusieurs codes d’État pour une seule réponse.</span><span class="sxs-lookup"><span data-stu-id="a6c41-134">During a World Wide Web Distributed Authoring and Versioning (WebDAV) operation, this indicates multiple status codes for a single response.</span></span> <span data-ttu-id="a6c41-135">Le corps de la réponse contient des Extensible Markup Language (XML) qui décrivent les codes d’État.</span><span class="sxs-lookup"><span data-stu-id="a6c41-135">The response body contains Extensible Markup Language (XML) that describes the status codes.</span></span> <span data-ttu-id="a6c41-136">Pour plus d’informations, consultez [Extensions http pour la création distribuée](../webdav/webdav-portal.md).</span><span class="sxs-lookup"><span data-stu-id="a6c41-136">For more information, see [HTTP Extensions for Distributed Authoring](../webdav/webdav-portal.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_État http \_ ambigu**</span><span class="sxs-lookup"><span data-stu-id="a6c41-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-138">300</span><span class="sxs-lookup"><span data-stu-id="a6c41-138">300</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-139">La ressource demandée est disponible à un ou plusieurs emplacements.</span><span class="sxs-lookup"><span data-stu-id="a6c41-139">The requested resource is available at one or more locations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_État http \_ déplacé**</span><span class="sxs-lookup"><span data-stu-id="a6c41-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-141">301</span><span class="sxs-lookup"><span data-stu-id="a6c41-141">301</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-142">La ressource demandée a été affectée à un nouveau Uniform Resource Identifier permanent (URI), et toutes les références futures à cette ressource doivent être effectuées à l’aide de l’un des URI renvoyés.</span><span class="sxs-lookup"><span data-stu-id="a6c41-142">The requested resource has been assigned to a new permanent Uniform Resource Identifier (URI), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**redirection HTTP \_ Status \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-144">302</span><span class="sxs-lookup"><span data-stu-id="a6c41-144">302</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-145">La ressource demandée réside temporairement sous un autre URI.</span><span class="sxs-lookup"><span data-stu-id="a6c41-145">The requested resource resides temporarily under a different URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_méthode de \_ redirection http status \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-147">303</span><span class="sxs-lookup"><span data-stu-id="a6c41-147">303</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-148">La réponse à la demande se trouve sous un autre URI et doit être récupérée à l’aide d’un [*verbe http*](glossary.md) obtenir sur cette ressource.</span><span class="sxs-lookup"><span data-stu-id="a6c41-148">The response to the request can be found under a different URI and should be retrieved using a GET [*HTTP verb*](glossary.md) on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_État http \_ non \_ modifié**</span><span class="sxs-lookup"><span data-stu-id="a6c41-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-150">304</span><span class="sxs-lookup"><span data-stu-id="a6c41-150">304</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-151">La ressource demandée n’a pas été modifiée.</span><span class="sxs-lookup"><span data-stu-id="a6c41-151">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_proxy d' \_ utilisation d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-153">305</span><span class="sxs-lookup"><span data-stu-id="a6c41-153">305</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-154">La ressource demandée doit être accessible via le proxy donné par le champ d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a6c41-154">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbe de \_ redirection d’État http \_ Keep \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-156">307</span><span class="sxs-lookup"><span data-stu-id="a6c41-156">307</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-157">La demande redirigée conserve le même [*verbe http*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a6c41-157">The redirected request keeps the same [*HTTP verb*](glossary.md).</span></span> <span data-ttu-id="a6c41-158">Comportement HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="a6c41-158">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_demande d’État http \_ incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-160">400</span><span class="sxs-lookup"><span data-stu-id="a6c41-160">400</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-161">La requête n’a pas pu être traitée par le serveur en raison d’une syntaxe non valide.</span><span class="sxs-lookup"><span data-stu-id="a6c41-161">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_État http \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="a6c41-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-163">401</span><span class="sxs-lookup"><span data-stu-id="a6c41-163">401</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-164">La ressource demandée nécessite l'authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a6c41-164">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_demande de \_ paiement d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-166">402</span><span class="sxs-lookup"><span data-stu-id="a6c41-166">402</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-167">Non implémenté dans le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="a6c41-167">Not implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_État http \_ interdit**</span><span class="sxs-lookup"><span data-stu-id="a6c41-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-169">403</span><span class="sxs-lookup"><span data-stu-id="a6c41-169">403</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-170">Le serveur a compris la demande, mais ne peut pas la traiter.</span><span class="sxs-lookup"><span data-stu-id="a6c41-170">The server understood the request, but cannot fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_État http \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="a6c41-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-172">404</span><span class="sxs-lookup"><span data-stu-id="a6c41-172">404</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-173">Le serveur n’a trouvé rien qui correspond à l’URI demandé.</span><span class="sxs-lookup"><span data-stu-id="a6c41-173">The server has not found anything that matches the requested URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ méthode incorrecte de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-175">405</span><span class="sxs-lookup"><span data-stu-id="a6c41-175">405</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-176">Le [*verbe http*](glossary.md) utilisé n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="a6c41-176">The [*HTTP verb*](glossary.md) used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_État http \_ aucun \_ acceptable**</span><span class="sxs-lookup"><span data-stu-id="a6c41-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-178">406</span><span class="sxs-lookup"><span data-stu-id="a6c41-178">406</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-179">Aucune réponse acceptable pour le client n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="a6c41-179">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_demande d' \_ authentification du proxy d’État http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-181">407</span><span class="sxs-lookup"><span data-stu-id="a6c41-181">407</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-182">Authentification du proxy requise.</span><span class="sxs-lookup"><span data-stu-id="a6c41-182">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ \_ délai d’expiration de la demande http Status**</span><span class="sxs-lookup"><span data-stu-id="a6c41-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-184">408</span><span class="sxs-lookup"><span data-stu-id="a6c41-184">408</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-185">Le serveur a expiré lorsqu'il attendait la demande.</span><span class="sxs-lookup"><span data-stu-id="a6c41-185">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflit d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-187">409</span><span class="sxs-lookup"><span data-stu-id="a6c41-187">409</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-188">La demande n’a pas pu aboutir en raison d’un conflit avec l’état actuel de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a6c41-188">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="a6c41-189">L’utilisateur doit renvoyer avec plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a6c41-189">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_État http \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="a6c41-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-191">410</span><span class="sxs-lookup"><span data-stu-id="a6c41-191">410</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-192">La ressource demandée n’est plus disponible sur le serveur et aucune adresse de transfert n’est connue.</span><span class="sxs-lookup"><span data-stu-id="a6c41-192">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_longueur d’État http \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="a6c41-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-194">411</span><span class="sxs-lookup"><span data-stu-id="a6c41-194">411</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-195">Le serveur ne peut pas accepter la demande sans longueur de contenu définie.</span><span class="sxs-lookup"><span data-stu-id="a6c41-195">The server cannot accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**échec de la \_ \_ précondition http status \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-197">412</span><span class="sxs-lookup"><span data-stu-id="a6c41-197">412</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-198">La condition préalable donnée dans un ou plusieurs champs d’en-tête de demande a été évaluée à false lorsqu’elle a été testée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a6c41-198">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_demande d’État http \_ \_ trop \_ grande**</span><span class="sxs-lookup"><span data-stu-id="a6c41-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-200">413</span><span class="sxs-lookup"><span data-stu-id="a6c41-200">413</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-201">Le serveur ne peut pas traiter la demande, car la taille de l’entité de la demande est supérieure à ce que le serveur est en mesure de traiter.</span><span class="sxs-lookup"><span data-stu-id="a6c41-201">The server cannot process the request because the request entity is larger than the server is able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI d’État http \_ \_ trop \_ long**</span><span class="sxs-lookup"><span data-stu-id="a6c41-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-203">414</span><span class="sxs-lookup"><span data-stu-id="a6c41-203">414</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-204">Le serveur ne peut pas traiter la demande, car l’URI de la demande est plus long que ce que le serveur peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="a6c41-204">The server cannot service the request because the request URI is longer than the server can interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**état HTTP- \_ \_ SUPPORT non pris en charge \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-206">415</span><span class="sxs-lookup"><span data-stu-id="a6c41-206">415</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-207">Le serveur ne peut pas traiter la demande, car l’entité de la demande est dans un format non pris en charge par la ressource demandée pour la méthode demandée.</span><span class="sxs-lookup"><span data-stu-id="a6c41-207">The server cannot service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ nouvelle tentative d’État http \_ avec**</span><span class="sxs-lookup"><span data-stu-id="a6c41-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-209">449</span><span class="sxs-lookup"><span data-stu-id="a6c41-209">449</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-210">La demande doit être retentée après l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="a6c41-210">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_Erreur du \_ serveur d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-212">500</span><span class="sxs-lookup"><span data-stu-id="a6c41-212">500</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-213">Le serveur a rencontré une condition inattendue qui l’a empêché de satisfaire la requête.</span><span class="sxs-lookup"><span data-stu-id="a6c41-213">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_État http \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a6c41-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-215">501</span><span class="sxs-lookup"><span data-stu-id="a6c41-215">501</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-216">Le serveur ne prend pas en charge les fonctionnalités requises pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="a6c41-216">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ passerelle incorrecte de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-218">502</span><span class="sxs-lookup"><span data-stu-id="a6c41-218">502</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-219">Le serveur, alors qu’il agit en tant que passerelle ou proxy, a reçu une réponse non valide du serveur en amont auquel il a accédé en tentant de répondre à la demande.</span><span class="sxs-lookup"><span data-stu-id="a6c41-219">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**\_service d’État http indisponible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a6c41-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-221">503</span><span class="sxs-lookup"><span data-stu-id="a6c41-221">503</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-222">Le service est temporairement surchargé.</span><span class="sxs-lookup"><span data-stu-id="a6c41-222">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ \_ délai d’expiration de la passerelle d’État http**</span><span class="sxs-lookup"><span data-stu-id="a6c41-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-224">504</span><span class="sxs-lookup"><span data-stu-id="a6c41-224">504</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-225">La demande a expiré lorsqu'elle attendait une passerelle.</span><span class="sxs-lookup"><span data-stu-id="a6c41-225">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6c41-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_version d’État http \_ \_ non \_ sup.**</span><span class="sxs-lookup"><span data-stu-id="a6c41-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6c41-227">505</span><span class="sxs-lookup"><span data-stu-id="a6c41-227">505</span></span>
</dt> <dt>



<span data-ttu-id="a6c41-228">Le serveur ne prend pas en charge la version du protocole HTTP qui a été utilisée dans le message de demande.</span><span class="sxs-lookup"><span data-stu-id="a6c41-228">The server does not support the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6c41-229">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6c41-229">Requirements</span></span>



| <span data-ttu-id="a6c41-230">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6c41-230">Requirement</span></span> | <span data-ttu-id="a6c41-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6c41-231">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c41-232">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6c41-232">Minimum supported client</span></span><br/> | <span data-ttu-id="a6c41-233">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6c41-233">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="a6c41-234">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6c41-234">Minimum supported server</span></span><br/> | <span data-ttu-id="a6c41-235">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6c41-235">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="a6c41-236">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6c41-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6c41-237"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6c41-237"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6c41-238">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6c41-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6c41-239">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a6c41-239">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

