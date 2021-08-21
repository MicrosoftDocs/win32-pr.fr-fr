---
title: Vue d’ensemble de l’API serveur HTTP
description: Cette rubrique identifie une séquence typique d’opérations qui utilisent l’API du serveur HTTP.
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d24defe190c073f7ca359309baf6731d466459d9bb7cfbd9ffc05268ded11ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150332"
---
# <a name="http-server-api-overview"></a>Vue d’ensemble de l’API serveur HTTP

La liste suivante identifie une séquence typique d’opérations qui utilisent l’API du serveur HTTP :

-   Initialisez l’API du serveur HTTP à l’aide de la fonction [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) .
-   Créez une file d’attente de demandes à l’aide de la fonction [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) .
-   Inscrire une ou plusieurs URL à l’aide de la fonction [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) .
-   Recevez les demandes entrantes dirigées vers les URL inscrites à l’aide de la fonction [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) et envoyez des réponses HTTP pour ces requêtes à l’aide de la fonction [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) .
-   Facultatif Lors de l’envoi d’une réponse, envoyez un corps d’entité supplémentaire à l’aide de la fonction [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .
-   Effectuez des opérations de nettoyage à l’aide des fonctions [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl), [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) et [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

Dans les opérations qui utilisent des URL, Notez qu’il s’agit de l’URL traitée contenue dans le membre **CookedUrl** de la structure de la [**\_ requête HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) qui doit être utilisée. N’utilisez pas l’URL non traités dans le membre **pRawUrl** , qui est uniquement destiné au suivi et à des fins statistiques.

Chaque application crée sa propre file d’attente de demandes. Une application obtient son descripteur de file d’attente de requêtes à partir de [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Il transmet ce handle à la fonction [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) pour ajouter une URL à la file d’attente de demandes. L’application reçoit la notification d’une demande entrante et la récupère à partir de la file d’attente des demandes en appelant la fonction [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) avec le descripteur de la file d’attente des demandes. Vous pouvez utiliser cette fonction pour recevoir les en-têtes de demande ou les en-têtes et le corps d’entité. [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) retourne également un identificateur de demande (RequestId) pour la demande reçue qui est unique pour le handle de demande.

> [!Note]  
> Il incombe à l’application d’examiner tous les en-têtes de requête pertinents, y compris les en-têtes Content-Negotiation s’ils sont utilisés, et de faire échouer les demandes en fonction du contenu d’en-tête. L’API du serveur HTTP garantit que chaque ligne d’en-tête est correctement terminée et ne contient pas de caractères non conformes.

 

Utilisez la fonction [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) avec le handle de la file d’attente des demandes pour récupérer les parties suivantes du corps d’entité d’une demande, le cas échéant.

> [!Note]  
> L’API du serveur HTTP décode les messages segmentés côté réception, mais n’effectue pas de codage mémorisé en bloc côté envoi. Si la segmentation est requise côté envoi, l’application doit l’implémenter. Pour plus d’informations sur l’encodage mémorisé en bloc, consultez [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

 

Utilisez la fonction [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) avec des applications qui traitent des URL à l’aide d’un schéma sécurisé («**https**») pour récupérer éventuellement les informations de certificat du client.

Les réponses sont envoyées avec la fonction [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) . Cette fonction utilise l’ID de requête de la demande correspondante pour envoyer la réponse. Une réponse peut être envoyée dans plusieurs appels d’API au fil du temps en appelant la fonction [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) avec RequestId à partir de la demande initialement reçue.

> [!Note]  
> Par défaut, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) utilise « Microsoft-HTTPAPI/1.0 » comme en-tête « Server : ». Si une application spécifie un en-tête de serveur dans une réponse, cette valeur est placée en tant que première partie de l’en-tête de serveur, suivie d’un espace, puis de « Microsoft-HTTPAPI/1.0 ».

 

En général, l’API du serveur HTTP masque les détails de la gestion des connexions et leur établissement et leur destruction à partir des applications. Toutefois, une application peut éventuellement détecter l’arrêt d’une connexion en appelant [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect).

Les applications doivent être nettoyées en procédant comme suit :

-   Lorsque l’application n’écoute pas ou ne répond pas à une URL, l’URL est supprimée à l’aide de la fonction [**HttpRemoveURL**](/windows/desktop/api/Http/nf-http-httpremoveurl) .
-   Lorsque l’application a terminé d’utiliser la file d’attente des demandes, fermez le handle de la file d’attente des demandes à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .
-   Lorsque l’application a terminé d’utiliser l’API du serveur HTTP, appelez la fonction [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

 

 