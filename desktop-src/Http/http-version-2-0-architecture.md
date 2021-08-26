---
title: Architecture (API serveur HTTP)
description: La session de serveur, la file d’attente des demandes et les objets de configuration de groupe d’URL permettent aux applications de configurer le service HTTP.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3905a27708c87c43e141dd4cf8d84b2f0e7e66bc4dd189440733321ee951a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997103"
---
# <a name="architecture-http-server-api"></a>Architecture (API serveur HTTP)

La session de serveur, la file d’attente des demandes et les objets de configuration de groupe d’URL permettent aux applications de configurer le service HTTP. Les propriétés définies sur ces objets remplacent les configurations par défaut de l’API du serveur HTTP.

-   Session serveur : objet de configuration de niveau supérieur qui définit des configurations pour tous les groupes d’URL créés dans le cadre de la session.
-   Groupe d’URL : le groupe d’URL, créé sous la session du serveur, contient un ensemble d’URL qui héritent des configurations définies sur la session serveur. Les configurations de groupe d’URL remplacent les configurations de session serveur quand elles sont définies par l’application. Le groupe d’URL définit une partie de l’espace de noms sur lequel l’application écoute et configure cette partie de l’espace de noms.
-   File d’attente des demandes : cet objet configure les paramètres spécifiques à la file d’attente des demandes. Ces configurations sont appliquées à toutes les URL dans les groupes associés à la file d’attente de demandes.

Le diagramme ci-dessous montre la relation entre les objets de configuration et l’application. En règle générale, une session de serveur unique est créée pour chaque application avec un ou plusieurs groupes d’URL créés sous celle-ci. Les files d’attente de demandes sont créées indépendamment du groupe d’URL ou de la session serveur. Les groupes d’URL doivent être associés à une file d’attente de demandes pour recevoir des demandes.

![relation entre les objets de configuration et l’application](images/architecture.png)

La fonctionnalité de file d’attente des demandes nommée de l’API du serveur HTTP version 2,0 permet à plusieurs processus de travail de recevoir des demandes sur une file d’attente de demandes. La file d’attente des demandes est créée par un processus de contrôleur qui identifie les processus de travail qui ont accordé l’accès à la file d’attente des demandes. Pour plus d’informations, consultez la rubrique [file d’attente des demandes nommées](named-request-queue.md) .

## <a name="property-configuration"></a>Configuration de la propriété

Pour plus d’informations sur la définition des propriétés sur les objets de configuration, consultez les rubriques suivantes :

-   [Configuration de la file d’attente des demandes](configuring-the-request-queue.md)
-   [Configuration de la session serveur](configuring-the-server-session.md)
-   [Configuration du groupe d’URL](configuring-the-url-group.md)

Le tableau suivant répertorie les propriétés définies sur les objets de configuration. Pour plus d’informations sur les configurations de propriétés, consultez la rubrique [Configuration des propriétés dans la version HTTP 2,0](configuring-properties-in-http-version-2-0.md) .



| Nom           | Propriété                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Session serveur | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| Groupe d’URL      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| File d'attente de requêtes  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





