---
description: En savoir plus sur l’inspection des suivis réseau pour l’échange de métadonnées HTTP. Utilisez un analyseur de paquets réseau qui affiche des paquets bruts.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Inspection des suivis réseau pour l’échange de métadonnées HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e653b0852f84382873973cd63fbd3223a245dd4
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262681"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Inspection des suivis réseau pour l’échange de métadonnées HTTP

N’importe quel analyseur de paquets réseau pouvant afficher des paquets bruts peut être utilisé pour inspecter les demandes d’échange de métadonnées HTTP. Moniteur réseau Microsoft 3 (NetMon) est recommandé. Pour plus d’informations sur NetMon, consultez le [téléchargement de Netmon et des exemples de filtres DPWS](downloading-netmon-and-sample-dpws-filters.md).

Cette procédure de diagnostic peut ne pas être aussi utile pour les clients et les hôtes utilisant un canal sécurisé pour les communications, car le contenu du message est chiffré.

**Pour inspecter les traces réseau pour l’échange de métadonnées HTTP**

1.  Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).
2.  Installez l’analyseur de paquets (NetMon) sur le client ou l’hôte.
3.  Configurez l’analyseur de paquets pour capturer le trafic sur la carte réseau qui connecte l’ordinateur hôte et le client.
4.  Reproduisez l’erreur en démarrant l’hôte et le client ou en appuyant sur F5 dans l’Explorateur réseau.
5.  Filtrez les résultats pour isoler les WS-Discovery et le trafic d’échange de métadonnées. Pour afficher des exemples de filtres NetMon, consultez le [téléchargement de Netmon et des exemples de filtres DPWS](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Cette étape est facultative.

     

6.  Vérifiez que les messages envoyés entre le client et l’hôte répondent aux exigences de trafic de base.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Vérification de la conformité des messages aux exigences du trafic

Les clients et hôtes WSDAPI doivent envoyer des messages conformes aux critères suivants. Pour obtenir des informations générales sur les modèles de message, consultez [modèles de message d’échange de métadonnées et de découverte](discovery-and-metadata-exchange-message-patterns.md).

-   Les messages doivent respecter les exigences de trafic fournies dans la rubrique [inspection des suivis réseau pour UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md), à moins qu’il soit absolument certain que WS-Discovery n’est pas utilisé pour l’échange de métadonnées.
-   Une connexion TCP doit être établie entre le client et la première adresse de transport fournie dans l’élément **XAddrs** d’un message [messages ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) . La liste suivante montre un échange de paquets standard utilisé pour établir une connexion TCP.
    -   Le client envoie un paquet TCP SYN à l’hôte sur un port spécifié.
    -   L’hôte envoie un paquet TCP SYN/ACK au client.
    -   Le client envoie un paquet TCP ACK à l’hôte sur un port spécifié.

    Une fois que le client a envoyé un paquet TCP ACK, la connexion TCP est établie. Notez que cet échange de messages ne se produira pas si une connexion TCP a déjà été établie.
-   Le client doit envoyer une requête et un message http de [récupération](get--metadata-exchange--http-request-and-message.md) valides.
-   L’hôte doit être à l’écoute sur le chemin d’URL spécifié dans la requête HTTP [obtenir](get--metadata-exchange--http-request-and-message.md) .
-   L’élément **to** d’un message d' [extraction](get--metadata-exchange--http-request-and-message.md) de métadonnées doit être présent et non vide. La valeur de l’élément **à** doit correspondre à l’une des adresses de point de terminaison de l’hôte. L’adresse de point de terminaison d’un hôte est généralement publiée dans un message [messages ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) .
-   L’hôte doit envoyer un en-tête de réponse HTTP valide. Si la demande initiale a réussi, l’en-tête de réponse doit contenir le code d’état HTTP/1.1 200.
-   L’hôte doit envoyer un message [GetResponse](getresponse--metadata-exchange--message.md) valide.
-   L’élément **latesto** d’un message [GetResponse](getresponse--metadata-exchange--message.md) doit être présent et ne doit pas être vide. Sa valeur doit correspondre à la valeur de l’élément **MessageID** à partir du message d' [extraction](get--metadata-exchange--http-request-and-message.md) correspondant.

Si les requêtes HTTP ou les messages d’échange de métadonnées envoyés par le programme ne sont pas conformes à ces exigences de trafic, la cause du problème a été correctement identifiée et aucune étape de dépannage supplémentaire n’est nécessaire. Réécrivez le programme afin qu’il génère des messages et des demandes conformes et retestez le programme.

Si la source du problème ne peut toujours pas être identifiée, contactez le support technique de Microsoft pour obtenir de l’aide. Avant de contacter le support technique, collectez les fichiers journaux appropriés afin d’identifier la cause racine du problème. Pour plus d’informations, consultez [activation du suivi wsdapi](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Téléchargement de Netmon et des exemples de filtres DPWS](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



