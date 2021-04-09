---
title: Traitement des requêtes
description: Le traitement des demandes comprend quatre étapes.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103869346"
---
# <a name="processing-requests"></a>Traitement des requêtes

Le traitement des demandes comprend quatre étapes :

-   Réception d’une demande
-   Gestion de la demande
-   Envoi de la réponse
-   Annulation des demandes qui ne peuvent pas être traitées

![Diagramme qui affiche la boucle de demande de processus.](images/processloop.png)

## <a name="receiving-a-request"></a>Réception d’une demande

L’API du serveur HTTP fournit une structure de demande pour stocker la demande entrante analysée. Cette structure est allouée par l’application et initialisée lors de la réception d’une demande entrante. L’application appelle la fonction [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) pour recevoir la demande. Si le tampon de demande est trop petit pour recevoir la demande, l’application peut augmenter la taille de la mémoire tampon et appeler à nouveau **HttpReceiveHttpRequest** pour recevoir la demande entière.

Si la demande comprend des données de corps d’entité à recevoir, les applications appellent [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) avec l’ID de demande retourné dans le paramètre *pRequestBuffer* pendant l’appel à [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).

## <a name="handling-the-request"></a>Gestion de la demande

L’application effectue le traitement propre à l’application de la demande et formule une réponse. L’API du serveur HTTP n’impose aucun délai d’attente sur ce processus.

## <a name="sending-the-response"></a>Envoi de la réponse

Lorsque l’application a terminé la gestion de la demande et en élaborant la réponse, elle appelle la fonction [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) pour envoyer la réponse. Si la réponse comprend des données de corps d’entité à envoyer, l’application appelle également [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

## <a name="canceling-requests"></a>Annulation des demandes

Une fois que l’application a reçu un ID de demande de son appel à [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), elle peut annuler la demande à tout moment en appelant [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).

 

 




