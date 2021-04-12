---
description: N’importe quel analyseur de paquets réseau pouvant afficher des paquets bruts peut être utilisé pour inspecter les paquets de WS-Discovery UDP. Moniteur réseau Microsoft 3 (NetMon) est recommandé. Pour plus d’informations sur NetMon, consultez le téléchargement de Netmon et des exemples de filtres DPWS.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Inspection des suivis réseau pour les WS-Discovery UDP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f4acd79588ef48c7f8e1ace2a44c9a3458475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203150"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Inspection des suivis réseau pour les WS-Discovery UDP

N’importe quel analyseur de paquets réseau pouvant afficher des paquets bruts peut être utilisé pour inspecter les paquets de WS-Discovery UDP. Moniteur réseau Microsoft 3 (NetMon) est recommandé. Pour plus d’informations sur NetMon, consultez le [téléchargement de Netmon et des exemples de filtres DPWS](downloading-netmon-and-sample-dpws-filters.md).

**Pour inspecter les suivis réseau pour la détection des services Web UDP**

1.  Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).
2.  Installez l’analyseur de paquets (NetMon) sur le client ou l’hôte.
3.  Configurez l’analyseur de paquets pour capturer le trafic sur la carte réseau qui connecte l’ordinateur hôte et le client.
4.  Reproduisez l’erreur en démarrant l’hôte et le client ou en appuyant sur F5 dans l’Explorateur réseau.
5.  Filtrez les résultats pour isoler WS-Discovery trafic. Pour afficher des exemples de filtres NetMon, consultez le [téléchargement de Netmon et des exemples de filtres DPWS](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Cette étape est facultative.

     

6.  Vérifiez que les messages envoyés entre le client et l’hôte répondent aux exigences de trafic de base.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Vérification de la conformité des messages aux exigences du trafic

Les clients et hôtes WSDAPI doivent envoyer des messages conformes aux critères suivants. Pour obtenir des informations générales sur les modèles de message, consultez [modèles de message d’échange de métadonnées et de découverte](discovery-and-metadata-exchange-message-patterns.md).

-   Les messages de [sondage](probe-message.md) doivent être envoyés par la multidiffusion UDP au port 3702.
-   L’élément **types** d’un message de [sondage](probe-message.md) doit être présent et ne doit pas être vide. Il doit contenir les types auxquels un hôte doit répondre.
-   Un message [messages ProbeMatches](probematches-message.md) doit être envoyé en monodiffusion au port UDP à partir duquel la [sonde](probe-message.md) a été envoyée.
-   L’élément **latesto** d’un message [messages ProbeMatches](probematches-message.md) doit être présent et ne doit pas être vide. Sa valeur doit correspondre à la valeur de l’élément **MessageID** du message de [sondage](probe-message.md) correspondant.
-   Si un élément **XAddrs** est inclus dans le message [messages ProbeMatches](probematches-message.md) , les adresses de transport fournies doivent être validées. Pour plus d’informations, consultez [règles de validation XAddr](xaddr-validation-rules.md).
-   Un message [messages ProbeMatches](probematches-message.md) doit être envoyé dans les 4 secondes du message de [sondage](probe-message.md) correspondant. Le pare-feu Windows peut supprimer un message messages ProbeMatches envoyé plus de 4 secondes après un message de sondage.
-   Si aucun élément **XAddrs** n’a été inclus dans le message [messages ProbeMatches](probematches-message.md) , et si le client ou l’hôte envoie un message http (par exemple, une [demande d’échange de métadonnées](get--metadata-exchange--http-request-and-message.md) ou un message de service), le client ou l’hôte doit envoyer un message de [résolution](resolve-message.md) par multidiffusion UDP au port 3702.
-   Si un message de [résolution](resolve-message.md) est envoyé, un message [ResolveMatches](resolvematches-message.md) doit être envoyé en monodiffusion au port UDP à partir duquel le message de résolution a été envoyé.
-   Un message [ResolveMatches](resolvematches-message.md) doit être envoyé dans les 4 secondes du message de [résolution](resolve-message.md) correspondant. Le pare-feu Windows peut supprimer un ResolveMatchesmessage envoyé plus de 4 secondes après un message de résolution.

Si les messages envoyés par le programme ne sont pas conformes à ces exigences de message, la cause du problème a été correctement identifiée et aucune autre étape de dépannage n’est nécessaire. Réécrivez le programme afin qu’il génère des messages conformes et retestez le programme.

Si la source du problème ne peut toujours pas être identifiée, contactez le support technique de Microsoft pour obtenir de l’aide. Avant de contacter le support technique, collectez les fichiers journaux appropriés afin d’identifier la cause racine du problème. Pour plus d’informations, consultez [activation du suivi wsdapi](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Téléchargement de Netmon et des exemples de filtres DPWS](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



