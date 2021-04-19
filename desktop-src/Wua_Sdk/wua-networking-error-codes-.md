---
description: 'En savoir plus sur : codes d’erreur de mise en réseau WUA'
ms.assetid: 07ff2ed7-09bc-4af7-84f9-66a921c0f53f
title: Codes d’erreur de mise en réseau WUA (Wuerror. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fb2c027939afda3fe5817a8a860469fc90b766
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545572"
---
# <a name="wua-networking-error-codes"></a>Codes d’erreur de mise en réseau WUA

L’API Windows Update Agent (WUA) peut retourner les codes d’erreur suivants lors de l’exécution d’opérations réseau telles que la recherche de mises à jour :



| Constante/valeur                                                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WU_E_WINHTTP_INVALID_FILE"></span><span id="wu_e_winhttp_invalid_file"></span><dl> <dt>**Wu \_ E \_ \_ \_ fichier 0x80240038 non valide pour WinHTTP**</dt> <dt></dt> </dl>                                  | Le fichier téléchargé possède un type de contenu inattendu.<br/>                                                                                                                               |
| <span id="WU_E_PT_HTTP_STATUS_BAD_REQUEST"></span><span id="wu_e_pt_http_status_bad_request"></span><dl> <dt>**Wu \_ E \_ PT \_ État http de la \_ \_ \_ Demande incorrecte**</dt> <dt>0x80244016</dt> </dl>              | Identique à l’état HTTP 400 – le serveur n’a pas pu traiter la requête en raison d’une syntaxe non valide.<br/>                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_DENIED"></span><span id="wu_e_pt_http_status_denied"></span><dl> <dt>**Wu \_ \_ \_ État http E \_ PT \_ refusé**</dt> <dt>0x80244017</dt> </dl>                              | Identique à l’état HTTP 401 – la ressource demandée nécessite l’authentification de l’utilisateur.<br/>                                                                                                    |
| <span id="WU_E_PT_HTTP_STATUS_FORBIDDEN"></span><span id="wu_e_pt_http_status_forbidden"></span><dl> <dt>**Wu \_ \_ \_ État http E \_ PT \_ interdit**</dt> <dt>0x80244018</dt> </dl>                     | Identique à l’état HTTP 403 – le serveur a compris la demande, mais refuse de la traiter.<br/>                                                                                              |
| <span id="WU_E_PT_HTTP_STATUS_NOT_FOUND"></span><span id="wu_e_pt_http_status_not_found"></span><dl> <dt>**Wu \_ \_ \_ État http E \_ PT \_ \_ introuvable**</dt> <dt>0x80244019</dt> </dl>                    | Identique à l’état HTTP 404 – le serveur ne parvient pas à trouver l’URI demandé (Uniform Resource Identifier).<br/>                                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_BAD_METHOD"></span><span id="wu_e_pt_http_status_bad_method"></span><dl> <dt>**Wu \_ E \_ PT \_ État http de la \_ \_ \_ méthode incorrecte**</dt> <dt>0x8024401A</dt> </dl>                 | Identique à l’état HTTP 405 – la méthode HTTP n’est pas autorisée.<br/>                                                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="wu_e_pt_http_status_proxy_auth_req"></span><dl> <dt>**Wu \_ \_Demande d' \_ \_ authentification du \_ proxy \_ \_ d’État http E PT**</dt> <dt>0x8024401B</dt> </dl>    | Identique à l’état HTTP 407 – l’authentification proxy est requise.<br/>                                                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="wu_e_pt_http_status_request_timeout"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ \_ Délai d’expiration de la demande d’État http E PT**</dt> <dt>0x8024401C</dt> </dl>  | Identique à l’état HTTP 408 – le serveur a dépassé le délai d’attente de la demande.<br/>                                                                                                           |
| <span id="WU_E_PT_HTTP_STATUS_CONFLICT"></span><span id="wu_e_pt_http_status_conflict"></span><dl> <dt>**Wu \_ 0x8024401D \_ \_ conflit d' \_ état \_ http E PT**</dt> <dt></dt> </dl>                        | Identique à l’état HTTP 409 – la demande n’a pas été effectuée en raison d’un conflit avec l’état actuel de la ressource.<br/>                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_GONE"></span><span id="wu_e_pt_http_status_gone"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ État http E PT**</dt> <dt>0x8024401E</dt> </dl>                                    | Identique à l’état HTTP 410 – la ressource demandée n’est plus disponible sur le serveur.<br/>                                                                                                |
| <span id="WU_E_PT_HTTP_STATUS_SERVER_ERROR"></span><span id="wu_e_pt_http_status_server_error"></span><dl> <dt>**Wu \_ \_Erreur du \_ \_ serveur d' \_ \_ État http E PT**</dt> <dt>0x8024401F</dt> </dl>           | Identique à l’état HTTP 500 – une erreur interne au serveur a empêché la réalisation de la demande.<br/>                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_NOT_SUPPORTED"></span><span id="wu_e_pt_http_status_not_supported"></span><dl> <dt>**Wu \_ \_ \_ État http E \_ PT \_ non \_ pris en charge**</dt> <dt>0x80244020</dt> </dl>        | Identique à l’état HTTP 501 – le serveur ne prend pas en charge les fonctionnalités requises pour satisfaire la demande. <br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_BAD_GATEWAY"></span><span id="wu_e_pt_http_status_bad_gateway"></span><dl> <dt>**Wu \_ \_ \_ État http E \_ PT \_ \_ passerelle incorrecte**</dt> <dt>0x80244021</dt> </dl>              | Identique à l’état HTTP 502 – le serveur, alors qu’il agit en tant que passerelle ou proxy, a reçu une réponse non valide du serveur en amont auquel il a accédé en tentant de répondre à la demande.<br/> |
| <span id="WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="wu_e_pt_http_status_service_unavail"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ service d’État http \_ \_ indispo**</dt> <dt>0x80244022</dt> </dl>  | Identique à l’état HTTP 503 : le service est temporairement surchargé.<br/>                                                                                                                  |
| <span id="WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="wu_e_pt_http_status_gateway_timeout"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ \_ Délai d’expiration de la passerelle d’État http E PT**</dt> <dt>0x80244023</dt> </dl>  | Identique à l’état HTTP 504 – la demande a dépassé le délai d’attente d’une passerelle.<br/>                                                                                                        |
| <span id="WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP"></span><span id="wu_e_pt_http_status_version_not_sup"></span><dl> <dt>**Wu \_ E \_ PT \_ \_ État http \_ version \_ non \_ sup**</dt> <dt>0x80244024</dt> </dl> | Identique à l’état HTTP 505 – le serveur ne prend pas en charge la version du protocole HTTP utilisée pour la demande.<br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_NOT_MAPPED"></span><span id="wu_e_pt_http_status_not_mapped"></span><dl> <dt>**Wu \_ \_ \_ État http E \_ PT \_ non \_ mappé**</dt> <dt>0x8024402B</dt> </dl>                 | La demande n’a pas pu être effectuée et la raison ne correspondait à aucun des \_ \_ codes d' \_ erreur http Wu E PT \_ \* .<br/>                                                               |
| <span id="WU_E_PT_WINHTTP_NAME_NOT_RESOLVED"></span><span id="wu_e_pt_winhttp_name_not_resolved"></span><dl> <dt>**Wu \_ \_ \_ Nom WinHTTP E \_ PT \_ non \_ résolu**</dt> <dt>0x8024402C</dt> </dl>        | Identique au \_ nom WinHTTP d’erreur \_ \_ non \_ résolu-le nom du serveur proxy ou du serveur cible ne peut pas être résolu.<br/>                                                                          |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wuerror. h</dt> </dl> |



 

 




