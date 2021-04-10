---
title: Tâches du serveur HTTP
description: En règle générale, les tâches du serveur HTTP sont exécutées dans un ordre spécifique. autrement dit, une tâche doit être terminée et la sortie obtenue avant le début de la tâche suivante.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- Tâches du serveur HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22455dbda21aca32b26f586eed6e51cef7509af2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675922"
---
# <a name="http-server-tasks"></a>Tâches du serveur HTTP

En règle générale, les tâches du serveur HTTP sont exécutées dans un ordre spécifique. autrement dit, une tâche doit être terminée et la sortie obtenue avant le début de la tâche suivante.

Une page de tâche est créée pour présenter un exemple de code sur les tâches spécifiques effectuées par une application serveur HTTP. Une page de tâches est un lien vers le fichier d’extension C de l’exemple de serveur HTTP. Quand vous installez le \\ Kit de développement logiciel (SDK) sur le lecteur c : d’un ordinateur local, l’exemple d’application de serveur complet est installé dans c : \\ Program Files \\ Microsoft SDK \\ Samples \\ netds \\ http \\ Server.

La liste suivante identifie les tâches du serveur HTTP :

-   [Initialiser le service HTTP](#initialize-the-http-service)
-   [Inscrire les URL à écouter](#register-the-urls-to-listen-on)
-   [Appeler la routine pour recevoir une demande](#call-the-routine-to-receive-a-request)
-   [Recevoir la demande](#receive-the-request)
-   [Gérer la requête HTTP](#handle-the-http-request)
-   [Envoyer la réponse HTTP](#send-the-http-response)
-   [Envoyer la réponse HTTP Après](#send-the-http-post-response)
-   [Nettoyer l’API du serveur HTTP](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Initialiser le service HTTP

Le service HTTP est initialisé à l’aide de la fonction [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) , et le descripteur de la file d’attente de demandes est créé à l’aide de [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Le serveur doit être initialisé avant de pouvoir appeler d’autres fonctions serveur. La file d’attente des demandes doit être créée pour que le service puisse inscrire des URL afin d’écouter les requêtes HTTP entrantes.

Pour plus d’informations et pour obtenir un exemple de code, consultez [initialiser le service http](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Inscrire les URL à écouter

Pour que l’API du serveur HTTP écoute les demandes entrantes, des URL spécifiques sont inscrites auprès de l’API en appelant la fonction [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . Les demandes entrantes qui correspondent à ces URL sont routées vers la file d’attente de demandes spécifiée dans cet appel.

Pour plus d’informations et pour obtenir un exemple de code, consultez [inscrire les URL à écouter](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Appeler la routine pour recevoir une demande

La fonction DoReceiveRequest alloue la mémoire tampon de la demande, initialise l’ID de la demande et démarre la boucle pour recevoir des demandes.

Pour plus d’informations et pour obtenir un exemple de code, consultez [appeler la routine pour recevoir une demande](http-server-sample-application.md).

## <a name="receive-the-request"></a>Recevoir la demande

L’API du serveur HTTP fournit une structure de demande pour stocker la demande entrante analysée. Cette structure est allouée par l’application et initialisée lors de la réception d’une demande entrante. L’application appelle la fonction [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) pour recevoir la demande. Si le tampon de demande est trop petit pour recevoir la demande, l’application peut augmenter la taille de la mémoire tampon et appeler à nouveau **HttpReceiveHttpRequest** pour recevoir la demande entière.

Pour plus d’informations et pour obtenir un exemple de code, consultez [receive a request](http-server-sample-application.md).

## <a name="handle-the-http-request"></a>Gérer la requête HTTP

L’exemple d’application montre comment gérer les verbes HTTP d’obtention et de requête après. L’application envoie une erreur 503 (**non \_ implémentée**) si les verbes sont présents dans la demande que l’application ne gère pas.

Notez que l’URL à utiliser pour la gestion des demandes est l’URL traitée contenue dans le membre **CookedUrl** de la structure de la [**\_ requête HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) . N’utilisez pas l’URL non traités dans le membre **pRawUrl** , qui est uniquement destiné au suivi et à des fins statistiques.

Pour plus d’informations et pour obtenir un exemple de code, consultez [gérer la requête http](http-server-sample-application.md).

## <a name="send-the-http-response"></a>Envoyer la réponse HTTP

La structure de la réponse est allouée et initialisée avec le code d’État et une phrase de raison dans la macro INITIALiser la \_ \_ réponse http. Un en-tête HTTP connu est ajouté à la structure de la réponse dans la \_ \_ macro ajouter un en-tête connu, et le corps d’entité est ajouté à la réponse à partir d’un bloc de données à partir de la mémoire. La fonction [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) est appelée pour envoyer la réponse. Dans cet exemple, l’application envoie une réponse simple 200 OK à la requête d’extraction.

Pour plus d’informations et pour obtenir un exemple de code, consultez [Envoyer une réponse http](http-server-sample-application.md).

## <a name="send-the-http-post-response"></a>Envoyer la réponse HTTP Après

La demande de publication requiert plus de traitement que la demande d’extraction. Le corps de l’entité de requête est reçu en appelant la fonction [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) . L’application envoie la réponse et le corps de l’entité de réponse dans des appels distincts à l’API du serveur HTTP. Les en-têtes de réponse sont envoyés avec le [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). Le corps d’entité est envoyé dans un bloc de données à partir d’un descripteur de fichier avec la fonction [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .

Pour plus d’informations et pour obtenir un exemple de code, consultez [Envoyer une réponse http après](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Nettoyer l’API du serveur HTTP

Les opérations de nettoyage pour l’API du serveur HTTP sont les suivantes :

-   Suppression de toutes les URL inscrites.
-   Fermeture du handle vers la file d’attente des demandes.
-   Fin des ressources créées par l’API du serveur HTTP.

L’application appelle la fonction [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) pour annuler l’inscription des URL inscrites par la fonction [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) initiale. L’application appelle également [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) pour chaque appel à [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) avec les paramètres d’indicateur correspondants. Cet appel met fin à toutes les ressources créées par l’appel à **HttpInitialize**.

Pour plus d’informations et pour obtenir un exemple de code, consultez [nettoyer l’API du serveur http](http-server-sample-application.md).

 

 




