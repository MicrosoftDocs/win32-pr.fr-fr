---
title: Codes d’état HTTP (Wininet. h)
description: Le tableau suivant contient les constantes et les valeurs correspondantes pour les codes d’état HTTP renvoyés par les serveurs sur Internet.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385224"
---
# <a name="http-status-codes-winineth"></a><span data-ttu-id="6eb69-103">Codes d’état HTTP (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="6eb69-103">HTTP Status Codes (Wininet.h)</span></span>

<span data-ttu-id="6eb69-104">Le tableau suivant contient les constantes et les valeurs correspondantes pour les codes d’état HTTP renvoyés par les serveurs sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6eb69-104">The following table contains the constants and corresponding values for the HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="6eb69-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_État http \_ continuer**</span><span class="sxs-lookup"><span data-stu-id="6eb69-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-106">100</span><span class="sxs-lookup"><span data-stu-id="6eb69-106">100</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-107">La demande peut être poursuivie.</span><span class="sxs-lookup"><span data-stu-id="6eb69-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocoles de \_ commutateur d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-109">101</span><span class="sxs-lookup"><span data-stu-id="6eb69-109">101</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-110">Le serveur a basculé les protocoles dans un en-tête de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="6eb69-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_État http \_ OK**</span><span class="sxs-lookup"><span data-stu-id="6eb69-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-112">200</span><span class="sxs-lookup"><span data-stu-id="6eb69-112">200</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-113">La demande s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="6eb69-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_État http \_ créé**</span><span class="sxs-lookup"><span data-stu-id="6eb69-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-115">201</span><span class="sxs-lookup"><span data-stu-id="6eb69-115">201</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-116">La demande a été traitée et a entraîné la création d’une nouvelle ressource.</span><span class="sxs-lookup"><span data-stu-id="6eb69-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_État http \_ accepté**</span><span class="sxs-lookup"><span data-stu-id="6eb69-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-118">202</span><span class="sxs-lookup"><span data-stu-id="6eb69-118">202</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-119">La demande a été acceptée pour traitement, mais le traitement n’a pas été effectué.</span><span class="sxs-lookup"><span data-stu-id="6eb69-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_État http \_ partiel**</span><span class="sxs-lookup"><span data-stu-id="6eb69-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-121">203</span><span class="sxs-lookup"><span data-stu-id="6eb69-121">203</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-122">Les méta-informations retournées dans l’en-tête d’entité ne sont pas le jeu définitif disponible à partir du serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="6eb69-122">The returned meta information in the entity-header is not the definitive set available from the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**état HTTP- \_ \_ aucun \_ contenu**</span><span class="sxs-lookup"><span data-stu-id="6eb69-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-124">204</span><span class="sxs-lookup"><span data-stu-id="6eb69-124">204</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-125">Le serveur a répondu à la demande, mais il n’existe aucune nouvelle information à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="6eb69-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenu de \_ réinitialisation de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-127">205</span><span class="sxs-lookup"><span data-stu-id="6eb69-127">205</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-128">La demande est terminée et le programme client doit réinitialiser la vue de document qui a provoqué l’envoi de la demande pour permettre à l’utilisateur de lancer facilement une autre action d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6eb69-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ contenu partiel de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-130">206</span><span class="sxs-lookup"><span data-stu-id="6eb69-130">206</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-131">Le serveur a rempli la requête d’extraction partielle pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="6eb69-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_État http \_ ambigu**</span><span class="sxs-lookup"><span data-stu-id="6eb69-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-133">300</span><span class="sxs-lookup"><span data-stu-id="6eb69-133">300</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-134">Le serveur n’a pas pu décider de ce qui doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="6eb69-134">The server couldn't decide what to return.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_État http \_ déplacé**</span><span class="sxs-lookup"><span data-stu-id="6eb69-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-136">301</span><span class="sxs-lookup"><span data-stu-id="6eb69-136">301</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-137">La ressource demandée a été assignée à un nouvel URI permanent (Uniform Resource Identifier), et toute référence future à cette ressource doit être effectuée à l’aide de l’un des URI renvoyés.</span><span class="sxs-lookup"><span data-stu-id="6eb69-137">The requested resource has been assigned to a new permanent URI (Uniform Resource Identifier), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**redirection HTTP \_ Status \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-139">302</span><span class="sxs-lookup"><span data-stu-id="6eb69-139">302</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-140">La ressource demandée réside temporairement sous un autre URI (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="6eb69-140">The requested resource resides temporarily under a different URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_méthode de \_ redirection http status \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-142">303</span><span class="sxs-lookup"><span data-stu-id="6eb69-142">303</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-143">La réponse à la demande se trouve sous un autre URI (Uniform Resource Identifier) et doit être récupérée à l’aide d’un verbe HTTP obtenir sur cette ressource.</span><span class="sxs-lookup"><span data-stu-id="6eb69-143">The response to the request can be found under a different URI (Uniform Resource Identifier) and should be retrieved using a GET HTTP verb on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_État http \_ non \_ modifié**</span><span class="sxs-lookup"><span data-stu-id="6eb69-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-145">304</span><span class="sxs-lookup"><span data-stu-id="6eb69-145">304</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-146">La ressource demandée n’a pas été modifiée.</span><span class="sxs-lookup"><span data-stu-id="6eb69-146">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_proxy d' \_ utilisation d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-148">305</span><span class="sxs-lookup"><span data-stu-id="6eb69-148">305</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-149">La ressource demandée doit être accessible via le proxy donné par le champ d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="6eb69-149">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbe de \_ redirection d’État http \_ Keep \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-151">307</span><span class="sxs-lookup"><span data-stu-id="6eb69-151">307</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-152">La demande redirigée conserve le même verbe HTTP.</span><span class="sxs-lookup"><span data-stu-id="6eb69-152">The redirected request keeps the same HTTP verb.</span></span> <span data-ttu-id="6eb69-153">Comportement HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="6eb69-153">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_demande d’État http \_ incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-155">400</span><span class="sxs-lookup"><span data-stu-id="6eb69-155">400</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-156">La requête n’a pas pu être traitée par le serveur en raison d’une syntaxe non valide.</span><span class="sxs-lookup"><span data-stu-id="6eb69-156">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_État http \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="6eb69-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-158">401</span><span class="sxs-lookup"><span data-stu-id="6eb69-158">401</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-159">La ressource demandée nécessite l'authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6eb69-159">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_demande de \_ paiement d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-161">402</span><span class="sxs-lookup"><span data-stu-id="6eb69-161">402</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-162">Non implémenté actuellement dans le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="6eb69-162">Not currently implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_État http \_ interdit**</span><span class="sxs-lookup"><span data-stu-id="6eb69-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-164">403</span><span class="sxs-lookup"><span data-stu-id="6eb69-164">403</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-165">Le serveur a compris la demande, mais refuse de la traiter.</span><span class="sxs-lookup"><span data-stu-id="6eb69-165">The server understood the request, but is refusing to fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_État http \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="6eb69-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-167">404</span><span class="sxs-lookup"><span data-stu-id="6eb69-167">404</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-168">Le serveur n’a trouvé aucun résultat correspondant à l’URI demandé (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="6eb69-168">The server has not found anything matching the requested URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ méthode incorrecte de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-170">405</span><span class="sxs-lookup"><span data-stu-id="6eb69-170">405</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-171">Le verbe HTTP utilisé n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="6eb69-171">The HTTP verb used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_État http \_ aucun \_ acceptable**</span><span class="sxs-lookup"><span data-stu-id="6eb69-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-173">406</span><span class="sxs-lookup"><span data-stu-id="6eb69-173">406</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-174">Aucune réponse acceptable pour le client n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="6eb69-174">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_demande d' \_ authentification du proxy d’État http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-176">407</span><span class="sxs-lookup"><span data-stu-id="6eb69-176">407</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-177">Authentification du proxy requise.</span><span class="sxs-lookup"><span data-stu-id="6eb69-177">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ \_ délai d’expiration de la demande http Status**</span><span class="sxs-lookup"><span data-stu-id="6eb69-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-179">408</span><span class="sxs-lookup"><span data-stu-id="6eb69-179">408</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-180">Le serveur a expiré lorsqu'il attendait la demande.</span><span class="sxs-lookup"><span data-stu-id="6eb69-180">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflit d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-182">409</span><span class="sxs-lookup"><span data-stu-id="6eb69-182">409</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-183">La demande n’a pas pu aboutir en raison d’un conflit avec l’état actuel de la ressource.</span><span class="sxs-lookup"><span data-stu-id="6eb69-183">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="6eb69-184">L’utilisateur doit renvoyer avec plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6eb69-184">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_État http \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="6eb69-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-186">410</span><span class="sxs-lookup"><span data-stu-id="6eb69-186">410</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-187">La ressource demandée n’est plus disponible sur le serveur et aucune adresse de transfert n’est connue.</span><span class="sxs-lookup"><span data-stu-id="6eb69-187">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_longueur d’État http \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="6eb69-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-189">411</span><span class="sxs-lookup"><span data-stu-id="6eb69-189">411</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-190">Le serveur refuse d’accepter la demande sans longueur de contenu définie.</span><span class="sxs-lookup"><span data-stu-id="6eb69-190">The server refuses to accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**échec de la \_ \_ précondition http status \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-192">412</span><span class="sxs-lookup"><span data-stu-id="6eb69-192">412</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-193">La condition préalable donnée dans un ou plusieurs champs d’en-tête de demande a été évaluée à false lorsqu’elle a été testée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="6eb69-193">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_demande d’État http \_ \_ trop \_ grande**</span><span class="sxs-lookup"><span data-stu-id="6eb69-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-195">413</span><span class="sxs-lookup"><span data-stu-id="6eb69-195">413</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-196">Le serveur refuse de traiter une demande, car l’entité de la demande est plus grande que le serveur est prêt ou en mesure de traiter.</span><span class="sxs-lookup"><span data-stu-id="6eb69-196">The server is refusing to process a request because the request entity is larger than the server is willing or able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI d’État http \_ \_ trop \_ long**</span><span class="sxs-lookup"><span data-stu-id="6eb69-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-198">414</span><span class="sxs-lookup"><span data-stu-id="6eb69-198">414</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-199">Le serveur refuse de traiter la demande, car l’URI de la demande (Uniform Resource Identifier) est plus long que le serveur est disposé à interpréter.</span><span class="sxs-lookup"><span data-stu-id="6eb69-199">The server is refusing to service the request because the request URI (Uniform Resource Identifier) is longer than the server is willing to interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**état HTTP- \_ \_ SUPPORT non pris en charge \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-201">415</span><span class="sxs-lookup"><span data-stu-id="6eb69-201">415</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-202">Le serveur refuse de traiter la demande, car l’entité de la demande est dans un format non pris en charge par la ressource demandée pour la méthode demandée.</span><span class="sxs-lookup"><span data-stu-id="6eb69-202">The server is refusing to service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ nouvelle tentative d’État http \_ avec**</span><span class="sxs-lookup"><span data-stu-id="6eb69-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-204">449</span><span class="sxs-lookup"><span data-stu-id="6eb69-204">449</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-205">La demande doit être retentée après l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="6eb69-205">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_Erreur du \_ serveur d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-207">500</span><span class="sxs-lookup"><span data-stu-id="6eb69-207">500</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-208">Le serveur a rencontré une condition inattendue qui l’a empêché de satisfaire la requête.</span><span class="sxs-lookup"><span data-stu-id="6eb69-208">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_État http \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="6eb69-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-210">501</span><span class="sxs-lookup"><span data-stu-id="6eb69-210">501</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-211">Le serveur ne prend pas en charge les fonctionnalités requises pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="6eb69-211">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ passerelle incorrecte de l’État http \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-213">502</span><span class="sxs-lookup"><span data-stu-id="6eb69-213">502</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-214">Le serveur, alors qu’il agit en tant que passerelle ou proxy, a reçu une réponse non valide du serveur en amont auquel il a accédé en tentant de répondre à la demande.</span><span class="sxs-lookup"><span data-stu-id="6eb69-214">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**\_service d’État http indisponible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eb69-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-216">503</span><span class="sxs-lookup"><span data-stu-id="6eb69-216">503</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-217">Le service est temporairement surchargé.</span><span class="sxs-lookup"><span data-stu-id="6eb69-217">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ \_ délai d’expiration de la passerelle d’État http**</span><span class="sxs-lookup"><span data-stu-id="6eb69-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-219">504</span><span class="sxs-lookup"><span data-stu-id="6eb69-219">504</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-220">La demande a expiré lorsqu'elle attendait une passerelle.</span><span class="sxs-lookup"><span data-stu-id="6eb69-220">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb69-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_version d’État http \_ \_ non \_ sup.**</span><span class="sxs-lookup"><span data-stu-id="6eb69-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eb69-222">505</span><span class="sxs-lookup"><span data-stu-id="6eb69-222">505</span></span>
</dt> <dt>



<span data-ttu-id="6eb69-223">Le serveur ne prend pas en charge ou refuse de prendre en charge la version du protocole HTTP qui a été utilisée dans le message de demande.</span><span class="sxs-lookup"><span data-stu-id="6eb69-223">The server does not support, or refuses to support, the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6eb69-224">Notes</span><span class="sxs-lookup"><span data-stu-id="6eb69-224">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6eb69-225">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="6eb69-225">WinINet does not support server implementations.</span></span> <span data-ttu-id="6eb69-226">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="6eb69-226">In addition, it should not be used from a service.</span></span> <span data-ttu-id="6eb69-227">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="6eb69-227">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6eb69-228">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6eb69-228">Requirements</span></span>



| <span data-ttu-id="6eb69-229">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6eb69-229">Requirement</span></span> | <span data-ttu-id="6eb69-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="6eb69-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb69-231">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eb69-231">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb69-232">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eb69-232">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6eb69-233">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eb69-233">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb69-234">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eb69-234">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6eb69-235">En-tête</span><span class="sxs-lookup"><span data-stu-id="6eb69-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eb69-236"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb69-236"><dt>Wininet.h</dt></span></span> </dl> |



 

