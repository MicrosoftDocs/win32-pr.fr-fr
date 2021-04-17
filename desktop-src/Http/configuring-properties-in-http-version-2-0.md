---
title: Configuration des propriétés
description: Configuration des propriétés
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f898467f92f669596b4a8b1a4e68581c343ea883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379915"
---
# <a name="configuring-properties"></a>Configuration des propriétés

L’API de la version 2,0 du serveur HTTP permet aux applications de configurer manuellement les files d’attente de demandes, les sessions serveur et les groupes d’URL. La session serveur est l’objet de niveau supérieur qui contient des informations de configuration qui s’appliquent à tous les groupes d’URL créés sous eux. L’application crée une session de serveur avec un ou plusieurs groupes d’URL sous celle-ci, puis associe le groupe d’URL à une file d’attente de demandes.

Pour plus d’informations sur les objets de configuration spécifiques de l’API de la version 2,0 du serveur HTTP, consultez :

-   [Configuration de la session serveur](configuring-the-server-session.md)
-   [Configuration du groupe d’URL](configuring-the-url-group.md)
-   [Configuration des timers larges de l’API du serveur HTTP](configuring-the-http-server-api-wide-timers.md)

Les propriétés des objets de configuration sont définies avec [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) et [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) , comme indiqué dans le diagramme ci-dessous. L’association entre la file d’attente des demandes et le groupe d’URL peut être modifiée à la demande, alors que l’association entre la session du serveur et les groupes d’URL ne peut pas être modifiée. Les groupes d’URL doivent être associés à une file d’attente de demandes pour recevoir des demandes.

![Propriétés des objets de configuration](images/configpropinv2.png)

Le tableau suivant répertorie les propriétés qui peuvent être définies sur chaque objet de configuration. En général, si aucune configuration de propriété n’est définie par l’application, les configurations par défaut de l’API du serveur HTTP s’appliquent. Les propriétés de configuration définies par l’application sur la session serveur remplacent les configurations à l’ensemble de l’API du serveur HTTP. Les configurations définies sur le groupe d’URL remplacent les configurations de session du serveur et les configurations de la file d’attente des demandes remplacent les configurations par défaut de l’API du serveur HTTP.



| Objet Configuration | Propriété                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Session serveur       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| Groupe d’URL            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| File d'attente de requêtes        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

Les propriétés de la session serveur sont définies dans l’énumération des [ \_ \_ Propriétés du serveur http](/windows/desktop/api/Http/ne-http-http_server_property) . Le tableau suivant répertorie les structures de propriété qui sont définies pour chaque type de propriété et l’API du serveur HTTP par défaut lorsque ces propriétés ne sont pas définies par l’application.



| Propriété                                                    | Structure                                                                     | API du serveur HTTP par défaut    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**\_ \_ informations d’authentification du serveur http \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Aucune authentification          |
| HttpServerLoggingProperty                                   | [**\_informations de journalisation http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Aucune journalisation                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**\_informations de \_ limite de connexion http \_**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Aucune limite                   |
| HttpServerTimeoutsProperty                                  | [**\_ \_ informations sur la limite du délai d’expiration http \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 s.                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**\_ \_ informations sur la limite de bande PASSANTe http \_**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Aucune limite                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1 000                       |
| HttpServerStateProperty                                     | [**\_informations d’État http \_**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | activé                    |
| HttpServer503VerbosityProperty                              | [**Commentaires sur la \_ réponse HTTP 503 \_ \_**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**\_informations de liaison http \_**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | Aucun                       |



 

Le tableau suivant répertorie les valeurs minimale et maximale pour les configurations de l’API du serveur HTTP.



| Propriété                                              | API serveur HTTP maximale et minimale                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | Min = minimum \_ autorisé \_ taux de limitation de bande passante \_ \_ Max = aucun |
| HttpServerQueueLengthProperty                         | Min = 0xA Max = 0xFFFF                                     |



 

 

 




