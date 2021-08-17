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
ms.openlocfilehash: 01c6a8fecf7d1c7b3f95c1d4ce8040b9ba25e7d72ee4a41c8cbbcd24cd0da4bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743807"
---
# <a name="http-status-codes-winineth"></a>Codes d’état HTTP (Wininet. h)

Le tableau suivant contient les constantes et les valeurs correspondantes pour les codes d’état HTTP renvoyés par les serveurs sur Internet.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_État http \_ continuer**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



La demande peut être poursuivie.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocoles de \_ commutateur d’État http \_**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Le serveur a basculé les protocoles dans un en-tête de mise à niveau.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_État http \_ OK**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



La demande s’est terminée correctement.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_État http \_ créé**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



La demande a été traitée et a entraîné la création d’une nouvelle ressource.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_État http \_ accepté**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



La demande a été acceptée pour traitement, mais le traitement n’a pas été effectué.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_État http \_ partiel**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



Les méta-informations retournées dans l’en-tête d’entité ne sont pas le jeu définitif disponible à partir du serveur d’origine.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**état HTTP- \_ \_ aucun \_ contenu**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



Le serveur a répondu à la demande, mais il n’existe aucune nouvelle information à renvoyer.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenu de \_ réinitialisation de l’État http \_**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



La demande est terminée et le programme client doit réinitialiser la vue de document qui a provoqué l’envoi de la demande pour permettre à l’utilisateur de lancer facilement une autre action d’entrée.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ contenu partiel de l’État http \_**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



Le serveur a rempli la requête d’extraction partielle pour la ressource.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_État http \_ ambigu**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



Le serveur n’a pas pu décider de ce qui doit être retourné.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_État http \_ déplacé**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



La ressource demandée a été assignée à un nouvel URI permanent (Uniform Resource Identifier), et toute référence future à cette ressource doit être effectuée à l’aide de l’un des URI renvoyés.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**redirection HTTP \_ Status \_**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



La ressource demandée réside temporairement sous un autre URI (Uniform Resource Identifier).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_méthode de \_ redirection http status \_**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



La réponse à la demande se trouve sous un autre URI (Uniform Resource Identifier) et doit être récupérée à l’aide d’un verbe HTTP obtenir sur cette ressource.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_État http \_ non \_ modifié**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



La ressource demandée n’a pas été modifiée.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_proxy d' \_ utilisation d’État http \_**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



La ressource demandée doit être accessible via le proxy donné par le champ d’emplacement.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbe de \_ redirection d’État http \_ Keep \_**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



La demande redirigée conserve le même verbe HTTP. Comportement HTTP/1.1.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_demande d’État http \_ incorrecte \_**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



La requête n’a pas pu être traitée par le serveur en raison d’une syntaxe non valide.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_État http \_ refusé**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



La ressource demandée nécessite l'authentification des utilisateurs.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_demande de \_ paiement d’État http \_**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



Non implémenté actuellement dans le protocole HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_État http \_ interdit**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Le serveur a compris la demande, mais refuse de la traiter.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_État http \_ \_ introuvable**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Le serveur n’a trouvé aucun résultat correspondant à l’URI demandé (Uniform Resource Identifier).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ méthode incorrecte de l’État http \_**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Le verbe HTTP utilisé n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_État http \_ aucun \_ acceptable**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Aucune réponse acceptable pour le client n’a été trouvée.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_demande d' \_ authentification du proxy d’État http \_ \_**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Authentification du proxy requise.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ \_ délai d’expiration de la demande http Status**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



Le serveur a expiré lorsqu'il attendait la demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflit d’État http \_**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



La demande n’a pas pu aboutir en raison d’un conflit avec l’état actuel de la ressource. L’utilisateur doit renvoyer avec plus d’informations.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_État http \_ supprimé**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



La ressource demandée n’est plus disponible sur le serveur et aucune adresse de transfert n’est connue.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_longueur d’État http \_ \_ requise**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



Le serveur refuse d’accepter la demande sans longueur de contenu définie.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**échec de la \_ \_ précondition http status \_**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



La condition préalable donnée dans un ou plusieurs champs d’en-tête de demande a été évaluée à false lorsqu’elle a été testée sur le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_demande d’État http \_ \_ trop \_ grande**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



Le serveur refuse de traiter une demande, car l’entité de la demande est plus grande que le serveur est prêt ou en mesure de traiter.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI d’État http \_ \_ trop \_ long**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Le serveur refuse de traiter la demande, car l’URI de la demande (Uniform Resource Identifier) est plus long que le serveur est disposé à interpréter.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**état HTTP- \_ \_ SUPPORT non pris en charge \_**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Le serveur refuse de traiter la demande, car l’entité de la demande est dans un format non pris en charge par la ressource demandée pour la méthode demandée.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ nouvelle tentative d’État http \_ avec**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



La demande doit être retentée après l’action appropriée.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_Erreur du \_ serveur d’État http \_**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



Le serveur a rencontré une condition inattendue qui l’a empêché de satisfaire la requête.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_État http \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



Le serveur ne prend pas en charge les fonctionnalités requises pour satisfaire la demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ passerelle incorrecte de l’État http \_**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



Le serveur, alors qu’il agit en tant que passerelle ou proxy, a reçu une réponse non valide du serveur en amont auquel il a accédé en tentant de répondre à la demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**\_service d’État http indisponible \_ \_**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



Le service est temporairement surchargé.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ \_ délai d’expiration de la passerelle d’État http**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



La demande a expiré lorsqu'elle attendait une passerelle.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_version d’État http \_ \_ non \_ sup.**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



Le serveur ne prend pas en charge ou refuse de prendre en charge la version du protocole HTTP qui a été utilisée dans le message de demande.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

