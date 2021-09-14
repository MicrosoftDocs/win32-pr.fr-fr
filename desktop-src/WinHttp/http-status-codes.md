---
description: Ces constantes et valeurs correspondantes indiquent les codes d’état HTTP renvoyés par les serveurs sur Internet.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Codes d’état HTTP (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008349"
---
# <a name="http-status-codes-winhttph"></a>Codes d’état HTTP (WinHTTP. h)

Ces constantes et valeurs correspondantes indiquent les codes d’état HTTP renvoyés par les serveurs sur Internet.

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

<span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**état \_ http \_ \_ multi- \_ État WebDAV**
</dt> <dd> <dl> <dt>

207
</dt> <dt>



Au cours d’une opération de création et de gestion de version (WebDAV) World Wide Web, il indique plusieurs codes d’État pour une seule réponse. Le corps de la réponse contient des Extensible Markup Language (XML) qui décrivent les codes d’État. Pour plus d’informations, consultez [Extensions http pour la création distribuée](../webdav/webdav-portal.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_État http \_ ambigu**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



La ressource demandée est disponible à un ou plusieurs emplacements.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_État http \_ déplacé**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



La ressource demandée a été affectée à un nouveau Uniform Resource Identifier permanent (URI), et toutes les références futures à cette ressource doivent être effectuées à l’aide de l’un des URI renvoyés.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**redirection HTTP \_ Status \_**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



La ressource demandée réside temporairement sous un autre URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_méthode de \_ redirection http status \_**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



La réponse à la demande se trouve sous un autre URI et doit être récupérée à l’aide d’un [*verbe http*](glossary.md) obtenir sur cette ressource.


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



La demande redirigée conserve le même [*verbe http*](glossary.md). Comportement HTTP/1.1.


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



Non implémenté dans le protocole HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_État http \_ interdit**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Le serveur a compris la demande, mais ne peut pas la traiter.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_État http \_ \_ introuvable**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Le serveur n’a trouvé rien qui correspond à l’URI demandé.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ méthode incorrecte de l’État http \_**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Le [*verbe http*](glossary.md) utilisé n’est pas autorisé.


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



Le serveur ne peut pas accepter la demande sans longueur de contenu définie.


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



Le serveur ne peut pas traiter la demande, car la taille de l’entité de la demande est supérieure à ce que le serveur est en mesure de traiter.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI d’État http \_ \_ trop \_ long**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Le serveur ne peut pas traiter la demande, car l’URI de la demande est plus long que ce que le serveur peut interpréter.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**état HTTP- \_ \_ SUPPORT non pris en charge \_**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Le serveur ne peut pas traiter la demande, car l’entité de la demande est dans un format non pris en charge par la ressource demandée pour la méthode demandée.


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



Le serveur ne prend pas en charge la version du protocole HTTP qui a été utilisée dans le message de demande.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>   |
| En-tête<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

